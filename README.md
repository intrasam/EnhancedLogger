# EnhancedLogger
To use my Logger just add this in your pom

```xml
<build>
<plugins>
<!-- AspectJ Weaver plugin -->
<plugin>
<groupId>org.codehaus.mojo</groupId>
<artifactId>aspectj-maven-plugin</artifactId>
<version>1.14.0</version>
<configuration>
<complianceLevel>16</complianceLevel>
<source>16</source>
<target>16</target>
<Xlint>ignore</Xlint>
<showWeaveInfo>true</showWeaveInfo>
<verbose>true</verbose>
<aspectLibraries>
<aspectLibrary>
<groupId>com.github.intrasam</groupId>
<artifactId>Logger</artifactId>
</aspectLibrary>
</aspectLibraries>
</configuration>
<executions>
<execution>
<goals>
<goal>compile</goal>
<goal>test-compile</goal>
</goals>
</execution>
</executions>
</plugin>
</plugins>
</build>
```
and then as a dependency:
````xml
<dependency>
    <groupId>com.github.intrasam</groupId>
    <artifactId>EnhancedLogger</artifactId>
    <version>1.0</version>
</dependency>
````
DON'T FORGET TO USE JITPACK!!!
````xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
````