
# 1 简介
springboot在建立生产中的独立程序上非常简便、只需要一些简便的配置就能运行起来。大致
有如下特点：<br>
1.创建独立的Spring applications
2.能够使用内嵌的Tomcat，Jetty or Undertow，不需要部署war
3.提供starter pom来简化maven配置
4.自动配置spring
5.提供一些生产环境的特性，比如metrics，health checks and externalized configuration
6.绝对没有代码生产和xml配置要求
# 2 快速开始
``` 
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>1.4.1.RELEASE</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>springboot-1</artifactId>


    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <version>1.4.1.RELEASE</version>
            </plugin>
        </plugins>
    </build>
</project>
```
这块统一用spring-boot-starter-parent做为parent，所以spring-boot-starter-web不用填写版本号。<br>
``` 
<parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>1.4.1.RELEASE</version>
 </parent>
```
下面这个插件是用来运行springboot的，通常有两种方式可以运行springBoot，一种是通过直接
运行main方法，另外一种是通过使用下面的插件运行。<br>
