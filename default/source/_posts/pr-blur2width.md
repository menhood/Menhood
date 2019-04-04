---
title: Premiere竖屏视频模糊加宽效果实现
tags:
  - 教程
  - PR
  - 效果
  - Premiere
  - 模糊
url: NaN.html
id: .nan
categories:
  - 影视
date: 2018-08-22 09:35:00
---

很多时候视频是竖屏拍摄的，所以在大部分是横屏比例的设备上观看特别别扭，这种情况可以用模糊后的视频来当背景……

新建项目
----

### 新建项目流程

![01新建项目.png](https://i.loli.net/2018/08/22/5b7cb959ba666.png "01新建项目.png")

### 设置项目名称

![02设置项目名称.png](https://i.loli.net/2018/08/22/5b7cb959c3c1f.png "02设置项目名称.png")

导入视频
----

![03导入竖屏视频.png](https://i.loli.net/2018/08/22/5b7cb959cc2b5.png "03导入竖屏视频.png")

新建序列
----

### 新建序列流程

![04新建序列.png](https://i.loli.net/2018/08/22/5b7cb959cc14c.png "04新建序列.png")

### 设置序列参数

![05设置序列参数.png](https://i.loli.net/2018/08/22/5b7cb959df95d.png "05设置序列参数.png")

编辑视频
----

### 放入时间线

![06将素材拖入时间线.png](https://i.loli.net/2018/08/22/5b7cb959df95d.png "06将素材拖入时间线.png")

### 如遇提示

![07保持现有设置.png](https://i.loli.net/2018/08/22/5b7cb959de278.png "07保持现有设置.png")

### 调整素材大小

选中素材，然后找到`效果控件`，调节`缩放`至合适位置  
![08选中素材，然后找到效果控件，选中运动，右边的节目窗口会出现调整用的框.png](https://i.loli.net/2018/08/22/5b7cb95a02cab.png "08选中素材，然后找到效果控件，选中运动，右边的节目窗口会出现调整用的框.png")

### 如无上图面板

![09如果没有效果控件和效果面板在这里打开.png](https://i.loli.net/2018/08/22/5b7cb959df8cd.png "09如果没有效果控件和效果面板在这里打开.png")

### 复制视频轨道

按住`alt`键，用鼠标左键拖动v1轨道到v2轨道，复制一层  
![10按住alt键，用鼠标左键拖动v1轨道到v2轨道，复制一层.png](https://i.loli.net/2018/08/22/5b7cb959de887.png "10按住alt键，用鼠标左键拖动v1轨道到v2轨道，复制一层.png")

### 添加模糊效果

选中v1轨道素材，进入效果面板，搜索`快速模糊`，将快速模糊拖到v1的素材上  
![11选中v1轨道素材，进入效果面板，搜索快速模糊，将快速模糊拖到v1的素材上.png](https://i.loli.net/2018/08/22/5b7cbb4f0c134.png "11选中v1轨道素材，进入效果面板，搜索快速模糊，将快速模糊拖到v1的素材上.png")

### 调整背景及效果参数

保持v1轨道素材为选中状态，在效果控件面板调整`缩放`使背景层全屏，调整快速模糊的`模糊度`  
![12保持v1轨道素材为选中状态，在效果控件面板调整缩放使背景层全屏，调整快速模糊的模糊度.png](https://i.loli.net/2018/08/22/5b7cbb4f15faa.png "12保持v1轨道素材为选中状态，在效果控件面板调整缩放使背景层全屏，调整快速模糊的模糊度.png")  
大概是这个效果  
![13大概是这个效果.png](https://i.loli.net/2018/08/22/5b7cbb4f2a08c.png "13大概是这个效果.png")

导出
--

### 导出媒体流程

![14导出媒体.png](https://i.loli.net/2018/08/22/5b7cbb4f1461f.png "14导出媒体.png")

### 导出参数

`输出名称`处蓝色的字可以点击，点击后可调整保存位置及保存名称  
![15调整导出参数.png](https://i.loli.net/2018/08/22/5b7cbb4f27a67.png "15调整导出参数.png")

### 等待读条

![16等读条.png](https://i.loli.net/2018/08/22/5b7cbb4ef3899.png "16等读条.png")

完成！

const dp = new DPlayer({ container: document.getElementById('dplayer'), video: { url: 'https://menhood.320.io/files/%E6%95%99%E7%A8%8B/%E8%87%AA%E5%88%B6%E6%95%99%E7%A8%8B/pr%E7%AB%96%E5%B1%8F%E5%8A%A0%E5%AE%BD%E6%95%99%E7%A8%8B/%E7%AB%96%E5%B1%8F%E6%A8%A1%E7%B3%8A%E5%8A%A0%E5%AE%BD.mp4', pic: 'https://i.loli.net/2018/08/27/5b83607b300cd.png', thumbnails: '' }, danmaku: { id: 'prdemo01', api: 'https://api.prprpr.me/dplayer/' } });