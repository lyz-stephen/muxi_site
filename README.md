木犀官网项目github测试版
===

    我们在路上、前方不会太远

木犀官网项目是面向木犀内部的一系列服务网站,分为团队介绍、图书、分享、博客四个板块

<hr>

### 状态
#### 当前状态: 开发中
#### 分支

    master: 主分支: 发布特定功能
    develop: 开发分支

### 合作
#### 1:本地环境搭建
1.安装flask

    教程: http://docs.jinkan.org/docs/flask/installation.html#installation
    不懂处请私聊朱承浩或者王怡凡

2.安装扩展环境

    进入虚拟环境(还是请参见教程)
    pip install -r requirment.txt

    安装遇到问题请私聊朱承浩或者王怡凡


3.构建本地测试数据库
运行 data.sh 脚本

	$ chmod 777 data.sh
	$ ./data.sh

然后在跳出的交互解释器中输入以下命令来创建用户角色

	>> Role.insert_roles()
	>> quit()

然后本地测试数据库就搭好了

4.连接远程测试数据库

    搭建中........

5.运行项目

    运行: python manage.py runserver
    当前路由:
        127.0.0.1:5000/muxi  木犀官网
        127.0.0.1:5000/book  木犀图书
        127.0.0.1:5000/share/1 木犀分享

#### Git 工作流

    项目采用git工作流
    每当有特定功能提交时, 请一定一定一定一定要遵循以下步骤

0: fork 项目仓库

    在github上fork这个仓库

1: clone fork的项目仓库

    git clone https://github.com/your_username/muxi_site.git

2: 从development分支开出功能分支(以feature为例)

    git checkout develop
    git checkout -b feature develop

3: 在feature分支进行功能开发

    写写写写写..............代码

4: 本地调试

    确保代码修改可以在本地调试通过

5: 向feature分支提交

    请提交时只提交改动的文件，并写好commit信息

6: 在Github 上向dev分支发送pull request

7: 并入development分支(项目维护人负责)

8: merge development分支到master，发布版本(项目维护人负责)

### 进度

    2015年10月19号: 木犀图书测试版1.0上线，1.0+正在修bug
    -----------------------------------------------------
    2015年10月19日: 木犀分享完成基本功能，下一步整合markdown编辑器和优化
    -----------------------------------------------------
    2015年10月20日: 木犀分享完成分页功能、权限管理
    -----------------------------------------------------
    2015年10月22日: 总结此仓库的合作方式(前后端)，因为有点混乱有点烦
    -----------------------------------------------------
    2015年10月23日: 完成博客数据库model编写, master<->development
    -----------------------------------------------------
	2015年11月5日 : 木犀分享基本功能完成，待前端修改相关样式
    -----------------------------------------------------
	2015年11月7日 : 编写data脚本，自动构建本地测试数据库
    -----------------------------------------------------
	2015年11月9日 : 新的开发分支 develop 替代 development

