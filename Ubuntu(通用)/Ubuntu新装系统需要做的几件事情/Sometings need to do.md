# 还是在这记录一下吧，一些新装Linux系统之后需要做的事情

## 像我这样的换系统狂魔，记性还这么差，是时候记录一些事情了

    1. 安装Synaptic Package Manager
    2. 安装apt-xapian-index插件
    3. 安装Tweaks
    4. 安装dash-to-dock插件
    5. `sudo ubuntu-drivers autoinstall`
    6. 增加对RAM的使用
       1. `cat /proc/sys/vm/swappiness`
       2. `gedit admin:///etc/sysctl.conf`
       3. 文件末尾加如语句`vm.swappiness=10`
       4. `showdown -r now`
       5. `cat /proc/sys/vm/swappiness`
    7. 减少对硬盘的写入
       1. 打开disks工具，enable write cache
       2. `systemctl status fstrim`
       3. `gedit admin:///etc/fstab`
       4. 把`errors=remount-ro`改为`noatime,errors=remount-ro`
    8. 安装`User Themes`插件
    9. 激活shell可编辑状态`sudo apt-get install gnome-shell-extensions`
    10. 安装`Bleachbit`
    11. `sudo sed -i 's/NoDisplay=true/NoDisplay=false/g' /etc/xdg/autostart/*.desktop`
    12. install tlp and tlp-rdw
    13. `sudo tlp start`