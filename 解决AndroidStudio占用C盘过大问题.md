## Android Studio默认文件夹
~~~
C:\Users\user_name\.android
C:\Users\user_name\.gradle
C:\Users\18463\AppData\Local\Android\Sdk
C:\Users\18463\AppData\Local\Google\AndroidStudio
C:\Users\18463\AppData\Roaming\Google\AndroidStudio(可选)
~~~

1. 移动`C:\Users\18463\AppData\Local\Android\Sdk`文件夹到其他位置，如E:\AndroidData目录下
2. 移动`C:\Users\user_name\.gradle`文件夹到其他位置，如E:\AndroidData目录下
3. 移动`C:\Users\user_name\.android`文件夹到其他位置，如E:\AndroidData目录下
4. 删除`C:\Users\18463\AppData\Local\Google\AndroidStudio`文件夹
5. 删除`C:\Users\18463\AppData\Roaming\Google\AndroidStudio`文件夹(可选)
6. 添加系统环境变量
~~~
1. 设置 SDK 安装目录的路径
变量名：ANDROID_HOME
值：E:\AndroidData\Sdk

2. 为 Android SDK 中包含的工具设置用户偏好设置目录的路径，默认为 $HOME/.android/。
某些较旧的工具（例如 Android Studio 4.3 及更低版本）不会读取 ANDROID_USER_HOME。如需替换这些旧工具的用户偏好设置位置，请将 ANDROID_SDK_HOME 设置为要在其下创建 .android 目录的父目录。
变量名：ANDROID_USER_HOME
值：E:\AndroidData
注意修改avd目录下ini配置文件的路径

3. 设置.gradle目录的路径
变量名：GRADLE_USER_HOME
值：E:\AndroidData\.gradle

~~~

7. 配置Android Studio安装目录bin目录下的idea.properties文件
~~~
1. 取消如下项的注释
# idea.config.path=E:\AndroidData (自定义路径)
# idea.system.path=E:\AndroidData (自定义路径)
# idea.plugins.path=${idea.config.path}/plugins
# idea.log.path=${idea.system.path}/log
~~~

8. 重新启动Android Studio