---
title: Web配置命令代码记录，Nginx，PHP，MySQL，Docker，宝塔
tags:
  - 系统
  - 配置
  - Linux
  - ubuntu
  - centos
  - Docker
  - php
  - web
  - Nginx
  - mysql
  - lnmp
  - mingling
url: NaN.html
id: .nan
categories:
  - 系统
date: 2019-04-01 14:51:00
---

Web配置命令代码记录，重建服务器时用

Ubuntu
------

Centos
------

Nginx
-----

PHP
---

MySQL
-----

Docker
------

Docker常用命令

### API相关

#### RTMP推流

建立

    docker run -it -p 1935:1935 -p 8090:80 --rm alfg/nginx-rtmp

进入 `ad7a8ee8f00a`为容器id

    docker exec -it ad7a8ee8f00a  /bin/sh

宝塔
--

更改默认PHP版本

    rm -rf /usr/bin/php
    
    ln -s /www/server/php/7/bin/php /usr/bin/