# Labo01 - Environment Setup

* [Labo description](https://cpnv-es-ngy.gitbook.io/vir1/labs/labo01-environment-setup)

## DevOps Stack to setup

Mention in this documentation the orders carried out and the results obtained.

If you have opted for a graphical installation, provide screenshots and describe the procedure up to the result
obtained.

### Cloud cmd line interface - AWS Cli

```shell
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg ./AWSCLIV2.pkg -target /
which aws
> /usr/local/bin/aws
aws --version
> aws-cli/2.15.41 Python/3.11.8 Darwin/23.4.0 exe/x86_64 prompt/off
```

### IDE - Intellij

```
IntelliJ IDEA 2024.1 (Ultimate Edition)
Build #IU-241.14494.240, built on March 28, 2024
Licensed to Dimitri RUTZ
Subscription is active until September 14, 2024.
For educational use only.
Runtime version: 17.0.10+8-b1207.12 aarch64
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.
macOS 14.4.1
GC: G1 Young Generation, G1 Old Generation
Memory: 2048M
Cores: 10
Metal Rendering is ON
Registry:
  ide.experimental.ui=true
Non-Bundled Plugins:
  com.jetbrains.space (241.14494.150)
  com.intellij.ml.llm (241.14494.320)
  com.demonwav.minecraft-dev (2024.1-1.7.4)
Kotlin: 241.14494.240-IJ

```

### Containers Engine - Docker

```shell
> docker -v
Docker version 25.0.2, build 29cf629
```

### Versioning - Git + Git flow

```shell
> git -v
git version 2.44.0
> git flow version
0.4.1
```

### IDE Plugin - Docker plugin for IntelliJ

```
bundled 241.14494.240
```

### Development Kit - JDK

```shell
> java --version
java 17.0.11 2024-04-16 LTS
```

### Package manager - Maven

```shell
> brew install maven
Apache Maven 3.9.6 (bc0240f3c744dd6b6ec2920b3cd08dcc295161ae)
Maven home: /opt/homebrew/Cellar/maven/3.9.6/libexec
Java version: 17.0.9, vendor: JetBrains s.r.o., runtime: /Users/dimitrirutz/Library/Java/JavaVirtualMachines/jbrsdk-17.0.9/Contents/Home
Default locale: fr_CH, platform encoding: UTF-8
OS name: "mac os x", version: "14.4.1", arch: "aarch64", family: "mac"
```

## Schema

Show your development environment, mentioning all the components in the stack.

Identify the links between components.

![](schema.png)

## Analysis

Answer the questions below, giving reasons for your answer (link, source).

### AWS CLI

* How does the AWS Cli interact with the cloud ?

```
//TODO answer the question
```

* What other ways do we have of dialoguing/interacting with the AWS cloud if we wanted to do without the CLI?

```
Using the web app
```

* What commands do I need to run in the CLI to start an ec2 instance?

```
aws ec2 run-instances --image-id <AMI_ID> --instance-type <INSTANCE_TYPE> --key-name <KEY_PAIR_NAME> --security-group-ids <SECURITY_GROUP_ID>
```

### Docker Engine

* What type of hypervisor does Docker use?

```
Type 2 he is over the OS
```

* What role does the Docker Desktop play in the Docker architecture?

```
It play as an user interface to the containers and volumes
```

### Java Environment

* JDK, JRE, JVM... what's the difference?

```
JDK is to develop with Java.
JRE is the runtime that iclude de JVM that is the virtual machine on what the runtime will run and it's platform independant
```

### Maven

* What is the command you need to use Maven to retrieve dependencies (and only that)?

```
mvn dependency:resolve

And pom.xml that contains dependancy list
```

