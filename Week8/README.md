# Week 8 - Serverless Challenge 🚀

In this challenge, you will use Serverless Functions to build a serverless API. All major cloud providers offer Serverless Functions, a compute service that lets you run code without provisioning or managing servers. You can use these to build many applications, including APIs, web applications, and mobile backends.

The following are the services:

- [AWS Lambda](https://aws.amazon.com/lambda/)
- [Azure Functions](https://azure.microsoft.com/en-in/products/functions#:~:text=Azure%20Functions%20is%20an%20event,highest%20level%20of%20hardware%20abstraction.)
- [GCP Cloud Functions](https://cloud.google.com/functions)

## Requirements 🙋‍♂️

- A cloud provider account (AWS, Azure or GCP)
- Knowledge of Python or another programming language supported by these services.
- IaC Tool like Terraform or Pulumi
- CICD: Continuous Integrations and Continuous Deployment

## Challenge Ideas 💡

Here are some examples of serverless APIs that you can build with AWS Lambda:

- A simple API for your favorite TV Show (see below for reference)
- An API that fetches data from a database
- An API that processes images or videos (see below an example of QR Code Generator)
- An API that triggers other AWS services, such as Amazon Simple Notification Service (SNS) or Amazon Simple Email Service (SES)

## Steps 👇

1. Create a Serverless function. You can do this using the cloud management console or the cloud provider CLI.
2. Write the code for your function. Your function should handle incoming HTTP requests and return a response.
3. Deploy your function to the cloud.
4. Create an API Gateway resource or HTTP trigger and configure it to trigger your Serverless function.
5. Test your API by sending HTTP requests to the API Gateway resource.
6. Write IaC for your Serverless Function so that you can use code to deploy it.
You can use any one of the following: Terraform or Pulumi.
7. Set up a GitHub repository where you will push your serverless function code and IaC code.
8. Set up a CICD pipeline using GitHub Actions or a tool of your choice to deploy your Function if a push or change is made to the code in the repo.

## Examples 🟢

Here are a few example ideas of what you can build.

### Serverless Resume API

Would you be interested in a beginner-friendly cloud serverless project? I have one for you.
AWS Lambda Resume API Challenge. A project where you can build and deploy a serverless API using AWS Lambda and DynamoDB, integrated with GitHub Actions. The primary goal? Construct an API that can serve resume data in JSON format.

I have a GitHub repo where you can submit your solutions!
Link to the [GitHub Repo](https://github.com/rishabkumar7/aws-resume-api)

#### Code walkthrough

[![Serverless Resume API](https://img.youtube.com/vi/-pKrT7Ix3G0/sddefault.jpg)](https://youtu.be/-pKrT7Ix3G0?si=tZ784UqtJdKpq6kH)

### QR Code Generator

I built an API using AWS Lambda that accepts POST requests with a URL field in the body and generates a QR Code for the provided URL, saves the QR Code in the S3 bucket, and then sends back the QR Code S3 Object with 200 OK response.

[![QR Code Generator](https://img.youtube.com/vi/j8QZwM3LFDM/sddefault.jpg)](https://youtu.be/j8QZwM3LFDM?si=Ue46RnlmYzaJsGMY)

#### [Live App](https://url2qr.rishab.cloud)

### Peaky Blinders API

An API for my favorite TV Show, the Peaky Blinders. This was built as FastAPI in Python, but you can convert it into a Serverless Lambda API. It has a different endpoint that you can send GET requests to show data like:

- Cast
- Seasons
- Episodes

[![Peaky Blinders API](https://img.youtube.com/vi/LVuxmQfqivA/sddefault.jpg)](https://youtu.be/LVuxmQfqivA?si=qaGv51-10CF8X8cN)

#### [Live App](https://peaky-blinders.calmsand-ff14fe59.eastus.azurecontainerapps.io/)

## Conclusion

Serverless Functions are a powerful tool for building serverless APIs. Following this challenge's steps, you can learn how to build your serverless API with AWS, Azure, or GCP.
