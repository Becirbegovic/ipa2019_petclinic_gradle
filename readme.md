# Spring PetClinic Sample Application with Java 11 and Gradle


## Running petclinic locally
Petclinic is a [Spring Boot](https://spring.io/guides/gs/spring-boot) application built using [Gradle](https://spring.io/guides/gs/gradle/). 
You can build a jar file and run it from the command line:

<br>

```
git clone https://github.engineering.zhaw.ch/bacn/spring-petclinic-gradle
cd spring-petclinic-gradle
./gradlew build
java -jar build/libs/*.jar
```
<br>

You can then access petclinic here: http://localhost:8080/

<br>

<img width="1042" alt="petclinic-screenshot" src="https://cloud.githubusercontent.com/assets/838318/19727082/2aee6d6c-9b8e-11e6-81fe-e889a5ddfded.png">

<br>

Or you can run it from Gradle directly using the Spring Boot Gradle plugin. 
If you do this it will pick up changes that you make in the project immediately 
(changes to Java source files require a compile as well - most people use an IDE for this):

```
./gradlew bootRun
```

## Database configuration

In its default configuration, Petclinic uses an in-memory database (HSQLDB) which
gets populated at startup with data. A similar setup is provided for MySql in case a persistent database configuration is needed.
Note that whenever the database type is changed, the app needs to be run with a different profile: `spring.profiles.active=mysql` for MySql.

You could start MySql locally with whatever installer works for your OS, or with docker:

```
docker run -e MYSQL_ROOT_PASSWORD=petclinic -e MYSQL_DATABASE=petclinic -p 3306:3306 mysql:5.7.8
```


### Guides
The following guides illustrates how to use certain features concretely:

* [Caching Data with Spring](https://spring.io/guides/gs/caching/)
* [Building a RESTful Web Service with Spring Boot Actuator](https://spring.io/guides/gs/actuator-service/)
* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Accessing data with MySQL](https://spring.io/guides/gs/accessing-data-mysql/)
* [Handling Form Submission](https://spring.io/guides/gs/handling-form-submission/)
* [Validating Form Input](https://spring.io/guides/gs/validating-form-input/)

