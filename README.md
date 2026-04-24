# fast-food-tech-challenge-lambda

AWS Lambda function responsible for user authentication in the Fast Food Tech Challenge platform, integrated with **AWS Cognito**.

## Objective

The objective of this repository is to provide a serverless authentication layer for the fast-food ordering system. The Lambda function handles user sign-in via Cognito User Pools and issues JWT tokens used to authorize requests to the backend microservices.

It is part of the broader [FIAP Tech Challenge](https://github.com/viniciussantos45/fast-food-tech-challenge) project.

## Tech Stack

- Node.js (AWS Lambda runtime)
- AWS Cognito
- GitHub Actions (automated deploy via `.github/workflows/deploy_lambda.yml`)

## Deploy

The function is deployed automatically via GitHub Actions on push. To deploy manually:

```bash
cd lambda_auth
npm install
zip -r function.zip .
aws lambda update-function-code --function-name <function-name> --zip-file fileb://function.zip
```
