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

brew install httpie

http://www.kitploit.com/2015/08/httpie-cli-curl-like-tool-for-humans.html?utm_content=buffer3e195&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer#.VcsqqCIFMMQ.twitter


##### building uaa war file and deploying on VM

git clone https://github.com/cloudfoundry/uaa.git

Changing database settings in uaa/src/main/resources/uaa.yml

spring_profiles: mysql,default

database:
  driverClassName: org.mariadb.jdbc.Driver
  url: jdbc:mysql://localhost:3306/uaa
  username: root
  password: root

Skiping tests as we want only war file

./gradlew build -x test

deploy uaa/build/libs/cloudfoundry-identity-uaa-2.6.1.war to tomcat installation.. 



gyp ERR! configure error
gyp ERR! stack Error: `gyp` failed with exit code: 1
gyp ERR! stack     at ChildProcess.onCpExit (/Users/svennela/workspace/myapps/ionic-apps/ionic-projects-demo/node_modules/gulp-sass/node_modules/node-sass/node_modules/pangyp/lib/configure.js:346:16)
gyp ERR! stack     at emitTwo (events.js:87:13)
gyp ERR! stack     at ChildProcess.emit (events.js:172:7)
gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:200:12)
gyp ERR! System Darwin 14.3.0
gyp ERR! command "/usr/local/bin/node" "/Users/svennela/workspace/myapps/ionic-apps/ionic-projects-demo/node_modules/gulp-sass/node_modules/node-sass/node_modules/pangyp/bin/node-gyp" "rebuild"
gyp ERR! cwd /Users/svennela/workspace/myapps/ionic-apps/ionic-projects-demo/node_modules/gulp-sass/node_modules/node-sass
gyp ERR! node -v v4.0.0
gyp ERR! pangyp -v v2.3.2
gyp ERR! not ok
Build failed
gulp-rename@1.2.2 node_modules/gulp-rename



solution

npm install iconv



Exception encountered connecting to CoreSimulatorBridge: Unable to connect to CoreSimulatorBridge


cordova platform add ios
cordova build --emulator
ios-sim launch platforms/ios/build/emulator/ionFullApp.app --devicetypeid "com.apple.CoreSimulator.SimDeviceType.iPhone-6"

//remove with sudo
sudo ionic platform remove ios

//add iOS back without sudo
ionic platform add ios

//worked for me
ionic emulate ios

