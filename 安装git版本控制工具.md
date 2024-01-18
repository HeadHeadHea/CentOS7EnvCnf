# Git源码安装
---
  
- **官网下载最新版git安装包**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[git下载](https://mirrors.edge.kernel.org/pub/software/scm/git/)

- **解压，安装，配置**
```shell
# 解压
tar -zxvf git-2.43.0.tar.gz -C /usr/local

# 安装
cd /usr/local/git-2.43.0
./config --prefix=/usr/local/git_tool
make && make install

# 配置
cd ~ && vim .bashrc

# 添加如下语句
# git环境变量
PATH="$PATH":/usr/local/git_tool/bin

# 保存退出，更新bash配置
source .bashrc
```

- **查看git版本**
```shell
git --version
```

- **配置账户和邮箱**
```shell
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

- **生成ssh密匙**
```shell
ssh-keygen -t rsa -C "你的邮箱"
```

- **将ssh密匙复制到远程仓库**
```shell
cat /root/.ssh/id_rsa.pub
```

- **将代码推送到远程分支**
```shell
git init
git add .
git commit -m '注释'
git branch -M main
git remote add origin xxxx.git
git push -u origin main
```

- **安装成功后可删除源码文件git-2.43.0**