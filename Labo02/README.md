# Labo02 - Run a Spring App Locally

## Pedagogical intent
In this lab, we'll be taking the application we're going to evolve into our own hands, to discover the Spring architecture.

---

## Task 01 - Run the app

### Use Maven to package the solution

* [Maven Doc](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html#build-the-project)

```bash
mvn package
```

* What operation does maven perform ?

```
Download packages and build the dependencies
1. validate
2. generate-sources
3. process-sources
4. generate-resources
5. process-resources
6. compile
```

* What java dependencies are needed to make this work?

```
All dependencies are listed in the pom.xml file
```

* Where do we find the pre-compiled application after that?

```
In './target' Directory
```

* Delete the folder containing the pre-compiled application, try again to observe the process.

* Is it a build ready for prod ?

```
No
```

### Use Java to launch the application

* [The java command](https://docs.oracle.com/en/java/javase/14/docs/specs/man/java.html)

```bash
java -jar target/spring-petclinic-3.2.0-SNAPSHOT.jar
```

* Try to access to the app via your browser

```
It work correctly on localhost:8080
```

* You should get this page

![Home Page](img/webappSample.JPG)

* Stop the app

## Use the Spring Boot Maven plugin to launch the application

* [Maven plug in to run the app](https://docs.spring.io/spring-boot/docs/current/maven-plugin/reference/htmlsingle/#run)

```
BEFORE:
in project > dependencies
<dependency>
  <groupId>org.codehaus.mojo</groupId>
  <artifactId>exec-maven-plugin</artifactId>
  <version>1.6.0</version>
</dependency>

AND
in project > build > plugins
<plugin>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>exec-maven-plugin</artifactId>
    <version>1.6.0</version>
    <configuration>
      <mainClass>org.springframework.samples.petclinic.PetClinicApplication</mainClass>
    </configuration>
</plugin>
```

```bash
mvn exec:java
```

---

## Task 02 - Explore the app

### Kind of app

* How can we access a home page via our browser?

```
Type localhost:8080 in your address bar
```

* Go to http://localhost:8080/owners/find and add an owner

* Using the search function, can you find it?

* Relaunch the application and try again. How is data persistence ensured?

```
The data are cached
```

* How many logic layers are implemented on this application?

```
//TODO
```

---
## Task 03 - Docker - First Analysis

* At this stage of the analysis, can you imagine a little better what kind of needs Docker could help us with?

```
//TODO
```

* Try to list the tasks to be carried out to obtain two tiers, one hosting the application part locally and the second tier using Docker for the database engine.

```
//TODO
```
