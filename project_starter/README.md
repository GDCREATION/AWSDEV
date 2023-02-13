### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the starter code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


#### STEP 1
## network.yml
First we must execute this file to create network infrastructure and S3 bucket.

aws cloudformation create-stack --stack-name udagram --template-body file://network.yml  --parameters file://networkParameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1

#### STEP 2
## Demo.zip
Upload the Demo.zip to the newly bucket created 

#### STEP 3
## servers.yml
we must execute this file to create Server infrastructure.

aws cloudformation create-stack --stack-name udagramFinal --template-body file://servers.yml  --parameters file://serverParameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1 --disable-rollback

Link to the website is provided in the Outputs Section

Terminate the instances after test





