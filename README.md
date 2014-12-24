# *comsat-mvn-archetype*

A [Parallel Universe Comsat](http://www.paralleluniverse.co/comsat/) Maven archetype for Tomcat standalone Java 1.7+ applications.

## Getting started

```
git clone https://github.com/puniverse/comsat-mvn-archetype
cd comsat-mvn-archetype
mvn install
cd ..
mvn archetype:generate -DarchetypeGroupId=co.paralleluniverse -DarchetypeArtifactId=comsat-mvn-archetype -DarchetypeVersion=0.1.0 -DgroupId=testgrp -DartifactId=testprj
cd testprj
mvn -Ptomcat7x dependency:properties clean verify
mvn -Ptomcat8x dependency:properties clean verify
```

Other useful properties to set during project generation are `-DjavaVersion=<1.7|1.8> -DquasarVersion=<quasarVersion, e.g. 0.6.2> -DcomsatVersion=<comsatVersion, e.g. 0.3.0> -Dtomcat7Version=<tomcat7Version, e.g. 7.0.56> -Dtomcat8Version=<tomcat8Version, e.g. 8.0.15> -Djetty8Version=<jetty8Version, e.g. 8.1.15.v20140411> -Djetty9Version=<jetty9Version, e.g. 9.2.1.v20140609 or 9.2.4.v20141103> -DuseWebXml=<true|false>`

The result of cargo deployments can be inspected in `target/cargo/configurations`.
