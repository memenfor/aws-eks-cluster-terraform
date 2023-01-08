# aws-eks-cluster-terraform 
This project create and manage  AWS eks cluster using terraform for local k8s learning purpose.

## Terraform Workspace
Make sure you are connected to a workspace 

## To  list all available workspaces 
```hcl
terraform workspace list
```
## To Create a workspace 
```hcl
terraform workspace new sbx
```

## To switch from one workspace to the other 
```hcl
terraform workspace select sbx
```

## To run this project 
Please make sure you provide your own s3 bucket name on line 9
```
terraform {
  required_version = ">=v1.2.1" 

  backend "s3" {
    bucket         =`BucketName`
    key            = "path/env"
    region         = "us-east-1"
  }
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.0"
    }
  }
}
```
## Terraform init
```hcl
terraform init
```
## Connect to your desired workspace (sbx, prod, dev)
```
terraform workspace select sbx
terraform valiidate 
terraform plan 
terraform apply
```
Connect:
```
```