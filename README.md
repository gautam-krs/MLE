
# Install GIT and Download Course Repo on the Amazon EC2 Instance

#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd
cd /var/www/
yum install git -y
git clone https://github.com/gautam-krs/MLE-POC.git
cp -rf MLE-POC/* /var/www/html/
