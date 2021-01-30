# ExpressMongoAPI

A simple but very useful example of API using Mongoose and Express.

## Descriptions

To run the application, you need to have NodeJs and MongoDB installed.
If you need, it's possible to find some instruction in the links below:
- [Install Node.js](https://nodejs.org/en/)
- [Install MongoDB](https://docs.mongodb.com/manual/installation/)

### Installing this API

- Download the ExpressMongoAPI folder.
- Install all dependencies with the command ```npm install```
- Make sure MongoDB is running, if necessary, open another terminal and run the command ```mongod``` 
- Before testing this code, it's necessary to complete the files on folder ```/src/config``` and change their extensions from ```.example.json``` to ```.json``` only. the config path, should be like this:
```shell
  .
  └── src
       └── config
            ├── auth.json
            └── mail.json
```
- Everything is configured, now you only need to run the API with the command ```npm start```
- A server will be create on **PORT 3000** from localhost.

## API Endpoints
|Method |URL                                         |Authenticate|
|-------|--------------------------------------------|------------|
|GET    |http://localhost:3000/auth/register         |            |
|POST   |http://localhost:3000/auth/authenticate     |            |
|POST   |http://localhost:3000/auth/forgot_password  |            |
|POST   |http://localhost:3000/auth/reset_password   |            |
|GET    |http://localhost:3000/projects              |required    |
|GET    |http://localhost:3000/projects/:projectID   |required    |
|POST   |http://localhost:3000/projects              |required    |
|PUT    |http://localhost:3000/projects/:projectID   |required    |
|DELETE |http://localhost:3000/projects/:projectID   |required    |

## Dependencies used

|Dependency                     |Description                                                                                              |
|-------------------------------|---------------------------------------------------------------------------------------------------------|
|Express                        |Framework to facilitate the creation of web applications with NodeJS                                     |
|body-parser                    |Handles the request body to facilitate the use of the information in your application                    |
|Mongoose                       |Assists the use of data persistence using MongoDB                                                        |
|JWT                            |Assists the use of Token for route authentication                                                        |
|nodemailer                     |In this application, it was used to send email for password recovery                                     |
|nodemailer-express-handlebars  |Template system for using email                                                                          |
|nodemon                        |Used only in development, this tool restarts the server whenever a file has been changed                 |



This example was based on the tutorial created by Rocketseat, which by the way I highly recommend.
[Rocketseat Tutorial](https://www.youtube.com/watch?v=BN_8bCfVp88)
