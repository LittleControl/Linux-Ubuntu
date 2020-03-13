# ArchLinux - 'hostname' command not found

前几天的时候,系统反正是出问题了,反正最后还是重新装了一下Arch,虽然用了Arch很久了,但是重新再安装一便的话也不是那么轻车熟路.中间不知道瞎搞什么的,应该是删除了一个依赖关系.导致`hostname`这个命令丢失了.虽然平时不怎么用这个命令,但是每次打开终端的时候,用的oh-my=zsh就会提示`command not found: hostname`.像我这种有强迫症的人,怎么受的了.不过最后还是把问题解决了.

经过也是各种Google,终于找到了包含hostname打软件包.  
直接`pacman -S inetutils`就ok了
