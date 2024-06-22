## Overview

- Project created using: start.spring.io
- To replicate how this project was created with start.spring.io, use this [custom link](https://start.spring.io/#!type=maven-project&language=java&platformVersion=3.3.1&packaging=war&jvmVersion=22&groupId=com.example&artifactId=demo&name=demo&description=Demo%20project%20for%20Spring%20Boot&packageName=com.example.demo&dependencies=data-jpa,web,h2)
- default implementation under JPA interface is Hibernate imported via jakarta.persistence package from spring-boot-starter-data-jpa dependency
- apachet tomcat is used as a web container (from spring-boot-starter-web)
- in-memory database is provided by com.h2database (Note: database will be erased after process is stopped).
- maven binaries are present in the root, no need for local maven install

# How to run

- after cloning this repo, run: `./mvnw spring-boot:run`

# How to test

- see all employees: visit [localhost:8080/](http://localhost:8080/api/employees)
- add employee 1

```bash
curl -X POST http://localhost:8080/api/employees \
-H "Content-Type: application/json" \
-d '{
  "name": "John Doe",
  "position": "Software Engineer",
  "salary": 60000
}'

```

- add employee 2

```bash
curl -X POST http://localhost:8080/api/employees \
-H "Content-Type: application/json" \
-d '{
  "name": "Janet Smith",
  "position": "Software Engineer",
  "salary": 60000
}'

```

- add employee 3

```bash
curl -X POST http://localhost:8080/api/employees \
-H "Content-Type: application/json" \
-d '{
  "name": "John Doe",
  "position": "Software Engineer",
  "salary": 60000
}'
```

- delete employee 3

```bash
curl -X DELETE http://localhost:8080/api/employees/3
```

- change name of employee 2

```bash
curl -X PUT http://localhost:8080/api/employees/2 \
-H "Content-Type: application/json" \
-d '{
  "name": "Lisa Smith",
  "position": "Project Manager",
  "salary": 85000
}'
```
