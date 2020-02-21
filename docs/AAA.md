# 开发环境搭建
## 安装开发工具
开发工具:Visual Studio 2017 Community免费版，企业版须破解

## 数据库
SQL SERVER 2012 R2,Express免费版，其他版本须破解，如有其他版本也可

## 数据库工具
若安装数据库后，无数据库工具：SQL SERVER Management Studio，可前往官网下载期望的版本。

官网下载地址：https://docs.microsoft.com/zh-cn/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15

## 安装SVN
若无登录账号，可联系相关同事创建

## 安装IIS
打开【控制面板】—＞【程序】—＞【打开或关闭Windows功能】，勾选【Internet信息服务】

## 签出项目代码
项目具体的 SVN 地址请询问同事，然后在对应目录鼠标右击，签出到指定文件夹即可

## 还原数据库
从 https://120.77.37.241/svn/wms/fx/trunk/db.zip 下载空数据库，可使用 svn 签出，还原 WMS 数据库，还原时注意使数据库名字与 web.config 连接字符串的数据库名字相同

## 还原技术日志数据库

## 创建网站
使用Windows + R键，输入命令：inetmgr，回车，打开【IIS管理器】，右键点击【网站】，选择【添加网站】，填写以下信息：

【网站名称】

【物理路径】，WebUI的路径

【端口】，按项目中的配置填写，包括网站访问端口和WCF服务端口
## Windows服务
应将以下服务设为自动启动 
MSDTC

Net.Tcp Listener Adapter

Net.Tcp Port Sharing Service


## DTC配置
在【管理工具】【组件服务】中，展开【Distributed Transaction Coordinator】【本地 DTC】，在【属性】页的【安全】选项卡中，做以下配置：
【网络 DTC 访问】，选中【允许远程客户端】，选中【允许远程管理】，选中【允许入站】，选中【允许出站】，选中【不要求进行验证】，选中
•【启用 XA 事务】，选中
•【启用 SNA LU 6.2 事务】，选中
•【DTC 登录账户】，使用 NetworkService 账户

## 防火墙
应关闭防火墙，防止无法连接到该计算机



