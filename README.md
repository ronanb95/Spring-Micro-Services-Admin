## Spring-Micro-Services ##

### Overview ###
This basic web application showcases the use of a micro service architecture. It is comprised of 3 individual service and 1 common service and is centred around the use of OPA, a policy decision engine.

### Code Reuse ###
This repository also showcases code reuse across the various microservices, made possible by the @ComponentScan annotation provided by Spring. This annotation is placeed in the common main application and picks up any @Component, @Service, @Repository and @Controller annotations within the basepackages added to @ComponentScan. You may notice that none of the other services actually have a main class and each is controlled through common's main class, made possible by the annotation mentioned above. Common mainly contains conde related to mongoDB. Therefore we can create a service that produces data for Mongo and another service that consumes data from Mongo, all while not having to repeat code related to mongo set up etc.

### Efficency ###
Please note that this application is not designed with efficency in mind. Therefore some architecture decisions have been made in order to shwcase certain features.

### Running the application ###
In order to run the opa executable use the command ./opa run --server
