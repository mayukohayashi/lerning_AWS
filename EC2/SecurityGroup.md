## Introduction to Security Groups
- Security Groups are the fundamental of network security in AWS
- The control how traffic is allowed into or out of our EC2 Machines.

        inbound traffic
        ======================================>
    WWW                       Security Group      EC2 Machine
        outbound traffic
        <======================================

- It is the most fundamental skill to learn to troubleshooting networking issues
- We will learn how to use them to allow, inbound and outbound ports


## Security Groups Deeper Dive
- Security groups are acting as a "firewall" on EC2 instances
- They regurate
  - Access to Ports
  - Authorised IP ranges - IPv4 and IPv6
  - Control of inbound network (from other to the instance)
  - Control of outbound network (from the instance to the other)

## Security Groups Good to Know
- Can be attached to multiple instance
- Locked down to a region / VPC combination
- Does live "outside" the EC2 -- if traffic is blocked the EC2 instance wont see it
- Its good to maintain one separate security group for SSH access
- If your application is not accessible(time out) error, then its an application error or its not launched
- All inbound traffic is blocked by default
- All outbound traffic is authorised by default
