This is a modified version of SNMP4J 2.5.3 (http://snmp4j.org)
SNMP4J was lacking of OSGI bundle definitions so org.apache.felix:maven-bundle-plugin introduced.
Also SNMP4J was using log4j, which is a logging framework that is not compatible with OSGI environments. It's replaced with JDK Logging facility.
