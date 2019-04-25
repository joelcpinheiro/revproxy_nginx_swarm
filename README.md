# revproxy-nginx

  `yum install epel-release`
  vim /etc/yum.repos.d/nginx.repo
  [nginx]
  name=nginx repo
  baseurl=http://nginx.org/packages/mainline/rhel/7/$basearch/
  gpgcheck=0
  enabled=1
    
  yum repolist all
  yum install nginx.x86_64
  systemctl enable nginx

Create a file vhosts.conf

  firewall-cmd --add-service=http --permanent
  firewall-cmd --reload
  systemctl start nginx
  
