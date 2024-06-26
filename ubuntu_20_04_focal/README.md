## 项目描述
该Dockerfile是提供ubuntu20.04为基础的image，提供了curl、vim、zsh、wget、curl、中文支持的镜像。
项目简短不代表不重要，在非linux开发环境下，打包镜像、linux特有的操作在其他开发平台是无法满足的， 如windows不支持Go项目打包成deb。

由于公司项目软件运行在Ubuntu下，deb文件又是ubuntu的软件包，将二进制文件打包成deb文件那只有ubuntu才能满足。

## 项目工作目录
镜像会默认工作在`/app`目录下，是镜像默认支持的工作区域，在Dockerfile中使用了WORKDIR明确指定了工作区域。

## 文件魔改思路
目前该镜像是不对外暴露端口的，如果你需要用ssh工具可以更方便的管理，你可以自行修改对外暴露22端口，在docker run时候与宿主机进行绑定即可，
这样就能支持本地的ssh链接，例如使用Mobxterm工具，可以可视化管理文件，实际上我们文件都是由volume进行映射，不是那么刚需。

## 使用教程
将Dockerfile打包成镜像
```shell
	docker build -t xh-ubuntu .
```

运行容器
```shell
	docker run -it -v .:/app --name easy-ubuntu xh-ubuntu zsh
```

> PS: 容器运行结尾用的是zsh目的是进去容器就可以使用zsh的功能，如果你不需要你可以删除Dockerfile的zsh和curl等模块，结尾修改成`/bin/bash`即可，包会更小。
