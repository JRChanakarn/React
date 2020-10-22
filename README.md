# React
React NGINX


# Code command
    - sudo apt-get update.
    - sudo apt-get install nginx 
    - curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
    - sudo apt install nodejs
    - sudo apt install git-all
    - git clone https://github.com/JRChanakarn/React.git
    - ls
    - cd REACT_FB/  
    - npm i
    - npm run build
    - sudo npm i node-modules
    - sudo npm i pm2 -g
    - pm2 start server/index.js 
    - pm2 stop 0
    - sudo apt-get install ufw
    - sudo ufw enable
    - sudo ufw status
    - sudo ufw allow ssh
    - sudo ufw allow http
    - sudo ufw allow https
    - sudo ufw stats
    - sudo ufw status
    - sudo nano /etc/nginx/sites-available/default
                                                 #delete line try_files $uri $uri/ =404; and paste
                                                    proxy_passhttp://localhost:3000; #whatever port your app runs on
                                                    proxy_http_version 1.1;
                                                    proxy_set_header Upgrade $http_upgrade;
                                                    proxy_set_header Connection 'upgrade';
                                                    proxy_set_header Host $host;
                                                    proxy_cache_bypass $http_upgrade;
    - sudo service nginx restart
    - nano src/register/Register.js                  #Edit ur
    - nano src/showdata/Showdata.js                  #Edit url
    - nano src/App/Facebook.js                       #Edit Facebook AppId
    - nano server/app.js                             #Edit database
    - npm run build
    - pm2 restart 0
    - pm2 stop 0
