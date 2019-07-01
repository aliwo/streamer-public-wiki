**인증번호 요청**
----
  인증번호 요청

* **URL**

  /sms/send

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
          "phone_num": "01022380476"
      }
  ```

* **Success Response:**
  

  * **Code:** 200 <br />
    **Content:** `{ "okay": true "auth_key" : "e75fb03b-83ac-4aff-89b3-bf3e9458cdb1" }`
 
* **Error Response:**

* **Sample Call:**

* **Notes:**

