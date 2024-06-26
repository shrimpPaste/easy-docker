## Dockerfile 镜像描述
该Dockerfile是用于构建mysql镜像的，用于提供定制化的mysql镜像服务。
镜像对外提供3306端口
内部挂载点容器默认存放，/var/lib/mysql

## 目录说明
data: 用于存储容器运行时持久化数据，容器崩坏时再开启容易映射到物理地址既可以找回数据。
script: 用于存放初始化sql文件
docker-compose.yml: 用于构建docker容器
Dockerfile: 用于构建docker镜像

## 使用说明
镜像提供四个执行时必须输入的参数，如下:
- MYSQL_DATABASE: 创建数据库
- MYSQL_USER: 数据库用户名
- MYSQL_PASSWORD: 用户名密码
- MYSQL_ROOT_PASSWORD: 管理员密码

## docker-compose使用
```shell
pwd
            
\xh\docker\mysql

docker-compose up -d
```

## docker run 使用
docker run -d -e MYSQL_DATABASE=kfr_flow_db -e MYSQL_USER=kungfu -e MYSQL_PASSWORD=kungfu123 -e MYSQL_ROOT_PASSWORD=123 --name mysql-test -p 3306:3306 dispatch-mysql

