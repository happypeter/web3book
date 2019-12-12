## 概述

- 初衷
  - Lee 逐渐发现自己的发明正在被滥用
    - 很多公司靠占有用户的数据，甚至出卖用户的隐私牟利。
    - Berners-Lee 认为 Web 有些基本的设计问题是需要被修复的，他自己给出的答案就是 Solid 项目。
    - 2018年 Inrupt 公司成立，专注 Solid 项目的开发。social linked data
    - 提供一系列开放标准，协议，工具，帮助大家开发去中心化应用。

- Solid 项目的口号是 Re-decentralizing the web [1]
  - 让用户真正拥有自己的数据，实际上是非常的难的
  - Solid 的愿景跟 Web3.0 是完全一致的，但是缺失了信任，是不可能实现的。

- 根据维基百科上的介绍 Solid 有两个目标
  - 用户真正拥有自己的数据
  - 更好的隐私

弱点 摆脱不了信任。

## SOLID 基本架构

- 用户的数据存储在 POD （ personal online data stores ）中，POD 具体存在哪里可以由用户自己去指定。

- Solid 应用于是可以去访问 POD 中的数据，但是必须要满足前提条件
  - POD 的主人授权了这个应用去访问 POD 中的数据
  - 可见隐私控制，完全可以由用户自己把握

- 跟 Web3.0 有大量的思想是一致的
  - 数据和应用解耦
- Solid 的组件
  - 提供了描述类似 Facebook 或者 Twitter 这样的社交应用所需的数据格式，例如评论，ID ，登录，好友管理等等。
  -  WebID [2] 身份提供者：WebID-TLS [3]
    - WebID 的愿景也是让用户持有自己的身份 https://www.w3.org/2005/Incubator/webid/spec/tls/
    - WebID-TLS 是带公钥的，跟 DID 是比较像的
    - 不理解：WebID-TLS is done without referring to Certificate Authority hierarchies, and instead encourages host server-signed (or self-signed) certificates.
      - In Solid, certificate creation is typically done in the browser using the HTML5 keygen element, to provide a one-step creation and certificate publication user experience.
      - 证书是应用自己生成的。
        - These certificates can be created by any Web Site for their users
        - https://www.w3.org/2005/Incubator/webid/spec/tls/
        - Web Of Trust 的思路
        - 不需要依赖 CA without needing to rely on this being signed by a well known Certificate Authority

- POD 中的数据格式是 Linked Data
  - Linked Data 是更早的 Berners-Lee 提出的语义网的思想
  - 数据按照互联网公开标准存放，这和 Web3.0 是一致的。
  - 我的 POD 中存放这我的一章照片
  - 而你评论了我的照片，于是这个评论存放在了你的 POD 中
  - 这二者之间会按照 Linked Data 的方式进行链接
  - 从 Solid 官方文档[4]上可以找到一个非常容易看懂的例子。
    - 问题：如何验证评论的发布时间和是否伪造（防止水军）


- 个人持有数据和去信任是一个硬币的两面。
  - 公司持有数据的时代，公司可以提供信任
    - 我在知乎上发布一篇文章，知乎记录了我的 ID 和发布时间，所以可以证明这篇文章的确是我的
    - 支付宝我给你转一块钱，支付宝数据库会记录这次转账
  - 个人一旦持有数据了
    - 如何证明我是我？ID 系统
    - 如何证明我的数据属于我？
      - 如何证明发布时间和发布人
      - 如何证明我自己没有篡改过我的数据
    - 如何安全的存储我的数据？

- 优势
  - 满足 Web3.0 的第一个特征：数据归个人持有
  - 基于互联网协议和标准
  - Solid 要做的核心的一件事就是让数据归用户控制
    - 解除 App 和数据的耦合
    - freedom to exit
  - 拥有数据
    - Pod 是一个可编程的网盘，数据都在里面
    - A 应用可以用这个 Pod 里面的数据，B 应用也可以
  - 控制数据
    - 我自己决定，哪些服务提供商可以读取我的数据

    - Solid 是互联网的数据层和身份层
      - 应用开发者不需要自己的数据库了

- Solid 的核心分为三点：Social Linked Data


## 弱点1：ID 基于信任
- ID 还是基于信任
  - WebID
  - 一旦 WebID 的提供者下线，那么所有的 POD 中的数据都没有了主人

- 与商业利益冲突
  - 为何要开放我的数据？

  - 使用 Solid 登录
    - 唯一的身份
    - 登录任意 Solid 应用

- Solid 用户 ID
  - 应该是使用第三方 https://github.com/inrupt/solid-react-sdk#user-authentication
  - 有两种方式实现 ID
    - 一种是 password 方式
      - 这种要基于对 Solid 项目服务器的信任
        - https://github.com/solid/webid-oidc-spec#brief-workflow-summary
    - 另一种是 WebID-TLS 
      - 基于 CA 证书

Your public Solid POD URL will be: https://happypeter.inrupt.net

Your public Solid WebID will be: https://happypeter.inrupt.net/profile/card#me


- Solid 和 Web3.0 
  - Web3.0 不仅仅要保证数据持有在用户手里，更要保证确权
    - 如何证明一个评论是我发的，发在哪里，什么时间发布的？
    - 一篇公开博客如何证明是我发表的
  - Solid 似乎更强调开放共享，对确权很不清晰
    - 不能确权就不能防止伪造和滥用

参考：

- [1] https://github.com/solid/solid
- [2] https://www.w3.org/2005/Incubator/webid/spec/identity/
- [3] https://www.w3.org/2005/Incubator/webid/spec/tls/
- [4] https://solid.inrupt.com/docs/intro-to-linked-data
