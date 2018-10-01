***API Authentication***


**Sign Up**
----
  Returns user data in json if valid credentials.

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

  * **Code:** 403 FORBIDDEN <br />
    **Content:** `{ "error" : "Email is already in used" }`

  OR

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `VALIDATION ERROR`


**Sign In**
----
  Returns json web token if valid credentials.

* **URL**

  https://apiauthentication.herokuapp.com/users/signin

* **Method:**

  `POST`

* **Data Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJBdXRoIiwic3ViIjoiNWJiMTM4ZmRlZjM2MDM2MDc0ZmUwZTFlIiwiaWF0IjoxNTM4MzY3NDQ5MzIwLCJleHAiOjE1Mzg0NTM4NDkzMjB9.cvHccUvqznZWY5HGsAVhculoUEbIkd5F7ulUHoTXDTI"} }`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `Unauthorized`

  OR

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `VALIDATION ERROR`



**Secret**
----
  Returns resources if valid credentials.

* **URL**

  https://apiauthentication.herokuapp.com/users/secret

* **Method:**

  `GET`

* **Header**
 
   `Authorizatoin=[Valid Token]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "secret": "resource" }`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `Unauthorized`
