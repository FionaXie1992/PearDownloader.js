<h1 align="center">
  <img src="fig/pear.png" height="110"></img>
  <br>
  <a href="http://demo.webrtc.win/downloader">PearDownloader.js</a>
  <br>
  <br>
</h1>

<h4 align="center">A Downloader that Supports Multi-protocol, Multi-source and P2P-CDN</h4>
<br>

The release of [PearPlayer.js](https://github.com/PearInc/PearPlayer.js) has attracted constant attention from the industry and we have received many precious suggestions. On the one hand, we will continue maintaining and updating PearPlayer to support more extended functions. On the other hand, we will rearrange the related module that is of deeper layer, more flexible and applicable to wider areas. Besides, focused on node selection and data scheduling, we separate out multi-source transmission parts and thus PearDownloader.js is formed.

PearDownloader (梨享下载器) **[[Demo](http://demo.webrtc.win/)]**, serving as base download module of the [PearPlayer](https://github.com/PearInc/PearPlayer.js), combines HTTP (including HTTPS, HTTP2) & WebRTC and achieves the streaming media acceleration on Web client side, which features multi-protocol, multi-source, low latency and high bandwidth utilization. Our scheduling algorithm, based on high efficiency, integrates data from many nodes to form a complete file or transfers the well-organised data/media stream to upper layer applications such as audio & video players. Thus, PearPlayer can ensure the downloading speed while maximizing the P2P ratio at the same time.
 
 
PearDownloader aims to lower the migration cost for content providers (CP) of present well-developed players: CP manufacturers can choose to integrate it into their own products and achieve Web P2P ability. They can also schedule the massive node sources of Pear Fog to enjoy low-cost, high-quality sharing fog CDN service. PearDownloader supports more kinds of file types, provides more flexible scheduling algorithm & strategies and satisfies broader and more flexible business situations and needs.

![multisources](fig/fogvdn_multisources.png)

`pear-downloader.min.js` can be imported with the html label`<script>`, refer to  [code example](#使用方法), also [`/examples/download.html`](/examples/download.html) can help you. 

To know more information [API document](docs/get-started.md).<br/>

### Feature

- P2P based on **WebRTC**, no plug in
- **Speed up**, reliable
- Multi-protocol (HTTP, HTTPS, WebRTC), multi-source
- No parameter
- Saves data usage
- Supports all well-known browsers
- Supports [Pear Fog CDN](https://github.com/PearInc/FogVDN)
- Encoded with TLS/DTLS, no DPI feature; Pear Fog dynamic port mapping
<br>
Demo: https://demo.webrtc.win/pear/downloader/


## Quick Start

### Import the js packet
use script label to import pear-downloader.min.js：
```html
<script src="./dist/pear-downloader.min.js"></script>
```
or

```html
<script src="https://cdn.jsdelivr.net/npm/peardownloader@latest/dist/pear-downloader.min.js"></script>
```
suppose we want to download（/tv/pear001.mp4）
```html
<script>
/**
 * first parameter is the file's URL
 * opts is optional parameter
 */
var downloader = new PearDownloader('/tv/pear001.mp4', opts);
</script>
```
Congratulations! You can use the PearDownloader now!

### Who is using Pear Downloader today?

+ [Pear Limited](https://pear.hk)
+ [Lenovo China](https://www.lenovo.com.cn/)
+ [Newifi xCloud](http://www.newifi.com/)
+ [UCloud](https://www.ucloud.cn)
+ [Tencent Cloud](https://qcloud.com)
+ [Tencent X5/TBS](https://x5.tencent.com/tbs/)

### Pear Downloader document
- **[get-started](docs/get-started.md)**
- **[API](docs/api.md)**

### Thanks


- [WebTorrent](https://github.com/webtorrent/webtorrent)
- [Peer5](https://www.peer5.com/#)

###  Talks

- 2018.02.07 （36Kr） - [「Pear梨享」让雾计算落地，百万边缘节点的背后是提高效率和成本控制](http://36kr.com/p/5118296.html) 
- 2017.08.18 (IT Talks) - [WebRTC会成主流吗？众包CDN时代到了！](http://mp.weixin.qq.com/s/cx_ljl2sexE0XkgliZfnmQ)
- 2017.07.11 (OSChina) - [PearPlayer.js —— 混合P2P-CDN的流媒体播放器](https://www.oschina.net/p/PearPlayerjs)
- 2017.06.24 (Tencent Frontend Conference] - [基于WebRTC的P2P-CDN流媒体加速](http://www.itdks.com/dakalive/detail/2577)
- 2017.05.17 (SUSTech) - Edge Computing and Shared Fog Streaming
- 2017.05.08 (FCU) - A Cooler Fruit Venture: Scaling up a Network from Cloud to Fog with Crowdsourcing
- 2016.08.17 (HKUST) - From Cloud to Fog: Scaling up a Network with Crowdsourcing

### License

MIT. Copyright (c) [Pear Limited](https://pear.hk) and [snowinszu](https://github.com/snowinszu).

### Service
E-mail: <service@pear.hk>; QQ group：`373594967`; [Business](https://github.com/PearInc/FogVDN)
