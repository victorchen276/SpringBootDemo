# SpringBootDemo
docker run --name postgres-spring -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres:alpine
docker exec -it 342765dfc82d bin/bash
CREATE DATABASE demodb;
\c demodb
\dt
\d
CREATE EXTENSION "uuid-ossp()";
select uuid_generate_v4();
insert into person (id, name) values (uuid_generate_v4(), 'Maria Jones');