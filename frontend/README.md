
This project is full-stack web application implementation using fronted ->backend->MySQL
this is a 3-tier application which contain 3 layers . where presentation layer (React js ), application logic layer (express js) and data layer (MYSQL) these are separated into tiers

* we are using the aws CLI


#Data layer
 
create the rds in the same vpc



# Application layer

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



