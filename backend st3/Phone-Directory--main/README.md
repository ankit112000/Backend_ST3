
Web application "Phone book"
=======================================

Web service for storing contacts info.

User can register in the system and create/edit/delete storing records,
view them with the possibility of filtering by name/second name/phone number.

To deploy app You need <a href="http://www.oracle.com/technetwork/pt/java/javase/downloads/jdk8-downloads-2133151.html">Java JDK 8</a>, <a href="https://maven.apache.org/download.cgi">Maven</a>
<p>If You want to use local RDBMS You also need  <a href="https://www.postgresql.org/download/">PostgreSQL</a></p>

## Running phonebook locally
```
	git clone https://github.com/SergiyDyrda/Phone-Book
	cd Phone-Book
	./mvnw spring-boot:run
	
```

## Database configuration

In case you want to run it with local postgres database
open PostgreSQL console editor and execute following commands
```       
    CREATE DATABASE phonebook;   
    CREATE USER bookuser WITH password 'password';     
    GRANT ALL privileges ON DATABASE phonebook TO bookuser; 
```
then go to project folder and execute
```
   ./mvnw spring-boot:run -Drun.jvmArguments="-Dspring.profiles.active=postgres" -P postgres 
```