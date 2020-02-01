## Private vs Public IP(IPv4)
- Networking has 2 sort of IPs. IPv4 and IPv6
  - IPv4: 1.160.10.240
  - IPv6: 1900:3232:4:200:f4rr:fr43:32gq

- we will use only be using IPv4
- IPv4 is still the most common format used online
- IPv6 is newer and solves problems for the Internet of Things(IoT)

- IPv4 allows for 3.7billion different address in the public space.
- IPv4: [0-255].[0-255].[0-255].[0-255].


## Private vs Public IP (IPv4) Fundamental Differences
- Public IP
  - Public IP means the machine can be identified on the internet (WWW)
  - Must be unique across the whole web (not two machine can have the same public IP)
  - Can be geo-located easily
- Private IP
  - Private IP means the machine can only be identified on a private network only
  - The IP must be unique across the private network
  - BUT two different private networks (2 companies) can have the same IPs
  - Machines connect to WWW using an internet gateway (a proxy)
  - Only a specified range of IPs can be used as private IP

## Elastic IPs
- When you stop and then start an EC2 instance, it can change its public IP
- If you need to have a fixed public IP for your instance, you need an Elastic IP
- An Elastic IP is a public IPv4 IP you own as long as you dont delete it
- You can attach it to one instance at the time

## Elastic IP
- With an Elastic IP address you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account
- You can only have 5 Elastic IP in your account (can increase ask AWS)
- Overall, try to avoid using Elastic IP
  - They often reflect poor architectural decisions
  - Instead, use a random public IP and register a DNS name to it
  - Or, as we will see later, use a Load Balancer and dont use a public IP

## Private vs Public IP (OPv4) In AWS EC2 - hands on
- By default, your EC2 machine comes with:
  - A private IP for the internal AWS Network
  - A public IP, for the WWW.
- When we are doing SSH into our EC2 machines:
  - We cant use a private IP, bacause we are not in the same network
  - We can only use the public IP
- If your machine is stopped and then started, the public IP can change



