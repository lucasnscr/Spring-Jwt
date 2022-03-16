# Spring-Jwt

### **Project description**
This project implementing REST API authentication using JWT(Json Web Token), this token is used for identify users at the the moment to request. Spring Security used for provider authorization and authentication layer and MongoDB for persist User in Database.


[For more details to the implementation 
](https://dev.to/lucasnscr/explaining-jwt-with-spring-and-mongodb-26ln)


## **Installation and  Technologies**

The following technologies were used to carry out the project and it is necessary to install some items:

- Docker
- Java
- Maven
- SpringBoot
- Spring Security
- MongoDB
- JWT

### **Jwt**

JWT is an open standard (RFC 7519) that is a good way to exchange information securely as JSON objects between different parties. JWT is very popular in the microservice world and it is widely used in the authorization process in web apps. JWT can send via URL, POST request, HTTP header and it is very fast.

Let’s see what is authorization because you might have some doubts difference between authentication and authorization. In authentication process checks the identity of the user to provide them access to the system, simply checks who are you (By checking username, passwords, or any other methods). Usually, this process is done before authorization. In authorization process verifies whether access is allowed through policies and rules. Usually done after successful authentication.

We can use JWT to implement the authorization process in our application because nowadays JWT is widely used for the authorization process. I have implemented this process with JWT in this blog. Apart from authorization, we can use JWT for information exchanges because we can exchange information very securely using JWT.

### **Structure JWT**

The structure to the JWT is divided in three parts and parts separated by dots: Header, Payload and Signature.

Header: It contains signing algorithm like SHA256.
Payload: It contains our user data.
Signature: To verify the message wasn’t changed along the way, making it secure.


![jwt example](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5vrmuyeyfpzgbk90tw1t.jpeg)


Each part that composes to the real JWT. 

![illustration to the JWT and](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/apwyikymn7fzrv44rc1f.jpeg)

### **How to Works JWT**

![Using JWT](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i8edxaog6wp9d4pnb7p8.png)

You can understand clearly how the authorization process works with JWT from the above diagram. When you log in to the application you need to give your login credentials (Username, Password). After that server generates a JWT. Then that JWT will send to the browser and then the JWT is re-sent to the server with an authorization header. Then check the JWT signature and get user credentials from encoded JWT. If user details are correct send the required response to the user. That is how simply JWT works in the authorization process.


