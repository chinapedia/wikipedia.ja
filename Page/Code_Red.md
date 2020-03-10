> この記事は[Code Red](https://ja.wikipedia.org/wiki/Code_Red)から翻訳されています。


**Code Red**（コードレッド）は、[2001年](../Page/2001年.md "wikilink")[7月13日](../Page/7月13日.md "wikilink")に[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")で発見された[ワームである](https://ja.wikipedia.org/wiki/ワーム_\(コンピュータ\) "wikilink")。[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [IIS](../Page/Internet_Information_Services.md "wikilink") [Webサーバ](../Page/Webサーバ.md "wikilink")が動作するコンピュータを攻撃した。このワームについて最も深く調査したのは、eEye Digital Security のプログラマ達であった。彼らはワームの名称も決めたが、その由来はソフトドリンク「[マウンテンデュー](https://ja.wikipedia.org/wiki/マウンテンデュー "wikilink")」のチェリー味の商品名（CODE RED）と、このワームに攻撃されたWebサイトで見られた "Hacked By Chinese\!" という文字列からの連想である（[赤狩り](https://ja.wikipedia.org/wiki/赤狩り "wikilink")参照）。このワームが出現したのは7月13日だが、被害が拡大したのは**2001年7月19日**のことだった。この日感染したホスト数は359,000に達した\[1\]。当日は、世界中のネットワークのトラフィックの急増により、どのサイトへもつながりにくい状態が発生し、唯一インターネットが麻痺した日とされる。

## 概説

### 利用された脆弱性

このワームは IIS に付属して配布されたインデックスサーバの脆弱性を利用した。この脆弱性については [MS01-033](http://www.microsoft.com/technet/security/bulletin/MS01-033.asp) で説明されている。それによると、ワーム出現の約1ヵ月前にパッチが公開されている。

このワームは自身の拡散のために、いわゆる[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")と呼ばれる脆弱性を利用した。'N' を繰り返した長い文字列でバッファをオーバーフローさせ、任意のコードを実行してマシンに感染する。

### ワームのペイロード

このワームのペイロードには、以下が含まれる。

  - 感染したWebサイトは次のように表示させられる（最後の部分はネット上での敗北を表す決まり文句となった。外部リンク参照）:
    > HELLO\! Welcome to http://www.worm.com\! Hacked By Chinese\!
  - インターネット上のIISサーバを探し、さらに感染させようとする。
  - 感染後20日から27日待って、いくつかの固定の[IPアドレス](../Page/IPアドレス.md "wikilink")に[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")を仕掛けるようになっていた。攻撃目標には[ホワイトハウス](../Page/ホワイトハウス.md "wikilink")のWebサーバも含まれていた\[2\]。

感染可能なマシンを探す際に、このワームは IIS の脆弱性のあるバージョンが動作しているかをチェックしていない。さらに言えば、IIS が動作しているかどうかすらチェックしていなかった。そのため、当時の [Apache](../Page/Apache_HTTP_Server.md "wikilink") のアクセスログを調べると、以下のようなエントリが頻繁に見つかる\[3\]

  -
    GET /default.ida?NNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
    NNNNNNNNNNNNNNNNNNN
    %u9090%u6858%ucbd3%u7801%u9090%u6858%ucbd3%u7801
    %u9090%u6858%ucbd3%u7801%u9090%u9090%u8190%u00c3
    %u0003%u8b00%u531b%u53ff%u0078%u0000%u00=a HTTP/1.0

## 類似のワーム

[2001年](../Page/2001年.md "wikilink")[8月4日](../Page/8月4日.md "wikilink")、Code Red II が出現した。Code Red II は、Code Red ワームから派生したものでは**ない**。感染方法が同じであるものの、[ペイロードは全く異なる](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。感染したマシンと同じサブネットかまたは異なるサブネットのターゲットを、ある固定の確率分布に従った[擬似乱数](../Page/擬似乱数.md "wikilink")的な手法で選択する。通常、同じサブネット内のターゲットを選ぶことが多い。さらに、Code Red で 'N' を繰り返していた部分（バッファオーバーランを発生させる文字列）が 'X' の繰り返しになっている。

eEye はワームの発信地が[フィリピン](https://ja.wikipedia.org/wiki/フィリピン "wikilink")の[マカティ](https://ja.wikipedia.org/wiki/マカティ "wikilink")であると考えている（[VBS/Loveletter](https://ja.wikipedia.org/wiki/VBS/Loveletter "wikilink") ワームと同じ発信地である）。

## 脚注

### 注釈

<references group="注釈"/>

### 出典

## 外部リンク

  - [CERT Advisory CA-2001-19](http://www.cert.org/advisories/CA-2001-19.html)
  - [eEye Code Red advisory](http://research.eeye.com/html/advisories/published/AL20010717.html)
  - [Code Red II analysis](http://www.unixwiz.net/techtips/CodeRedII.html)
  - [Urban Dictionary](http://www.urbandictionary.com/define.php?term=Hacked+by+Chinese) における "Hacked by Chinese" というフレーズについての説明

[Category:マルウェア](https://ja.wikipedia.org/wiki/Category:マルウェア "wikilink")

1.
2.
3.  このワームのペイロードは 'N' の羅列の後の文字列である。脆弱なホストはこの文字列を命令列として実行してしまう。