This is a modified version of SNMP4J 2.5.3 (http://snmp4j.org) SNMP4J was using log4j, which is a logging framework that is not compatible with OSGI environments. It's replaced with JDK Logging facility.

To make it a OSGI bundle, first download bnd-2.4.0.jar from http://central.maven.org/maven2/biz/aQute/bnd/bnd/2.4.0/bnd-2.4.0.jar
Then execute
java -jar bnd-2.4.0.jar wrap -p bnd.properties -o snmp4j-2.5.3-osgibundle.jar snmp4j-2.5.3.jar
with bnd.propeties given as follows:
```
version: 2.5.3
Bundle-ManifestVersion: 2
Bundle-SymbolicName: org.snmp4j
Bundle-Version: ${version}
Bundle-Name: snmp4j
Export-Package: *;version=${version}
Import-Package: *
```
