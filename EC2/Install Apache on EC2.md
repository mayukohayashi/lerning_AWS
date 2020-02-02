## Launching an Apache Server on EC2
- Lets leverage our EC2 instance
- We will install an Apache Web Server to display a web page
- We will create an index.html that shows the hostname of our machine

> ec2-user@ip-***** ➜  ~ sudo su
> [root@ip-****** ec2-user]# yum update -y
>  yum install -y httpd.x86_64
> systemctl start httpd.service
> systemctl enable httpd.service
> Created symlink from /etc/systemd/system/multi-user.target.wants/httpd.service to /usr/lib/systemd/system/httpd.service.
> curl localhost:80
> echo "Hello World" > /var/www/html/index.html
> [root@ip-************]# hostname -f
> ip-************.ap-where-1.compute.internal