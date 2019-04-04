---
title: DPlayer缩略图生成脚本
tags:
  - 代码
  - DPlayer
  - 缩略图
url: NaN.html
id: .nan
categories:
  - 前端
date: 2019-01-05 09:56:00
---

DPlayer-thumbnails 批量生成脚本

项目地址：[https://github.com/MoePlayer/DPlayer-thumbnails](https://github.com/MoePlayer/DPlayer-thumbnails)

确保已安装[`NPM`](https://www.baidu.com/s?ie=UTF-8&wd=%E5%AE%89%E8%A3%85npm)即可食用

DPlayer-thumbnails
==================

> Generate thumbnails for [DPlayer](https://github.com/MoePlayer/DPlayer)

[![npm](https://img.shields.io/npm/v/dplayer-thumbnails.svg?style=flat-square "npm")](https://www.npmjs.com/package/dplayer-thumbnails)[![npm](https://img.shields.io/npm/dt/dplayer-thumbnails.svg?style=flat-square "npm")](https://www.npmjs.com/package/dplayer-thumbnails)[![dependency Status](https://img.shields.io/david/MoePlayer/DPlayer-thumbnails.svg?style=flat-square "dependency Status")](https://david-dm.org/MoePlayer/DPlayer-thumbnails#info=dependencies)

Install（安装）
-----------

输完命令等读条，可能会有点慢

    $ npm install -g dplayer-thumbnails

Usage（使用）
---------

**命令结构：**  
命令 参数（输出） 缩略图路径 参数（质量，默认60即可） 视频路径

    $ dplayer-thumbnails --help
    $ dplayer-thumbnails -o ./thumbnails.jpg -q 60 demo.mp4

script（批量生成脚本）
--------------

复制以下代码另存为`thumbs.sh`，然后使用`chmod +x thumbs.sh`更改权限，就可以使用了。  
**使用条件：**

*   脚本与文件在同一个文件夹
*   视频文件名为纯数字.mp4，例如`01.MP4` `02.mp4`,小于10需要带`0`
*   具有目录的读写权限  
    **使用方法：**

`./thumbs 1 12` ：脚本路径 参数1（起始数字） 参数2（结束数字）

    #!/bin/bash
    for i in `seq $1 $2`
    do
        if [ "$i" -lt "10" ];then
            dplayer-thumbnails -o ./0$i.jpg -q 60 ./0$i.mp4
            echo "Video "$i".mp4 Done"
            echo "10! "
        fi
    done

在DPlayer中使用
-----------

在加载时`video`带有`thumbnails`参数即可