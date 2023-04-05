
<b>Practice Project for Serverless Stack with Go </b>

After cloning the repo, follow the instructions below.
    
- Go to project directory cmd and build the project using ```go build main.go```
- Put the output file in an archive.
- Go to AWS Management Console
---
- Head over to lambda
- Define function name and run time (Go 1.x)
- Change execution role to create a new role from AWS policy templates 
- Define a role name (etc. go-serverless-executor)
- Add ```Simple microservice permissions``` into Policy templates.
---
- Click edit on runtime settings
- Change Handler part to main
- After that, click upload from button and upload the zip file (archive that we created)
---
- Go to AWS Management Console, and head over to DynomoDB
- Create Table
- Define table name as in the program. (go-serverless)
- define partition key (email string)
---
- Head over to API Gateway
- Crete API
- REST API
- API Name go-serverless
- Actions/Create Method
- Select ANY
- Lambda Function - Use Lambda Proxy Integration - go-serverless - use default timeout
- Actions/DeployAPI - New Stage - staging - deploy
- Copu invoke URL and test it on Postman or using curl
---

