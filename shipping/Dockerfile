from maven:3.9.11
expose 8080
workdir /opt/server
copy pom.xml .
copy src .
run mvn clean package
run mv target/shipping-1.0.jar shipping.jar
env cart_endpoint="cart:8080" \
    db_host="mysql"
cmd ["java","-jar","shipping.jar"]