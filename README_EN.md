<h1 align="center">
  <img src="fig/pear.png" height="110"></img>
  <br>
  <a href="http://demo.webrtc.win/downloader">PearDownloader.js</a>
  <br>
  <br>
</h1>

<h4 align="center">A Downloader that Supports Multi-protocol, Multi-source and Mixed P2P-CDN</h4>
<br>

The release of [PearPlayer.js](https://github.com/PearInc/PearPlayer.js) has attracted constant attention from the industry and we have received many precious suggestions. On the one hand, we will continue maintaining and updating PearPlayer to support more extended functions. On the other hand, we will rearrange the related module that is of deeper layer, more flexible and applicable to wider areas. Besides, focused on node selection and data scheduling, we separate out multi-source transmission parts and thus form PearDownloader.js.

PearDownloader (梨享下载器) **[[Demo](http://demo.webrtc.win/)]**, serving as base download module of the [PearPlayer](https://github.com/PearInc/PearPlayer.js), combines HTTP (including HTTPS, HTTP2) & WebRTC and achieves the streaming media acceleration on Web client side, which features multi-protocol, multi-source, low latency and high bandwidth utilization. Our scheduling algorithm, based on high efficiency, can integrate data from multi nodes to form a complete file or transfer well-organised data/media stream to upper layer applications like audio & video players. Thus, PearDownloader can ensure the downloading speed while maximizing the P2P ratio at the same time.
 
 
PearDownloader aims to lower the migration cost for content providers (CP) of the present well-developed players: CP manufacturers can choose to integrate it into their own products and achieve Web P2P ability. They can also schedule the massive node sources of [Pear Fog](https://github.com/PearInc) to enjoy low-cost, high-quality sharing fog CDN service. PearDownloader supports more kinds of file types, provides more flexible scheduling algorithm & strategies and satisfies broader and more flexible business situations and needs.

<p align="center">
<a href="https://www.npmjs.com/package/peardownloader"><img src="./fig/player-arch.png" alt="arch"></a>
</p>

PearDownloader can be used by just importing `pear-downloader.min.js` to HTML via `<script>` tag. Please refer to [code example](#使用方法) or consult [`/examples/downloader-test.html`](/examples/downloader-test.html) or [get-started](docs/get-started.md) for usages.<br/>


## Features

- Client- and plugin-free because of P2P ability based on WebRTC
- Multi-protocol (HTTP, HTTPS, WebRTC), multi-source
- Support the present mainstream browsers because of the multi-source transmission ability (Fully schedule HTTP nodes when browser does not support WebRTC.)
- Support simultaneously playing and downloading of audios & videos using MSE within the browser kernel
- Self-developed scheduling algorithm ensures the downloading speed while maximizing the P2P ratio at the same time. (Users can also use their own scheduling algorithm to fulfill various situation needs.)
- No parameter needed to be entered by default (The system can self-adapt according to the video bit rate, etc.). Algorithms and parameters can be adjusted in advanced mode.
- Optional access to low cost, high availability Pear [Fog CDN](https://github.com/PearInc/FogVDN)
- Fully encrypted via TLS/DTLS by default, no DPI features; Statistical characteristics can be further eliminated using dynamic port mapping of Pear Fog pack.
- With Browser P2P ability (based on WebTorrent)


## Usages

First, use script tag to import pear-downloader.min.js：
```html
<script src="./dist/pear-downloader.min.js"></script>
```
or use CDN
```html
<script src="https://cdn.jsdelivr.net/npm/peardownloader@latest"></script></script>
```
If we want to download https://example.com/file.zip
```html
<script>
  var downloader = new PearDownloader('https://example.com/file.zip');
</script>
```

### How to accelerate your files?
The videos above has already been dispatched. So how to speed up other files? It's a piece of cake. Just add your file URL into [File distribution system](https://oss.webrtc.win/). And then you can feel free to use Pear's massive nodes to accelerate your file downloading! Please click [here](https://manual.webrtc.win/oss/) for detailed guide. (You need to add `Pear-Demo` in front of the file name, such as `Pear-Demo-file.zip`)


### Who's using PearDownloader today?

+ [Pear Limited](https://pear.hk)
+ [Lenovo China](https://www.lenovo.com.cn/)
+ [Newifi xCloud](http://www.newifi.com/)
+ [UCloud](https://www.ucloud.cn)
+ [Tencent Cloud](https://qcloud.com)
+ [Tencent X5/TBS](https://x5.tencent.com/tbs/)
+ [Tencent APD](http://www.chinaz.com/news/2016/0707/548873.shtml)

### PearDownloader Documents
- **[get-started](docs/get-started.md)**
- **[API](docs/api.md)**

### Acknowledgement
Special thanks goes to the following projects that provide some inspirations and API design references:

- [WebTorrent](https://github.com/webtorrent/webtorrent)
- [Peer5](https://www.peer5.com/#)

###  Talks

- Feb 2018 (36Kr) - [「Pear Share」practises fog computing, behind millions of fringe nodes are efficiency promotion and cost control](http://36kr.com/p/5118296.html) 
- Nov 2017 (Gold Science and Technology) - [DITING Technologies Inc. officially enters the blockchain domain and invests Pear Limited](http://www.jinse.com/blockchain/99767.html)
- Aug 2017 (IT Biggie Talks) - [Will WebRTC be the mainstream? Here comes the era of CDN crowdsourcing!](http://mp.weixin.qq.com/s/cx_ljl2sexE0XkgliZfnmQ)
- Jul 2017 (OSChina) - [PearPlayer.js - A streaming media player supports Mixed P2P-CDN](https://www.oschina.net/p/PearPlayerjs)
- Jun 2017 (Tencent Frontend Conference) - [P2P-CDN streaming media acceleration based on WebRTC](http://www.itdks.com/dakalive/detail/2577)
- May 2017 (Southern University of Science and Technology) - Edge Computing and Shared Fog Streaming
- May 2017 (Feng Chia University) - A Cooler Fruit Venture: Scaling up a Network from Cloud to Fog with Crowdsourcing
- Aug 2016 (Hong Kong University of Science and Technology) - From Cloud to Fog: Scaling up a Network with Crowdsourcing

### License

MIT. Copyright (c) [Pear Limited](https://pear.hk) and [snowinszu](https://github.com/snowinszu).

### Help and Support
E-mail: <service@pear.hk>; QQ group: `373594967`; [CP/CDN, OEM and other business cooperations](https://github.com/PearInc/FogVDN)
