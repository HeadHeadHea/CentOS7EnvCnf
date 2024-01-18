# 升级gcc和g++编译器
---

- **通过centos-release-scl源安装devtoolset包**
```shell
yum install centos-release-scl
```

- **安装devtoolset包**

    devtoolset对应的gcc版本
```shell
devtoolset-3对应gcc4.x.x版本
devtoolset-4对应gcc5.x.x版本
devtoolset-6对应gcc6.x.x版本
devtoolset-7对应gcc7.x.x版本
devtoolset-8对应gcc8.x.x版本
devtoolset-9对应gcc9.x.x版本
devtoolset-10对应gcc10.x.x版本

# 安装devtoolset-10
yum install devtoolset-10
```

- **激活gcc版本**
```shell
cd ~ && vim .bashrc

# 添加如下语句保存并退出
# 使用gcc和g++ 10.0版本
source /opt/rh/devtoolset-10/enable

# 更新配置
source .bashrc
```