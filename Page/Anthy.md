> この記事は[Anthy](https://ja.wikipedia.org/wiki/Anthy)から翻訳されています。


**Anthy**（アンシー）とは、[LGPLでライセンスされた](../Page/GNU_Lesser_General_Public_License.md "wikilink")[フリーな](../Page/フリーソフトウェア.md "wikilink")[日本語入力システム](../Page/日本語入力システム.md "wikilink")である。

Anthy自体は[かな漢字変換](https://ja.wikipedia.org/wiki/かな漢字変換 "wikilink")ソフトウェアであるため、文字入力には[uim](https://ja.wikipedia.org/wiki/uim "wikilink")、[SCIM](../Page/SCIM.md "wikilink")、[iBus](https://ja.wikipedia.org/wiki/iBus "wikilink")、[Tamago](https://ja.wikipedia.org/wiki/Tamago "wikilink")、付属ユーティリティのanthy.elなどの[インプットメソッド](../Page/インプットメソッド.md "wikilink")を用いる。また[Canna](../Page/Canna.md "wikilink")や[Wnn](../Page/Wnn.md "wikilink")と違い[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")を採用せず、他のソフトウェアとの[プロセス間通信](../Page/プロセス間通信.md "wikilink")は[パイプによって行われている](../Page/パイプ_\(コンピュータ\).md "wikilink")。

変換アルゴリズムにはA Discriminative Language Model with Pseudo-Negative SamplesとMemory Based Reasoningと[ビタビアルゴリズム](../Page/ビタビアルゴリズム.md "wikilink")を採用。漢字変換には、省メモリと高速化を図った独自のバイナリ形式辞書を使用するが、テキスト形式のCanna用辞書を扱うこともできる。漢字変換辞書はcannadicを流用しており、cannadicはAnthyのアーカイブに同梱されている。

[IA-32](../Page/IA-32.md "wikilink") 200MHzの[CPU](../Page/CPU.md "wikilink")を搭載したマシンで、一文0.1秒前後、[ヒープ](../Page/ヒープ.md "wikilink")消費がピークで200KiB以内、起動時の初期化は一瞬で完了するという条件で動作することを想定\[1\]しており、[ソースコード](../Page/ソースコード.md "wikilink")はほぼ[POSIX](../Page/POSIX.md "wikilink")に準拠。そのため、ほとんどの[UNIX](../Page/UNIX.md "wikilink")ライクな[OSでの使用が可能である](../Page/オペレーティングシステム.md "wikilink")。[ZETA](../Page/ZETA.md "wikilink")や[Microsoft Windowsにも移植されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

Anthyのバージョニング規則は、バージョン番号が*9026*の場合、Anthyの開発が始まってから90ヶ月と26日目であることを示している。*9100*のように、下2桁が*00*のバージョン番号がつけられたものは、それが安定版であることを示しており、[ソフトウェア保守](../Page/ソフトウェア保守.md "wikilink")の際には*9100a*のように末尾に[アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink")がつけられる。

名前の由来はアニメーション作品『[少女革命ウテナ](../Page/少女革命ウテナ.md "wikilink")』の二人の主人公の一人・**姫宮アンシー**から（もう一人は天上ウテナ）。

## 歴史

[2000年](../Page/2000年.md "wikilink")5月19日に[京都大学](../Page/京都大学.md "wikilink")を中心に活動している[コンピュータ](../Page/コンピュータ.md "wikilink")[サークル](../Page/サークル.md "wikilink")である[京大マイコンクラブ](https://ja.wikipedia.org/wiki/京大マイコンクラブ "wikilink")内の[Project Hekeにて開発が始まる](https://ja.wikipedia.org/wiki/Project_Heke "wikilink")。

その後、[IPAの平成](../Page/情報処理推進機構.md "wikilink")13年度[未踏ソフトウェア創造事業](https://ja.wikipedia.org/wiki/未踏ソフトウェア創造事業 "wikilink")として採択される。採択期間中の[2001年](../Page/2001年.md "wikilink")7月に開発版がリリースされ、2001年11月にα版がリリースされた。

採択期間終了後も活発に開発が継続されていたが、[2007年](../Page/2007年.md "wikilink")10月29日現在では、主要開発者による開発は終了されている\[2\]。

## 脚注

<references/>

## 外部リンク

  - [公式サイト](http://anthy.osdn.jp/)
  - [平成13年度未踏ソフトウェア創造事業 採択案件評価書](http://www.ipa.go.jp/NBP/13nendo/13mito/mdata/14-18.htm)
  - [Project Heke](https://www.kmc.gr.jp/projects/heke/)
  - [WinAnthy](https://www.kmc.gr.jp/projects/winanthy/) windowsへの移植版。2013年6月現在、64ビットアプリケーションでは動作しない。

[Category:日本語入力ソフト](https://ja.wikipedia.org/wiki/Category:日本語入力ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.  <http://srad.jp/~tabatee/journal/407854/>
2.  を参照