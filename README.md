# Cloudflared  
A Cloudflared docker's image made with Alpine, for DNS over HTTPS.  
Can be use with Pihole.  

## How to use  
- Update **.env** with your informations. Choose the right architectrue (amd64, 386 or arm) For a Raspberry py, choose **arm**.  
- Start the container with ```docker-compose up --build -d```.  
- Connect into the container with ```docker-compose exec cloudflared sh ```.  

## Relative links  
https://docs.pi-hole.net/guides/dns-over-https/