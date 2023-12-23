# Install-word-Press-on-CentOS-7
WordPress is an online, open source website creation tool written in PHP.  But in non-geek speak, it’s probably the easiest and most powerful blogging and website  content management system (or CMS) in existence today. In this project, set up an  instance for WordPress with an Apache Web Server on Centos 7, which installs  WordPress on your Centos.
# WordPress Installation on CentOS 7
## Project Overview
This project guides you through the process of setting up WordPress on a CentOS 7 server with a LAMP stack. The instructions include creating a MySQL database, installing necessary PHP modules, and updating WordPress to the latest version.
## Prerequisites
1. CentOS 7 server installed and configured with a non-root user having sudo privileges.
2. LAMP stack installed on CentOS 7.
## MySQL Database Setup
- Create a MySQL database for WordPress.
## WordPress Installation and Configuration
1. **Flush Privileges and Install PHP Module:**
    ```bash
    sudo mysql -u root -p
    FLUSH PRIVILEGES;
    exit;
    
    sudo yum install php-gd
    sudo service httpd restart
    ```
2. **Download and Update WordPress:**
    ```bash
    cd ~
    wget http://wordpress.org/latest.tar.gz
    tar xzvf latest.tar.gz
    sudo rsync -avP ~/wordpress/ /var/www/html/
    mkdir /var/www/html/wp-content/uploads
    sudo chown -R apache:apache /var/www/html/*
    ```
## WordPress Configuration
1. **Configure WordPress:**
   Update the root directories and any other necessary configurations.
2. **Complete Installation:**
   Access the WordPress installation via your server's domain name or IP address. Follow the web interface for WordPress installation.
   Example: http://server_domain_name_or_IP
## Data Entry
- Now that your WordPress installation is complete, log in and start entering data using the WordPress dashboard.
## Contributors
- [Your Name](https://github.com/sathyasai-git/Install-word-Press-on-CentOS-7)

