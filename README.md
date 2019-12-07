# web3book

- 第一章 技术发展的去中心趋势
  - 硬件的去中心化
  - 软件的去中心化
  - 网络空间独立化趋势
- 第二章 为何 Web3.0 是去中心化的？
  - Web 架构的迭代
  - 智能合约全球愿景
    - 高阶：DAO
  - 数据民主化
    - 数据即我
    - 互联网公司的监管噩梦
      - 持有用户数据，也同时意味着对数据隐私负责，想想 Facebook
      - 如果用户自己持有，公司就不必承担这部分责任了
    - 自由数据市场
    - 区块链的启示
  - 打破网络效应
    - 网络效应之恶
    - 垄断形成的根源
    - 从“不作恶”到“不能作恶”
  - Lee 的 Web3.0 架构的弱点
    - 语义网
    - RSS 的没落
    - 互联网之父的 Solid 项目
      - Solid 大有可以借鉴的内容
  - 密码学和互联网隐私
    - 密码学圣战
    - 密码朋克运动
    - 隐私即安全
  - 区块链为何可以作为信任之根？
    - 密码学
    - 机器共识
      - 比特币
      - POW 原理
  - 机器共识
    - 去中心化共识 POW vs POS
    - 机器共识取代人类共识
      - 基于数学做判断 vs 基于人文，价值观做判断
  - 带状态的协议 Stateful Protocols
    - https://blockchainhub.net/web3-decentralized-web/

第三章 Web3.0 架构组件
  - 把一个 Web2.0 应用升级到 Web3.0
  - 去中心化的电商防刷单
    - 真正绝对避免是不可能的
    - 但是情况不会币中心化监控条件下糟糕
    - 因为可以通过追加成本，来增加刷单的难度
      - 本身注册 DID 就是要写入区块链的，就是要花钱的
      - 也会对 DID 在整个网络上的行为做分析，如果这个 DID 是新创建的，没有任何信誉屏障，那么降低这个 DID 发布的信息的关注度
        - 任何信誉，都是要有某个第三方给签名的，所以获得是有真正成本的
  - 去中心化身份
    - 为何需要去中心化身份
      - DID also called Self-Sovereign ID
    - 如何实现认证
    - 如何实现授权
    - 实际项目
  - 去中心化支付
    - 比特币
    - 隐私币
    - 稳定币
  - 去中心化存储
    - HTTP 的中心化问题
    - 按内容寻址
    - 去中心化的 DNS
    - DNS 的中心化现状
  - 去中心化 DNS 的基本原理
  - 去中心化的 CA 和 PKI
    - 公钥密码学的局限
    - 数字证书的作用
    - 发证机构 CA 
    - 去中心化 PKI 的实现原理

第四章 去中心化身份
  - 何为用户 ID ？
    - https://didproject.azurewebsites.net/docs/overview.html
    - 虚拟的我
    - 目前割裂在各个巨头 App 中
    - 完全自持有
  - W3C 的 DID 标准
    - 数据结构
    - 去中心化标识符
    - 绑定公钥
    - 认证策略
  - DID 案例
  微软的 Ownyouridentity 项目
    比原链的去中心化身份架构
    亦来云的去中心化身份架构
    波卡的去中心化身份架构
    去中心化 ID 基金会
  - 从密码到私钥
    - 从登录到授权
    - 生物信息识别的局限
    - 密码的局限
    - 算力消耗是唯一的安全屏障
  - 人性化设计
    - https://tor.us/
    - blockstack 的 ID 命名空间
    - https://sovrin.org/
    - ID As A Service
第五章 去中心化支付
  - 互联网的原生支付层
  - Token 经济
  - 可编程的价值
  - 原生激励
  - 资源定价
  - Hashcash
  - DDos 攻击的防范
  - 比特币
  - 比特币的隐私
  - 硬顶的智慧
  - 基于计算机共识的货币发行
  - 隐私币
  - Grin
  - 门罗币
  - Zcash
  - 稳定币
  - 央行数字货币和人民币的区别
  - 稳定币和法币的区别
  - MakerDAO 和 DAI
  - Defi 去中心化金融
  - USDT 和其他
第六章 去中心化存储方案
  - 用户自控制的存储
  - 为何要自己持有
  - 数据资产确权
  - 数据和  App 的分离
  - 区块链和自控制存储的分工
  - 哈希上链
  - 时间戳服务
  - 去中心化可信签名
  - 从 HTTP 到 IPFS
  - 代币激励
  - 碎片化存储
  - 半中心化存储
    - Blockstack 的 Gaia 系统
    - 加密后存储到普通云服务

第七章 去中心化的 DNS 和 PKI
  - 加密通信原理
    - 公钥和私钥
    - 无秘密加密
    - 数字签名
    - HTTPS 基本原理
    - 混合加密策略
    - 数字证书
    - 发证机构 CA
      - https://en.wikipedia.org/wiki/Chain_of_trust
    - 中间人攻击
    - CA 如何去信任化
    - Web Of Trust
      - https://sovrin.org/
    基于区块链的信任
    案例
    Namecoin 区块链
    IPFS 的去中心化域名服务
    以太坊的去中心化域名服务
    Blockstack 的命名系统
第八章 Web3.0 之上的 App 架构
  DApp 是什么？
  无平台方的平台
  用户自持数据
  DApp 架构原则
  胖协议
  用户为中心的设计
  从 App 到 DApp 
  无大型数据库
  无服务器
  从服务器端代码到智能合约
  去中心化登录认证系统
  可编程代币资产
DApp 的分层结构
区块链层
存储层
认证层
SDK 层
DApp 的用户体验优势
退出的自由
定制客户端的自由

第九章 Web3.0 时代的商业模型
  - 去中心化经济激励
    - 比特币模式的众筹
      - https://happypeter.github.io/binfo/bitcoin-funding
    - 商业模型之谈一个字：钱
      - 标准化组织，如何拿到钱
  - 区块链永动机机制设计
    - 经济模型闭环
    - Blockstack 的经济模型
    - Nervos 的通胀税模型
  - 从信任到验证
  - 去中介化
  - 去中心化的经济学：市场为王
    - 奥派经济学
  - 标准化组织的钱
  - 相信人到相信数学
  - 从监管到验证
  - 信任之根
    - Chain Of Trust
    - 自持数据的权威性
  - 从权威存储到权威签名
  - 时间戳服务器
  - Web of Trust
  - 数据的商业价值
  自处理获取有用结论
  主动发布获取有用服务
  - 售卖特定数据获取收益
    - https://neilpatel.com/blog/behavioral-advertising/


  零知识证明保护隐私

第十章 Web3.0 实战 -- Blockstack
  - 创建 Blockstack ID
    - 注册账号
    - 申请 ID
    - 底层原理
      - 给去中心化 ID 一个友好的用户名
      - OpenBarzzar 是一个案例：https://www.youtube.com/watch?v=_ai0fXJUoo8
    - 单点登录
  Gaia 数据存储系统
  申请空间
  存储数据
  安全策略
  React 前端编程框架
Hello World
完成登录功能
与 Gaia 交互
Clarity 智能合约编程
为何要图灵不完备
编写智能合约
与 React 客户端交互
Web3.0 版本的 Twitter
数据如何存储
朋友关系的建立
实时性
私钥签名授权

第十一章 结语
  - 个人的崛起
    - 个人即机构
    - 机器赋能个人
    - 机器共识

如今的万维网（互联网）主要存在两大缺陷：

- 它不会保留独立于可信的运营者的“状态”
- 它没有一个原生机制来实现状态转移
 
Web2.0 的事实几乎没有例外的是来自私人的服务器，Web3.0 时代，私人服务器依然可以作为事实的来源之一，但是经过某种程度共识的存储媒介（公有链，或者联盟链）也必将找到自己的角色。

## 人们对 Web3.0 的理解都不一样

“人们不停地质问 Web 3.0 到底是什么。我认为当可缩放矢量图形在 Web 2.0 的基础上大面积使用——所有东西都起波纹、 被折叠并且看起来没有棱角——以及一整张语义网涵盖著大量的数据，你就可以访问这难以置信的数据资源。”

                             —Tim Berners Lee(2006-5)

“Web 1.0 是拨号上网，50K 平均带宽，Web 2.0 是 1M 平均宽带，那 Web 3.0 就该是10M 带宽，全视频的网络，这才感觉像 Web3.0。”

—- Netflix 创始人 Reed Hastings(2006-11)

“(Web 3.0)创建应用程序的方法将不同。到目前为止 Web 2.0 一词的出现主要是回应某种叫做“AJAX”的概念……而对 Web 3.0 我的预测将是拼凑在一起的应用程序，带有一些主要特征:应用程序相对较小、数据处于 Cloud 中、应用程序可以在任何设备上运行(PC 或者移动电话)、应用程序的速度非常 快并能进行很多自定义、此外应用程序像病毒一样地扩散(社交网络，电子邮件等)。”

— 谷歌首席执行官EricSchmidt(2007- 8)

https://blog.csdn.net/shangsongwww/article/details/90269519


- https://blog.csdn.net/weixin_44383880/article/details/90823832


## 各种去中心化技术

- Internet 的发展
  - Email 技术 SMTP
  - TCP/IP 的去中心化思想
- Web 的去中心化思想
- BT 和 GIT 的胜利

## Web 和 区块链 的融合

- 用私钥，去加密我们的 Web 数据
  - 并且可以去使用数字资产
- 信息和资产和钱就成为了一类东西
  - 只要你有私钥，这些东西就是你的
    - 注意是直接属于你，而不需要基于第三方
      - 这一点是非常让人激动的

# Zero Knowledge

Non-interactive ZKPs for privacy and scalability

# 协议

互联网的本质是一系列的游戏规则，或者术语叫做协议，W3C https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force 这些协议的制定。

RFC 是允许公开讨论的。

Linux 的网络模块和 Chrome 浏览器是规则的载体。

浏览器直接链接的是 ISP 。

> The terms Internet and World Wide Web are often used interchangeably in everyday speech;

- https://en.wikipedia.org/wiki/Internet

- TCP/IP intro
  - https://www.bilibili.com/video/av5139978?from=search&seid=9702015957132993653

- https://www.youtube.com/watch?v=gkJqMSbI1IA&feature=em-lsp
  - 假名经济
    - 不是真实姓名，但是也是你的长期代号
    - Twitter 上很多人都是用假名，但是这些假名也可以用来构建声誉和信用
    - 中本聪也是个假名

- https://www.youtube.com/watch?time_continue=384&v=E-IaSS0bbGU
  - 比特币是自由主义者的愿景--彼得蒂尔

## 写作规范

- 每个小节分三部分
  - 写3000字
  - 开头一段是一个问题，最后一段是对这个问题的答案
    - 中间各个部分是对这个问题的展开回答

- 技术书要有个技术书的样子
  - 很多人文政治理念或者故事，都要一笔带过
    - 自由主义
    - 密码朋克运动
    - 数字空间独立思想
    - 如果一个小节的内容，不能画出框图，或者时序图，基本上可以认为这一节不是技术内容
      - 不是技术内容的，不能单独做为一个小节出现
    - 但是《碳基硅基世界解耦》这样的话题，还是非常技术性的，可以写
  - 不要讨论太多超前的区块链技术
    - 多聊清楚 Web2.0 的架构，这样大家才清楚要升级的是哪些组件
    - 区块链的颠覆性体现在哪里
      - POS 还是 POW
      - 公共数据库
- 章节格式
  - 按照《图解密码学》就可以
  - 每章多个小节，小节标题是 11.1， 11.2 这样，除了每章第一小节《概述》之外，其他的每个小节都对应我的一篇 binfo 文章。每个文章的每部分对应 11.1.1 11.1.2 这样的标题
    - 每个小节一定要对应一篇文章，保证立意鲜明，言之有物
- 引用格式
  - 暂时参考：https://courses.csail.mit.edu/6.857/2014/files/19-fromknecht-velicann-yakoubov-certcoin.pdf
  - 使用 [1] [2] 这样的序号
