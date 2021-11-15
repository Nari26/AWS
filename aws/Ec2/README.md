# How to launch a new EC2 instance
>>- Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/
>>- From the console dashboard, choose Launch Instance.
>>- Specify the following instance details:
>>>1.  **Choose AMI:** Select an HVM version of Amazon Linux 2, Notice that these AMIs are marked "Free tier eligible."(Ex. ami-04ad2567c9e3d7893)
>>>2. **Choose instance type:** Select the **t2.micro** instance type, which is selected by default.Then click on **Next:configure instance details**
>>>3. **Configure Instance Details:** specify the following properties.
>>>>- Network: VPC-84 (Select your VPC from the dropdown list).
>>>>- Subnet: VPC84PublicSubnet1. (Select your VPC public subnet).
>>>>- Auto-assign Public IP: Use subnet setting. (Ensure auto assign public Ipv4 option is enabled for your public subnet).
>>>>- Click on **Next: Add storage**
>>>4. **Add Storage:** Update root EBS volume storage as desired (ex. 8Gib). Then click on **Next: Add Tags**
>>>5. **Add Tags:** Click on **Add Tag** and add the following tags
>>>>- Key: Name 
>>>>- Value: Public-EC2 
>>>>- Click on **Next: Configure security group**
>>>6.  **Configure Security Group:** Ensure that **Select an existing security group** option is selected.
>>>>- Assign a security group: Select an existing security group.
 >>>>- Select default Security group, then choose **Review and Launch**
>>>7. **Review:** Choose Launch.
>>>>- When prompted for a key pair, select Create a new key pair and specify the following details.
>>>>>- key pair type: RSA
>>>>>- key pair name: Test-kp (Enter your keypair name), then click on **Download keypair** option.
>>>>- Choose **launch Instances**.

