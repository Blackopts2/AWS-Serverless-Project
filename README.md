# Serverless App with AWS and Terraform

## Project Overview

This project demonstrates the deployment of a serverless application using AWS services and Terraform. The application includes:

1. An AWS Lambda function written in Python to handle HTTP requests.
2. An API Gateway to expose the Lambda function as an HTTP endpoint.
3. A DynamoDB table to store application data.
4. Version control and collaboration through GitHub.

## Project Architecture

1. **Lambda Function**:
- Handles GET and POST requests.
2. **API Gateway**:
- Provides an HTTP interface for the Lambda function.
3. **DynamoDB Table**:
- Stores application data in a NoSQL format.

## Terraform Configuration

- **Provider**: AWS
- **Key Resources**:
  - Lambda, DynamoDB, API Gateway
  - Python
- **Outputs**:
  - The API Gateway endpoint upon successful deployment.  

## Getting Started
### Prerequisites
- Terraform installed locally.
- AWS CLI configured with appropriate permissions.
- Python runtime and dependencies (boto3, json) installed.
- A GitHub repository for version control (optional).

## Deployment Instructions
1. Clone the Repository
    ```bash
    git clone https://github.com/your-username/AWS-Serverless-Project.git
    cd AWS-Serverless-Project
2. Initialize Terraform
    ```bash
    terraform init
3. Apply Terraform Configuration
    ```bash
    terraform apply

## Usage
### POST Request
**Purpose**: Add a new item to the DynamoDB table.
**Request Format**: Payload must be in JSON format, including a unique id and other attributes.
**Example**:
    ```bash
    curl -X POST https://your-api-id.execute-api.region.amazonaws.com -H "Content-Type: application/json" -d '{"id": "1","name": "Bruce Wayne","age": 30}'

### GET Request
Purpose: Retrieve all items stored in the DynamoDB table.

**Example**:
    ```bash
    curl -X GET https://your-api-id.execute-api.region.amazonaws.com

**Expected Response**:
    ```bash
    [{"id": "1","name": "Bruce Wayne","age": 30}]

## Improvements and Next Steps
1. **Enhance Infrastructure Organization**:
- Use Terraform modules to better structure and manage resources.
2. **Strengthen Security**:
- Implement custom IAM policies for least privilege access.
- Secure API Gateway with API keys, AWS Cognito, or JWT tokens.
3. **Enable Monitoring and Logging**:
- Integrate AWS CloudWatch for detailed logs and metrics.
4. **Expand Features**:
- Add error handling for unsupported HTTP methods.
- Implement query and update endpoints for the DynamoDB table.

## Contributing
Contributions are welcome! Feel free to fork this repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Feedback
If you encounter any issues or have suggestions for improvement, please create an issue in the GitHub repository.