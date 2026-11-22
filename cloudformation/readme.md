# CloudFormation

This project has two parts: first, it creates the base scenario, including the VPCs and their resources. Then, a second stack of Cloud Formation creates the private links. This separation allows you to observe the state both before and after the changes.

## Part One - basescenario 

This will create the infrastructure for the two VPCs, with their resources in isolated private networks that have no communication with each other.

1. Manually create an S3 bucket 

2. Upload the Cloud Formation **basescenario** scripts in the S3 bucket previously configured.

3. Create an RDS password-type SecureString parameter in AWS Systems Manager - Parameter Store, and save the DB password.

4. Enter into CloudFormation and upload and run the file **basescenario** main.yaml from your s3 bucket previously configured.

5. Verify that everything was created successfully. Should have two VPCs with their respective private subnets, two EC2 instances—one in each VPC—an RDS server with a 'customer' database, and an S3 bucket.

## Part Two - privatelink

Private Links for each resource, including the gateway endpoint for S3, will now be created.

1. Upload the CloudFormation **privatelink** scripts in the S3 bucket previously configured.

2. Enter into CloudFormation and upload the file **privatelink** main.yaml from your s3 bucket previously configured.

3. Verify that everything was created successfully, The instance, resource, and gateway endpoints should be created.