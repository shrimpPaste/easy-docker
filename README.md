# easy-docker

#### 介绍
市面上的教程大多告诉你一些简单的定义，例如docker run就可以开启一个容器，-v 就可以加上映射的关系，对于一个新手来说这是不友好的，
名词太多看到最后就剩下**十万个为什么**。

本项目会提供定制化的Dockerfile文件，让开发者不需要创建新的容器而消费心智，做到开箱即用才是我们的目的。同时，在后续会继续完成0基础
该如何学习docker，甚至你可以在我的Dockerfile或者项目的Redeme中学习，我会尽力的把买个Dockerfile涉及的知识点都说出来且说明白，可以让你
的学习路径不那么陡峭。

#### 软件架构
```text
.
├── LICENSE
├── mysql
│   ├── docker-compose.yml
│   ├── Dockerfile
│   ├── README.md
│   └── script
│       ├── create_table.sql
│       └── setup.sh
├── README.en.md
├── README.md
└── ubuntu_20_04_focal
    ├── Dockerfile
    └── README.md
```

每个目录都是一个服务，我会在目录下把需要创建的目录，使用到的配置都写在里面。


#### 使用说明

开箱即用即是你拿到就可以使用，如果你需要使用mysql，你只需要吧Mysql目录复制一份到你的项目地址，进入到项目地址/mysql目录下运行docker-composer.yml，
他会需要在目录下创建一个`data`目录，来持久化的存放数据，更详细的内容会在每个项目下的README.md文件中体现

#### 参与贡献

1.  Fork 本仓库
2.  新建 feature/你的名字-模块 分支
3.  提交代码
4.  新建 Pull Request


