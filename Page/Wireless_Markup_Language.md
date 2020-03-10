> この記事は[Wireless Markup Language](https://ja.wikipedia.org/wiki/Wireless_Markup_Language)から翻訳されています。


**Wireless Markup Language**（**WML**）とは、携帯電話インターネット用のコンテンツ記述言語。そのルーツは、1990年代のUnwired Planetの[HDML](https://ja.wikipedia.org/wiki/HDML "wikilink")である。1998年にモバイルインターネットの業界標準化団体[WAPフォーラム](https://ja.wikipedia.org/wiki/WAPフォーラム "wikilink")が発足し、HDMLをベースに最初のWMLが策定された。WMLは、その後、バージョンアップして、[XML](https://ja.wikipedia.org/wiki/XML "wikilink")にも準拠するようになった。2002年にWAP仕様は、WAP2.0にバージョンアップされたが、この中で、コンテンツ記述言語は、WML1.3、cHTML、XHTML/MPが、参加団体間の妥協の産物として併記された。XHTML/MPが採用されたことにより、これ以降、WMLを使用する利点は、オペレータにもコンテンツ・プロバイダーにもなくなったので、WMLの利用は急速に廃れた。

## 概要

携帯機器の性能向上と共に [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") や [HTML](../Page/HyperText_Markup_Language.md "wikilink") が使われるようになり、WML の利用は古い携帯機器に限られるようになってきている。

WML 文書は、WML（現在バージョン 1.3）DTD（[Document Type Definition](../Page/Document_Type_Definition.md "wikilink")）に従った XML 文書である。W3C Markup Validation サービス (http://validator.w3.org/) を使って WML 文書が正しい形式か（宣言された文書型に照らして正しいか）確認できる。

例えば、以下の WML ページを "example.wml" としてセーブするとする。

```
 <?xml version="1.0"?>
 <!DOCTYPE wml PUBLIC "-//PHONE.COM//DTD WML 1.1//EN"
    "http://www.phone.com/dtd/wml11.dtd" >
 <wml>
   <card id="main" title="First Card">
     <p mode="wrap">This is a sample WML page.</p>
   </card>
 </wml>
```

WML ページは[Webサーバ](../Page/Webサーバ.md "wikilink")上に格納される。そして、携帯電話網と World Wide Web の間にあるWAPゲートウェイを通してアクセスされる。WAPゲートウェイは一種の[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")として機能する。ページは携帯電話に適した形式に変換される。この処理は携帯電話からは見えないので、携帯電話から見れば、通常のブラウザで URL を指定して [HTML](../Page/HyperText_Markup_Language.md "wikilink") にアクセスするのと変わらない。

WML は HTML とよく似ており、ハイパーリンク、テキストと画像の混在、フォームによる入力などが可能である。WML 文書を "deck" とも呼ぶ。deck 内のデータは1つ以上の "card"（ページ）に構造化されており、各 card がユーザーとの1つの[インタラクションを表現している](../Page/相互作用.md "wikilink")。WML には手続き要素の縮小セットがあり、他の card へのナビゲーション制御を可能としている。

WAP2.0の規格制定にあたっては、WMLは、[cHTML](https://ja.wikipedia.org/wiki/cHTML "wikilink")、 XHTML/MPとならんで、コンテンツ記述言語としてかろうじて併記された。しかしながら、WMLおよびcHTMLは、ワイヤレス・インターネットの通信速度が低速であったころは存在理由があったが、今日のように比較的安価に高速な通信速度とリッチなコンテンツがある状況には、適合しなくなった。この為、WMLおよびcHTMLは、限られた環境のレガシーコンテンツで残っていることがあるだけで、消滅しつつあるコンテンツ記述言語である。

## 関連項目

  - [Compact HTML](https://ja.wikipedia.org/wiki/Compact_HTML "wikilink")
  - [WMLScript](https://ja.wikipedia.org/wiki/WMLScript "wikilink")
  - [Wireless Bitmap](https://ja.wikipedia.org/wiki/Wireless_Application_Protocol_Bitmap_Format "wikilink")
  - [マイクロブラウザ](https://ja.wikipedia.org/wiki/マイクロブラウザ "wikilink")
  - [XHTML Mobile Profile](https://ja.wikipedia.org/wiki/XHTML_Mobile_Profile "wikilink")

## 外部リンク

  - [W3Schools WAP Tutorial](http://www.w3schools.com/wap/default.asp)
  - [An Overview of Mobile Versions of XHTML](http://www.littlespringsdesign.com/design/xhtmlinfo/)
  - [XHTML-MP Authoring Practices](http://www.passani.it/gap/)
  - [DevGuru WML Quick Reference](http://devguru.com/technologies/wml/)
  - [Mobile Web Toolkit](http://www.beeweeb.com/mwt/index.php/products/mobile-web-toolkit/)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:携帯電話ブラウジング](https://ja.wikipedia.org/wiki/Category:携帯電話ブラウジング "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")