### CloudFormation template to create CodeDeploy resources
==========================
### Resources created:
==========================
**AWS::CodeDeploy::DeploymentGroup**
**AWS::Lambda::Function**
**AWS::IAM::Role**
**AWS::CodeDeploy::Application**
==========================
### CloudFormation with a Lambda function CustomResouce to update CodeDeploy deployment Group configuration: 

**1. Add Trigger**

**2. Add Alarm**
==========================

**Steps to follow:**

**1. Upload updateddeploymentgroup.zip to S3 bucket in AWS account**
**2. Update codedeploy.json Ec2TagFilters to approriate Ec2Tags for instances that have been launched with the purpose of being used with CodeDeploy**
**3. Launch codedeploy.json**
**4. codedeploy.json has the following parameters require input & understanding:**

**AlarmName -> CloudWatch alarm name to add**
**AppName -> CodeDeploy Application Name**
**CodeDeployTriggerName -> CodeDeploy trigger name**
**IgnorePollAlarmFailure -> Specifies whether to pass or continue on Alarm failure**
**S3Bucket -> S3 bucket that contains CodeDeploy application code**
**S3BucketName -> S3 bucket which has Lambda function code (updateddeploymentgroup.zip)**
**S3Key: S3 CodeDeploy application code**
**SNSTopicARN: SNS topic arn**
**TriggerEventsArray: Events trigger**

==========================

                
