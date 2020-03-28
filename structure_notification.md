```json
{
            "id": 55,
            "author_id": 7,
            "target_user_id": 2,
            "created_at": "2019-08-20 13:49:00",
            "read": true,
            "body": {
                "kind": "CLIP_COMMENT_RECEIVED",
                "title": "smen 님이 회원님의 게시물에 댓글을 남겼습니다.",
                "clip_id": "32",
                "user_id": "7",
                "document_id": "225"
            },
            "fire": true,
            "author": {
                "user": "유조 구조 참조!"
            },
            "clip": {
              "clip" : "클립 구조 참조!"
            }
}

```

fire 는 실제 fcm 이 문제없이 notify 되었다면 true.
FCM 토큰이 없다거나 하는 문제가 발생했다면 false 입니다.

다음과 같은 kind 가 있습니다!

HEART_RECEIVED <br>
LIKE_RECEIVED <br>
CLIP_COMMENT_RECEIVED <br>
CHILD_CLIP_COMMENT_RECEIVED <br>
USER_COMMENT_RECEIVED <br>
CHILD_USER_COMMENT_RECEIVED <br>
ANNOUNCEMENT <br>
FOLLOW <br>

