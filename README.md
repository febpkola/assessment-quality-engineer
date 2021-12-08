# Quality Engineer Assessment project

This is a base project that contains a simple REST API, exposed using a swagger doc, as well as a simple login UI. The purpose of this project is to provide a foundation for you to build tests around the API and UI using whatever tools you prefer.

## Testing Requirements

### API Testing

Please download the [GitHub Spring Boot project](https://github.com/MomInv/assessment-quality-engineer) and follow the README.md instructions to run the application on your local machine.

If you need an IDE, you can use [IntelliJ](https://www.jetbrains.com/idea/download) (The free Community Edition, or make use of the 30-day trial Ultimate edition)

Write functional Test features to test against the REST API exposed by the application. The swagger doc can be found opening a browser to
http://localhost:8080/swagger-ui.html

There is a username-password to access it. These same credentials are required when making the REST request to the service.


Please write tests using whatever tool you would like to and showcase success and various failure scenarios for each.

1. ID Number must be a valid South African ID number (13 digits)
2. The client must be >/= 18years
3. Name and surname must not have any special characters and digits
4. A valid bank must be captured. Allowed banks are Scrum Bank, Iconic Bank, Minions Bank, and Molewa Bank
5. If Molewa bank is captured, then the following warning must be returned: “refer to compliance”
6. The bank account number must be 10 digits

###Minimum requirement:
1. Write a simple test spec or document detailing your "sign off" for the feature for **any _one_** of the tests above
2. Automated _**all**_ tests as part of a suite that can be run by simple command (CLI script, Postman collection, SoapUI test suite etc)


###Desirable requirement:
Demonstrate automation using a test framework like REST Assured, Karate or other framework, to showcase your understanding of using frameworks to test APIs

###Optional extra
1. Review the two frameworks ([REST Assured](https://www.pluralsight.com/courses/rest-assured-fundamentals) and [Karate](https://www.softwaretestinghelp.com/api-testing-with-karate-framework/)) and recommend which one you would prefer to use for testing a REST API and why.
2. Write a **_load test_** suite for the Loan REST API - options can include using either [JMeter](https://jmeter.apache.org/) or [Gatling](https://gatling.io/), or one of your own choice Load Test frameworks/Tools

##Assessment deliverables

###Time duration 
5 days

###Submission
Please provide the link to your github or bitbucket project with clear details of how you built your test project.
You may be required to attend a subsequent technical review regarding your solution, so please be prepared to discuss any design decisions you may have taken or assumed.

**Note**: Comments in code help a lot!

#Getting up and running

## Installations
* 	[Spring Boot](https://spring.io/projects/spring-boot) - Framework to ease the bootstrapping and development of new Spring Applications
* 	[JDK](https://www.oracle.com/za/java/technologies/javase/jdk11-archive-downloads.html) - Java™ Platform
* 	[Gradle](https://gradle.org/) - An open-source build automation tool

## Getting started

* Make sure Java Development Kit (JDK) 8 or higher is installed on your local machine.
```bash
java -version
```

## Testing

* [JUnit](https://junit.org/) - For Developer-side (unit) Testing, non-mandatory

* An example of the rest request is given in the **postman collection** found in the ```docs``` folder

## Running the application locally

*   Start application: There are several ways to run a Spring Boot application on your local machine. 
    1. Execute the `main` method in the `za.co.loans.Application` class from your IDE. 
    2. Alternatively you can use the [Spring Boot Gradle plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-gradle-plugin) as follows:
  
from the terminal, navigate to the root of the project 
```
assessment-quality-engineer$
```

build the project first using
```
./gradlew clean build
```

Command and output should lik as follows
```
assessment-quality-engineer$ ./gradlew clean build

> Task :test

za.co.loans.IdNumberTest > getAgeShouldReturnZero PASSED

za.co.loans.IdNumberTest > getAgeShouldReturnValidAge PASSED

BUILD SUCCESSFUL in 6s
7 actionable tasks: 7 executed
```

Start up the app with the command
```
./gradlew bootRun
```
Successful start up should display the last few logs as follows
```
- Scanning for api listing references
- Tomcat started on port(s): 8080 (http) with context path ''
- Started Application in 5.074 seconds (JVM running for 5.668)
```

* Open [Swagger UI](http://localhost:8080/swagger-ui.html) on a browser: 
  http://localhost:8080/swagger-ui.html
  
  There is a username/password required to access the swagger doc
    ```admin : password```



