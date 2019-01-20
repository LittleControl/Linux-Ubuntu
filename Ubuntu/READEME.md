开机时候在bois界面编译Ubuntu
在编辑模式下找到 
>linux	/vmlinuz-4.15.0-43-generic root=UUID=fa1f350e-d809-474f-9c92-d4f31c24e002 ro  quiet splash $vt_handoff

在这行末尾添加如下内容：
```
acpi_osi=! acpi="windows 2009"
```
开机后grub目录在/boot/grub/grub.cfg
修改该文件的内容即可永久解决
