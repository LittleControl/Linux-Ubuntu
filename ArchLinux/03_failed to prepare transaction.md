# failed to prepare transaction (could not satisfy dependencies)

昨天更新Arch的时候出现了以下错误

｀｀｀shell
error: failed to prepare transaction (could not satisfy dependencies)
:: installing xorgproto (2019.2-2) breaks dependency 'dmxproto' required by libdmx
:: installing xorgproto (2019.2-2) breaks dependency 'xf86dgaproto' required by libxxf86dga
Error installing repo packages
｀｀｀

---
出现这个问题的原因不清楚,但是解决办法很简单  
解决办法: 执行一下命令,即可正常更新

1. `pacman -Rdd dmxproto xf86dgaproto`
2. `pacman -Syu`

这样就没有问题了
