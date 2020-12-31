# **AutoScaling for RDS and S3 Bucket**

## **About**

Make New EC2 Instanse use RDS with following packages
- mysql-client
- nginx
- php7.3
- [sample-laravel-app-s3](https://github.com/siwai0208/food-app-s3)

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) and [**Security-Group**](https://github.com/siwai0208/cloudformation/tree/main/security-group) and [**S3**](https://github.com/siwai0208/cloudformation/tree/main/s3) and [**RDS**](https://github.com/siwai0208/cloudformation/tree/main/rds) and [**ALB**](https://github.com/siwai0208/cloudformation/tree/main/alb) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- KeyName
- InstanceType
- GitUser
- GitEmail
- GitPassword
- WebServerCapacity (default: 2)

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name autoscaling-s3 \
    --template-body file://autoscaling-s3.yml \
    --parameters file://parameters.json