# IntelliJ IDEA 2016

## 1.系统设置

### 1.1 jvmoptions

修改idea.exe.vmoptions

```
-server
-Xms512m
-Xmx2048m
-XX:ReservedCodeCacheSize=240m
-XX:+UseCompressedOops
-XX:MaxPermSize=128m
-XX:NewRatio=4
-Xss128k
-Dsun.awt.keepWorkingSetOnMinimize=true
```

> -Xms 初始内存，增加该值可以提高Java程序的启动速度。  
> -Xmx 最大内存数，提高该值，可以减少内存Garage收集的频率，提高程序性能。  
> -Dsun.awt.keepWorkingSetOnMinimize=true 可以让IDEA最小化到任务栏时依然保持以占有的内存，当你重新回到IDEA，能够被快速显示，而不是由灰白的界面逐渐显现整个界面，加快回复到原界面的速度。  
> -server 控制内存garage方式，这样你无需在花一到两分钟等待内存garage的收集。  


### 1.2 Appearance & Behavior

#### 1.2.1 Appearance

1. 设置黑色主题  
  Theme -> Darcula

2. 设置字体  
  勾选“Override defult fonts by (no recommended)”  
  字体可以选“微软雅黑”

3. 设置显示内存使用情况  
  勾选“Show memory indicator”

#### 1.2.2 System Settings

1. 设置启动的时候不打开工程文件  
  去掉勾选 “Reopen last project on startup”

##### 1.2.2.1 Updates

1. 关闭自动更新  
  去掉勾选“Automatically check updates”


### 1.3 Keymap

1. 修改快捷键  
  如果是Eclipse转过来，可以选择Eclipse。


### 1.4 Editor

#### 1.4.1 General

1. 设置光标位于行后  
  去掉勾选“Allow placement of caret after end of line”

##### 1.4.1.1 Auto Import

1. 自动优化导入的包  
  勾选“Optimize imports on the fly”

2. 自动导入需要用到的包  
  勾选“Add unambiguous imports on the fly”

##### 1.4.1.2 Appearance

1. 设置显示代码行号  
  勾选“Show line numbers”

2. 设置显示方法线  
  勾选“Show method separators”

3. 设置显示空白字符  
  勾选“Show whitespaces”

##### 1.4.1.3 Code Completion

1. 设置代码提示不区分大小写  
  Case Sensitive completion -> None

##### 1.4.1.4 Editor Tabs

1. 设置Tab显示多行  
  去掉勾选“Show tabs in single row”

2. 设置Tab显示个数  
  Tab limit -> 16  

3. 标记未保存的文件  
  勾选“Mark modified tabs with asterisk”

#### 1.4.2 Colors & Fonts

##### 1.4.2.1 Font

1. 设置代码的字体  
  勾选“Show only monospaced fonts”，选择字体

##### 1.4.2.2 Console Font

1. 设置控制台的字体  
  勾选“Show only monospaced fonts”，选择字体

##### 1.4.2.3 General

1. 设置选中变量高亮显示  
  Identifier under caret 设置foreground和Background

#### 1.4.3 Code Style

##### 1.4.3.1 Java

1. 设置Tab和缩进  
  Tabs and Indents，根据需要设置

2. 设置导入包时不使用*来匹配  
  Imports  
    Names Count to use static import with '*' -> 99

3. 设置代码单行注释不在行最开头处，而是紧跟代码
  Code Generation  
    去掉勾选“Line comment at first column”

#### 1.4.4 Inspections

##### 1.4.4.1 Java

1. serialVersionUID的验证  
  Serialization issues->Serializable class without 'serialVersionUID' 勾选

2. 不验证声明访问权限  
  Declaration redundancy -> Declaration access can be weaker 去掉勾选

3. 忽略未使用的声明  
  Declaration redundancy -> Unused declaration 去掉勾选

##### 1.4.4.2 Maven

1. 忽略提示冗余GroupId  
  Redundant groupId 去掉勾选

##### 1.4.4.3 Spelling

1. 忽略拼写错误
  Typo 去掉勾选

#### 1.4.5 File and Code Templates

1. Java文件  
  Includes->File Header

```
/**
 * Created on ${YEAR}-${MONTH}-${DAY} ${HOUR}:${MINUTE}
 * @author ${USER}
 * @version 1.0
 */
```

#### 1.4.6 File Encodings

1. 设置编写国际化资源文件时，自动为中文转码  
  勾选“Transparent native-to-ascii conversion”


### 1.5 Version Control

根据实际需要设置版本管理工具，如：SVN、Git。


### 1.6 Build,Execution,Deployment

#### 1.6.1 Build Tools

添加构建工具，如：Maven、Gradle。

#### 1.6.2 Application Servers

添加应用服务器，如：tomcat。

