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

##### Adding new user in rabbit mq.

* sudo rabbitmqctl add_user myuser mypass
* sudo rabbitmqctl set_permissions -p / myuser ".*" ".*" ".*"
* sudo rabbitmqctl set_user_tags myuser administrator

##### redis latency test.

redis-cli -h IPADDRESS --intrinsic-latency 30 

393825778 total runs (avg latency: 0.0762 microseconds / 761.76 nanoseconds per run).
Worst run took 1969x longer than the average latency.
