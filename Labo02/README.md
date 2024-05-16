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

[OUTPUT]
```
~/PhpstormProjects/vir-labs/Labo02 git:[main]
mvn package
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------< org.springframework.samples:spring-petclinic >------------
[INFO] Building petclinic 3.2.0-SNAPSHOT
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- enforcer:3.4.1:enforce (enforce-java) @ spring-petclinic ---
[INFO] Rule 0: org.apache.maven.enforcer.rules.version.RequireJavaVersion passed
[INFO] 
[INFO] --- spring-javaformat:0.0.40:validate (default) @ spring-petclinic ---
[INFO] 
[INFO] --- checkstyle:3.3.1:check (nohttp-checkstyle-validation) @ spring-petclinic ---
[INFO] You have 0 Checkstyle violations.
[INFO] 
[INFO] --- jacoco:0.8.11:prepare-agent (default) @ spring-petclinic ---
[INFO] argLine set to -javaagent:/Users/dimitrirutz/.m2/repository/org/jacoco/org.jacoco.agent/0.8.11/org.jacoco.agent-0.8.11-runtime.jar=destfile=/Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/jacoco.exec
[INFO] 
[INFO] --- git-commit-id:6.0.0:revision (default) @ spring-petclinic ---
[INFO] dotGitDirectory '/Users/dimitrirutz/PhpstormProjects/vir-labs/.git'
[INFO] Collected git.build.user.name with value drutz-cpnv
[INFO] Collected git.build.user.email with value dimitri.rutz@eduvaud.ch
[INFO] Collected git.branch with value main
[INFO] --always = true
[INFO] --dirty = -dirty
[INFO] --abbrev = 7
[INFO] Tag refs [[]]
[INFO] Created map: [{}]
[INFO] evalCommit is [4c19ed73401dd31218dcb9c4d0f9fac7bdcf2dc7]
[INFO] Collected git.commit.id.describe with value 4c19ed7-dirty
[INFO] Collected git.commit.id.describe-short with value 4c19ed7-dirty
[INFO] Collected git.commit.id with value 4c19ed73401dd31218dcb9c4d0f9fac7bdcf2dc7
[INFO] Collected git.commit.id.abbrev with value 4c19ed7
[INFO] Collected git.dirty with value true
[INFO] Collected git.commit.user.name with value drutz-cpnv
[INFO] Collected git.commit.user.email with value dimitri.rutz@eduvaud.ch
[INFO] Collected git.commit.message.full with value chore: respect naming conventions
[INFO] Collected git.commit.message.short with value chore: respect naming conventions
[INFO] Collected git.commit.time with value 2024-05-16T08:33:31+0200
[INFO] Collected git.commit.author.time with value 2024-05-16T08:33:31+0200
[INFO] Collected git.commit.committer.time with value 2024-05-16T08:33:31+0200
[INFO] Collected git.remote.origin.url with value https://github.com/drutz-cpnv/vir-labs.git
[INFO] Collected git.tags with value 
[INFO] evalCommit is [4c19ed73401dd31218dcb9c4d0f9fac7bdcf2dc7]
[INFO] Tag refs [[]]
[INFO] Created map: [{}]
[INFO] Collected git.closest.tag.name with value 
[INFO] evalCommit is [4c19ed73401dd31218dcb9c4d0f9fac7bdcf2dc7]
[INFO] Tag refs [[]]
[INFO] Created map: [{}]
[INFO] Collected git.closest.tag.commit.count with value 
[INFO] Collected git.total.commit.count with value 30
[INFO] Collected git.local.branch.ahead with value 1
[INFO] Collected git.local.branch.behind with value 0
[INFO] Collected git.build.time with value 2023-05-10T09:42:50+0200
[INFO] Collected git.build.version with value 3.2.0-SNAPSHOT
[INFO] Collected git.build.host with value MacBook-Pro-de-Dimitri.local
[INFO] including property 'git.tags' in results
[INFO] including property 'git.build.version' in results
[INFO] including property 'git.branch' in results
[INFO] including property 'git.build.host' in results
[INFO] including property 'git.commit.id' in results
[INFO] including property 'git.commit.user.email' in results
[INFO] including property 'git.local.branch.behind' in results
[INFO] including property 'git.commit.author.time' in results
[INFO] including property 'git.build.user.name' in results
[INFO] including property 'git.dirty' in results
[INFO] including property 'git.closest.tag.commit.count' in results
[INFO] including property 'git.commit.user.name' in results
[INFO] including property 'git.commit.id.abbrev' in results
[INFO] including property 'git.commit.id.describe-short' in results
[INFO] including property 'git.total.commit.count' in results
[INFO] including property 'git.commit.id.describe' in results
[INFO] including property 'git.build.user.email' in results
[INFO] including property 'git.commit.message.short' in results
[INFO] including property 'git.commit.committer.time' in results
[INFO] including property 'git.closest.tag.name' in results
[INFO] including property 'git.local.branch.ahead' in results
[INFO] including property 'git.commit.time' in results
[INFO] including property 'git.build.time' in results
[INFO] including property 'git.commit.message.full' in results
[INFO] including property 'git.remote.origin.url' in results
[INFO] Reading existing properties file [/Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/classes/git.properties] (for project petclinic)...
[INFO] Writing properties file [/Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/classes/git.properties] (for project petclinic)...
[INFO] 
[INFO] --- spring-boot:3.2.1:build-info (default) @ spring-petclinic ---
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ spring-petclinic ---
[INFO] Copying 3 resources from src/main/resources to target/classes
[INFO] Copying 34 resources from src/main/resources to target/classes
[INFO] 
[INFO] --- compiler:3.11.0:compile (default-compile) @ spring-petclinic ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ spring-petclinic ---
[INFO] skip non existing resourceDirectory /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/src/test/resources
[INFO] 
[INFO] --- compiler:3.11.0:testCompile (default-testCompile) @ spring-petclinic ---
[INFO] Changes detected - recompiling the module! :input tree
[INFO] Compiling 12 source files with javac [debug release 17] to target/test-classes
[INFO] 
[INFO] --- surefire:3.1.2:test (default-test) @ spring-petclinic ---
[WARNING]  Parameter 'systemProperties' is deprecated: Use systemPropertyVariables instead.
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running org.springframework.samples.petclinic.vet.VetControllerTests
SLF4J: Class path contains multiple SLF4J providers.
SLF4J: Found provider [ch.qos.logback.classic.spi.LogbackServiceProvider@6ca320ab]
SLF4J: Found provider [org.slf4j.nop.NOPServiceProvider@50d68830]
SLF4J: Found provider [org.slf4j.jul.JULServiceProvider@1e53135d]
SLF4J: See https://www.slf4j.org/codes.html#multiple_bindings for an explanation.
SLF4J: Actual provider is of type [ch.qos.logback.classic.spi.LogbackServiceProvider@6ca320ab]
08:57:24.113 [main] INFO org.springframework.test.context.support.AnnotationConfigContextLoaderUtils -- Could not detect default configuration classes for test class [org.springframework.samples.petclinic.vet.VetControllerTests]: VetControllerTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
08:57:24.267 [main] INFO org.springframework.boot.test.context.SpringBootTestContextBootstrapper -- Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.vet.VetControllerTests
08:57:24.344 [main] INFO org.springframework.boot.devtools.restart.RestartApplicationListener -- Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:24.603+02:00  INFO 5240 --- [           main] o.s.s.petclinic.vet.VetControllerTests   : Starting VetControllerTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:24.604+02:00  INFO 5240 --- [           main] o.s.s.petclinic.vet.VetControllerTests   : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:26.401+02:00  INFO 5240 --- [           main] o.s.b.t.m.w.SpringBootMockServletContext : Initializing Spring TestDispatcherServlet ''
2024-05-16T08:57:26.401+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Initializing Servlet ''
2024-05-16T08:57:26.402+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Completed initialization in 1 ms
2024-05-16T08:57:26.428+02:00  INFO 5240 --- [           main] o.s.s.petclinic.vet.VetControllerTests   : Started VetControllerTests in 2.094 seconds (process running for 3.076)
[INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 3.235 s -- in org.springframework.samples.petclinic.vet.VetControllerTests
[INFO] Running org.springframework.samples.petclinic.vet.VetTests
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.068 s -- in org.springframework.samples.petclinic.vet.VetTests
[INFO] Running org.springframework.samples.petclinic.owner.OwnerControllerTests
2024-05-16T08:57:27.258+02:00  INFO 5240 --- [           main] t.c.s.AnnotationConfigContextLoaderUtils : Could not detect default configuration classes for test class [org.springframework.samples.petclinic.owner.OwnerControllerTests]: OwnerControllerTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
2024-05-16T08:57:27.274+02:00  INFO 5240 --- [           main] .b.t.c.SpringBootTestContextBootstrapper : Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.owner.OwnerControllerTests
2024-05-16T08:57:27.277+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:27.291+02:00  INFO 5240 --- [           main] o.s.s.p.owner.OwnerControllerTests       : Starting OwnerControllerTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:27.291+02:00  INFO 5240 --- [           main] o.s.s.p.owner.OwnerControllerTests       : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:27.459+02:00  INFO 5240 --- [           main] o.s.b.t.m.w.SpringBootMockServletContext : Initializing Spring TestDispatcherServlet ''
2024-05-16T08:57:27.460+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Initializing Servlet ''
2024-05-16T08:57:27.460+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Completed initialization in 0 ms
2024-05-16T08:57:27.465+02:00  INFO 5240 --- [           main] o.s.s.p.owner.OwnerControllerTests       : Started OwnerControllerTests in 0.188 seconds (process running for 4.113)
[INFO] Tests run: 12, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.434 s -- in org.springframework.samples.petclinic.owner.OwnerControllerTests
[INFO] Running org.springframework.samples.petclinic.owner.PetControllerTests
2024-05-16T08:57:27.697+02:00  INFO 5240 --- [           main] t.c.s.AnnotationConfigContextLoaderUtils : Could not detect default configuration classes for test class [org.springframework.samples.petclinic.owner.PetControllerTests]: PetControllerTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
2024-05-16T08:57:27.702+02:00  INFO 5240 --- [           main] .b.t.c.SpringBootTestContextBootstrapper : Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.owner.PetControllerTests
2024-05-16T08:57:27.712+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:27.722+02:00  INFO 5240 --- [           main] o.s.s.p.owner.PetControllerTests         : Starting PetControllerTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:27.723+02:00  INFO 5240 --- [           main] o.s.s.p.owner.PetControllerTests         : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:27.830+02:00  INFO 5240 --- [           main] o.s.b.t.m.w.SpringBootMockServletContext : Initializing Spring TestDispatcherServlet ''
2024-05-16T08:57:27.830+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Initializing Servlet ''
2024-05-16T08:57:27.830+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Completed initialization in 0 ms
2024-05-16T08:57:27.834+02:00  INFO 5240 --- [           main] o.s.s.p.owner.PetControllerTests         : Started PetControllerTests in 0.123 seconds (process running for 4.483)
[INFO] Tests run: 6, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.205 s -- in org.springframework.samples.petclinic.owner.PetControllerTests
[INFO] Running org.springframework.samples.petclinic.owner.VisitControllerTests
2024-05-16T08:57:27.903+02:00  INFO 5240 --- [           main] t.c.s.AnnotationConfigContextLoaderUtils : Could not detect default configuration classes for test class [org.springframework.samples.petclinic.owner.VisitControllerTests]: VisitControllerTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
2024-05-16T08:57:27.908+02:00  INFO 5240 --- [           main] .b.t.c.SpringBootTestContextBootstrapper : Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.owner.VisitControllerTests
2024-05-16T08:57:27.911+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:27.921+02:00  INFO 5240 --- [           main] o.s.s.p.owner.VisitControllerTests       : Starting VisitControllerTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:27.921+02:00  INFO 5240 --- [           main] o.s.s.p.owner.VisitControllerTests       : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:28.027+02:00  INFO 5240 --- [           main] o.s.b.t.m.w.SpringBootMockServletContext : Initializing Spring TestDispatcherServlet ''
2024-05-16T08:57:28.027+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Initializing Servlet ''
2024-05-16T08:57:28.027+02:00  INFO 5240 --- [           main] o.s.t.web.servlet.TestDispatcherServlet  : Completed initialization in 0 ms
2024-05-16T08:57:28.031+02:00  INFO 5240 --- [           main] o.s.s.p.owner.VisitControllerTests       : Started VisitControllerTests in 0.12 seconds (process running for 4.679)
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.168 s -- in org.springframework.samples.petclinic.owner.VisitControllerTests
[INFO] Running org.springframework.samples.petclinic.owner.PetTypeFormatterTests
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.021 s -- in org.springframework.samples.petclinic.owner.PetTypeFormatterTests
[INFO] Running org.springframework.samples.petclinic.system.CrashControllerTests
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in org.springframework.samples.petclinic.system.CrashControllerTests
[INFO] Running org.springframework.samples.petclinic.system.CrashControllerIntegrationTests
2024-05-16T08:57:28.108+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:28.122+02:00  INFO 5240 --- [           main] .s.s.p.s.CrashControllerIntegrationTests : Starting CrashControllerIntegrationTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:28.123+02:00  INFO 5240 --- [           main] .s.s.p.s.CrashControllerIntegrationTests : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:28.845+02:00  INFO 5240 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port 0 (http)
2024-05-16T08:57:28.858+02:00  INFO 5240 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2024-05-16T08:57:28.858+02:00  INFO 5240 --- [           main] o.apache.catalina.core.StandardEngine    : Starting Servlet engine: [Apache Tomcat/10.1.17]
2024-05-16T08:57:28.906+02:00  INFO 5240 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2024-05-16T08:57:28.906+02:00  INFO 5240 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 782 ms
2024-05-16T08:57:29.402+02:00  INFO 5240 --- [           main] o.s.b.a.e.web.EndpointLinksResolver      : Exposing 0 endpoint(s) beneath base path '/actuator'
2024-05-16T08:57:29.471+02:00  INFO 5240 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port 54843 (http) with context path ''
2024-05-16T08:57:29.477+02:00  INFO 5240 --- [           main] .s.s.p.s.CrashControllerIntegrationTests : Started CrashControllerIntegrationTests in 1.369 seconds (process running for 6.125)
2024-05-16T08:57:29.576+02:00  INFO 5240 --- [o-auto-1-exec-1] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring DispatcherServlet 'dispatcherServlet'
2024-05-16T08:57:29.576+02:00  INFO 5240 --- [o-auto-1-exec-1] o.s.web.servlet.DispatcherServlet        : Initializing Servlet 'dispatcherServlet'
2024-05-16T08:57:29.577+02:00  INFO 5240 --- [o-auto-1-exec-1] o.s.web.servlet.DispatcherServlet        : Completed initialization in 1 ms
2024-05-16T08:57:29.586+02:00 ERROR 5240 --- [o-auto-1-exec-1] o.a.c.c.C.[.[.[/].[dispatcherServlet]    : Servlet.service() for servlet [dispatcherServlet] in context with path [] threw exception [Request processing failed: java.lang.RuntimeException: Expected: controller used to showcase what happens when an exception is thrown] with root cause

java.lang.RuntimeException: Expected: controller used to showcase what happens when an exception is thrown
        at org.springframework.samples.petclinic.system.CrashController.triggerException(CrashController.java:33) ~[classes/:na]
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:na]
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77) ~[na:na]
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:na]
        at java.base/java.lang.reflect.Method.invoke(Method.java:568) ~[na:na]
        at org.springframework.web.method.support.InvocableHandlerMethod.doInvoke(InvocableHandlerMethod.java:262) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.method.support.InvocableHandlerMethod.invokeForRequest(InvocableHandlerMethod.java:190) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.ServletInvocableHandlerMethod.invokeAndHandle(ServletInvocableHandlerMethod.java:118) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter.invokeHandlerMethod(RequestMappingHandlerAdapter.java:917) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter.handleInternal(RequestMappingHandlerAdapter.java:829) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.AbstractHandlerMethodAdapter.handle(AbstractHandlerMethodAdapter.java:87) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.DispatcherServlet.doDispatch(DispatcherServlet.java:1089) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.DispatcherServlet.doService(DispatcherServlet.java:979) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.FrameworkServlet.processRequest(FrameworkServlet.java:1014) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.FrameworkServlet.doGet(FrameworkServlet.java:903) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at jakarta.servlet.http.HttpServlet.service(HttpServlet.java:564) ~[tomcat-embed-core-10.1.17.jar:6.0]
        at org.springframework.web.servlet.FrameworkServlet.service(FrameworkServlet.java:885) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at jakarta.servlet.http.HttpServlet.service(HttpServlet.java:658) ~[tomcat-embed-core-10.1.17.jar:6.0]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:205) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.websocket.server.WsFilter.doFilter(WsFilter.java:51) ~[tomcat-embed-websocket-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.RequestContextFilter.doFilterInternal(RequestContextFilter.java:100) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.FormContentFilter.doFilterInternal(FormContentFilter.java:93) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.ServerHttpObservationFilter.doFilterInternal(ServerHttpObservationFilter.java:109) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.CharacterEncodingFilter.doFilterInternal(CharacterEncodingFilter.java:201) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardWrapperValve.invoke(StandardWrapperValve.java:167) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardContextValve.invoke(StandardContextValve.java:90) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.authenticator.AuthenticatorBase.invoke(AuthenticatorBase.java:482) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardHostValve.invoke(StandardHostValve.java:115) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:93) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardEngineValve.invoke(StandardEngineValve.java:74) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:340) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.http11.Http11Processor.service(Http11Processor.java:391) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.AbstractProcessorLight.process(AbstractProcessorLight.java:63) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.AbstractProtocol$ConnectionHandler.process(AbstractProtocol.java:896) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1744) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:52) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1191) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:659) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at java.base/java.lang.Thread.run(Thread.java:840) ~[na:na]

2024-05-16T08:57:29.633+02:00 ERROR 5240 --- [o-auto-1-exec-2] o.a.c.c.C.[.[.[/].[dispatcherServlet]    : Servlet.service() for servlet [dispatcherServlet] in context with path [] threw exception [Request processing failed: java.lang.RuntimeException: Expected: controller used to showcase what happens when an exception is thrown] with root cause

java.lang.RuntimeException: Expected: controller used to showcase what happens when an exception is thrown
        at org.springframework.samples.petclinic.system.CrashController.triggerException(CrashController.java:33) ~[classes/:na]
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:na]
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77) ~[na:na]
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:na]
        at java.base/java.lang.reflect.Method.invoke(Method.java:568) ~[na:na]
        at org.springframework.web.method.support.InvocableHandlerMethod.doInvoke(InvocableHandlerMethod.java:262) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.method.support.InvocableHandlerMethod.invokeForRequest(InvocableHandlerMethod.java:190) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.ServletInvocableHandlerMethod.invokeAndHandle(ServletInvocableHandlerMethod.java:118) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter.invokeHandlerMethod(RequestMappingHandlerAdapter.java:917) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter.handleInternal(RequestMappingHandlerAdapter.java:829) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.mvc.method.AbstractHandlerMethodAdapter.handle(AbstractHandlerMethodAdapter.java:87) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.DispatcherServlet.doDispatch(DispatcherServlet.java:1089) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.DispatcherServlet.doService(DispatcherServlet.java:979) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.FrameworkServlet.processRequest(FrameworkServlet.java:1014) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at org.springframework.web.servlet.FrameworkServlet.doGet(FrameworkServlet.java:903) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at jakarta.servlet.http.HttpServlet.service(HttpServlet.java:564) ~[tomcat-embed-core-10.1.17.jar:6.0]
        at org.springframework.web.servlet.FrameworkServlet.service(FrameworkServlet.java:885) ~[spring-webmvc-6.1.2.jar:6.1.2]
        at jakarta.servlet.http.HttpServlet.service(HttpServlet.java:658) ~[tomcat-embed-core-10.1.17.jar:6.0]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:205) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.websocket.server.WsFilter.doFilter(WsFilter.java:51) ~[tomcat-embed-websocket-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.RequestContextFilter.doFilterInternal(RequestContextFilter.java:100) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.FormContentFilter.doFilterInternal(FormContentFilter.java:93) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.ServerHttpObservationFilter.doFilterInternal(ServerHttpObservationFilter.java:109) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.springframework.web.filter.CharacterEncodingFilter.doFilterInternal(CharacterEncodingFilter.java:201) ~[spring-web-6.1.2.jar:6.1.2]
        at org.springframework.web.filter.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:116) ~[spring-web-6.1.2.jar:6.1.2]
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:174) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:149) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardWrapperValve.invoke(StandardWrapperValve.java:167) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardContextValve.invoke(StandardContextValve.java:90) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.authenticator.AuthenticatorBase.invoke(AuthenticatorBase.java:482) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardHostValve.invoke(StandardHostValve.java:115) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:93) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.core.StandardEngineValve.invoke(StandardEngineValve.java:74) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:340) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.http11.Http11Processor.service(Http11Processor.java:391) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.AbstractProcessorLight.process(AbstractProcessorLight.java:63) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.coyote.AbstractProtocol$ConnectionHandler.process(AbstractProtocol.java:896) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1744) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:52) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1191) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:659) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61) ~[tomcat-embed-core-10.1.17.jar:10.1.17]
        at java.base/java.lang.Thread.run(Thread.java:840) ~[na:na]

[INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 1.561 s -- in org.springframework.samples.petclinic.system.CrashControllerIntegrationTests
[INFO] Running org.springframework.samples.petclinic.model.ValidatorTests
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.010 s -- in org.springframework.samples.petclinic.model.ValidatorTests
[INFO] Running org.springframework.samples.petclinic.service.ClinicServiceTests
2024-05-16T08:57:29.673+02:00  INFO 5240 --- [           main] t.c.s.AnnotationConfigContextLoaderUtils : Could not detect default configuration classes for test class [org.springframework.samples.petclinic.service.ClinicServiceTests]: ClinicServiceTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
2024-05-16T08:57:29.683+02:00  INFO 5240 --- [           main] .b.t.c.SpringBootTestContextBootstrapper : Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.service.ClinicServiceTests
2024-05-16T08:57:29.686+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:29.697+02:00  INFO 5240 --- [           main] o.s.s.p.service.ClinicServiceTests       : Starting ClinicServiceTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:29.697+02:00  INFO 5240 --- [           main] o.s.s.p.service.ClinicServiceTests       : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:29.789+02:00  INFO 5240 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2024-05-16T08:57:29.816+02:00  INFO 5240 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 20 ms. Found 2 JPA repository interfaces.
2024-05-16T08:57:29.884+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2024-05-16T08:57:30.134+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Added connection conn0: url=jdbc:h2:mem:674f4dae-a8e0-4f71-a999-cd41caa0edba user=SA
2024-05-16T08:57:30.135+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Start completed.
2024-05-16T08:57:30.230+02:00  INFO 5240 --- [           main] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [name: default]
2024-05-16T08:57:30.289+02:00  INFO 5240 --- [           main] org.hibernate.Version                    : HHH000412: Hibernate ORM core version 6.4.1.Final
2024-05-16T08:57:30.318+02:00  INFO 5240 --- [           main] o.h.c.internal.RegionFactoryInitiator    : HHH000026: Second-level cache disabled
2024-05-16T08:57:30.416+02:00  INFO 5240 --- [           main] o.s.o.j.p.SpringPersistenceUnitInfo      : No LoadTimeWeaver setup: ignoring JPA class transformer
2024-05-16T08:57:31.195+02:00  INFO 5240 --- [           main] o.h.e.t.j.p.i.JtaPlatformInitiator       : HHH000489: No JTA platform available (set 'hibernate.transaction.jta.platform' to enable JTA platform integration)
2024-05-16T08:57:31.196+02:00  INFO 5240 --- [           main] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2024-05-16T08:57:31.365+02:00  INFO 5240 --- [           main] o.s.d.j.r.query.QueryEnhancerFactory     : Hibernate is in classpath; If applicable, HQL parser will be used.
2024-05-16T08:57:31.683+02:00  INFO 5240 --- [           main] o.s.s.p.service.ClinicServiceTests       : Started ClinicServiceTests in 1.997 seconds (process running for 8.332)
Hibernate: select v1_0.id,v1_0.first_name,v1_0.last_name from vets v1_0
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select s1_0.vet_id,s1_1.id,s1_1.name from vet_specialties s1_0 join specialties s1_1 on s1_1.id=s1_0.specialty_id where s1_0.vet_id=?
Hibernate: select distinct o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.last_name like ? escape ''
Hibernate: select p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,t1_0.id,t1_0.name from pets p1_0 left join types t1_0 on t1_0.id=p1_0.type_id where p1_0.owner_id=? order by p1_0.name
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,t1_0.id,t1_0.name from pets p1_0 left join types t1_0 on t1_0.id=p1_0.type_id where p1_0.owner_id=? order by p1_0.name
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select distinct o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.last_name like ? escape ''
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: insert into visits (visit_date,description,id) values (?,?,default)
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: update owners set address=?,city=?,first_name=?,last_name=?,telephone=? where id=?
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 order by pt1_0.name
Hibernate: insert into pets (birth_date,name,type_id,id) values (?,?,?,default)
Hibernate: update pets set owner_id=? where id=?
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select distinct o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.last_name like ? escape ''
Hibernate: insert into owners (address,city,first_name,last_name,telephone,id) values (?,?,?,?,?,default)
Hibernate: select distinct o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.last_name like ? escape ''
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 where pt1_0.id=?
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: select v1_0.pet_id,v1_0.id,v1_0.visit_date,v1_0.description from visits v1_0 where v1_0.pet_id=? order by v1_0.visit_date
Hibernate: update pets set birth_date=?,name=?,type_id=? where id=?
Hibernate: select o1_0.id,o1_0.address,o1_0.city,o1_0.first_name,o1_0.last_name,p1_0.owner_id,p1_0.id,p1_0.birth_date,p1_0.name,p1_0.type_id,o1_0.telephone from owners o1_0 left join pets p1_0 on o1_0.id=p1_0.owner_id where o1_0.id=? order by p1_0.name
Hibernate: select pt1_0.id,pt1_0.name from types pt1_0 order by pt1_0.name
[INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 2.291 s -- in org.springframework.samples.petclinic.service.ClinicServiceTests
[INFO] Running org.springframework.samples.petclinic.PetClinicIntegrationTests
2024-05-16T08:57:31.965+02:00  INFO 5240 --- [           main] t.c.s.AnnotationConfigContextLoaderUtils : Could not detect default configuration classes for test class [org.springframework.samples.petclinic.PetClinicIntegrationTests]: PetClinicIntegrationTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
2024-05-16T08:57:31.968+02:00  INFO 5240 --- [           main] .b.t.c.SpringBootTestContextBootstrapper : Found @SpringBootConfiguration org.springframework.samples.petclinic.PetClinicApplication for test class org.springframework.samples.petclinic.PetClinicIntegrationTests
2024-05-16T08:57:31.975+02:00  INFO 5240 --- [           main] o.s.b.d.r.RestartApplicationListener     : Restart disabled due to context in which it is running


              |\      _,,,--,,_
             /,`.-'`'   ._  \-;;,_
  _______ __|,4-  ) )_   .;.(__`'-'__     ___ __    _ ___ _______
 |       | '---''(_/._)-'(_\_)   |   |   |   |  |  | |   |       |
 |    _  |    ___|_     _|       |   |   |   |   |_| |   |       | __ _ _
 |   |_| |   |___  |   | |       |   |   |   |       |   |       | \ \ \ \
 |    ___|    ___| |   | |      _|   |___|   |  _    |   |      _|  \ \ \ \
 |   |   |   |___  |   | |     |_|       |   | | |   |   |     |_    ) ) ) )
 |___|   |_______| |___| |_______|_______|___|_|  |__|___|_______|  / / / /
 ==================================================================/_/_/_/

:: Built with Spring Boot :: 3.2.1


2024-05-16T08:57:31.984+02:00  INFO 5240 --- [           main] o.s.s.p.PetClinicIntegrationTests        : Starting PetClinicIntegrationTests using Java 17.0.9 with PID 5240 (started by dimitrirutz in /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02)
2024-05-16T08:57:31.984+02:00  INFO 5240 --- [           main] o.s.s.p.PetClinicIntegrationTests        : No active profile set, falling back to 1 default profile: "default"
2024-05-16T08:57:32.119+02:00  INFO 5240 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2024-05-16T08:57:32.123+02:00  INFO 5240 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 3 ms. Found 2 JPA repository interfaces.
2024-05-16T08:57:32.237+02:00  INFO 5240 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port 0 (http)
2024-05-16T08:57:32.237+02:00  INFO 5240 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2024-05-16T08:57:32.237+02:00  INFO 5240 --- [           main] o.apache.catalina.core.StandardEngine    : Starting Servlet engine: [Apache Tomcat/10.1.17]
2024-05-16T08:57:32.248+02:00  INFO 5240 --- [           main] o.a.c.c.C.[Tomcat-1].[localhost].[/]     : Initializing Spring embedded WebApplicationContext
2024-05-16T08:57:32.248+02:00  INFO 5240 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 262 ms
2024-05-16T08:57:32.327+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-2 - Starting...
2024-05-16T08:57:32.328+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-2 - Added connection conn10: url=jdbc:h2:mem:98bfa709-cc5f-4ca6-bfb4-9d7a8edab41b user=SA
2024-05-16T08:57:32.328+02:00  INFO 5240 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-2 - Start completed.
2024-05-16T08:57:32.358+02:00  INFO 5240 --- [           main] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [name: default]
2024-05-16T08:57:32.360+02:00  INFO 5240 --- [           main] o.h.c.internal.RegionFactoryInitiator    : HHH000026: Second-level cache disabled
2024-05-16T08:57:32.362+02:00  INFO 5240 --- [           main] o.s.o.j.p.SpringPersistenceUnitInfo      : No LoadTimeWeaver setup: ignoring JPA class transformer
2024-05-16T08:57:32.426+02:00  INFO 5240 --- [           main] o.h.e.t.j.p.i.JtaPlatformInitiator       : HHH000489: No JTA platform available (set 'hibernate.transaction.jta.platform' to enable JTA platform integration)
2024-05-16T08:57:32.426+02:00  INFO 5240 --- [           main] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2024-05-16T08:57:32.839+02:00  INFO 5240 --- [           main] o.s.b.a.e.web.EndpointLinksResolver      : Exposing 13 endpoint(s) beneath base path '/actuator'
2024-05-16T08:57:32.865+02:00  INFO 5240 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port 54846 (http) with context path ''
2024-05-16T08:57:32.870+02:00  INFO 5240 --- [           main] o.s.s.p.PetClinicIntegrationTests        : Started PetClinicIntegrationTests in 0.895 seconds (process running for 9.518)
2024-05-16T08:57:32.896+02:00  INFO 5240 --- [o-auto-2-exec-1] o.a.c.c.C.[Tomcat-1].[localhost].[/]     : Initializing Spring DispatcherServlet 'dispatcherServlet'
2024-05-16T08:57:32.896+02:00  INFO 5240 --- [o-auto-2-exec-1] o.s.web.servlet.DispatcherServlet        : Initializing Servlet 'dispatcherServlet'
2024-05-16T08:57:32.896+02:00  INFO 5240 --- [o-auto-2-exec-1] o.s.web.servlet.DispatcherServlet        : Completed initialization in 0 ms
[INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.963 s -- in org.springframework.samples.petclinic.PetClinicIntegrationTests
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 43, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] --- jacoco:0.8.11:report (report) @ spring-petclinic ---
[INFO] Loading execution data file /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/jacoco.exec
[INFO] Analyzed bundle 'petclinic' with 21 classes
[INFO] 
[INFO] --- jar:3.3.0:jar (default-jar) @ spring-petclinic ---
[INFO] Building jar: /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/spring-petclinic-3.2.0-SNAPSHOT.jar
[INFO] 
[INFO] --- spring-boot:3.2.1:repackage (repackage) @ spring-petclinic ---
[INFO] Replacing main artifact /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/spring-petclinic-3.2.0-SNAPSHOT.jar with repackaged archive, adding nested dependencies in BOOT-INF/.
[INFO] The original artifact has been renamed to /Users/dimitrirutz/PhpstormProjects/vir-labs/Labo02/target/spring-petclinic-3.2.0-SNAPSHOT.jar.original
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  13.577 s
[INFO] Finished at: 2024-05-16T08:57:33+02:00
[INFO] ------------------------------------------------------------------------
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
3 the models, the controllers and the views
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
