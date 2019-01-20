# 修改Ubuntu系统默认Python版本为Python3
虽然今天已经进入Python3的时代了
但是似乎现在的Linux系统默认的版本还是2.7
虽然预装了3的版本，但每次调用都要用Python3来运行文件
多不方便呀
最重要的是，Sublime它编译的只认你的系统默认版本:angry:
话不多说，直接来干货
## 方法一：
该方法我在deepin系统里成功了，但在Ubuntu下没有成功
该方法虽然在终端里的编译系统是Python3了，但在Sublime里的编译系统还是Python2.7
仅供参考
方法就是修改`~/.bashrc`文件
用vim，vi，gedit随便什么，你用的习惯的一个编辑器打开该文件
在文件末尾加入`alias python='python3'`
就是这样：
```
# enable programmable completion features (you don't need to enable
# this, if it's already enabled in /etc/bash.bashrc and /etc/profile
# sources /etc/bash.bashrc).
if ! shopt -oq posix; then
  if [ -f /usr/share/bash-completion/bash_completion ]; then
    . /usr/share/bash-completion/bash_completion
  elif [ -f /etc/bash_completion ]; then
    . /etc/bash_completion
  fi
fi
alias python='python3'
```
## 方法二：
该方法是我推荐的一种方法
据说上面的是在用户级修改的Python版本，而这个方法则是在系统级别修改的版本
首先打开终端，切换到root身份
输入`update-alternatives --list python`来查看当前`alternatives`里已经存在的Python版本
如果终端给你返回的是`update-alternatives: error: no alternatives for python`
那么我们就需要先把Python包导入到`alternatives`里
现在的Linux系统一般都自带Python2和Python3，且路经都是`/usr/bin/python(?)`
在终端输入以下命令：` update-alternatives --install /usr/bin/python python /usr/bin/python(?)`
即可导入你想安装的Python版本
然后终端会给你一个返回消息：`update-alternatives: using /usr/bin/python2.7 to provide /usr/bin/python (python) in auto mode`
则说明导入成功
然后输入`update-alternatives --config python`
根据终端的返回消息即可切换对应的Python版本
