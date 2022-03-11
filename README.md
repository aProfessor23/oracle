# rootoracle
甲骨文开启密码登录
# 创建VPS的时候使用一下代码就行了，其他默认不用管
```
#!/bin/bash
echo root:要修改的密码 |sudo chpasswd root
sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;
sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;
sudo service sshd restart
```
