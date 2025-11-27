from python:3.9
expose 8080
workdir /opt/server
copy payment.ini .
copy *.py .
copy requirements.txt .
run pip3 install -r requirements.txt
env CART_HOST="cart" \
    CART_PORT="8080" \
    USER_HOST="user" \
    USER_PORT="8080" \
    AMQP_HOST="rabbitmq" \
    AMQP_USER="roboshop" \
    AMQP_PASS="roboshop123"
cmd ["uwsgi","--ini","payment.ini"]
