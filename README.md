# Virtual_Machine
 Linux distribution on a virtual machine and web application
The IP address and SSH port of the VM is 52.27.83.26:2200
The web application can be reached at http://ec2-52-27-83-26.us-west-2.compute.amazonaws.com/

Summary of installed packages and configuration:  
Installed git, libapache2-mod-wsg, apache2, psql  
Created grader and catalog users with sudo permission  
Configured (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)  
disabled root ssh login  

Web application setup:  
cd /var/www  
git clone https://github.com/396xwz/catalog.git  
chgrp -R www-data /var/www/catalog  
chgrp -R www-data /var/www  
chmod -R 2770 /var/www   

