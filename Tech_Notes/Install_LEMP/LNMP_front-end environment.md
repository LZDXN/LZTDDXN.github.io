Install LEMP Stack
---
- **L** - Linux operating system
- **E** - Nginx, an HTTP and reverse proxy server
- **M** - MySQL or MariaDB relational database management system
- **P** - PHP programming language

**Table of contents**
- [[#Simple update]]
- [[#Installing Database]]
	- [[#Option1: MySQL]]
	- [[#Option2: MariaDB]]
	- [[#After choose option 1 or 2 (Optional)]]
- [[#Installing PHP]]
- [[#Configuring Nginx to Process PHP Pages]]


# Simple update
```shell
sudo apt update
```

# Installing Nginx
```shell
sudo apt install nginx
```

# Installing Database
## Option1: MySQL
```shell
sudo apt install mysql-server
```

## Option2: MariaDB
```shell
sudo apt install mariadb-server
```

## After choose option 1 or 2 (Optional)
To improve the security of those database
```shell
sudo mysql_secure_installation
```

# Installing PHP
```shell
sudo apt install php-fpm php-opcache php-cli php-gd php-curl php-mysql
```

# Configuring Nginx to Process PHP Pages
First go the Nginx config file:
```bash
nano /etc/nginx/sites-available/default
```
Then find the code (default is commented) copy those code and add int eh following lines
```nginx
server {
  # other code

  location ~ \.php$ {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/run/php/php3.0-fpm.sock;
  }
}
```
Save the file than restart the Nginx service:
```bash
sudo systemctl restart nginx
```

Done