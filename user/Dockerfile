from node:20
workdir /opt/server
expose 8080
copy package.json .
copy *.js .
run npm install
env MONGO="true" \
    REDIS_URL="redis://redis:6379" \
    MONGO_URL="mongodb://mongodb:27017/users"
cmd ["node","server.js"]


