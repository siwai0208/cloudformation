# **EC2-LEMP**

## **About**

Make New EC2 Instanse with following packages
- mysql5.7
- nginx
- php7.3
- [sample-laravel-app](https://github.com/siwai0208/food-app)

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) and [**Security-Group**](https://github.com/siwai0208/cloudformation/tree/main/security-group) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- KeyName
- InstanceType
- DBUser
- DBPassword
- DBName
- GitUser
- GitEmail
- GitPassword

**2. Run commands using the AWS CLI**

    aws cloudformation create-stack \
    --stack-name ec2-lemp \
    --template-body file://ec2-lemp.yml \
    --parameters file://parameters.json