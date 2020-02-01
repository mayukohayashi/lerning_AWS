## SSH Troubleshooting


- 1) There's a connection timeout

This is a security group issue. Any timeout (not just for SSH) is related to security groups or a firewall. Ensure your security group looks like this and correctly assigned to your EC2 instance.


- 2) There's still a connection timeout issue

If your security group is properly configured as above, and you still have connection timeout issues, then that means a corporate firewall or a personal firewall is blocking the connection. Please use EC2 Instance Connect as described in the next lecture.



- 3) SSH does not work on Windows

If it says: ssh command not found, that means you have to use Putty

Follow again the video. If things don't work, please use EC2 Instance Connect as described in the next lecture



- 4) There's a connection refused

This means the instance is reachable, but no SSH utility is running on the instance

Try to restart the instance

If it doesn't work, terminate the instance and create a new one. Make sure you're using Amazon Linux 2



- 5) Permission denied (publickey,gssapi-keyex,gssapi-with-mic)

This means either two things:

You are using the wrong security key or not using a security key. Please look at your EC2 instance configuration to make sure you have assigned the correct key to it.

You are using the wrong user. Make sure you have started an Amazon Linux 2 EC2 instance, and make sure you're using the user ec2-user. This is something you specify when doing ec2-user@<public-ip> (ex: ec2-user@35.180.242.162) in your SSH command or your Putty configuration



- 6) Nothing is working - "aaaahhhhhh"

Don't panic. Use EC2 Instance Connect from the next lecture. Make sure you started an Amazon Linux 2 and you will be able to follow along with the tutorial :)



- 7) I was able to connect yesterday, but today I can't

This is probably because you have stopped your EC2 instance and then started it again today. When you do so, the public IP of your EC2 instance will change. Therefore, in your command, or Putty configuration, please make sure to edit and save the new public IP.