Copy & paste the Shell Script below onto the EC2 User Data, when you launch an EC2 instance. EC2 will automatically run commands and deploy the Super Kitty Piano website during launch:

    #!/bin/bash
    yum update -y
    yum install git -y
    yum install httpd -y
    systemctl start httpd
    systemctl enable httpd
    git clone https://github.com/CloudemyTV/super-kitty-piano.git /var/www/html/
    
