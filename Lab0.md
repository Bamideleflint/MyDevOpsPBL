# **Setup AWS infrastructure - Create two EC2 instances**

**What is EC2 instance?** 
An EC2 instance, in the context of cloud computing, refers to a virtual server provided by Amazon Web Services (AWS) as part of its Elastic Compute Cloud (EC2) service. EC2 instances enable users to rent virtual servers on which they can run their applications. These instances are highly scalable and customizable, allowing users to choose configurations such as CPU, memory, storage, and networking capacity based on their requirements.

EC2 instance is a virtual server provided by AWS. We will be creating two EC2 instances:
- One EC2 instance to setup Jenkins  
- Another EC2 instance for setting up Tomcat

Steps:
1: Login to AWS console by clicking this link -->  https://aws.amazon.com/console/
click on All services, Click on Compute -->  Click on EC2
![EC2](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/0247c07e-a465-4960-815c-2e10e2320509)

2. Click on Launch instance
![Launch Instance](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/6f02c4bc-550d-48ea-ba75-258625e775c9)

3. Enter Name as EC2 and enter 2 as number of instances (one for Jenkins and another for Tomcat)
![Name Instances](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/e18f3852-f100-4b32-b78a-5301abde41cd)

4. Select Ubuntu 
![Choose Ubuntu](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/7cf5b211-1147-45fd-b33e-97c41c331911)

5. choose Ubuntu server 22.0.4 as AMI
![AMI Ubuntu](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/41e6a54c-4682-4e32-9ca7-00aa2219fd64)

6. Enter t2.small as instance type
![Instance Type](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/1a50089d-f5d3-4031-b761-4051ac661ac6)

7. Click on Create new Key Pair
![Create Key pair](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/7eee5606-ddf9-49d1-8024-e3b2150d253f)

8. Choose the existing key pair if you have one, otherwise create new one, give some name as myJenkinsKey. Make sure you download the key in your local machine. Please do NOT give space or any character while naming the key.
![New Key](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/02ef3a1a-b724-4aa4-b897-6600c33713b5)

9. Under Network settings, Click Edit
![Network Settings Edit](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/95a92fed-c426-429f-a2ea-a54745582b85)

![New Security Group Rule](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/071dec20-6402-4ea3-b6ea-c29baf585116)

Add port range as 8080 and select AnyWhere as Source Type, that should enter 0.0.0.0/0 as Source
![Port 8080](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/40c71a6e-817d-45e1-af0e-7b36a226cd57)

10. Enter 10 GB as storage 
![Storage](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/eb0ac1dd-8912-40c6-9a79-66ad1dae3daa)

And then make sure in Summary, values appear as below:

![Summary](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/74b3d5d6-6c72-4b27-b29e-c8ae984d4815)

11. Click on Launch Instance.
![Instances Created](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/f45bf817-7d35-4b1b-aeb5-e97f3c941025)

Click on View instances
![View Instances](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/48f54a3b-5aa3-4796-8d55-9f9dd99d1c88)

Now you should be able to view instances in AWS console. Now you can re-name as Jenkins-EC2 and Tomcat-EC2
![Instances Running](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/a27fe9e5-3077-424d-98f8-82385c5a37b7)


## ***congratulations.***
