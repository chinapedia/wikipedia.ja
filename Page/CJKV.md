> この記事は[CJKV](https://ja.wikipedia.org/wiki/CJKV)から翻訳されています。


[CJKV-logo.png](https://ja.wikipedia.org/wiki/File:CJKV-logo.png "fig:CJKV-logo.png") **CJKV** は、[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")・[日本語](../Page/日本語.md "wikilink")・[朝鮮語](../Page/朝鮮語.md "wikilink")・[ベトナム語](../Page/ベトナム語.md "wikilink") () の略。特に、その四[言語](../Page/言語.md "wikilink")で共通して使われる、または使われていた[文字体系](https://ja.wikipedia.org/wiki/文字体系 "wikilink")である[漢字](../Page/漢字.md "wikilink")（[チュノム](../Page/チュノム.md "wikilink")を含む）のこと。[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[国際化](../Page/国際化と地域化.md "wikilink")、中でも[文字コード](../Page/文字コード.md "wikilink")に関する分野で用いられる。

比較的早くに漢字を廃止し、漢字に含めるべきか諸説あるチュノムを擁するベトナム語を除いた[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")、[日本語](../Page/日本語.md "wikilink")、[朝鮮語](../Page/朝鮮語.md "wikilink")の頭文字だけをとって **CJK** と呼ぶこともある。主な[東アジア](../Page/東アジア.md "wikilink")の[書記系](https://ja.wikipedia.org/wiki/書記系 "wikilink")を総称するときに用いられる。用語の使用頻度は CJKV より CJK のほうが多いが、CJK と言いながら実際は CJKV について述べていることも多い。

## 特徴

### マルチバイト文字

中国語・日本語・朝鮮語を[コンピュータ](../Page/コンピュータ.md "wikilink")で扱う場合、英数字と[プログラミング](../Page/プログラミング.md "wikilink")や操作に使われる記号に加え、[漢字](../Page/漢字.md "wikilink")・[平仮名](../Page/平仮名.md "wikilink")・[片仮名](../Page/片仮名.md "wikilink")・[ハングル](https://ja.wikipedia.org/wiki/ハングル "wikilink")が必要となる。これらの文字集合は、欧米の言語の多くが用いているような[アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink")とは異なり、1 [バイト](../Page/バイト_\(情報\).md "wikilink") (8[ビット](../Page/ビット.md "wikilink")) で表現できる文字の総数を大きく越えている。このため、これらの言語では[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")を使うことになる。

### 文字の入力

漢字・平仮名・片仮名・ハングル（特に漢字）は[文字集合](../Page/文字集合.md "wikilink")が大きいので、すべての文字を[キーボードに直接割り当てると巨大なものとなり](../Page/キーボード_\(コンピュータ\).md "wikilink")、習得は難しくなってしまう。そのため現在では、英字キーボード、もしくはそれにいくつかのキーを追加したキーボードとソフトウェアによる[インプットメソッド](../Page/インプットメソッド.md "wikilink")を使用して入力することが一般的である。そのためには入力先となるソフトウェアが、使用しているインプットメソッドに対応している必要がある。

漢字を用いる日本語と中国語では、読みを入力してソフトウェアで変換を行い、目的の表記を得る種類のインプットメソッドが一般的である（[ATOK](../Page/ATOK.md "wikilink")、[SKK](../Page/SKK.md "wikilink") など）。読みによるインプットメソッドは、さらに変換の区切りによって漢字 1 文字を単位とする[単漢字変換](https://ja.wikipedia.org/wiki/単漢字変換 "wikilink")、漢字[熟語](../Page/熟語.md "wikilink")と助詞で構成される[文節](../Page/文節.md "wikilink")の並びを単位とする[連文節変換](https://ja.wikipedia.org/wiki/連文節変換 "wikilink")などに分けられる。中国語では文字全体の形状の分類と一部の[筆画](../Page/筆画.md "wikilink")を与えて漢字を特定するなど、字の構造に基づくインプットメソッドも使われている\[1\]。 朝鮮語のインプットメソッドでは、ハングルを構成する要素である[チャモ](https://ja.wikipedia.org/wiki/チャモ "wikilink")（字母）単位で入力を行う方法が一般的である\[2\]。

### 組版

主に紙面上の文書を作る際、CJKV では欧米言語と異なる[組版](../Page/組版.md "wikilink")の方法が必要になる。

**縦書き**（**縦組み**）はその一つである。コンピュータのテキスト表示および処理は元来横書きであったが、CJK/CJKV のテキストは伝統的に縦書きであるため、組版では縦書きへの対応が求められる。その際には単に縦に表示するだけではなく、文字の間隔や配置を縦書き対応にしなければならない\[3\]。

また、CJKV の組版では縦組み、横組みのどちらであっても、正方形で構成される[格子](../Page/格子.md "wikilink")上に文字を配置する機能が求められる。これは、漢字・平仮名・片仮名・ハングルなど CJKV 特有の文字の大半が、正方形に合う[字形](https://ja.wikipedia.org/wiki/字形 "wikilink")を持つためである。しかし、一部の記号や[ラテン文字](../Page/ラテン文字.md "wikilink")はそうでないため、それらが混在する文書では縦書き用文字への置き換えなど、複雑な処理が必要になる\[4\]。

CJKV に適用できる組版規則を定めた[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")としては、[JIS X 4051](../Page/JIS_X_4051.md "wikilink")-1995 （2004年に改正）が知られている\[5\]。

## 文字コード規格

###

の [CJK統合漢字](../Page/CJK統合漢字.md "wikilink")は、ベトナムの[符号化文字集合](https://ja.wikipedia.org/wiki/符号化文字集合 "wikilink")規格である [TCVN 5773](https://ja.wikipedia.org/wiki/TCVN_5773 "wikilink"):1993 と [TCVN 6056](https://ja.wikipedia.org/wiki/TCVN_6056 "wikilink"):1995 の漢字（[チュニョ](https://ja.wikipedia.org/wiki/チュニョ "wikilink")とチュノム）も[原規格](https://ja.wikipedia.org/wiki/原規格 "wikilink")として統合しており、実態は CJKV である。例えば、「 畑」には、日本語の[国字](../Page/国字.md "wikilink")の「畑」 ([JIS X 0208](../Page/JIS_X_0208.md "wikilink")-1990 の 482A) とチュノムの「畑」 (TCVN 5773:1993 の 3C2F) が統合されている。

## 脚注

## 参考文献

  -
## 関連項目

  - [FIGS](https://ja.wikipedia.org/wiki/FIGS "wikilink") （[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")・[イタリア語](../Page/イタリア語.md "wikilink")・[ドイツ語](../Page/ドイツ語.md "wikilink")・[スペイン語](https://ja.wikipedia.org/wiki/スペイン語 "wikilink")）
  - [インプットメソッド](../Page/インプットメソッド.md "wikilink")
  - [漢字](../Page/漢字.md "wikilink")
      - [朝鮮における漢字](https://ja.wikipedia.org/wiki/朝鮮における漢字 "wikilink")
      - [日本における漢字](../Page/日本における漢字.md "wikilink")
      - [チュノム](../Page/チュノム.md "wikilink")、[チュニョ](https://ja.wikipedia.org/wiki/チュニョ "wikilink")
  - [縦書きと横書き](../Page/縦書きと横書き.md "wikilink")
  - [文字コード](../Page/文字コード.md "wikilink")
      - [CJK統合漢字](../Page/CJK統合漢字.md "wikilink")
      - [マルチバイト文字](../Page/マルチバイト文字.md "wikilink")

## 外部リンク

  - [CJKV統合漢字](http://e-words.jp/w/CJKVE7B5B1E59088E6BCA2E5AD97.html) - IT用語辞典 e-Words。
  - [CJKとは](http://www.keyman.or.jp/it-word/21/61003353/?vos=evpakey0008x0003446) - [キーマンズネット](../Page/キーマンズネット.md "wikilink")

[Category:頭字語](https://ja.wikipedia.org/wiki/Category:頭字語 "wikilink") [Category:中国語](https://ja.wikipedia.org/wiki/Category:中国語 "wikilink") [Category:日本語](https://ja.wikipedia.org/wiki/Category:日本語 "wikilink") [Category:朝鮮語](https://ja.wikipedia.org/wiki/Category:朝鮮語 "wikilink") [Category:ベトナム語](https://ja.wikipedia.org/wiki/Category:ベトナム語 "wikilink") [Category:漢字](https://ja.wikipedia.org/wiki/Category:漢字 "wikilink") [Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")

1.  [ランディ(2002)](https://ja.wikipedia.org/wiki/#ランディ2002 "wikilink")、pp.231-237
2.  [ランディ(2002)](https://ja.wikipedia.org/wiki/#ランディ2002 "wikilink")、pp.266-267
3.  [ランディ(2002)](https://ja.wikipedia.org/wiki/#ランディ2002 "wikilink")、p.347
4.  [ランディ(2002)](https://ja.wikipedia.org/wiki/#ランディ2002 "wikilink")、p.349
5.  [ランディ(2002)](https://ja.wikipedia.org/wiki/#ランディ2002 "wikilink")、pp.341-343