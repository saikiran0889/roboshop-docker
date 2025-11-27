from python:3.9
expose 8080
workdir /opt/server
copy payment.ini .
copy *.py .
copy requirements.txt .
run pip3 install -r requirements.txt
env cart_host="cart" \
    cart_port="8080" \
    user_host="user" \
    user_port="8080" \
    amqp_host="rabbitmq" \
    amqp_user="roboshop" \
    amqp_pass="roboshop123"
cmd ["uwsgi","--ini","payment.ini"]
