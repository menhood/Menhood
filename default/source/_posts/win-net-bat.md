---
title: Win更改DNS以及网关脚本
tags:
  - windows
  - bat
  - 脚本
  - dns
  - 网关
url: NaN.html
id: .nan
categories:
  - 计算机
  - 系统
date: 2019-01-19 09:52:00
---

公司内网用，设置DNS和网关服务器

注意
--

参数根据自己需要进行调整，我们公司三条线，网关路由分别为`192.168.1.1`；`192.168.1.2`；`192.168.1.3`；

    @ECHO OFF&PUSHD %~DP0 &TITLE 设置DNS和网关服务器 CM Made By Menhood
    
    
    color a
    
    for /f "tokens=4*" %%a in ('netsh interface show interface ^| findstr "已连接"') do set "ConName=%%~a"
    
    echo %ConName%>name.txt
    
    for /f "tokens=2 delims=:" %%i in ('ipconfig^|findstr "IPv4 地址"') do set "ip=%%i"
    
    echo %ip%>ip.txt
    
    :menu
    
    cls
    
    echo.
    
    
    echo   说明：
    
    echo.
    
    echo.  请点击右键，“以管理员身份运行”
    
    echo.
    
    echo   如果安全软件提示修改，请允许操作
    
    echo.
    
    echo   当前使用的网卡名是：[%ConName%]
    
    echo.
    
    echo.  当前IP地址为：[%ip%]
    
    echo.
    
    echo   本程序预置两组DNS服务器网关
    
    echo.
    
    echo   可多次切换尝试
    
    echo.
    
    echo   如果全都无法使用 请直接呼叫网管……
    
    echo.
    
    echo ======================================================
    
    echo.
    
    echo 请输入相应数字选择服务器并回车执行操作(使用说明往上翻)
    
    echo.
    
    echo ======================================================
    
    echo.
    
    echo   1，DNS：192.168.1.1  网关：192.168.1.1（电信光猫）
    
    echo.
    
    echo   2, DNS：192.168.1.2  网关：192.168.1.2（IP池较小）
    
    echo.
    
    echo   3, DNS：192.168.1.3  网关：192.168.1.3（400M带宽）
    
    echo.
    
    echo.  4, DNS：223.6.6.6 (阿里云) 网关：192.168.1.254（爱快软路由）
    
    echo.
    
    echo.  5, DHCP分配（全自动分配，可能会随机到较慢线路）
    
    echo.
    
    echo.  6, 重启网卡
    
    echo.
    
    echo.  7, 当前网卡信息
    
    echo.
    
    echo.  8, 还原网络设置
    
    echo.
    
    echo.  9, 自定义网关
    
    echo.
    
    echo   0, 退出程序
    
    echo =======================================================
    
    echo.
    
    echo.
    
    set /p user_input=    请输入数字：
    
    if %user_input% equ 1 (goto set1)
     
    if %user_input% equ 2 (goto set2)
    
    if %user_input% equ 3 (goto set3)
    
    if %user_input% equ 4 (goto set4)
    
    if %user_input% equ 5 (goto setdhcp)
    
    if %user_input% equ 6 (goto netrestart)
    
    if %user_input% equ 7 (goto ipconf)
    
    if %user_input% equ 8 (goto winsockreset)
    
    if %user_input% equ 9 (goto custom)
    
    if %user_input% equ 0 (goto ex)
    
    :custom