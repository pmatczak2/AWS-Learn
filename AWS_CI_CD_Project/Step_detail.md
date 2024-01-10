
Alt text

AWS CI/DC Project

In this project i will intigrate AWS different sercices to create CI CD project completely on AWS by using all AWS services.

I will be using AWS manage servisec. For example, i'll be using code commit. AWS code commit to store the source code instead of GitHub AWS code build service to build the artifact as we do it from Jenkins, we can have multiple code build projects for various kinds of jobs like running code analysis, running build, running unit test. Once we get our artifact, we can store it on the S3 bucket. We can have AWS code deploy service. This service can deploy artifact to various targets. For example beanstalk. We are going to use AWS beanstalk where a Tomcat platform will be running. So AWS code deploy is going to take the artifact and deploy to Beanstalk Tomcat platform. That will be also connected to an RDS database because our view profile application needs the database, my SQL database. So we are going to use RDS for that and we're going to combine everything with AWS code pipeline service. So as soon as developer makes a code change, the entire process gets executed and we'll have our application up and running on Beanstalk environment. First we will set up our infrastructure. We are going to set up for Beanstalk and RDS and show the integration. Then we are going to set up the CICD pipeline which can continuously deploy artifact or beanstalk environment.

(Step Detail)

Elastic Beanstalk

AWS Beanstalk It's a platform as a service for running application workload. you can get very quickly up and running within minutes by using Beanstalk service.

Elastic Beanstalk is a easier way for developers to quickly deploy and manage applications in the AWS cloud. Upload and lunch applications to AWS in minutes. Retain control over the underlying infrastructure. Open Elastic beanstalk  application is the project. It's just a way to group your different Beanstalk environment. Dev, QA staging, production multiple environments, you need to group them together. Elastic Beanstalk is for application what RDS is for the database. Underlying Elastic Beanstalk, there is load balancer, auto scaling group, EC2 instances, and many other services that you have to otherwise manage manually. If you use Beanstalk, you will have the control of all the underlying infrastructure centrally and all you need to do is create it, upload your artifact, and just run it.

RDS & Aoo Setup on Beanstalk:

Create RDS Allow port 3306 in RDS form Beanstalk SG Initialize database SSH to bean instance install mysql client & login to RDS Deploy db_backup.sql file Update health check to /login in Target Group

Code Commit Setting up CI CD ppeline.Alt text

To understand AWS code commit quicklythink of just a replacement of GitHub.Alt text

AWS CodeCommit it's a version control service and it is hosted by AWS and you get all the AWS security and power and also integration with other AWS services. If you're using code commit instead of using GitHub, client will be again the same git. You're going to do version controlling by using git and instead of pushing or changes to GitHub, we are going to use AWS code commit. So first I'll create a code commit repository, then I'll move or switch or transition from GitHub to code commit.

Code Build

I am going to go to AWS CodeBuild service so that I can access the code build service here itself. I'LL build code build and I'll create a project over here. This code build job or the project will be team as what I did in Jenkins. When I create a job I'll fetch the code, build then code, test it, notify. So here all the information I can provide and about the build I provide the information in a YAML format, it's called build spec. AWS CodeBuild it's fully managed continuous integration service that compiles source code, runs, test and produce software packages that are ready to deploy. That's what I want. I need to create the artifact so I can deploy to my beanstalk environment. Here you create the project and when you run the project only then you pay for it.

![Alt text](image.png)

![Alt text](image-1.png)