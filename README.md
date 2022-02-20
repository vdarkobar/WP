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
  
### Clone WordPress Git Repository:
```
RED='\033[0;31m'; echo -ne "${RED}Enter directory name: "; read NAME; mkdir -p "$NAME"; \
cd "$NAME" && git clone https://github.com/vdarkobar/WordPress.git .
```
  
#### *Decide what you will use for*:
```
Time Zone,
Domain name,
Subdomain (if planned),
WordPress Port Number.
```
  
### Select and run all at once. Enter required data:
*Only works once, on wrong data input delete folder and clone again*.
```
clear
RED='\033[0;31m'
echo -ne "${RED}Enter Time Zone: "; read TZONE; \
echo -ne "${RED}Enter Domain name: "; read DNAME; \
echo -ne "${RED}Enter Subdomain with . (dot) at the end, or just press Enter to default to Domain name: "; read SDNAME; \
echo -ne "${RED}Enter WordPress Port Number (WPPORTN:80): "; read WPPORTN; \
sed -i "s|01|${TZONE}|" .env && \
sed -i "s|02|${DNAME}|" .env && \
sed -i "s|03|${WPPORTN}|" .env && \
sed -i "s|04|${SDNAME}|" .env && \
echo | openssl rand -base64 48 > secrets/mysql_root_password.secret && \
echo | openssl rand -base64 20 > secrets/wp_mysql_password.secret && \
sudo chown -R root:root secrets/ && \
sudo chmod -R 600 secrets/ && \
rm README.md
```
    
### Start:  
*Change Container names/Port numbers, if multiple instances are planed.*
```
sudo docker-compose up -d
```
### Log:
```
sudo docker logs -tf --tail="50" wordpress
sudo docker logs -tf --tail="50" wp-db
```
