## EC2 User Data
- It is possible to bootstrap our instances using an EC2 User data script.
- bootstrapping means launching commands when a machine starts.
- That script is only run once at the instance first start
- EC2 user data is used to automate boot tasks such as:
  - installing updates
  - installing software
  - Downloading common files from internet
  - Anything you can think of
- The EC2 User Data Script runs with the root user

## EC2 User Data hands-on
- We want to make sure that this EC2 instance has an Apache HTTP server installed on it - to display a simple web page
- For it, we are going to write a user-data script
- This script will be executed at the first boot of the instance


> #!/bin/bash
> # install httpd (Linux 2 version)
> yum update -y
> yum install -y httpd.x86_64
> systemctl start httpd.service
> systemctl enable httpd.service
> echo "Hello World from $(hostname -f)" > /var/www/html/index.html