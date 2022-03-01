<p align="left">
  <a href="https://github.com/vdarkobar/home-cloud">Home</a>
  <br><br>
</p> 
  
# WordPress
  
Login to <a href="https://dash.cloudflare.com/">CloudFlare</a> and set Domain name, or Domain name and Subdomain for your WordPress.
```
    A | example.com | YOUR WAN IP
```
or:
```
    A | example.com | YOUR WAN IP
```
```
    CNAME | subdomain | @ (or example.com)
```

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
  
