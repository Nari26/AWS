# AWS VPC

Amazon VPC lets you provision a logically isolated section of the Amazon Web Services (AWS) cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including a selection of your own IP address ranges, creation of subnets, and configuration of route tables and network gateways. 

## Components of Amazon VPC

>1. **Virtual private cloud (VPC)** - A logically isolated virtual network in the AWS cloud. You define a VPC’s IP address space from the ranges you select.
>2. **Subnet** - A segment of a VPC’s IP address range where you can place groups of isolated resources.
>3. **Internet Gateway** - The Amazon VPC side of a connection to the public Internet.
>4.**Route table** - A set of rules, called routes, that are used to determine where network traffic is directed.
>5. **CIDR block** - Classless Inter-Domain Routing. An internet protocol address allocation and route aggregation methodology.


## How to Create an AWS VPC using Console

### Step-1: Creating a VPC 

>>1. Open the Amazon VPC console at https://console.aws.amazon.com/vpc/ and login to your account. 
>>2. Make sure to choose **N.Virginia (us-east-1)** region. (top right section of the page)
>>3. In the left navigation pane, choose **Your VPCs**. 
>>4. Choose **Create VPC** (At top right section).
>>5. Specify the following VPC details as needed.
>>>- Name tag: VPC88 (Unique name based on the requirement)
>>>- IPv4 CIDR block: 10.0.0./24 (example)
>>6. Choose **Create VPC**.

>> ![alt text](./Create-VPC.png)

>Step-2: Creating Public and Private Subnets 
>>**Private Subnet:**
>>- Navigate to AWS VPC 
>>- In the left navigation pane, choose **Subnets**, then click on **Create subnet**.
>>- Specify the subnet details as necessary 
>>>- **VPC:** VPC88 (choose your vpc from the dropdown list)
>>>- **Name tag:** VPC88-PrivateSubnet1 (include vpc name prefix to identify the subnets easily)
>>>- **Availability Zone:** us-east-1a (choose a availability zone when you create multiple subnets)
>>>- **IPv4 CIDR block:** 10.0.0.0/25 (make sure to provide the CIDR within your VPC CIDR range)
>>- Choose **Create Subnet** at the bottom of the page. 

>>> ![alt text](./private-subnet1.png)

>>**Public Subnet:**
>>- Navigate to AWS VPC 
>>- In the left navigation pane, choose **Subnets**, then click on **Create subnet**.
>>- Specify the subnet details as necessary 
>>>- **VPC:** VPC88 (choose your vpc from the dropdown list)
>>>- **Name tag:** VPC88-PublicSubnet1 (include vpc name prefix to identify the subnets easily)
>>>- **Availability Zone:** us-east-1b (choose a availability zone when you create multiple subnets)
>>>- **IPv4 CIDR block:** 10.0.0.129/25 (make sure to provide the CIDR within your VPC CIDR range)
>>- Choose **Create Subnet** at the bottom of the page. 
>>- Once you create the public subnet, we need to enable public ipv4 settings as below 
>>>- Navigate Subnets in the VPC page, search for your public subnet(VPC88-PublicSubnet1). 
>>>- Click the check box next to the subnet name, go to **Actions** at the top right and click on **Modify auto-assign IP settings**.  
>>>>> ![alt text](./public-subnet1-Ipv4-settings.png)
>>>- Click on the check box next to **Enable auto-assign public IPv4 address**, then choose **Save**.
>>>>> ![alt text](./public-subnet1-Ipv4-settings-update.png)



