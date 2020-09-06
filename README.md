# toastmc.dev website
https://toastmc.dev

# Docker Remake Commands:

docker container rm web    
        
docker run -d --name web -p 80:80 -p 443:443    
\ --mount type=bind,source=/srv/web/pages,target=/usr/share/nginx/html,readonly     
\ --mount type=bind,source=/srv/web/config,target=/etc/nginx nginx  
          
docker container exec web apt-get update                
                           
docker container exec web apt-get install certbot python3-certbot-nginx -y     
        
docker container exec -it web certbot --nginx         
