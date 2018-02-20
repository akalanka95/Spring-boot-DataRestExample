RESTful API Example with Spring Boot, Spring Data REST and H2
================================================================

This guide will help you expose RESTful API using a combination of Spring Boot, JPA/Hibernate, Spring Data and Spring Data REST. We will use H2 as the in memory database.Spring Data REST takes the features of Spring HATEOAS and Spring Data JPA and combines them together automatically.

Find all books 
==============

      http://localhost:8080/books 
    
Find book with id = 1
=====================
      
      http://localhost:8080/books/2 
      
Update book id = 1 
====================

      PATCH http://localhost:8080/books/1
      
Replace book id 2 
==================

      PUT http://localhost:8080/books/2
      
Search Book 
============

      http://localhost:8080/books/search
      
       {
    "_links": {
        "findByDescription": {
            "href": "http://localhost:8080/books/search/findByDescription{?description}",
            "templated": true
        },
        "findByTitle": {
            "href": "http://localhost:8080/books/search/findByTitle{?title}",
            "templated": true
        },
        "self": {
            "href": "http://localhost:8080/books/search"
        }
    }
 }
 
 Search Book By Title
 ======================
 
        http://localhost:8080/people/search/findByTitle?nTitle=Hong
