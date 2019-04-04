---
title: 黑群以及DDNS配置命令
tags:
  - 配置
  - 命令
  - 群晖
  - DDNS
url: NaN.html
id: .nan
categories:
  - 系统
date: 2019-03-22 23:18:00
---

黑群命令，DDNS站点配置，常见故障排除

DDNS
----

自动换ip脚本

    cd /volume1/ds/aliyundns && date >> log && python ddns.py >> log

群晖
--

### 映射下载卷到共享文件夹

Download Station 未下载完的内容

    mount --bind /volume1/@download /volume1/web/NAS/d