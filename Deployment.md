> As **http://builds.archive.org** is not accessible from China, I have to upload heritrix artifacts and its dependencies to qiuniu cloud storage space

## Prepare local repository

* Create a directory named **mvnrepository**
* Download dependencies to **mvnrepository** following the maven repository layout
* Deploy to **mavenrepository** using the command below

```shell
mvn clean deploy -DskipTests=true -Drepository.url=file://{path_to_mvnrepository}
```

## Upload artifacts and dependencies to qiniu

Read the docs [here](http://developer.qiniu.com/docs/v6/tools/qrsync.html) to sync **mvnrepository** to qiniu storage space.
