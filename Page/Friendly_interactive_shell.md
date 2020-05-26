> この記事は[Friendly interactive shell](https://ja.wikipedia.org/wiki/Friendly_interactive_shell)から翻訳されています。


**fish**（**f**riendly **i**nteractive **sh**ell）とは[UNIX](../Page/UNIX.md "wikilink")における[シェル](../Page/シェル.md "wikilink")の一つである。

## 概要

fishは対話的利用・判り易さ・ユーザフレンドリさに重きを置いている。fishの最終目標は、簡単に発見でき、覚えられ、利用できるようなかたちで強力な機能を提供することである。fishの提供するタブ補完機能はユーザフレンドリかつ強力であり、全ての補完に対する簡易な説明や、[ワイルドカードを含む文字列での補完や](../Page/ワイルドカード_\(情報処理\).md "wikilink")、たくさんのコマンドについて固有の補完を含む。また、fishは拡張可能かつ判り易いヘルプを備えている。特別なヘルプコマンドでは、ユーザの設定した[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")にて全てのfishドキュメントにアクセスが可能である。

## 文法

fishの文法は他のシェルスクリプト言語と少し異なる。これらの変更は言語を容易に学習できるように、そして言語を強力にしている。fishと[Bash](../Page/Bash.md "wikilink")に代表する他のシェルスクリプト言語との明確な違いは、変数はトークンを必要としない。これはすなわち、引用符を用いて文字列を囲むということを滅多にしないのである。

``` fishshell
 # 変数代入: 変数fooに対しbarという値をセットする。
 # ここで=演算子を使ってはならない。これは空白文字によって判別される。
 # 加えてsetコマンドは配列やスコープなどと拡張して使うことが出来る。
 > set foo bar
 > echo $foo
 bar

 # コマンド代入: 変数wdに対してpwdコマンドの出力を代入する。
 # ここで `` を使ってはならない。これはネストが出来ない上、'' と非常に紛らわしいからである。
 # それから$()も使ってはならない。fishに於いて$は変数を展開するときのみ利用される。
 > set wd (pwd)
 > echo $wd
 ~

 # 配列変数: 変数Aに対して、3, 5, 7, 9, 12という値を配列として代入する。
 > set A 3 5 7 9 12
 > echo $A[(seq 3)]
 3 5 7
 # 配列分割: 変数Bは、変数Aの1つ目と2つ目の値である。
 > set B $A[1 2]
 > echo $b
 3 5
 # 変数Aの3つ目と5つ目の要素を削除する。
 > set -e A[$B]; echo $A
 3 5 9

 # forループ: JPEGからPNGへ変換する。
 > for i in *.jpg; convert $i (basename $i .jpeg).png; end

 # whileループ: /etc/passwdを読み込み、コロンで区切られた5番目のフィールドを出力する。
 # これはユーザの説明のフィールドである。
 > cat /etc/passwd|while read line; set arr (echo $line|tr : \n); echo $arr[5]; end
```

fishと他のシェルスクリプト言語との重要な違いの一つに、サブシェルの有無がある。他の言語に於いてパイプラインや関数、ループのような沢山のタスクはサブシェルを呼ぶことで実装している。サブシェルは親プログラムのために1-2個のコマンドを実行し終了する、シンプルな子プログラムである。しかしこの変更は、サブシェルの如何なる変化もメインシェルへ与えない。これはすなわち、変数の代入や多くのビルトイン関数が期待通りに動作しないのである。fishはサブシェルを決して呼ばず、それゆえ多くのビルトイン関数が完全に動作するのである。

``` fishshell
 # これは多くの他のシェルでは動作しない。
 # これはreadコマンドがビルトイン関数だからである。
 # サブシェルをforkしないため、fishとzshで期待通り動く。
 > cat *.txt | read line
```

## 親切なヘルプメッセージ

fishに於ける[エラーメッセージ](../Page/エラーメッセージ.md "wikilink")は、何が間違っていたのか、どうすればいいのかを実際にユーザへ伝えるように設計されている。

`> foo=bar`
`fish: foo=bar というコマンドはありません。もしかしたら“set 変数 値”と`
`いう意味ですか？　変数値を設定する情報を見るためには、“help set”と入力`
`し、ヘルプセクションを見て下さい。`

`> echo ${foo}bar`
`fish: {$変数名}という意味ですか？　文字$は変数の初めに用います。$に続く`
`ブラケットは変数名の一部としては許可されておらず、変数名が0文字になって`
`しまいます。fishに於ける変数展開についての情報は“help expand-variable”`
`を入力して下さい。`

`> echo $(pwd)`
`fish: (コマンド)という意味ですか？　fishに於いて文字$は変数値を利用する`
`ときのみ利用します。fishに於けるコマンド代用に関する情報は、“help`
`expand-command-substitution”を見て下さい。`

## ユニバーサル変数

fishは、ユーザが複数のfishシェルに対して横断的で永久に変数値を設定できる、*ユニバーサル変数*として知られる機能を持っている。この変数はログアウトか再起動するまで有効で、反映は全ての動作しているシェルに対して即座に行われる。

`# デフォルトのテキストエディタをemacsに設定する。`
`# -Uオプションによってユニバーサル変数として扱う。`
`> set -U EDITOR emacs`

`# このコマンドは、全てのfishシェルに対してプロンプトを青色に設定するもの`
`# である。`
`> set -U fish_color_cwd blue`

## 他の機能

  - 拡張[タブ補完](https://ja.wikipedia.org/wiki/タブ補完 "wikilink")（*Advanced tab completion*）
  - 拡張エラーチェックと[シンタックスハイライト](../Page/シンタックスハイライト.md "wikilink")（*Syntax highlighting with extensive error checking*）
  - [X](../Page/X_Window_System.md "wikilink")[クリップボード](../Page/クリップボード.md "wikilink")のサポート（*Support for X clipboard*）
  - terminfoに基づく[ターミナル](../Page/ターミナル.md "wikilink")ハンドリング（*Smart terminal handling based on terminfo*）
  - 検索可能なコマンド履歴（*Searchable command history*）

## 脚注

## 外部リンク

  -
  -
[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")