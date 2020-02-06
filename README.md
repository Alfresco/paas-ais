The purpose of this repository is to share an AWS CloudFormation template for consumption by Alfresco AIS customers.

The CloudFormation template, when executed in a customer's own AWS account, creates an S3 storage bucket with two IAM roles providing Alfresco access to that bucket and AWS AI services.

The template requires three parameter inputs.
1. AlfrescoAccountID - Provided by Alfresco
2. BucketName - A globally unique name for the customer's S3 bucket.  We suggest something the customer can easily identify.
3. AlfrescoExternalID - Provided by Alfresco to additionally validate that Alfresco is the party connecting to the customer account.

The template outputs the below three paramters which need to be passed back to Alfresco.
1. S3Bucket - ARN for the S3 Bucket
2. AICrossAccountRole - ARN for the IAM role that allows Alfresco access.
3. AIComprehendAsyncRole - ARN for the IAM role that allows Alfresco to submit asynchronous Comprehend jobs.
