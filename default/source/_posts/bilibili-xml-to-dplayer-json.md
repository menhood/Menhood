---
title: 哔哩哔哩弹幕xml批量转json（DPlayer支持的格式）
tags:
  - DPlayer
  - php
  - 哔哩哔哩
  - 弹幕
  - 格式
  - 转换
url: NaN.html
id: .nan
categories:
  - 前端
date: 2018-11-08 15:30:00
---

php正则替换，可能很慢且很卡

先上代码
----
```php
<?php
header("Content-type: text/html; charset=utf-8");
function ReplaceSpecialChar($C_char) {
        //过滤特殊字符
        $C_char = HTMLSpecialChars($C_char);
        //将特殊字元转成 HTML 格式
        $C_char = str_replace(",","，",$C_char);
        //替换英文逗号,
        $C_char = str_replace("<","《",$C_char);
        //替换英文小破折号<
        $C_char = str_replace(">","》",$C_char);
        //替换英文小破折号>
        $C_char = str_replace("'","~",$C_char);
        //替换英文单引号 '
        $C_char = str_replace("{","《",$C_char);
        //替换英文大括号{
        $C_char = str_replace("}","》",$C_char);
        //替换英文大括号}
        $C_char = str_replace("(","《",$C_char);
        //替换英文小括号(
        $C_char = str_replace("）","》",$C_char);
        //替换英文小括号）
        htmlentities($C_char,ENT_QUOTES);
        //替换英文双引号 "
        return $C_char;
        //返回处理结果
    }
    
function x2j($path) {
    $preg_p = '|<d p="(.*?)">|i';
    $preg_d = '|">(.*?)<\/d>|i';
    $preg_id = '|<chatid>(.*?)<\/chatid>|i';
    $fopath = 'xml/'.$path['basename'];
    $contents = file_get_contents($fopath);
    preg_match_all($preg_p,$contents,$p);
    preg_match_all($preg_d,$contents,$d);
    preg_match_all($preg_id,$contents,$id);
    $arrlength = count($p[1]);
    
    for ($i = 0;$i < $arrlength;$i++) {
        $pieces = explode(",", $p[1][$i]);
        $type = 0;
        if ($pieces[1] === '4') {
            $type = 2;
        } else if ($pieces[1] === '5') {
            $type = 1;
        }
        $addtime=0;
        $minustime=0;
        $time=floatval($pieces[0])+$addtime+$minustime;
        $data .= '['.$time.','. $type.','. $pieces[3].',"'. $pieces[6].'","'.ReplaceSpecialChar(preg_replace('/[\\x00-\\x08\\x0B\\x0C\\x0E-\\x1F-\\\]/','',$d[1][$i])).'"],';
    }
    $newstr = substr($data,0,strlen($data)-1);
    $fstr = '{"code":0,"data":['.$newstr.']}';
    $fwpath = 'json/'.basename($path['basename'],'.xml').'.json';
    $res = file_put_contents($fwpath,$fstr);
}
function fRename($dirname) {
    if (!is_dir($dirname)) {
        echo "{$dirname}不是一个有效的目录！";
        exit();
    }
    $handle = opendir($dirname);
    while (($fn = readdir($handle)) !== false) {

        if ($fn != '.' && $fn != '..') {
            echo "<br>正在将：".$fn."\n\r";
            $curDir = $dirname.'/'.$fn;
            if (is_dir($curDir)) {
                fRename($curDir);
            } else {
                $path = pathinfo($curDir);
                echo "转换成:".basename($path['basename'],".xml").'.json'."\r\n";
                x2j($path);
            }
        }
    }
}
fRename('xml/');
echo "<br><strong style='color:green'>Done!</strong>";
exit();
?>
```