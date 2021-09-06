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
`10.0.0.0/16`
`10.0.(Change).0/16`

#### Step 2: 
Create Internet Gateway (IG)   
- 2.1. Attach the IG to your VPC

#### Step 3: Create route table 
 - 3.1 Edit route and insert you IG in `target`

#### Step 4: Create public subnet 
- `10.0.(Change).0/24`
- 4.1 Associate public subnet with out RT 
#### Step 5: Create public NACLs 
- create inbound and outbound rules 
## Step 6:
create a Secure group  for our app
