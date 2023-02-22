# middleware_script1
#!/bin/bash
#author : tenneh 
#date : 2/19/23

# description sonarqube 

echo "installing sonarqube"

#update your server
sudo yum update -y

#Step 1: Java 11 installation openjdk-devel
sudo yum install java-11-openjdk-devel -y

#install java-11-openjdk    
sudo yum install java-11-openjdk -y

#cd into /opt directory
#cd /opt

#If wget is not installed on your system, run the command to install it. Then download SonarQube package:
sudo yum install wget -y

sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip -y

#If unzip is not installed on your system, run the command 
sudo yum install unzip -y

#To install it. Now, unzip the previously installed package:
sudo unzip /opt/sonarqube-9.3.0.51899.zip

#Change ownership to the user and Switch to Linux binaries directory to start service
#sudo chown -R vagrant:vagrant /opt/sonarqube-9.3.0.51899

#cd /opt/sonarqube-x.x/bin/linux-x86-64 
 
 #now now run sonar.sh start to start
 #./sonar.sh start

 #To connect to SonaQube copy your ip and add port 9000 

#Some servers have firewall enabled. So if you are not able to connect from the browser, then you might want to open the port 9000 with this command:
#sudo firewall-cmd --permanent --add-port=9000/tcpcd
#sudo firewall-cmd --reload


