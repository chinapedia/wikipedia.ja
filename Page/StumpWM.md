> この記事は[StumpWM](https://ja.wikipedia.org/wiki/StumpWM)から翻訳されています。


**StumpWM**は、ソフトウェア開発者のShwan Bettsによって作られた[タイル型ウィンドウマネージャ](https://ja.wikipedia.org/wiki/タイル型ウィンドウマネージャ "wikilink")である。[ratpoison](https://ja.wikipedia.org/wiki/ratpoison "wikilink")が肥大化していることをきっかけに、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")を用いて作られた。ratposionの後継となることを意図されており、StumpWMは、[GNU GPLv](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink")2の下でリリースされている\[1\]。

StumpWM wikiにおける説明によると、WMの開発者は、ratipoisonを[CLX](https://ja.wikipedia.org/wiki/CLX "wikilink")を使って[Common Lispで再実装することを意図している](../Page/Common_Lisp.md "wikilink")\[2\]。

## Lispとカスタマイズ

StumpWMは、Steel Bank Common Lisp（SBCL）と、[GNU](../Page/GNU.md "wikilink") CLISPにおいて動作し、このうちSBCLがよりよいパフォーマンスのために好まれる\[3\]。Superior Lisp Interaction Mode for Emacs（SLIME）環境は、StumpWMのリアルタイムのアップデートとカスタマイズに広く使用される。また、*stumpish*（"StumpWM Interactive Shell"）と呼ばれるプログラムが存在し、これは[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")からウィンドウマネージャにアクセスする標準的なインターフェイスを提供している\[4\]。

StumpWMは、各ユーザのホームディレクトリに存在する*.stumpwmrc*ファイルにカスタマイズ設定を保存する。このファイルは、StumpWMを設定するためのLispのコードが含まれている\[5\]。

## 開発

StumpWMのソースコードは[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")にホストされており、[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")に[Git](../Page/Git.md "wikilink")を用いて開発されている\[6\]。また、メーリングリストが存在し、これはStumpWMに関連する問題を扱っている\[7\]。

## 関連項目

  - [Sawfish](https://ja.wikipedia.org/wiki/Sawfish "wikilink")

## 脚注

### 出典

[Category:Xウィンドウマネージャ](https://ja.wikipedia.org/wiki/Category:Xウィンドウマネージャ "wikilink")

1.
2.
3.
4.
5.
6.
7.