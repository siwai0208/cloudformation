# **RDS (MySQL 5.7.31)**

## **About**

Make New RDS Database and RDS SecurityGroup

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) stack before using this stack

## **How to Use**

**1. Set following parameter in parameters.json**

- DBId
- DBUser
- DBPassword
- DBName
- DBAz
- DBSourceIP

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name rds \
    --template-body file://rds.yml \
    --parameters file://parameters.json