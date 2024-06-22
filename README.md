## Overview

- Project created using: start.spring.io
- TO replicate with start.spring.io, use this [custom link](https://start.spring.io/#!type=maven-project&language=java&platformVersion=3.3.1&packaging=war&jvmVersion=22&groupId=com.example&artifactId=demo&name=demo&description=Demo%20project%20for%20Spring%20Boot&packageName=com.example.demo&dependencies=data-jpa,web,h2)

# How to run

- `./mvnw spring-boot:run`

# How to test

- see all employees: visit [localhost:8080/](http://localhost:8080/api/employees)
- add employee 1 `curl -X POST http://localhost:8080/api/employees \\n-H "Content-Type: application/json" \\n-d '{\n  "name": "John Doe",\n  "position": "Software Engineer",\n  "salary": 60000\n}'`
- add employee 2 `curl -X POST http://localhost:8080/api/employees \\n-H "Content-Type: application/json" \\n-d '{\n  "name": "Jane Smith",\n  "position": "Project Manager",\n  "salary": 85000\n}'\`
- add employee 3 `curl -X POST http://localhost:8080/api/employees \\n-H "Content-Type: application/json" \\n-d '{\n  "name": "Jane Smith",\n  "position": "Project Manager",\n  "salary": 85000\n}'\`
- delete employee 3`curl -X DELETE http://localhost:8080/api/employees/3\n`
- change name of employee 2 `curl -X PUT http://localhost:8080/api/employees/2 \\n-H "Content-Type: application/json" \\n-d '{\n  "name": "Lisa Smith",\n  "position": "Project Manager",\n  "salary": 85000\n}'\n`

Note: database will be arased after process is stopped.
