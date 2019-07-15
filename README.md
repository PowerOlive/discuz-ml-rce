# dz-ml-rce.py ：discuz ml rce 漏洞检测工具
<br/><br/>

## 概述
<br/>
漏洞在于cookie的language可控并且没有严格过滤，导致可以远程代码执行，详情参考
<br/>

(discuz ml RCE漏洞重现及分析)[http://www.lsablog.com/networksec/penetration/discuz-ml-rce-analysis/]

<br/>
本工具支持单url和批量检测，有判断模式（只判断有无该漏洞）、cmdshell模式（返回简单的cmd shell）和getshell模式（写入一句话木马）。
<br/><br/>

## 需求
<br/>
python2.7<br/>
pip install -r requirements.txt 
<br/><br/>

## 快速开始
<br/>
使用帮助<br/>
python dz-ml-rce.py -h<br/>

![](https://github.cn/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce06.png)

<br/><br/>
判断模式<br/>
python -u "http://www.xxx.cn/forum.php" <br/>

![](https://github.com/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce03.png)

<br/><br/>
cmdshell模式<br/>
python -u "http://www.xxx.cn/forum.php" --cmdshell<br/>

![](https://github.com/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce04.png)

<br/><br/>
getshell模式<br/>
python -u "http://www.xxx.cn/forum.php" --getshell<br/>

![](https://github.com/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce05.png)

<br/><br/>
批量检测<br/>
python -f urls.txt<br/>

![](https://github.com/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce01.png)

<br/><br/>
批量getshell<br/>
python -f urls.txt --getshell<br/>

![](https://github.com/theLSA/discuz-ml-rce/raw/master/demo/dzmlrce02.png)

<br/><br/>

## TODO
<br/>
解决<br/>
SyntaxWarning: name 'total_count' is assigned to before global declaration<br/>
  global total_count<br/>
这个语法警告。。。。。。<br/>
该警告不影响正常使用。
<br/><br/>

## 反馈

<br/>
[issus](https://github.com/theLSA/discuz-ml-rce/issues)
<br/>
博客：http://www.lsablog.com/networksec/penetration/discuz-ml-rce-analysis/
<br/>
gmail：lsasguge196@gmail.com
<br/>
qq：2894400469@qq.com

