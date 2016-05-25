# AWS Build AMI

Packer will use a source AMI for run EC2 and provision with our scripts for then build a new AMI image will uploaded on AWS account.

## Requirement

 1. You must have AWS cli tools installed => refer to http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html
 2. Create an user dedicated to packer build with only policy he need `refer to file iam-policy.json`
 3. Register user credential as an aws profile in your terminal under the name `infra-packer` 

**You must select the same region as define in Template.json**

## Run

$ make build
