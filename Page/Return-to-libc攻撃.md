> この記事は[Return-to-libc](https://ja.wikipedia.org/wiki/Return-to-libc)から翻訳されています。


**Return-to-libc攻撃**とは、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")によって[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")上の[リターンアドレスを別の](https://ja.wikipedia.org/wiki/Return文 "wikilink")[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")へのアドレスへ書き換え、さらにスタック上の引数に当たる位置も書き換えることで、[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")を呼び出させる[コンピュータセキュリティ](../Page/コンピュータセキュリティ.md "wikilink")の攻撃手法である。攻撃者は、悪意あるコードをプログラムに注入することなく、単に既存の関数を呼び出すだけで攻撃を行う。

[Unix系](../Page/Unix系.md "wikilink")システムでは、[C言語](../Page/C言語.md "wikilink")ランタイムとして "[`libc`](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")" という共有ライブラリが使われる（[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink") でも該当するライブラリが存在する）。[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")では攻撃者は任意のコードに戻るように細工できるが、常にリンクされていて攻撃に使い易い機能が多く存在する `libc` をターゲットとすることが多い（例えば、[`system`](https://ja.wikipedia.org/wiki/:en:system_\(C_standard_library\) "wikilink")`()` は引数さえ正しく指定すれば、任意のプログラムを実行できる）。このため、全く別の場所を呼び出すようになっていても総称として "return-to-libc" と呼ぶ。

## 防御方法

スタックに実行コードを書き込むようなバッファオーバーランを利用した攻撃の場合と異なり、[NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")でスタック上のコード実行を防御しても、return-to-libc攻撃ではスタック上のコードを実行するわけではないので、防ぐことができない。[Stack smashing protection](https://ja.wikipedia.org/wiki/バッファオーバーフロー防御 "wikilink") は、スタック内容の破壊を検出したり、可能であれば破壊されたセグメントを復旧することで、この種の攻撃を防御できる。

[ASLR](https://ja.wikipedia.org/wiki/ASLR "wikilink") (Address Space Layout Randomization) は、実行プログラムの各モジュールのコードが配置される位置をランダム化することで、狙い撃ちでコードを実行されることを防ぐ。ASLRは、特に[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")システム上での攻撃成功確率を劇的に低下させる。[32ビット](../Page/32ビット.md "wikilink")システムでは、一般的には16ビット分のランダム化しか提供しないため（すなわち65536通り）、総当たり攻撃により分単位で攻撃を成功されてしまう可能性がある。

## 関連項目

  - [バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")
  - [スタックオーバーフロー](https://ja.wikipedia.org/wiki/スタックオーバーフロー "wikilink")
  - [NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")
  - [PaX](../Page/PaX.md "wikilink")

## 参考文献

  -
## 外部リンク

  - [Bypassing non-executable-stack during exploitation using return-to-libc](http://www.infosecwriters.com/text_resources/pdf/return-to-libc.pdf) by c0ntex at InfoSecWriters.com

[Category:エクスプロイト](https://ja.wikipedia.org/wiki/Category:エクスプロイト "wikilink") [Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")