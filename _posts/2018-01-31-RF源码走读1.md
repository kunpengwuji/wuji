---
published: true
date: 2018-01-31T10:44:21.000Z
categories:
  - Tech
tags:
  - 测试
  - RobotFramework
---
## ./ 
- rundevel.py 运行RF代码
- setup.py 安装程序，含有一个类-custom_install_scripts
- tasks.py 帮助RF打包的Tasks，每一个task对应一个函数


## ./src/robot
- /src/robot
- __init__.py 初始化程序
- __main__.py 启动程序
- errors.py 定义异常类和异常返回代码，外部库不使用此处定义的异常
- jarrunner.py 含有一个类-JarRunner，用来从.jar文件运行RF时完成Java-Jython的交互
- libdoc.py 含有一个类-LibDoc，实现了Libdoc工具命令行入口的模块
- pythonpathsetter.py 增加目录（Robot所需）到sys.path
- rebot.py 含有一个类-Rebot，实现了处理后结果输出命令行入口的模块
- run.py 含有一个类-RobotFramework，实现了执行测试命令行入口的模块
- testdoc.py 含有三个类-TestDoc，TestdocModelWriter，JsonConverter，实现了Testdoc工具命令行入口的模块
- tidy.py 含有三个类-Tidy，TidyCommandLine，ArgumentValidator，实现了Tidy工具命令行入口的模块
- version.py 定义和获取RF版本信息





