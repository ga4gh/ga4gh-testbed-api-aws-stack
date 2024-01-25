# ga4gh-testbed-api-aws-stack
This repository contains the infrastructure set up for the GA4GH Testbed API

Please follow the steps to test successful deployment of backend on AWS Infrastructure:
1. Verify database is created.
    1. Navigate to the AWS RDS Management Console and verify, or Navigate to resources tab in CloudFormation template stack for database, there will be a list of resources created as part of this CFT execution.
    2. Use any database management that support Postgres database(e.g. pgAdmin), and use the properties from RDS management console to connect to the database.
2. Insert data into database, execute DDL and DML script from https://github.com/ga4gh/ga4gh-testbed-api/tree/main/database/postgresql
    1. Execute create-tables.sql
    2. Execute add-dev-dataset.sql
3. Verify deployment of backend application.
    1. Navigate to resources tab in CloudFormation templte stack for backend and look for ALBBalancer and open it.
    2. To make an api call to backend use: **ALBBalancer_DNS_URL:4500/testbeds**
    3. Similarly other APIs could also be tested replacing testbeds in point 2.
       
