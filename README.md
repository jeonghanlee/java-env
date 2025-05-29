# Very Simple JAVA and Maven Configuration Environment


## JAVA and Maven

* OpenJDK 21
* Maven 3.9.9

## Default Installation Location `/opt/java-env`

```bash
make install
```

```bash
## JAVA Environment
JAVA_HOME=/opt/java-env/JDK
JAVA_PATH=/opt/java-env/JDK/bin
##
## MAVEN Environment
MAVEN_HOME=/opt/java-env/MAVEN
MAVEN_PATH=/opt/java-env/MAVEN/bin
##
```

## Customized Intallation Location

```bash
echo "INSTALL_LOCATION=${HOME}/java-env" > configure/CONFIG_SITE.local
```

## Uninstall

```bash
make uninstall
```

