# Terraform

## Project
- Provision EC2 based HTTP Servers with Load Balancer

## Steps
- Step 01 - Creating and Initializing First Terraform Project
- Step 02 - Create AWS IAM User Access Key and Secret
- Step 03 - Configure Terraform Environment Variables for AWS Access Keys
- Step 04 - Creating AWS S3 Buckets with Terraform
- Step 05 - Creating AWS IAM User with Terraform
- Step 06 - Updating AWS IAM User Name with Terraform
- Step 07 - Creating Terraform Project for Multiple IAM Users
- Step 08 - Creating Terraform Project for Understanding List and Map
- Step 09 - Adding Elements - Problem with Terraform Lists
- Step 10 - Creating Terraform Project for Learning Terraform Maps 
- Step 11 - Creating New Terraform Project for AWS EC2 Instances
- Step 12 - Creating New EC2 Key Pair and Setting Up
- Step 13 - Adding AWS EC2 Configuration to Terraform Configuration
- Step 14 - Installing Http Server on EC2 with Terraform - Part 1
- Step 15 - Installing Http Server on EC2 with Terraform - Part 2
- Step 16 - Remove hardcoding of Default VPC with AWS Default VPC
- Step 17 - Remove hardcoding of subnets with Data Providers
- Step 18 - Remove hardcoding of AMI with Data Providers
- Step 19 - Playing with Terraform Graph and Destroy EC2 Instances
- Step 20 - Creating New Terraform Project for AWS EC2 with Load Balancers
- Step 21 - Create Security Group and Classic Load Balancer in Terraform




## Commands Executed

```
brew install terraform
terraform --version
terraform version
terraform init
export AWS_ACCESS_KEY_ID=*******
export AWS_SECRET_ACCESS_KEY=*********
terraform plan
terraform console
terraform apply -refresh=false
terraform plan -out iam.tfplan
terraform apply "iam.tfplan"
terraform apply -target=aws_iam_user.my_iam_user
terraform destroy
terraform validate
terraform fmt
terraform show
export TF_VAR_iam_user_name_prefix = FROM_ENV_VARIABLE_IAM_PREFIX
export TF_VAR_iam_user_name_prefix=FROM_ENV_VARIABLE_IAM_PREFIX
terraform plan -refresh=false -var="iam_user_name_prefix=VALUE_FROM_COMMAND_LINE"
terraform apply -target=aws_default_vpc.default
terraform apply -target=data.aws_subnet_ids.default_subnets
terraform apply -target=data.aws_ami_ids.aws_linux_2_latest_ids
terraform apply -target=data.aws_ami.aws_linux_2_latest

```