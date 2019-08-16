# Docker Mysql

Run docker : docker run --name mysqldb -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -d mysql

Access MySQL command : 
docker exec -it mysqldb bash
mysql --user=root -p
