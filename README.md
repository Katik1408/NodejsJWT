# NodejsJWT
This is the JWT Token Generation Code using Nodejs and Mongo DB at the backend. Main Source is this link 
https://jasonwatmore.com/post/2018/06/14/nodejs-mongodb-simple-api-for-authentication-registration-and-user-management


# Install the packages 
Use command
npm install


# Create a Database named as node-mongo-registration-login-api
# Create a collection name as users


# Requests

After You see successful message on Terminal as 
Server listening on port 4000

Then go to PostMan and fire the post request with the below URL

http://localhost:4000/users/register
and in body provide the following json data

{
    "firstName": "Kartik",
    "lastName": "Saxena",
    "username": "katik93",
    "password": "my-super-secret-password"
}

After creation of Data in MongoDb

Call the other Authenticate API using below URL in PostMan using POST Request Type
http://localhost:4000/users/authenticate 

and pass the following data 
{
    "username": "katik93",
    "password": "my-super-secret-password"
}

After this you will get a token in response like below

{
    "firstName": "Kartik",
    "lastName": "Saxena",
    "username": "katik93",
    "createdDate": "2021-04-17T08:18:39.296Z",
    "id": "607a99df8a471a6a4027a571",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiI2MDdhOTlkZjhhNDcxYTZhNDAyN2E1NzEiLCJpYXQiOjE2MTg2NDc1NzUsImV4cCI6MTYxOTI1MjM3NX0.LNxcdSQZY--QQuKbyt5oZrKn21OFcoJygArmUttGRsg"
}
