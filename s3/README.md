# **S3**

## **About**

Make New S3-Bucket

## **How to Use**

**1. Set following parameter in parameters.json**

- S3BucketKeyID
- S3BucketAccessKey
- S3BucketRegion
- S3BucketName

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name s3 \
    --template-body file://s3.yml \
    --parameters file://parameters.json