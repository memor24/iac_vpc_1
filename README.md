## Infrastructure as Code
In this repo, I will be adding infrastructure as code templates using Terraform for each of the AWS main services like IAM, S3, EC2, VPC, Lambda, DynamoDB, etc.
```terraform
terraform init
```
To clean the code syntax, basic validation and detailed planning, use:
```
terraform fmt
terraform validate
terraform plan
```
To create the infrastructure as planned, use:
```
terraform apply
```
To delete and completely remove the infrastructure (e.g. for cost control), use:
```
terraform destroy
```
#### Note
If you don't want to deploy them directly to AWS, you may also use Local Stack that helps with deploying to a localized AWS environment. 
First install a docker container of localstack, then launch it in a seperate terminal before terraform apply.
```
localstack start
```
In this case, you want to use tflocal command instead of terraform command to avoid credentials related complications:
```
tflocal apply
tflocal destroy
```
