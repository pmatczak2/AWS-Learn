
DB Initialization
SQL queries GitHub
Access the source code. 
AWS main branch. 
SRC
Main
Records 
db_backup.sql

EC2 Service
Lance Instance 
name 
mysql-client
Ubuntu

instance type
t.2.micro
	
Key pair
vpro-bean-key

Network Settings
Security group 	
mysql-client-sg
Description
mysql-client-sg
Inbound security group rules	
		source type
		     My IP

Lance Instance
Security groups 
Copy mysql-client-SG, got to vprofile-backend-SG, 
	Edit inbound rules 
		Type		Protocol	Port range		
	      Custom TCP.           TPC		   3306             mysql-client-sg

Save rules 


Terminal
Back in the instance, mysql-client copy the public IP, open the terminal ssh into that IP

Run commands.
Sudo apt update && amp install maysql-client -y 
Test the connection 
Log in to RDS
Mysql “copy and paste the RDS endpoint” -u admin -p “paste password” accounts 

Exit from SQL

Git clone the source code from GitHub

Cd to vprofile-project
Ls 

Log back in to RDS 
Mysql “copy and paste the RDS endpoint” -u admin -p “paste password” accounts < src/main/recources/db_backup.sql

Log in to RDS instances 
Mysql “copy and paste the RDS endpoint” -u admin -p “paste password” accounts

Show tables; 
Exit

Terminate the SQL services right after you are done!
Broker

Click on Vprofile-rmq
Copy Endpoint to sticky note “remove the port number form the end”

Take endpoint for ElasticCache 
rqditMQ endpoint remove AMPQPS from the beginning. 
Copy endpoint to sticky note “remove the port number for the end” 
