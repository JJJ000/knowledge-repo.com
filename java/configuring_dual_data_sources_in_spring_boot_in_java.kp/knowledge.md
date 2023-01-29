---
title: Configure and utilize two data sources with spring boot
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Create two separate DataSource beans in the configuration class and use the @Primary annotation on one of them to set it as the default.
---

**Contents**

[TOC]

### Configuring Two Data Sources

1. Add the following dependencies to your `pom.xml` file: 
    ```xml
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-jdbc</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    ```
2. Create two separate `DataSource` beans in your `application.properties` file, one for each data source:
    ```properties
    spring.datasource.first.url=jdbc:mysql://localhost:3306/db1
    spring.datasource.first.username=username1
    spring.datasource.first.password=password1
    spring.datasource.first.driver-class-name=com.mysql.jdbc.Driver
    
    spring.datasource.second.url=jdbc:mysql://localhost:3306/db2
    spring.datasource.second.username=username2
    spring.datasource.second.password=password2
    spring.datasource.second.driver-class-name=com.mysql.jdbc.Driver
    ```

### Using Two Data Sources

1. Create two separate `@Configuration` classes to configure each data source:
    ```java
    @Configuration
    public class FirstDataSourceConfig {
    
        @Bean
        @ConfigurationProperties(prefix="spring.datasource.first")
        public DataSource firstDataSource() {
            return DataSourceBuilder.create().build();
        }
    }
    
    @Configuration
    public class SecondDataSourceConfig {
    
        @Bean
        @ConfigurationProperties(prefix="spring.datasource.second")
        public DataSource secondDataSource() {
            return DataSourceBuilder.create().build();
        }
    }
    ```
2. Autowire both data sources into your service class:
    ```java
    @Service
    public class MyService {
    
        @Autowired
        private DataSource firstDataSource;
    
        @Autowired
        private DataSource secondDataSource;
    
        // ...
    }
    ```
3. Use the data sources in your service methods:
    ```java
    public void doSomething() {
        // Use first data source
        JdbcTemplate jdbcTemplate = new JdbcTemplate(firstDataSource);
        // ...
    
        // Use second data source
        JdbcTemplate jdbcTemplate2 = new JdbcTemplate(secondDataSource);
        // ...
    }
    ```
