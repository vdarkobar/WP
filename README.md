# WP
WordPress

  
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
    
### Clone WordPress Git Repository:
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
