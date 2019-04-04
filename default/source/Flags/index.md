---
title: Flags
url: NaN.html
id: .nan
date: 2018-07-21 22:08:00
---

/\* Reset */ *, *:after, *:before { -webkit-box-sizing: border-box; -moz-box-sizing: border-box; box-sizing: border-box; } /* Clearfix hack by Nicolas Gallagher: http://nicolasgallagher.com/micro-clearfix-hack/ */ .clearfix:before, .clearfix:after { content: " "; display: table; } .clearfix:after { clear: both; } .demo{ padding: 2em 0; background: #dbc1af; height:500px; } .progress{ height: 7px; background: #e3e3e3; border-radius: 0; box-shadow: none; margin: 40px 0 80px; overflow: visible; position: relative; } .progress .progress-title{ padding: 1px 10px; margin: 0; background: #393a3d; border-radius: 5px 0 0 5px; box-shadow: 0 7px 7px rgba(0,0,0,0.4); font-size: 18px; font-weight: 700; color: #fff; text-transform: uppercase; position: absolute; top: -13px; left: 0; z-index: 1; } .progress .progress-title:after{ content: ""; border-left: 17px solid #393a3d; border-top: 17px solid transparent; border-bottom: 17px solid transparent; position: absolute; top: 0; right: -17px; } .progress .progress-bar{ box-shadow: none; border-radius: 0; position: relative; -webkit-animation: animate-positive 2s; animation: animate-positive 2s; } .progress .progress-bar:after{ content: ""; width: 20px; height: 20px; border-radius: 50%; box-shadow: 0 5px 5px rgba(0,0,0,0.6); background: #fff; position: absolute; right: -5px; top: -6px; } .progress .progress-value{ width: 45px; height: 30px; line-height: 30px; border-radius: 3px; background: #393a3d; box-shadow: 0 5px 5px rgba(0,0,0,0.4); font-size: 15px; font-weight: 700; color: #fff; text-align: center; position: absolute; bottom: 30px; right: -17px; } .progress .progress-value:after{ content: ""; border-top: 7px solid #393a3d; border-left: 7px solid transparent; border-right: 7px solid transparent; position: absolute; bottom: -7px; left: 35%; } .progress.green .progress-bar:after{ border: 5px solid #21da9a; } .progress.pink .progress-bar:after{ border: 5px solid #ff1170; } .progress.blue .progress-bar:after{ border: 5px solid #294bdc; } .progress.yellow .progress-bar:after{ border: 5px solid #ffa900; } @-webkit-keyframes animate-positive{ 0% { width: 0; } } @keyframes animate-positive{ 0% { width: 0; } } 剪辑 50% AE 20% C4D 30% 拍摄 33% 文稿 15%

网上扒来的，直接扔在typecho的默认编辑器里了，虽然丑先用着 :huaji21:

    !!!
    
    /* Reset */
    *,
    *:after,
    *:before {
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
    }
    
    /* Clearfix hack by Nicolas Gallagher: http://nicolasgallagher.com/micro-clearfix-hack/ */
    .clearfix:before,
    .clearfix:after {
        content: " ";
        display: table;
    }
    
    .clearfix:after {
        clear: both;
    }
    .demo{
        padding: 2em 0;
        background: #dbc1af;
    }
    .progress{
        height: 7px;
        background: #e3e3e3;
        border-radius: 0;
        box-shadow: none;
        margin: 40px 0 80px;
        overflow: visible;
        position: relative;
    }
    .progress .progress-title{
        padding: 1px 10px;
        margin: 0;
        background: #393a3d;
        border-radius: 5px 0 0 5px;
        box-shadow: 0 7px 7px rgba(0,0,0,0.4);
        font-size: 18px;
        font-weight: 700;
        color: #fff;
        text-transform: uppercase;
        position: absolute;
        top: -13px;
        left: 0;
        z-index: 1;
    }
    .progress .progress-title:after{
        content: "";
        border-left: 17px solid #393a3d;
        border-top: 17px solid transparent;
        border-bottom: 17px solid transparent;
        position: absolute;
        top: 0;
        right: -17px;
    }
    .progress .progress-bar{
        box-shadow: none;
        border-radius: 0;
        position: relative;
        -webkit-animation: animate-positive 2s;
        animation: animate-positive 2s;
    }
    .progress .progress-bar:after{
        content: "";
        width: 20px;
        height: 20px;
        border-radius: 50%;
        box-shadow: 0 5px 5px rgba(0,0,0,0.6);
        background: #fff;
        position: absolute;
        right: -5px;
        top: -6px;
    }
    .progress .progress-value{
        width: 45px;
        height: 30px;
        line-height: 30px;
        border-radius: 3px;
        background: #393a3d;
        box-shadow: 0 5px 5px rgba(0,0,0,0.4);
        font-size: 15px;
        font-weight: 700;
        color: #fff;
        text-align: center;
        position: absolute;
        bottom: 30px;
        right: -17px;
    }
    .progress .progress-value:after{
        content: "";
        border-top: 7px solid #393a3d;
        border-left: 7px solid transparent;
        border-right: 7px solid transparent;
        position: absolute;
        bottom: -7px;
        left: 35%;
    }
    .progress.green .progress-bar:after{ border: 5px solid #21da9a; }
    .progress.pink .progress-bar:after{ border: 5px solid #ff1170; }
    .progress.blue .progress-bar:after{ border: 5px solid #294bdc; }
    .progress.yellow .progress-bar:after{ border: 5px solid #ffa900; }
    @-webkit-keyframes animate-positive{
        0% { width: 0; }
    }
    @keyframes animate-positive{
        0% { width: 0; }
    }
    
    
    
    
                
                    
                        剪辑
                        
                            50%
                        
                    
    
                    
                        AE
                        
                            20%
                        
                    
    
                    
                        C4D
                        
                            30%
                        
                    
    
                    
                        拍摄
                        
                            33%
                        
                    
    
                                    
                        文稿
                        
                            15%
                        
                    
                
    
    
    !!!