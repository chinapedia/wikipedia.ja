> この記事は[ConTeXt](https://ja.wikipedia.org/wiki/ConTeXt)から翻訳されています。


**** (**ConTeXt**) は、[](../Page/TeX.md "wikilink") (TeX) [組版](../Page/組版.md "wikilink")システムに基づいた文書作成システムの一種である。

## 概要

[](../Page/LaTeX.md "wikilink") (LaTeX) と同様の汎用目的で設計されているが、比較的新しいためにマークアップなどの最近の考え方が取り入れられ、概念的にはよりモジュール化が進み、実装はよりモノリシックとなっている。 はエンドユーザーの自由度が向上していて、 のマクロ言語を学ばなくとも新たなレイアウトを容易に生成できる。 は設計が一貫していて、 で起きやすいパッケージの組み合わせによる不具合は発生しない。

は教材・ユーザーガイド・技術マニュアルといった、複雑で大きな文書の組版に用いられる。そのような文書は、構造・設計・アクセス可能性について高い水準を要求されることが多い。保守が容易であること、内容を再利用できること、組版の一貫性が重要な前提条件となる。 はそのような文書作成を行う人のために開発された。 は  を使っているが、利用にあたって  に関する知識は不要である。組版や文書設計について基本的な知識があれば  を充分に活用できる。

には [MetaPost](https://ja.wikipedia.org/wiki/MetaPost "wikilink") を拡張した MetaFun が組み込まれていて、強力な[ベクターグラフィックス](https://ja.wikipedia.org/wiki/ベクターグラフィックス "wikilink")システムを備えている。MetaFun は単独でも利用可能だが、その強みは精細なグラフィック要素を使って文書レイアウトを拡張できることにある。

では、ユーザインタフェースを変えずにエンジン部 ([pdf](https://ja.wikipedia.org/wiki/pdfTeX "wikilink") (pdfTeX), [](https://ja.wikipedia.org/wiki/XeTeX "wikilink") (XeTeX, [XeTeX_Logo.svg](https://ja.wikipedia.org/wiki/File:XeTeX_Logo.svg "fig:XeTeX_Logo.svg")), [](https://ja.wikipedia.org/wiki/LuaTeX "wikilink") (LuaTeX)) を入れ替えることができる。

は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")の企業 PRAGMA Advanced Document Engineering (PRAGMA ADE) の Hans <span style="font-variant: small-caps">Hagen</span> が開発した。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

上で[分子構造式を描く](https://ja.wikipedia.org/wiki/化学式 "wikilink")[マクロパッケージとして](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink") <span style="text-transform: lowercase">PPCH</span> (PPCHTeX) がある。これも  のマクロパッケージの一部であるが、 などでも利用可能である。

## 機能詳細

  - 図、数式、表などの浮動体を自動的に配置
  - 略語、同義語などソートが必要なリストを自動的に生成
  - 脚注を自動的に番号付け
  - フッターとヘッダーをページの中身によって調整
  - 箇条書きの形式を拡張可能
  - 数式の記号の一貫した組版
  - 拡張可能なクロスリファレンス機能
  - 図や表や数式を使った箇条書きが可能
  - 一部の文字列を全体を通して強調印字可能
  - プロジェクト環境での文書管理
  - 傍注の自動配置
  - 複数カラムでの組版
  - 文書の一部をまとめて認識し、それを隠したり、移動させたり、コピーしたりできる（問題・解答・定義など）
  - 1つのテキストを複数の文書に利用でき、必要ならレイアウトを変更可能
  - 単語のハイフネーションや言語の特性への適応
  - 他のアプリケーションで作成した標準的形式のイラストを組み込み可能
  - カラーを使用可能
  - 組版の一貫性を保ったまま、レイアウトを容易に変更
  - 目次を各種レベルで生成可能
  - 定理や補題などの要素を自動番号付け
  - 図、表などを自動番号付け
  - 表や数式の自動組版

は [PDF](../Page/Portable_Document_Format.md "wikilink") 形式をサポートしていて、pdf を使ってインタラクティブな PDF ファイルを直接生成可能である。クロスリファレンスは全て[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")に変換される。そのように作成された文書は [Adobe Acrobat](../Page/Adobe_Acrobat.md "wikilink") で参照・編集可能である。ナビゲーション的要素は全てプログラミング無しで実現できるため、教材などの作成には効果を発揮する。

## 脚注・出典

<references/>

## 外部リンク

  - [PRAGMA ADE web page: text](http://www.pragma-ade.nl/)…… の配布元
  - [the Comprehensive  Archive Network](http://www.ctan.org/) (CTAN)
      - [The  Catalogue OnLine, Entry for , Ctan Edition](http://www.ctan.org/get/help/Catalogue/entries/context.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/context.html)）
  - [The ConTeXt wiki](http://contextgarden.net/)

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink")