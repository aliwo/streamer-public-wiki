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
