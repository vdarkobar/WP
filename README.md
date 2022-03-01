<p align="left">
  <a href="https://github.com/vdarkobar/home-cloud">Home</a>
  <br><br>
</p> 
  
# WordPress
  
Login to <a href="https://dash.cloudflare.com/">CloudFlare</a>, add *Subdomain* for your *WordPress*. 
```
    CNAME | subdomain | @ (or example.com)
```
#### *No need to add A record to put WordPress on your Root Domain (already set by Argo Tunnel), just skip it, including CNAME creation.*
  
---
  
#### *Decide what you will use for*:
```
Time Zone and WordPress Port Number.
```
    
### *Run this command*:
```
RED='\033[0;31m'; echo -ne "${RED}Enter directory name: "; read DIR; \
mkdir -p "$DIR"; cd "$DIR" && git clone https://github.com/vdarkobar/WP.git . && \
chmod +x setup.sh && \
./setup.sh
```
  
### Log:
```
sudo docker logs -tf --tail="50" wordpress
sudo docker logs -tf --tail="50" wp-db
```
  
### Follow <i><a href="https://github.com/vdarkobar/NPM/blob/main/shared/WP%20Additional%20Settings.md">this link</a></i> for important WordPress settings.  
  
