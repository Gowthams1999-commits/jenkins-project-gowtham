# Ultimate CI and Cd pipeline using Github,Jenkins,Maven,Sonar qube,docker,shell,argocd and kubernetes.

1. Install docker on your machine and installed docker related plugin in jenkins to integrate with docker.

2. added jenkins user in docker group so that jenkins user access docker related command with out any issues.

3. Sonar qube installation.

   Sonar Qube installation steps:

* Download and install Sonar qube 

wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.7.0.96327.zip 

* Install unzip and extract.

Ex:
apt install unzip -y 

unzip sonarqube-<version>.zip

* Move SonarQube to /opt:

mkdir /opt/sonarqube

mv sonarqube-<version> /opt/sonarqube

* Create a Dedicated User for SonarQube

For security, create a sonarqube user:

useradd sonarqube

passwd sonarqube

* Chage onwership or directory.

chown -R sonar:sonar /opt/sonarqube

* Switch to sonarqube user and execute starting script

cd /opt/sonarqube

chown -R sonar:sonar sonarqube-<version

cd sonarqube-<version/bin/linux-x86-64

./sonar.sh start

Now you can access the SonarQube Server on http://<ip-address>:9000

4. Reset the pwd  for sonarqube. default user & password is "admin"

5. Installed sonarqube plugin in jenkins to integrate with sonarqube






