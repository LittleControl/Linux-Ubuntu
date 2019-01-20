# 完美解决系统开机后登陆后死机问题，理论上支持所有Linux系统

首在在BIOS界面，按‘e’进入Ubuntu的编辑模式
<linux	/vmlinuz-4.15.0-43-generic root=UUID=fa1f350e-d809-474f-9c92-d4f31c24e002 ro  quiet splash $vt_handoff
找到这行
在其后面加入`acpi_osi=! acpi="windows 2009"
即如下图所示
```
linux	/vmlinuz-4.15.0-43-generic root=UUID=fa1f350e-d809-474f-9c92-d4f31c24e002 ro  quiet splash $vt_handoff acpi_osi=! acpi="windows 2009"
```
开机后找到`/boot/grub/grub.cfg`
修改该文件中对应的内容即可永久解决问题
