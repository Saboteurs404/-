# 关于Spring开发部署全过程进行记录：
## 1、下载jdk1.8.0_152 并配置环境，将bin目录加到PATH中。
jre是Java的运行环境，也就是说如果你只装了jre那么你的电脑只能运行Java程序而无法编译Java程序
jre式运行Java程序必备的环境的集合，包含JVM标准实现及java核心类库，它包含Java虚拟机、Java平台核心类支持文件。他不包括开发工具（编译器、调试器）
JDK(java Development kit)又称J2sdk,是Java开发包。它提供了Java的开发环境（提供了编译器javac等工具，用于将java文件编译为class文件）和运行环境（提供了JVM和Runtime辅助包）
用于解析class文件使其得到运行）
如果你下载了jdk，那么你不仅可以开发java程序，也同时拥有了运行Java程序的平台。jdk是整个Java的核心，包括java运行环境（jre）
## 2、安装Apache commons Logging API
     jakarta Commons Logging(JCL)提供了一个日志（Log）接口（interface）,同时兼顾轻量级和不依赖具体的日志实现。
     它提供了给中间件/日志工具开发者一个简单的日志操作抽象，允许程序开发人员使用不同的具体日志实现工具。
     用户被假定已熟悉某种日志实现工具的更高级别的细节，JCL提供的接口，对其他一些日志工具，包括Log4j,Avalon LogKit,and JDK 1.4等，进行了简单的包装，此接口更接近与Log4j和LogKit的实现
从 http://commons.apache.org/logging/ 下载 Apache Commons Logging API 的最新版本。
![20220527180919](https://user-images.githubusercontent.com/65841055/170679437-e9da5a58-fe89-4a14-be45-b86b8466b167.png)
## 3、IDEA安装
## 4、Tomact的安装与配置
Tomcat官网：https://tomcat.apache.org/index.html

从Tomcat的官方文档可以看到，Tomcat 10有一个大的变动：jar包从 javax.* 变成了 jakarta.*，这就要求从Tomcat 9 等 迁移到Tomcat 10的时候，要么做一些代码改动，要么借助Tomcat官网提供的迁移工具将编译好的war变更成用jakarta的。

![20220530150004](https://user-images.githubusercontent.com/65841055/170935245-5d299784-b4c4-430b-b6b9-fd724cdb15ec.png)
![20220530150144](https://user-images.githubusercontent.com/65841055/170935367-599d9419-2e43-4fb7-92e4-0120340be1b2.png)
  如果出现乱码需要修改Tomcat目录下的conf文件夹中的logging.properties文件，找到对应的出现乱码的位置，将utf-8修改成GBK
## 5、MAVEN(建议不要装在C盘，否者加载仓库文件时，可能因为权限问题无法写入)
MAVEN官网：https://maven.apache.org/download.cgi

下载好后在path中配置到bin目录，使用mvn -v检查是否安装成功
### 配置MAVEN本地仓库
 1. 在D:\Program Files\Apache\目录下新建maven-repository文件夹，该目录用作maven的本地库。

 2. 打开D:\Program Files\Apache\maven\conf\settings.xml文件，查找下面这行代码：
  ```
  <localRepository>/path/to/local/repo</localRepository>
  ```
 3、localRepository节点默认是被注释掉的，需要把它移到注释之外，然后将localRepository节点的值改为我们在3.1中创建的目录D:\Program Files\Apache\maven-repository。
 当我们从maven中获得jar包的时候，maven首先会在本地仓库中查找，如果本地仓库有则返回；如果没有则从远程仓库中获取包，并在本地库中保存。
 此外，我们在maven项目中运行mvn install,项目将会自动打包并安装到本地仓库中
 ### 配置IDEA的maven环境


## 6、mysql数据库安装与部署
在通过mysql压缩包来安装时，经过多次尝试最终都无法修改密码。所以最后选择通过.exe文件进行安装。运行正常，不用进行额外的配置
## 7、navicat安装
navicat是一套可创建多个连接的数据库管理工具
安装的是navicat15  安装包放在了百度网盘里
