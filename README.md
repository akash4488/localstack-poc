# lambda-localstack-project

## Overview
This project is designed to demonstrate the use of AWS Lambda functions locally using LocalStack. It includes a simple Lambda function that processes incoming events and can be tested in a local environment.

## Project Structure
```
lambda-localstack-project
├── src
│   ├── handler.py          # Main Lambda function handler
│   └── utils
│       └── __init__.py     # Utility functions for the handler
├── requirements.txt         # Python dependencies
├── docker-compose.yml       # Docker configuration for LocalStack
└── README.md                # Project documentation
```

## Setup Instructions

1. **Clone the repository**:
   ```
   git clone <repository-url>
   cd lambda-localstack-project
   ```

2. **Install dependencies**:
   Make sure you have Python and pip installed. Then run:
   ```
   pip install -r requirements.txt
   ```

3. **Run LocalStack**:
   Use Docker to start LocalStack:
   ```
   docker-compose up
   ```

4. **Deploy the Lambda function**:
   After LocalStack is running, you can deploy your Lambda function using the AWS CLI configured to point to LocalStack.

## Usage Example
Once the Lambda function is deployed, you can invoke it using the AWS CLI:
```
aws lambda invoke --function-name your_lambda_function_name --payload '{"key": "value"}' response.json --endpoint-url=http://localhost:4566
```

## Contributing
Feel free to submit issues or pull requests for improvements or bug fixes.