# 使用教程
1. cp docker-compose.yml.sample  docker-compose.yml
2. cp .env.sample .env
3. 修改.env中的MYSQL5_ROOT_PASSWORD，换成强密码
4. 切换到项目根目录，docker-compose up -d启动项目
5. 进入mysql，创建数据库
6. 上传代码到www目录下
7. 在根目录执行chown -R 1000:1000 www, 避免php程序没有对应权限

## 注意事项：
1. www下文件权限为644，文件夹权限为755.请勿使用777，这会带来安全风险
2. 安装完成后删除typecho源代码中的install.php