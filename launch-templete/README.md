# **Launch Template LEMP with Code-deploy Agent**

## **About**

Make New Amazon Linux2 Instanse with following packages
- mysql5.7
- nginx
- php7.3
- Code-deploy Agent

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) and [**Security-Group**](https://github.com/siwai0208/cloudformation/tree/main/security-group) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- KeyName
- InstanceType
- DBName
- DBUser
- DBPassword
- EC2RoleforCodeDeployArn (arn:aws:iam::xxxxxxxxxxxx:instance-profile/EC2RoleforCodeDeploy")

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name launch-template \
    --template-body file://launch-template.yml \
    --parameters file://parameters.json