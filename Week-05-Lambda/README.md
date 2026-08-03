# Week 5 - AWS Lambda

## Overview

AWS Lambda is a serverless compute service that allows you to run code without provisioning or managing servers. Lambda automatically scales your application by running code in response to events and only charges for the compute time used.

AWS Lambda supports multiple programming languages, including Python, Java, Node.js, C#, Go, and Ruby.

---

## Key Features

- Serverless computing
- Automatic scaling
- Pay only for execution time
- Event-driven architecture
- Supports multiple programming languages
- Easy integration with other AWS services

---

## Common Use Cases

- Backend APIs
- File processing
- Data transformation
- Scheduled tasks
- Real-time stream processing
- Automation

---

## Hands-on Lab

### Lab 1: Create a Lambda Function

#### Steps Performed

1. Opened the AWS Management Console.
2. Navigated to **AWS Lambda**.
3. Clicked **Create Function**.
4. Selected **Author from scratch**.
5. Configured:
   - Function Name: `HelloAWS`
   - Runtime: **Python 3.x**
6. Created the function.

---

### Lab 2: Write the Lambda Function

Used the following Python code:

```python
def lambda_handler(event, context):
    return {
        "statusCode": 200,
        "body": "Hello AWS"
    }
```

---

### Lab 3: Deploy and Test

#### Steps Performed

1. Clicked **Deploy**.
2. Created a test event.
3. Clicked **Test**.
4. Verified the successful execution.

Example Output:

```json
{
  "statusCode": 200,
  "body": "Hello AWS"
}
```

---

## Outcome

Successfully:

- Created an AWS Lambda function.
- Wrote a Python Lambda function.
- Deployed the function.
- Executed the function using a test event.
- Verified the expected output.

---

## Skills Gained

- Understanding serverless computing.
- Creating AWS Lambda functions.
- Writing Python code for Lambda.
- Testing and deploying Lambda functions.
- Understanding event-driven execution.

---

## AWS Services Used

- AWS Lambda

---

## Key Takeaways

- AWS Lambda is a serverless compute service.
- No server management is required.
- Functions run only when triggered by an event.
- AWS automatically handles scaling.
- Lambda integrates seamlessly with other AWS services.
