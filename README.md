# Employee API - 3 Tier DevOps Project

Architecture:

Route 53
   |
CloudFront
   |
Application Load Balancer
   |
Nginx EC2
   |
Tomcat EC2
   |
Amazon RDS MySQL

Application context path:
  /employee-api

Health:
  GET /employee-api/health

CRUD:
  GET    /employee-api/api/employees
  GET    /employee-api/api/employees/{id}
  POST   /employee-api/api/employees
  PUT    /employee-api/api/employees/{id}
  DELETE /employee-api/api/employees/{id}

Build:
  mvn clean package

WAR:
  target/employee-api.war

Environment variables:
  DB_HOST
  DB_PORT
  DB_NAME
  DB_USERNAME
  DB_PASSWORD

Example:
  export DB_HOST=mydb.xxxxxx.ap-south-1.rds.amazonaws.com
  export DB_PORT=3306
  export DB_NAME=employee_db
  export DB_USERNAME=employee_app
  export DB_PASSWORD='your-password'
