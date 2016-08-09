# product-demo
Sample project utilizing Spring Boot and Reac.js

This project is a sample demo example. It simulates standard CRUD operations for dealing with a Product.
A Product has the following attributes:
- ID
- Name
- Description
- Tags - reusable for all products
- Price - with setting currency option
- Price points - representing the price in a specific currency (USD/GBP only).

Prerequisites:
1. Java 1.8
2. Maven 3.x

How to run:
mvn package && java -jar target/product-demo-0.0.1-SNAPSHOT.jar
or
mvn spring-boot:run

React.js client functionality:
- Crate a new product
- Get a list of all products
- Get details about a product
- Update a product

A complete Asciidoc documentation of the REST API is [here!](src/docs/api-guide.html).

Integration Testing
There are several test cases, testing the main app use cases.

Considerations:
1. Security - There is no security functionality neither on client nor server side.
A direct approach might be Spring Security Oauth or Spring Security plus custom session token logic.

2. This app follows Domain Driven Design paradigms. Logic is decoupled in several layers:
- REST Facade - Deals with REST and DTOs.
- Domain - Core business logic.
-- Service - Business services.
-- Model - Entities.
-- Repository - Repositories for Entities.
