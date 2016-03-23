---
layout: default
title:  openwrt编译未生成factory.bin和sysupdate.bin原因
---

最近需要做点一个热点范围内的移动终端的检测，想到用openwrt实现，通过移动终端发起的管理帧来检测。

##问题：
编译openwrt时遇到了问题，没有生成factory.bin和sysupdate.bin

##原因：
查了下是当生成bin大于4m时不会生成这两个文件。

##解决办法：
1. 尝试少选几个编译选项
2. 参考https://forum.openwrt.org/viewtopic.php?pid=238165解决
```
To make these changes via a script (works on BB, b41353):
sed -i '/TLWR703/              s/4Mlzma/16Mlzma/'   target/linux/ar71xx/image/Makefile
sed -i '/TL-WR703Nv1/,/layout/{s/4Mlzma/16Mlzma/;}' tools/firmware-utils/src/mktplinkfw.c
FWIW, I did not change fw_max_len, but the thing still built!
```

