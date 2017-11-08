Pomelo服务器管理工具
======
安装方法：
```
git clone https://github.com/LiveXY/pomelo-servers-manager.git
cd pomelo-servers-manager
npm install -ddd && npm link
```
使用方法：
```
psm list/servers/connections/ps/start/stop/check/config/restart/repair/kill/getmain/setmain/get/set path [ids]

实例：
psm list /path	 查看server状态，+rss
psm servers /path	 查看server状态，+port
psm connections /path 查看前端链接用户数
psm ps /path		 查看server进程
psm start /path	 启动server
psm stop /path	 停止server
psm check /path	 检查server
psm repair /path	 恢复server
psm config /path	 查看server配置
psm restart /path	 重启server
psm kill /path	 终止server进程 用于执行stop后没有停止server的清理

psm start /path db-server-1 db-server-2	 启动指定的server
psm stop /path db-server-1 db-server-2	 停止指定的server
psm restart /path db-server-1 db-server-2	 重启指定的server 不建议使用

psm getmain /path	 	 获取master参数main的值
psm setmain /path	 	 修改master参数main=启动文件路径
psm get /path id key	 	 获取server配置
psm set /path id key value	 修改server配置

1分钟自动恢复
crontab -e
* * * * * /usr/bin/psm repair /path >> /dev/null 2>&1

```