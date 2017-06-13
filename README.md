# CloudFormation template to create CodeDeploy resources

==========================
### Resources created:
==========================

* AWS::CodeDeploy::DeploymentGroup
* AWS::Lambda::Function
* AWS::IAM::Role
* AWS::CodeDeploy::Application

==========================

### CloudFormation with a Lambda function CustomResouce to update CodeDeploy deployment Group configurations: 

* 1. Add Trigger

* 2. Add Alarm

==========================

### Steps to follow:
```sh
1. Upload updateddeploymentgroup.zip to S3 bucket in AWS account
2. Update codedeploy.json Ec2TagFilters to approriate Ec2Tags for instances that have been launched with the purpose of being used with CodeDeploy
3. Launch codedeploy.json
4. codedeploy.json has the following parameters require input & understanding:

| Parameter | Detail |
| ------ | ------ |
| AlarmName | CloudWatch alarm name to add [PlDb] |
| AppName | CodeDeploy Application Name [PlGh] | 
| CodeDeployTriggerName | CodeDeploy trigger name [PlGd] |
| IgnorePollAlarmFailure | Specifies whether to pass or continue on Alarm failure [PlOd] |
| S3Bucket | S3 bucket that contains CodeDeploy application code [PlMe] |
| S3BucketName | S3 bucket which has Lambda function code (updateddeploymentgroup.zip) [PlGa] |
| S3Key | S3 CodeDeploy application code [PlDb] |
| SNSTopicARN | SNS topic arn [PlDb] |
| TriggerEventsArray | Events trigger [PlDb] |
```
==========================

                
