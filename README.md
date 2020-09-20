# Toastmc.dev Website
The website for the [toastmc](https://toastmc.dev) development group. Started and Maintained by RemainingToast  

## Docker Usage
How to use with [Docker](https://www.docker.com/)
```
   docker run -d --name web -p 80:80 -p 443:443 \  
   --mount type=bind,source=/srv/web/pages,target=/usr/share/nginx/html,readonly \   
   --mount type=bind,source=/srv/web/config,target=/etc/nginx nginx   
   
   docker container exec web apt-get update                                   
   
   docker container exec web apt-get install certbot python3-certbot-nginx -y 
   
   docker container exec -it web certbot --nginx    
```
        
