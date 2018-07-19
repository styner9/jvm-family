# Parent POM for JVM Languages
Personal preferences for maven project

## Modules
- [java](./java)
- [kotlin](./kotlin)
- ~~[scala](./scala)~~

## Usage
```xml
<parent>
    <groupId>com.github.styner9</groupId>
    <artifactId>jvm-family-{module:java|kotlin}</artifactId>
    <version>{VERSION}</version>
</parent>

<repositories>
    <repository>
        <id>bintray-styner9-utils</id>
        <url>https://dl.bintray.com/styner9/utils</url>
    </repository>
</repositories>
```

## Features

### Plugins
1. [gitflow-maven-plugin](https://github.com/aleksandr-m/gitflow-maven-plugin)
    ```
    $ mvn gitflow:feature-start
    $ mvn gitflow:feature-finish
    ```
1. [git-commit-id-plugin](https://github.com/ktoso/maven-git-commit-id-plugin) (+ maven-jar/war-plugin)
    - [Use Cases](https://github.com/ktoso/maven-git-commit-id-plugin#use-cases)
    - Stamps git properties to  `META-INF/MANIFEST.MF`
        ```
        $ unzip -p path/to/your.jar META-INF/MANIFEST.MF
        ```
1. [versions-maven-plugin](https://www.mojohaus.org/versions-maven-plugin/)
    ```
    $ mvn versions:display-property-updates
    [INFO] The following version properties are referencing the newest available version:
    [INFO]   ${git-commit-id-plugin.version} ............................... 2.2.3
    [INFO]   ${maven-jar-plugin.version} ................................... 3.0.2
    ...
    ```