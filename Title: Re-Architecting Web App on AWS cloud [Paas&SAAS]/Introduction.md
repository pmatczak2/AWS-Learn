

Title: Re-Architecting Web App on AWS cloud [Paas&SAAS]
Project refactoring AWS
Multi Tier web application stack
Re architecting services for AWS clouds
Architecture to boost agility or improve business continuity 
Scenario:
Project services running on physical/ viral/cloud machines
Varieties of services that pose your project runtime
Cloud computing team
virtualization team
DC OPS team
Monitoring team 
Sys admin ect involved
Problem:
Operational Overhead
Struggling with uptime & Scaling
Upfront CapEx & Regular OpEx
Manual Process/ Difficult to automat	
Solution:
Cloud Setup
PaAS/SAAS (services)
Iaac
Flexibility
Pay as you Go
AWS Services
BEANSTALK: Vm for Tomcat (app server)
BEANSTALK: Nginx LB replacement
BEANSTALK: automation for VM scaling
S3/EFS: Storage	
RDS SERVICES: Databases
ELACTIC MQ: RABBIT MQ
ROUTE52: DNS
CLOUDFORNT: CONTENT DELIVERY NETWORK
Object:
Flexible infra
No upfront cost
IAAC
PAAS
SAAS
COMPARISON:
Beanstalk | tomcat ec2/VM
Elb in beanstalk | nginx le/elb
Autoscaling | none/autoscaling
Efs/s3 | nfs/s3/efs
Ads | mysql on vm/ec2
Elastic cache | memcached on mv/ec2
Active mq | ravvitmq on vm/ec2
Route53 | go daddy, local dns
Cloudfromt no-one / multi dc across
Architecture of AWS services for project:

Ec2 instances
Elb
Autoscaling
Efs/s3
Rds
Elastic cache
Active mq 
Route53
Cloudfromnt 
Flow of execution:

Login to was account
Create key pair for beanstalk instance login  
Create security group for elasticcache, rds and activemq
Create
rds 
amazon elastic cache 
amazon active mq
Create elastic beanstalk enforcement
Update SG of backend to allow traffic form Beas SG 
update SG of backend to allow internal traffic 
Launch ec2-instance for DB initializing
Lofin to the instance and initialize RDS DB
Cache health check on beanstalk to /login
Add 443 https listener to ELB
Build artifact with backer information dolly artifact to beanstalk
Create CDN with ssl cert
Update entry in go daddy DNS zones
Test the url

