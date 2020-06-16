# ClipboardIndexTool
划词索引工具    A Simple Tool For Indexing By CTRL+C 

### 项目说明

这是一个基于监控当前系统剪切板的内容索引工具，你可以复制一些关键词，然后通过该程序将关该键词对应的内容查找出来。
项目基于maven进行构建，目前仍处于初期开发阶段，如果你有好的意见，请提交你的Pull Request。

### 使用说明 beta 0.1版本 (ps:需要有java以及mysql操作基础）

1.你需要拥有一个mysql数据库，并创建一个内含两个属性的表（一个属性为问题，另一个属性为该问题对应的索引结果）

2.向该表中录入你需要的数据，并将连接信息输入到  src/main/resources/mybatis-config.xml 中

3.修改并根据自己的需要决定是否重写 /src/main/resources/mapper/ExamMapper.xml 

4.运行Code.java（命令行运行或IDE内运行）

5.程序在运行时会监控您的剪切板，当内容发生变化时会自动获取当前剪切板的内容进行索引，并将索引结果以弹窗的方式展示出来，弹窗的样式可在 /src/main/java/util/util2/WindowTip.java 中自由修改，需要有Java Swing的基础知识

6.bug反馈：

提交Issues或fork本仓库进行修改后PL

* 建议 *

若鼠标支持鼠标宏，可将ctrl+c快捷键绑定到侧键位，提高效率


### 结构说明

src/main/java/util目录下有一个util2文件夹，里面的内容和util中的内容有些许不同

（util2为目前的Code主函数服务，util为正在开发中的GUI界面服务）

### 开发进度

Code.java可正常启动运行，使用前需部署对应mysql服务器，数据库框架使用mybatis

GUI.java也可正常启动，使用方式和Code.java大同小异，但目前无法实现类似Code.java的弹窗提醒形式，暂时不可用


**项目组件参考：**
[1.剪切板操作功能 ](https://blog.csdn.net/xietansheng/article/details/70478266 "1.剪切板操作功能 ")
