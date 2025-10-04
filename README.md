# Serverless Media Upload Hub (AWS Lambda + S3 + DynamoDB)

This project presents a **serverless media upload hub** built using **AWS Lambda, Amazon S3,** and **Amazon DynamoDB.** It allows users to upload media files through a web interface, storing the files securely in S3 and saving related metadata in DynamoDB.

## Features 

### Serverless Backend :
Leverages AWS Lambda to power backend processing, delivering efficient, auto-scaling performance without the overhead of server management.
### Scalable Object Storage :
Employs Amazon S3 to securely store media files with industry-leading durability, availability, and seamless scalability.

### Fast and Flexible Metadata Storage :
Uses Amazon DynamoDB to maintain media metadata, ensuring low-latency, highly flexible data access.

### Intuitive Web Interface :
Offers a clean, user-friendly web form that lets users upload media files effortlessly from any browser.

## Project Architecture Diagram

![](./project%20img/AWS-Lambda-with-S3-and-DynamoDB-%20architecture.png)

## Architecture Overview

* **Frontend:** A responsive web-based upload form built with HTML and JavaScript.

* **API Gateway:** Routes incoming HTTP requests to corresponding AWS Lambda functions.

* **AWS Lambda:** Processes uploads and extracts metadata for storage.

* **Amazon S3:** Securely stores the uploaded media files with high durability.

* **Amazon DynamoDB:** Persists metadata such as filename, file type, upload timestamp, and user details.

## Project Walkthrough and Components

Below are the key components of the project, illustrated with screenshots to guide you through each step.

### 1. Upload Interface

![](./project%20img/photo_2025-10-04_14-48-25.jpg)

This image shows the web form used for uploading media, where users input a name, caption, and select a file.

### 2. IAM Role Permissions

![](./project%20img/Screenshot%20(62).png)

Details of the IAM role permissions granted to the Lambda function, allowing it to interact with S3 and DynamoDB.

### 3. Lambda Function Code

![](./project%20img/Screenshot%20(67).png)

A view of the Python code for the AWS Lambda function, which orchestrates the upload to S3 and data entry into DynamoDB.

### 4. S3 Bucket Overview

![](./project%20img/Screenshot%20(60).png)

The Amazon S3 bucket (lamdawithdynadb) where the media files are stored.

### 5. DynamoDB Table Entries

![](./project%20img/Screenshot%20(61).png)

The projectDynamoDB DynamoDB table displaying the metadata for uploaded items, including id, caption, file_url, and name.

### 6. Successful Upload Confirmation

![](./project%20img/final%20img.jpg)

The confirmation message displayed on the web interface after a successful media upload, showing the stored details and file URL.

## High-Level Deployment Steps

* Get started with the Serverless Media Upload Hub by completing these key steps:

**1.Create an S3 Bucket to Store Files**

Make a place in AWS called an S3 bucket where all your pictures, videos, or other files will be saved.

**1.Create a DynamoDB Table for Information**

Make a DynamoDB table to save details about the files, like their names, upload times, or who uploaded them.

**3.Set Up Permissions with an IAM Role**

Make a special role in AWS that lets your code (Lambda) access the S3 bucket and DynamoDB table safely.

**4.Write and Deploy Your Lambda Function**

Write the code (Lambda function) that will handle uploading files, saving info, and answering requests. Then upload it to AWS.

**5.Use a Lambda Layer for Extra Code**

If your code needs extra libraries, put them in a Lambda layer so your function stays clean and easy to update.

**6.Connect Lambda to API Gateway**

Create an API Gateway so people can send requests over the internet to your Lambda function using HTTP (like web requests).

**7.Build a Simple Frontend**

Make a basic website or app that talks to your API, lets users upload files, and shows them info about their uploads.
