# Parent POM for Scala

## Features

### Plugins

1. [scalatest-maven-plugin](https://github.com/scalatest/scalatest-maven-plugin)
`-Dmaven.test.skip=true` 에 반응하지 않는 문제 때문에, `scalatest` 라는 profile 을 사용함
   - `-DskipTests` 옵션을 쓰면 되긴 함
   - https://github.com/scalatest/scalatest/issues/466
    
1. [scoverage-maven-plugin](https://github.com/scoverage/scoverage-maven-plugin) 
    ```
    $ cd path/to/repo
    $ mvn clean package -Dmaven.test.skip=true (or -DskipTests)
    $ mvn scoverage:report sonar:sonar
    ```
- https://github.com/scoverage/scoverage-maven-samples/issues/2