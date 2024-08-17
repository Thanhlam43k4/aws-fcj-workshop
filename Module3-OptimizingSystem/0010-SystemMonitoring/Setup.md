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

- Install Grafana

    - Use can use client connect in EC2 dashboard to connect to your EC2 instance

    <img alt = "Ec2 Image" src = "./Image/ConnectClient.png" width = "500">

    - You can install Grafana with these commands

            sudo yum update -y

            sudo nano /etc/yum.repos.d/grafana.repo

          ####  (add the content below to the file grafana.repo)

                [grafana]
                name=grafana
                baseurl=https://rpm.grafana.com
                repo_gpgcheck=1
                enabled=1
                gpgcheck=1
                gpgkey=https://rpm.grafana.com/gpg.key
                sslverify=1
                sslcacert=/etc/pki/tls/certs/ca-bundle.crt 


            sudo yum install grafana -Y

            sudo systemctl daemon-reload


