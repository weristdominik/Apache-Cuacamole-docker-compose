# Apache-Cuacamole-docker-compose
Run Apache Cuacamole (MYSQL Backend) in docker-compose


Installing Guacamole with Docker
https://guacamole.apache.org/doc/gug/guacamole-docker.html


1. Download .ZIP and extract
2. run docker-compose
3. copy File initdb.sql to Your mysql docker container

     3.1 docker exec -it mysql bin/bash/
   
     3.2 mysql -u root
   
     3.3 GRANT ALL PRIVILEGES ON guacamole.* TO 'guacamole_user'@'%';
   
     3.4 FLUSH PRIVILEGES;
   
     3.5 exit

     3.6 mysql -u guacamole_user -p < initdb.sql
   
     (initdb.sql ist in / directory of docker mysql)


Once the containers are running, you can access the Guacamole web interface at http://localhost:8080/guacamole/. Log in using the default credentials (username: guacadmin, password: guacadmin), and you can change the password after logging in.
