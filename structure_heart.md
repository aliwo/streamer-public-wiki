```json
{
    "id": 17,
    "from": 3,
    "to": 4,
    "clip_id": 2,
    "amount": 30,
    "type": "USER",
    "created_at": "2019년 11월 24일",
    "created_at_full": "YYYY-MM-DD HH:MM:SS",
    "tag": "GIVE"
}
```

타입은 이 하트변동이 왜 일어났냐! 를 설명해 줍니다. <br>
타입의 종류는... <br>
TYPE_USER = 'USER' # 유저끼리의 교환 <br>
TYPE_RECHARGE = 'RECHARGE' # 충전 <br>
TYPE_WITHDRAW = 'WITHDRAW' # 출금 <br>
TYPE_GIVE = 'GIVE' # 관리자가 하트를 적선. <br>
TYPE_TAKE = 'TAKE' # 관리자가 강제로 뺏은 경우 <br>
TYPE_REFUND = 'REFUND' # 하트 환전요청으로 인한 하트 감소 <br>
TYPE_REJECT = 'REJECT' # 하트 환전요청 거절로 인한 하트 증가 <br>

태그는 이 하트가 '나'(하트 내역을 요청하는 사람)을 기준으로
하트를 누구한테 준 것이냐, 아니면 충전을 한 것이냐 등등의 정보를 알려줍니다. <br>
태그의 종류는... <br>
GIVE <br>
RECHARGE <br>
WITHDRAW <br>
RECEIVE <br>

# 하트 경우의 수 정리

## 먼저 현재 태그를 정하는 기준은 다음과 같습니다.
(내 id => 하트 내역을 요청하는 유저의 id)
from 값이 내 id 인 경우 -> 무조건 GIVE 태그
to 값이 내 id 인데...
타입이 RECHARGE 라면-> RECHARGE
타입이 WITHDRAW 라면 -> WITHDRAW (이건 버그인거 같음...) 
해당 안되면 나머지는 모두 -> RECEIVE

## 하트 경우의 수

하트가 + 됨
(받은 하트) 특정 유저에게 하트를 받음 (type = USER tag = RECEIVE) 
(충전 하트) 내 하트를 충전 (type = RECHARGE tag = RECHARGE)
(충전 하트) 관리자가 충전 하트를 주는 경우 (type = GIVE_RECHARGE tag = RECHARGE)
(받은 하트) 하트 환전 거절로 인한 증가 (type = WITHDRAW_REJECT tag = RECEIVE)
(받은 하트) 관리자가 받은 하트를 주는 경우 (type = GIVE_RECEIVE tag = RECEIVE)

하트가 -됨
(충전 하트) 특정 유저에게 하트를 보냄 (type = USER tag = GIVE)
(충전 하트) 하트 환불 완료 (type = REFUND tag = GIVE)
(충전 하트) 관리자가 충전 하트를 뺏는 경우 (type = TAKE_RECHARGE tag = GIVE)
(받은 하트) 하트 환전 성공으로 인한 회수 (type = WITHDRAW_APPROVE tag = GIVE)
(받은 하트) 관리자가 받은 하트를 뺏는 경우 (type = TAKE_RECEIVE tag = GIVE)

## 하트 경우의 수

하트가 + 됨
특정 유저에게 하트를 받음 (type = USER tag = RECEIVE) 
내 하트를 충전 (type = RECHARGE tag = RECHARGE)
관리자가 하트를 주는 경우 (type = GIVE tag = RECEIVE)
하트 환전 거절로 인한 하트 증가 (type = WITHDRAW_REJECT tag = RECEIVE)


하트가 -됨
특정 유저에게 하트를 보냄 (type = USER tag = GIVE)
하트 환불 완료 (type = REFUND tag = GIVE)
관리자가 하트를 뺏는 경우 (type = TAKE tag = GIVE)
하트 환전 성공으로 인한 회수 (type = WITHDRAW_APPROVE tag = GIVE)
