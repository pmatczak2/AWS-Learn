

Build & Deploy Artifact
Create a folder somewhere in your computer Clone the source code there and you will build the source code for there.
Terminal
Mkdir Desktop/aws-refactor
VS Code
Enter the GitHub URL 
Copy the URL
Clone the Repository 
Select the aws-refactor as a destination.

SRC
resources
Application.properties 

Line 3, Remove the db01, Paste RES endpoint in its place. From your notes
jdbc.User name: whatever you chose
jdbc.Password: past from notes

Memcache.active.host= paste memchacke endpoint

Rabbitmq.addtess= paste rabbitmq endpoint
rabbitmq.uername= check the port endpoint 
Rabbitmq.username = paste the user name
Rabbitmq.password = paste password from tour sticky note

save
Build the source code to artifact
Terminal
Make sure you are in the aws-refactor folder
Validate the application.properties file and the changes that were made with CAT 

Mvn -version

mvn install
Beanstalk 
Go to your envoirements
Click on the environment 

Upload and deploy
Choose file, find your artifact where is located on your computer. 
Vprofile.v2.war

Version label
profile-app-v2.5

Deploy	

When the instance is in a good state check the URL. Check the domain in the HTTPS associate your domain with the certificate

Go daddy 
Setting 
DNS records
add new record
			
New Records 
Type			Name				Value
CNAME	        	vprofile		Copy the endpoint in elastic beanstalk 
				
Save

Check the URL 
Try to login