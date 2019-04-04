---
title: AE仿抖音图标的色散效果
tags:
  - 教程
  - AE
  - 效果
  - AfterEffect
  - 色散
  - 抖音
url: NaN.html
id: .nan
categories:
  - 影视
date: 2018-09-16 16:02:00
---

禁忌：多重存在！

导入以及基本操作
--------

> 导入文件  
> ![01导入文件.jpg](https://i.loli.net/2018/09/16/5b9e0b42b0ea2.jpg "01导入文件.jpg")  
> 新建合成

![02新建合成.jpg](https://i.loli.net/2018/09/16/5b9e0b4252cd9.jpg "02新建合成.jpg")

效果参数
----

> 选中素材 添加效果

![03选中素材 添加效果.jpg](https://i.loli.net/2018/09/16/5b9e0b43463b6.jpg "03选中素材 添加效果.jpg")

> 特效选择为and模式 叠加模式改为screen

![04特效选择为and模式 叠加模式改为screen.jpg](https://i.loli.net/2018/09/16/5b9e0b4325634.jpg "04特效选择为and模式 叠加模式改为screen.jpg")

> `Ctrl`+`D`复制三份

![05Ctrl加D复制三份，每层的效果value值只能为一个通道255.jpg](https://i.loli.net/2018/09/16/5b9e0b4329ecd.jpg "05Ctrl加D复制三份，每层的效果value值只能为一个通道255.jpg")

> 看参数调节

![06看参数调节.jpg](https://i.loli.net/2018/09/16/5b9e0b432cd3f.jpg "06看参数调节.jpg")

> 看参数调节

![07最后一层参数.jpg](https://i.loli.net/2018/09/16/5b9e0b432be6e.jpg "07最后一层参数.jpg")

> 把指针在想要加效果的位置然后全选层 按`P`键 点上秒表记录关键帧

![08把指针在想要加效果的位置然后全选层 按P键 点上秒表记录关键帧.jpg](https://i.loli.net/2018/09/16/5b9e0b431f48d.jpg "08把指针在想要加效果的位置然后全选层 按P键 点上秒表记录关键帧.jpg")

> 调节位置参数1

![09调节位置参数.jpg](https://i.loli.net/2018/09/16/5b9e0b4324070.jpg "09调节位置参数.jpg")

> 调节位置参数2

![10调节位置参数.jpg](https://i.loli.net/2018/09/16/5b9e0b43244f2.jpg "10调节位置参数.jpg")

> 调节位置参数3

![11调节位置参数.jpg](https://i.loli.net/2018/09/16/5b9e0b4df0393.jpg "11调节位置参数.jpg")

导出
--

> 调整完毕后导出 快捷键 `Ctrl`+`M`

![12调整完毕后导出 快捷键 Ctrl加M.jpg](https://i.loli.net/2018/09/16/5b9e0b4e0853b.jpg "12调整完毕后导出 快捷键 Ctrl加M.jpg")

> 导出参数

![13导出参数.jpg](https://i.loli.net/2018/09/16/5b9e0b4e3be26.jpg "13导出参数.jpg")

> 选择位置>渲染

![14选择位置 渲染.jpg](https://i.loli.net/2018/09/16/5b9e0b4e54d78.jpg "14选择位置 渲染.jpg")

> 等读条

![15等读条.jpg](https://i.loli.net/2018/09/16/5b9e0b4e1d9e8.jpg "15等读条.jpg")

Done.

效果
--

Chrome下可见 :huaji8:  
好吧，现在Firefox下应该也可以了 :huaji4:

const dp = new DPlayer({ container: document.getElementById('dplayer'), loop:true, video: { url: 'https://menhood.320.io/files/%E6%95%99%E7%A8%8B/%E8%87%AA%E5%88%B6%E6%95%99%E7%A8%8B/AE%E8%89%B2%E6%95%A3/%5B4K%5D%20%E8%B5%9B%E8%BD%A6.mp4' } });