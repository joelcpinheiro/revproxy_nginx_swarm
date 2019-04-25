# revproxy-nginx

  `yum install epel-release` <br />
  vim /etc/yum.repos.d/nginx.repo <br />
  [nginx] <br />
  name=nginx repo <br />
  baseurl=http://nginx.org/packages/mainline/rhel/7/$basearch/ <br />
  gpgcheck=0 <br />
  enabled=1 <br />
    
  yum repolist all <br />
  yum install nginx.x86_64 <br />
  systemctl enable nginx <br />

Create a file vhosts.conf <br />

  firewall-cmd --add-service=http --permanent <br />
  firewall-cmd --reload <br />
  systemctl start nginx <br />
  
