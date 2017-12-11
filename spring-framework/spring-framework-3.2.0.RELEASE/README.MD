### 基于eclipse的Spring-framework-3.2.0项目源码
### 基于gradle 1.6进行构建
### 基于jdk1.8

gradle构建出错：<br/>
1、如果在执行一段时间后，抛出一个错误。<br/>
Could not find com.itextpdf:itextpdf:4.2.2. Required by: <br/>
org.springframework:spring-context-support:3.2.4.RELEASE > com.lowagie:ite xt:4.2.2 <br/>
这个是因为3.2.0版本比较老。一些jar发生了变化。解决办法。就是打开gradle的仓库下的。 <br/>
C:\Users\Administrator.gradle\caches\artifacts-24\module-metadata\com.lowagie\itext\下有两个版本2.1.7、4.2.2，它们各有一个个ivy.xml <br/>
找到4.2.2下面的ivy.xml。<br/>
将 <br/>
dependency org=”com.itextpdf” name=”itextpdf” rev=”4.2.2” <br/>
修改为 <br/>
dependency org=”com.itextpdf” name=”itextpdf” rev=”5.2.0”<br/>
