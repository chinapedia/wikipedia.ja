> この記事は[Lint](https://ja.wikipedia.org/wiki/Lint)から翻訳されています。


**lint** とは、主に[C言語](../Page/C言語.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")に対し、[コンパイラ](../Page/コンパイラ.md "wikilink")よりも詳細かつ厳密なチェックを行うプログラムである。静的解析ツールとも呼ばれる。

  - 型の一致しない[関数呼び出し](../Page/サブルーチン.md "wikilink")
  - 初期化されていない[変数の参照がある](../Page/変数_\(プログラミング\).md "wikilink")
  - 宣言されているが使われていない変数がある
  - 同じ関数を参照しているが、戻り値を使う場合と使わない場合がある
  - 関数が戻り値を返す場合と返さない場合がある

など、コンパイラではチェックされないが、[バグ](../Page/バグ.md "wikilink")の原因になるような曖昧な記述についても警告される。[構文](../Page/構文解析.md "wikilink")（シンタックス）レベルのチェックだけでなく、[意味](../Page/プログラム意味論.md "wikilink")（セマンティクス）レベルのチェックまで実行するものもある。

## lintで警告が出る例

``` c
int foo(int count) {
    int sum = 0;
    int i;
    for (i = 1; i <= count; ++i) {
        sum += i;
    }
    if (sum >= 100) {
        return sum;
    }
}
```

上記の例の場合、`foo()` は、`sum` が100以上であれば値を返すが、それ以外の時には値を返さない。これはC言語の構文的には合法だが、実行時エラーなどの未定義動作を引き起こす。そのため、lint では警告が出る。

ただ、のコンパイラは、細かな警告やエラーを出す機能が強化されているため、以前は lint を使わなければ検出できなかった類のミスも、コンパイル段階で検出できるようになっているものがある。上記の例は、[Microsoft Visual C++では既定で](../Page/Microsoft_Visual_C++.md "wikilink") C4715 の警告が生成され、コンパイルオプション`/we"4715"`を指定することでコンパイルエラーになる。[GCCや](../Page/GNUコンパイラコレクション.md "wikilink")[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")ではコンパイルオプション`-Wreturn-type`を指定することで警告が生成され、また`-Werror=return-type`を指定することでコンパイルエラーになる。

後発のプログラミング言語では安全性を考慮して、上記のようなコードを常に非合法とし、必ずコンパイルエラーにしてしまう仕様となっているもののほうが多い。C言語では仕様により動作が厳密に規定されていない事項が非常に多く、そのためコンパイラやlintによる警告に頼らなければならないことが多い。

## 「lint」の派生用法

転じて、コードをチェック・解析することを**lint**\[1\]、lintを行うプログラムを**linter**と呼ぶ\[2\]。linterの例には[HTMLの文法チェックを行う](../Page/HyperText_Markup_Language.md "wikilink")[Another HTML-lint](../Page/Another_HTML-lint.md "wikilink") がある。[Android Studioでは](https://ja.wikipedia.org/wiki/Android_Studio "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")および[Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")で書かれたコードに対してlint（静的解析）が利用可能である\[3\]。

コンパイラが存在する言語の場合、[静的コード解析](../Page/静的コード解析.md "wikilink")に[コンパイラ](../Page/コンパイラ.md "wikilink")とlinterを併用することで、字句/構文チェックと意味論的チェックを実現できる。リアルタイムに動作するlinterを利用すれば、コーディングしながら常時lintingを行える。例えばVSCode上でTypeScriptコードを書く場合、字句/構文チェックを担う`tsserver`\[4\]とlintingを担う`ESLint`を用いてコーディング中に常時静的コード解析が走る状態を実現できる。

lintingをおこなっても即座にバグが発見されるわけではない（lintエラー≠コンパイルエラー）。lintingの主たる目的は低品質コードの検出による**バグの予防**である。linterは「エラーをしばしば引き起こすパターン\[5\]」あるいは「エラーを避けるベストプラクティスパターン\[6\]」を用いて[品質](../Page/品質.md "wikilink")の低いコードを検出する。検出された低品質コードを改善することにより、バグが埋め込まれる可能性を低減しバグを予防できる。

## 脚注

## 関連項目

  - [Portable C Compiler](../Page/Portable_C_Compiler.md "wikilink")
  - [Another HTML-lint](../Page/Another_HTML-lint.md "wikilink")
  - [静的コード解析](../Page/静的コード解析.md "wikilink")

## 外部リンク

  - [ - Unix & Linux Commands](http://www.unix.com/man-page/FreeBSD/1/lint)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink")

1.  "lint/linting"の用例: [**Linting** Python in Visual Studio Code - VSCode](https://code.visualstudio.com/docs/python/linting)
2.  "linter"の用例: [ESLint - Pluggable JavaScript **linter**](https://eslint.org/)
3.  [lint/libs/lint-checks/src/main/java/com/android/tools/lint/checks - platform/tools/base - Git at Google](https://android.googlesource.com/platform/tools/base/+/studio-master-dev/lint/libs/lint-checks/src/main/java/com/android/tools/lint/checks?autodive=0/)
4.  likeなプロトコルでリアルタイム動作するTypeScriptコンパイラ/Language server。VSCode組み込み。
5.  Possible Errors: These rules relate to possible syntax or logic errors [Rules - ESLint](https://eslint.org/docs/rules/)
6.  Best Practices: These rules relate to better ways of doing things to help you avoid problems [Rules - ESLint](https://eslint.org/docs/rules/)