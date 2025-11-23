from node:20
workdir /opt/server
copy package.json .
copy *.js .
run npm install
env mongo="true" \
    mongo_url="mongodb://mongodb:27017/catalogue"
cmd ["node","server.js"]


