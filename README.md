# Serverless-Web-Application
I built a backend using AWS Lambda, API Gateway, and DynamoDB.

# Serverless Web Application (Lambda, API Gateway, DynamoDB)

## Overview

This project implements a **serverless backend** using AWS services. The goal is to build a scalable, pay-per-use application without managing servers.

## What I Did

- Designed RESTful APIs with **Amazon API Gateway**
- Implemented business logic with **AWS Lambda** functions
- Stored data in **Amazon DynamoDB**
- Configured IAM roles and permissions for secure access
- Monitored logs and performance using **CloudWatch**

## Architecture

- **API Gateway** – handles HTTP requests and routes them to Lambda
- **Lambda** – runs stateless functions (e.g., create/read/update/delete items)
- **DynamoDB** – NoSQL database for storing application data
- **CloudWatch** – logging and metrics

## Steps I Followed

### 1. Define the data model

- Identified entities and attributes to store in DynamoDB
- Created a DynamoDB table with a primary key (partition key, and optionally sort key)

### 2. Write Lambda functions

- Created Lambda functions (e.g., `createItem`, `getItem`, `listItems`, `deleteItem`)
- Implemented logic using Python/Node.js SDKs (AWS SDK)
- Configured environment variables as needed

### 3. Expose APIs with API Gateway

1. Created a **REST API** in API Gateway
2. Added methods (GET, POST, PUT, DELETE) for the resources
3. Integrated each method with the corresponding Lambda function
4. Enabled CORS (if called from a browser)
5. Deployed the API to a stage (e.g., `dev`)

### 4. Permissions and security

- Created IAM roles for Lambda with least-privilege access to DynamoDB tables
- Configured execution roles and resource-based policies

### 5. Testing and monitoring

- Tested endpoints using Postman / curl
- Verified DynamoDB records were created/updated correctly
- Monitored execution logs in **CloudWatch Logs**

## Example Endpoints

- `POST /items` – create a new item
- `GET /items/{id}` – retrieve an item
- `GET /items` – list all items

## Key Learnings

- How to build a backend without managing servers
- Designing DynamoDB tables and access patterns
- Integrating API Gateway and Lambda
- Observability using CloudWatch logs and metrics

  refered from https://www.freecodecamp.org/news/how-to-deploy-a-static-web-app-on-aws-with-amplify-lambda-api-gateway-and-dynamodb/#:~:text=AWS%20Lambda:%20Imagine%20you%20have,super%2Dfast%2C%20flexible%20database.
  
