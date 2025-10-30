# VPC-Virtual-Private-Cloud-Public-Subnet-and-Private-Subnet-Create-Public-EC2-instance

VPC: Virtual Private Cloud 
The following diagram shows an example VPC. The VPC has one subnet in each of the Availability Zones in the Region, EC2 instances in each subnet, and an internet gateway to allow communication between the resources in your VPC and the internet.
<img width="814" height="486" alt="image" src="https://github.com/user-attachments/assets/b8d4aa04-c159-4898-b65a-ea71b4ae21ab" />

Public Subnet and Private Subnet:

<img width="735" height="536" alt="image" src="https://github.com/user-attachments/assets/19676e58-dbb9-4194-be1e-5ed21d38f865" />


## Public Subnet: A default VPC comes with a public subnet in each Availability Zone, which is accessible from the internet. This type of subnet has a direct route to an Internet Gateway, allowing resources within it to have direct access to and from the internet. Resources in a public subnet can be assigned a public IP address.
## Private Subnet: A VPC can be configured with only private subnets, where all resources require a gateway to connect to the internet or a VPN to connect to an on-premises network. This subnet does not have a direct route to an Internet Gateway. Resources in a private subnet can access the internet indirectly, typically by routing their traffic through a NAT gateway located in a public subnet. 

In EC2 Console there are subnets that is private subnet and public subnet but how to identify them by checking its route table

Public subnet: 0.0.0.0/0 -igw-xxxx (internet gateway)
Private subnet:0.0.0.0/0-nat-xxxx (Network Address Translation Gateway)

## Create Public EC2 instance:
-	Launch instance
-	Name instance -Publicinstance
-	Select Amazon linux
-	T2.micro
-	Select key pair
-	In Network settings
      VPC -default.
      Select Public subnet .
      Auto assign Public IP -Enable.
  
<img width="1073" height="854" alt="image" src="https://github.com/user-attachments/assets/20fd0d67-f7af-4249-a992-f4fae438e6fa" />

## Launch instance 

<img width="1244" height="353" alt="image" src="https://github.com/user-attachments/assets/1f255fc6-afa5-41c5-a898-05683127c960" />

