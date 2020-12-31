# **Security-Group**

## **About**

Make New Security-Group for EC2 Instanse via SSH and HTTP

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- SSHLocation
- HTTPLocation

**2. Run commands using the AWS CLI**

    aws cloudformation create-stack \
    --stack-name security-group \
    --template-body file://security-group.yml \
    --parameters file://parameters.json