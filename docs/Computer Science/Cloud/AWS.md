Amazon EC2
    Amazon Elastic Beanstalk    
Amazon S3 block storage
Amazon Glacier


Cross Region Replication
Versioning
S3 transfer configuration
AWS cloudfront edge location : Cache data 
Amazon VPC
Subnets are logical subdivision of a larger network

Public subnet 
    * Connect to internet
    * Resources are exposed to the internet using the internet Gateway
    * Makes use of both public and private IP
    * Mainly used for external facing applications like web servers


Private subnet 
    
    * Not connect to internet
    * Resources are not exposed to the outer world
    * Make use of only private IPs
    * Mainly used for backend application (Database & application servers)
    
A route table contains a set of rules used to determine where network traffic from your VPC is directed

Cloud Storage Practices
* Scruntize SLA
* Follow your business needs
* Ensure security
* Plan your storage future
* Beware of hidden costs

Benefits of using cloud for data Storage
• Customer Friendly
• Secure
• Pocket friendly

Elastic Load Balancer : automatically  distribute incoming traffic across ex: EC2, Container, IP address : availability
 * Classic load balancer
 * Application load balancer
 * Network Load balancer
 * Gateway Load balancer
 AWS Direct connect:
 clody service that make it easy to estabilish a dedicated network connection from your premise to AWS

 AWS Route S3:
 is a highly available and scalable cloud domain name system or DNS web service
 * Register Domain names
 * Route internet traffic to the resources
 * Monitor health of the resources

Internet gateway --> VPC
Amazon Cloudwatch 

AWS Rute53
Dynamic DNS
:Domain names changes when IP address changed
