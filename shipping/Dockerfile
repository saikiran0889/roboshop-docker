from maven:3.9.11
expose 8080
workdir /opt/server
copy pom.xml .
copy src ./src
run mvn clean package 
run mv target/shipping-1.0.jar shipping.jar
env CART_ENDPOINT="cart:8080" \
    DB_HOST="mysql"
cmd ["java","-jar","shipping.jar"]