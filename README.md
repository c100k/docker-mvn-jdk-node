# Docker Maven JDK Node

Maven, JDK and Node to build projects.

## See components versions

```shell
docker run chafik/mvn-jdk-node
```

## Test Maven project

If you want to avoid downloading all the internet every time you launch a build,
you can mount your local `.m2` folder.

```shell
docker run \
    -v /Users/chafik/.m2:/root/.m2 \
    -v $PWD:/home/app \
    chafik/mvn-jdk-node \
    mvn -f /home/app/pom.xml -B clean test verify
```
