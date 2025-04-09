# AI Platform

This project is a web-based platform built using **Next.js** and hosted on **AWS Amplify**. It is designed to facilitate secure and scalable access to AI tools and resources.

## Key Features

- **SageMaker Integration**: Access to Amazon SageMaker notebook instances with automatic data fetch on startup and auto-shutdown after periods of inactivity.
- **Data Upload**: Supports uploading datasets directly to S3 for processing and storage.
- **User Management**: Authentication and authorization are handled via AWS Cognito and DynamoDB.
- **Access Control**: Data access is governed strictly through IAM roles and policies—no direct access to underlying storage is permitted.
- **Security**: Utilizes AWS KMS to enforce encryption and secure handling of sensitive data.
- **Annotation Support**: Integrated with CVAT for visual data annotation.

