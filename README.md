# week-7-SRE_AWS_VPC 
# (VPC) CIDR Blocks for VPC
## Internet Gateway 
### subnets 
#### Rounte tables 
#### Network Access Control (NACLs)
## Security Groups 


![image](https://user-images.githubusercontent.com/17476059/132219539-c66623d9-c7d5-4ad9-90ff-594b3f01fcf8.png)

___
What is a VPC 
- AWS isolated virtual network 
    - it allows control over virtual enviroments 
    - creating mutiple subnets with 

What is an Internet Gateway ?
- The internet gateway is path that is used by default.
- it allows internet access into the VPC 

what is a subnet?
- A subnet is a smaller part of a larger network (SUB-NET)
- Subnet splits the group into a smaller piece and helps with orginalzation and siloing of networks. Having this impoves network flow as well as reduce 

Route tables:
- Contains a set of rules that determin network flow. 

Network Access Controller
- NACLs are stateless 
- allow inbound and outbound rules 


### TO DO
#### Step 1: Create a VPC with IPV valid CIDR blocks 
`10.7.0.0/16`

#### Step 2: 
Create Internet Gateway (IG)   
- 2.1. Attach the IG to your VPC

#### Step 3: Create route table 
 - 3.1 Edit route and insert you IG in `target`

#### Step 4: Create public subnet 
- `10.7.0.0/24`
    - 4.1 Associate public subnet with out RT 
#### Step 5: Create public NACLs 
- create inbound and outbound rules 
## Step 6:
create a Secure group  for our app

___

# AWS Regions 

![alt text](Images\screen-shot-2016-03-20-at-3-06-22-pm.png)


## Avliablity zone:
Availability zones (AZs) are isolated locations within data center regions from which public cloud services originate and operate

### Deployment 

The depoyment needs to be higly reliable and fast. Thus, you need to deploy to the server that is closer to the  client. 



# Creating a custom VPC with subnets
![image](https://i.ytimg.com/vi/gUesnoDzNr4/maxresdefault.jpg)

## Overall steps
- Create and configure VPC
- Internet Gateway(IG)
- Create the Subnets

## Creating the VPC


### Open the Amazon VPC console at https://console.aws.amazon.com/vpc/

### Select the second option, VPC with a Single Public Subnet, and then click Select

### Enter the following information into the wizard and click Create VPC.
```
IP CIDR block - 10.0.0.0/16
VPC name - ADS VPC
Public subnet - 10.0.0.0/24
Availability Zone - select Preferenced zone
Set an IPv4 CIDR block
(in my case  CIDR = 10.7.0.0/16)

```

### Create an Internet Gateway
 - In the side tab navigate to the `Internet Gateway`  and create a new gateway
 - give it a name and attach it to the VPC that you created 


![image](https://docs.axway.com/bundle/SecureTransport_54_on_AWS_InstallationGuide_allOS_en_HTML5/page/Content/Resources/Images/AWS/ig-attached.PNG)

### Create Subnets
- Navigate to the subnet in the dashbaord and select the `Create subnet` button 
- select your VPC 
- Select your preferred availability zone
- set the IPv4 CIDR block to your preferred value
(In my case it was 10.7.0.0/16 and the private subnet is 10.7.1.0/16)  


## - Making a  Route Table 

## - Creating a Network Access Control List

## Public Subnet Rules

## Private Subnet Rules

## loading the instance using AMI

![image](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/07/009-AMIPermissions-590x159.png)