## SSH Summary Table
- SSH is not work with "Windows < 10"
- Putty works with all Windows
- EC2 Instance Connect work with "Windows", "MAC", and "Linux"

### How to SSH into your EC2 Instance / Linux and Mac OS X
- We will learn how to SSH into your EC2 instance using Linux / Mac
- SSH is one of the most important function.
  > It allows you ro control a remote machine, all using the command line

### from hands-on
- ~ ᐅ chmod 0400 mypemname.pem
- whoami とかでユーザーなにか見たりして慣れる。

[ec2-user@ip-]~% echo $SHELL
/usr/bin/zsh
[ec2-user@ip-]~% sudo chsh ec2-user
Changing shell for ec2-user.
New shell [/usr/bin/zsh]: /bin/zsh
Shell changed.

which chsh
chsh: Command not found.
chshを使えるようにするには、「util-linux-user」をインストール
$ sudo yum install util-linux-user
インストール後はchshが使える。
$ which chsh
/usr/bin/chsh