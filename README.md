# Comcast
Example for the Challenges 
1. Architecting a scalable and secure web application in AWS
2. For keeping a Scalable applicatiin the fiest I will be adding the Auto scaling group and then using 
3. Secure the application and host such that only appropriate ports 
4. Develop and apply automated test to validate the correctness of the server configuration 

Approach =>
1. Launching an EC2 instance and make sure that the security groups are open 
2. Installing a Docker
3. Design a Docker File 
4. Create a Docker Image from (Docker Build )
5. Run the image as a container and check for the Public IP (docker run )
6. For making sure that the IP is up and running create a Runscope test which will check the output


/usr/bin/wget "Public IP" --timeout 30 -O - 2>/dev/null | grep "Normal operation string" || echo "The site is down" | /usr/bin/mail -v -s "Site is down" r7@gmail.com

THe other method would be launching an EC2 instance with Web server => Creating a AMI image => Creating a Launch Configuration => Creating a Auto scaling group => Creating an ELB and attaching it to the ASG

For Monitoring that application we can use Cloud Watch for monitoring the metrics  
