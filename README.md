# React
React NGINX


**Code command** 
    1  sudo apt-get update 
    2  sudo apt-get install nginx 
    3  curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
    4  sudo apt install nodejs
    5  sudo apt install git-all
    6  git clone https://github.com/JRChanakarn/React.git
    7  ls
    8  cd REACT_FB/  
    9  npm i
   10  npm run build
   11  sudo npm i node-modules
   12  sudo npm i pm2 -g
   13  pm2 start server/index.js 
   14  pm2 stop 0
   15  sudo apt-get install ufw
   16  sudo ufw enable
   17  sudo ufw status
   18  sudo ufw allow ssh
   19  sudo ufw allow http
   20  sudo ufw allow https
   21  sudo ufw stats
   22  sudo ufw status
   23  sudo nano /etc/nginx/sites-available/default #delete line try_files $uri $uri/ =404; and paste 
                                                     proxy_passhttp://localhost:3000; #whatever port your app runs on
                                                     proxy_http_version 1.1;
                                                     proxy_set_header Upgrade $http_upgrade;
                                                     proxy_set_header Connection 'upgrade';
                                                     proxy_set_header Host $host;
                                                     proxy_cache_bypass $http_upgrade;
   24  sudo service nginx restart
   25  nano src/register/Register.js #Edit url
   26  nano src/showdata/Showdata.js #Edit url
   27  nano src/App/Facebook.js      #Edit Facebook AppId 
   28  nano server/app.js            #Edit database
   29  npm run build
   30  pm2 restart 0
   31  pm2 stop 0
