## CloudFormation will automatically create the following resources in your AWS account:
* IAM roles for MediaConvert and Lambda
* S3 bucket (you will provide bucket name as CloudFormation parameter)
* SNS topic (you will provide email address as CloudFormation parameter)
* CloudWatch events for AWS Transcribe and AWS MediaConvert
* MediaConvert JSON template with job settings
* Lambda Python scripts
* SSM Parameter store
* CloudFront distribution for S3 folder containing final video playlist and CloudFront Origin Access Identity

## Prior the provisioning the stack, you must complete some preparation steps:

1. Create a new encrypted S3 bucket in us-east-1 region to hold the Lambda function zip files.  CloudFormation will read files from this bucket during stack creation.
1. Upload the 2 zip files from this repo to the new bucket.
1. You are now ready to return to the main [README.md](../README.md) and continue with `Run the CloudFormation template`.  The name of the S3 bucket containing the zip files will be specified as a CloudFormation template parameter `SourceZipFileBucketName`
