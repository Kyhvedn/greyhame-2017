# Mobile/App

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-05-26:

> 匿名用户 提问：
弦哥，能分析下前段时间引起iOS微信crash的天线宝宝gif图么


FreeBuf 上已经有分析：

[一张GIF引发的微信崩溃 - FreeBuf.COM | 关注黑客与极客](http://www.freebuf.com/articles/terminal/135577.html)



这种畸形 gif 也是可以 fuzzing 出来的。


---

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-05-29:

> Oliver 提问：
余大大，最近一个月从Web安全转到了App安全，感觉测重点还是业务和服务端，余大大怎么看待app安全测试呢


挺好的，Web 安全的技能还能延续。

App 安全分为几大块：

1. 本地安全，如：权限控制、数据安全、第三方接口安全、恶意代码执行、代码保护等

2. 通信安全，如：SSL 证书机制、一些加密算法等，主要对抗中间人劫持

3. 云端安全，由于很多是走 HTTP 这种轻量级协议，所以 Web 安全的技能在这可以复用起来

那么做 App 安全测试这些都需要覆盖。还有一般情况下除了网络安全外，企业还会考虑业务安全，比如风控有关的，对抗羊毛党。

App 安全审计推荐个不错的自动化平台 Janus(appscan.io)，看看，可以开眼。另外我昨天发的那个“渗透技能树之利器”，里面有 Android 安全审计相关的平台或工具，可以也顺便了解看看。

工欲善其事，必先利其器。


---

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-06-06:

> 匿名用户 提问：
目前来说，有没有可能利用web安全技术，在手机上实现非交互式(或者一次点击)的获取物理地址。
有什么方案吗？


暂无非交互。


---

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-06-14:


__#资源#__

  Android 应用逆向入门

圈子有不少同学有问安卓安全/调试/逆向方面的知识，这里推荐这篇：


[https://www.evilsocket.net/2017/04/27/Android-Appl...](https://www.evilsocket.net/2017/04/27/Android-Applications-Reversing-101/)



这篇文章很不错，可以学到：

apk 基本知识，adb 基本命令，网络分析（用到了作者自己开发的 bettercap），静态分析，动态分析，动态注入等入门知识。

除了文中这些，我还有用到的如：Inspeckage、MobFS。

实战出真知。

<img src="https://images.xiaomiquan.com/FnpxBcd8M5Z8YfmmTHV_tusHlkbn?imageMogr2/auto-orient/thumbnail/800x/format/jpg/blur/1x0/quality/75&e=1843200000&token=kIxbL07-8jAj8w1n4s9zv64FuZZNEATmlU_Vm6zD:lz2IwMYoeus_E09sqOHOl57X0Ys=" width="50%" height="50%" align="middle"/>


---

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-07-16:


__#经验#__

想刷黑手的同学，重点推荐一加1代（淘宝买二手就好），一加2、3、3T也行，如果你钱多的话。现在一加最新是5（没有4），但是5还不建议去刷，官方没出兼容方案，如果你不怕，可以自己折腾。

黑手可刷机型完整清单可以看官方这个链接：


[Home · offensive-security/kali-nethunter Wiki · Gi...](https://github.com/offensive-security/kali-nethunter/wiki)

 

一旦有一加5可刷黑手的新消息，我会乘势好好跟进并分享黑手使用经验。



...

<img src="https://file.xiaomiquan.com/b2/3c/b23c795737adee8dc13ad0c866f32f05b6b4bdd374a2cd62d6fa8eee0396f1a4.jpg" width="25px"/> __K3vi__: ZUK Z1也可以刷

...

---

<img src="https://file.xiaomiquan.com/60/64/60640ca1fb2dfb0131ee8573a60ad8d86961495d76e4d6f025927ab4ce652fcb.jpg" width="25px"/> __国勇@ATToT__ on 2017-08-29:

有一天我一个做程序员的朋友收到一条短信，内容是“看看我们之前的回忆影集
[http://118.184.51.172](http://118.184.51.172)”，看到这个内容，顿时感觉是一条诱惑短信，一打开网站，为一个 apk 文件下载地址。文件引起了我的兴趣，下载后进行了编译分析，发现主要是获取用户短信、电话簿等信息，通过短信或邮箱的方式发送给控制者，同时启动了多个服务，用于长期监听用户的短信，并可以通过指定手机号码下发指令到受害者手机上进行长期的远程遥控。

从 apk 用来接收邮件的邮箱来看，2017-08月份查到有 2 万多人已安装了，而这些大部份是发生在 2017-08-18号。

感觉可以做的事情就很多了，现在的银行等好多互联网服务依赖于短信通知，如快捷支持、验证码、注册、找回密码等等，从这个 apk 用于接收邮件的邮箱可以看出，有多条敏感短信信息。

源码分析过程中，主要涉及了 android 的反编译、android 开发基础知识已及 java 基础知识。


__分享文件:__

[一款 android 木马分析.pdf](https://github.com/ChrisLinn/greyhame-2017/blob/master/shared-files/%E4%B8%80%E6%AC%BE%20android%20%E6%9C%A8%E9%A9%AC%E5%88%86%E6%9E%90.pdf)


...

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__: 可以对指定受害者进行长期控制 这个有意思。

<img src="https://file.xiaomiquan.com/60/64/60640ca1fb2dfb0131ee8573a60ad8d86961495d76e4d6f025927ab4ce652fcb.jpg" width="25px"/> __国勇@ATToT__ replies to <img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__: 是的，通过短信发送命令给手机，手机负责执行。

<img src="https://file.xiaomiquan.com/58/e0/58e0e911c15f99cfb8994d9f484be21c5966b3c50e4241e5e2617599f157c67c.jpg" width="25px"/> __5u9ar__: 想问下如何查到的接收邮箱用户安装量？

<img src="https://file.xiaomiquan.com/60/64/60640ca1fb2dfb0131ee8573a60ad8d86961495d76e4d6f025927ab4ce652fcb.jpg" width="25px"/> __国勇@ATToT__ replies to <img src="https://file.xiaomiquan.com/58/e0/58e0e911c15f99cfb8994d9f484be21c5966b3c50e4241e5e2617599f157c67c.jpg" width="25px"/> __5u9ar__: 反编译后，密码就在代码里面

<img src="https://file.xiaomiquan.com/b4/60/b460e6ec9b8123ffccbe6825deec13b1b9f636a3925194d65240bb559366a436.jpg" width="25px"/> __Canng__: 这不就是Android源码吗？入门水平

<img src="https://file.xiaomiquan.com/60/64/60640ca1fb2dfb0131ee8573a60ad8d86961495d76e4d6f025927ab4ce652fcb.jpg" width="25px"/> __国勇@ATToT__ replies to <img src="https://file.xiaomiquan.com/b4/60/b460e6ec9b8123ffccbe6825deec13b1b9f636a3925194d65240bb559366a436.jpg" width="25px"/> __Canng__: android 基础知识


...

---

<img src="https://file.xiaomiquan.com/0a/bd/0abddfca718a9f30c1e29e53617f76be9cc86b9fe12b387e9899e75a3427aeec.jpg" width="25px"/> __豆@ATToT__ on 2017-10-12:

一加氧OS窃密事件，没事给自己的设备做做流量分析，也许就发现。。。
[OnePlus OxygenOS built-in analytics](https://www.chrisdcmoore.co.uk/post/oneplus-analytics/)



<img src="https://file.xiaomiquan.com/cb/2c/cb2c84dd33d174bb8d52e92a3356f6a6a8c27645825f4f79341eb1581184c767.jpg" width="50%" height="50%" align="middle"/>


---

<img src="https://file.xiaomiquan.com/96/86/9686aeac0faa9aa0efc8cc53e1617273dd5e53e7a0425b9f06b68f806f03ca15.jpg" width="25px"/> __余弦@ATToT__ on 2017-11-13:


__#资源#__

对 Android 安全感兴趣的实际上也可以看看这个，懂开发是做好安全研究的必备一步：


[重磅登场！中文版 Android 开发教学视频终于来啦！](http://mp.weixin.qq.com/s/pbnzmoI1h_Bc8qSebp-xZQ)



Google 为中国开发者特别创立的视频频道，真是福利。



...

<img src="https://file.xiaomiquan.com/1b4/12/b412a4b8821a304f3f60e636b08f26953e27f32c187cb1281f487fe9efd52c14.jpg" width="25px"/> __Not__: 懂开发是做好安全研究的必备一步，懂这句话的人应该都已经过了入门坑了吧[捂脸]


...

---
