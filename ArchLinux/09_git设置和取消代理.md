# git设置和取消代理

```shell
git config --global http.proxy 'socks5://127.0.0.1:1080'

git config --global https.proxy 'socks5://127.0.0.1:1080'

git config --global --unset http.proxy

git config --global --unset https.proxy

```

## git的一些简单命令

### 初始化

```shell
git config --global user.name 'LittleControl'
git config --global user.email 'litlecontrol2019@gmail.com'
```
