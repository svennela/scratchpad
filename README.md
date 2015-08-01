##### MySQL access on my mac
/usr/local/mysql/bin/mysql -h IpAddress -u root -p

##### shuting down tomcat through remove ssh. nohup will help to keep session active.
 nohup /opt/apache-tomcat-8.0.14/bin/startup.sh


##### renaming hostname in ubuntu:
sudo -s
sudo vi /etc/hostname
sudo vi /etc/hosts
shutdown -ry now
