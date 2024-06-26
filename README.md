# **easy-docker指南**

## **引言**

在众多Docker教程中，初学者常常被复杂的术语和操作弄得晕头转向，最终满腹疑惑。本项目旨在为开发者提供一个易于理解和使用的Docker环境，通过定制化的Dockerfile文件，让开发者能够轻松实现“开箱即用”的体验。

## **项目宗旨**

我们的目标是简化Docker的使用流程，让每位开发者都能在不消耗过多精力的情况下快速上手并利用Docker技术。随着项目深入，我们将继续完善零基础学习Docker的教程，并在Dockerfile和项目文档中详细解释每个知识点，确保你的学习之路既平坦又高效。

## **软件架构**

以下是本项目的目录结构概览：

```
.
├── LICENSE
├── mysql
│   ├── docker-compose.yml
│   ├── Dockerfile
│   ├── README.md
│   └── script
│       ├── create_table.sql
│       └── setup.sh
├── README.en.md
├── README.md
└── ubuntu_20_04_focal
    ├── Dockerfile
    └── README.md
```

每个子目录代表一个独立的服务单元，包含创建服务所需的所有配置和脚本。

## **使用指南**

“开箱即用”意味着无需额外配置即可立即使用。例如，若需使用MySQL服务，只需将`mysql`目录复制至你的项目路径下，然后在`mysql`目录中运行`docker-compose.yml`。系统将提示创建一个`data`目录以持久化存储数据。更详尽的使用说明，请参考各个项目目录下的`README.md`文件。

## **贡献指南**

欢迎每位开发者为本项目贡献力量：

1. **Fork 本仓库** - 将本项目Fork至你的GitHub账户。
2. **新建分支** - 创建一个以`feature/你的名字-模块`命名的新分支。
3. **提交代码** - 完成功能开发或改进后，提交你的代码。
4. **新建Pull Request** - 向本项目发起Pull Request，以便我们将你的贡献合并入主分支。
