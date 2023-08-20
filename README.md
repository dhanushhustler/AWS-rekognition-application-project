# AWS-rekognition-application-project
Our project revolved around image classification powered by AWS Rekognition. By leveraging advanced machine learning techniques, we developed a robust system that could accurately categorize images based on their content. This solution not only showcased the capabilities of AWS Rekognition but also demonstrated the potential of AI-driven image analysis in various industries, from e-commerce to healthcare.

## How to Use
Install aws-shell

    pip install aws-shell

Configure

    aws configure

Create a collection on aws rekognition

    aws rekognition create-collection --collection-id facerecognition_collection --region us-east-1

Create table on DynamoDB

    aws dynamodb create-table --table-name facerecognition \ --attribute-definitions AttributeName=RekognitionId,AttributeType=S \ --key-schema AttributeName=RekognitionId,KeyType=HASH \ --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1 \ --region us-east-1

Create S3 bucket

    aws s3 mb s3://bucket-name --region us-east-1
