## AWS Route 53 Overview

- Route 53 is a Managed DNS (Domain Name System)
- DNS is a collection of rules and records which helps clients understand how to reach a server through URLs
- In AWS, the most common records are:

  - A: URL to IPv4
  - AAAA: URL to IPv6
  - CNAME: URL to URL
  - Alias: URL to AWS resources

- Route53 can use:
  - Public domain names you own (or buy)
    > aoolication1.mydomaain.com
  - private domain names that can be resolved by your VPCs
    > application1.company.internal
- Route53 has advanced features such as:
  - Load balancing (through DNS - also called client load balancing)
  - Health checks (although limited....)
  - Routing policy: simple, failover, geolocation, geoproximitly, latenciy, weighted
- Prefer Alias Over CNAME for AWS resources (for performance reasons)

## CHECK LIST

- Overall Route53 is not much used in the AWS Certificated Developer Exam
- You should know all the record types:

  - A: URL to IPv4
  - AAAA: URL to IPv6
  - CNAME: URL to URL
  - Alias: URL to AWS resources

- You should know to use Alias records over CNAME for AWS resources

> I made DOMAIN
> goboiskonsai.net
