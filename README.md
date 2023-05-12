AWS Project (End-to-End Web Application Deployment)
What is Web application — It is a stand-alone application.
Steps:
1) Created a vpc
2) Created subnets
3) Created route-tables, internet-gateway
4) Configured rt,igw and subnets
5) Created an ec2 instance
6) Installed apapche2 webserver
7) Cloned my app from github and moved /var/www/html folder(delete default index.html before moving)
8) Purchased a domain
9) Create hosted-zone with the domain name
10) Copied the ns records into the domain provider
11) Create a record in route53 hosted zone
12) Browse application with the domain name

Should have an AWS account.
We need to have own network (VPC)
Step 1 : Create a VPC
 ![image](https://github.com/Mahesh8887/static-webapp/assets/119730245/bc8d8e78-9c07-4fcd-9383-bf26046f06ea)

- Provide the Ip range — 20.0.0.0/16
•	Name: my-vpc
 
16 — the number of Ip addresses that will be allocated.
There is a formula to calculate the Ip address:
2^(32-n)
n is nothing but the CIDR range (Classless inter-domain routing or subnetting)
Here 16 is CIDR.
2^(32–16) =2^(16)=65536
(Few ip address will be used for internal purpose by the aws,
1 subnet = 5 ip address cannot be used for our requirements.)
