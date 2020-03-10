> この記事は[CompJapan](https://ja.wikipedia.org/wiki/CompJapan)から翻訳されています。


**CompJapan**（コンプジャパン）とは、16歳（[1999年](../Page/1999年.md "wikilink")当時）の少年2人で構成された[オンラインソフトウェア](../Page/オンラインソフトウェア.md "wikilink")の開発を目的とする営利団体（現在は活動停止）である。

「**ASテクノロジ**」という不可解な独自の技術を用いてメモリ内のデータを最適化するという「**新メモリ最適化ツール**」を、[シェアウェア](../Page/シェアウェア.md "wikilink")の形態で[Vector等を介し公開したことで広く知られるようになった](https://ja.wikipedia.org/wiki/ベクター_\(企業\) "wikilink")。同ソフトは、「大変効果があった」という意見もあるにはあったが、技術的にメモリを最適化する機能がないことが指摘され、公開は停止されるに至った。

この騒動の被害総額は10万円を超えるとされ、現在も放置状態で解決していない。この事件はオンラインソフト界に衝撃を与えるほどのことはなかったが、なんちゃってソフトが公開される度に「**CompJapan的**ソフト」というように引き合いに出され、語り継がれるようになった。

## 新メモリ最適化ツール

### 概要

  - 対応OS:Windows95(OSR1.0～2.5)、Windows98（要VB5ランタイム）
  - 価格:900円
  - 試用期間:2週間

### 機能

CompJapanによれば、「新メモリ最適化ツール」は、Kernel32.DLL等のメモリ管理可能なDLLを呼び出し[Win32 APIを主に利用して管理を行うことで以下のような機能を備えることに成功したとのことであった](https://ja.wikipedia.org/wiki/Win32_API "wikilink")。

1.  [メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")の最適化
2.  エラーの減少
3.  [スワップ](https://ja.wikipedia.org/wiki/スワップ "wikilink")の減少
4.  圧縮を行なわない方法による、より多くのデータの物理メモリへの収納
5.  [ウィルス](https://ja.wikipedia.org/wiki/ウィルス "wikilink")スキャン
6.  [CPU](../Page/CPU.md "wikilink")への負担の軽減
7.  CPUの発熱軽減
8.  [Windowsのパフォーマンスのわずかながらの向上](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")

上記の機能は、「アセンブル的処理」や「ASテクノロジ」、「UNIX系特殊メモリフォーマット」により実現しているとのことであった。

### 問題視されたソースの内容

開発元のCompJapanの主張とは異なり、一般には上記のような機能はないと考えられている。そのように考えられている根拠に、メモリ最適化のためのエンジンが「ある変数に一定の数を足した後に同じ数を引く作業を36万回繰り返すだけで、メモリに一切干渉していない」点が指摘されている。

具体的には下記の通りである。

`   For Bbbb = 1 To 3000`
`   Print #1, Jjjj 'CPU処理のためのPrint文`
`   For Kkkk = 1 To 120`
`   Kkkk = Kkkk + 65468543`
`   Kkkk = Kkkk - 65468543`
`   Next Kkkk`
`   Next Bbbb`

開発元のCompJapanの弁解によれば、メール等でメモリ最適化の効果があった旨の報告を受けたことで、「（メモリ最適化の効果に）何が関係しているのかは分からないが、本当に最適化させる効果があるのではないかと思うようになった」とのことである。もっとも、CompJapanは効果の実証にあたりソフトウェアをつかった[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")テストを行ってはいなかった。

## 経緯

  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink") - CompJapan、[Visual Basic](../Page/Visual_Basic.md "wikilink")5.0を購入。
  - 1998年[4月](https://ja.wikipedia.org/wiki/4月 "wikilink") - CompJapan、全30種類のサービスを有料で開始。
  - [1999年](../Page/1999年.md "wikilink")[1月20日](../Page/1月20日.md "wikilink") - CompJapan、新メモリ最適化ツール1.00aをベクターにて公開開始。
  - 1999年[2月](https://ja.wikipedia.org/wiki/2月 "wikilink") - 早速、新メモリ最適化ツールの機能が虚偽ではないかという指摘がなされる。
  - 1999年[2月20日](../Page/2月20日.md "wikilink") - 「RADICA EXPRESS」に[「詐欺？機能しないシェアウエア」](http://www.ninjin.net/radica/HTML/990220.html)というタイトルで取り上げられる。CompJapan、新メモリ最適化ツールに効果がないことを認め謝罪を行なう。同時にVectorでの公開の停止、返金の発表を行う。
  - 1999年[2月27日](../Page/2月27日.md "wikilink") - 「RADICA EXPRESS」に[「 Comp Japanシェアウェア騒動、その後」](http://www.ninjin.net/radica/HTML/990227.html)というタイトルで取り上げられる。
  - 1999年[4月](https://ja.wikipedia.org/wiki/4月 "wikilink") - ASCII5月号に取り上げられる。

## 関連項目

  - [Vocal Cancel](https://ja.wikipedia.org/wiki/Vocal_Cancel "wikilink")
  - [WinGroove](../Page/WinGroove.md "wikilink")

## 外部リンク

  - [CompJapan事件の経緯](http://page.freett.com/hachikou/index.html)
  - [CompJapanのサービス全30種類！](http://page.freett.com/hachikou/service.html)

[Category:ソフトウェア](https://ja.wikipedia.org/wiki/Category:ソフトウェア "wikilink") [Category:日本の詐欺事件](https://ja.wikipedia.org/wiki/Category:日本の詐欺事件 "wikilink")