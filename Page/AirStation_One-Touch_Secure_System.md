> この記事は[AirStation One-Touch Secure System](https://ja.wikipedia.org/wiki/AirStation_One-Touch_Secure_System)から翻訳されています。


**AirStation One-Touch Secure System**（エアーステーション ワンタッチ セキュア システム）は、[バッファローが発売している無線LAN機器](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink")・**[AirStation](../Page/AirStation.md "wikilink")**に導入されている[無線LAN](../Page/無線LAN.md "wikilink")設定システムである。一般的に**AOSS**（エーオーエスエス）と呼ばれる。後発である[NECアクセステクニカ](https://ja.wikipedia.org/wiki/NECアクセステクニカ "wikilink")の[らくらく無線スタート](../Page/らくらく無線スタート.md "wikilink")と共に二大無線設定システムとして知られ、らくらく無線スタート共々[Wi-Fiアライアンスに](../Page/Wi-Fi_Alliance.md "wikilink")[WPSを策定させる遠因となった](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Setup "wikilink")。

## 概要

2003年に発表された\[1\]。[無線LAN](../Page/無線LAN.md "wikilink")の[アクセスポイント](../Page/アクセスポイント_\(無線LAN\).md "wikilink")（親機）と端末（子機）の両方で同時に**AOSSボタン**を押すだけで簡単に[無線LANのセキュリティなどの設定ができる](https://ja.wikipedia.org/wiki/無線LAN#無線LANとセキュリティ "wikilink")｡

[ソニー](../Page/ソニー.md "wikilink")の[携帯ゲーム機](https://ja.wikipedia.org/wiki/携帯ゲーム機 "wikilink")[PlayStation Portable](../Page/PlayStation_Portable.md "wikilink")（PSP）のインフラストラクチャモードを利用するときのアクセス先設定\[2\]や[任天堂](../Page/任天堂.md "wikilink")・[ニンテンドーDS](../Page/ニンテンドーDS.md "wikilink")の「[ニンテンドーWi-Fiコネクション](../Page/ニンテンドーWi-Fiコネクション.md "wikilink")」のアクセス先設定などにAOSSモジュールが組み込まれている。[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（20GBモデルは無線機能なし）、[PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")、[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")・[Wii U](https://ja.wikipedia.org/wiki/Wii_U "wikilink")・[ニンテンドー3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")・[PlayStation Vitaにも採用されている](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")｡

ちなみに[バッファローが配布する無線LAN接続ソフト](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink")「ClientManager」のバージョン3からバッファロー製でない無線LAN端末でもAOSSで設定が出来るようになった。なお一つの[SSIDには一つの無線暗号しか設定できないため](../Page/サービスセット識別子.md "wikilink")、接続機器全てのうち、**最も低い強度の暗号を選択する仕組みだった**（たとえば[CCMP](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink")([AES](../Page/Advanced_Encryption_Standard.md "wikilink"))方式の設定の中に[WEPしか対応していないものを追加すると](../Page/Wired_Equivalent_Privacy.md "wikilink")、全ての機器がWEPによるアクセスに変わる）が最近はマルチSSIDにより接続する機器それぞれに対して異なる暗号を設定できる機種が発売されている。

WPA2には対応しておらず、WPA-PSK-[CCMP](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink") ([AES](../Page/Advanced_Encryption_Standard.md "wikilink"))、WPA-PSK-[TKIP](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink")、[WEPに標準で対応している](../Page/Wired_Equivalent_Privacy.md "wikilink")。

### 方法

1.  ClientManagerのAOSSボタンを押す（PSP、ニンテンドーDSも同様）。
2.  アクセスポイントをAOSSモードにする。これには2つの方法がある。
    1.  機器にあるAOSSボタンを押す方法。
    2.  アクセスポイントにアクセスして、そのメニューにあるAOSSボタンを押す方法。

なお、AOSS/WPS両対応の場合はWPSが優先される。

### 課題

パソコンに接続した子機からAOSSを利用するためのアプリケーションソフトウェア・**ClientManager**（クライアントマネージャ）は、[Windows 98SE以降のデスクトップおよびノートパソコンのみの対応となっている](../Page/Microsoft_Windows_98.md "wikilink")。

非対応のPCでAOSSのネットワークに参加するためには、以下に挙げるような方法が必要である。

1.  AOSS対応のイーサネットコンバーターで、有線LANとして認識させる。
2.  アクセスポイントのポートからAOSSの暗号を確認し、それを手入力する。

## AOSS2

2012年6月6日に発表され\[3\]、それ以降に発売されるルーターの新製品に搭載される。パソコンがなくても[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")などの[Android](../Page/Android.md "wikilink")・[iOS端末だけで接続設定が行える](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。特にWPSすら対応していないiOSデバイスでは設定が飛躍的に簡単になる\[4\]。Windowsと[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にも対応している。[Google Playに標準で対応していないAndroid端末は対象外](https://ja.wikipedia.org/wiki/Google_Play "wikilink")。

### 方法 (2)

1.  アクセスポイントをAOSSモードにする。
2.  クライアントから「\!AOSS」で始まるSSIDに接続する。
3.  ブラウザでAOSS2キーを入力（画面上のボタンでしか受け付けない）。
4.  iOSの場合はプロファイルがインストールされ、iOS以外の場合は従来のAOSSで設定され完了となる。

## 競合技術

  - [らくらく無線スタート](../Page/らくらく無線スタート.md "wikilink") - [NECアクセステクニカ](https://ja.wikipedia.org/wiki/NECアクセステクニカ "wikilink")
    AOSSはNECのらくらく無線スタートと共に二大無線設定システムとしてPSPやニンテンドーDS、[Wi-Fi WINに対応した一部の](https://ja.wikipedia.org/wiki/Wi-Fi_WIN "wikilink")[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")の[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")（例・[biblio](https://ja.wikipedia.org/wiki/biblio "wikilink")（TSY01）、[AQUOS SHOT SH006等](https://ja.wikipedia.org/wiki/SH006 "wikilink")）などパソコン以外のさまざまなインターネット対応機器に組み込まれている。

<!-- end list -->

  - [Wi-Fi Protected Setup](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Setup "wikilink")
    [Wi-Fiアライアンスによって](../Page/Wi-Fi_Alliance.md "wikilink")2007年に策定された類似の技術。

## 脚注

<references/>

## 関連項目

  - [AirStation](../Page/AirStation.md "wikilink")
  - [Wi-Fi Protected Access](../Page/Wi-Fi_Protected_Access.md "wikilink")

## 外部リンク

  - [AirStation One-Touch Secure System](https://www.buffalo.jp/topics/utilize/detail/aoss.html)
  - [AOSS2](https://www.buffalo.jp/contents/topics/utilize/aoss2/)
  - [PSPをインターネットにつないでもっと楽しもう\!](http://buffalo.jp/products/catalog/network/psp/index.html)
  - [ニンテンドーDSが無線LANでもっと楽しくなる\!](http://buffalo.jp/products/catalog/network/nds/index.html)
  - [クライアントマネージャ](https://www.buffalo.jp/news/detail/20170531-02.html)

[Category:通信機器](https://ja.wikipedia.org/wiki/Category:通信機器 "wikilink") [Category:Wi-Fi](https://ja.wikipedia.org/wiki/Category:Wi-Fi "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.  ファームウェアVer.2.00以降
3.
4.