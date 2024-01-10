

Update on Security Group & ELB
S3

Buckets 
select the bucket in the region you are working with

Permissions
Object ownership 
ACLs ownership.
Enabling ACLs turns off the bucket owner
I acknowledge that ACLs will be restored. 	
		
Beanstalk 
envoirement 
		
Configuration 
	
Instance traffic and scaling
edit 
Processes 
action 
edit
Health check
Path
/login
sessions 
Sessions stickiness 
Enabled


Save
Next we will add https listener 
Add port 443 https listener. 
Select SSL certificate from AMC
Modify Application Load Balancer 
Add listener 
     Port
443
     Protocol
HTTPs
	SSL Certificate
choose your certificate
Add

Come down to the bottom of the page and APPLY

EC2
In instances, click on a instance, go to security group, click on the security group. This will take you to the security group directly. 

Security Group ID
copy the security group

Go back to your security group and find your vprofile backend security group 

Inbound rules
Edit

Add rule
Type		                          Info					Description
all trafficpaste    security group ID of the instance	Allow all form of traffic from Instance SG

Add Rule
Type		             Port                 Info					Description
Custom TPC		3306		security group ID of the instance

Add Rule
Type		             Port                 Info					Description
Custom TPC		11211		security group ID of the instance

Type		             Port                 Info					Description
Custom TPC		5672		security group ID of the instance

Save rules
Health check 
Processes 
Check box  in the default
Actions 
Edit 
Health check
Path
/login
sessions 
Sessions stickiness 
Enabled