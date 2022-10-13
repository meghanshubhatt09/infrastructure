# Infrastructure
## AWS CloudFormation
## CSYE6225-Cloud Computing
----------------------------

### What is Amazon VPC?

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.

----------------------------

### What is AWS CloudFormation?
AWS CloudFormation is a service that gives developers and businesses an easy way to create a collection of related AWS and third-party resources, and provision and manage them in an orderly and predictable fashion.

----------------------------

### How to set and configured AWS ?
$ curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"

$ sudo installer -pkg AWSCLIV2.pkg -target /

aws configure --profile [profileName]

Set the information

### Setting up the infrastructure in dev account:

$ export AWS_PROFILE=dev

$ aws --region us-east-1 cloudformation create-stack --stack-name myvpc --template-body file://csye6225-infra.yml


--parameters ParameterKey=SubnetRegion1,ParameterValue="us-east-1a" ParameterKey=SubnetRegion2,ParameterValue="us-east-1b" ParameterKey=SubnetRegion3,ParameterValue="us-east-1c"


$ aws cloudformation delete-stack --stack-name myvpc 

## AWS CLI

## AWS Profile

aws configure --profile=dev

aws configure --profile=prod

export AWS_PROFILE=dev

export AWS_PROFILE=prod

## AWS Networking

aws ec2 create-vpc --cidr-block "10.0.0.0/16" --no-amazon-provided-ipv6-cidr-block --instance-tenancy default

aws ec2 delete-vpc --vpc-id vpc-08ccb95c7042bc32e

aws ec2 describe-vpcs --filters Name=Name,Values=demo

aws ec2 modify-vpc-attribute --enable-dns-hostnames --enable-dns-support --vpc-id <value>

aws ec2 modify-vpc-attribute --no-enable-dns-hostnames --vpc-id vpc-08f37ad6c277af8a5



----------------------------
| Name | NEU ID | Email Address              |
|------| --- |----------------------------|
| Meghanshu Bhatt | 002961585 | bhatt.me@northeastern.edu |




