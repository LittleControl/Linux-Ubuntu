# 笔记本电脑装双系统后时间不一致问题

## 关于为何时间不一致，为何是相差八个小时的问题自己百度一下就可一了

  这里只简单介绍一下相关的操作

    - 现在Ubuntu里更新一下时间，确认与实时时间保持一致

       - 执行命令 `sudo apt install ntpdate` 安装需要的组件
       - 执行命令 `sudo ntpdate time.windows.com` 使Ubuntu时间与Windows时间同步
       - 执行命令 `sudo hwclock --localtime --systohc` 讲当前时间更新到硬件上
    - 大功告成!