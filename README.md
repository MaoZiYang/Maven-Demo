# 欢迎来到Maven项目训练
------
![Maven-logo](https://github.com/MaoZiYang/Maven-Demo/blob/master/src/main/image/Mavenlogo.png)
### [Apache Maven官网](https://maven.apache.org/)
## 一、为什么使用Maven这样的构建工具【why】
### ① 一个项目就是一个工程
    如果项目非常庞大，就不适合使用package来划分模块，最好是每一个模块对应一个工程，利于分工协作。
    借助于maven就可以将一个项目拆分成多个工程
### ② 项目中使用jar包，需要“复制”、“粘贴”项目的lib中
    同样的jar包重复的出现在不同的项目工程中，你需要做不停的复制粘贴的重复工作。
    借助于maven，可以将jar包保存在“仓库”中，不管在哪个项目只要使用引用即可就行。
### ③ jar包需要的时候每次都要自己准备好或到官网下载
　　借助于maven我们可以使用统一的规范方式下载jar包，规范
### ④ jar包版本不一致的风险
　　不同的项目在使用jar包的时候，有可能会导致各个项目的jar包版本不一致，导致未执行错误。
　　借助于maven，所有的jar包都放在“仓库”中，所有的项目都使用仓库的一份jar包。
### ⑤ 一个jar包依赖其他的jar包需要自己手动的加入到项目中
　　FileUpload组件->IO组件，commons-fileupload-1.3.jar依赖于commons-io-2.0.1.jar
　　极大的浪费了我们导入包的时间成本，也极大的增加了学习成本。
　　借助于maven，它会自动的将依赖的jar包导入进来。
 ## 二、maven是什么【what】
### ① maven是一款服务于java平台的自动化构建工具
　　make->Ant->Maven->Gradle
　　名字叫法：我们可以叫妹文也可以叫麦文，但是没有叫妈文的。
### ② 构建
　　构建定义：把动态的Web工程经过编译得到的编译结果部署到服务器上的整个过程。
　　√ 编译：java源文件[.java]->编译->Classz字节码文件[.class]
　　√ 部署：最终在sevlet容器中部署的不是动态web工程，而是编译后的文件
  ![WEB-Design](https://github.com/MaoZiYang/Maven-Demo/blob/master/src/main/image/WEB-Design.png)
  ### ③ 构建的各个环节
  
   　[1] 清理clean：将以前编译得到的旧文件class字节码文件删除

　　[2] 编译compile：将java源程序编译成class字节码文件

　　[3] 测试test：自动测试，自动调用junit程序

　　[4] 报告report：测试程序执行的结果

　　[5] 打包package：动态Web工程打War包，java工程打jar包

　　[6] 安装install：Maven特定的概念-----将打包得到的文件复制到“仓库”中的指定位置

　　[7] 部署deploy：将动态Web工程生成的war包复制到Servlet容器下，使其可以运行
  
 ## 三、安装maven
### ① 当前系统是否配置JAVA_HOME的环境变量

### ② 下载maven，解压maven放在一个非中文无空格的路径下

### ③ 配置maven的相关环境变量
  
### ④ 验证：maven -v 查看maven版本
   ![mvn-version](https://github.com/MaoZiYang/Maven-Demo/blob/master/src/main/image/mvn-version.png)
   
