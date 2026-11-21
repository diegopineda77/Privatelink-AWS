# Terraform

Each version also contains a dedicated `terraform` directory.

```text
V1/
└── terraform/
    ├── main.tf
    ├── variables.tf
    ├── outputs.tf
    ├── providers.tf
    └── README.md
```

Terraform is used as the **Infrastructure as Code (IaC)** layer.

The Terraform configuration defines and provisions the cloud infrastructure required by each version.

Depending on the version, this may include resources such as:

* VPC
* Subnets
* Route tables
* Internet Gateway
* NAT Gateway
* Security Groups
* EC2
* ECS
* Load Balancers
* S3
* CloudFront
* RDS
* IAM
* CloudWatch
* Other AWS services

The Terraform configuration allows the infrastructure to be reproduced consistently and provides a documented representation of the cloud architecture.

The Terraform README contains instructions for:

1. Initializing Terraform
2. Reviewing the execution plan
3. Applying the infrastructure
4. Reviewing outputs
5. Destroying the environment

Example:

```bash
terraform init
terraform plan
terraform apply
```