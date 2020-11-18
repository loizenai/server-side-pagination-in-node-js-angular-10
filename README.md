# Server Side Pagination in Node.js Angular 10 + MySQL + Sequelize

[Server Side Pagination in Node.js Angular 10 + MySQL + Sequelize](https://loizenai.com/server-side-pagination-in-node-js-angular-10-mysql-sequelize/#sourcecode)

![Server Side Pagination in Node.js Angular 10 MySQL database + Express + Sequelize CRUD](https://loizenai.com/wp-content/uploads/2020/07/Angular-Nodejs-Pagination-RestAPIs-Tutorials-Sequelize-Pagination-Filtering-Sorting-APIs.png)

In the tutorial, I introduce how to build an “Angular 10 Nodejs Pagination RestAPIs Example with MySQL database (Server Side Pagination with filtering and sorting)” project using Express framework and Sequelize crud queries to interact with database’s records.

– Nodejs Express project (server side pagination) produces pagination RestAPIs with MySQL database records using Sequelize CRUD queries.
– Angular 10 project (client side pagination) will consume the Node.js pagination RestAPIs then show up on component’s views.

## Architecture Design Angular Node.js Application

![Angular Nodejs MySQL RestAPIs Overview](https://loizenai.com/wp-content/uploads/2020/08/Angular-Nodejs-MySQL-RestAPIs-Overview.png)

In the tutorial “Server Side Pagination in Node.js Angular 10”, We develop 2 projects:

Backend Project – Nodejs MySQL Pagination Application gets data from MySQL database then provides RestAPIs with pagination, filtering and sorting function for frontend
Frontend Project – Angular Application use HttpClient to fetch data from Backend Application then shows them in Bootstrap table with pagination, filtering and sorting functions

## Goal

– Make a request at API: /api/customers/pagefiltersort with pagination, filtering and sorting params as below:

- page: 0 – first page
- size: 5 – size of a page
- salary: 4000 – filtering by salary field
- agesorting: true – sorting by age
- desc: true – descending or ascending sorting

Result:

![Nodejs MySQL Pagination RestAPIs Examples](https://loizenai.com/wp-content/uploads/2020/08/Nodejs-MySQL-Pagination-RestAPIs-Examples.png)

– Angular Frontend Pagination with Filtering and Sorting table:


![Angular Pagination Frontend](https://loizenai.com/wp-content/uploads/2020/08/Angular-Pagination-Frontend.png)

## Video Guide – Server Side Pagination in Node.js Angular 10

For the tutorial “Angular 10 Nodejs Pagination RestAPIs Example (Server Side Pagination)”, I create a Youtube video guide with clearly steps to debug full-stack for all running flows of living code from Angular client to Nodejs backend pagination:

https://youtu.be/pkQY56B5Ut0

## Overall Node.js Sequelize MySQL Pagination

To handling Pagination RestAPI requests and do Paging Filtering and Sorting queries with MySQL database, we create a backend web Node.js application with 4 main points:

![Overall Node.js Sequelize MySQL Pagination](https://loizenai.com/wp-content/uploads/2020/08/Nodejs-Pagination-Overall-Architecture.png)

- To handle pagination RestAPI requests with Node.js, We use Express framework.
- To do pagination filtering and sorting queries with MySQL database, We use Sequelize ORM.
- We define all RestAPI URLs in router.js.
- We implement code how to process each paging filtering and sorting RestAPI request in controller.js file.

## Nodejs Sequelize Pagination Queries

To do the pagination with database, Sequelize ORM provides 2 model methods for supporting the purpose with limit and offset parameters:

- .findAll() – Search for multiple elements in the database
- .findAndCountAll() - Search for multiple elements in the database, returns both data and total count

How about limit & offset for nodejs pagination?

- limit is the maximum number of records to fetch
- offset is the quantity of records to skip

For example, if we have total 12 items:

- { offset: 5 }: skip first 5 items, fetch 7 remaining items.
- { limit: 5 }: fetch first 5 items.
- { offset: 5, limit: 5 }: skip first 5 items, fetch 6th and 10th items.

## Related post

- [Nodejs JWT Authentication Example – Express RestAPIs + JSON Web Token + BCryptjs + Sequelize + MySQL/PostgreSQL](https://loizenai.com/nodejs-jwt-authentication-example-with-mysql-postgresql-database/)
- [Angular & Nodejs JWT Authentication fullstack Example | Angular 6, 7, 8, 9 – Express RestAPIs + JWT + BCryptjs + Sequelize + MySQL/PostgreSQL](https://loizenai.com/angular-nodejs-jwt-authentication-examples-tutorials/)
- [Nodejs MySQL Pagination Filtering Sorting Tutorial – Stack: Express RestAPIs + Sequelize ORM + MySQL database Examples](https://loizenai.com/tutorial-nodejs-mysql-pagination-filtering-sorting-express-restapis-sequelize-orm-example/)
