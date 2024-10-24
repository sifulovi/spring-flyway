# Flyway Spring boot POC

Tools:
1. JAVA 21
2. Spring boot 3
3. flyway
4. PostGRES DB



To run the mvn script for flyway add following under plugins section in **pom.xml**

```

<plugin>
    <groupId>org.flywaydb</groupId>
    <artifactId>flyway-maven-plugin</artifactId>
    <configuration>
        <url>jdbc:postgresql://localhost:5432/flyway</url>
        <user>postgres</user>
        <password>postgres</password>
    </configuration>
</plugin>

```

in **application.properties** add following


```
spring.flyway.enabled=true
spring.flyway.locations=classpath:db/migration
spring.flyway.validate-on-migrate=true
```