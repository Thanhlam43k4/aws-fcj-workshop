## NAT Gateway

- By default, any EC2 instance running inside a Private Subnet will not be able to communicate with the Internet through the Internet Gateway (IGW). This situation becomes problematic when the EC2 instance needs to access the Internet for security updates, patch downloads, or application software updates.

- Recognizing this need, AWS offers two methods for granting EC2 instances in a Private Subnet access to the Internet: **NAT Instance** and **NAT Gateway**. In most scenarios, it is advisable to opt for NAT Gateway over NAT Instance due to its enhanced availability, bandwidth, and reduced administrative overhead.

- To set up a NAT Gateway, you are required to specify a public subnet and an Elastic IP address. Ensure that the chosen Elastic IP address is not associated with any other instances or network interfaces.
