**하트 출금 요청**
----
  
  하트를 출금해 달라는 요청을 보냅니다.

* **URL**

  /heart/request/withdraw

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
        "amount": 30000
      }
    ```

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:**
    ```json
        {
           "okay": true,
           "id" : 30
        }
    ```
 
* **Error Response:**

* **Sample Call:**


* **Notes:**
    마지막 점검일: 2019-07-23
