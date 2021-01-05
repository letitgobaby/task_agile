### mysql 실행
sudo docker pull mysql

sudo docker run -d --name mysql -p 3306:3306  \
-e MYSQL_ROOT_PASSWORD=password \
mysql:5.7

sudo docker exec -it XXXX /bin/bash

mysql -u root -p
password

myql>
CREATE DATABASE task_agile CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

CREATE USER 'app_user'@'%' IDENTIFIED BY'aabb1122!!';
GRANT ALL PRIVILEGES ON task_agile.* TO 'app_user'@'%';


---
### rabbitmq 실행

sudo docker pull rabbitmq

sudo docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 \
--restart=unless-stopped \
-e RABBITMQ_DEFAULT_USER=username \
-e RABBITMQ_DEFAULT_PASS=password \
rabbitmq:management

