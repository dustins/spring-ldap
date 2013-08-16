##Spring LDAP

###INTRODUCTION

Spring LDAP is a library to simplify LDAP programming in Java, built on the same
principles as Spring Jdbc. 

The LdapTemplate class encapsulates all the plumbing work involved in traditional LDAP 
programming, such as creating, looping through NamingEnumerations, handling Exceptions
and cleaning up resources. This leaves the programmer to handle the important stuff - 
where to find data (DNs and Filters) and what do do with it (map to and from domain 
objects, bind, modify, unbind, etc.), in the same way that JdbcTemplate relieves the 
programmer of all but the actual SQL and how the data maps to the domain model.

In addition to this, Spring LDAP provides Exception translation from NamingExceptions
to an unchecked exception hirearchy, as well as several utilities for working with filters,
LDAP paths and Attributes.

As of version 1.2, support for client-side compensating transaction is provided, as well as 
Java 5 generics support with the SimpleLdapTemplate.

As of version 1.3.1, there is support for LDIF parsing and Object-Directory Mapping (ODM).

For detailed information on the project, please refer to the [reference documentation](http://static.springsource.org/spring-ldap/docs/1.3.x/reference/html/) and [javadocs](http://static.springsource.org/spring-ldap/site/apidocs/).
See [the changelog](https://jira.springsource.org/browse/LDAP#selectedTab=com.atlassian.jira.plugin.system.project%3Achangelog-panel) for detailed information on changes.

###MAVEN USERS

All major releases of this library are available in the central Maven repository.
The following components are available:

* spring-ldap-core - the core Spring LDAP library
* spring-ldap-tiger - the Spring LDAP Java 5 support library
* spring-ldap-test - support classes that helps LDAP with integration testing
* spring-ldap-ldif-core - the Spring LDAP LDIF parsing library
* spring-ldap-ldif-batch - the Spring Batch integration layer for the LDIF parsing library
* spring-ldap-odm - The Object-Directory Mapping (ODM) framework

To include e.g. the spring-ldap-core component in your project, use the following dependency tag:

    <dependency>
      <groupId>org.springframework.ldap</groupId>
      <artifactId>spring-ldap-core</artifactId>
      <version>1.3.1.RELEASE</version>
    </dependency>

Milestone releases (such as release candidates) are available from the Spring
framework milestone repo:

    <repository>
      <id>spring-milestone</id>
      <name>Spring Portfolio Milestone Repository</name>
      <url>http://maven.springframework.org/milestone</url>
    </repository>

Snapshot builds produced by the CI builds are available from the Spring framework snapshot repo:

    <repository>
      <id>spring-milestone</id>
      <name>Spring Portfolio Milestone Repository</name>
      <url>http://maven.springframework.org/snapshot</url>
    </repository>

In order to e.g. try out the latest build snapshot of the core module, include the repository above and
use the following dependency tag:

    <dependency>
      <groupId>org.springframework.ldap</groupId>
      <artifactId>spring-ldap-core</artifactId>
      <version>1.3.2.CI-SNAPSHOT</version>
    </dependency>

Note that while all milestone and snapshot builds have passed the (quite extensive) test suite,
the artifacts here are obviously still work in progress. Feel free to use them for trying out new functionality
and bug fixes for an upcoming version. Please report any problems or bugs in the [issue tracker](https://jira.springsource.org/browse/LDAP).

###ADDITIONAL RESOURCES

* [Official site](http://www.springframework.org/ldap)
* [Support forum](http://forum.springframework.org/forumdisplay.php?f=40)
* [Issue tracker](https://jira.springsource.org/browse/LDAP)
