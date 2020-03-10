> この記事は[WebXR](https://ja.wikipedia.org/wiki/WebXR)から翻訳されています。


**WebXR**（ウェブエックスアール）とは、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でデバイスの位置，向き，[加速度](../Page/加速度.md "wikilink")などの情報を取得するために用いられていた[JavaScript](../Page/JavaScript.md "wikilink")の[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink")（API）である。WebVR Device APIから用途をARまで広げた[WebXR Device APIへの置き換えが進行している](../Page/WebXR_Device_API.md "wikilink")。

## 歴史

WebVRは，2014年の春に[Vladimir Vukićevićによって提唱された](https://ja.wikipedia.org/wiki/:en:Vladimir_Vukićević "wikilink")。2016年3月1日に WebVR API version 1.0、 2017年12月12日にversion 1.1がリリースされた。

WebVR APIの開発は終了しており、バーチャルリアリティ（VR）と[拡張現実](../Page/拡張現実.md "wikilink")（AR）の両方に対応した[WebXR Device APIに置き換えられる予定である](../Page/WebXR_Device_API.md "wikilink")\[1\]。2019年4月23日にWebXR Editor's Draftが公開された\[2\]\[3\]。2019年12月現在、Google Chromeは[WebXR Device APIをデフォルトでサポートしており](../Page/WebXR_Device_API.md "wikilink")、Chrome80にてWebVR APIは廃止される可能性が示唆されている\[4\]。

## 特徴

### 開発者側

WebXRを利用してWebページを作成することで、外部デバイスとしてVR[ヘッドマウントディスプレイ](../Page/ヘッドマウントディスプレイ.md "wikilink")（HMD）やスマートフォンを認識できる。さらには[ジャイロセンサ](https://ja.wikipedia.org/wiki/ジャイロセンサ "wikilink")やポジショントラッキング等の情報を取得することで、位置や姿勢、目の瞳孔間距離などのHMDの状態・情報を知ることが可能になる。またコントローラーに限定すると、WebVR APIではなくGamepad APIによってコントローラーの情報を取得する\[5\]。

### 利用者側

WebXR APIを使うことで、利用者はWebブラウザからアクセスするだけでVRコンテンツが体験・利用できる。これによりURLをシェアするだけで他人に体験してもらうことができる。Webブラウザを入り口とするXR体験ということは、HMDのようなデバイスが必須であったこれまでのVR/AR体験とは異なり、デバイスを限定しないということを意味する\[6\]。VR/ARは3Dを取扱うため、モバイル端末やスタンドアローンのHMDからアクセスした場合には、3Dの[レンダリングに負荷がかかり処理が追いつかないことがある](../Page/レンダリング_\(コンピュータ\).md "wikilink")。しかし、[第5世代移動通信システム](https://ja.wikipedia.org/wiki/第5世代移動通信システム "wikilink")である5Gのサービス提供が2020年に始まる\[7\]\[8\]ことで、「サーバー側で3Dレンダリングの処理を行い、モバイル端末では処理結果を表示する」仕組みで、低スペックの端末でも利用できることで、WebXRの活用の幅が広がると期待されている\[9\]\[10\]。

## セキュリティー

WebVRはデバイスの動きや方向を取得するAPIであるが、ユーザーの同意なくセンサー情報にアクセスできる可能性があることから、[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")では2019年3月25日に提供されたiOS 12.2より[safari](https://ja.wikipedia.org/wiki/safari "wikilink")の設定「モーションと画面向きのアクセス」がデフォルトでオフとなった。これにより、ユーザーが自ら設定をオンとするか、ブラウザ起動後にポップアップにてユーザーの同意を得る必要がある\[11\]。

## WebXRを体験できる作品

  - Pepsi Go Back
  - The Searching Planet
  - Access Mars
  - Inside Music
  - Quake 3
  - Blair Witch
  - Konterball
  - Shopify VR
  - VR部
  - Google検索結果の「3Dで表示」

## WebVR対応

WebXR対応している開発プラットフォームやブラウザでなければ、WebXR APIを利用することはできないため、以下に主要なものを列挙する。

### 開発プラットフォーム

  - [Three.js](https://ja.wikipedia.org/wiki/Three.js "wikilink")
  - [A-Frame](https://ja.wikipedia.org/wiki/A-Frame "wikilink")
  - [PlayCanvas](https://ja.wikipedia.org/wiki/PlayCanvas "wikilink")
  - AR.js
  - Zapworks
  - React 360
  - Hubs

### ブラウザ

  - Firefox Nightly
  - Samsung Internet for Gear VR
  - Experimental Chromium Builds
  - [Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")
  - Oculus Browser

## 脚注

## 参考文献

  -
  -
  -
## 関連項目

  - [WebXR Device API](../Page/WebXR_Device_API.md "wikilink")
  - [WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")
  - [VRML](../Page/VRML.md "wikilink")

## 外部リンク

  - [Mozilla Developer Network](https://developer.mozilla.org/ja/docs/Web/API/WebVR_API)
  - [OpenXR](https://www.khronos.org/openxr)

[Category:HTML5](https://ja.wikipedia.org/wiki/Category:HTML5 "wikilink") [Category:仮想世界](https://ja.wikipedia.org/wiki/Category:仮想世界 "wikilink") [Category:拡張現実](https://ja.wikipedia.org/wiki/Category:拡張現実 "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink")

1.  Legacy Specification. The WebVR API is being replaced by the WebXR Device API, but may still be available in some browsers while that API is finalized. This specification is preserved here for reference purposes. [WebVR Spec](https://immersive-web.github.io/webvr/)
2.
3.
4.  Removal is expected in Chrome 80. [Chrome Platform Status - WebVR](https://chromestatus.com/features/4532810371039232)
5.
6.
7.
8.
9.
10.
11.