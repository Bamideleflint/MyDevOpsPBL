## Install Jenkins on Ubuntu 22.0.4 | Setup Jenkins on AWS EC2 Ubuntu instance | How to setup Jenkins in Ubuntu EC2 instance.

  
Jenkins, coded in Java, is an open-source DevOps tool designed for continuous integration/continuous delivery and deployment (CI/CD). This automation software facilitates the creation of CI/CD workflows, termed as pipelines, enabling seamless software development processes.  

  
Follow the steps to install Java, Jenkins, Maven on Ubuntu 22.0.4 instance. Jenkins, Maven are Java based applications, so we need to install Java first. 

  
**Change Host Name to Jenkins**  
`sudo hostnamectl set-hostname Jenkins`  

  
**Perform update first**  
`sudo apt update`  
  
**Install Java 11**
`sudo apt install default-jdk -y`

⁠⁠⁠⁠
Once  java is installed, enter the command below to verify the version:  

  
**Verify Java Version**
`java -version`

  
![JavaVersion](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/8f8e5d32-a94e-4c9f-bcf9-8ece1fdc7663) 

  
**Maven Installation**  
Maven is a popular build tool used for building Java applications. Please [click](https://www.cidevops.com/2020/03/what-is-maven-why-we-need-maven.html) here to learn more about Maven. 

You can install Maven by executing below command:  
`sudo apt install maven -y`

  
you can type `mvn --version` to verify the version  
you should see the below output.

  
![MavenVersion](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/49774981-db8a-46ac-8f70-e3d7f56654a1) 

  
**Jenkins Installation**  
  

**Add Repository key to the system**  
`curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \   /usr/share/keyrings/jenkins-keyring.asc > /dev/null`

  
**Append debian package repo address to the system**  
`echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \   https://pkg.jenkins.io/debian binary/ | sudo tee \   /etc/apt/sources.list.d/jenkins.list > /dev/null`

  
**Update Ubuntu package**
`⁠sudo apt update`

⁠
![UbuntuPackageUpdate](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/6cf93697-c62e-42df-b06b-9c8f7c191ffc)

  
**Install Jenkins**  
`sudo apt install jenkins -y`  


### **Access Jenkins in web browser**

Now Go to AWS console. Click on EC2, click on running instances link. Select the checkbox of EC2 you are installing Java and Jenkins. Copy the public IP address or public IP DNS

  
![IPaddressOrDNS](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/701ca16e-6acc-4286-a36b-80851d32b29e)
 
  
Go to the browser. enter public dns name or public IP address with port no 8080.
[http://public\_dns\_name:8080](http://public_dns_name:8080/)  

  
**Unlock Jenkins**  
You may get screen, enter the below command in Git bash( Ubuntu console)

  
![UnlockJenkins](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/bdb152d2-9b38-40d7-880c-355e2c1f5746) 

  
**Get the initial password from the below file**  
`sudo cat /var/lib/jenkins/secrets/initialAdminPassword`  

  
![AdminPassword](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/f68fa197-bff1-4218-9fba-73ef6c99beeb) 

  
Copy the password and paste in the browser, then click on install suggested plug-ins. 

  
![CustomizeJenkins](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/5089fae2-eb39-4b78-9a11-f5af91cf11d8)

  
Create username and password, you can enter everything as admin for a start. at least username as admin password as admin

  
![FirstAdminUser](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/7d32cc26-12fb-440d-bd5a-7050dbe7f74f)
  

![JenkinsInstanceConfig](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/43d4ac52-d32e-4561-9c29-7bc8ccc00ce6)  

  
**Jenkins webpage should look like the picture below**


![JenkinsPage](https://github.com/Bamideleflint/MyDevOpsPBL/assets/122679229/55008d3e-a3fd-426c-a214-08bf5fdc418f)
  

  

### **_There you have a successful Jenkins setup, congratulations._**
