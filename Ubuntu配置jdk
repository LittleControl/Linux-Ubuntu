# 在Ubuntu里配置jdk

既然你都用上Linux了，所以单纯的JRE肯定满足不了你的需要
所以[JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html/"jdk"
)是你的不二选择

下载好jdk后解压啥的就不多说了

关键是是添加java到环境变量里
windows简单，直接可以手动导入，可惜了，这是Linux


思路就是这样的在 /etc/profile
打开编辑这个文件
在文件末尾加入以下内容
```
JAVA_HOME=/usr/java/jdk1.8.0_201
JRE_HOME=${JAVA_HOME}/jre
CLASS_PATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
PATH=${JAVA_HOME}/bin:${JRE_HOME}/bin:$PATH
export JAVA_HOME JRE_HOME PATH CLASS_PATH
```
注意，只要第一个JAVA_HOME=后的路径是你的解压出来的路径，其他的都无需修改，因为都是相对路径
然后保存 打开终端 输入`source /etc/profile`命令或者重启一下电脑
再在终端里输入`java -version`
就可以看到成功的返回结果了
