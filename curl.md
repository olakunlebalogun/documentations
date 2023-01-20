# Using curl to Make RESTful API Requests

## Format
`curl <options> <url>`

## Options  
-d, --data:     To pass data to a **POST** or **PUT** request    
e.g   
`curl -X POST --data '{"name":"Subtle Act of not giving a Fuck","author":"Mark Mason","price":350}' -H 'content-type:application/json' http://localhost:9000/book/add`  
  
Alternatively, you can import a file with the data with .json extension. To do that, use  
`curl -X POST -H 'Content-Type: application/json' -d @book.json http://localhost:9000/book/add`

---

-H:     To pass headers  
This helps to set the http headers e.g  
`-H 'Content-Type: application/json'` for single header or  `-H 'Content-Type: application/json'  -H 'Accept-Charset: UTF-8'`   

Logging in with username and password  
`curl --user baeldung:secretPassword http://example.com`

For authentication `curl -H "Authorization: Basic <ACCESS_TOKEN>" http://www.example.com`  

Bearer Authentication
`curl -H "Authorization: Bearer <ACCESS_TOKEN>" http://www.example.com`  
Auth2 Authentication
`curl -H "Authorization: OAuth <ACCESS_TOKEN>" http://www.example.com`  
Basic Authentication  
`curl -H "Authorization: Basic <ACCESS_TOKEN>" http://www.example.com`  


---
-X:     To specify the request type e.g **POST**,**PUT**,**DELETE**, **GET**

---

> Note:   
> - All commands must be on a continuous line, if it needs to be formatted then backward slashes(\\) to format.  
> - Also, the URL **must**  start with *http://* or *https://* e.g http://localhost:8080


