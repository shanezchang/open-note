# Java Note

# BackendServer Doc

## 1. 本地打包 `jar` 包

```
NACOS_HOST=172.26.37.219:8848;NAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b

```



## 2. 发送 `jar` 包到云服务器

```shell
scp ./target/object-storage-center-0.0.1-SNAPSHOT.jar root@120.24.6.195:/root/object-storage-center

Ks.210905

lsof -i:9998

kill ${PID}


```

## 3. 环境变量 `java`

`source /etc/environment`

## 4. 执行

```bash
nohup java -Xmx1024m -DNACOS_HOST=172.26.37.219:8848 -DNAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b -jar object-storage-center-0.0.1-SNAPSHOT.jar > /dev/null 2>&1 &

java -Xmx1024m -DNACOS_HOST=172.26.37.219:8848 -DNAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b -jar gateway-center-0.0.1-SNAPSHOT.jar

nohup java -Xmx1024m -DNACOS_HOST=172.26.37.219:8848 -DNAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b -jar gateway-center-0.0.1-SNAPSHOT.jar > /dev/null 2>&1 &




java -Xmx1024m -DNACOS_HOST="172.26.37.219:8848" -DNAME_SPACE="02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b" -jar object-storage-center-0.0.1-SNAPSHOT.jar


nohup java -Xmx1024m -DNACOS_HOST="172.26.37.219:8848" -DNAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b -jar object-storage-center-0.0.1-SNAPSHOT.jar &


```









---







# java

## install java on linux

```bash
sudo mkdir /usr/local/java

sudo tar -zxf /path/to/java.tar.gz -C /usr/local/java
sudo nano /etc/environment
PATH="/usr/local/java/jdk/bin:$PATH"
JAVA_HOME="/usr/local/java/jdk"
source /etc/environment


export JAVA_HOME=/usr/local/java/jdk-21.0.3
export PATH=$JAVA_HOME/bin:$PATH

/usr/local/java/jdk/bin/java

java -version
javac -version


java -Xmx1024m -DMYSQL_HOST=172.26.23.176 -DMYSQL_USERNAME=root -DMYSQL_PASSWORD=51XWf3FBGs2XVqig -DMACHINE_HOST=172.26.23.176 -jar object-storage-center-0.0.1-SNAPSHOT.jar


java -Xmx1024m -DNACOS_HOST=172.26.23.176:8848 -jar object-storage-center-0.0.1-SNAPSHOT.jar


nohup java -Xmx1024m -DNACOS_HOST=172.26.23.176:8848 -jar object-storage-center-0.0.1-SNAPSHOT.jar > /dev/null 2>&1 &


nohup java -Xmx1024m -DNACOS_HOST=172.26.37.219:8848 -DNAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b -jar object-storage-center-0.0.1-SNAPSHOT.jar > /dev/null 2>&1 &


NACOS_HOST=172.26.37.219:8848;NAME_SPACE=02f79b1d-b0d1-4fe5-b341-27bd5b5ab20b

MYSQL_HOST=172.26.37.219;MYSQL_USERNAME=root;MYSQL_PASSWORD=51XWf3FBGs2XVqig;SERVICE_MACHINE_HOST=120.24.6.195

MAIL_USERNAME=garvinzhang@foxmail.com;MAIL_PASSWORD=cctdqyvmoecvbhbg

MYSQL_HOST=172.26.37.219;MYSQL_USERNAME=root;MYSQL_PASSWORD=51XWf3FBGs2XVqig;SERVICE_MACHINE_HOST=120.24.6.195
```



## maven 配置阿里源

```xml
<settings>
  <!-- 其他设置 -->
  <mirrors>
    <!-- 阿里云Maven仓库 -->
    <mirror>
      <id>alimaven</id>
      <mirrorOf>central</mirrorOf>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
    </mirror>
    <!-- 其他镜像 -->
  </mirrors>
  <!-- 其他设置 -->
</settings>

```



## maven打包部署程序

```shell
# IDE 配置
File -> Project Structure -> Artifacts -> + Jar From modules -> ...
delete test files, maven clean, maven install

# 修改端口号为9998
scp ./target/thirdHouseAdaptServer-1.0.jar Garvin@120.26.240.186:/home/Garvin/thirdHouseAdaptServer-1.9.jar

AJMzl3xt5&C0l3II

scp ./thirdHouseAdaptServer-2.1.jar root@172.19.153.155:/root/de-wms/

lsof -i:9991

kill ${PID}

vim /etc/nginx/conf.d/fat-wms-gps.cht-group.net.conf

java -Xmx1024m -DNACOS_HOST=mse-8bfaa4d0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=d2301169-62ae-4e37-9972-d564c7f7ae9f -DNACOS_USERNAME=nacos -DNACOS_PASSWORD=nacos -jar thirdHouseAdaptServer-1.5.jar

nohup java -Xmx1024m -DNACOS_HOST=mse-8bfaa4d0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=d2301169-62ae-4e37-9972-d564c7f7ae9f -DNACOS_USERNAME=nacos -DNACOS_PASSWORD=nacos -jar thirdHouseAdaptServer-1.0.jar > /dev/null 2>&1 &

java -Xmx1024m -DNACOS_HOST=mse-8bfaa4d0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=d2301169-62ae-4e37-9972-d564c7f7ae9f -DNACOS_USERNAME=nacos -DNACOS_PASSWORD=nacos -jar thirdHouseAdaptServer-1.0.jar

java -Xmx1024m -DNACOS_HOST=mse-8bfaa4d0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=d2301169-62ae-4e37-9972-d564c7f7ae9f -DNACOS_USERNAME=nacos -DNACOS_PASSWORD=nacos -jar thirdHouseAdaptServer-1.0-20240924.jar

java -Xmx1024m -DNACOS_HOST=mse-8bfaa4d0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=d2301169-62ae-4e37-9972-d564c7f7ae9f -DNACOS_USERNAME=nacos -DNACOS_PASSWORD=nacos -jar thirdHouseAdaptServer-1.0-20240924-bac.jar


java -Xmx1024m -DNACOS_HOST=mse-29f0b9a0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=DEFAULT_GROUP -DNAME_SPACE=test -DNACOS_USERNAME=nacos -DNACOS_PASSWORD='ytgroup1234!@#$' -jar thirdHouseAdaptServer-1.0-20240909-bac.jar


java -Xmx1024m -DNACOS_HOST=mse-29f0b9a0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=java -DNAME_SPACE=test -DNACOS_USERNAME=nacos -DNACOS_PASSWORD='ytgroup1234!@#$' -jar thirdHouseAdaptServer-1.0-20240909-bac.jar


java -Xmx1024m -DNACOS_HOST=mse-29f0b9a0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=java -DNAME_SPACE=test -DNACOS_USERNAME=nacos -DNACOS_PASSWORD='ytgroup1234!@#$' -jar thirdHouseAdaptServer-1.0-20240924-bac.jar


nohup java -Xmx1024m -DNACOS_HOST=mse-29f0b9a0-nacos-ans.mse.aliyuncs.com:8848 -DNACOS_GROUP=java -DNAME_SPACE=test -DNACOS_USERNAME=nacos -DNACOS_PASSWORD='ytgroup1234!@#$' -jar thirdHouseAdaptServer-1.0-20240924-bac.jar > /dev/null 2>&1 &


curl http://localhost:9991/health


# 验证部署成功
https://fat-wms-gps.cht-group.net/health


# 环境变量配置
MYSQL_HOST=rm-bp1bcncxz746vi4fc8o.mysql.rds.aliyuncs.com;MYSQL_PASSWORD=Yt_wms_fat20230812+;MYSQL_USERNAME=yt_wms_fat;OSS_AK=xxx;OSS_AS=xxxx;OSS_BUCKET=yt-wms;OSS_ENDPOINT=https://oss-cn-beijing.aliyuncs.com;OSS_HOST=https://yt-wms.oss-cn-beijing.aliyuncs.com;S3_AK=1;S3_AS=1;S3_ENDPOINT=1;REDIS_PASSWORD=
```



# Java Stream Note

常用的 java stream 用法;

```java
// basic usage
Set<Object> objectSet =  objectList.stream().map(ObjectClass::getObject).collect(Collectors.toSet())

Map<Integer, List<String>> m = detailEntities.stream()
    .collect(Collectors.groupingBy(
    ReturnSkuDetailEntity::getLocationId,
    Collectors.mapping(ReturnSkuDetailEntity::getSnCode, Collectors.toList())
));

// 分组计数之和
Map<Integer, Integer> resultMap = detailEntities.stream()
    .collect(Collectors.groupingBy(ReturnSkuDetailEntity::locationId,
    Collectors.summingInt(e -> 1)));

// 去重分组计数之和
Map<Integer, Integer> resultMap = detailEntities.stream()
    .collect(Collectors.groupingBy(ReturnSkuDetailEntity::locationId,
    Collectors.mapping(ReturnSkuDetailEntity::snCode, Collectors.collectingAndThen(
    Collectors.toSet(), Set::size))));

// 分组获得List
snCodeMap = detailEntities.stream().collect(Collectors.groupingBy(ReturnSkuDetailEntity::getLocationId,
    Collectors.mapping(ReturnSkuDetailEntity::getSnCode, Collectors.toList())));

```

# Spring Transactional

Spring 事务 (Transactional) 的传播 (Propagation) 行为: 

- **REQUIRED** (default): 如果当前存在事务，则加入该事务；如果没有事务，则新建一个事务
- **SUPPORTS**: 如果存在事务，则加入此事务；如果当前无事务，则以非事务的方式继续运行
- **MANDATORY**: 如果当前存在事务，则加入；如果当前没有事务，则抛出异常
- **REQUIRES_NEW**: 创建一个新的事务，如果当前存在事务，则把当前事务挂起
- **NOT_SUPPORTED**: 以非事务方式运行，如果当前存在事务，则把当前事务挂起
- **NEVER**: 以非事务方式运行，如果当前存在事务，则抛出异常
- **NESTED**: 如果当前存在事务，则创建一个新事务作为当前事务的嵌套事务运行；如果当前没有事务，则新建一个正常事务

```java
@Transactional(rollbackFor = Exception.class, propagation = Propagation.NOT_SUPPORTED)
```

