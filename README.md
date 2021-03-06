# 前言

弹指之间，从我开始接触编程至今已五年有余，从大一的懵懂少年到现在对计算机编程的一知半解,其中经历的酸甜苦辣实在是太多太多，不是一两句话就能说清楚的，这本小书在某种程度上也可以认为是我在学习计算机编程过程中的一些笔记。在线阅读页面见[计算机编程导论之FAQ](http://billryan.gitbooks.io/programming-notes/)，在线托管网址见 [billryan/programming-notes](https://github.com/billryan/programming-notes)，gitbook/github 大法好！

## 简介

本书内容的主要素材源于网络资源，主要以「碧蓝右耳」07年发布的 [C/C++ FAQ](http://www.vcgood.com/BBS/forum_posts.asp?TID=1559) 为蓝本进行创作，在此做了大量的整合，以便适应如今蓬勃发展的计算机大潮。这本小书浅析了一些计算机编程背后蕴含的思想，同时提供了不少方法论层面上的技巧——形而下者是也。目的是希望能为大家从全局去把握编程提供一定的思路，不为细节所困。本书是一篇散文，形散神不散——以编程为神，以各章节为形；它同时又是一篇科普文章，读起来自然不难理解，甚至是轻松幽默的，不过也不要对这本书期望过高，全书是从一个初学者的角度去感悟计算机编程的，功力自然是比不过各路大神大牛。另外需要指出的是，光看书是不够的，有些东西必须在你有一定实践经验后才能体会。

正如许三多当初选择在五班修路一样，我们也抱着同样的信念选择为大家奉献这么一本小册子，虽然自身水平有限，但我还是非常愿意和大家一起分享成长路上所获得的点点滴滴...

虽然几经修订，但是书中错误也在所难免，gitbook/git 是一个很好的平台，有任何不满意的地方你都可以自行修改。

## 为什么要写这本书

大约是在2009年，也就是我当年大一的时候，对计算机各方面了解都不多，上了很久的「计算机文化」和C语言也没搞懂编程到底是在干啥，只是觉得编程是一件很神奇的事，就像是魔法一般，不过雾里看花终隔一层，始终也未能亲身体验它的乐趣。那时多希望有个诸葛能扶一扶我这个阿斗，即便不是卧龙，凤雏也行嘛！我想现在一定也有那么一小撮人抱着这种想法，我只想对你说：「该醒醒了！现在不是立波梦话板块！」**在任何关键时刻，能帮助你的人只有你自己，即便你能找到愿意帮助你的人，那也要你花心思去找不是么？**

作为一个曾经的新手，我深知从新手过渡到老鸟需要拨开天空的乌云，翻山越岭... 正如你们所看到的，书店和网络上充斥着无数的编程教材，同时可以肯定的是，目前已经面世的教材，穷一人一生之力是不可能看完的。在这些书中，有大量的垃圾书，海量的平庸之作，还有少量的精品，而即使是这少量的精品，也不可能看全。既然书这么多，我为什么还要抽时间再来整理一篇呢？拿本书蓝本创作者碧蓝右耳的话来说，他还能多画几张效果图挣俩钱花呢。

情况是这样的，市场上的书虽多，但其中几乎没有几本是面向初学者的。这样的书是如此之少，以至于要去购买或是阅读到它们都是很困难的事。他们要么是一下子告诉你所有的事，好像你能在千分之一秒中突然从菜鸟变成高手，要么就是认为有些事你早就应该知道，拿你当高手看，导致你有一种赤身裸体被抛弃于猛兽横行的非洲旷野的感觉。你还没有穿上衣服走出帐篷，连刀子都没有摸过，他们就试图告诉你草原上有多少可以捕获的猎物以及他们的位置，告诉你几百种武器和毒药的使用秘籍，告诉你两百条以上的陷阱安放要领。你没有经过丝毫的练习，甚至还没有杀死过一只刚出壳的小鸡，他们就要你独自去捕猎数十头饥饿的狮子。这种看似荒谬的情况从过去持续到今天，至今仍然存在。这并不是说那些写教材的朋友都是傻瓜，他们面向的读者是专业的程序员。专业的程序员就像是猎人，他们更换语言就像猎人更换武器一样，不管他使用哪一种武器，捕猎的基本原理没有变化，变化的只是武器的使用方法。对一个成熟的猎人而言，再强调基本原理就没有必要，所以教材编者们对地球人都知道的一些事也就避而不提。

**一个成熟的猎人，他心中的捕猎知识是浑然一体的，武器的选择，野兽的习性，陷阱的安放，怎样做和为什么这样做都结合在一起，没有哪一部分可以独立出来。**一部分一部分的教给别人是极度困难的，要教就只能混杂在一起。编程的情况类似，它的知识体系是一个完整系统，谈到一个问题总会牵扯到另一个，只不过初学者平时遇到的问题太简单了，以至于没有感觉到一个完整知识体系的存在，学起来自然只能是云里雾里。

那么怎么写好一本面向新手的教材呢？个人认为除了介绍一些必要的基础和核心知识外，更重要的是知识背后的思维逻辑，功力欠佳的作者往往很难将其如庖丁解牛般解剖到深入浅出的程度。同时思维上的过程有时只可意会而不可言传，很少有人能很好地注意到思维过程的弥足珍贵。这两方面原因共同导致了好教材难以复制。

## 读者群

读完上边的那几段话你就应该能猜到本书的服务对象了。没错，就是为那些**毫无编程经验但对计算机感兴趣**的人准备的，甚至是**接触计算机不多**的人。这本书的目的也正在于此——**为新手介绍一些编程所必需的背景知识和有利的方法，以便于更好地去开启计算机编程这扇神奇的大门。** 如果你认为自己已有一定的编程经验，那你可以把你编程入门的这一段经历与大伙儿分享一下，完善一下这本书或者提 issue 等都是极好的 :)

## 约定、排版及其它

本书中所采用的语言和句法与正规书籍并不完全一样，中英文混排贯穿全文，有些例子只是为说明问题方便而假设，严谨性可能不够，偶尔还会耍点小聪明或是利用编程中常用的符号，例如用&&代表和，||代表或者，更多的东西等着你们自己去挖掘。在这次改版中我尽量做到中英文分离，不必要的中英文混排其实对读者并不太友好。

**“尽信书则不如无书”**——本书仅仅只是把各种资料收集之后再结合我的编程体验进行一次大的整合，但是水平毕竟有限，无法保证所有内容都是正确合理的，信口雌黄和胡说八道仅一步之差，部分评论我们尽量保持中立态度。本文引用参考的地方会尽量标注出处以供进一步查阅，同时希望大家阅读的时候带着怀疑的态度。

### 本书结构安排

首先说说书名吧——*Introduction To Programming*, 中文书名《计算机编程导论之FAQ》，顾名思义，**本书只准备讨论编程中最为底层最为基础的部分，让初学者能建立起一个自己的最小学习系统。**

FAQ——Frequently Asked Questions，也就是常见问题解答。这玩意儿通常是一些所谓的高手、前辈和公司的support为了节省回答新手的大量简单重复问题所耗费的时间精力而采用的一种手法。一旦完成，对于问与被问双方都轻松省事，效率甚高，实在是居家旅行杀人越货之必备良药。

### 鸣谢

<dl>
  <dt>Blue Auris</dt>
  <dd>中文昵称：碧蓝右耳，本书的原材料创作者，前言中提到的 C/C++ FAQ 正是出自他之手，我只是做了大量的组织和整合。可以说，没有他的 C/C++ FAQ 就没有这个合辑，谨在此致以崇高的敬意！</dd>

  <dt>[Bill Ryan](http://billryan.me)</dt>
  <dd>本书的发起者与主力作者之一，也是一位伪编程菜鸟，热爱计算机给人类生活所带来的便利和美。</dd>

  <dt>Everyone</dt>
  <dd>本书的最终完善者，没有大家的努力与汗水就没有这个优质的文档。</dd>
</dl>

### License(许可证)

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />如无特殊说明，本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。

### Contribution(贡献)

[billryan/programming-notes](https://github.com/billryan/programming-notes)

Pull requests or issues are both welcome!
