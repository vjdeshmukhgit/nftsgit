# mdas-ii Readme
## Pre-requisites to run the automation script 
1. Verify Terraform version 0.11.13 is installed. Click [here](https://releases.hashicorp.com/terraform/0.11.13/) to download the version
1. Verify git (2.21.0.windows.1) bash (version 4.4.23(1)-release (x86_64-pc-msys)) is installed. Click [here](https://git-scm.com/download/win) to download the version
1. Verify AWS CLI (aws-cli/1.16.165 Python/3.6.0 Windows/10 botocore/1.12.155) is installed. Click [here](https://aws.amazon.com/cli/) to download the version
1. Setup AWS environment to the correct account and region by running the **aws configure** command from command prompt
1. Verify **make.exe** is installed and in the path. If not installed follow the [instructions](https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058) to setup. 
   1.  The git location will be at location - C:\Users\**username**\AppData\Local\Programs\Git\mingw64
   1.  Copy the downloaded make.exe to **bin** folder
1. Copy the openShift_rsa file to the **.ssh** folder located in c:\users\**username** folder

## Instructions for deploying the solution in an AWS account


The scripts performs the following tasks:
1. Create VPC, Subnet, Internet Gateway, S3 bucket, Openshift cluster and EC2 instances
1. Setup Security Groups, Route Tables
1. Install build tools - Jenkins, Nexus, and SonarQube in Openshift
1. Create the Dev, Test and Prod environments with the above resources. Only the Dev environment will have the build tools. 





## Repository Hierarchy




## Solution Description



## Instructions for running from code to full deployment




## Consideration of the stability, maintainability (including fault tolerance and monitoring), and scalability security of the 
solution

Stability and maintainability of application has been a strong consideration for our solution approach. The solution is based on simple architecture, uses proven and well known technology stack and is well augmented with unit and integration test cases to ensure stability and maintainability.
The application uses OpenShift Container Platform that is designed for scaling. The platform allows for hundreds of containerized workloads to be scheduled and run without any performance bottlenecks. The physical resources such as compute nodes and storage can be scaled as the workload and user base grows. 

Fault tolerance is provided to critical container workloads via OpenShift built-in mechanisms. In addition, data and configuration settings for container images can be persisted across instances via persistent volume claims and stateful sets. Monitoring of application will be supported by AWS CloudWatch.
We use OWASP scan to identify and address security vulnerabilities within the application code beside that OpenShift Container Platform has built-in enterprise grade security, all the way from the operating system layer up to the container registries. OpenShift allows administrators to configure role-based authorization to manage the system resources such as compute, networking, and storage, and application workloads.