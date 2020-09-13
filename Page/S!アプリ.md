> この記事は[S!アプリ](https://ja.wikipedia.org/wiki/S!アプリ)から翻訳されています。


**S\!アプリ**（エス アプリ）は[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")が提供する、[Yahoo\!ケータイ](../Page/Yahoo!ケータイ.md "wikilink")対応[携帯電話](../Page/携帯電話.md "wikilink")の一部で実行できる[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")およびサービスである。 主に[ゲームなどに利用されている](../Page/携帯型ゲーム.md "wikilink")。ボーダフォン時代の旧称は**Vアプリ**、その前のJ-フォン時代は**Java™アプリ**という呼称が使われていた。

## 概要

  - S\!アプリの実体は[EZアプリ (Java)と同様に](../Page/EZアプリ_\(Java\).md "wikilink")[MIDP](https://ja.wikipedia.org/wiki/MIDP "wikilink")(Mobile Information Device Profile)にしたがって作成されたJavaアプリケーションである。
  - 50kアプリ（[SoftBank 403SH及びV](https://ja.wikipedia.org/wiki/SoftBank_403SH "wikilink")3.V4.J-0xシリーズ対応\*注1）・100kアプリ（V5.V6.V8.J-5xシリーズ対応）・256kアプリ/256ver2アプリ（[SoftBank 502T及びV](https://ja.wikipedia.org/wiki/SoftBank_502T "wikilink")5.V6シリーズ\*注2）・メガアプリ（1M、[SoftBank 3G](../Page/SoftBank_3G.md "wikilink")\*注3）の5種類があり、容量が多いアプリ対応機は容量が少ないアプリにも対応しているが、SoftBank 3Gではアプリの実行環境が変わり、一部の下位アプリは利用できなくなっている。
  - 一部のシャープ製端末はモーションコントロールセンサーに対応している。
  - EZアプリ (Java)と比較すると、ゲーム関連の機能を早くから実装していたことなどの理由から、ゲームアプリが充実している。
      - 注1:V3シリーズはシャープ製のみ対応、V401SAは非対応、J-0xはJ-SH07以降の一部機種を除き対応。
      - 注2:V601NやJ-5x（J-SH53を除く）などは非対応。J-SH53、V601SH及び[V601T](../Page/V601T.md "wikilink")、[V602T](../Page/V602T.md "wikilink")ではアプリによっては非対応もしくは仕様変更となっている（一例:[アークザラッド](../Page/アークザラッド.md "wikilink")）。
      - 注3:708SC、730SC、930SC、V8シリーズ、[SoftBank X シリーズは非対応](../Page/SoftBank_X.md "wikilink")。また、702NK、702NK II、702MO、702sMO、802SCはQVGAに対応していない。
  - セキュリティの関係上、一般の開発者がS\!アプリを公開するためには、アプリゲットS\!などのコンテンツアグリゲータの審査を受けて、コンテンツアグリゲータのサイトでアプリを公開する方式をとる。審査は特別な事情がない限り無料である。
  - セキュリティの関係上、アプリの実行権限はUSIM-IDとリンクされる。その為USIM破損等でUSIMを交換した場合はそれまで利用していたすべてのアプリが利用できなくなる。この場合は「S\!アプリオールリセット」を行う事で現在のUSIM-IDと再リンクされる。

## 対応API

[SoftBank 3G](../Page/SoftBank_3G.md "wikilink") は以下のAPIの一部または全部に対応。

  - [CLDC](https://ja.wikipedia.org/wiki/CLDC "wikilink") 1.1 (JSR 139)
  - [MIDP](https://ja.wikipedia.org/wiki/MIDP "wikilink") 2.0 (JSR 118)
  - Location API (JSR 179)
  - Mobile Media API (JSR 135)
  - Wireless Messaging API (JSR 120)
  - [Mobile 3D Graphics API](../Page/Mobile_3D_Graphics_API.md "wikilink") (JSR 184)
  - 独自拡張
      - MEXA - Mobile Entertainment eXtension API (J-PHONE Specific Class Library, JSCL ベース)
      - VSCL - Vodafone Services Class Libraries （EnhancedGraphics を含む、Vアプリのみ）

例えば、[SoftBank 942SH](https://ja.wikipedia.org/wiki/SoftBank_942SH "wikilink") は Wireless Messaging API, Mobile 3D Graphics API, VSCL に対応しておらず、3次元グラフィックスは MEXA OPGL ([OpenGL ES](../Page/OpenGL_ES.md "wikilink") 1.1）と MEXA Enhanced 3D Graphics（MascotCapsule）が利用可能\[1\]。

## 沿革

  - [2001年](../Page/2001年.md "wikilink")[6月22日](../Page/6月22日.md "wikilink") - [J-SH07](https://ja.wikipedia.org/wiki/J-SH07 "wikilink")より「Javaアプリ」が開始\[2\]
  - 2001年[11月28日](../Page/11月28日.md "wikilink") - 公式コンテンツプロバイダー以外の一般の開発者もアプリを開発できるようになり、[2002年](../Page/2002年.md "wikilink")[3月1日](../Page/3月1日.md "wikilink")発売の[J-SH51](../Page/J-SH51.md "wikilink")から利用可能\[3\]
  - [2003年](../Page/2003年.md "wikilink")[10月1日](../Page/10月1日.md "wikilink") - ボーダフォンになり「Vアプリ」に名称変更\[4\]
  - [2006年](../Page/2006年.md "wikilink")[10月1日](../Page/10月1日.md "wikilink") - ボーダフォンがソフトバンクモバイルに社名変更されたことから、名称が「Vアプリ」から「S\!アプリ」に変更された。
  - [2015年](../Page/2015年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink") - ボーダフォン時代に発売された機種、ならびに2007年夏モデルまでのサムスン電子製機種での提供終了\[5\]。
  - [2020年](../Page/2020年.md "wikilink")[3月24日](../Page/3月24日.md "wikilink") - 全アプリケーションの配信を終了\[6\]。

## 特徴

現在は、MIDP 2.0 と CLDC 1.1 の組み合わせだが、かつては MIDP 1.0 と CLDC 1.0 の組み合わせがあった。 また、JSR に基づく標準 API とは別に、J-PHONE 時代から存在する JSCL とその後継の MEXA、ボーダフォン時代に独自拡張した VSCL もある。 独自拡張した API は オラクル提供の Java ME SDK だけではコンパイルできないため、ビルドライブラリに Softbank 提供のスタブクラスを追加する必要がある。またアプリの .jad ファイルに使用した API 名を記載する必要がある。

記憶領域は[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")とリソースファイルを圧縮した JAR ファイルと内容変更可能なレコードストアに割り当てられる。

## 互換性

EZアプリ(Java)もMIDPを採用しているが、KDDI、ソフトバンクモバイルともに独自拡張したAPIを含んでいるため移植時にはソースの修正が必要となる。ただし、プロファイルが異なるDoJaプロファイルよりは比較的修正点が少ない。

## 脚注

## 関連項目

  - [iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")
  - [オープンアプリプレイヤー](../Page/オープンアプリプレイヤー.md "wikilink")（オープンアプリ）
  - [EZアプリ (Java)](../Page/EZアプリ_\(Java\).md "wikilink")
  - [Yahoo\!ケータイ](../Page/Yahoo!ケータイ.md "wikilink")
  - [日本における携帯電話](https://ja.wikipedia.org/wiki/日本における携帯電話 "wikilink")
  - [スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")

## 外部リンク

  - [S\!アプリ](http://www.softbank.jp/mobile/service/3g/contents/game/)
  - [S\!アプリ開発ガイド](http://creation.mb.softbank.jp/mc/tech/tech_sapp/sapp_index.html)

### コンテンツアグリゲータ

  - [アプリ★ゲット](http://appget.com/vf/pc/)
  - [ビジネスプロバイダ](http://support.vappli.com/)
  - [ゲームチャンネル](http://appli.channel.or.jp/pc/v/)

[Category:携帯電話_(ソフトバンク)](https://ja.wikipedia.org/wiki/Category:携帯電話_\(ソフトバンク\) "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:携帯電話アプリ](https://ja.wikipedia.org/wiki/Category:携帯電話アプリ "wikilink")

1.  [端末情報 942SH](http://creation.mb.softbank.jp/mc/terminal/doc/B-504-001-HandsetInformation_942SH_1.0.0.pdf)
2.  [J-フォン，Javaサービス6月22日開始──「J-SH07」も登場](http://www.itmedia.co.jp/mobile/news/0106/19/jphone.html)
3.  [J-フォン，Javaアプリを一般に開放](http://www.itmedia.co.jp/mobile/news/0111/28/jphone.html)
4.  [ボーダフォン、すべてのVアプリの仕様公開](http://www.itmedia.co.jp/mobile/0310/01/n_vappli.html)
5.  [「S\!アプリ」一部機種での提供終了のご案内](http://www.softbank.jp/mobile/info/personal/news/service/20141031a/)
6.  [「S\!アプリ」配信終了のご案内](https://www.softbank.jp/mobile/info/personal/news/service/20190918a/)