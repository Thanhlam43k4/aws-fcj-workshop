# Preparatory steps


## Overview

-  The objective is to establish a VPC and subnet, along with a security group tailored for a **Linux Ec2 Instance**.
  
-  Concurrently, an IAM User and IAM Role should be created.



### Create VPC and Security Group

- VPC after creation

    <img alt = "vpc image" src = "./Image/VPC.png" width = "500">

- Subnet after creation

    <img alt = "Subnet Image" src = "./Image/subnet.png" width = "500">

- Security Group after creation

    <img alt = "Security Group Image" src = "./Image/SecurityGroup.png" width = "500">

- IAM Role for Grafana EC2 

    <img alt = "Grafana image" src = "./Image/GrafanaRole.png" width = "500">

### Create EC2 instance

- Ec2 Instance after creation

    <img alt = "Ec2 Image" src = "./Image/Ec2.png" width = "500">

- Attach Role to Ec2 instance 

    -  At the Instances Dashboard, click to your Ec2 instance and click **Action** choose **Security** then click **Modify IAM role**

        
    <img alt = "Ec2 Image" src = "./Image/Step1.png" width = "500">

    - Choose `GrafanaEc2Role` and click **Update IAM Role**

    <img alt = "Ec2 Image" src = "./Image/Step2.png" width = "500">

- **Install Grafana**

    - Use can use client connect in EC2 dashboard to connect to your EC2 instance

    <img alt = "Ec2 Image" src = "./Image/ConnectClient.png" width = "500">

    - You can install Grafana with docker 
     
          sudo yum update -y

          sudo yum install docker -y
  
          sudo usermod -a -G docker ec2-user

          sudo systemctl enable docker 

          sudo systemctl start docker 

          docker run -d -p 3000:3000 --name=grafana grafana/grafana

- **Config Grafana**

    - Login Grafana with user and password are admin
  
    <img alt = "Grafana login" src = "./Image/Grafana-login.jpg" width = "500">

    - Add Grafana Data sources with Cloud Watch
  
    <img alt = "Grafana Data Source" src = "./Image/Grafana-datasource.jpg" width = "500">

    - Configure Grafana
  
    <img alt = "Grafana Configuration" src = "./Image/Grafana-config.jpg" width = "500">

    - Edit Panel with Id Instance of EC2
  
    <img alt = "Grafana Panel" src = "./Image/Grafana-editPanel.jpg" width = "500">

- **Result**

    - The visualization of CPU Utilization of Ec2 instances in Grafana Dashboard

    <img alt = "Grafana Dashboard" src = "./Image/Grafana-result.jpg" width = "500">

