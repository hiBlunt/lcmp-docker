# 使用教程
1. cp docker-compose.yml.sample  docker-compose.yml
2. cp .env.sample .env
3. cp services/caddy/etc/caddy/Caddyfile.sample services/caddy/etc/caddy/Caddyfile
4. 修改.env中的MYSQL5_ROOT_PASSWORD，换成强密码
5. 切换到项目根目录，docker-compose up -d启动项目
6. 进入mysql，创建数据库
7. 上传代码到www目录下
8. 在根目录执行chown -R 1000:1000 www, 避免php程序没有对应权限
9. 修改services/caddy/etc/caddy/Caddyfile文件，配置caddy代理
10. 打开网页，开始安装

## 注意事项：
1. www下文件权限为644，文件夹权限为755.请勿使用777，这会带来安全风险
2. 安装完成后删除typecho源代码中的install.php, install文件夹
3. 因为services/mysql/mysql.cnf下的client，mysqld，mysql三项编码已经设为utf8emb4，
   在创建数据库时，输入create database your_bd即可，无需重复设置编码。
