parent-pom [![Build Status](https://travis-ci.org/caarlos0/parent-pom.svg?branch=master)](https://travis-ci.org/caarlos0/parent-pom) [![Stories in Ready](https://badge.waffle.io/caarlos0/parent-pom.png?label=ready&title=Ready)](https://waffle.io/caarlos0/parent-pom)  [![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.carlosbecker/parent-pom/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/com.carlosbecker/parent-pom)
==========

Just a parent pom project that I use in some projects.

## Quality Assurance

Use the `qulice` profile:

```sh
mvn clean install -Pqulice
```

## Add/Update license headers:

Use the `header` profile:

```sh
mvn clean install -Pheader
```

## Send data to Coveralls

Use the `CI` profile:

```sh
mvn clean install -PCI
```

Don't forget to set the `coveralls.token` property.

## Run mutation tests

Use the `mutation` profile:

```sh
mvn clean install -Pmutation
```

You might want to adjust the `mutation.minimum` property.

## Add coverage check to build

This will break the build if the coverage is less than 70%
(configurable via `jacoco.minimum` property):

```xml
<build>
  <plugins>
    <plugin>
      <groupId>org.jacoco</groupId>
      <artifactId>jacoco-maven-plugin</artifactId>
    </plugin>
  </plugins>
</build>
```
