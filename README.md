# Nginx Reverse Proxy instructions

#### Install the repository epel executing the command bellow:

```sh
yum install epel-release
```

#### Insert the repo creating a file called nginx.repo and add the lines bellow:
```sh
vim /etc/yum.repos.d/nginx.repo
[nginx] 
name=nginx repo 
baseurl=http://nginx.org/packages/mainline/rhel/7/$basearch/ 
gpgcheck=0 
enabled=1 
```

#### Execute the commands and install Nginx

```sh
yum repolist all 
yum install nginx.x86_64
systemctl enable nginx
```

#### Create a file called in the /etc/nginx/conf.d/ with the name vhosts.conf and insert the code present in this project 

```sh
firewall-cmd --add-service=http --permanent 
firewall-cmd --reload 
systemctl start nginx 
```

