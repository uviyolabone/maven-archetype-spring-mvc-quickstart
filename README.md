# maven-archetype-spring-mvc-quickstart
Spring MVC Quickstart Maven Archetype

A Maven archetype for a simple Spring MVC web application using the following components:

    Spring MVC - Web Framework
    Thymeleaf - Template Engine
    Spring Data JPA - Data Access Layer
    Hibernate - ORM
    SLF4J - Simple Logging Facade for Java
    HikariCP - High Performance JDBC connection pool
    Other helpful utilities (Validation, DI, JSON, etc)

Table of Contents

    Prerequisites
    Creating a project
    Testing a project

Prerequisites

    Java JDK 8
    Maven 3

Creating a Project

To start working on your new project, you will need to:

Install this archetype in your local maven repo:

git clone https://github.com/uviyolabone/maven-archetype-spring-mvc-quickstart.git

cd maven-archetype-spring-mvc-quickstart

mvn clean install

Generate your project based on the installed archetype:

mvn archetype:generate \
        -DarchetypeGroupId=com.uviyolabone \
        -DarchetypeArtifactId=maven-archetype-spring-mvc-quickstart \
        -DarchetypeVersion=5.1.9 \
        -DgroupId=uviyolab-one \
        -DartifactId=uvo-v2 \
        -Dversion="1.0-SNAPSHOT" \
        -DinteractiveMode=false \
        -DarchetypeRepository=https://github.com/uviyolabone/maven-archetype-spring-mvc-quickstart
        
Note: Replace GROUP_ID and ARTIFACT_ID with your own.

Testing a Project

If you don't want to be deploying your war file everytime you make a change, simply run the following command on the root of the project:

mvn test tomcat7:run
