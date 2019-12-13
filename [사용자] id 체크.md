**id 체크**
----
    
    특정 oauth id 가 이미 가입되어 있는지 확인합니다.
    
* **URL**

  /user/oauth_id/check

* **Method:**
  
  | `GET` |
  
*  **URL Params**

   type : GOOGLE, FACEBOOK, KAKAO 중 택1
   party_id : 해당 oauth_id

   **Optional:**
 
   N/A

* **Data Params**
    


* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```json
    {
      "okay": true
    }
    ```
    okay 가 true 라면 가입한 적이 없습니다.
    false 라면 중복 id 가 존재합니다.
 
* **Error Response:**

  * **Code:** HTTP_400_BAD_REQUEST <br />
    **Content:** `{ "okay" : false,  "msg":"Unknown oauth party" }`
    **Cause:** type이 이상할때

* **Sample Call:**

* **Notes:**

