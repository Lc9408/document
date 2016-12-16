# 二、搭建season开发环境,熟悉spring boot

#### 参照[文档](http://test.haier.com/doc/season/base/hello-world.html) 搭建season开发环境

## 学习周期：

*  一天

## 完成条件：

*  能正常启动自己的项目，并能访问自己的controller

* 了解spring boot的基本知识
## Hello World

### 1.1 创建项目

推荐使用Intellij Idea15进行开发，直接官网下载最新版。 Intellij idea的开源版是免费的，收费版功能插件多些。如果支持正版可以选择购买正版，免费版也能完全满足我们的开发需求。 可以为自己的工具更换下主题，获取主题地址：http://www.riaway.com，所有安装都默认就行。
###完整结构图：

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-496bb1b065b2d3b1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* #### 新建maven工程

       jdk选择1.7及以上

     GroupId必须填写为trs.com.cn

    ArtifactId填写为你的应用名称，版本号默认即可。
### 1.2 配置pom.xml

* 添加打包格式

		<packaging>war</packaging>
        // war或jar都可以

* 添加season的支持
```xml
      <parent>
       <artifactId>season-parent</artifactId>
       <groupId>trs.com.cn</groupId>
       <version>1.2</version>
    </parent>
```
* 添加season-core的依赖
```xml
      <dependency>
        <groupId>trs.com.cn</groupId>
        <artifactId>season-core</artifactId>
    </dependency>
```
不用添加版本，在season-parent中已指定，最新版本可到maven仓库查看。
* 添加海尔maven仓库地址
```xml
    <repository>
        <id>haier-maven-repository</id>
        <url>http://test.haier.com/nexus/content/groups/public/</url>
    </repository>
  ```
* 添加打包插件
```xml
    <plugin>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
    </plugin>
```
在IntelliJ IDEA中新建一个`groupId`为**trs.com.cn**，`artifactId`为**season_test** , `version`为**14-SNAPSHOT** 的Maven工程`SeasonTest` , 然后如下所示为其配置`pom.xml`文件：
``` xml
    <?xml version="1.0" encoding="UTF-8"?>
    <project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
        <modelVersion>4.0.0</modelVersion>

        <groupId>trs.com.cn</groupId>
        <artifactId>season-test</artifactId>
        <version>1.0-SNAPSHOT</version>

        <packaging>war</packaging>

        <parent>
            <artifactId>season-parent</artifactId>
            <groupId>trs.com.cn</groupId>
            <version>1.2</version>
        </parent>

        <dependencies>
            <dependency>
                <groupId>trs.com.cn</groupId>
                <artifactId>season-core</artifactId>
            </dependency>
        </dependencies>

        <build>
            <finalName>SeasonTest</finalName>
            <plugins>
                <plugin>
                    <groupId>org.springframework.boot</groupId>
                    <artifactId>spring-boot-maven-plugin</artifactId>
                </plugin>
            </plugins>
        </build>

        <repositories>
            <repository>
                <id>haier-maven-repository</id>
                <url>http://test.haier.com/nexus/content/groups/public/</url>
            </repository>
        </repositories>

    </project>
```
### 1.3 创建启动类

在`SeasonTest`工程的`src/main/java`下创建一个包`com.trs.config`，然后新建一个继承自`com.season.core.spring.SeasonApplication`的类并为其添加如下主方法：
```java
    public static void main(String[] args){
        SeasonRunner.run(App.class);
    }
```
 

App为你的类。

启动main方法，即可启动应用。当然现在什么功能也没有，只是启动了应用，应用默认的容器是Tomcat8。

### 1.4 创建Controller

在`src/main/java`下再创建一个包`com.trs.Controller`，然后新建一个继承自`com.season.core.controller`的类并为其添加`@ControllerKey`注解：
```java
    @ControllerKey("hello")
    public class HelloController extends Controller{
        public void season(){
            renderText("hi season!");
        }
    }
```
运行`main()`方法，IDEA的Run窗口出现下面的代码即为运行成功(***此处注意程序运行一次后需杀掉运行进程然后再再次运行，否则就会抛出tomcat启动的异常，异常是因为启动中的port被占用所造成的***)：

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3946479-464661812e944019.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)