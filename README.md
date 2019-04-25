# Nginx Reverse Proxy instructions

```sh
yum install epel-release
```
#### Insert the repo creating a file called nginx.repo and add the lines bellow

vim /etc/yum.repos.d/nginx.repo <br>
[nginx] 
name=nginx repo
baseurl=http://nginx.org/packages/mainline/rhel/7/$basearch/ 
gpgcheck=0 
enabled=1 
    
#### Execute the commands and install Nginx

yum repolist all 
yum install nginx.x86_64 
systemctl enable nginx 

#### Create a file called in the /etc/nginx/conf.d/ wuth the name vhosts.conf 

firewall-cmd --add-service=http --permanent 
firewall-cmd --reload 
systemctl start nginx 
```

