## EC2 Instance Launch Types
- On Demand Instances: short workload, predictable pricing
- Reserved Instances: long workloads (>= 1 year)
- Convertible Reserved Instances: long workloads with flexible instances
- Scheduled Reserved Instances: launch within time window you reserve
- Spot Instances: short workloads, for cheap, can lose instances
- Dedicated Instances: no other customers will share your hardware
- Dedicated Hosts: bool an entire physical server, control instance placement

## EC2 On Demand
- Pay for what you use (billing per second, after the first minute)
- Has the highest cost but no upfront payment
- No long term commitment
- Recommended for short-term and un-interrupted workloads, where you cant predict how the application will behave


## EC2 Reserved Instances
- Up to 75% discount compared to On-demand
- Pya upfront for what you use with long term commitment
- Reservation period can be 1 or 3 years
- Reserve a specific instance type
- Recommended for steady state usage applications (think database)

- Convertible Reserved Instance
  - can change the EC2 instance type
  - Up to 54%
- Scheduled Reserved Instances
  - launch whithin time window you reserve

## EC2 Spot Instances
- Can get a discount of up to 90% compared to On-demand
- You bid a price and get the instance as long as its under the price
- Price varies based on offer and demand
- Spot instances are reclaimed with a 2 minute notification warning when the spot price goes above your bid
- Used for batch jobs, Big Data analysis, or workloads that are resilient to failures.
- Not great for Database or so.

## EC2 Dedicated Hosts
- Phisical dedicated Ec 2 server for your use
- Full control og EC2 instqance placement
- Visibly into the underlying sockets / physical cores of the hardware
- Allocated for your account for a 3 year period reservation
- More expensive
- Useful for software that have complicated licensing model (BYOL - Bring your own licences)
- Or for companies that have strong regulatory or compliance needs

## EC2 Dedicated Instances
- Instances running on hardware thats dedicated to you
- May share hardware with other instances in same account
- No control over instance placement (can move hardware after Stop / Start)
