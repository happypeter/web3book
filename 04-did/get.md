## Getting started with DIDs

把 DID 跟目前现有的身份系统做一下比较，能让我们更好的理解 DID 。现在的很多网站，要么通过 email 注册，要么是手机号，要么是用一个社交网络的用户名注册，例如，用微信账户登录其他网站 。这些方式比起 DID 来要更方便，容易记住。但是缺点也是明显的，如果 email 或者手机号被停用了，或者微信号被封了，那么我们的账户也就没有了，或者说就是身份标识就丢失了。丢失的原因就是这些身份标识都是基于别人中心化系统的，不是用户自己持有的。DID 就不一样，DID 是用户自己生成的，保存在区块链这种不被任何人控制的存储媒介上，没有任何人能够关停和删除我们的 DID 。

## 如何获取一个 DID ？

如何获取一个 DID 呢？首先需要一个完全受自己支配的硬件，例如自己的手机，然后在上面安装一个 DID 的客户端 App 。所谓客户端就是可以方便我们使用一个系统的软件，例如浏览器就是方便我们使用 Web 的客户端。DID 客户端可以帮助用户管理和使用 DID ，包括创建 DID ，实现认证，数据加密，保存密钥和管理授权。DID 和 DID 文档要保存到区块链上，但是身份数据要保存到链下数据库中。

## DID 和个人数据库交互

## 在 DID 之间建立信任

世界上的每个人都可以自由的创建 DID ，那么如何判断一个 DID 身份是不是假的呢？一个 DID 就跟一个人的个人声誉一样，在最初的时候都是空的，没有任何证据能证明这个 DID 是可信的。一个 DID 的声誉，或者可信度，来自其他可信的人的推荐。而通过可验证证书，就可以完成这种推荐。可验证证书，就是一个或者多个 DID 签署的，用来证明另外一个 DID 的一些属性的证书。一个可信的人对一个 DID 给出一个推荐，任何人都可以验证这个推荐的确是这个可信的人发出的。随着收到的推荐越来越多，一个 DID 的声誉和可信度也就越来越高。例如，一个大型可以可以去签一个证书，证明一个 DID 对应的人名字叫做 Peter ，并且他是一个在校生。

## 通过 DID 进行认证

DID 可以有不同方式跟一个 App 进行交互，但是最基本的交互形式就是认证。要对一个 App 验证一个 DID ，首先 DID 持有人要对 App 公开者个 DID 。App 会去区块链上查找者个 DID 和它对应的公钥。接下来 App 会基于 DID 的公钥，要求 DID 持有人展示他拥有对应私钥的数学证据，例如，App 会加密一段信息，发送给持有人，要求持有人将解密后的内容发送回来，或者 App 发送一小段信息给持有人，要求持有人签署这个信息，然后用 DID 绑定的公钥来验证这个签名。总之，如果持有人成功证明了自己是持有私钥的，就可以认证这个持有人的确是 DID 的所有者。

图：https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE2DjfY Managing permissions for data access

## 数据的同步和拷贝

DIF Identity Hub （后面简称 DIH ）的一个核心特点是可以让用户方便的启动多个数据库，而且很容易的在各个数据库之间同步数据。同时，要注意 DIH 是一套开源代码，你可以在任意的自己的机器上部署代码，来搭建一个 DIH 服务器，或者可以付费使用一些 DIH 提供商的服务器。总之，你的数据你做主，没有任何人能控制。

存储到 DIH 服务器上的数据是遵从统一规范的，并且会有统一的 API 提供出来。所以开发者可以开发遵从规范的 App 来和 DIH 上的数据进行交互。另外，每个人都会主动的去公开一部分自己的数据，来增强自己的声誉，或者享受某些服务器，例如，我会公开我的博客，出租信息，某些项目经历，来方便我的粉丝，租客，或者雇主来找到我。不管 DIH 服务器在哪里，整个网络都能很容易的找到这些服务器，拿到用户公开的数据，这样，这些数据就会形成一个全网通用的，符合统一规范的公开数据层，这将是一个巨大的公共财物。


## DIF Identity Hub 

下面来介绍一下 DIH 的一些概念。

什么是一个 DIH 呢？

在去中心化身份系统中，身份标识和公钥是存在区块链上的。但是个人数据并不存在区块链上，因为区块链本身存储比较昂贵，另外就是一旦存上去之后，就可以由所有人看到了。所以我们需要其他的方式来存储这些数据，DIH 就是解决方案。

DIH 是赋予了用户个人完全的对数据的控制权的一种去中心化的链下数据仓库。用户可以把自己的私人数据，例如，私人文档，联系人名单，身份数据等等，存到一个 DIH 中，这样，任何人不经过主人授权都无法访问到这些数据。主人可以在暴露最少量的隐私的条件下跟其他的人或者 App 共享数据来完成工作。App 方其实会喜欢这种模式的，因为 App 不需要自己保存用户数据了，也避免了承担数据泄露带来的风险。

DIH 跟传统的数据仓库相比有一些明显的特征。下面咱们来看看用户如何对 DIH 中的数据实现有效控制。

如何让一个 DIH 变得去中心化呢？

首先，所有的 DIH 都遵照统一的规范进行数据的读和写。用户可以在任何地方运行自己的 DIH ，而不会对任何厂商形成依赖。每个 DID 文档中都可以在 `service` 字段下面保存执行 DIH 的指针。例如

```js
{
  "document": {
    "@context": "https://w3id.org/did/v1",
    "publicKey": [
      {
        "id": "#key-1",
        "type": "Secp256k1VerificationKey2018",
        "publicKeyJwk": {
          "kty": "EC",
          "kid": "#key-1",
          "crv": "P-256K",
          "x": "Y4ezHen9MPuJcowKwhc9jT1owEzNb65BMUqtS7NH_C8",
          "y": "wWDGd0PHYjIGRcP9owNvsSLYWzSbFLuCKE8KX75KFRY",
          "use": "verify",
          "defaultEncryptionAlgorithm": "none",
          "defaultSignAlgorithm": "ES256K"
        }
      }
    ],
    "service": [
      {
        "id": "IdentityHub",
        "type": "IdentityHub",
        "serviceEndpoint": {
          "@context": "schema.identity.foundation/hub",
          "@type": "UserServiceEndpoint",
          "instance": [
            "did:test:hub.id"
          ]
        }
      }
    ],
    "id": "did:ion-test:EiDDNR0RyVI4rtKFeI8GpaSougQ36mr1ZJb8u6vTZOW6Vw"
  },
  "resolverMetadata": {
    "driverId": "did:ion-test",
    "driver": "HttpDriver",
    "retrieved": "2019-05-10T20:07:17.489Z",
    "duration": "152.6719ms"
  }
}
```

App 们就可以通过这个指针去获取 DID 对应的数据了，而不用管这个 DIH 到底托管到哪里了。

DIH 的标准 API 有一些不同的接口，可以用于不同目的，包括：

- Collections 这个接口是主要用来存储私人数据的，是 DIH 最主要的一个接口。用户数据都应该用这个接口去存储。
- Profile 这是一个特殊的 collection ，里面保存的是 DID 的元数据，也就是一下描述 DID 的数据。例如，DID 的类型（用户，组织或者其他），名字，联系方式等等。
- Permissions 顾名思义，是用来管理访问权限的。

当开发者要基于 DIH 的数据进行开发的时候，可以选择上面之中适合自己的接口。大部分时候大家都会使用 collections 接口。

跟传统的数据库不同，DIH 的存储数据没有固定的 schema ，也没有固定的数据类型。DIH 遵从 Semantic data model 语义数据模型。数据本身和描述数据的元数据是一起存放的。例如

```js
{
  "@context": "http://schema.org",
  "@type": "MusicPlaylist",
  "name": "Classic Rock Playlist",
  "numTracks": "5",
  "track": [
    {
      "byArtist": "Lynard Skynard",
      "duration": "PT4M45S",
      "inAlbum": "Second Helping",
      "name": "Sweet Home Alabama",
    }
  ]
}
```

在这个例子里面，`@context` 和 `@type` 这些元数据字段，告诉大家这个数据是一个音乐播放列表。DIH 会把这个播放列表和其他的同类型的播放列表都存到 `Collections` 中。不同的 App 都可以添加播放列表，只要大家都遵从相同的数据格式。数据格式的规范都在 schema.org 这样的地方标准化了，大家只要一起遵守就好。

每个保存到 DIH 中的文件都是由多个 commit 组成的。commit 是 git 的术语，意思就是版本。每次都文件的修改就对应一个版本。读取一个文件的时候，需要读取所有的 commit ，然后按照循序把这些 commit 累加，得到文件。

使用这种思路保存文件是有非常多的优势的：

- 让一个用户的不同 DIH 之间同步数据变得容易。
- 每个 commit 都可以单独被 DID 签署，整个文件的改版历史也都记录的很清楚。
- 这样，如果用户有时候做一些离线操作，那么跟其他的在线 App 的改动发生冲突了，融合这些冲突也变得很容易。

commit 的具体结构给文件指定的策略有关。目前，DIH 只支持一种策略，名叫 `basic` 。每个 commit 都把汗完整的数据和元数据。类似

```js
// Commit 1
{
  "@context": "http://schema.org",
  "@type": "MusicPlaylist",
  "@committed_at": "2019-02-12T22:15:22Z",
  "name": "Classic Rock Playlist",
  "numTracks": "1",
  "track": [
    {
      "byArtist": "Lynard Skynard",
      "duration": "PT4M45S",
      "inAlbum": "Second Helping",
      "name": "Sweet Home Alabama",
    }
  ]
}
```

```
// Commit 2
{
  "@context": "http://schema.org",
  "@type": "MusicPlaylist",
  "@committed_at": "2019-02-12T22:16:47Z",
  "name": "Classic Rock Playlist",
  "numTracks": "0",
  "track": []
}
```

```
// Commit 3
{
  "@context": "http://schema.org",
  "@type": "MusicPlaylist",
  "@committed_at": "2019-02-13T22:16:47Z",
  "name": "Classic Rock Playlist",
  "numTracks": "1",
  "track": [
    {
      "byArtist": "Jimi Hendrix",
      "duration": "PT4M45S",
      "inAlbum": "Axis: Bold As Love",
      "name": "Castles Made of Sand",
    }
  ]
}
```

`basic` 策略下，最新的 commit 其实就是文件的最新状态。

未来很可能会退出其他的策略。

对数据的访问权限控制是通过 `Permissions` 接口完成的。DID 所有人可以通过创建 PermissionGrant 文件来给其他 DID 赋予各种访问权限。例如

```
{
  "@context": "https://identity.foundation",
  "@type": "PermissionGrant", 
  "owner": "did:example:abc123",
  "grantee": "did:example:xyz456", // who is being granted access
  "context": "https://schema.org",
  "type": "MusicPlaylist", // what objects are being accessed
  "allow": "-R--", // allows create, read, update, and delete
}
```

`PermissionGrant` 文件跟其他文件的格式是一样的，可以通过 `Permissions` 接口访问到。上面例子中国，文件创建之后 `did:example:abc123` 就有了读取所有播放列表的权力了。当前权限可以以更细的粒度去赋予给其他 DID 。

另外，DIH 还提供的在不同实例间进行同步数据，以及加密数据的功能。数据传送过程中，可以用 DIH 自带的公钥进行加密。
