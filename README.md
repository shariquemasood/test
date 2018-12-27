# SSL Certificate Expiry Check

A simple Lambda Function to check domain ssl certificate expiration. Using cloudwatch event rule, sns notification, IAM rule

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Default Environment Varible

The environmmet varible to pass in lambda function

```
threshold = 30
```
```
topicname = SslCertCheckSnsTopic
```
<b>threshold is in days you want notification </b><br>
<b>topicname should be the sns topic name </b>

### Required Environment Varible
The required environment varinle to pass in lambda function. we can pass multiple value as a comma seprated list

```
domainname = domain1.com,domain2.com
```
```
email = mailid@example.com,mainid2@example.com
```
<b> email of subscriber to get notification of ssl expiration </b><br>
<b> domainname to check ssl expiry </b>

### Running Terraform
Apply Terraform

```
AWS_PROFILE=default terraform apply
```

Destroy Terraform

```
AWS_PROFILE=default terraform destroy
```
## Built With

* [Terraform](https://www.terraform.io/) - The IaC used
* [Python](https://www.python.org/) - python2.7
* [AWS_Lambda](https://aws.amazon.com/lambda/) - Serverless computing platform

