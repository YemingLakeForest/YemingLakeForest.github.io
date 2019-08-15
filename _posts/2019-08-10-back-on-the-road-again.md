---
layout: post
title:  "Back on the Road Again 重新上路"
date:   2019-08-10 16:11:16 +0100
categories: Rants_and_Scribbles
comments: true
---
直至2019年第三季度，我参加工作正好7年。<!--MORE--> 在'7'这个魔法数字面前，以及人生第二次职业转型的节骨眼上，
我是时候稍对过往7年的工作事业做个简短的总结了。这篇博文主要是写给我自己，特别是7年后，或是 ``while(isAlive) {age += 7;}``
 年后的自己看的。你若无意逛了进来，而又对此博文有所感触，欢迎留言。

一改本站其他博文的风格，此文是以中文写作的。选择中文的原因是，在谈论'事'和'物'时，我喜欢用工作语言（英文）表达。
但在讲'人'的时候，而这个'人'又是自己，用母语表述最好不过。为了本站观感的一致性，我会在本文正文之后附上英文译文。

本文略长，一万来字，慢慢看。

&nbsp;

## 零
----
自2011年从 Imperial 硕士课程毕业以后，我不免俗地和很多毕业生一样迷茫一段时间。那年保守党刚上台执政，缩紧移民政策。
时任内政大臣梅姨取消了上届政府设立的 Post Study Work 签证。这意味着我并没有那奢侈的两年时间在伦敦找工作。
时不我待，我没法迷茫太久。我跟打鸡血似的投报了伦敦各大投资银行的应届毕业生录取计划。乱面了几次之后我逐渐掌握了投行面试的套路，
后陆续收了三间银行的 offer。

在权衡得失利弊后，我选择了三间银行中其中一间，兴高采烈上班去了。

&nbsp;

## 壹
----
2012年秋天，我作为毕业生加入了伦敦花期银行的 ICG Global Markets Technology（企业客户部全球市场交易技术部门）。你不用 Google 了，
你搜也搜不到，大公司的企业架构名称总变来变去的。简单来说这是投行部技术部门。干'金融码农'。

我不同意也不喜欢'码农'这个描述。'农'这个字有劳动密集型工作的涵义（没有诋毁农业工作者的意思）。而软件工程师的核心任务,
恰恰是消除劳动密集型的工作。如果你当软件工程师，当成了个'农'，净干些重复劳动，那你这工程师就别当了。

从2012年作为应届生加入公司到2017年底跳槽，我在公司效力了5年有余。5年的经历全写出来写10篇文都不够。总结下来，我会以**做了什么**，
**得到什么**，**为什么离开**这三方面说说在这间企业这几年的喜怒得失。

#### 壹·零
__做了什么__

做了些什么最难写。

难写当然不是因为不知道自己做过什么，不然把直接简历复制黏贴来就好了。难在于如何在做过的芸芸众项目里提炼一些出可圈点的，
有持续性系统性贡献的遗产。

我在公司的大部分时间任职于期货期权交易清算抵押管理技术部门（Futures Clearing and Collateral Management, 简称 Fucc'm，
真的，我座位头顶天花板上挂的牌子就这么写的），服务于期货期权电子交易及风险控制业务。你看这部门名称不能硬译，译出来也白瞎。

刚进组的时候，我的天，整个技术架构就一西部，等着我去大开发。持续集成约等于没有，自动部署没有，代码仓库是SVN。记得第一次观摩同事做部署，
我看着他，点开 Windows Remote Desktop，登进生产环境，把本地 maven 构建的 zip 包（你没看错）手动地拉到生产环境的桌面。我看得一愣一愣的。
他接着手动解压该 zip，把子文件一个个给拉到部署目录里。我惊为天人。

这当然不是个事儿。我在组内的几年时间里，在保证项目进度输出的前提下，对下辖软件系统的 SDLC 成熟度持续不断地进行着改进。
把代码仓库从 SVN 移到了内部主持的 git server，再移到了全银行共用的 Bitbucket。最初我们的软件是直接部署在裸金属（bare metal）服务器上的，
我陆续地把它们移到虚拟机，而后又全部移植到公司的内部云里。我陆续地把持续集成，自动部署，自动测试，静态代码质量分析，代码质量把关等系统一一建立。
而后，我又在各不同业务领域内的项目标准化了技术骨架和构建方法。这让后代陆陆续续加入的工程师们可以很舒服地在我们的系统上进行开发，
同时保证着在这框架内产出的软件的质量相对高。

一言以概之，我在这做的最重要的一件事，是向所管辖的系统**注入了可持续地，往横向扩展的 DNA**，并且把它这一定程度上传播到部门内其它的姐妹系统中。
那段时间公司爱搞软件成熟度模型评估（software maturity model scorecard），我的系统总能出现在大部门的榜单上。这也是很能让我的老板脸上有光的。
我当时的小老板还以此作为他的'政绩'之一拿去搞升职了，哈哈哈哈，笑死我了。

至于在业务上，我留下的遗产是，**把一个服务数名内部员工的软件系统，扩展到可以满足内外部客户需求的软件服务**。
这系统最早就只安装在了几个风险管理人员的台式机上，追踪监测客户的维持保证金（maintenance margin）需求。在我离开前，
系统已经被反转成能满足实时即席保证金运算的服务，并且把这服务公开在了公司门户网站平台上，供外部客户使用。因为这个项目的交付，
公司赢得了新加坡一政府背景投资机构的业务。这在当时还是很能让不少人乐呵的一个成绩。虽说在投行环境里，技术部门只能切到一小块蛋糕，
然而我作为新人完成这些任务，还是得到了各方面的回报。这就很自然地转接到了下一个章节，看看我这些年得到了什么。

#### 壹·壹
__得到什么__

白岩松同志说过，[失败不是成功之母，胜利才是成功之母](http://news.ifeng.com/a/20160907/49929707_0.shtml)。对此我深表认同。
这些年我目击并参与了软件项目从无到有，从弱到强的全过程。了解了如何把客户和交易员的想法，点子，变成稳健，可扩展的系统。
这些备受瞩目项目的成功交付，让我建立起在本行业立足的信心。能以项目管理，人事主管，技术骨干的身份参与这些项目，
并和(哥|姐)几个撸起袖子拼得一些成绩，这份心理优势（mentality）可以让我有底气信心揽下任何同等规模，甚至更复杂的开发任务。

在公司的大部分时间，除了人事和一些官僚的事物外，我很少需要和我的直系领导汇报。我直接对我们的客户负责。
自主性强的环境也是让我能够快速成长的重要因素。

那几年这企业阶梯我攀爬地可是相当顺利，火箭似地升，能升职的机会全都把握住了，在第四年升成了 VP。一部分的原因在于我搭上了职称膨胀的快车，
同时也遇到了愿意栽培我的好领导。对这位有知遇之恩的领导，到今天我还是非常地心存感激。

我当组长那年，领导了一帮散落在世界各地的小弟们。为什么会这样呢？我们这样的大企业爱搞一些'卓越中心'（centre of excellence, 简称 COE）。
这什么东西？COE 是廉价劳工地点（cheap location）的政治正确的称呼。这些 COE 是公司为了节省成本，在亚非拉各地成立的办事机构。

我在北爱 Belfast 的 COE 里有个小弟（其实该小弟比我年纪还大）。这大小弟后来转组，临走前跟我说，我不会忘记你教过我的东西。
这让我膨胀了好一阵子。

非要总结的话，这几年我得到最多的是成长。如果非要再说点什么，就是获得了 title （职称）。有某大牛说过，
[职位，title 都是虚的](https://coolshell.cn/articles/10688.html)。那是扯淡。要真是虚的，让你把自己 title 给免了试试？
这职称本身固然没有什么实际意义，也没人会真的管你叫黄VP的。但 title 背后代表着的你在行业内的江湖地位（gravitas）却是实打实的。
各大行对 title 都有严格的薪金水准定位，而且有了 title 找工作上便利也不少，新的公司总得给你对应上你曾获得的职称。

好哇，你看你说这些，顺风顺水，好得不能再好了，你干嘛跳槽呢？你会这么问。别急，吐槽马上就来了。

#### 壹·贰
__为什么离开__

终于到这章节了。写这么久就等着写这个。

干得这么好干嘛要走啊。身边的人，包括家人，太太，都会对我要跳槽的决定感到疑惑。事实上，在公司后面的这几年，我的心理状态越来越糟糕。痛苦，煎熬，悲怆
（好像其实也没那么夸张）。有一点是确定的，在公司最后的一年，我吃了秤砣子，要离开的信念相当笃定。

为啥呢？三点。

第一，__*那是跳槽的最优化时机*__。那年我刚升上了 VP。在银行里，VP （副总监）这个职称，一般正常人，俩眼睛一嘴俩胳膊俩腿，过个几年总能搞上去。
再往上要变 Director 就需要人脉年资各种的积累了。我并不想在这蹲太久。再者，英国的移民政策允许连续工作了5年的外国人申请永久居留，
就业情况不受限制。这个时候刚好移民监也坐完了，心里的什么想法也应该在这个时候有了。

我在这个企业连续工作了5年，虽说每年都会涨薪不少，但因毕业生的基数低，我那时的工资水平是远低于市场价的。有天我手贱，
跑去 Glassdoor 评估自己的工资水平。谁知一输入，哎？本银行的 Vice President 薪金统计数据的下界，怎么就变成了我的工资了呢？

你说这咋整？

第二，在公司最后这一两年我的技术水平和业务知识提升得越来越慢。交到我手上的任务变得越来越同质化。当任务日渐趋同，我内心不安全感与日俱增。
再这么搞下去，我这技能会越来越与市场需求不相干。__*是时候多样化自己的经历和技能了*__。

诚然，在公司积累下的人脉年资，让我在这企业逐步上升，搞个 Director 当当不是没可能。可是这么搞，我就是在做空波动率（short volatility）。
什么意思呢？如果我决定待在公司不走，我就是在期待周遭一切趋于静止，公司不会裁员，业务部门不会被砍，人脉环境不会变动，业务市场不会萎缩。
这些外部条件一旦渐渐消失，我屁股热着的这个位置的处境就会越发危险。继续这样下去我就变得脆弱。
而我要把自己变得[反脆弱（anti-fragile）](https://www.amazon.co.uk/Antifragile-Things-that-Gain-Disorder/dp/0141038225)，
我得强化自己技能的宽度硬度，做多波动率（long volatility），别让个什么风暴把自己给整个推了。

为什么在后来我的能力提升慢起来了呢，这很大程度上归咎于公司一些制度性，哲学上的问题。你看，我一下就把这格局拉这么大了。
下面我说说这都是些什么制度问题。

我离开公司的第三个，也是最重要原因在于，这些年来，我看清了这个公司，在哲学的层面上，
[像陈皓同志说的](https://coolshell.cn/articles/17737.html)，__*偏向通过管理解决问题，而不是通过技术解决问题*__。
这是我最不能苟同，甚至痛恨的一点，也是我在公司后期痛苦煎熬的根本源泉。

体现在哪里呢？作为一个基层干部，我被公司产生的各种匪夷所思的官僚形式主义工作掩埋得严严实实。各种奇奇怪怪的 spreadsheet（报表）要去填。
每次部署前至少搞一两天文件，催七八个签名。你永远不知道哪会突然蹦出来一个，你听都没听过的部门来的人，训你一顿说你这些文件没做好。
每周三都会收到一份抄送给各大佬的文件完成情况评估报告，你要是哪份东西填晚了，就会出现在大领导的'淘气表'上。我经常会为这些愚蠢透顶的事，
殚精竭虑。回想起来，我能搞妥这么多文件同时又保证了项目开发进程，真是个壮举。

你一定会说，这是大企业的通病。你如果适应不了它，就下功夫改良它。对于这种观点，我原则上是认同的，但你先别急，请听我讲三个故事。

第一件事是关于银行内部关于密码存档文件管理的问题。公司每年都会找 KPMG 的技术审计来评估软件系统的健康程度。喂，KPMG 诶。
虽说我们投行业的技术不一定能看齐 GAFAM (Google, Amazon, Facebook, Apple and Microsoft），但也轮不到四大的外行来给评估把。
当然外部审计总是必需的，KMPG 的人来找，还找出来了一些问题。其中一个问题，是一些系统的密码裸存在了文件里。

这个问题在我看来来根本不是问题。有人认为裸存密码会被有恶意的程序员使用来搞破坏。这个看法很蠢，如果程序员有需要，可以有无数的方式搞破坏。
他们又说，这会让有恶意的外部人员更容易入侵银行系统。这也是外行看法，都入侵到你内网了，黑客还要看你密码？

当然这只是我的看法，稽核部（Compliance）的外行们可不这么看。外部审计出问题了啊，稽核同事们可慌了去了。咋办呐？赶紧上马一个密码管理项目吧。
后来他们上了这么一个密码管理系统，以后密码都不分散在各地储存了，你们要设密码，派人登入我们的系统把密码敲进来，然后把它忘掉（真的）。
系统运行时通过访问一个 REST API 实时获取你的密码。听闻这个系统，我的内心无比崩溃。

![Face Palm](/assets/face-palm.jpg)

这在我看来完全就是在自慰（masturbate），让自己舒服点，实际作用一点儿没有。你真的认为设立后忘记（set and forget）可行？
REST 放送的内容真的安全？全公司的系统都访问你的 API，你确定不会被DoS（拒绝访问）？

好了，密码系统确立好了，是时候赶鸭子上架了。稽核部定了一个死线，规定全公司系统必须按时将密码移交。果不其然，一些先行者们用上这系统之后，
坏事了，生产环境访问 REST API 的时候卡住了，拿不到密码。气急败坏的先行者们，声泪俱下地把这密码系统批判了一通，这不是活活让尿给憋死了吗？
然后这系统就没有然后了。

密码管理方法有很多，我认为最有效的方式是不设密码。没有密码不代表没有认证，有很多无密码的方式可以实施系统认证。
可惜公司希冀通过管理方式，让外行人搞一刀切，搞砸是在所难免的。

第二个故事也很好玩儿。

有一天，一个内部电话打了进来，对方是一位操着东欧口音的阿姨（估计是布达佩斯'卓越中心'的）。她说，我们监察到，你的系统有通过 ftp 传输数据。
你给我个 deadline（死线），什么时候把 ftp 管道移植到 sftp 上呢？我心里一堆问号，这又搞个什么大龙凤？后来了解到，是日本分公司的某部门，
用 ftp 传输泄漏了数据。上头很生气，决定又来一次一刀切，把所有 ftp 传输管道都给毙掉。

我心里好笑极了。诶，我是在访问 CME（芝商所）的公开交易数据哎，为什么要用 sftp ？阿姨不知道听懂了没有，接着问，那你什么时候能解决呢？
我多精一人啊，当然不会和她进行降维交流。我后来和她说，CME 数据目前只提供 ftp 访问方式，如果你必须要做 sftp，我可以和他们联系，
问个移植到 sftp 的要价，你看到时这笔支出应该记在哪个部门的帐上呢？

阿姨后来就没再烦我了。

还有第三个故事，这件事是压垮骆驼最后的几根稻草之一。

前面说过，部署系统前要搞好几天的文件工作。这包括填个十几页的部署预案表格。谁有空填那个呀。那时后我就让我的一位小弟，
用 selenium WebDriver 写了个自动填表系统，一键完成这些傻工作。乐呵了没几天，我们被告知这自动填表系统不能用了。
原因是这消息传到了系统部署管理部门耳朵里（没错，有这么个部门，我一直认为这些部门是用来创造就业的）。他们说你们这些人，
怎么能这样绕过部署规范流程呢？

![Face Palm](/assets/face-palm.jpg)

平心而论，这间投资银行的确是个很好的企业。在这企业里我也遇到了很多在其领域卓越出众的人。**公司内部有个宣言--我们是拿着银行牌照的技术公司
（we are a technology firm with a banking licence）。我认为它没能实践这句话。**

看到这里，你也应该了解了。这事情我是赢不了的。你若果不能选择输赢，你至少还能选择战场。我要重新选择战场了。

&nbsp;

---
> 中场休息

读累了，欣赏一段舞蹈表演吧。

![Spiderman Dancing](/assets/spiderman_dancing.gif)

这个跃动的蜘蛛侠也是有典故的。当年我在所编写的一套系统里，用了这个蜘蛛侠跳舞的 gif 作为系统的加载缓冲图片。你看他多有趣啊。

当然不是所有人都这么看。这可爱的蜘蛛侠被责令整改了。为了抗议，同时也为了减少工作量，我把新的正常的加载缓冲图片也命名为 
``spiderman_dancing.gif``。至此，我们系统内所有缓冲图片都叫``spiderman_dancing.gif``。

---

&nbsp;

## 贰
----
在2017年第三季度我开始密集面试，准备跳槽。那年正值比特币泡沫，各种虚拟币火的一比。区块链创业公司这又一家那又一家。火到什么程度呢？
我那年跑去面了个区块链公司，待遇还没我之前好，猎头还信心满满地说，你来这呀，学点区块链，这技术市场可追捧了。好些人降薪都想进来学啊不拉不拉。

带着大公司的惨痛记忆，这轮求职我主要把目标定在中小公司，特别是买方金融机构上。又乱面了几次后，我再一次掌握了面试的套路。又拿了仨 offer。
这次我选了间小型技术驱动的买方自营交易机构（systematic prop shop）。这次跳槽，简直一下子从光谱的一端直接抛掷到另一端，要多极限有多极限。

这家公司，怎么说呢，很有趣。你看啊，我用了'有趣'这两个字。在英语国家呆过的同志们应该会感受到，'有趣'是个礼貌性的形容词。
我这么形容也有那么一点儿这样的想法。同时，用'有趣'的字面意义来形容我这间公司，也非常恰当。

同样的，我以**做了什么**，**得到什么**，和**为什么离开**这三方面回顾下我在这间公司的经历。

#### 贰·零

__做了什么__

我做了什么呢，要先看这间公司都做些什么。

这间公司长得很像 The Big Short (电影 -- 大卖空）里哥几个那办公室，就是到处架满屏幕那个。公司很小，你进去一眼整个公司就能看下来。
公司员工一共十二个人左右。为什么我说'左右'呢？我刚刚加入的时候，公司里软件工程师一共五个，还有仨交易员，俩矿工（quantitative analysts）。
还有一些人事，助理之类的兼职人员，连 COO（首席运营官）都是兼职的。加上创始人兼 CEO ， 十二人左右。

公司这么小，愿景却很远大。公司的使命（mission statement）是什么呢？我试着表述一下。

我司主要交易的金融工具是挂牌期权（listed options）。期权这东西，你可以看成像是买了份保险，以有限损失投博无限利益嘛。买保险呢，
你付的保险费当然是和保险期限时长正相关的，投保时间越长，保费越高。投射到期权上来看，履约日期（expiration date）越来越近，
你这受这期'权'保护的时间就越短，价格也就越来越低。所以平值（at the money）期权是个价值不断下降的金融产品。

这就可以做些文章了。知道了你是不断下降的产品，我干嘛不做空（short）你呢？我这公司就是干**抓取时间值（theta capture）**的。
公司的目标是，通过做空无方向性的期权组合，比如跨式（straddle），勒式（strangle），来抓取其不断消逝的时间价值（time value）。
*如果*你的动态对冲（dynamic hedge）支出小于你获取的时间价值，这策略就能奏效。

你看我把*如果*加斜体了。精通买方量化交易的同志们可能已经开始吐槽了，想的很丰满，你这*如果*怎么实现呢？

你可能注意到了，这公司一大半都是技术人员。事实上整个公司都是技术主导的，交易员和矿工全都自己敲代码。为了实现公司的宏伟目标，
CEO 制定的路线是通过技术力量，运用自动化，横向化的系统多快好省地实施交易策略。而我自己的本职工作和这路线还是挺高度一致的。

对于这种规模的公司来说，我们自动化的程度是相当之高。下单交易到分配清算，全自动无人驾驶。这些自动化项目我都没少参与。这些项目里让我印象最深刻，
在工作面试里总会拿出来吹嘘的，是我编写的波动率模型管理系统（volatility model manager）。

搞期权总绕不开波动率，
[波动率模型](https://www.investopedia.com/articles/stock-analysis/081916/volatility-surface-explained.asp)对于我司至关重要。
简单来说，如果你把这波动率系统看成个黑盒子（black box），进去是市场价更新，出来的就是最新的波动率曲面（volatility surface）。
本着可重用，可横纵向扩展的理念，我把波动率计算和曲线优化（curve refit）的代码提取出来，作为库依赖注入到各场景的业务代码里。
我这系统能 refit 市场价，结算价。能持续检测优化模型，又能做即席实时运算。我还把计算原子变成无状态的运算一个个跑到 AWS 云上，要加加要减减，
很方便。

这个系统我自认还是实现得相当良心的。各个环节我都尽可能地做得优雅。私下和同事聊天时，首席交易员跟我说，如果公司黄了，
你这波动率系统是唯一有赎回价值的东西。

说来也很惭愧，在这公司一又四分之三年的时间里，能拿得出手的成绩就这么点。但是没关系，下个章节比这个更短。

#### 贰·壹

__得到什么__

我这个公司的蜜月期还是很乐呵的。公司在搭建程序员工作环境上很能下功夫，人手一台 Mac，显示器要多大有多大，要几块有几块。
工作流程也很能治愈我的大公司后遗症，上面提到的繁缛文件审批都没有了，作为软件工程师的主观能动性被极大释放。同时公司就这么几个人，
每个员工都不但止要独当一面，还要面面俱到地了解公司各种业务流程。在技术上，公司鼓励调研测试前沿技术。
我在技术上的见闻和累积的增长和之前的岗位相比不可同日而语。

我就直接坐在交易员旁边，和他们亲密合作（别想歪），实时接受交易员的反馈，了解厘清他们的想法。实现的系统在市场上真金白银地交易，
我心里还是十分满足的。

刚到公司的时候，我觉得自己就是个聋子。什么 straddle, strangle, calendar spread，什么 delta, theta, gamma, rho。
交易员们巴拉巴拉的讲，我跟听天书似的。
为此我搞来了本 [Natenberg 绿宝书](https://www.amazon.co.uk/Option-Volatility-Pricing-Strategies-Techniques/dp/155738486X),
硬着头皮啃。现在各期权组合（option spreads）的风险参数（greeks）我能给你皱着眉头讲个大概。跟交易员讨论交易策略，
总不用只是点头笑而不语，能把问题问在点子上。实现波动率模型时，我把布莱克76模型（Black 76）和 SABR 模型（Stochastic alpha beta rho）
全手撸了一遍。在这个公司我学到了不少的业务知识。

另外，这一年多里我的'云'技能长足进展。之前的公司虽说也有"云平台"（这个双引号用得很恰当，这个云系统从头到脚都是内部开发的，
和外部的商业云不能比，最多是个高级的虚拟机管理器），我只是叉车式地把系统移植到云上。现在这间公司对云的运用更加深入，
恨不得把整套系统都建立在云端上。
[我也顺便去考了个 AWS 云计算开发人员资格证](/rants_and_scribbles/2019/07/03/i-passed-aws-cert-developer/)。

总结来说，在这间小公司的经历，**多样化了我的知识技能**。这具有非常显性的效果。最近一次工作面试，我对该单位的大领导说，
我认为我的技能，经验与贵司的需求相当的匹配。那大领导说，呵呵呵，可不咋的，是我挑的你的简历啊，你忘了？你以为是随机的呢？

这件小公司算是可以实现我之前提到的三个从上一间公司跳槽的愿景。如果可以，我是愿意长期在本公司效力下去的。
可惜，有这么一道鸿沟，阻挡着，不能让我这么做。我在公司时间越久，这道鸿沟越来越大。下面我来说说这是道什么鸿沟。

#### 贰·贰

__为什么离开__

在小公司，特别是创业公司任职过的同志们应该会感受到，这种企业特别受老板的个人风格影响。我这公司的 CEO 是美国人，
之前任职于某著名高频量化交易企业，后其被派驻伦敦担任欧非中东（EMEA）区首长，而移民的英国。公司的主要交易场所（venue）是 CME（芝商所），
交易员需要覆盖的也是美国中西部市场时间。为什么公司会开设在伦敦呢？因为 CEO 的孩子还在英国读书（what？！）。后来我了解到，
这公司是由 CEO 自己全资支撑的。这让我对公司前途深深地产生了不安全感，老板那天要不想玩儿了咋整？

当然这都是次要的，让我对前途最为感到不安的原因，是**公司理想与现实之间无情的撕裂（好厉害！）**。

之前提到，*如果*可以实现既定的交易策略，这公司的经济前景是相当可观的。作为半个外行加入公司时，我也被这宏伟远景哄得团团转。
随着我对公司业务和系统认识的日渐加深，这目标好像离我们越来越远。我们公司其实也有一系列可以在小规模内盈利的策略，但 CEO 对这些似乎不感兴趣。
CEO 会这么想也能够理解，他在职业生涯的前半段已经功名成就，累积下了几辈子都用不完的净值了。然而，人很容易把理念想法（idea）当作自己的宝贵财产，
当你把 idea 当成宝贝时，你很难舍弃它，即使你的理念像是魁地奇里那虚无缥缈转瞬即逝小金球。追逐小金球的游戏固然有趣，
但是实现的困难会很打击团队的士气。谁会饿着肚子跟着你追小金球呢？

2019 财年年初绩效评估的时候，我听到了那句经典的，*过去一年你的表现很不错，公司感激你的贡献。但基于公司去年业绩表现一般，
所以不拉不拉...* 对，结果是，年薪不涨不跌，奖金若干。

功利的我认为，在职业生涯的前十年，你必须每年都获得高于通胀的涨薪。基于你今后还有数十年的职业生涯（当然不考虑创业者），薪停金涨造成的损失，
即使算成净现值（net present value）也是很可观的。更不要说对日后涨薪的复利的影响了。

这位 CEO 最让我钦佩的特质，是他六出祁山，不撞南墙心不死追寻他心里那片海的坚持和义无返顾。这恰恰也是个双刃剑。
简单描述我在这间创业机构的观感，像是坐在一只小艇，漂浮在大海上，开船的人还不是你。

是时候又重新上路了。

&nbsp;

## 叁
----
说了那么多，到这才终于点回了主题。是的，又要**重新上路**了。在写此文的时候，你们的博主我，已经递上了辞呈。当然我没裸辞，我又不傻。
就在被告知公司去年业绩欠佳之后，我就开始计划另谋新就了。我又稍稍调整了求职定位，这次面试**主攻较成功的企业内较成功的业务**。
于是，在乱面了几家之后，我又再一次掌握了面试的套路。这次我拿了4个 offer。

带着依然新鲜的记忆，我想说说这轮面试的经历和观感。

#### 叁·零

__重新上路__

多次面试与被面试，我对于‘工作面试’这事有这么几点观察，欢迎各位同志评论指导。

第一，我们大家**高估了面试表现与实际工作表现之间的相关性**。换句话说，面试技巧与工作技能是相互独立的两种属性。之前我面过俩哥们。
哥们A面试的时候对答如流，简直一行走的 Java 题库。哥们B就没答得那么溜，而且还有点小个性，面试过程很不流畅。我给的反馈是A优于B。后来我们预算充盈，
俩哥们都招了。实际工作时，我发现他们的工作表现与面试相反，A按部就班，能完成任务但也仅此而已，当一天和尚敲一天钟。B这哥们除了完成本职工作，
还能很有批判性地思考，指出流程中不合理的部分，并发挥主观能动性带头做优化。

我每次开始面试的时候，技巧日久生疏，总免不得会‘乱’面几间。后来越来越渐入佳境，‘掌握套路’，面哪中哪。估计不少同志都会有这样的体验。
真替我最早面那几家公司，跑了大金子，感到不值！

第二，**求职与择业，路径依赖性很强**。为什么这么说呢？这轮我买方卖方公司都面了不少。我总感觉，卖方投行出身的我，
面试投行职位的时候会和面试官交流得更投机。跨行业面试时，我总会感觉我和对方都认为对方怪怪的。不知道你们是否有此感受。

第三点最气人。一朋友和我说过，你在面试时，**面试官在前五分钟其实已经无意识地做出决定了**。我觉得有点道理。很多时候第一印象，甚至是对你简历的第一印象，
就决定了这个面试的结果。这次我面了一个量化做市商，面得还挺溜，问题都答出写出绝大部分。就当我心里感觉挺良好的时候，中介告诉我，挂了。
我给气的，让给回馈。对方说，这位求职者知识水平不错，但是量化做市系统开发经验较少，我们要多花时间把他培养出来。

我去你的。

相反地，眼缘中了，面试会很顺利，尽管你暴露了些知识漏洞。我面高盛的时候，前端技术问题没答上来几个，我是偏后端的。结果反馈，对方说很满意，
他没涉及过的方面我们可以对他进行培养，相信他会学习得很迅速。你说这是什么事？

其实这也好理解。这种现象就是老生常谈的[确认偏见（confirmation bias）](https://en.wikipedia.org/wiki/Confirmation_bias)。
当你确立了一个观点，你会偏重于佐证你观点的事实，而忽略排斥你观点那些，形成偏见。

总结下来，工作面试就是个玄学，充斥着随机，偏见，独断（arbitrary）。很不靠谱。

#### 叁·壹

__路在何方__

是的，路在何方呢？

看到这里，大家可能会这么认为，你这个人那，知道避害，但不懂趋利，没有着眼于明确的目标（keep your eyes on the prize）。这个总结不无道理。
每次转型我都以解决痛点为主导，略显被动。前文提到，若条件允许，我希望可以在一个岗位上连续效力较长的时间。我们不宜轻视跳槽的隐形支出。
除去求职面试所花费的时间精力，换工作对你造成最大的损失是，它拦腰斩断了你在一个单位累积的各种动能。这些动能包括业务知识积累，人脉资源，
年资积累（就是你领导对你说的，好好干，在 x 年后你就能升到叉叉叉）。这些大多都要在新单位重新累积。跳槽，就是通过涨薪变现累积能量的过程。
我希望接下来就职的这个企业是可以让我持续效力的。

我在这四份 offer 中筛选出两个单位。一间是一大型共同基金，技术主管职位，但业务方向欠佳。另一间是某顶级（top-tier）投资银行。是的，
这些投行机构是分三六九等的。这间投行正在从根本上重建升级更新他们的股市交易系统。'十年计划'。这跟我的目标相当匹配。
我挥笔一签，准备上班去了。

我对这间投行的第一印象很好。这当然得益于这间机构本身的威望。而在面试的整个过程体现出这个机构的效率，标准化流程，让人眼目一新。
人力资源也很给力，知道我 offer 多，赶着公共假期之前，连夜催促审批，很快地就把合约发了过来。一般求职的时候，人力资源问待遇要求，
我都会比心理预期多要求 5-10%，因为人力资源可会议价了。唯独这间公司，我开价要多少，他们还给我往上加。真够意思。

好了，最后，在30岁这年，我对今后职业生涯提提这么几个愿景。

1. **加强把握职业发展方向的能力。** 如前文所说，我很清楚自己不喜欢什么，但是对'想要什么'这方面需要加强。毕竟通过'避害'来微调路线，
效率还是欠佳。通过怎么实现呢？看下一条。
2. **提高积累知识和学习技能的能力，已及更有的放矢地进行积累。** 在这个行业摸爬滚打这些年，软硬各种技能没少积累。这些技能也是通过市场，
真金白银验证出来的。这些技能的一大部分都是通过工作机遇所获得，属于无意识，被动的积累。从此希望将吸收方式反转，主动设立技能框架，
主宰知识吸收。
3. 我自从毕业以来这几年，自己的价值都是附属于企业而体现。我写过的每一段精妙的代码，实现过的稳定高效的系统，都直接变成了公司的财产。
心里多少有些不甘。希望在将来，**我的技能可以独立地实现出来，毋需依附于所效力企业。** 怎么实现这一条，我还没什么头绪。
如果有在这方面的经验又愿意分享的同志，欢迎留言讨论。

终于看完了，辛苦了。[吃颗土豆吧。](https://qr.ae/TWvmIi)

![Potato](/assets/potato.png)

（完）

----

&nbsp;

&nbsp;

&nbsp;

以下为译文 / English Version

Till the third quarter of 2019, I have been in this industry for exactly 7 years. 
In the face of the magic number of '7', as well as the second career transition of my life, 
I will briefly summarise these years of my career. 
This blog post is mainly written for myself, especially for the self 7 years later, or even 
```while (isAlive) {age += 7;}``` years later. 
If have wandered in and have a thought for this blog post, please leave a comment.

I changed the style of this blog posts a little. In contrast to other posts in this site, 
This article was written in Chinese. 
The reason for choosing Chinese is that when I talk about 'things', I like to express myself in my work language (English). 
But when it comes to 'people', and this 'person' is himself, it is best to express it in a mother tongue. 
For the consistency of the look and feel of this site, I will attach an English translation (what you are looking at). 

This is a rather long text, take your time and enjoy.

&nbsp;

## 0
----
Since graduating from the Imperial Master's program in 2011, I was just confused about future as many other grads. 
That year, the Conservative Party just came to power and tightened its immigration policy. 
The then Home Secretary, Theresa May, cancelled the Post Study Work visa established by the previous Labour government. 
This means that I don't have the luxury of two years to look for a job in London.  
I haven't got long to be confused. I frenziedly applied for the graduates jobs of London's major investment banks. 
After a few misses, I gradually mastered the routine of the investment bank interviews, 
and subsequently received the offers of three banks.

After weighing the pros and cons of the gains and losses, I chose one of the three banks and went to work happily. 
I spent 5 good years of my career in this place

&nbsp;

## 1
----
In the fall of 2012, I joined the the bank;s Global Markets Technology as a graduate. 
Simply put, this is the technology arm of its investment banking department. In Chinese context, 
this type of role is often referred as 'financial code farmer'.

I do not agree nor like the description of 'code farmer'. 
The word 'farming' has the subtle meaning of labor-intensive work (no offence to agricultural professionals). 
The essence of software engineers is precisely to eliminate labor-intensive work. 
As a software engineer, if you find yourself 'farming' a lot, you probably are in the wrong trade.

Joined as a grad in 2012, I spent a little more than 5 years in the bank.
My experience of all these years would warrant 10 blog post or more.
I will sum up my joys and sorrows in this company in the aspect of **what I've done, what I've achieved,** and 
**why I left**.

#### 1·0
__What I've Done__

This is actually quite difficult to sum up.

Difficult, of course, is not because you do not know what you have done, otherwise you would just copy and paste the CV.
The difficulty lies in how to extract some of the legacies of sustainable and systematic contributions in the dizzying 
array of projects that have been done.

I spent most of my time in the bank within the Futures Clearing and Collateral Management (Fucc'm, that's right, 
this is how the sign above my head reads) technology department, serving the Futures eTrading and Risk business.

When I first joined the team, jeez, the entire tech stack was a big wild west.
Continuous integration was next to non-exist, one click deployment was not there, 
the code repository was still SVN. I remember the first time I watched my colleagues do the deployment. 
I was watching him, clicked open Windows Remote Desktop, logged into the production environment, 
and manually pulled the local maven-built zip package (that's right) to the desktop of the production environment.
He then manually unzips the zip and pulls the sub-files one by one into the deployment directory. 
I was shocked out of the roof.

It certainly can't go on like this. During the my years in the team, I continued to improve the SDLC maturity of the 
software system under the premise of ensuring the progress of projects. I moved the code repository from SVN to the 
internally hosted git server and then to the Bitbucket shared by the entire bank. Initially our software was deployed 
directly on bare metal servers, and I moved them to virtual machines. And then they were all migrated to the firm's internal
cloud. I have successively established systems such as continuous integration, automatic deployment, automatic testing, 
static code quality analysis, and code quality gates. Also, I standardized the technology structure and build methods for 
projects across different business areas. This allows future generations of engineers to join to develop on our systems 
with ease, while ensuring that the quality of the software produced within this framework is relatively high.

In a nutshell, the most important legacy I left was that I injected the **sustainable, horizontally scalable software development
DNA into my systems**, and spread it to other sisters in the wider organisation to some extent. 
This company was quite fund of scorecarding systems based on their software development maturity, and my system always appeared 
on the top lists within the department. This kind of made every one look good.
My direct manager back then even used it as one of his 'achievements' to justify his promotion. I laughed my head off.

As for the business, my legacy was to extend a software system that serves several internal employees to a software 
service that can meet the needs of numerous internal and external customers. The system was first installed on the 
desktops of several risk managers, tracking and monitoring our clients' maintenance margin requirements. 
By the time I left, the system has been reversed to a service that satisfies real-time ad hoc margin calculations, 
and the service is exposed on the portal site for use by external clients. Because of the delivery of 
this high profile project, the company won the business of a government backed investment institution in Singapore. 
This was quite an achievement back then and put a smile in many's faces. Although in the investment banking environment, 
the technical department only gets a small slice of the cake, but as a relatively junior guy delivering all these, 
I was quite well rewarded. And we will now smoothly transition to the next chapter, what I've got.

#### 1·1
__What I've Achieved__

Bai Yansong once said that, [failure is not the mother of success, rather, victory is the mother of success](http://news.ifeng.com/a/20160907/49929707_0.shtml)). 
I deeply agree with this. Over the years I have witnessed first hand and participated in the whole progress of 
software projects from scratch. Learn how to turn the ideas and ideas of customers and traders into a robust, scalable systems. 
The successful delivery of these high profile projects has built up my confidence in this industry. 
I participated in these projects as project manager, personnel supervisor, and technical backbone, 
as well as getting my hands dirty to lead charges up front. This mentality gave me confidence to take on any complex 
development projects and challenges.

Apart from some bureaucratic matters, I rarely needed to report to my direct manager. I directly engage to clients and 
business owners. An autonomous environment is also an important factor that propelled my growth.

Through these years I rose up the corporate ladder pretty quickly and grasped all possible opportunities for promotion. 
I made VP in the fourth year since graduation. This was partially due to the trend of corporate title inflation back in those days. 
More importantly, I had a good nurturing boss, to whom I felt grateful, even till this day.

When I was a team lead, my subordinates were scattered around the world. Why is this so? 
Bulge bracket banks had this practice of setting up "centres of excellence" (COE). So what the hell are these?
The COE is the politically correct term for a cheap locations. These COEs are offices established by the firm in 
third world countries to cut costs.

I had a team member in the COE of Belfast, who later transferred a different team in the bank.
Before he left, he told me that he would well remember what I've taught him all these time. My ego was much boosted.

To sum up, the most import thing I achieved is growth. To add a bit more, I have achieved the 'title'.
[Some argues that titles are all non-substantial](https://coolshell.cn/articles/10688.html)). 
Yet very few would actually be willing to give their titles away.
Titles themselves do not carry practical significance, no one is going to address you as Mr VP. 
But your status in the industry (gravitas) backed by the title is real. Each major bank has a strict salary band 
for each title. Having achieve certain title it is also beneficial in job hunting. 
The new company will always have to match you the corresponding title you have obtained.

So why move? You may ask. Sit tight, here comes the roast.

#### 1·2
__What I Left__

Finally. I waited too long to write this.

Why are you doing this? People around me, family and wife, were confused about my decision to quit. 
In fact, during the final years in the bank, my mental state was progressively worsen. I felt pain, suffering and grief 
(ok I exaggerated a little). One thing was certain. In the last year of my tenure, I had made up a firm mind to leave.

3 main factors.

First, **that was the optimal time to move**. As stated I made VP that year. In banks, the title of VP (Vice President) 
is generally an achievable goal. To get promoted to Director, though, needs years of glooming.
I didn't want to spend all of my career there. Furthermore, the UK's immigration policy allows foreigners who have 
worked continuously for five years to apply for permanent residence, then employment won't be restricted. 
Now that I have done my sentences I was naturally encouraged to plan for a move.

I had been working at the same bank for five consecutive years. Albert having good raises each year
my salary level is far below the market because of the low base of graduates. 
There was this time that I was dumb enough to assess my salary level in Glassdoor. So I entered my salary. Oh, 
my salary just became the lower bound of the statistics for Vice President in that bank.

Tough!

Secondly, my technical skills and business knowledge have been improving much slower during the last two years. 
The tasks handed over to me are becoming more and more homogeneous, and I am became increasingly insecure.
My skills will become more and more irrelevant to market. **It's time to diversify my experiences and skills.**

Given my position and the connections I accumulated, is not impossible for me to rise up the rank and make Director
one day. However, to do this I will be shorting volatility. What do I mean, you ask.
If I decide to stay, I am betting on things to stay static, the company will not lay off staffs, 
the business department will not be cut, the my network in the firm will still be there, and the market 
will not shrink. Once these external conditions fade away, my position would be endangered.
I will become fragile. And I want to be anti-fragile, I have to strengthen the width and depth of my skills, 
and long volatility. 

The slow down of my improvement is largely due to some institutional and philosophical problems of the company. 
See how I raise up the whole topic here? Let's talk about these institutional issues I faced.

The third and the most important reason why I left is that over the years, I realised that the firm, as [put by
Chen Hao, tent to solve problems through management rather than technology](https://coolshell.cn/articles/17737.html). 
This is the very point I disagree with the firm and despite. It is also the fundamental cause of my grievances
in my final days in the company.

As a junior team lead in the firm I was buried with all sorts of ruthless bureaucratic formalism work. 
A variety of weird spreadsheets to be filled; at least two days of paperwork before each deployment, 
with eight approvals to chase; there's always someone from some part of the company you never heard up jumping up 
out of no where to chase you for paperwork. Every Wednesday, you receive a scorecard on paperwork completion cc'd to all big cheeses,
and risk of being in their 'naughty list'. I lost sleep on dump things as such.
In retrospect, it was a quite a feat that I could handle so these bureaucracy while ensuring the projects' delivery.

Some would say that this is a common problem for big firms. If you can't adapt to it, change it,
which point I agree with in principle. Well, I got three stories to tell, please hear me out.

The first story was about the bank's management of password files. 
Every year, the company goes through a technology audit by KPMG to assess the health of the software system. 
Um, well, it's KPMG. It didn't feel right to get audited by some lesser firms in terms of tech.
Of course, external auditing is always necessary, and they did found some problems. One of the themis that some of 
the system's passwords stored naked in files.
 
This problem was not a real problem. Some people think that the bare password will be used by malicious 
programmers. This view is dumb, and if the programmer needs it, there are countless ways break the systems. 
Some would think that this would make it easier for external attacks. Another stupid view, now that they are in your
intranet, what make you think the hackers would need your passwords?

Compliance did not necessary shared the same view. Compliance made a panic move to on-board a password management system.
Now passwords were not scattered all over the place. To set passwords, you send 
someone to log in to our system and type in the password, then forget it (that's right). Get your password in real time by 
accessing a REST API at the start of your system. Hearing this password thing, I face palmed.

![Face Palm](/assets/face-palm.jpg)

This is masturbation, to make you feel better, and the actual effect is not there at all. 
Do you really think that set and forget is feasible? Is REST content really safe? When the whole bank's systems access
your API, are you sure you won't be denial of access (DoS)?

Compliance has set a dead line, stipulating that all software systems company-wide should be on-board in time. 
There were some pioneering teams to use this system. Let's say disappointed was an understatement. The anticipated DoS
happened and they could not access password in production environment. And the password system was put on ice.

There are many ways to manage passwords, the best being no password. No password does not mean there is no authentication, 
there are many ways to implement system authentication without passwords. When the firm tried to solve problems through 
management methods rather than technology, and laymen to run the effort with one-size-fits-all approach, failure is 
inevitable.

The second story was also a good one.

So I got phoned up one day, it was a lady with Eastern European accent.
(probably from the Budapest Center of Excellence). She said that they found that our systems had been transferring data 
via ftp. And she asked a deadline from me to port all ftp pipelines to sftp. 
Later I learned that it was a department of the Japanese branch that leaked data with ftp transmission. 
Some big cheeses were very crossed and decided to slash all the ftp transmission pipes.

I told her that I am visiting (CME Group) public data, why use sftp? 
She didn't seemed to have got the gist and asked when can I resolve this. I later told her that CME data currently only provides ftp access. 
If you have to do sftp, I can contact them, ask for the asking price for porting to sftp. So which department should 
I bill this on?

The lady did not bother me any more.

There is also a third story, one of the last few straws that crushed the camel.

As mentioned earlier, it is necessary to do a few days of paperwork before each system deployment. This includes 
filling out a dozen pages of release plan forms. Ain't nobody got time for that. I had one of my guys to write a 
automatic form filling system with Selenium WebDriver.
After a few days of fun, we were told that this automatic filling system could not be used anymore. 
The reason is that the news reached the ears of the release management department
(yes, there is such a department, I always think that these departments are job creation schemes). 
They said you guys can't just by pass the software deployment process.

![Face Palm](/assets/face-palm.jpg)

In all fairness, this bank is indeed a great company. I met many people who are outstanding
in their own respective fields. There is a saying inside the company – we are a technology firm with a banking licence. 
I don't think it lived up to it.

You can probably see by now, I can't win this thing. If you can't choose to result of battle, you can at least choose the battlefield. 
And now I have to re-select the battlefield.

&nbsp;

---
> Half Time break

![Spiderman Dancing](/assets/spiderman_dancing.gif)

I used this dancing spider man as loading gif for my systems. See how cute he is.

You guessed it, not that everyone likes the spider man. I had to change the gif but left the file name unchanged.
Now all loading images in my systems are called ``spiderman_dancing.gif``.

---

&nbsp;

## 2
----
In the third quarter of 2017, I went job hunting frenziedly.
What also went frenzied were the crypto currencies. The Bitcoin bubble was at its all time height, and blockchain start-ups grew like 
mushrooms. I interviewed with a blockchain firm, which offered a lower salary. The head-hunter's sales pitch went like, 
oh, blockchain is the most sought after skill in the market and loads people are taking a pay cut just to get in
the game blah-blah.

Traumatised by big companies, in this round of job hunting I mainly aimed at small and medium-sized companies, 
especially the buy-side financial institutions. After a few misses, I once again mastered the interview routine. 
I took the offer of a small technology-driven buy-side proprietary trading shop. 
It was a jump all the way across to the other end of the spectrum.

This company, well, is very interesting. See? I used the polite word 'interesting', which also pretty well defined 
my time at this company in its pure literal sense.

As usual, I'll go over my experience in this company in aspects of **what I've done, what I achieved**, and **why I left**.

#### 2.0
__What I've Done__

So, what I have done. Let's look at what this company is doing.

The company looks a lot like the office in The Big Short, the one where they got screen hanging all over.
The company is small, you can look at the entire company at a glance. 
The company employs about 12 people. Why do I say 'about'? When I first joined, 
there were a total of five software engineers in the company, as well as traders and two quantitative analysts. 
There are also some part-time workers like personal assistants, and even COO (Chief Operating Officer) was 
part-time. Plus the founder and CEO, about twelve people.

The company is small, while, the ambition is big. I'll try briefly explain the mission of the company.

We mainly trade listed options. Options, are like buying an insurance policy, to bet for an unlimited return with limited 
premium. And that premium you pay is proportional to the length of the policy.
The longer the insurance period, the higher the premium. Projecting the principle to options, when the expiration date 
gets closer, and the time you are protected by this “right” gets shorter and the price gets lower. 
Therefore, at the money option is an ever declining financial product.

This is where all the fun starts. So you are a declining product, why not go short on you. One of the key goals of the 
firm is to capture time value loss of options with smooth continuous hedging. The business works *if* the theta captured
is higher than your hedge cost.

See how I italic this *if*. Now this is a big *if*. How on earth are you guys going to achieve that.

You may have noticed that the company is mainly made up of technologists. In fact, the entire company is technology-led, 
and traders and quants all code themselves. In order to achieve the company's ambitious goals, 
the CEO's vision is to implement trading strategies faster and more economically through the use of technology, 
automation, and horizontal systems. And my work in this firm pretty much aligns with this vision.

For companies of this size, the level of automation is quite high. From order placement to allocation and clearing, 
all processes are driverless. I participated in almost all of these system implementation. Let me go through one of these
system that I was most proud of and liked to brag about in job interviews, the volatility model manager.

The [volatility model](https://www.investopedia.com/articles/stock-analysis/081916/volatility-surface-explained.asp) is imperative to option houses,
To put it simply, if you look at the volatility model manager as a black box, the input are market price updates and 
the outputs are the latest volatility curves. With reusability and horizontal and vertical scalability in mind, 
I extracted the volatility calculation and curve refit code as library dependencies, and injected those into different 
business services. The system is capable of refitting either market price or settlement prices. I can refit continuously
or handle ad-hoc calculation request.
I also ran the computational units as stateless operations and ramp them into AWS cloud.

This was a rather polished and elegantly implemented system. Our head trader told me that if the company went under,
your volatility system is the only thing with some redeemed value.

This chapter is quite short for a year and three quarters' work, and the next chapter would be even shorter if anyone 
cares.

#### 2.1
__What I've Achieved__

I had a good honeymoon period in this firm. The firm comes with great mod-con and thrives to build the development 
environment for developers. No more boring paperwork, my initiatives as a software engineer is greatly released. 
At the same time, being a small firm, everyone takes ownership of their project. 
Research and testing of cutting-edge technologies are encouraged. My tech capabilities grew a great deal.

I sit close to the traders and work intimately with them. With fast feedback loop with traders, it was quite 
satisfying to see your work actually running and making money in the market.

When I first joined the company, I felt that I was a blind man. Straddle, strangle, calendar spread,  
delta, theta, gamma, rho, was all like Klingon to me. For which reason I got myself a [copy of Natenberg](https://www.amazon.co.uk/Option-Volatility-Pricing-Strategies-Techniques/dp/155738486X) 
and chewed through it.Now I can give brief explanation the risk exposures of the 
different options spreads, and won't have to smile and nod when discussing trading strategies with traders.
I hand coded the Black 76 model and the Stochastic alpha beta rho model，when implementing the Volatility Model project.
I have learned a lot of business knowledge in this company.

In addition, my 'cloud' skills have progressed over the past year. Though there was "cloud platform" in my previous company
(this double quote is used properly, this cloud system is developed entirely in-house, not comparable to the external
 business cloud, at most an advanced virtual machine manager), I was just forklifting the system 
 to the cloud. This firm embraces cloud very deep and had the vision to build the entire infrastructure on cloud. 
 [I also took and passed the AWS Cloud Developer Developer Certificate exam](/rants_and_scribbles/2019/07/03/i-passed-aws-cert-developer/).

In summary, **I diversified my knowledge and skills at this firm**. The effect was very apparent.
In a recent job interview, I told the hiring manager that my skill set matches the role's profile very well.
And he went, I picked your CV remember? It wasn't random.

All there reasons why I left the previous firm was quite dealt with. I had plan to spent some longer time in this firm
until I discovered it was not possible. Will elaborate more on that next chapter.

#### 2.2
__Why I Left__

Comrades who have worked in small companies, especially start-ups, should feel that such companies are particularly 
influenced by the personal style of the founder. The CEO of my company is from the US, formally a senior manager of
a US elite systematic trading fund. We are here in London because the CEO was sent in by he's previous firm as the
EMEA head, and he kind of put down roots here, with kids sent in schools. The firm is fully funded by the CEO's personal
wealth. I was quite insecure about my place in the firm learning all these. What happens if our boss quits?

Although, the thing that I felt the most insecure about, was the **elusiveness of the vision of the company (whoa!)**.

As mentioned earlier, *if* the strategy worked, the economic prospects of the company 
are quite considerable, which was the very reason I was so keen to join the firm in the first place. 
As my knowledge of the company's business and systems deepens, this goal seems to be getting farther and farther 
away from us. Our company actually has a series of strategies that can be profitable on a small scale, 
but the CEO does not seem interested in these. He has made a name for 
himself in the first half of his career and has accumulated a net worth enough for several after-lifes. However, 
people tend to see idea as their valuable asset. When you think of an idea an property, 
it is difficult to abandon it, even if your idea is like the faint little golden snitch in Quidditch. 
The game of chasing a small golden snitch could be interesting, but that would certainly hurt the morale 
of the team. No one would chase the snitch for you with empty tummies.

In the performance review at beginning of the 2019 fiscal year, I heard the classic one. 
*You perform well in the past year, however the firm didn't do so well so blah-blah*
Yup, I got a small bonus with no pay rise.

Utilitarian I believe that in the first ten years of your career, you pay rise must beat the inflation. 
The loss for not getting pay rise this early in your career, even if it is calculated as the net present value, 
is considerable. Not to mention the impact on compounded pay rises in the future.

I admire our CEO for his persistence and constance pursue for the goal and vision of his. Which, sadly, could be
a double edged sword.

My experience in this firm, to put it simply, is like sitting in a small boat, floating in the sea, 
and you don't really get to drive the boat.

It’s time to get back on the road again.

---

&nbsp;

## 3
----
After all these, here we are again. Yes, **time to get back on the road again**.
At the time of writing this article, your blogger had already submitted my resignation. 
Of course, I didn't quit without somewhere to go, I am not that dumb. Just after the year end review, I started to look in the market. 
I re-calibrated my target a little. This time I focused on successful businesses in established firms. And, 
after a few misses, I once again mastered the interview routine. This time I got 4 offers.

With a still fresh memory, I want to talk about the experience and perception of this round of interviews.

#### 3.0
__Back on the Road Again__

Having been in either end of the table in numerous job interviews, I abstracted a few points of my thoughts about
this matter. 

First, we all **overestimated the correlation between interview performance and actual work performance.** 
In other words, interview skills and work skills are two separate attributes. 
There was this time I interviewed 2 guys for the same job. Interviewee A was like a walking banking of Java interview 
questions and passed with flying colours.
Interviewee B didn't do nearly as good A, and the interview was rather bumpy.
The feedback I gave was A better than B. And we actually got enough funding to hire them both. In actual work, 
I found that their work performance is in contrary to the interviews. A can manage all the tasks threw at him, but that's 
about it. While B, in addition to completing he's own duties, employs critical thinking and 
point out what were wrong with the process, and take the initiative to take the lead to change them.

In each round of job hunting, my interview skills were rather rusty in the beginning. Through the process my skills would gradually get better and 
with exponentially growing success rate. I felt bad for those firms I interviewed in the beginning for missing me out.

Secondly, I find **job hunting is very much path dependent**. I interview many firms across buy-side and sell-side.
Having spent most my career in sell-side, I always feel that I can resonate better with sell-side banks, 
Not sure if you've felt the same way.

The third point is the most irritating one. A friend told me that during the interview, 
the **interviewers made up an unconscious decision in the first five minutes**. I tend to agree with this.
Many times the first impression, even the first impression of your resume, determines the outcome of this interview. 
That was a time I interviewed with a quantitative market maker, and I felt I did ok. However the recruiter told me that
it was a no. The feedback was that they thought my I had good knowledge at what I do, 
but lack experience in quantitative market making and we had to spent time to bring him up to speed.

Screw you mate.

On the contrary, the interview will go smoothly if they had a good impression, even though they find some holes in your knowledge base.
When I interviewed with Goldman Sachs, I couldn't answer much of the front-end questions. But the feedback was,
they believed I could pick things up fast and were quite happy with my performance. Strange.

In fact, this is quite understandable. It is called [confirmation bias](https://en.wikipedia.org/wiki/Confirmation_bias). 
When you established a point of view, you will focus on the facts that support it, while ignoring those facts that reject
your opinion, forming a bias.

To sum up, I find job interviews are full of randomness, prejudice, and arbitrary. Very unreliable.

#### 3.1
__Where will the Road Leads__

So, where will the Road Leads?

Many of you may think that this blogger knows to avoid what he doesn't want, but doesn't know what he really wants. 
This is not incorrect. Every career moves I took were aiming to solve the paint points, which is rather passive.
As mentioned above, if conditions permit, I hope that I can continuously work in a same firm.
We should not underestimate the hidden cost of job changes. 
Excluding the time and effort spent on job interviews, the biggest cost for switching job 
is that it curbs all the momentum you have built up. These could be  
business knowledge accumulated, network resources, and seniority (as your boss told you that, in x years you'll be xyz, etc). 
Most of these will be rebuilt in your in position. Job changing is like cashing out of momentum. I hope I get to build
up momentum for a longer time in the next job.

I narrowed down these 4 offers to 2. One is a large mutual fund, technical lead position, 
but the business area is a bit dull. The other is a top-tier investment bank. 
Yes, these investment banking are all 'tiered'.
The investment bank is rebuilding and upgrading its equities trading system top down. 
It's a 'ten year plan'. A good match to my ambitions. Was a easy decision in the end and I signed the contract with them.

I had good first impression with this investment bank. This of course partially have to do with the banks' prestige.
Also the whole interview process was refreshingly efficient and smooth. Their HR knew that I had multiple offers and
had the contract prepared overnight before 4th July. I normally ask for 5-10% more my expected salary, for HR would 
almost always negotiate it down. And this bank gave a number even higher than what I asked for, with annualised bonus
at year end. 

Now, at the age of 30, and the end of this post, please allow me to ink down a few vision for my career ahead.

1. **Strengthen the ability to grasp the direction of career development.** 
As I said earlier, I know very well what I don't like, but I need to strengthen the 'what I want' aspect. 
After all, calibrating with 'avoidance' is not efficient. 
How to achieve it? Look at the next one.

2. **Targeted accumulation of knowledge and learning skills**.
Through the years I had acquired skills in this industry what are fairly priced in the market.
Although, large portion of these skills are obtained through work and are unconscious and passively 
accumulated. From now on, I should work on reverse the absorption method and actively set up a framework to 
dominate knowledge acquisition.

3. Ever since I started to work, all my values are add to the companies I worked for. 
Every piece of code that I've written, every system that I've built, 
turned straight into company's property. I would like to **use my skills out side of my day job**.
I don't have a clue what to do with this. If you have an idea and like to share, 
please leave a message.

Thanks for reading this long post and [here is your potato.](https://qr.ae/TWvmIi)

![Potato](/assets/potato.png)

(The End)























