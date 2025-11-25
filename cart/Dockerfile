from node:20
workdir /opt/server
expose 8080
copy package.json .
copy *.js .
run npm install
env redis_host="redis" \
    catalogue_host="catalogue" \
    catalogue_port="8080"
cmd ["node","server.js"]


