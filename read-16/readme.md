# AWS: Cloud Servers


## What is an EC2 Instance?

An Amazon EC2 instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure.


## Name 2 use cases for EC2.

Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) Cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.

## Provide 1 reason to use ECS instead of Heroku.

allows you to easily deploy containerized workloads on AWS. The powerful simplicity of Amazon ECS enables you to grow from a single Docker container to managing your entire enterprise application portfolio.

---

## Where can we find EC2 on the AWS Console?

Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/ .

- In the navigation pane, choose Instances.

- Select the instance and choose Connect.

- Choose EC2 Instance Connect 

- Verify the user name and choose Connect to open a terminal window

## Explain the general difference between T2 Micro and XL

1. **T2 Micro**

T2 instances are Amazon EC2 instance types designed to dramatically reduce costs for applications that benefit from the ability to burst to full core performance whenever required. T2 instances are available to use in the AWS Free Tier, which includes 750 hours of Linux and Windows t2.micro instances each month for one year for new AWS customers.

---

## What is Elastic Beanstalk?

AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.


## Describe the relationship between EC2 and Elastic Beanstalk

Elastic Beanstalk is one layer of abstraction away from the EC2 layer. Elastic Beanstalk will setup an "environment" for you that can contain a number of EC2 instances, an optional database, as well as a few other AWS components such as a Elastic Load Balancer, Auto-Scaling Group, Security Group.


## Name some benefits of using Elastic Beanstalk.

timesaving server configuration, powerful customization, and a cost-effective price point