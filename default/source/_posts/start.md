---
title: 欢迎使用 Typecho
tags:
  - 搬家
  - 新的开始
url: NaN.html
id: .nan
categories:
  - 计算机
date: 2018-07-16 13:02:00
---

如果您看到这篇文章,表示您的 blog 已经安装成功.

今天正式搬家到typecho，zblog停更，将陆续迁移到此处

以后会在这里记录一些修改Typecho的教程

隐藏博主评论
------

在评论所在的位置，如本主题的`footer.php`中`Widget_Comments_Recent`所在位置  
然后将

    $this->widget('Widget_Comments_Recent')->to($comments);

改为

    widget('Widget_Comments_Recent','ignoreAuthor=true')->to($comments);

获取访客真实IP（相对）
------------

将以下代码添加到站点根目录的`config.inc.php`内

    //绕过 CDN 代理IP获取客户真实IP地址
    if(isset($_SERVER['HTTP_X_FORWARDED_FOR']))
    {
    $list = explode(',',$_SERVER['HTTP_X_FORWARDED_FOR']);
    $_SERVER['REMOTE_ADDR'] = $list[0];
    }

邮件插件通知模板
--------

部分仿QQ样式

    
        在援军博客的&nbsp;{title}&nbsp;有新的回复
        本邮件为{siteTitle}Mail自动发送，请勿直接回复如有疑问，请联系我 。
    
            {author_p}
            {text_p}
        {author}&nbsp;{time}
            {text}