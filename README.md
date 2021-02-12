# JAVA, Maven, and Ant Configuration Environment

![Linter Run](https://github.com/jeonghanlee/java-env/workflows/Linter%20Run/badge.svg)

## Java Packages

This is the JAVA packages (JDK, ANT, MAVEN) configuration environment. It supports Linux, and Darwin x86 and arm64. And it configures the predefined JAVA packages.

## Requirements

`wget` is required to download the java package.

* Debian

```bash
sudo apt install wget
```

* Fedora

```bash
sudo dnf install wget
```

* Darwin

```bash
sudo port install wget
```

### JAVA

* JDK 8 : <https://github.com/corretto/corretto-8> (Linux)
* JDK 11 : openjdk11 (Linux), azul jdk11 (Darwin x86, Darwin arm64)
* JDK 15 : openjdk15 (Linux), azul jdk15 (Darwin x86, Darwin arm64)

### MAVEN

* Maven 3.6.3

### ANT

* Ant 1.10.9

## Rules

### Default Installation Location `/opt/java-env`

```bash
make install
```

```bash
$  make conf
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/opt/java-env/JDK11
JAVA_PATH:=/opt/java-env/JDK11/bin
##
## JAVA Environment, Please pick one of them.
JAVA_HOME:=/opt/java-env/JDK15
JAVA_PATH:=/opt/java-env/JDK15/bin
##
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
JAVA_HOME:=/home/jhlee/java-env/JDK11
JAVA_PATH:=/home/jhlee/java-env/JDK11/bin
##
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
