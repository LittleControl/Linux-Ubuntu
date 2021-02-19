# nmcli的简单使用

nmcli是NetworkManager内置的命令行工具, 一般新系统或者tty环境下需要连接WiFi时会用得到,这里主要指的是WiFi的使用

- 查看附近可见的无线网络 `nmcli device wifi list`
- 使用默认的无线网卡连接到特定的无线网络 `nmcli device wifi connect SSID password PASSWORD`
- 使用默认的无线网卡连接到隐藏的网络 `nmcli device wifi connect SSID password PASSWORD hidden yes`
- 使用特定的网卡连接网络,假设接口名称为`wlan1`, 要保存的配置文件名为`wlan1_profile` `nmcli device connect SSID password PASSWORD ifname wlan1 wlan1_profile`
- 断开一个网络接口(`wlan1`)的连接 `nmcli device disconnect ifname wlan1`
- 查看所有配置文件的具体信息 `nmcli connection show`
- 激活一个配置文件`profile0` `nmcli connection up profile0`
- 删除一个配置文件, 通过name或者uuid `nmcli connection delete name_or_uuid`
- 查看所有接口的状态 `nmcli device`
- 关闭WiFi `nmcli radio wifi off`
