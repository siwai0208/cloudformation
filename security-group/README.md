# **Security-Group**

## **About**

Make New Security-Group for EC2 Instanse via SSH and HTTP

## **How to Use**

**1. Set following parameter in parameters.json**

- SSHLocation
- HTTPLocation

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name security-group \
    --template-body file://security-group.yml \
    --parameters file://parameters.json