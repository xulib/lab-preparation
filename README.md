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

## Start jenkins with docker 

```
docker run --name jenkins -d --publish 127.0.0.1:8080:8080 --publish 127.0.0.1:50001:50001 --volume jenkins_home:/var/jenkins_home \
        --env JENKINS_SLAVE_AGENT_PORT=50001 \
        --env JENKINS_OPTS="--prefix=/jenkins" \
        jenkins/jenkins:lts
```
