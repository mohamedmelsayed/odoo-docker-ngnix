Steps to configure ngnix domain to map  odoo v 15.0 
++ SSL certificate activation 

1. edit dns zone (add record)
2. install odoo in your ubuntu server
3. install ngnix </br>
<b>sudo apt install nginx -y</b>
5. create your site config file in <b>/etc/ngnix/site-available && copy it to site-available </b>
6. install cerbot </br>
<b>sudo add-apt-repository ppa:certbot/certbot -y && sudo apt-get update -y</br>
  sudo apt-get install python3-certbot-nginx -y</b>
7. run certbot to install letsencrypt ssl certificate </br>
<b>sudo certbot --nginx -d "yourdomain" --noninteractive --agree-tos --email "youremail"  --redirect</b>
8. reload ngnix </br>
<b>sudo service ngnix reload</b>
9. your odoo now linked to your domain


Authored by Mohamed Osman 
for help contact me https://twitter.com/MohamedOsmanIT
