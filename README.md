# CI/CD for Mobile - AWS DevOps Essentials

## An Introductory Workshop on CI/CD Practices

In few hours, quickly learn how to effectively leverage various AWS services to improve developer productivity and reduce the overall time to market for new product capabilities and Mobile development. In this session, we will demonstrate a prescriptive approach to incrementally adopt and embrace some of the best practices around continuous integration & delivery using AWS Developer Tools and 3rd party solutions including, AWS CodeCommit (a managed source control service), AWS CodeBuild (a fully managed build service), CodePipeline (a fully managed continuous delivery service), and AWS Device Farm (a managed app testing service that lets you interact with physical devices in the cloud). We will also highlight some best practices and productivity tips that can help make your software release process fast, automated, and reliable.

## Prerequisites

* **Configure AWS CodeCommit:** The easiest way to set up AWS CodeCommit is to configure HTTPS Git credentials for AWS CodeCommit. On the user details page in IAM console, choose the **Security Credentials** tab, and in **HTTPS Git credentials for AWS CodeCommit**, choose **Generate**.

![HTTPS Git Credential](./img/codecommit-iam-gc1.png)

**💡 Note:** Make Note of the Git HTTP credentials handy. It will be used for cloning and pushing changes to Repo. Also, You can find detail instruction on how to configure HTTPS Git Credential [here](https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html).

  **💡 Note:** Note that this option is only available if you are using an IAM user to access CodeCommit. If you are using another type of sign-in, set up your connection to AWS CodeCommit repositories using the credential helper included in the AWS CLI. This is the only connection method for AWS CodeCommit repositories that does not require an IAM user, so it is the only method that supports root access, federated access, and temporary credentials. Follow the steps [here](https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-https-unixes.html#setting-up-https-unixes-credential-helper).

* **IAM Permissions:** Finally, for the AWS account ensure you have sufficient privileges. You must have permissions for the following services:

- AWS Identity and Access Management
- Amazon Simple Storage Service
- AWS CodeCommit
- AWS CodeBuild
- AWS CodePipeline
- AWS CloudFormation
- AWS Cloud9
- Amazon EC2
- Amazon SNS
- Amazon CloudWatch Events
- AWS Device Farm

***

### **Important:**
Preferred regions for lab
- North Virginia US-EAST-1
- Oregon US-WEST-2

If you want to your own region choice for the lab, kindly select the region which has all three Code* services and Cloud9 service. You can find the [region services list](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/). Stick to the same region throughout all labs. 
**Make sure you have not reached the VPC or Internet Gateway limits for that region. If you already have 5 VPCs/IGWs, delete at least one before you proceed or choose an alternate region.** 

# Labs
This workshop is broken into multiple labs. You must complete each Lab before proceeding to the next.

1. [Lab 1 - Build project on the cloud](1_Lab1.md) 
2. [Lab 2 - Setup CI/CD using AWS CodePipeline](2_Lab2.md)
3. [Lab 3 - Using AWS Device Farm as Test Stage in CodePipeline](3_Lab3.md)
4. [Lab 4 - Hands-on with Device Farm](4_Lab4.md)



## Clean up

1. Visit [CodePipeline console,](https://console.aws.amazon.com/codepipeline/home) select the created pipeline. Select the Edit and click **Delete**.
2. Visit [CodeBuild console,](https://console.aws.amazon.com/codebuild/home) select the created project. Select the Action and click **Delete**.
3. Visit [CodeCommit console,](https://console.aws.amazon.com/codecommit/home) select the created repository. Go to setting and click **Delete repository**.
4. Visit [Cloudformation console,](https://console.aws.amazon.com/cloudformation/home) select the created stacks. Select the Action and click **Delete Stack**.
5. Visit [Cloud9 console,](https://console.aws.amazon.com/cloud9/home) select the created Environment. Select the Action and click **Delete**.
6. Visit [Simple Notification Service console,](https://console.aws.amazon.com/sns/home) select Topics. Select the created topic.  Select the Action and click **Delete topics**. Next select Subscriptions. Select the created subscription. Select the Action and click **Delete subscriptions**.

## License

This library is licensed under the Apache 2.0 License. 
