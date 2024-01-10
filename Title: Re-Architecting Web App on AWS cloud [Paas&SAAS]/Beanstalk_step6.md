

Beanstalk
IAM 

Create role
Use case
EC2
Next

Permissions policies
AWSElasticBeanstalkWebTier
AbministratorAccess-AWSElasticBeanstalk
AWSElasticBeanstlkRoleSNS
AWSElasticBeanstakCustomPlatformforEC2Role

Next

Role details
Role Name
vprofilebean-role
Description
allows EC2 instances to call AWS services on your behalf.
Create role

In the IAM role, if there is a name aws-elasticbeacstalk-service-role, delete it.

Beanstalk

Create application

Environment tier
Web server environment

Allocation information
 vprofile-app

Environment information
environment name 
vprofile-app-prod
	
domain
“create a name”			Check availability

Platform
Tomcat
Platform brand
tomcat 8.5 with Corretto 11 
	
Application code
sample application 

Presets
custom configuration

Next

Service Access
Create and use new service role
	
EC2 key pair
vprofile-prod-key

Next

Virtual Private Cloud (VPC)
VPC
Select Default
	
Public IP Address
Select Activated
“check box all the zones, except from zone 1e”

Tag
	
	Key		Value
	name		vproapp
	Project		vprofile

Next

Instances

Root volume (boot Drive)
Root volume type
		
Capacity
auto scaling group	
LOAD BALANCES	

Instances 
2 min
2 max

instane type
t3.micro
Next
Rolling updates and deployments
Application deployments
Deployment policy
Rolling

Batch size
Percentage
50 % instances at a time

Next

Review all the settings you selected.

Submit (if everything is good)

	
	
	
			