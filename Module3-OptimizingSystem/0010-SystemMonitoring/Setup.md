# Preparatory Steps

## Overview

The objective is to establish a VPC and subnet, along with a security group tailored for a **Linux EC2 Instance**. Concurrently, an IAM User and IAM Role will be created.

## Steps

### 1. Create VPC and Security Group

- **VPC after creation:**

  ![VPC Image](./Image/VPC.png)

- **Subnet after creation:**

  ![Subnet Image](./Image/subnet.png)

- **Security Group after creation:**

  ![Security Group Image](./Image/SecurityGroup.png)

- **IAM Role for Grafana EC2:**

  ![Grafana Role Image](./Image/GrafanaRole.png)

### 2. Create EC2 Instance

- **EC2 Instance after creation:**

  ![EC2 Image](./Image/Ec2.png)

- **Attach Role to EC2 Instance:**

  - At the Instances Dashboard, select your EC2 instance, click **Actions**, choose **Security**, then click **Modify IAM role**.

    ![Step 1](./Image/Step1.png)

  - Choose `GrafanaEc2Role` and click **Update IAM Role**.

    ![Step 2](./Image/Step2.png)

### 3. Install Grafana

- You can use **Client Connect** in the EC2 dashboard to connect to your EC2 instance.

  ![Connect Client](./Image/ConnectClient.png)

- Install Grafana using Docker:

    ```bash
    sudo yum update -y
    sudo yum install docker -y
    sudo usermod -a -G docker ec2-user
    sudo systemctl enable docker
    sudo systemctl start docker
    docker run -d -p 3000:3000 --name=grafana grafana/grafana
    ```

### 4. Configure Grafana

- **Login to Grafana** with the username and password: `admin`.

  ![Grafana Login](./Image/Grafana-login.jpg)

- **Add Grafana Data Sources** with CloudWatch.

  ![Grafana Data Source](./Image/Grafana-datasource.jpg)

- **Configure Grafana**:

  ![Grafana Configuration](./Image/Grafana-config.jpg)

- **Edit Panel** with the EC2 Instance ID.

  ![Grafana Panel](./Image/Grafana-editPanel.jpg)

### 5. Result

- **CPU Utilization Visualization** of EC2 instances in the Grafana Dashboard.

  ![Grafana Dashboard](./Image/Grafana-result.jpg)
