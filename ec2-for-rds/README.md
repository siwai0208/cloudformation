# **EC2-for-RDS**

## **About**

Make New EC2 Instanse use RDS with following packages
- mysql-client
- nginx
- php7.3
- [sample-laravel-app](https://github.com/siwai0208/food-app)

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) and [**Security-Group**](https://github.com/siwai0208/cloudformation/tree/main/security-group) and [**RDS**](https://github.com/siwai0208/cloudformation/tree/main/rds) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- KeyName
- InstanceType
- GitUser
- GitEmail
- GitPassword

**2. Run commands using the AWS CLI**

    aws cloudformation create-stack \
    --stack-name ec2-for-rds \
    --template-body file://ec2-for-rds.yml \
    --parameters file://parameters.json