### EC2 pricing
- EC2 instances prices (per hour) varies based on these parameters:
  - Region you re in
  - instance type you are using
  - On-Demand VS spot VS Reserved VS Dedicated Host
  - Lunux VS Windows VS Private OS(RHEL, SLES, Windows SQL)
- You are billed by the second, with a minumum of 60 seconds

- You also pay for other factors such as storage, dat transfer, fixed IP, public addresses, load balancing
- You do not pay for the instance if the instance is stopped

[information](http://aws.amazon.com/ec2/pricing/on-demand)

### What is an AMI
- As we saw, AWS comes with base images such as:
  - Ubunts
  - Fedira
  - RedHat
  - Windows
- These images can be customised at runtime using EC2 User data

- But what if we could create our own image, ready to go?
- That is an AMI - an image to use to create our instances
- AMI's can be built for Lunux or Windows machines

### Why would you use a custom AMI?
- Using a custom build AMI can provide the following advantages.
  - Pre-installed packages needed
  - Faster boot time (no need for long ec2 user data at boot time)
  - Machine comes configured with monitoring / enterprise software
  - Security concerns - control over the machines in the network
  - Control of maintenance and updates of AMIs over time
  - Active Directory Integration out of the box
  - Installing your app ahead of time (for faster deploys when auto-scaling)
  - Using someone else's AMI that is optimized for running an app, DB, etc...
- AMI are built for specific region!!!!!!!!!!!!!!!!!!!!!

### EC2 Instances Overview
- Instances have 5 distinct characteristics advertised on the website
  - RAM
  - CPU
  - I/O
  - Network
  - Graphic Processing Unit (GPU)
- It may be daunting to choose the right instance type (there are over 50 of them)
  [information](http://aws.amazon.com/ec2/instance-types/)
- [here](http://ec2instances.info) can help with summarizing the types of instances
- R/C/P/G/H/X/I/F/Z/CR are specified in RAM, CPU, I/O, Network, GPU
- M instance types are balranced
- T2/T3 instance types are "burstable"

### Burstable Instances(T2)
- AWS has the concept of burstable instances (T2 machines)
- Burst means that overall, the instance has OK CPU performance.
- When the machine needs to process something unexpected (a spike in load for example), it can burst, and CPU can be VERY good
- If machines bursts, it utilizes "burst credits"
- If all the credits are gone, CPU becomes BAD
- If the machine stipes bursting, credits are accumulated over time


# EC2 - CHECKLIST
- Know how to SSH into EC2 (and change .pem file permissions)
- Know how to properly use security groups
- Know the fundamental differences between private vs public vs elastic IP
- Know how to use User Data ti customize your instance at boot time
- Know that you can build custom AMI to enhance your OS
- EC2 instances are billed by the second and can be easily created and thrown away, welcome to cloud!!!