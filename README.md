# docker-Onlyoffice
Docker-Compose Script for setup Onlyoffice for Nextcloud

With this Setup you have an onlyoffice Container für your Nextcloud installation with an Nginx Reverse Proxy

Copy the docker-compose.yml to your favorite Folder and start the Container with 

Docker-compose up -d

after that create an Nginx Config. 

cp docker-Onlyoffice/etc/nignx/sites-available/onlyoffice.conf /etc/nginx/sites-available && sudo ln -s /etc/nginx/sites-available/onlyoffice.conf /etc/nginx/sites-enabled/onlyoffice.conf && sudo service nginx restart

Now you must create an Certificate (Letsencrypt maybe)

sudo apt install certbot && sudo certbot certonly 

now you can restart Nginx again and add the settings to your Nextcloud

Complete Articel: https://dasnetzundich.de/setup-onlyoffice-mit-docker-compose/
