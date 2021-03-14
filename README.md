# lab-preparation
jenkins gitea preparation with docker

## Install nginx on ubuntu 
``` apt-get update && apt-get upgrade -y && apt-get install nginx -y```

https://ubuntu.com/tutorials/install-and-configure-nginx#5-activating-virtual-host-and-testing-results

```
/etc/init.d/nginx start
```
https://www.techrepublic.com/article/how-to-enable-ssl-on-nginx/
```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt
```

