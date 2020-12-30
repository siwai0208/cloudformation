# **ALB**

## **About**

Make New ALB and SecurityGroup and TargetGroup(AutoScaling)

## **Dependency**

You have to execute [**VPC**](https://github.com/siwai0208/cloudformation/tree/main/vpc) and [**Security-Group**](https://github.com/siwai0208/cloudformation/tree/main/security-group) stack before using this stack

## **How to Use**

**1. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name alb \
    --template-body file://alb.yml