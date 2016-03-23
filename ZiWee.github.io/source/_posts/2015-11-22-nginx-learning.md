---
layout: default
title:  nginx学习
---


---

#2015-11-22
#对nginx的现有认知

##进程结构:

```
    root     19386  0.0  0.0   3600   288 ?        Ss   16:08   0:00 nginx: master process nginx
    nobody   19387  0.0  0.0   3792  1956 ?        S    16:08   0:00 nginx: worker process
    ...
```

##对并发的处理
1. master为管理进程,worker为实际的处理连接的进程,
2. 一般为一个master带k个worker进程, k一般设置为cpu核数
3. master-worker结构做了对连接的负载均衡
4. 对连接采用epoll模型

##对某个连接的处理
1. 模块化,多个模块通过函数指针连接起来

#新的学习
进行中
