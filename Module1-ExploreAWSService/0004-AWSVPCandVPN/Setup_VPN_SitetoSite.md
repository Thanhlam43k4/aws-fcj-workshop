## VPN Connection in AWS

In this guide, we will discuss how to connect an on-premises data center to Amazon VPC using either a hardware or software VPN, depending on the specific requirements. To establish a Site-to-Site VPN connection, the following steps need to be taken:

### 1. Virtual Private Gateway (VPG) and Customer Gateway (CGW) Setup

- **Virtual Private Gateway (VPG)**: This serves as the control center that connects the virtual private network (VPN) within AWS.
  
- **Customer Gateway (CGW)**: This component represents the hardware or software VPN device located at the client's end.

### 2. VPN Tunnel Establishment

- A VPN tunnel will be initiated as soon as data traffic is exchanged between AWS and the client's network. It is important to specify the routing type to ensure secure and efficient data transmission:
  
  - If the CGW on the client side supports Border Gateway Protocol (BGP), dynamic routing should be configured for the VPN connection.
  
  - If not, static routing must be set up. For static routing, specific routes must be entered to establish the connection from the client's side to the VPG at AWS. Additionally, the VPC routing must be configured to allow seamless data exchange within the VPN tunnel.

### 3. VPG, CGW, and VPN Features

- Some key features of VPG, CGW, and VPN include:
  
  - **VPG**: The terminal component of the VPN tunnel within AWS.
  
  - **CGW**: Can be either a hardware device or a software application located at the client's end in the VPN tunnel.

  - **VPN tunnel connections** are initiated from CGW to VPG.

  - **VPG** supports both dynamic routing (BGP) and static routing.

  - **Each VPN connection** comprises two tunnels for high availability.

### 4. Lab Setup and Configuration

- The lab provides hands-on experience in setting up a Site-to-Site VPN connection in AWS. This solution is popular due to its cost-effectiveness and ease of configuration, as AWS offers instructions for various types of client devices. The primary responsibility of the customer is to prepare the internet connection, which will establish a secure tunnel (using IPSec) connecting to AWS via the VPN tunnel.

- In the lab setup, there are two VPCs: the Main Office (VPC ASG) and the Branch Office (VPC ASG VPN), located in different Availability Zones (AZs) to ensure network diversity. While EC2 instances can be created in each VPC with external SSH access, they cannot communicate or ping each other using private IP addresses. The goal is to configure the VPN to enable private IP addresses to communicate over the Site-to-Site VPN.
