***API Authentication***


**Sign Up**
----
  Returns json web token if valid credentials.

* **URL**

  https://apiauthentication.herokuapp.com/users/signup

* **Method:**

  `POST`

* **Data Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "newUser" : {
      "_id":"5bb19d3bfa63315d1099388c",
      "email":"hjpolisticaaoo@gmail.com",
      "password":"$2a$10$o1hyTw82lV9SKuma0Ip1UuCBEJFmrnEa3UcELOfbcIcO3JriwjL/e",
      "__v":0 } }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ "error" : "Email is already in used" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `VALIDATION ERROR`