# Automating-code-deployments-using-AWS-CodePipeline

Automated Deployment of Windows Service Application Using AWS CodePipeline and AWS CodeDeploy
Project Overview
This project demonstrates the use of AWS CodePipeline to automate the deployment of a Windows Service application to a fleet of Amazon EC2 instances running the Windows Server operating system. It builds on previous manual deployments done with AWS CodeDeploy by adding automation using AWS CodePipeline, reducing the chance of human error and speeding up the deployment process.

Key Objectives:
Use AWS Cloud9 to package the application and upload it to an Amazon S3 bucket.
Build a multi-stage AWS CodePipeline with Amazon S3 as the source stage and AWS CodeDeploy as the deployment stage.
Review deployment configurations and automate code deployment using AWS CodeDeploy.
Verify the successful deployment using AWS Systems Manager Session Manager.
Project Steps
1. Package Application in AWS Cloud9
Open the AWS Cloud9 development environment.
Package the Windows Service application code and prepare it for deployment.
Upload the application revision to an Amazon S3 bucket for use in the pipeline.
2. Create a Multi-Stage AWS CodePipeline
In AWS CodePipeline, create a pipeline with the following stages:
Source Stage: Set Amazon S3 as the source stage to pull the application from the S3 bucket.
Deploy Stage: Configure AWS CodeDeploy to deploy the application to the EC2 fleet.
3. Configure AWS CodeDeploy
Set up the deployment configuration in AWS CodeDeploy.
Specify the EC2 instances running Windows Server as deployment targets.
Ensure the correct deployment group is configured for your application.
Define the deployment strategy (e.g., CodeDeployDefault.AllAtOnce for immediate deployment).
4. Automate Deployment with AWS CodePipeline
With the pipeline set up, initiate the automatic deployment by running the pipeline.
AWS CodeDeploy will automatically deploy the application to all EC2 instances in the specified deployment group.
5. Verify Deployment
Use AWS Systems Manager Session Manager to access one of the EC2 instances in the fleet.
Verify that the Windows Service application has been successfully deployed and is running as expected.
