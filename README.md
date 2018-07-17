# Apache Mac 服务器本地搭建
## 创建需要存放网站目录
`/Users/"用户名" 目录下 创建"Sites" 的文件夹`
快速显示隐藏显示系统文件快捷键（command + shift + .）
## apache 相关命令
* 关闭
`$sudo apachectl -k stop`
* 开启
`$sudo apachectl -k start`
* 重启
`$sudo apachectl -k restart`


-------

1. 切换工作目录
`cd /etc/apache2`
2. 编辑配置文件
`sudo vim httpd.conf`
3. 查找DocumentRoot
`/DocumentRoot`
替换成
`/Users/"用户名" 目录下 创建"Sites`
```
DoucumentRoot "Users/用户名/Sites"
<Directory "Users/用户名/Sites">
Options Indexes FollowSymLinks Multiviews
```
4. 查找php
`/php` 去掉前面的注释#
5. 切换工作目录
`cd /etc`
6. 拷贝 php 文件
`sudo cp php.ini.default php.ini`
7. 重启Apache
`$sudo apachectl -k restart`

###### 本地服务搭建完成

