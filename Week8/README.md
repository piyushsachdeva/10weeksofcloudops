# Week 8 - Serverless Challenge

In this challenge, you will use AWS Lambda to build a serverless API. AWS Lambda is a compute service that lets you run code without provisioning or managing servers. You can use Lambda to build many different types of applications, including APIs, web applications, and mobile backends.

## Requirements

- An AWS account
- Knowledge of Python or another programming language supported by AWS Lambda
- IaC Tool like Terraform, Pulumi or CloudFormation
- CICD: GitHub Actions

## Challenge Ideas

Here are some examples of serverless APIs that you can build with AWS Lambda:

- A simple API for your favorite TV Show (see below for reference)
- An API that fetches data from a database
- An API that processes images or videos (see below an example of QR Code Generator)
- An API that triggers other AWS services, such as Amazon Simple Notification Service (SNS) or Amazon Simple Email Service (SES)

## Steps

1. Create an AWS Lambda function. You can do this using the AWS Lambda console or the AWS CLI.
2. Write the code for your function. Your function should handle incoming HTTP requests and return a response.
3. Deploy your function to AWS Lambda.
4. Create an API Gateway resource and configure it to trigger your Lambda function.
5. Test your API by sending HTTP requests to the API Gateway resource.
6. Write IaC for your Lambda Function, so that you can use code to deploy it.
You can use any one of the following: Terraform, CloudFormation or Pulumi.
7. Setup a GitHub repository where you will push your lambda function code and IaC code.
8. Setup a CICD pipeline using GitHub Actions to deploy your Lambda Function if a push or change is made to the code in the repo.

## Examples

Here are few example ideas of what you can build.

### Serverless Resume API

Looking for a beginner friendly cloud serverless project? I have one for you.
AWS Lambda Resume API Challenge. A project where you will have the opportunity to build and deploy a serverless API using AWS Lambda and DynamoDB, integrated with GitHub Actions. The primary goal? Construct an API that can serve resume data in JSON format.

I have a GitHub repo for this one, where you can submit your solutions!
Link to the [GitHub Repo](https://github.com/rishabkumar7/aws-resume-api)

#### Code walkthrough

[![Serverless Resume API](https://img.youtube.com/vi/-pKrT7Ix3G0/sddefault.jpg)](https://youtu.be/-pKrT7Ix3G0?si=tZ784UqtJdKpq6kH)

### QR Code Generator

I built an API using AWS Lambda, that accepts POST requests with URL field in the body and generates a QR Code for the provided URL, saves the QR Code in S3 bucke and then sends back the QR Code S3 Object with 200 OK response.

[![QR Code Generator](https://img.youtube.com/vi/j8QZwM3LFDM/sddefault.jpg)](https://youtu.be/j8QZwM3LFDM?si=Ue46RnlmYzaJsGMY)

#### Live App

### Peaky Blinders API

An API for my favorite TV Show, the Peaky Blinders. This was built as FastAPI in Python but you can convert it into a Serverless Lambda API. It has different endpoint that you can send GET requests to get show data like:

- Cast
- Seasons
- Episodes

[![Peaky Blinders API](https://img.youtube.com/vi/LVuxmQfqivA/sddefault.jpg)](https://youtu.be/LVuxmQfqivA?si=qaGv51-10CF8X8cN)

## Conclusion

AWS Lambda is a powerful tool for building serverless APIs. By following the steps in this challenge, you can learn how to build your own serverless API with AWS Lambda.