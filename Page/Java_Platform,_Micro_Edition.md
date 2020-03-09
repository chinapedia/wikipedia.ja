> この記事は[Java Platform, Micro Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Micro_Edition)から翻訳されています。


**Java Platform, Micro Edition** (**Java ME**) は[携帯電話](../Page/携帯電話.md "wikilink")、[PDA](https://ja.wikipedia.org/wiki/携帯情報端末 "wikilink")、[テレビのようなリソースが制限されたデバイスにおける](../Page/テレビ受像機.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の小型セット。JSR 68 で規定されている。当初は、**Java 2 Platform, Micro Edition** (**J2ME**) という名称だった。

## コンフィギュレーションとプロファイル

様々なデバイスに対応するため、コンフィギュレーションと[プロファイルと呼ばれるものでAPIを定義している](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。コンフィギュレーションには次の2つがある。

  - [Connected Limited Device Configuration](https://ja.wikipedia.org/wiki/Connected_Limited_Device_Configuration "wikilink") (CLDC)
  - [Connected Device Configuration](https://ja.wikipedia.org/wiki/Connected_Device_Configuration "wikilink") (CDC)

## Connected Limited Device Configuration (CLDC)

携帯電話のような非力な[CPU](../Page/CPU.md "wikilink")を対象とする。 [Java VMから新たにKVM](../Page/Java仮想マシン.md "wikilink") (Kilobyte Virtual Machine) を開発し、[Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink") (Java SE) とは一部互換性がないものの最小限の機能で動作するようにしたもの。 次のようなプロファイルがある。

### Mobile Information Device Profile (MIDP)

携帯電話で最も広く普及しているプロファイル。最新の仕様は*JSR 271: Mobile Information Device Profile 3*、3世代目のMobile Information Device Profile (MIDP3)。そのなかで、全体的な機能拡張の他、デバイス間の相互接続性も拡張されている。MIDP3では、MIDP2の後方互換性も保たれている。

MIDP上で動く、高レベルなUIライブラリとして、[Lightweight User Interface Toolkit](https://ja.wikipedia.org/wiki/:en:Lightweight_User_Interface_Toolkit "wikilink") (LWUIT) も提供されている。

### DoJaプロファイル、Starプロファイル

[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")社の携帯電話上で実行するJavaアプリケーションのためのプロファイル。

### Information Module Profile

[Information Module Profile](https://ja.wikipedia.org/wiki/Information_Module_Profile "wikilink") (IMP) は、自動販売機や組み込み向け産業機器、セキュリティシステム、シンプルでディスプレイを持たず、ネットワークへの接続が限定されているような組み込みデバイスのためのプロファイルである。もともとは、[Siemens Mobileと](https://ja.wikipedia.org/wiki/Siemens_AG "wikilink")[Nokia](https://ja.wikipedia.org/wiki/Nokia "wikilink")によって、[JSR](https://ja.wikipedia.org/wiki/JSR "wikilink")-195として導入され、IMP 1.0は、[MIDP](https://ja.wikipedia.org/wiki/MIDP "wikilink") 1.0からユーザインターフェースAPIを除いたサブセットである。

## Connected Device Configuration (CDC)

[Connected Device Configurationは](https://ja.wikipedia.org/wiki/Connected_Device_Configuration "wikilink")、[Java SEのサブセットで](https://ja.wikipedia.org/wiki/Java_SE "wikilink")、その中には、GUI関係を除く、ほとんど全てのライブラリが入っている。CLDCよりもリッチな仕様である。 カーナビや[セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")などの中程度の能力をもったCPUを対象にする。

### Foundation Profile

Foundation Profileは、Java ME Connected Device Configuration (CDC) プロファイルのひとつである。 このプロファイルは、Java Platform, Standard Edition API全てが実行できるJava仮想マシンを必要とするデバイスで使用することを目的としている。 典型的な実装では、追加のプロファイルのサポートに応じて、そのAPIのサブセットを使用する。 この仕様は、[Java Community Processのもので開発されている](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink")。

### Personal Basis Profile

Personal Basis Profileは、Foundation Profileを拡張したもので、軽量なGUI ([AWTのサブセット](https://ja.wikipedia.org/wiki/Abstract_Windowing_Toolkit "wikilink")) が含まれている。

### Personal Profile

Personal Profileは、Personal Basis Profileをさらに拡張したもので、より完全なAWTのサブセットと[Javaアプレット](../Page/Javaアプレット.md "wikilink")サポートが含まれている。

## 携帯電話でのアプリの互換性

日本の携帯電話では[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](https://ja.wikipedia.org/wiki/沖縄セルラー電話 "wikilink")[連合](https://ja.wikipedia.org/wiki/連合 "wikilink")）の[EZアプリ (Java)](https://ja.wikipedia.org/wiki/EZアプリ_\(Java\) "wikilink")、[SoftBank](../Page/SoftBank_\(携帯電話\).md "wikilink")([ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink"))の[S\!アプリ](https://ja.wikipedia.org/wiki/S!アプリ "wikilink")、[WILLCOM](https://ja.wikipedia.org/wiki/WILLCOM "wikilink")のJavaアプリが[MIDP](https://ja.wikipedia.org/wiki/MIDP "wikilink")を採用しており、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")は同社が独自に作成した[DoJaプロファイル](https://ja.wikipedia.org/wiki/DoJaプロファイル "wikilink")やStarプロファイルを使っている。各社の機能が少しずつ違うため、現状では互換性は少ない。

## 開発方法

開発は Java SE 上でMicro Edition用の[開発ツールを組み合わせて行う](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。 [APIも必要なものに限って実装する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

### 開発ツールの例

  - Java ME SDK
  - [Sun ONE Studio 4](https://ja.wikipedia.org/wiki/Sun_ONE_Studio_4 "wikilink") Mobile Edition
  - [SophiaCompress(Java)：携帯Javaアプリ圧縮ツール](http://www.s-cradle.com/products/sophiacompress_java/index.html)

<!-- end list -->

  -
    Java MEアプリケーションのサイズを[実行形式](https://ja.wikipedia.org/wiki/実行ファイル "wikilink") ([JAR形式](https://ja.wikipedia.org/wiki/JAR_\(ファイルフォーマット\) "wikilink")) のまま軽量化するJavaアプリ圧縮ツール。

<!-- end list -->

  - [NetBeans](https://ja.wikipedia.org/wiki/NetBeans "wikilink") IDE開発環境　60MBぐらいの本体を入れた後にnetbeans_mobilityをインストールするだけで開発環境が整う

## JSR (Java Specification Requests)

### 基礎

| JSR 番号                                         | 名称                          | 備考 |
| ---------------------------------------------- | --------------------------- | -- |
| [68](http://www.jcp.org/en/jsr/detail?id=68)   | J2ME Platform Specification |    |
| [30](http://www.jcp.org/en/jsr/detail?id=30)   | CLDC 1.0                    |    |
| [37](http://www.jcp.org/en/jsr/detail?id=37)   | MIDP 1.0                    |    |
| [118](http://www.jcp.org/en/jsr/detail?id=118) | MIDP 2.0                    |    |
| [139](http://www.jcp.org/en/jsr/detail?id=139) | CLDC 1.1                    |    |
| [271](http://www.jcp.org/en/jsr/detail?id=271) | MIDP 3.0                    |    |
| [360](http://www.jcp.org/en/jsr/detail?id=360) | CLDC 8                      |    |
| [361](http://www.jcp.org/en/jsr/detail?id=361) | Java ME Embedded Profile 8  |    |

### 主要な拡張

<table>
<thead>
<tr class="header">
<th><p>JSR 番号</p></th>
<th><p>名称</p></th>
<th><p>備考</p></th>
<th><p>MSA</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=75">75</a></p></td>
<td><p>File Connection and PIM</p></td>
<td><p>ファイルシステム・アドレス帳・カレンダー・TODO</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=82">82</a></p></td>
<td><p>Bluetooth</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=120">120</a></p></td>
<td><p>Wireless Messaging API (WMA)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=135">135</a></p></td>
<td><p>Mobile Media API (MMAPI)</p></td>
<td><p>音声・動画</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=172">172</a></p></td>
<td><p>Web Services</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=177">177</a></p></td>
<td><p>Security and Trust Services</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=179">179</a></p></td>
<td><p>Location API</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=180">180</a></p></td>
<td><p>SIP API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=184">184</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Mobile_3D_Graphics_API" title="wikilink">Mobile 3D Graphics API</a></p></td>
<td><p>高レベル3Dグラフィックス</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=185">185</a></p></td>
<td><p>Java Technology for the Wireless Industry (JTWI)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=205">205</a></p></td>
<td><p>Wireless Messaging 2.0 (WMA)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=211">211</a></p></td>
<td><p>Content Handler API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=226">226</a></p></td>
<td><p>Scalable 2D Vector Graphics API for J2ME</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=228">228</a></p></td>
<td><p>Information Module Profile - Next Generation</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=229">229</a></p></td>
<td><p>Payment API</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=234">234</a></p></td>
<td><p>Advanced Multimedia Supplements (AMMS)</p></td>
<td><p>MMAPI 拡張</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=238">238</a></p></td>
<td><p>Mobile Internationalization API</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=239">239</a></p></td>
<td><p>Java Bindings for the OpenGL ES API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=248">248</a></p></td>
<td><p>Mobile Service Architecture</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=253">253</a></p></td>
<td><p>Mobile Telephony API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=256">256</a></p></td>
<td><p>Mobile Sensor API</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=257">257</a></p></td>
<td><p>Contactless Communication API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=258">258</a></p></td>
<td><p>Mobile User Interface Customization API</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=272">272</a></p></td>
<td><p>Mobile Broadcast Service API for Handheld Terminals</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=280">280</a></p></td>
<td><p>XML API for Java ME</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=281">281</a></p></td>
<td><p>IMS Services API</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=287">287</a></p></td>
<td><p>Scalable 2D Vector Graphics API 2.0 for Java ME</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=293">293</a></p></td>
<td><p>Location API 2.0</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=298">298</a></p></td>
<td><p>Telematics API for Java ME</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=300">300</a></p></td>
<td><p>DRM API for Java ME</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://www.jcp.org/en/jsr/detail?id=325">325</a></p></td>
<td><p>IMS Communication Enablers</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 未完成の規格

| JSR 番号                                         | 名称                               | 備考 |
| ---------------------------------------------- | -------------------------------- | -- |
| [297](http://www.jcp.org/en/jsr/detail?id=297) | Mobile 3D Graphics API (M3G) 2.0 |    |

## 外部リンク

  - [Java ME](http://www.oracle.com/technetwork/java/javame/)
  - [JSR 68: J2ME Platform Specification](http://www.jcp.org/en/jsr/detail?id=68)
  - [Open source Mobile & Embedded Community](http://community.java.net/mobileandembedded/)
  - [Java Technology for Wireless, Mobile, and Embedded Devices](http://developers.sun.com/mobility/)

[Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")