

Elastic Cache
Subnet Groups
Create subnet group
Subnet group settings
Name
vprofile-memcached-sub-group
Description
vprofile-memcached-sub-group
Select deafult VPC
Select subnets
Check all the subnets are selected 
Create

Parameter groups

Create parameter group

Name 
Vprofile-memcached-para-group
Description 
Vprofile-memcached-para-group
Family
Memcached1.6

Create
Memcached clusters

Create cluster 
Create memcached cluster

Cluster settings

Choose a cluster creation method
Standard create

Location
AWS cloud

Cluster info 
Name 
vprofile-elasticache-svc
Description
vprofile-elasticache-svc

Cluster Settings
Engine version
1.6.17
Parameter groups
Vprofile-memchached-para-group
Node type
Cache.t2.micro (0.5 GiB memory)

Subnet group settings
vprofile-memcached-sub-group

Next

Select Security groups
Manage
vprofile-backend-SG
Next

Check all the details, especially in Cluster settings node type (cache.t2.micro)

Create




