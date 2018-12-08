# aws-python-snippets

This is a simple test repo for generic actions a user may want to take against an AWS service. Please note that there is no sequence to the information and it will consist of simple scripts to illustrate what is possible and for my own learning purposes.

Ensure access is configured using AWS CLI: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html

Moving files from your local machine into S3 using Python (boto3):
```
# Imports
import boto3

# Create a s3 service resource.
s3 = boto3.resource('s3')


# Create a s3 bucket.
my_bucket = s3.create_bucket(
    ACL='private'
    , Bucket='aws-python-snippet-bucket'
    , CreateBucketConfiguration={
        'LocationConstraint': 'ap-southeast-2'
    }
)
```
