> この記事は[Less](https://ja.wikipedia.org/wiki/Less)から翻訳されています。


**less**（レス）は、[Unix系](../Page/Unix系.md "wikilink")のシステムにおいて、[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")の内容を閲覧するために用いられるプログラム（[ページャ](https://ja.wikipedia.org/wiki/ページャ "wikilink")）である。[`more`](https://ja.wikipedia.org/wiki/more_\(UNIX\) "wikilink")に似ているが、前方向だけでなく後方向にもスクロールできるよう拡張されている。

## 使用法

構文は次の通りである。

`less [options] `<file_name>

`less`はオプションを指定することで振る舞いを変えることができる。例えば、スクリーン上に表示する行数などである。これらのオプションはシステムによって異なる可能性がある。閲覧中にはさまざまなコマンドが利用できるが、これらのコマンドは[`more`](https://ja.wikipedia.org/wiki/more_\(UNIX\) "wikilink")や[`vi`](https://ja.wikipedia.org/wiki/vi "wikilink")のものに基づいている。[インクリメンタルサーチ](https://ja.wikipedia.org/wiki/インクリメンタルサーチ "wikilink")によるパターン検索も可能である。

デフォルトでは、`less`はファイルの内容を[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")に書き出す。出力が[端末](../Page/端末.md "wikilink")以外のものに[リダイレクトされた場合](https://ja.wikipedia.org/wiki/リダイレクト_\(CLI\) "wikilink")、例えば[パイプによって別のコマンドに渡された場合](../Page/パイプ_\(コンピュータ\).md "wikilink")、`less`は`cat`コマンドのように振舞う。

## 作者･著作権他

`less`は[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")にMark Nudelmanによって書かれ、2012年現在は[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部となっている。大抵の[オープン・ソースに基づくUNIX系システムには含まれているユーティリティである](../Page/オープンソース.md "wikilink")。

## 日本語への対応

オリジナルの`less`はそのままでは日本語を表現するために広く用いられていた[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")（JISコード）、[EUC-JP](../Page/EUC-JP.md "wikilink")や[Shift_JIS](../Page/Shift_JIS.md "wikilink")を正しく表示することができなかった（ただし オリジナルのバージョン346以降はUTF-8の表示への対応を謳っている\[1\]）。

これに対処するためKazushi (Jam) Marukawaらがオリジナルのソースに対するパッチを制作した。パッチを適用したコマンドは**jless**と呼ばれており、上記の複数の漢字コードの自動認識、自動変換に対応している。これは日本国内において広く受け容れられ、[FreeBSD](../Page/FreeBSD.md "wikilink") ports collectionにも含まれている\[2\]。また[Microsoft Windowsにも移植されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。しかしながらjlessには以下のような問題もある。

### jlessの問題点

  - Marukawaがjlessのパッチを配布していた公式サイトは2010年現在アクセスできない状況にある\[3\]。開発は事実上停止していると言ってもよい状況である。
  - オリジナルの`less`はしばしばアップデートが行われるが、jlessは最も新しいものでもバージョン382に対するパッチとして提供されている。
  - Unicodeに対応していない。特に、最近のlinuxのディストリビューションでは、インストール時に「利用する言語」として日本語を選ぶと標準のエンコーディングとしてUTF-8が採用されるケースが多いが、jlessではUTF-8をうまく表示できない。(j)lessに代えてページャとして、UTF-8、UTF-7他多くのエンコーディングに対応している`lv`\[4\]を採用しようという動きも見られるが、lvの機能がlessの全ての機能をカバーするわけではない。

## 脚注

## 注

<div class="references-small">

<references group="注" />

</div>

## 外部リンク

  - [The LESS Home Page（英語）](http://www.greenwoodsoftware.com/less/)
  - [Manpage of LESS（日本語）](https://linuxjm.osdn.jp/html/GNU_less/man1/less.1.html)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")

1.
2.
3.  Web Archiveされたものが残っている。
4.