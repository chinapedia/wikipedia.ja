> この記事は[ERuby](https://ja.wikipedia.org/wiki/ERuby)から翻訳されています。


**eRuby**とは、[Ruby](../Page/Ruby.md "wikilink")の周辺技術の一つで、[HTMLへRubyスクリプトを埋め込む事を可能とする技術である](../Page/HyperText_Markup_Language.md "wikilink")。**embedded Ruby**の略。**ERB**とも表記され、ファイル拡張子も.erbである事が多い。対象としてはHTMLだけでなく、任意の[プレインテキスト](https://ja.wikipedia.org/wiki/プレインテキスト "wikilink")に適用できる。[Ruby on Railsの](https://ja.wikipedia.org/wiki/Ruby_on_Rails "wikilink")[MVCの内で](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")、Viewの開発言語にも採用されている。

元々[まつもとゆきひろ](../Page/まつもとゆきひろ.md "wikilink")の構想と[ePerl](https://ja.wikipedia.org/wiki/ePerl "wikilink")の実装を基にした議論から、関将俊が開発した[1](http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-dev/6055)。Ruby 1.8以降のバージョンでは、Ruby処理系の標準ライブラリとして同梱されるようになった。また、前田修吾によるC実装によるeRuby処理系も開発されている[2](http://www.modruby.net/ja/index.rbx/eruby/whatis.html)。

## 概要

従来、Rubyで[CGIなどを作成するとき](../Page/Common_Gateway_Interface.md "wikilink")、HTML部分を記述するにはprint（もしくはputs）によってそのコードを記述していかなければならなかった。しかし、HTMLのタグを書く毎にprint文を記述するのは非常に手間がかかり、修正する場合にも多大な労力を必要としてしまうことが多い。

さらにこの方式では、CGIや[WEBアプリケーションを作成しようとしたとき](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、プログラマーと[WEBデザイナーの分離が難しく](https://ja.wikipedia.org/wiki/ウェブデザイナー "wikilink")、また[Dreamweaverなどの](https://ja.wikipedia.org/wiki/Adobe_Dreamweaver "wikilink")[WEBオーサリングツールの利用も不可能となってしまう](../Page/Webオーサリングツール.md "wikilink")。

そこで考え出されたのが、HTML埋め込み型の処理系である[PHPに似た文法で](../Page/PHP_\(プログラミング言語\).md "wikilink")、HTMLにRuby文を埋め込む実装である。こうして考え出されたのが、eRubyである。

## 文法

HTMLファイルの中に\<%...%\> （もしくは、\<%=...%\>。こちらは、\<%print ...%\>の省略形である）の記号で囲った空間があれば、そこをRubyが書かれた部分として認識する。

``` html+erb
<html>
<head>
<title>eRuby</title>
</head>
<body>
<p><% Rubyコード1 %></p>
<p><% Rubyコード2 %></p>
<p><% Rubyコード3 %></p>
</body>
</html>
```

以上のように\<%...%\>と記述した箇所で、Rubyの命令が実行可能となる。それ以外の場所では、通常のHTML文が表示され、PHPと似た記述が可能となる。

## その他の実装

Rubyの標準添付ライブラリのERB以外にも、ERBの実装が存在する。

  - [Erubis](https://github.com/kwatch/erubis)
    ERBより高速なことを特徴とする。Ruby on Rails 5.0まで採用されていた。
  - [Erubi](https://github.com/jeremyevans/erubi)
    Erubisより高速であることを特徴とする。Ruby on Rails 5.1以降、採用されている\[1\]。

## 脚注

## 外部リンク

  - [Ruby リファレンスマニュアル \> ライブラリ一覧 \> erbライブラリ](https://docs.ruby-lang.org/ja/latest/library/erb.html)（Ruby標準添付ライブラリであるERBのマニュアル）
  - [ERB](http://www2a.biglobe.ne.jp/~seki/ruby/erb.html) 公式サイト

[Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink") [Category:テンプレートエンジン](https://ja.wikipedia.org/wiki/Category:テンプレートエンジン "wikilink")

1.