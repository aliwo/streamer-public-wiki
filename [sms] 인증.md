**인증**
----
  sms 인증

* **URL**

  /sms/auth

* **Method:**
  
  | `POST` |
  
*  **URL Params** 

   **Required:**
 
   N/A

   **Optional:**
 
   N/A

* **Data Params**

  ```json
    {
        "auth_key": "e75fb03b-83ac-4aff-89b3-bf3e9458cdb1",
        "auth_value": "625382",
        "phone_num": "01022380476"
    }
  ```
    인증에 성공하면 user 의 phone 에 핸드폰 번호가 등록되며
    phone_registered 가 true 가 됩니다.
    
* **Success Response:**
  

  * **Code:** 200 <br />
    **Content:** `{ "okay": true }`
 
* **Error Response:**

* **Sample Call:**

* **Notes:**

