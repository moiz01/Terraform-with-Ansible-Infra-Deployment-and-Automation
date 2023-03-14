# terraform_workspace
Terraform Workflow
 1. write terraform config
	write your terraform code: start with creating HCL config file for infra.
 2. Plan Infrastructure
	Review: user will continously add and review changes to code files
 3. Deploy Infrastructure
	Apply: user will deploy the infrastructure.

Terraform Initialization
terraform init 
terraform plan
terraform apply
terraform destroy

## download and install Terraform on local Machine (ubuntu 16)
 cat /etc/lsb-release 
 wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
 
 AWS 
 create user:terraadmin
 access type: programatic
 Group: terraform-admin
 Policy: AdministratorAccess
 
 Security Group:
 edit default security group  inbound role all traffic from all
 
 
 https://github.com/anshulc55/terraform/tree/master/Start%20With%20Terraform%20Basics
 
 
 mkdir providers
 cd providers
 export TF_LOG=TRACE
 vim main.tf
 vim myvar.tf
 vim provider.tf
 vim createInstance.tf
 
 terraform init 
 ls -latrh
 
 terraform init
 terraform apply
 
 
 ## Terraform Variable
 method 1: 
  terraform plan 
 method 2:
 terraform plan -var AWS_ACCESS_KEY="AKIAS6HD3C5BMSUA4L52" -var AWS_SECRET_KEY="";
 method 3:
 vim terraform.tfvariables
 AWS_ACCESS_KEY="";
 AWS_SECRET_KEY="";
 

terraform plan -var AWS_ACCESS_KEY="AKIAS6HD3C5BMSUA4L52" -var AWS_SECRET_KEY="" -var AWS_REGION="us-west-2";
 
 
