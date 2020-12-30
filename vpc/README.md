# **VPC**

## **About**

Make New VPC, InternetGateway, and 4-subnets(2-public and 2-private in 2az)

## **How to Use**

**1. Set following parameter in parameters.json**

- VPC-CIDR (default: 10.0.0.0/20)
- Public-Subnet1 (default: 10.0.0.0/24)
- Public-Subnet2 (default: 10.0.1.0/24)
- Private-Subnet1 (default: 10.0.8.0/24)
- Private-Subnet2 (default: 10.0.9.0/24)

**2. Execute AWS CLI**

    aws cloudformation create-stack \
    --stack-name vpc \
    --template-body file://vpc.yml \
    --parameters file://parameters.json