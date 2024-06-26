FROM mysql:latest

# =两边不允许有空格
LABEL release-date="2024-06-26" \
      version="0.0.1" \
      description="Mysql"

MAINTAINER xh

RUN chown -R mysql:root /var/lib/mysql

ARG MYSQL_DATABASE
ARG MYSQL_USER
ARG MYSQL_PASSWORD
ARG MYSQL_ROOT_PASSWORD

ENV MYSQL_DATABASE=$MYSQL_DATABASE
ENV MYSQL_USER=$MYSQL_USER
ENV MYSQL_PASSWORD=$MYSQL_PASSWORD
ENV MYSQL_ROOT_PASSWORD=$MYSQL_ROOT_PASSWORD

COPY script/create_table.sql /docker-entrypoint-initdb.d

# 设置容器对外暴露3306端口
EXPOSE 3306
