> この記事は[ASIO](https://ja.wikipedia.org/wiki/ASIO)から翻訳されています。


**ASIO**（Audio Stream Input Output：エイシオ、アシオ、アジオ）は、オーディオデバイスの[ドライバインタフェースの一つである](../Page/デバイスドライバ.md "wikilink")。

## 概要

ASIOは、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[スタインバーグ](https://ja.wikipedia.org/wiki/スタインバーグ "wikilink")によりオーディオを入出力するためのアプリケーション用[APIとして提供された規格であり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、販売されている高級[オーディオカードの多くがこの規格に準拠し](../Page/サウンドカード.md "wikilink")、[Windows用および](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用のドライバも存在し、ほぼ業界標準として採用されている。[Mac OS Xの](https://ja.wikipedia.org/wiki/macOS "wikilink")[Core Audioはこれと同等の技術とされる](../Page/Core_Audio_\(アップル\).md "wikilink")\[1\]。

WindowsやMac OS上にもサウンドドライバは存在するが、ASIOはそれよりも低遅延、高同期性、高い[スループット](../Page/スループット.md "wikilink")を実現している。開発された理由としては従来の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) に搭載されているサウンドドライバでは2以上のマルチチャンネル入力が考慮されていなかったためである。ASIOではマシンの処理速度が許す限りはあらゆるチャンネル数、[標本化周波数](../Page/サンプリング周波数.md "wikilink")、[量子化ビット数のデータを扱うことができる](https://ja.wikipedia.org/wiki/ビット深度_\(音響機器\) "wikilink")。

### 低レイテンシ

Windows旧来の[MMEではその](https://ja.wikipedia.org/wiki/Windows_Multimedia_Extensions "wikilink")[レイテンシ](../Page/レイテンシ.md "wikilink")（データ送信から音声が出力されるまでの遅延時間）は200から500ミリ秒、[DirectSound](../Page/DirectSound.md "wikilink")でも50から100ミリ秒、Mac OSのSound Managerで20から50ミリ秒とされているが、ASIOの場合は数ミリ秒から10ミリ秒以下で、環境によっては1ミリ秒以下となる場合もある。そのため、PCに接続したキーボードで[ソフトウェア・シンセサイザー](../Page/ソフトウェア・シンセサイザー.md "wikilink")を演奏したり、エレキギターにリアルタイムでエフェクトをかけたりといったことが可能になる。また、OSのソフトウェアミキサーを通らずに元の波形がそのままオーディオ出力されるため、良好な音質が得られる場合がある。

### マルチチャンネル

ASIOでは、複数同時に出力するなど、複数のポートを同時に扱うことができる。エフェクタを経由させる出力と、ノーマル出力とを同時に実施するなどの効用がある。

## ASIO 2.0

ASIO 1.0の後継規格として、ASIO 2.0が提供されている。最大の相違点は、入力信号をそのまま出力するダイレクトモニタリング機能をサポートしている点である。ダイレクトモニタリング機能は、入力信号をコンピュータを介さずモニタすることから、レイテンシが生じないという効用がある。

## ASIO 2.1

[2005年](../Page/2005年.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")の働きかけにより[DSD対応が盛り込まれた](../Page/Direct_Stream_Digital.md "wikilink")。他の変更点はない。

## 開発

スタインバーグによりライセンスフリーのSDK（[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")）が無償で配布されている。同社は直接のサポートはおこなわないがメーリングリストにおいて開発者同士の意見交換がおこなわれている。

## 関連項目

  - [Windows Multimedia Extensions](https://ja.wikipedia.org/wiki/Windows_Multimedia_Extensions "wikilink"), MME
  - [DirectSound](../Page/DirectSound.md "wikilink")
  - [Sound Manager](https://ja.wikipedia.org/wiki/Sound_Manager "wikilink")
  - [Core Audio (アップル)](../Page/Core_Audio_\(アップル\).md "wikilink")
  - [Core Audio (Windows)](https://ja.wikipedia.org/wiki/Core_Audio_\(Windows\) "wikilink")
  - [レイテンシ](../Page/レイテンシ.md "wikilink")
  - [Virtual Studio Technology](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink"), VST
  - [WASAPI](https://ja.wikipedia.org/wiki/WASAPI "wikilink")

## 外部リンク

  - [ASIO SDK](http://www.steinberg.de/329+M52087573ab0.html) - スタインバーグによる無償SDK配布およびメーリングリストの参加窓口
  - [ASIO4ALL](http://www.asio4all.com/) - [Windows NTの機能であるカーネルストリーミングを使用したフリーのASIOエミュレーションドライバ](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")\[2\]。

## 脚注

<references/>

[Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink")

1.  <http://allabout.co.jp/entertainment/dtm/closeup/CU20030706/>
2.  ASIOに対応していないオーディオハードウェアとドライバ環境向けに擬似的にASIOインターフェイスを提供するエミュレーションインターフェイスもしくはカーネルストリーミングラッパーであり、[TASCAM US-144MKIIなどのネイティブにASIO対応している環境ではインストールする必要はない](../Page/ティアック.md "wikilink")