# aws-cloudformation-ecs-poc-simple

## Synopsis

The `aws-cloudformation-ecs-poc-simple` demonstrates a Senzing deployment using an AWS Cloudformation template.

Detailed instructions at
[hub.senzing.com/aws-cloudformation-ecs-poc-simple](http://senzing.github.io/aws-cloudformation-ecs-poc-simple)

## How to deploy without much thinking

1. Visit [AWS Cloudformation with Senzing template](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=senzing-poc&templateURL=https://s3.amazonaws.com/public-read-access/aws-cloudformation-ecs-poc-simple/cloudformation.yaml)
1. In lower-right, click on "Next" button.
1. In **Specify stack details**
    1. In **Parameters**
        1. In **Acknowledge insecure system**
            1. Understand the nature of the security in the deployment.
            1. Once understood, enter "I AGREE".
        1. In **Senzing installation**
            1. Accept the End User Licence Agreement
    1. Other parameters are optional.
    1. In lower-right, click "Next" button.
1. In **Configure stack options**
    1. In lower-right, click "Next" button.
1. In **Review senzing-poc**
    1. Near the bottom, in **Capabilities**
        1. Check ":ballot_box_with_check: I acknowledge that AWS CloudFormation might create IAM resources."
    1. In lower-right, click "Create stack" button.

## Using deployment

1. Visit [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/home).
    1. Make sure correct AWS region is selected.
1. Wait until "senzing-poc" status is `CREATE_COMPLETE`.
    1. Senzing formation takes about 15 minutes to fully deploy.
    1. May have to hit the refresh button a few times to get updated information.
1. Click on "senzing-poc" stack
1. Click on "Outputs" tab
1. Click on "WebAppUrl" value

## Behind the scenes

### What Cloudformation does

1. Provisions:
    1. AWS infrastructure: VPC, subnets, Internet Gateway, Routes, IAM Roles and Policies, Logging
    1. AWS: EFS, 3 SQS queues, 3 AWS Aurora Postgres Serverless databases, ECS
    1. Senzing: Stream-loader (with autoscale), Redoer, API Server, Entity Search Web App

### What is not supported

1. What this doesn't support (i.e. what you don't get):
    1. Specification of existing AWS resources
        1. VPC, Subnets, RDS, SQS
