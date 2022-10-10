# AWS_SAA_HandsOn
Following the great Stephane Maarek SAA full course. I have documented my hands on training. Enjoy!

AWS Solutions Architect Associate 


Idenity and Access Management (IAM)


Created an AWS account (Free tier) and downloaded the code required for the course.

Created a user named Turysanchez5 and added AdminPrivileges policy to the user.
  
Created a group named Admins and Developers, added AdministratorAccess policy to Admins group and ended up deleting the Developers group.
  
Added MFA to the root account by downloading Duo Mobile to my phone and linking them both together, easy and simple process.
  
Learned how to create and access users Access Keys.

Downloaded the AWS CLI on my windows computer by searching through google for the latest version. Once download was finished I ran aws --version to check the version. Also ran aws iam list-users to return a list of all users.

Brief overview of Cloudshell, which is a terminal inside of the cloud, pretty awesome! 

Created a role called DemoRoleForEC2, which to this role I added the policy of IAMReadOnlyAccess. I then added the role to a EC2 instance.

Generated a Credential Report and downloaded to inspect, which showed a lot of good information regarding logins, access keys, access times, last rotations, MFA status etc.

Went to my user Turysanchez5 and located Access Advisor on the far right tab which shows all services assigned to the user and last accessed, from here you can decide if certain services aren't needed for the user and remove them.


EC2 Fundamentals 


Under the user Turysanchez5 I tried setting a budget alert but did not have access. Had to login to my root account and under account > IAM User and Role Access to Billing Information I activated this setting to be enabled.

Back to my user account I went to create a budget named CourseBudget. Created an alert to email me when it reaches the threshold I defined. 

Next I went ahead and launched an EC2 instance and named it MyFirstInstance. Selected the Operating System of Amazon Linux (Free Tier Eligible), selected the t2.micro instance type, created a Key Pair (Named EC2 Tutorial, Key pair=RSA, private key=.pem), under Network Settings I allowed SSH traffic from Anywhere and allowed HTTP traffic from the internet as I am going to launch a web server, under Advance Details I added a script to User Data in order to run some updates and installations on start up, launched my first instance! 

Opened a browser and ran http://x.xxx.xx.xxx (public IP) in order to connect to my instance and was succesfull.

