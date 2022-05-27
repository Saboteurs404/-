# 关于Spring开发部署全过程进行记录：
   Jakarta Commons Logging(JCL)提供了一个日志（Log）接口（interface）,同时兼顾轻量级和不依赖具体的日志实现。
     它提供了给中间件/日志工具开发者一个简单的日志操作抽象，允许程序开发人员使用不同的具体日志实现工具。
     用户被假定已熟悉某种日志实现工具的更高级别的细节，JCL提供的接口，对其他一些日志工具，包括Log4j,Avalon LogKit,and JDK 1.4等，
     进行了简单的包装，此接口更接近与Log4j和LogKit的实现
     
 
## 1、下载jdk1.8.0_152 并配置环境，将bin目录加到PATH中。
jre是Java的运行环境，也就是说如果你只装了jre那么你的电脑只能运行Java程序而无法编译Java程序
jre式运行Java程序必备的环境的集合，包含JVM标准实现及java核心类库，它包含Java虚拟机、Java平台核心类支持文件。他不包括开发工具（编译器、调试器）
JDK(java Development kit)又称J2sdk,是Java开发包。它提供了Java的开发环境（提供了编译器javac等工具，用于将java文件编译为class文件）和运行环境（提供了JVM和Runtime辅助包）
用于解析class文件使其得到运行）
如果你下载了jdk，那么你不仅可以开发java程序，也同时拥有了运行Java程序的平台。jdk是整个Java的核心，包括java运行环境（jre）
## 2、
