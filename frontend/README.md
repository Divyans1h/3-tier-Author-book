
This project is full-stack web application implementation using fronted ->backend->MySQL
this is a 3-tier application which contain 3 layers . where presentation layer (React js ), application logic layer (express js) and data layer (MYSQL) these are separated into tiers

* we are using the aws CLI



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
curl frontend ip
curl backend ip


Now you can access the fronted with public_ip
hit ip in your browser you get response
