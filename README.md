# docker-mysql-spring-boot
How to run

Build docker-mysql-spring-boot image
$docker build . -t users-mysql

Start mysql ( pull and start in the one command )
$docker run --name mysql-standalone -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test -e MYSQL_USER=sa -e MYSQL_PASSWORD=password -d mysql:5.6

Run docker-mysql-spring-boot and link to running mysql in the one command
$docker run -p 8086:8086 --name users-mysql --link mysql-standalone:mysql -d users-mysql

Test on web browser
http://<host-ip>:8086/all/
http://<host-ip>:8086/all/create

