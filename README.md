# Springbootsamples

The system is designed to run the Springboot application to run individually using the java command.

Example is to demo how to avoid cross origin (CROS)issue when integrated with springboot application with angular 
application running on the same system 

Access to XMLHttpRequest at '<serviceurl>' from origin 
'<ipaddress:port>' has been blocked by CORS policy: Response to preflight  request doesn't pass access control 
check: It does not have HTTP ok status.

Step 1) MongoDB needs to be started since I am using MAC 

I have started by navigating to mongodb/bin folder and run the command
$mongod

Step 2) Spring Service 
CustomerController.java 

Changed annonation 
From 

@CrossOrigin(origins = "http://localhost:4200")
To 
@CrossOrigin(origins = "*")

Step 3)In Application properties 

Added 
server.address=<ipaddress>
server.port=<port>


Run the sprint boot application using 

Java – jar spring-boot-rest-mongodb-0.0.1-SNAPSHOT.jar

Before running the above command make sure that mongodb is running

