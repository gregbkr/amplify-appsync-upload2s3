# Amplify + AppSync: Upload image to s3 demo

## Overview
This setup will deploy an app using Amplify and AppSync (GraphQL).
A simple upload image:
- That only authenticated user can access
- Image goes to S3
- Metadata go to Dynamo 

### Infra

- Cloud: AWS
- Framework: [Amplify](https://aws.amazon.com/amplify) will help connect to AWS service in a simple way, permit efficient & fast coding
- GraphQL API: [AppSync](https://aws.amazon.com/appsync) from AWS, to unify and control user requests (Amplify managed) 
- Auth: [Cognito](https://aws.amazon.com/cognito) provide easy authentification for our users (email, google, facebook, etc..) - (Amplify managed) 
- Database: [DynamoDB](https://aws.amazon.com/dynamodb) is powerfull NoSQL DB, fully managed, autoscaling and HA (Amplify managed) 
- App: a simple app to upload a picture
- Code source: Github

## Deploy

### Prerequisites
Please setup on your laptop:
- AWS cli, and AWS account to deploy in `eu-west-1`

### Deploy
- Start locally `npm start`
- Browser http://localhost:3000

## Annexes

- Amplify setup for a new project, check [documentation](https://docs.amplify.aws/start/getting-started/installation/q/integration/react) to setup the framework:
```
npm install aws-amplify @aws-amplify/ui-react
npm install history react-bootstrap react-router-dom
amplify init
amplify add auth
amplify add storage
amplify add api
amplify push
```