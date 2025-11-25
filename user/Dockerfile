from node:20
workdir /opt/server
expose 8080
copy package.json .
copy *.js .
run npm install
env mongo="true" \
    redis_url="redis://redis:6379" \
    mongo_url="mongodb://mongodb:27017/user"
cmd ["node","server.js"]


