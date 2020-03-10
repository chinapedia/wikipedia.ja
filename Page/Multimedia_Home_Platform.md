> この記事は[Multimedia Home Platform](https://ja.wikipedia.org/wiki/Multimedia_Home_Platform)から翻訳されています。


**Multimedia Home Platform**（DVB-MHP）とは、DVB（[デジタルビデオブロードキャスティング](https://ja.wikipedia.org/wiki/デジタルビデオブロードキャスティング "wikilink")）プロジェクトにおいて双方向デジタルテレビのために標準化されたオープンな[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")体系である。MHP はインタラクティブな[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのアプリケーションをテレビ受像機上に実装して実行可能にする。[双方向番組](https://ja.wikipedia.org/wiki/双方向番組 "wikilink")アプリケーションは、音声と動画と並行して放送チャンネル上で提供される。アプリケーションには、情報サービス、ゲーム、双方向の投票、電子メール、ショッピングなどがある。いずれにしても、双方向型のアプリケーションには放送チャンネルとは別に応答を返すための経路が必要である。

## 採用状況

2005年ごろの DVB-MHP の採用状況としては、[イタリア](../Page/イタリア.md "wikilink")（DVB-T）、[韓国](https://ja.wikipedia.org/wiki/韓国 "wikilink")（ASTC）がある。また、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")、[フィンランド](https://ja.wikipedia.org/wiki/フィンランド "wikilink")、[スペイン](https://ja.wikipedia.org/wiki/スペイン "wikilink")、[オーストリア](../Page/オーストリア.md "wikilink")、[オーストラリア](https://ja.wikipedia.org/wiki/オーストラリア "wikilink")で実験的に採用されている。[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")では MHP に基づいた [OCAP](https://ja.wikipedia.org/wiki/OpenCable_Application_Platform "wikilink") がケーブルテレビ業界によって策定されている。[ベルギー](https://ja.wikipedia.org/wiki/ベルギー "wikilink")最大のケーブルテレビ会社 Telenet は DigiBox と名づけた DVB-MHP システムを完成させた。ノルウェーでも DVB-MHP の採用が予定されている。

日本では [Broadcast Markup Language](https://ja.wikipedia.org/wiki/Broadcast_Markup_Language "wikilink") (BML) が独自に策定・採用されていたが、2003年に[電波産業会](https://ja.wikipedia.org/wiki/電波産業会 "wikilink") (ARIB) がMHPをベースとしたデータ放送規格「デジタル放送におけるアプリケーション実行環境標準規格」（ARIB-STD-B23、通称ARIB-AE）を規格策定した[1](http://www.arib.or.jp/tyosakenkyu/kikaku_hoso/hoso_std-b023.html)。ARIB-AE については運用規定が定まっていないため、運用はまだ始まっていない。

## 技術

[frame](https://ja.wikipedia.org/wiki/ファイル:MHP-software_stack_english.png "wikilink")\]\] MHP はデジタル双方向テレビにおける拡張可能なアプリケーション実行環境を定義しており、それを支えるベンダー固有のハードウェアやソフトウェアとは独立している。この実行環境は[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")とデジタル双方向テレビが一般に持っているリソースや機能への汎用アクセスAPI定義に基づいている。インタラクティブなMHPアプリケーションはこれらAPI上で動作する。ユーザーは、テレビ本体のソフトウェアであるナビゲーターを通してMHPアプリケーションにアクセスできる。

MHP は [Globally Executable MHP](https://ja.wikipedia.org/wiki/Globally_Executable_MHP "wikilink") (GEM) 標準の一部である。

## DVB-HTML

MHPアプリケーションには2種類ある。ひとつは、DVB-HTML アプリケーションである。これはあまり採用されていない部分である。その理由は、DVB-HTML の仕様が MHP 1.1 でのみ示されている点と、仕様が複雑すぎて実装が難しいためである。DVB-HTMLアプリケーションは、一種の[HTMLページとして放送時に配信される](../Page/HyperText_Markup_Language.md "wikilink")。その仕様は[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") 1.1 をモジュール化したものに基づき、[CSS](../Page/Cascading_Style_Sheets.md "wikilink") 2.0、[DOM](../Page/Document_Object_Model.md "wikilink") 2.0、[ECMAScript](../Page/ECMAScript.md "wikilink") が含まれている。

なお、日本では [BML](https://ja.wikipedia.org/wiki/Broadcast_Markup_Language "wikilink") がこれに相当し、今後も BML が使用される見込みである。

## DVB-J

DVB-J（DVB-Java）の方がずっと一般的である。この場合、アプリケーションは MHP [APIを使って](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれ、[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")群が放送時に配信される。DVB-Java アプリケーションを "Xlet" とも呼ぶ。これは[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")と似た概念であり、サンが JavaTV 仕様の中で使い始めた用語である。アプレットと同様、Xlet インタフェースでは外部ソース（MHP準拠のテレビの場合、テレビ内のアプリケーションマネージャ）がアプリケーションの起動・停止を制御できる。

## 応答経路

MHP [セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")は、投票やショッピングといったアプリケーションが外界と通信するための応答経路を用意している。媒体としては電話回線や[ADSL](../Page/ADSL.md "wikilink")程度のインターネット接続が一般的であり、[FTTH](../Page/FTTH.md "wikilink")を前提とする[IP放送](https://ja.wikipedia.org/wiki/IP放送 "wikilink")とは異なる。

## 関連項目

  - [電波産業会](https://ja.wikipedia.org/wiki/電波産業会 "wikilink") (ARIB)
  - [BD-J](https://ja.wikipedia.org/wiki/BD-J "wikilink")
  - [双方向番組](https://ja.wikipedia.org/wiki/双方向番組 "wikilink")
  - [IP放送](https://ja.wikipedia.org/wiki/IP放送 "wikilink")
  - [MHEG-5](https://ja.wikipedia.org/wiki/MHEG-5 "wikilink")
  - [セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")
  - [OSGi](../Page/OSGi.md "wikilink")
  - [データ放送](../Page/データ放送.md "wikilink")
  - [DVB-H](https://ja.wikipedia.org/wiki/DVB-H "wikilink")

## 参考文献

  - Ulrich Reimers: DVB, The Family of International Standards for Digital Video Broadcasting, Second Edition, 2005, ISBN 3-540-43545-X (chapter 14, MHP)

## 外部リンク

  - [Official MHP and GEM website](http://www.mhp.org/)
  - [MHP tutorials](http://www.mhp-interactive.org/)
  - [MHP Knowledge Database](http://www.mhp-knowledgebase.org)

<!-- end list -->

  - [OpenMHP](http://www.openmhp.org/) - MHP-オープンソースプロジェクト
  - [Sun Microsystems' Java TV](http://java.sun.com/products/javatv)
  - [xleTView](http://xletview.sourceforge.net/)
  - [Interactive-TV-Web](http://www.interactivetvweb.org)

[Category:テレビ](https://ja.wikipedia.org/wiki/Category:テレビ "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java仮想マシン](https://ja.wikipedia.org/wiki/Category:Java仮想マシン "wikilink")