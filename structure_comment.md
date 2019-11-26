
```json
{
  "id": 4, 
  "user_id": 11, 
  "body": "이거슨 방명록 댓글이야", 
  "author_id": 12, 
  "parent_id": 2, 
  "created_at": "2019-06-10 11:09:28", 
  "secret": true, 
  "censored": null, 
  "likes": 0,
  "children_cnt": 0,
  "document_id": 3,
  "author": {
                "id": 2,
                "google_id": 2,
                "google_email": "ridickle7@gmail.com",
                "name": "Sang Woo Lee",
                "intro": "가나다라마",
                "google_picture": "https://lh5.googleusercontent.com/-3JsMq9XkqXc/AAAAAAAAAAI/AAAAAAAADW0/D4SdFW0dpS0/photo.jpg",
                "background_image": null,
                "fcm_token": null,
                "followers": 0,
                "phone_registered": true,
                "last_access": "2019-08-12 15:01:25",
                "registered_at": "2019-06-27 19:43:35",
                "phone": "01089077586"
  }
}

```

parent_id 는 부모가 되는 댓글의 id 입니다.
(parent_id 가 있는 것은 답글, 없는 것은 댓글입니다.)
children_cnt 는 자식의 개수입니다. (답글의 개수)
censored 가 true 라면 관리자에 의해 검열된 댓글입니다!

author 는 리스트 '조회' 시에 부착됩니다. 
/comment/user/<int:user_id>
/comment/user/children/<int:comment_id> 등등등...
