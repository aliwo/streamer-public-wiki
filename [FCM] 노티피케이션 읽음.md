**노티피케이션 읽음**
----
  노티피케이션 읽음.
  자신이 받은 모든 노티피케이션의 read 를 true 로 바꿉니다.
  <br> 2020-04-16 한 개의 노티피케이션만 읽음 처리하는 기능이 추가 되었습니다. notification_id 를 지정하면 되용

* **URL**

  /notification/read <br>
  /notification/<int:notification_id>/read

* **Method:**
  
  | `PUT` |
  
*  **URL Params** 

   **Required:**
 
   N/A

   **Optional:**
 
   N/A

* **Data Params**

* **Success Response:**
  

  * **Code:** 200 <br />
    **Content:** 
    ```json
    { "okay": true }
    ```
    
    
* **Error Response:**

* **Sample Call:**

* **Notes:**


