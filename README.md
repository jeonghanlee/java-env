# JAVA, Maven, and Ant Configuration Environment

![Linter Run](https://github.com/jeonghanlee/java-env/workflows/Linter%20Run/badge.svg)

## Java Packages

### JAVA

* JDK 8 : <https://github.com/corretto/corretto-8>

* JDK 11 : openjdk11

* JDK 12 : openjdk12

### MAVEN

* Maven 3.6.3 : latest

### ANT

* Ant 1.10.8 :
* Ant 1.10.9 : latest

## Rules

### Default Installation Location `/opt/java-env`

```bash
make install
```

```bash
$ make conf
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/opt/java-env/JDK8
JAVA_PATH:=/opt/java-env/JDK8/bin
##
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/opt/java-env/JDK11
JAVA_PATH:=/opt/java-env/JDK11/bin
##
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/opt/java-env/JDK12
JAVA_PATH:=/opt/java-env/JDK12/bin
##
## ANT Environment, Please pick one of them.
ANT_HOME:=/opt/java-env/ANT1108
ANT_PATH:=/opt/java-env/ANT1108/bin
## ANT Environment, Please pick one of them.
ANT_HOME:=/opt/java-env/ANT1109
ANT_PATH:=/opt/java-env/ANT1109/bin
##
## MAVEN Environment, Please pick one of them.
MAVEN_HOME:=/opt/java-env/MAVEN363
MAVEN_PATH:=/opt/java-env/MAVEN363/bin
##
```

### Customized Intallation Location

```bash
echo "INSTALL_LOCATION=${HOME}/java-env" > configure/CONFIG_SITE.local
```

```bash
make clean
make install
```

```bash
java-env (master)$ make conf
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/home/jhlee/java-env/JDK8
JAVA_PATH:=/home/jhlee/java-env/JDK8/bin
##
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/home/jhlee/java-env/JDK11
JAVA_PATH:=/home/jhlee/java-env/JDK11/bin
##
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/home/jhlee/java-env/JDK12
JAVA_PATH:=/home/jhlee/java-env/JDK12/bin
##
## ANT Environment, Please pick one of them.
ANT_HOME:=/home/jhlee/java-env/ANT1108
ANT_PATH:=/home/jhlee/java-env/ANT1108/bin
## ANT Environment, Please pick one of them.
ANT_HOME:=/home/jhlee/java-env/ANT1109
ANT_PATH:=/home/jhlee/java-env/ANT1109/bin
##
## MAVEN Environment, Please pick one of them.
MAVEN_HOME:=/home/jhlee/java-env/MAVEN363
MAVEN_PATH:=/home/jhlee/java-env/MAVEN363/bin
##
```

### More Rules

```bash
make uninstall

make jdk.install
make jdk.uninstall
make jdk.clean
make jdk.conf

make mvn.install
make mvn.uninstall
make mvn.clean
make mvn.conf

make ant.install
make ant.uninstall
make mvn.clean
make ant.conf
```
