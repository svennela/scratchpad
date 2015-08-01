##### MySQL access on my mac
/usr/local/mysql/bin/mysql -h IpAddress -u root -p

##### shuting down tomcat through remove ssh. nohup will help to keep session active.
 nohup /opt/apache-tomcat-8.0.14/bin/startup.sh


##### renaming hostname in ubuntu:
* sudo -s
* sudo vi /etc/hostname
* sudo vi /etc/hosts 
* shutdown -ry now 

##### Commands to make all users root

* sudo vi /etc/sudoers 
* %sudo ALL=NOPASSWD: ALL  

##### Allow members of group sudo to execute any command 

* %sudo   ALL=(ALL:ALL) NOPASSWD: ALL 

##### SSH without password. Copy pub keys to remote machine.

scp /Users/yourmachinename/.ssh/id_rsa.pub ubuntu@<IPADDRESS>:/ubuntu/.ssh/authorized_keys
