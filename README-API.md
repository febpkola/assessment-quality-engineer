# API Testing

A simple REST API, exposed using a swagger doc.

https://assessment-api-loan.herokuapp.com/swagger-ui.html

## Testing Requirements

Write functional Test features to test against the REST API exposed by the application. The swagger doc can be found opening a browser to
http://localhost:8080/swagger-ui.html

There is a username-password to access it. These same credentials are required when making the REST request to the service.

Please write tests using whatever tool you would like to and showcase success and various failure scenarios for each.

1. ID Number must be a valid South African ID number (13 digits)
2. The client must be >= 18years
3. Name and surname must not have any special characters and digits
4. A valid bank must be captured. Allowed banks are Scrum Bank, Iconic Bank, Minions Bank, and Molewa Bank
5. If Molewa bank is captured, then the following warning must be returned: “refer to compliance”
6. The bank account number must be 10 digits

### Minimum requirement:
1. Write a simple test spec or document detailing your "sign off" for the feature for **any _one_** of the tests above
2. Automated _**all**_ tests as part of a suite that can be run by simple command (CLI script, Postman collection, SoapUI test suite etc)


### Desirable requirement:
Demonstrate automation using a test framework like REST Assured, Karate or other framework, to showcase your understanding of using frameworks to test APIs

### Optional extra
1. Review the two frameworks ([REST Assured](https://www.pluralsight.com/courses/rest-assured-fundamentals) and [Karate](https://www.softwaretestinghelp.com/api-testing-with-karate-framework/)) and recommend which one you would prefer to use for testing a REST API and why.
2. Write a **_load test_** suite for the Loan REST API - options can include using either [JMeter](https://jmeter.apache.org/) or [Gatling](https://gatling.io/), or one of your own choice Load Test frameworks/Tools

# Getting up and running
Open [Swagger UI](https://assessment-api-loan.herokuapp.com/swagger-ui.html) on a browser:
http://localhost:8080/swagger-ui.html

There is a username/password required to access the swagger doc
```admin : password```

## Testing

An example of the rest request is given in the **postman collection** found in the ```docs``` folder




