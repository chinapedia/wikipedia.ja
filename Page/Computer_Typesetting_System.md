> この記事は[Computer Typesetting System](https://ja.wikipedia.org/wiki/Computer_Typesetting_System)から翻訳されています。


**Computer Typesetting System**（CTS、Computerized Typesetting System、**コンピュータ組版**ともいう）とは、[コンピュータ](../Page/コンピュータ.md "wikilink")を使用した[組版](../Page/組版.md "wikilink")システムのことを言う。組版システムをコンピュータ化するには、コンピュータで文字を扱うための[文字コード](../Page/文字コード.md "wikilink")規格が前提となり、システムとしては文字コードを入力・編集・処理する機能、レイアウトを指定する機能、[版下](../Page/版下.md "wikilink")を出力する機能の3要素が揃う必要がある。汎用コンピュータを組版に初めて使ったのはフランスのGeorges P. Bafourらで1954年に特許を申請している。米国では1960年代初頭から[M.I.T.などで研究が始まった](../Page/マサチューセッツ工科大学.md "wikilink")。

## 電算写植

日本では[電算写植](../Page/電算写植.md "wikilink")（電算植字）システムとして1970年代に実用化された。写植は、[鉛](https://ja.wikipedia.org/wiki/鉛 "wikilink")を溶かして作った[活字](../Page/活字.md "wikilink")を使うホットタイプに対する意味として、コールドタイプと呼ばれることから、電算写植は「**Cold Type System**」の略としてCTSともいわれる\[1\]。この意味の「CTS」という言葉は、特に新聞社や印刷会社などで素材の集配信から組版、出力まで使用する比較的大規模な組版システムのことを指す場合が多い。例えば、朝日新聞社が1970年代初めに運用開始した電算写植システムNELSONは、漢字キーボードによる原稿パンチとスキャナによる写真・カット入力装置、ディスプレイと漢字プリンタを組み合わせた校閲・前組・大組などの編集装置、記事・写真・カットなど組み合わせた完全な新聞紙面をネガフィルムに出力する全ページ写植機などから構成された。

初期の電算写植システムは、入力・編集・出力をそれぞれ専用の機器を使って行うバッチ方式であった。こうしたバッチ方式ではまとまったページ数を一括して処理するとともに工程ごとに作業担当者を置くのでシステムが大掛かりなものであった。コンピュータの処理能力の向上に伴いCTSも対話方式／[WYSIWYG](../Page/WYSIWYG.md "wikilink")方式に移行した。対話方式／WYSIWYG方式は小規模のシステムになるので印刷業界に広く受けいれられた。

## DTP

米国では1985年に[Appleの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")とともに[DTP](../Page/DTP.md "wikilink")が普及しはじめ、日本でも1986年から1987年にかけてDTP元年と騒がれた。DTPはレイアウト編集をWYSIWYGで行い、[ページ記述言語](../Page/ページ記述言語.md "wikilink")（PDL）でレイアウト結果を出力する。[PostScript](../Page/PostScript.md "wikilink")がPDLのデファクト・スタンダードとなった。当初はPostScriptに対応する日本語[Type 1フォントが少ないことなどで](../Page/PostScriptフォント.md "wikilink")、プロユースとしてはなかなか使えなかった。

DTPで出力するデータはPostScriptのプログラムであり、商業印刷ではこれをイメージセッターで版下とする。企業内印刷では[レーザープリンタ](https://ja.wikipedia.org/wiki/レーザープリンタ "wikilink")が使われた。1990年代初めにはPostScriptに対応する日本語フォントが充実し、ラスターイメージプロセサ（RIP）が改良されるなど、DTPの実用的環境が整った。

電算写植システムは、1990年代にはDTPによって代替された。

現在の[タイポグラファー](../Page/タイポグラファー.md "wikilink")（現代の植字工）の手元のコンピュータには、次のものが含まれる：テキストエディタ、組版ソフトウエア（composition software）、デジタルフォントのライブラリー、フォント管理ツールとフォントエディタ。

## バッチ組版の流れ

組版システムにはバッチ方式と対話方式がある。初期の組版システムはすべてバッチ方式であった。バッチ方式では文章データ中に組版体裁を制御する指令を混在させるのが一般的である。各社の独自開発したもののほか、1970年代後半には[TeX](../Page/TeX.md "wikilink")のように誰でもオープンに使えるものが誕生した。

印刷の対象となるテキストや画像に対して、指示マークを付けることをマークアップという\[2\]。

マークアップ標準化の流れとして[SGML](https://ja.wikipedia.org/wiki/SGML "wikilink")が作られ、その後継として1998年に[XML](https://ja.wikipedia.org/wiki/XML "wikilink")が登場した。SGMLのレイアウト指定の標準として[DSSSL](https://ja.wikipedia.org/wiki/DSSSL "wikilink")、XMLのレイアウト指定の標準として[XSL-FO](https://ja.wikipedia.org/wiki/XSL-FO "wikilink")がある。現在のバッチ処理はデータベースに保管したマークアップ文書をサーバ上で自動組版する仕組みが主流である。その典型的な例として[Darwin Information Typing Architecture](../Page/Darwin_Information_Typing_Architecture.md "wikilink")（DITA）のPDF作成が挙げられる。

## コンピュータ組版と職人の技

コンピュータ組版では改行位置の決定などの低レベルなレイアウトはプログラムで自動的に行う。これによって作業の効率と品質の均一化を保つことができる。改行位置は意味を加味して決定する場所がある。こうしたとき必ずしもコンピュータ組版で品質が上がっていると言えない。例えば、英文であるがMonotypeを使って手動で組まれた1960年版のACM Journalと、当時商用で最高といわれた数式組版システムで組まれた1980年版のACM Journalの先頭1000行を比較すると、1960年版は改行位置が良くないのが13カ所、1980年版は同55カ所であった。

コンピュータ組版の品質を上げるには組版規則を標準化してプログラムに組み込む必要がある。日本では[JIS X 4051が策定された](https://ja.wikipedia.org/wiki/JIS_X_4051 "wikilink")。

## 脚注

## 参考文献

  - Donald E. Knuth and Michael F. Plass "Breaking Paragraph into Lines", Software-Practice and Experience, Vol. 11, 1119-1184, 1981.
  - [Robert Bringhurst](https://ja.wikipedia.org/wiki/Robert_Bringhurst "wikilink") "The Elements of Typographic Style (Fourth Edition)", Hartley & Marks, 2016.
  - 大泊勝「新聞の電算写植システム」、『電気学会雑誌』98 巻 (1978) 11 号、1082-1085。
  - 小野澤賢三 「JIS X 4051 “日本語文書の行組版方法”の概要」、日本印刷学会誌第32巻第6号、1995年、328-333。
  - 島袋徹「プリプレス入門―１ CTS概論」、日本印刷学会誌第29巻第4号、1992年 437-444。
  - 島袋徹・高司誠喜 「プリプレス入門―２ 組版編集システム」、日本印刷学会誌第29巻第6号、1992年、521-530。
  - [中西秀彦](https://ja.wikipedia.org/wiki/中西秀彦 "wikilink") 『学術出版の技術変遷論考』、印刷学会出版部、2011年。
  - 浜谷卓美「DTPの現在」『情報の科学と技術』43巻（1993）12号、1071-1076
  - 布施茂編『技術者たちの挑戦　写真植字技術史』、創英社、2016年。

## 関連項目

  - [組版](../Page/組版.md "wikilink")
  - [電算写植](../Page/電算写植.md "wikilink")
  - [DTP](../Page/DTP.md "wikilink")
  - [印刷](../Page/印刷.md "wikilink")
  - [出版](../Page/出版.md "wikilink")
  - [新聞](../Page/新聞.md "wikilink")

[Category:印刷](https://ja.wikipedia.org/wiki/Category:印刷 "wikilink")

1.
2.