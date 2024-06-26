FROM ubuntu:20.04
LABEL authors="xh"

# 更新软件包列表并安装必要的软件包
RUN apt-get update && apt-get install -y \
    wget \
    curl \
    git \
    vim \
    zsh \
    && rm -rf /var/lib/apt/lists/* \
    # 配置本地环境
    && apt-get update && apt-get install -y locales \
    && rm -rf /var/lib/apt/lists/* \
    && localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 \
    && sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 设置环境变量
ENV LANG en_US.UTF-8
ENV TZ=Asia/Shanghai

WORKDIR /app

CMD ["zsh"]
