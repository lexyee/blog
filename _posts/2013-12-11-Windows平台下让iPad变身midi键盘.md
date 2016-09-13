---
layout: post
title: Windows平台下让iPad变身midi键盘
category: [musician, blog]
---

辞职之后，一度赋闲。本打算重新开始把琴好好学一学，结果右手因为练习过久不知轻重弹出了腱鞘炎，彻底废了；无奈之下转攻吉他，没想到左手也逢时地被菜刀切掉一块儿，按不了弦了。

两只手都不能用，于是只剩下电脑音乐可以一试；安了个cubase打算玩一玩，结果刚开头就发现输入音符的时候，如果没有外接midi键盘，用鼠标一个个点进去，那感觉真像是造了八辈子孽。

成千上万的midi外设买不起，但无所不能的ipad一定能解决这个问题。功夫不负有心人，在网上找到一篇[用iPad打造廉价midi键盘！「iPad+Pianist Pro+Mac+Logic Studio」](http://bbs.weiphone.com/read-htm-tid-1664135.html)，果然可以通过wifi，连接ipad与电脑，然后在ipad上使用相应模拟乐器软件，作为midi外设输入，就可以用于电脑的DAW编曲软件了，如此便从键鼠输入音符中得解放。

不过定睛一看，上面文章讲的是Mac + iPad组合，对使用windows的贫民而言完全不适用。（如果你用的是Mac，可以就此打住了，顺着上面链接看过去吧）

没关系，世界上最有折腾能力的就是穷人，所以研究一番之后，把 window + ipad打造midi键盘的方案记录如下，备案留底。


## 材料准备

```
Windows PC X 1；
iPad X 1；
用于Windows的DAW（数字音频工作站）软件，如Cubase；
用于Windows的rtpMidi软件；
用于iPad的midi模拟应用，这个在后文有介绍。
```
 
## 大体思路
确保pc与ipad处于同一网段；

1. Windows上下载安装rtpMidi，此软件使得windows可以与ipad间通过wifi连接，接收其发送的midi信号；
1. iPad安装钢琴、鼓垫等相应midi模拟应用，并与处于同一个网段的电脑建立连接；
1. 电脑上运行Cubase等编曲软件，iPad则作为midi键盘进行音符的录入。


## 设置篇

以ipad上的一款APP，pianist pro为例。

1. ipad中，进入pianist pro设置
![](/images/1.jpg)

1. 进入midi设置
![](/images/2.jpg)

1. 设置为网络连接
![](/images/3.jpg)

1. 电脑上，rtpMIDI的设置
     1. 安装并启动rtpMIDI [下载地址](http://pan.baidu.com/s/128QcB)
     1. 点击+号，新增一个会话
     1. 点击connect，显示会话连接成功
 见下图：
 ![](/images/4.jpg)

1. 回到ipad上，此时pianist pro显示连接成功。
![](/images/5.jpg)
 

## 使用篇

以电脑上的Cubase为例。

1. 启动Cubase，在cubase中进行相应设置
1. 注意声卡设置问题。既然是屌丝，默认你用的集成声卡，cubase中选择的设置应如下：
![](/images/6.jpg)

1. 新建MIDI轨道，设置midi输入为刚才在rtpMIDI中建立的会话名，输出则为你所使用的音源，或系统自带的GS软波表
1. 此时，弹奏iPad上的键盘，就能听到cubase里发出声音了。注意，这里应该会听到两个声音，一个来自输入到电脑再从电脑的Cubase里出来的音，一个是自身乐器应用发出的，只要把应用静音就好（在pianist pro的设置里将音量调为静音），使其成为一个不发声的纯粹的MIDI键盘
1. 在Cubase的钢琴卷帘窗中，使用步进模式，或者录音模式，然后在iPad上开始你的演奏吧！
（2）~（4）如下图所示：
![](/images/7.jpg)


## MIDI模拟应用推荐

上面说的pianist pro只能作为键盘输入使用，那么如果录制鼓点时该怎么办？有比它更好的应用吗？
答案是当然有！这一类应用有很多，以下一一罗列：

1. Wifi MIDI
支持键盘、鼓垫、控制器三种模式。无需设置，与rtpMIDI连接成功即可使用。
![](/images/8.jpg)
 

1. MIDI Contral
同样支持键盘、鼓垫等多种模式，但是界面有点花，花得让人有点无所适从。。
![](/images/9.jpg)


1. MIDI Studio
推荐。可惜鼓垫界面下显示的不是鼓组名称而是键位，不过可以通过重命名修改之。
![](/images/10.jpg)


1. Cubasis（强烈推荐！！）
真正强烈推荐的是 cubasis，这是用于ipad上的cubase，它可以通过键盘、鼓垫等方式进行录入，并且鼓垫模式下各鼓组名称已经标好，用过了才知道好。毕竟一个公司出的嘛。随便建立一个音轨，就可以使用键盘或鼓垫映射了。同样注意，要把音轨静音。

![](/images/11.jpg)

![](/images/12.jpg)

以上。

之后我用以上方法，试着做了第一个demo，Damien Rice 的《9 Crimes》之前奏。

### 点这里试听我做的 [9 Crimes前奏Demo](http://pan.baidu.com/s/1EewO1)

——
Anyway，这已经是很久很久以前的事了。

