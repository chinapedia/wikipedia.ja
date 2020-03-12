> この記事は[YAML](https://ja.wikipedia.org/wiki/YAML)から翻訳されています。


**YAML**（ヤメル\[1\]\[2\]、ヤムル\[3\]）とは、構造化データや[オブジェクトを](../Page/オブジェクト_\(プログラミング\).md "wikilink")[文字列](../Page/文字列.md "wikilink")に[シリアライズ](../Page/シリアライズ.md "wikilink")（直列化）するための[データ形式の一種](../Page/ファイルフォーマット.md "wikilink")。

## 特徴

[テキストのため可読である](../Page/テキストファイル.md "wikilink")。その概念は[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である[C](../Page/C言語.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")からきている。 YAMLの原案はClark Evans、Brian Ingerson、Oren Ben-Kikが共同で出した。

YAMLは[再帰的に定義された頭字語であり](../Page/再帰的頭字語.md "wikilink") "YAML Ain't a Markup Language"（YAMLは[マークアップ言語](../Page/マークアップ言語.md "wikilink")ではない）の意味である。初期には "Yet Another Markup Language"（もうひとつ別のマークアップ言語）の意味と言われていたが、マークアップよりもデータ重視を目的としていたために後付されてできた名前である。しかしながら [XML](../Page/Extensible_Markup_Language.md "wikilink")（本当のマークアップ言語）が[データシリアライズ目的のために頻繁に使用されるため](../Page/シリアライズ.md "wikilink")、 YAMLを[軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")と考えることもできる。類似の規格として[JSONがある](../Page/JavaScript_Object_Notation.md "wikilink")。

## 表記方法

[インデントを使い階層構造を表現する](../Page/字下げ.md "wikilink")。ただし、インデントには[タブが使えず](../Page/タブキー.md "wikilink")[スペース](../Page/スペース.md "wikilink")のみが使える\[4\]。スペース2個単位でインデントすることが多い。

## 例

`#` は行コメント。`---`は、一つのファイル内に複数のYAMLドキュメントを埋め込むときに用いるセパレータ。

### リスト

``` yaml
--- # お好みの映画、ブロック形式
- Casablanca
- Spellbound
- Notorious
--- # 買い物リスト、インライン形式、またはフロー形式
[milk, bread, eggs]
```

### 連想配列

``` yaml
 --- # ブロック
 name: John Smith
 age: 33
 --- # インライン
 {name: John Smith, age: 33}
```

### 各行の改行の維持

``` yaml
 --- |
   There was a young fellow of Warwick
   Who had reason for feeling euphoric
       For he could, by election
       Have triune erection
   Ionic, Corinthian, and Doric
```

### 最終行の改行のみ維持し他はスペース一字に置換

``` yaml
 --- >
   Wrapped text
   will be folded
   into a single
   paragraph

   Blank lines denote
   paragraph breaks
```

### ハッシュのリスト

``` yaml
 - {name: John Smith, age: 33}
 - name: Mary Smith
   age: 27
```

### リストのハッシュ

``` yaml
 men: [John Smith, Bill Jones]
 women:
   - Mary Smith
   - Susan Williams
```

## 実装

YAMLは次の言語で利用可能である。

  - [Actionscript](https://ja.wikipedia.org/wiki/Actionscript "wikilink")
  - [C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")/[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [Cocoa](../Page/Cocoa.md "wikilink")
  - [Dart](https://ja.wikipedia.org/wiki/Dart "wikilink")
  - [Golang](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")
  - [Haskell](../Page/Haskell.md "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [JavaScript](../Page/JavaScript.md "wikilink")
  - [Lua](../Page/Lua.md "wikilink")
  - [Nim](https://ja.wikipedia.org/wiki/Nim "wikilink")
  - [OCaml](../Page/OCaml.md "wikilink")
  - [Perl](../Page/Perl.md "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") (PECLのモジュールや[Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")のYAMLコンポーネントがある)
  - [Python](../Page/Python.md "wikilink")
  - [Ruby](../Page/Ruby.md "wikilink") (Ruby 1.8から標準ライブラリに含まれる。)
  - [Rust](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")
  - [Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")
  - [Vim](../Page/Vim.md "wikilink")
  - [XML](../Page/Extensible_Markup_Language.md "wikilink") (ドラフト段階)

## 脚注

## 関連項目

  - [データ記述言語](../Page/データ記述言語.md "wikilink")
  - [マークアップ言語](../Page/マークアップ言語.md "wikilink")
  - [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")

## 外部リンク

  -
  - [YAML検証ツール](https://codebeautify.org/yaml-validator) YAML Lint

  - [YAML検証ツール](https://www.yamlonline.comr) YAML Lint|YAML TO JSON Converter

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink")

1.
2.
3.
4.