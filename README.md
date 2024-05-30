# boot-security

[![License](http://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

Simple backend app [Spring Boot](http://projects.spring.io/spring-boot/) for applying security features.

## Requirements

For building and running the application you need:

- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3](https://maven.apache.org)

## Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `dev.exampl.security.bootsecurity.Application` class from your IDE.

Alternatively you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn spring-boot:run
or
./mvnw spring-boot:run
```

## Credits
This application is based on an idea developed at https://spring.academy/courses/spring-academy-secure-rest-api-oauth2/lessons/introduction
in order to learn/improve skills related with securing a REST API.

## Features
The idea is to ask first for a valid JWT then submit in the request in order to return information related with
a user that has been authenticated and has authorization for submitting that request, otherwise no information is returned.

## Additional Information
In order to get a valid JWT you must run a Docker container that is the app responsible for minting the JWT.
Use the following command


```shell
docker run --rm --name sso -p 9000:9000 ghcr.io/vmware-tanzu-learning/course-secure-rest-api-oauth2-code/sso:latest
```
I tried to develop an app that also could mint JWT, is under development



## Copyright

Released under the Apache License 2.0. See the [LICENSE](https://github.com/codecentric/springboot-sample-app/blob/master/LICENSE) file.