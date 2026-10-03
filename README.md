# EC2 + S3 Access Using an IAM Role

## Objective
Show how an EC2 instance securely accesses S3 without storing AWS access keys.

## Architecture
EC2 → IAM Role → S3

## Services Used
EC2, S3, IAM

## Steps
1. Created S3 bucket `ec2-s3-project-thejus`
2. Created IAM policy (see IAM Role

## Objective
Show how an E# EC2 + S3 Acces# EC2 + S3 Acces3. Created IAM rolesing an IAM Rolwith EC2 as the trusted entity
4. Launched an Amazon Linux 2023 EC2 instance and attached the role
5. Connected using EC2 Instance Connect
6. Verified identity: → S3

## Services Used
EC2, S37. Uploaded a file:sing an IAM Role

## Objective
Show how an EC2 ins8. Downloaded it: Using an IAM Role

## Objective
Show how an EC2 in
## Screenshots
![Bucket](screenshots/01-bucket.png)
![Role attached](screenshots/02-role-attached.png)
![Upload](screenshots/03-upload.png)
![Download](screenshots/04-download.png)
![Access denied on delete](screenshots/05-access-denied.png)
![IAM policy](screenshots/06-policy.png)

## Least Privilege Demo
Deleting an object failed with *Access Denied* becauseole `EC2-S3-Role` wwas never granted to the IAM rolele

## Objectiv

## Key Learning
- Never store AWS access keys in EC2 code
- Use IAM roles for temporary, auto-rotating credentials

## Cleanup
Terminated the EC2 instance, emptied and deleted the bucket, deleted the role and policy.
