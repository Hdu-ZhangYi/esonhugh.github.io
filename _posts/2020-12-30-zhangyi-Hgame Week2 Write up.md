---
title: Hgame Week2 Write up
date: 2020-12-30 +0800
categories: [review]
tag: review
---
## **Week2 题解**

学习为主吧，大佬们太强了，个人也没有太多精力投入还要做开发。比赛要求要交题解顺便也发在知乎上。

## **WEB**

### **Liki的生日礼物**

根据hint：条件竞争，使用burpsuite先拦截购买时发出的包，然后使用intrader连续发送很多个包使得在服务器没有接收到购买成功之前多买几个券，兑换得到flag。

## **crypto**

### **WhitegiveRSA**

n,e,c已经给出，然后使用在线解质因数网站求出p,q，再求出d和m，最后找一个网上解rsa的python脚本跑一下得到flag。

## **MISC**

### **Tools**

就是使用四种工具（搜索压缩包名字的压缩方法就可以，密码在图片备注中）然后分别得到二维码的四分之一，扫描二维码后得到flag。

### **Telegraph：1601 6639 3459 3134 0892**

听音频发现是摩斯电码，然后使用au查看得到850hz，滤波

得到摩斯电码，抄下来翻译一下得到flag。

### **Hallucigenia**

使用stegsolve查看发现隐藏二维码，扫描得到base64，将base64编码转asc发现失败，猜测是将图片的二进制转成了base64编码，但是base64转16进制并且使用winhex并不能变成图片，查看asc后发现是需要反过来，反过来后再用winhex导出得到上下左右都颠倒的flag图片，简单处理后得到flag。