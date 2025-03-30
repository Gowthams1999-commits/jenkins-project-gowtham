## Jenkins Installation

### Follow these steps to install and configure Jenkins on your server:

1. **Install Java**  
   Jenkins is a Java-based application, so you need to install Java first. You can install the OpenJDK or Oracle JDK.

2. **Install Jenkins**  
   After Java installation, you can install Jenkins by adding the Jenkins repository and then installing it via your package manager (e.g., `apt`, `yum`).

3. **Verify Jenkins Service**  
   Verify the Jenkins service is running using the following command:
   ```bash
   systemctl status jenkins


If needed, restart the Jenkins service:



systemctl restart jenkins

Expose Jenkins to the Outside World
To make Jenkins accessible externally, configure your firewall, and allow traffic on port 8080 (default Jenkins port). You can do this using tools like ufw or firewalld, depending on your system.

Access Initial Admin Password
After installation, get the Jenkins initial admin password by reading the file:


cat /var/lib/jenkins/secrets/initialAdminPassword
Use this password to log in to the Jenkins UI.

## Reset the Jenkins Password

Once you're logged in to Jenkins, reset the admin password for security purposes. You can do this by navigating to the Manage Jenkins > Manage Users section, and changing the password for the admin user.
