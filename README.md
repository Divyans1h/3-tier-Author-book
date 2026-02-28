
This project is full-stack web application implementation using fronted ->backend->MySQL
this is a 3-tier application which contain 3 layers . where presentation layer (React js ), application logic layer (express js) and data layer (MYSQL) these are separated into tiers

* we are using the aws CLI

# Data layer
 
create the rds in the same vpc


# applicaion layer

connect to the backend server or instance


install git
command : " yum install git "

clone repository
command : "git clone


install the mariadb or mysql for intalized the database
command : "sudo yum install mariadb105-server -y"

install node js
command : "sudo dnf install -y nodejs"

install npm
command "npm install"

install pm2 (process manager of node js)
command : " npm install -g pm2"


go to backend directory
cd 3-tier-Author-book\
cd backen

change the database details in db.js
*** vi configs/db.js***
const mysql = require('mysql2');

const db = mysql.createConnection({
   host: 'rds endpoint',
   port: '3306',
   user: 'admin',
   password: 'cloud123',
   database: 'react_node_app'
});

module.exports = db;


Initilize the database
command "mysql -h <rdsendpoint> -u admin -p<cloud123> < db.sql"


run the following command for backend execution

pm2 start server.js --name "Divyansh"
pm2 startup
sudo systemctl enable pm2-root
sudo pm2 save



# Presentation layer
 
connect to the frontend server or instance


install git
command : " yum install git "

clone repository
command : "git clone

install node js
command: "sudo dnf install -y nodejs"

install nginx
sudo yum install nginx -y

start and enable nginx
command : "sudo systemctl start nginx && sudo systemctl enable nginx"

go to frontend
cd 3-tier-Author-book\
cd frontend

In frontend path .env file is there if not existis please create .env file
VITE_API_URL=http://3.85.56.86/api   //  use backend ip
VITE_API_URL= "/api"



Run the following commnads in frontend
npm install
npm run build
sudo cp -r dist/* /usr/share/nginx/html





test backend
curl  backend_ip

test frontend
command : "curl frontend ip"
command : "curl backend ip "


Now you can access the fronted with public_ip
hit ip in your browser you get response
