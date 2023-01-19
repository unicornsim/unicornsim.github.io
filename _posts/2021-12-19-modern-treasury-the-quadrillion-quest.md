---
layout:       post
title:        "Modern Treasury：探索万亿美元的市场"
author:       "zionfuo"
header-style: text
catalog:      true
tags:
    - Modern Treasury
    - Packy McCormick
---

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071001828.jpeg)

作者：Packy McCormick
编译：庄七

> “人们大概都忘记了，软件是一门好生意。”

如果估值有任何迹象，人们肯定不会被遗忘，但在 Dimitri Dadiomov 经营的这个庞大且不断增长的市场角落里，软件是一种逆向的商业模式。金融科技公司通常希望动用这笔钱，这样他们就可以通过借贷赚取利息或通过消费赚取交换费。

也许是因为 Dimitri 的父母都在微软工作，他从小就欣赏纯粹基于软件的业务规模和雄心。所以他与 CPO Matt Marcus 以及 CTO Sam Aarons 决定建立一家 “为金融科技制造软件，但不是金融科技” 的公司。这家公司就是 Modern Treasury。

Modern Treasury 没有追求特定的垂直领域或客户，而是为任何通过银行转账转移资金的公司建立横向的软件（Horizontal Software）基础设施。它是一个数据层，而不是一个资金搬运工。是金融科技软件，而不是金融科技。

为金融科技构建软件，而不是坐在资金流中，是该公司建立的两个大的非共识决策之一。那另一个呢？

与大银行合作，而不是试图去打倒它们。

银行在这些地方抓了很多东西，但他们确实转移了很多钱。

2020 年，ACH 网络处理了 61.86 万亿美元的交易量，其中 41.7 万亿美元是 B2B 的支付。而 ACH 仅在美国运营。

![Nacha](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071003313.png)
Nacha

甚至更多的钱通过电汇流动。仅在 8 月份，就有 85.4 万亿美元通过美联储的 FedWire 系统流通，银行通过该系统相互汇款。CHIPS 是最大的私人美元清算系统，每天的交易量为 1.8 万亿美元。除了这两个系统，还有更多的清算系统，但仅这两个系统每年在全球的交易量就超过了 1 万亿美元。相比之下，信用卡的年交易量约为 4 万亿美元。

但通过银行流转资金并不是一种现代的体验。如果你最近通过一家大银行发送过  ACH 或电汇，你就能理解公司从中是什么样的体验。银行不会给他们一些神奇的软件来让这一切变得简单。大银行通常也不会制造神奇的软件。

因此，公司要么雇人处理所有的支付业务，要么建立和维护自己与银行系统的整合，以便尽可能地将一切自动化。无论是哪种方式，他们都在为这个问题投入宝贵的人力。几乎每家公司都必须做同样的事情，与同样的银行建立整合，以同样的方式对账。Matt 告诉我，“如果每个人都在构建同样的东西，并且没有软件公司为他们服务，那这对于一个创业公司来说是一个很好的成功秘诀。”

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071004262.png)

因此，这三位联合创始人创办了 Modern Treasury ，在全球银行系统中构建 API 。他们努力与银行系统进行整合并创建高质量的软件构建模块，并为 Gusto、BlockFi、Equi、Marqeta 和 Pipe 等客户提供了一个干净的 API 来支撑他们的支付业务。

仅仅三年时间，它每个月的对账金额就超过了 20 亿美元。上个月，该公司宣布完成了 8500 万美元的 C 轮融资，由 Altimeter Capital 牵头，Benchmark、Quiet Capital 和其他公司（如 Not Boring Capital ）参与。估值与每月的对账量相匹配：20 亿美元。

不过，比数量或估值更重要的，可能是 Modern Treasury 正在锁定的宝贵战略地位。他们正在建立一个几乎完美的 API 领先业务，并且可以利用其在工作流程中的位置，成为一个公司资金的记录系统。

这是 Modern Treasury 的真正目标，也是它的机会：成为在支付领域里具有现代风格的 Salesforce 。为了了解它，我们将介绍：

✔ 认识 Modern Treasury 。在不到三年的时间里从 YC 到独角兽。

✔ 支付业务？了解支付难题的所有部分。

✔ 捆绑 API-First 记录系统。一个强大的、可防御的战略地位。

✔ 大机遇: 一个新的支付网络。👀

让我们来看看 Modern。

# 认识Modern Treasury

成功的初创企业有很多途径。一些公司从一系列的曲折、试验和转折中获得了胜利，如 Discord 。其他人则沿着一条直线走向他们的北极星愿景，在创业途中意识到机会比他们预期的还要大。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071005283.png)

Modern Treasury 就属于幸运的第二阵营。它的三位联合创始人从一开始就知道他们想要解决的问题：只是他们没有意识到这个机会那多大。

Dimitri、Matt和Sam是在 LendingHome 认识的，他们建立了一个抵押贷款（Mortgage）市场，将大量的资金在不同的人手中转移。他们负责公司的支付业务，其中包括为贷款提供资金、收取每月付款、启动投资者存款、处理转账，然后对所有款项进行核对。

他们不得不雇佣员工，建立工具来连接他们的银行，管理所有以贷款形式出去的钱和以每月还款形式回来的钱，并核对他们的账目。尽管如此，他们的支付业务并没有以科技公司应有的速度发展。当他们四处寻找那些可以复制更聪明的公司时，他们意识到其他人都在做和他们一样的事情。即使是大公司也只是把问题丢给了人。

正如企业家所做的那样，他们决定建立一个解决方案。他们申请并被 Y Combinator 孵化器录取，然后开始工作。

![Sam, Matt, and Dimitri at Y Combinator](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071005574.png)
Sam, Matt, and Dimitri at Y Combinator

有趣的是：他们的申请书上写的并不是 Modern Treasury ，而是写了 Turnkey Treasury 。导致了很多人问他们为什么要为火鸡建立 Treasury 的时候，于是团队以 7 美元的价格购买了 modernntreasury.com 这个新的域名。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071007174.png)

从 YC 孵化出来后，Rafter（一群火鸡的意思，这里代指 Modern Treasury 团队）在 2018 年 8 月写了一篇帖子《 Introducing Modern Treasury 》，明确列出了他们计划解决的问题：

由于越来越多的支付操作始于软件，我们认为软件不仅仅只是启动，还应该自动监测和调节这类支付活动。

在当时，他们还给出了一个清晰、明了的价值主张：

Modern Treasury 帮助客户将银行报表与公司的业务逻辑相结合，为客户提供丰富的财务交易历史数据。

在三年后的今天，Modern Treasury 在坚持了创业的初心的同时，也将服务的范围扩展了。如今，不仅为公司提供了一个进入银行的 API ，用于电汇、ACH 和实时支付，自动对账，让公司进行持续的会计核算，而不是堆积到月末。还建立了自己的分类账（Ledger）产品，可用来追踪任何东西，从金钱到电子游戏中的积分和资产。它为像 BlockFi 这样的大型加密货币公司提供上行和下行的动力，并且通过 Signet Network 服务为加密钱包的实时支付提供支持。

而且，它正以一种难以置信的速度增长。

在去年9月，Modern Treasury 每月处理1亿美元的RPV（支付对账量，Reconciled Payment Volume）。而今年 6 月，仅花了 9 个月时间，就突破了 20 亿美元的 RPV 大关，实现了 20 倍的增长。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071010271.png)

增长是在一个较小的早期基础上实现的，公司在成长过程中需要对增长负责。当然，也需要有一些注意事项。RPV 不是一个标准的指标，但它仍然令人印象深刻。投资者也会被打动了。

在 2018 年的夏天，Modern Treasury 从 YC 获得种子轮后，Modern Treasury 于2019 年 12 月从 Benchmark 筹集了 1000 万美元的 A 轮融资，合伙人 Chetan Puttagunta 加入了董事会，这在 B2B 软件领域就像让 Michael Jordan 加入你的团队。2021 年，Altimeter 的 Ram Woo 在 1 月领投了 3500 万美元的 B 轮融资，9月领投了 8500 万美元的C轮融资，Benchmark、Quiet Capital 和老牌的 Not Boring Capital 也参与其中。在估值大幅提升的情况下，如此迅速地进行背靠背（back-to-back）融资，这通常是一个非常强烈的信号。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071010914.png)

以每月 20 亿美元的对账量计算出来 20 亿美元的估值是非常激进的，但这些都是聪明的投资者。将高价归咎于热门市场是一种懒惰的行为。他们到底看到了什么？

首先，这是一个低门槛但市场巨大的产品。没有其他任何一个行业总交易量能达到以万亿（Quadrillion）作为结算单位的，而 ACH 和电汇并没有良好的用户体验。在过去的十年中，在消费者方面通过与银行的整合使 Plaid 成为一家 150 亿美元的公司，而使接入信用卡变得容易的 Stripe 成为一个 950 亿美元的巨无霸。帮助客户与传统金融机构的合作变得简单，拥有着巨大的市场。

那么，在这样一个市场中，问题不在于机会的规模，而在于某家公司抓住机会的能力。为此，Modern Treasury 已经向投资者展示了足够的实力，在过去的三年的成绩足以让他们相信，Modern Treasury 是一个从多个方面赢得市场的可靠竞争者。

团队。拥有强大的创始团队，不仅有相关经验，而且有相关的工作经验。他们也证明了团队有能力在困难的招聘市场上招聘到顶尖人才。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071021656.png)
Modern Treasury Team

例如，在 9 月份，Shruthi Murthy 宣布她将加入 Modern Treasury 团队担任工程主管，她从 2012 年起就一直担任 WhatsApp 的工程师，最近还领导了 WhatsApp 的支付业务。Matt 告诉我公司本季度的招聘目标实际上是超前的。

Modern Treasury 团队现在有 51 人，下周还有 10 人会入职，比起 8 月份的 35 人增加了近半。但是团队质量比数量更重要。

除了这些数字，团队还具有一些妙不可言的特性。几周前，我参加了 Modern Treasury 团队每周的 Coffee Break 时间。即使是在 Zoom 上，我也能感觉到团队的正能量，而且团队提出了非常聪明的问题。一些人提出了公司的写作文化，这在我看来一直都是一个优势。

客户。建立一个公司，让越来越多的大公司委托其负责不断增加的资金，这是一个艰巨的挑战。你需要以某种令人印象深刻的方式来说服第一个客户注册，然后将其转化为下一个稍大的客户，然后是下一个，再下一个，再下下一个，一次类推。这有点像 YouTube 上的某种挑战，人们随机拿一个家用物品，试图去换取更多有价值的东西，直到他们最终得到一栋房子。

Modern Treasury 在标识方面也很强大。它帮助它的第一个客户 Sana（一家小型企业的健康福利公司）与像 Gusto、Marqeta、Revolut 和 BlockFi 等大客户建立了关系，这些企业都依赖于 Modern Treasury 所构建的模块来进行组合。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071023052.png)
Modern Treasury Clients

尤其令人印象深刻的是，Modern Treasury 与这么多金融科技公司合作，也说明了他们在软件中如同瑞士一般，是银行和公司之间的技术中立方，没有涉足资金流的野心。

这些早期的多米诺骨牌可能是最难被推倒的。他们会帮助推动更大的骨牌，而更大的骨牌会帮助推动更大的骨牌。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071032602.webp)

这并不意味着签署那些流动资金最多的公司签约（如大型保险公司、医疗保健公司、房地产公司等等）会很容易，但这确实意味着 Modern Treasury 处在最佳位置。

在最后，当然还有产品本身。像最好的软件公司一样，Modern Treasury 能够在质量和速度之间取得平衡，在不损失客户资金的情况下更新软件。这是一种 "欲速则不达 "的心态。

Modern Treasury 在其官网的中心位置说，"使支付业务简单、可扩展和安全"。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071033231.png)

这就引出了一个问题，什么是支付业务？

# 产品：支付业务软件

我必须说实话。在与 Matt 和 Dimitri 会面之前，我知道 Modern Treasury 在圈子内引起了轰动，知道它在金融科技领域做了一些事情，也知道它有自己的分类账（Ledger）产品，但我并不是真正的了解 Modern Treasury 工作原理。这是因为支付业务，就像裁判一样，是一个理想的隐形角色。

但是，支付业务使经济持续运转。Dimitri 在《 Beginner’s Guide to Payment Operations》中写道，在Indeed上列出的支付业务岗位（95,900）比会计岗位多三倍。这些岗位职责范围从服务贷款，发送、核对 ACH 和电汇付款，为医疗账单发布付款信息，以及确保国际付款顺利进行。

一般来说，支付业务包括围绕资金流动本身的所有工作流程。这包括：

✅ 发起支付

✅ 设置审批流程

✅ 跟踪和分配已发送和收到的资金

✅ 解决支付失败和退货问题

✅ 将交易与银行报表进行核对

✅ 将付款记入总的分类账

这些工作流跨越公司内部的许多系统，从银行门户到电子表格再到ERP软件。

在 Modern Treasury 之前，公司必须雇用专门的人员，甚至整个团队来管理这些所有的工作。Airbnb 需要向客人收钱，向房东付钱，处理纠纷，以及管理市场支付的所有复杂问题，它有一个完整的页面专门介绍其支付团队，其中包括了12个当前开放的岗位。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071034959.webp)
Airbnb

Airbnb 是一家非 "支付 "技术公司，它仍然需要在支付问题上投入大量的人力，包括工程师来构建内部的解决方案，以及那些实际工作的人。甚至还还会有一个内容策略师。

每个获得有真实意义收入的公司都会有支付业务，无论是设置专门的员工还是那些处理支付工作的人员的形式。这可能是一个工程师在他们建立有趣东西的同时进行银行集成，或者财务团队成员花一部分时间来发送支票和电汇，并在每个月末结账。

Modern Treasury 的存在是为了构建软件，使所有这些更快、更可靠、更高效。这是他们所做的营销版本:

<iframe width="560" height="315" src="https://www.youtube.com/embed/qaK6PwebqgI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

让我们再深入了解一下， Modern Treasury 有三个核心产品支付、虚拟账户和分类账（Ledger），包括直接对接银行、自动对账和对手交易培训等软件功能，以及与会计系统的整合。这些产品涉及公司内部的各种角色，从财务到合规到工程。它所有产品都是为了释放团队的时间，使其专注于他们的核心产品，比公司自己建立的任何软件或流程做得更快、更准确。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071035106.png)

Modern Treasury 的产品包括 API 和用户界面。在 Invest Like the Best 上，Benchmark 的 Eric Vishria 描述了 B2B 软件的两种类型：人们通过图形用户界面（GUI）与软件进行交互，软件通过 API 与软件进行交互。Modern Treasury 两者兼得。

对于大多数客户来说，它从连接银行开始。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071035124.webp)

公司可以在一个地方对接他们所有的银行账户，包括那些来自不同银行的账户，这样他们就可以通过 Modern Treasury 的简洁界面与所有的现金和支付进行交互，或者使用 API 将数据插入他们自己的软件。

在这里，一家公司可能会使用 Modern Treasury 提供的支付API来构建支付的工作流，将钱从任何一家银行的账户中直接发送给“交易对手”，或其他企业、合作伙伴，或他们需要支付或收费的客户。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071036040.webp)

重要的是，通过使用 Modern Treasury，许多企业可以跳过通过支付处理器或账单支付解决方案汇款，使支付更快更便宜。

除了更顺畅、更快速的支付，Modern Treasury 还帮助企业更好地跟踪和了解他们的支付和账户。

一旦你的银行账户被接入，Modern Treasury 可以自动核对付款将具体交易与账户中的付款相匹配。它甚至可以通过持续的会计核算来消除可怕的月末结算过程，将对账的付款和银行交易自动同步到你的总的分类账中。在这两种情况下，都需要耗费时间和人力的过程，并用软件来取代或促进它们。

最后但同样重要的是，今年 6 月，Modern Treasury 推出了自己的分类帐 Ledger 产品。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071036859.webp)

每个企业都有一个分类账，用于为贷项和借项进行逐项的记账，每个会计软件如 Quickbooks、Xero、Netsuite 等，都很适合这个用例。但是数字产品本身需要实时更新产品的分类账。想想你 Robinhood 账户里的余额， Uber 里的积分，或者是 MetaMask 钱包里 ETH 的数量，从历史上看，他们不得不建立自己的分类账。

有了 Modern Treasury 的分类账 API ，开发者这只需几行代码可以为数字钱包、投资应用服务，比如游戏代币这些需要实时存储和跟踪价值的地方建立分类账。

在与 Matt 和 Dimitri 交谈时，他们把 Modern Treasury 的各种产品描述为支付的 "构建模块"，事实确实如此，我在研究的时候，让我印象深刻的是 Modern Treasury 产品的行为更像是在做拼图。客户可以单独使用每个产品，但组合在一起的模块越多，工作反而就越简单。所有这些都有企业级控件的支持，这对大公司来说非常重要的。在理想情况下，随着 Modern Treasury 建立其产品和集成套件，客户能够转向使用一个可信的产品，来满足他们所有的支付需求。

你们应该会记得我经常引用 Jim Barksdale 的那句老话，“据我所知，这个世界上的生意要赚钱，只有两种方式：捆绑或是分拆。” Modern Treasury 认为，当涉及到支付时，捆绑是赚钱的方法。

# 捆绑 API-First 记录系统

Modern Treasury 的增长了所有新闻的头条，但它的战略定位才是真正吸引人的地方。

Modern Treasury 的 API-First 工作流，是利用杠杆原理将在 API 上流经的数据记录进系统。

当 Dimitri 告诉我，他希望 Modern Treasury 成为支付领域的 Salesforce 。我来展开解释一下。

根据 Redpoint 的 Tomasz Tunguz 的说法：

划分软件世界的一个简单方法是区分是记录系统还是工作流（workflow）应用。记录系统是特定部门或公司的唯一真实来源。另一方面，工作流应用程序使工作人员能够工作。

SaaS 的下一个转变将会看到初创企业利用其工作流（workflow）的基础，通过改变购买流程来颠覆记录系统。

这充分说明了 Modern Treasury 的战略。

首先 API-first。在《APIs All the Way Down》中，我做了一个图，我现在经常用它来描述一个典型的 API-first 业务：

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071037679.webp)

一家公司所做的任何事情都是关键任务，但非核心的地方被 API 替代是非常理想的候选。支付显然对一个企业很重要，但它们不是一个差异化的因素。正如 Matt 所解释的，我不会因为他们按时支付而把我的房子挂在 Airbnb 上，但如果他们不按时支付，我也不会在 Airbnb 上做房东。

整合银行是无差别的繁重任务。公司希望有干净的 API 和开发者工具，就像他们在其他领域使用的那样（如 Twilio），这样他们就可以专注于产品本身。

通过建立 API，使其很容易连接到银行并进行支付，Modern Treasury 已经能够把自己放到工作流里面那个非常棘手的位置。利用这一地位，在流经 API 的数据之上构建产品，如对账和分类账，使其成为公司资金的记录系统。

因此，依靠 Modern Treasury 的不仅仅是工程师，甚至是财务团队，而是公司里任何需要了解公司资金流动情况的人。Modern Treasury 并没有纯粹地成为一家 "仅提供 API "的公司；它拥有各部门人员依赖的仪表盘和工具。

Dimitri 告诉我，有一个拥有 500 名员工的客户，每月有 72 个活跃的 Modern Treasury 账户，由客户支持、工程师、产品经理、会计、审计、运营和财务团队的员工使用。工程可能会建立集成，但随后 Modern Treasury 就成了公司里任何人的唯一真实信息来源，就像 Salesforce 一样。

这使我们又回到了捆绑的问题。

前几天，Mario 和我写一个情况，企业家们并没有试图取代 Discord ，而是在它的基础上进行建设。这是一个小组对话的记录系统。尽管 Salesforce 不是产品最漂亮的，也不是体验最好的，但它作为记录系统的地位意味着，想要为销售和营销团队提供服务的企业家需要与 Salesforce 进行整合并在上面进行构建，而不是试图取代它。

同样，Modern Treasury 认为，鉴于其作为支付记录系统的地位，构建一流金融科技产品的公司与 Modern Treasury 整合，而不是试图取代它，这将是很有意义的。与 Modern Treasury 整合的公司越多，它就越有粘性，也越有可能变得非常大。

在某些情况下，Modern Treasury 会与其他公司的产品整合。在其他情况下，用户将自己构建。作为记录系统，它有能力做出这样的选择：它认为支付业务应该捆绑在一起，问题只是在建立、购买或合作间选择。如果他们想转移资金，就需要构建在 Modern Treasury 的基础上。

这就是为什么 Modern Treasury 更关注对账支付量而不是收入。能够参与对账就意味着 Modern Treasury 拥有作为记录系统所需的所有数据。

从那里，它可以去追逐真正的大机遇。

# 大机遇: 一个新的B2B支付网络

Modern Treasury 押注的是大银行将继续为世界上最大的行业服务，如医疗保健、房地产、教育、工资，制造业，以及其他那些依靠电汇和 ACH 以及实时支付（RTP，Real Time Payments）来支付大额资金的行业。

这可能是一个糟糕的赌注，现在那些非常强大的金融科技公司正在向银行发起进攻。在未来的十年里，Web3 可能会得到巨大的发展，变得更加可靠，即使是世界上最笨拙的行业也没有理由通过古老的方式传输资金。Stripe 对 Web3 的推动可能是银行终结的预兆。

但是，Modern Treasury 有两个机会摆在面前，一个是非常非常大，一个是绝对巨大。

非常非常大的机会是继续扩张，大规模地做他们过去三年一直在做的事情，并成为公司支付业务一站式的平台。这意味着与更多的银行整合，进军新的国家，扩大产品供应，整合第三方工具，成为一站式服务，并且为越来越大的客户提供服务，帮助他们巨大的资金流动量。

在这个方向上，它看起来很像 Twilio，是至关重要的基础设施，能够在每次资金流动时收取平台费和延期费用。

但是如果你相信这三个假设:

1️⃣ 银行仍然是企业转移大量资金的方式；

2️⃣ 美国像其他国家一样采用实时支付（Signet在来，CHIPS正在运行，FedNow在几年后也会上线）；

3️⃣ Modern Treasury 能够像 Stripe 对信用卡和 Twilio 对消息传递所做的那样对支付业务进行处理，成为公司支付业务实际上的解决方案。

那么 Modern Treasury 的巨大机会可能是，它可以为足够多的银行和公司提供便利的支付操作，以重建支付网络。

一旦有足够多的大额资金流动者使用了 Modern Treasury 的产品，Modern Treasury 就可以建立自己的“闭环（closed-loop）”网络，通过这个网络，企业可以实时地将资金从自己银行账户转移到对方的银行账户。

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071039823.webp)

它可以即时核对交易，促进实时支付，通过自动更新确保账本在最新状态。

随着资金流动变成数据流动，两家银行更新各自的分类账，一家与银行合作并善于移动和理解数据的软件公司，可以重构全球的支付网络。

在这种情况下，在未来 Modern Treasury 可能会变得更像是 Modern VISA。就目前而言，VISA 是一家价值 4580 亿美元的公司，但是他最初也源自于银行网络。

这是一个崇高的愿景，每家支付公司都希望能实现这一目标。但是仅仅三年的时间，Modern Treasury 似乎最有能力在这个由银行主导的万亿美元的市场中实现这一目标。现在，这是执行的问题了。

原文：https://www.notboring.co/p/modern-treasury-the-quadrillion-quest

![](https://raw.githubusercontent.com/zionfuo/img/master/2022/202210071041333.png)