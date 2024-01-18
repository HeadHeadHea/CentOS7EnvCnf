# CMake源码安装
---

- **官网下载最新版cmake安装包**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[CMAKE下载](https://cmake.org)

- **解压安装包**
```shell
# 解压安装包到 /usr/local目录下
tar -zxvf cmake-3.28.1.tar.gz -C /usr/local
```

- **安装openssl(不安装可能会报错)**
```shell
yum install openssl openssl-devel
```

- **安装cmake**
```shell
# 1.进入目录
cd /usr/local/cmake-3.28.1

# 2.执行configure文件并指定安装目录
./configure --prefix=/usr/local/cmake_tool

# 3.安装cmake
make && make install
```

- **配置环境变量**
```shell
# 1.打开.bashrc文件
cd ~ && vim .bashrc

# 2.添加如下语句
# cmake环境变量
PATH="$PATH":/usr/local/cmake_tool/bin

# 3.保存，退出并更新bash配置
source .bashrc
```

- **查看cmake版本**
```shell
cmake --version
```

- **安装成功后可删除源码文件cmake-3.28.1**