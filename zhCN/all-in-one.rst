简体中文
=================

.. toctree::
   :maxdepth: 2

   preface-cn
   ch1-cn
   ch2-cn
   ch3-cn
   ch4-cn
   ch5-cn
   ch6-cn
   ch7-cn
   ch8-cn
   ch9-cn
   ch10-cn
   ch11-cn
   ch12-cn
   ch13-cn
   ch14-cn
   ch15-cn
   ch16-cn
   ch17-cn
   appendix-A-cn
   appendix-B-cn
   appendix-C-cn
   appendix-D-cn
   notes-cn
   
   前言
************

本书的目的是快速及全面的教你 Common Lisp 的有关知识。它实际上包含两本书。前半部分用大量的例子来解释 Common Lisp 里面重要的概念。后半部分是一个最新 Common Lisp 辞典，涵盖了所有 ANSI Common Lisp 的操作符。

这本书面向的读者
====================

ANSI Common Lisp 这本书适合学生或者是专业的程序员去读。本书假设读者阅读前没有 Lisp 的相关知识。有别的程序语言的编程经验也许对读本书有帮助，但也不是必须的。本书从解释 Lisp 中最基本的概念开始，并对于 Lisp 最容易迷惑初学者的地方进行特别的强调。

本书也可以作为教授 Lisp 编程的课本，也可以作为人工智能课程和其他编程语言课程中，有关 Lisp 部分的参考书。想要学习 Lisp 的专业程序员肯定会很喜欢本书所采用的直截了当、注重实践的方法。那些已经在使用 Lisp 编程的人士将会在本书中发现许多有用的实例，此外，本书也是一本方便的 ANSI Common Lisp 参考书。

如何使用这本书
====================

学习 Lisp 最好的办法就是拿它来编程。况且在学习的同时用你学到的技术进行编程，也是非常有趣的一件事。编写本书的目的就是让读者尽快的入门，在对 Lisp 进行简短的介绍之后，
第 2 章开始用 21 页的内容，介绍了着手编写 Lisp 程序时可能会用到的所有知识。
3-9 章讲解了 Lisp 里面一些重要的知识点。这些章节特别强调了一些重要的概念，比如指针在 Lisp 中扮演的角色，如何使用递归来解决问题，以及第一级函数的重要性等等。

针对那些想要更深入了解 Lisp 的读者：
10-14 章包含了宏、CLOS、列表操作、程序优化，以及一些更高级的课题，比如包和读取宏。

15-17 章通过 3 个 Common Lisp 的实际应用，总结了之前章节所讲解的知识：一个是进行逻辑推理的程序，另一个是 HTML 生成器，最后一个是针对面向对象编程的嵌入式语言。

本书的最后一部分包含了 4 个附录，这些附录应该对所有的读者都有用：
附录 A-D 包括了一个如何调试程序的指南， 58 个 Common Lisp 操作符的源程序，一个关于 ANSI Common Lisp 和以前的 Lisp 语言区别的总结，以及一个包括所有 ANSI Common Lisp 的参考手册。

本书还包括一节备注。这些备注包括一些说明，一些参考条目，一些额外的代码，以及一些对偶然出现的不正确表述的纠正。备注在文中用一个小圆圈来表示，像这样：○

.. note::

	译注: 由于小圈圈 ○ 实在太不明显了，译文中使用 λ 符号来表示备注。

`λ <http://ansi-common-lisp.readthedocs.org/en/latest/zhCN/notes-cn.html#viii-notes-viii>`_

代码
==========

虽然本书介绍的是 ANSI Common Lisp ，但是本书中的代码可以在任何版本的 Common Lisp 中运行。那些依赖 Lisp 语言新特性的例子的旁边，会有注释告诉你如何把它们运行于旧版本的 Lisp 中。

本书中所有的代码都可以在互联网上下载到。你可以在网络上找到这些代码，它们还附带着一个免费软件的链接，一些过去的论文，以及 Lisp 的 FAQ 。还有很多有关 Lisp 的资源可以在此找到：
http://www.eecs.harvard.edu/onlisp/
源代码可以在此 FTP 服务器上下载：
ftp://ftp.eecs.harvard.edu:/pub/onlisp/
读者的问题和意见可以发送到 pg@eecs.harvard.edu 。

.. tip::

	译注：下载的链接都坏掉了，本书的代码可以到此下载：https://raw.github.com/acl-translation/acl-chinese/master/code/acl2.lisp

On Lisp
=============

在整本 On Lisp 书中，我一直试着指出一些 Lisp 独一无二的特性，这些特性使得 Lisp 更像 “Lisp” 。并展示一些 Lisp 能让你完成的新事情。比如说宏： Lisp 程序员能够并且经常编写一些能够写程序的程序。对于程序生成程序这种特性，因为 Lisp 是主流语言中唯一一个提供了相关抽象使得你能够方便地实现这种特性的编程语言，所以 Lisp 是主流语言中唯一一个广泛运用这个特性的语言。我非常乐意邀请那些想要更进一步了解宏和其他高级 Lisp 技术的读者，读一下本书的姐妹篇： `On Lisp <http://www.paulgraham.com/onlisp.html>`_ 。

.. tip::

	On Lisp 已经由知名 Lisp 黑客 ── 田春 ── 翻译完成，可以在网络上找到。
	── 田春（知名 Lisp 黑客、Practical Common Lisp 译者）

鸣谢
==========

在所有帮助我完成这本的朋友当中，我想特别的感谢一下 Robert Morris 。他的重要影响反应在整本书中。他的良好影响使这本书更加优秀。本书中好一些实例程序都源自他手。这些程序包括 138 页的 Henley 和 249 页的模式匹配器。

我很高兴能有一个高水平的技术审稿小组：Skona Brittain, John Foderaro, Nick Levine, Peter Norvig 和 Dave Touretzky。本书中几乎所有部分都得益于它们的意见。 John Foderaro 甚至重写了本书 5.7 节中一些代码。

另外一些人通篇阅读了本书的手稿，它们是：Ken Anderson, Tom Cheatham, Richard Fateman, Steve Hain, Barry Margolin, Waldo Pacheco, Wheeler Ruml 和 Stuart Russell。特别要提一下，Ken Anderson 和 Wheeler Ruml 给予了很多有用的意见。

我非常感谢 Cheatham 教授，更广泛的说，哈佛，提供我编写这本书的一些必要条件。另外也要感谢 Aiken 实验室的人员：Tony Hartman, Dave Mazieres, Janusz Juda, Harry Bochner 和 Joanne Klys。

我非常高兴能再一次有机会和 Alan Apt 合作。还有这些在 Prentice Hall 工作的人士： Alan, Mona, Pompili Shirley McGuire 和 Shirley Michaels, 能与你们共事我很高兴。

本书用 Leslie Lamport 写的 LaTeX 进行排版。LaTeX 是在 Donald Knuth 编写的 TeX 的基础上，又加了 L.A.Carr, Van Jacobson 和 Guy Steele 所编写的宏完成。书中的图表是由 John Vlissides 和 Scott Stanton 编写的 Idraw 完成的。整本书的预览是由 Tim Theisen 写的 Ghostview 完成的。 Ghostview 是根据 L. Peter Deutsch 的 Ghostscript 创建的。

我还需要感谢其他的许多人，包括：Henry Baker, Kim Barrett, Ingrid Bassett, Trevor Blackwell, Paul Becker, Gary Bisbee, Frank Deutschmann, Frances Dickey, Rich 和 Scott Draves, Bill Dubuque, Dan Friedman, Jenny Graham, Alice Hartley, David Hendler, Mike Hewett, Glenn Holloway, Brad Karp, Sonya Keene, Ross Knights, Mutsumi Komuro, Steffi Kutzia, David Kuznick, Madi Lord, Julie Mallozzi, Paul McNamee, Dave Moon, Howard Mullings, Mark Nitzberg, Nancy Parmet 和其家人, Robert Penny, Mike Plusch, Cheryl Sacks, Hazem Sayed, Shannon Spires, Lou Steinberg, Paul Stoddard, John Stone, Guy Steele, Steve Strassmann, Jim Veitch, Dave Watkins, Idelle and Julian Weber, the Weickers, Dave Yost 和 Alan Yuille。

另外，着重感谢我的父母和 Jackie。

`高德纳 <http://zh.wikipedia.org/zh-cn/%E9%AB%98%E5%BE%B7%E7%BA%B3>`_\ 给他的经典丛书起名为《计算机程序设计艺术》。在他的图灵奖获奖感言中，他解释说这本书的书名源自于内心深处的潜意识 ── 潜意识告诉他，编程其实就是追求编写最优美的程序。

就像建筑设计一样，编程既是一门工程技艺也是一门艺术。一个程序要遵循数学原理也要符合物理定律。但是建筑师的目的不仅仅是建一个不会倒塌的建筑。更重要的是，他们要建一个优美的建筑。

像高德纳一样，很多程序员认为编程的真正目的，不仅仅是编写出正确的程序，更重要的是写出优美的代码。几乎所有的 Lisp 黑客也是这么想的。 Lisp 黑客精神可以用两句话来概括：编程应该是有趣的。程序应该是优美的。这就是我在这本书中想要传达的精神。

`保罗•格雷厄姆 (Paul Graham) <http://paulgraham.com/>`_

.. highlight:: cl

第一章：简介
*******************************

`约翰麦卡锡 <http://zh.wikipedia.org/zh-cn/%E7%BA%A6%E7%BF%B0%C2%B7%E9%BA%A6%E5%8D%A1%E9% 94%A1>`_\ 和他的学生于 1958 年展开 Lisp 的初次实现工作。 Lisp 是继 FORTRAN 之后，仍在使用的最古老的程序语言。 `λ <http://acl.readthedocs.org/en/latest/zhCN/notes-cn.html#notes-1>`_ 更值得注意的是，它仍走在程序语言技术的最前面。懂 Lisp 的程序员会告诉你，有某种东西使 Lisp 与众不同。

Lisp 与众不同的部分原因是，它被设计成能够自己进化。你能用 Lisp 定义新的 Lisp 操作符。当新的抽象概念风行时（如面向对象程序设计），我们总是发现这些新概念在 Lisp 是最容易来实现的。Lisp 就像生物的 DNA 一样，这样的语言永远不会过时。

1.1 新的工具 (New Tools)
=========================

为什么要学 Lisp？因为它让你能做一些其它语言做不到的事情。如果你只想写一个函数来返回小于 ``n`` 的数字总和，那么用 Lisp 和 C 是差不多的：

::

	; Lisp                   /* C */
	(defun sum (n)           int sum(int n){
	  (let ((s 0))             int i, s = 0;
	    (dotimes (i n s)       for(i = 0; i < n; i++)
	      (incf s i))))          s += i;
	                            return(s);
	                          }

如果你只想做这种简单的事情，那用什么语言都不重要。假设你想写一个函数，输入一个数 ``n`` ，返回把 ``n`` 与传入参数 (argument)相加的函数。

::

	; Lisp
	(defun addn (n)
	  #'(lambda (x)
	      (+ x n)))

在 C 语言中 ``addn`` 怎么实现？你根本写不出来。

你可能会想，谁会想做这样的事情？程序语言教你不要做它们没有提供的事情。你得针对每个程序语言，用其特定的思维来写程序，而且想得到你所不能描述的东西是很困难的。当我刚开始编程时 ── 用 Baisc ── 我不知道什么是递归，因为我根本不知道有这个东西。我是用 Basic 在思考。我只能用迭代的概念表达算法，所以我怎么会知道递归呢？

如果你没听过\ `词法闭包 「Lexical Closure」 <http://zh.wikipedia.org/zh-cn/%E9%97%AD%E5%8C%85_(%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6)>`_  (上述  ``addn``  的范例)，相信我， Lisp 程序员一直在使用它。很难找到任何长度的 Common Lisp 程序，没有用到闭包的好处。在 112 页前，你自己会持续使用它。

闭包仅是其中一个我们在别的语言找不到的抽象概念之一。另一个更有价值的 Lisp 特点是， Lisp 程序是用 Lisp 的数据结构来表示。这表示你可以写出会写程序的程序。人们真的需要这个吗？没错 ── 它们叫做宏，有经验的程序员也一直在使用它。学到 173 页你就可以自己写出自己的宏了。

有了宏、闭包以及运行期类型，Lisp 凌驾在面向对象程序设计之上。如果你了解上面那句话，也许你不应该阅读此书。你得充分了解 Lisp 才能明白为什么此言不虚。但这不是空泛之言。这是一个重要的论点，并且在 17 章用程序相当明确的证明了这点。

第二章到第十三章会循序渐进地介绍所有你需要理解第 17 章程序的概念。你的努力会有所回报：你会感到在 C++ 编程是窒碍难行的，就像有经验的 C++ 程序员用 Basic 编程会感到窒息一样。更加鼓舞人心的是，如果我们思考为什么会有这种感觉。 编写 Basic 对于平常用 C++ 编程是令人感到窒息的，是因为有经验的 C++ 程序员知道一些用 Basic 不可能表达出来的技术。同样地，学习 Lisp 不仅教你学会一门新的语言 ── 它教你崭新的并且更强大的程序思考方法。

1.2 新的技术 (New Techniques)
=================================

如上一节所提到的， Lisp 赋予你别的语言所没有的工具。不仅仅如此，就 Lisp 带来的新特性来说 ── 自动内存管理 (automatic memory management)，显式类型 (manifest typing)，闭包 (closures)等 ── 每一项都使得编程变得如此简单。结合起来，它们组成了一个关键的部分，使得一种新的编程方式是有可能的。

Lisp 被设计成可扩展的：让你定义自己的操作符。这是可能的，因为 Lisp 是由和你程序一样的函数与宏所构成的。所以扩展 Lisp 就和写一个 Lisp 程序一样简单。事实上，它是如此的容易（和有用），以至于扩展语言自身成了标准实践。当你在用 Lisp 语言編程时，你也在创造一个适合你的程序的语言。你由下而上地，也由上而下地工作。

几乎所有的程序，都可以从订作适合自己所需的语言中受益。然而越复杂的程序，由下而上的程序设计就显得越有价值。一个由下而上所设计出来的程序，可写成一系列的层，每层担任上一层的程序语言。 `TeX <http://en.wikipedia.org/wiki/TeX>`_ 是最早使用这种方法所写的程序之一。你可以用任何语言由下而上地设计程序，但 Lisp 是本质上最适合这种方法的工具。

由下而上的编程方法，自然发展出可扩展的软件。如果你把由下而上的程序设计的原则，想成你程序的最上层，那这层就成为使用者的程序语言。正因可扩展的思想深植于 Lisp 当中，使得 Lisp 成为实现可扩展软件的理想语言。三个 1980 年代最成功的程序提供 Lisp 作为扩展自身的语言: `GNU Emacs <http://www.gnu.org/software/emacs/>`_  ， `Autocad <http://www.autodesk.com.tw/adsk/servlet/pc/index?siteID=1170616&id=14977606>`_ ，和 `Interleaf <http://en.wikipedia.org/wiki/Interleaf>`_ 。

由下而上的编程方法，也是得到可重用软件的最好方法。写可重用软件的本质是把共同的地方从细节中分离出来，而由下而上的编程方法本质地创造这种分离。与其努力撰写一个庞大的应用，不如努力创造一个语言，用相对小的努力在这语言上撰写你的应用。和应用相关的特性集中在最上层，以下的层可以组成一个适合这种应用的语言 ── 还有什么比程序语言更具可重用性的呢？

Lisp 让你不仅编写出更复杂的程序，而且写的更快。 Lisp 程序通常很简短 ── Lisp 给了你更高的抽象化，所以你不用写太多代码。就像 `Frederick Brooks <http://en.wikipedia.org/wiki/Fred_Brooks>`_ 所指出的，编程所花的时间主要取决于程序的长度。因此仅仅根据这个单独的事实，就可以推断出用 Lisp 编程所花的时间较少。这种效果被 Lisp 的动态特点放大了：在 Lisp 中，编辑-编译-测试循环短到使编程像是即时的。

更高的抽象化与互动的环境，能改变各个机构开发软件的方式。术语\ *快速建型*\ 描述了一种始于 Lisp 的编程方法：在 Lisp 里，你可以用比写规格说明更短的时间，写一个原型出来，而这种原型是高度抽象化的，可作为一个比用英语所写的更好的规格说明。而且 Lisp 让你可以轻易的从原型转成产品软件。当写一个考虑到速度的 Common Lisp 程序时，通过现代编译器的编译，Lisp 与其他的高阶语言所写的程序运行得一样快。

除非你相当熟悉 Lisp ，这个简介像是无意义的言论和冠冕堂皇的声明。\ *Lisp 凌驾面向对象程序设计？* *你创造适合你程序的语言？* *Lisp 编程是即时的？* 这些说法是什么意思？现在这些说法就像是枯竭的湖泊。随着你学到更多实际的 Lisp 特色，见过更多可运行的程序，这些说法就会被实际经验之水所充满，而有了明确的形状。

1.3 新的方法 (New Approach)
=============================

本书的目标之一是不仅是教授 Lisp 语言，而是教授一种新的编程方法，这种方法因为有了 Lisp 而有可能实现。这是一种你在未来会见得更多的方法。随着开发环境变得更强大，程序语言变得更抽象， Lisp 的编程风格正逐渐取代旧的\ *规划-然后-实现* (\ *plan-and-implement*\ )\ 的模式。

在旧的模式中，错误永远不应该出现。事前辛苦订出缜密的规格说明，确保程序完美的运行。理论上听起来不错。不幸地，规格说明是人写的，也是人来实现的。实际上结果是， *规划-然后-实现* 模型不太有效。

身为 OS/360 的项目经理， `Frederick Brooks <http://en.wikipedia.org/wiki/Fred_Brooks>`_  非常熟悉这种传统的模式。他也非常熟悉它的后果：

  任何 OS/360 的用户很快的意识到它应该做得更好...再者，产品推迟，用了更多的内存，成本是估计的好几倍，效能一直不好，直到第一版后的好几个版本更新，效能才算还可以。

而这却描述了那个时代最成功系统之一。

旧模式的问题是它忽略了人的局限性。在旧模式中，你打赌规格说明不会有严重的缺失，实现它们不过是把规格转成代码的简单事情。经验显示这实在是非常坏的赌注。打赌规格说明是误导的，程序到处都是臭虫 (bug) 会更保险一点。

这其实就是新的编程模式所假设的。设法尽量降低错误的成本，而不是希望人们不犯错。错误的成本是修补它所花费的时间。使用强大的语言跟好的开发环境，这种成本会大幅地降低。编程风格可以更多地依靠探索，较少地依靠事前规划。

规划是一种必要之恶。它是评估风险的指标：越是危险，预先规划就显得更重要。强大的工具降低了风险，也降低了规划的需求。程序的设计可以从最有用的信息来源中受益：过去实作程序的经验。

Lisp 风格从 1960 年代一直朝着这个方向演进。你在 Lisp 中可以如此快速地写出原型，以致于你已历经好几个设计和实现的循环，而在旧的模式当中，你可能才刚写完规格说明。你不必担心设计的缺失，因为你将更快地发现它们。你也不用担心有那么多臭虫。当你用函数式风格来编程，你的臭虫只有局部的影响。当你使用一种很抽象的语言，某些臭虫(如\ `迷途指针 <http://zh.wikipedia.org/zh-cn/%E8%BF%B7%E9%80%94%E6%8C%87%E9%92%88>`_\ )不再可能发生，而剩下的臭虫很容易找出，因为你的程序更短了。当你有一个互动的开发环境，你可以即时修补臭虫，不必经历 编辑，编译，测试的漫长过程。

Lisp 风格会这么演进是因为它产生的结果。听起来很奇怪，少的规划意味着更好的设计。技术史上相似的例子不胜枚举。一个相似的变革发生在十五世纪的绘画圈里。在油画流行前，画家使用一种叫做\ `蛋彩 <http://zh.wikipedia.org/zh-cn/%E8%9B%8B%E5%BD%A9%E7%95%AB>`_\ 的材料来作画。蛋彩不能被混和或涂掉。犯错的代价非常高，也使得画家变得保守。后来随着油画颜料的出现，作画风格有了大幅地改变。油画“允许你再来一次”这对困难主题的处理，像是画人体，提供了决定性的有利条件。

新的材料不仅使画家更容易作画了。它使新的更大胆的作画方式成为可能。 Janson 写道：

  如果没有油画颜料，弗拉芒大师们的征服可见的现实的口号就会大打折扣。于是，从技术的角度来说，也是如此，但他们当之无愧地称得上是“现代绘画之父”，油画颜料从此以后成为画家的基本颜料。

做为一种介质，蛋彩与油画颜料一样美丽。但油画颜料的弹性给想像力更大的发挥空间 ── 这是决定性的因素。

程序设计正经历着相同的改变。新的介质像是“动态的面向对象语言” ── 即 Lisp 。这不是说我们所有的软件在几年内都要用 Lisp 来写。从蛋彩到油画的转变也不是一夜完成的；油彩一开始只在领先的艺术中心流行，而且经常混合着蛋彩来使用。我们现在似乎正处于这个阶段。 Lisp 被大学，研究室和某些顶尖的公司所使用。同时，从 Lisp 借鉴的思想越来越多地出现在主流语言中：交互式编程环境 (interactive programming environment)、\ `垃圾回收(garbage collection) <http://zh.wikipedia.org/zh-cn/%E5%9E%83%E5%9C%BE%E5%9B%9E%E6%94%B6_(%E8%A8%88%E7%AE%97%E6%A9%9F%E7%A7%91%E5%AD%B8)>`_\ 、运行期类型 (run-time typing)，仅举其中几个。

强大的工具正降低探索的风险。这对程序员来说是好消息，因为意味者我们可以从事更有野心的项目。油画的确有这个效果。采用油画后的时期正是绘画的黄金时期。类似的迹象正在程序设计的领域中发生。
