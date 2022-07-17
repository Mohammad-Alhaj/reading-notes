# AWS: API, Dynamo and Lambda

## What is Amazon API Gateway?
In this guide, we’ll walk you through all the details of API Gateway. We’ll show you how it can be used with the Serverless Framework and give you a list of resources should you want to learn even more.

Recently, AWS also launched AWS HTTP APIs. These are a potential alternative to API Gateway REST APIs that we discuss in detail in our Ultimate Guide to AWS HTTP APIs.

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

Many Serverless applications use Amazon API Gateway, which conveniently replaces the API servers with a managed serverless solution.


## How does API Gateway work?

API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

API Gateway integrates with many other AWS services like AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools. These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.


## Why is API Gateway an essential part of the Serverless ecosystem?

Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.

This brings the advantages of the serverless model—scalability, low maintenance, and low cost due to low overhead—to mainstream web applications.


## How API Gateway Works

![](../image/exercises/nw.png)


## What is DynamoDB?

DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

reliable performance even as it scales;
a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
a small, simple API allowing for simple key-value access as well as more advanced query patterns.
DynamoDB is a particularly good fit for the following use cases:


## Amazon DynamoDB How it works


Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools.