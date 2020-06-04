> この記事は[Rc \(シェル\)](https://ja.wikipedia.org/wiki/Rc_\(シェル\))から翻訳されています。


[Plan_9_from_Bell_Labs_(process_management).png](https://ja.wikipedia.org/wiki/File:Plan_9_from_Bell_Labs_\(process_management\).png "fig:Plan_9_from_Bell_Labs_(process_management).png") **rc**（"run commands"）は、[Version 10 Unixと](../Page/Research_Unix.md "wikilink")[Plan 9のための](../Page/Plan_9_from_Bell_Labs.md "wikilink")[コマンドラインインターフェースである](../Page/キャラクタユーザインタフェース.md "wikilink")。rcは[Bourne shellに似ているが](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink")、その構文はより簡潔なものになっている。また、rcはトム・ダフによって作られた。彼は[Duff's deviceと呼ばれる](../Page/Duff's_device.md "wikilink")[C言語](../Page/C言語.md "wikilink")の構築で有名である\[1\]。

オリジナルなrcの[UNIX](../Page/UNIX.md "wikilink")に対するポートは、[Plan 9 form User Spaceの一部としてなされた](https://ja.wikipedia.org/wiki/Plan_9_form_User_Space "wikilink")。rcの[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")OSへのリライトはバイロン・ラキツィスによるものも利用可能だが、それはいくつかの互換性のない変更を含んでいる。

rcは、オリジナルのBourne shellが[ALGOL](../Page/ALGOL.md "wikilink")風の構造を持つのに対して、C言語のような構造を持つ。ただし、"`if not`"構造を"`else`"の代わりに使い、リストの繰り返しにBourne shell風の"`for`"ループを持っている。rcにおいては"`$@`"のような構造を排除する必要のために、すべての変数は文のリストとなっている。変数は展開されるときに再分割されない。この言語はダフの論文に記載されている\[2\]。

## 影響

### es

es（"extensible shell"）は、ラキツィスとポール・ハウァーによって開発\[3\]された、[オープンソース](../Page/オープンソース.md "wikilink")のコマンドラインインターフェースで、rcシェルに影響を受けた[スクリプト言語](../Page/スクリプト言語.md "wikilink")の構文を利用している\[4\]\[5\]。esは、ラツキィスによるUNIXのためのrcのクローン のコードをオリジナルのベースにしている\[6\]\[7\]。

es（＝"extensible shell"）は、[UNIXシェル](https://ja.wikipedia.org/wiki/UNIXシェル "wikilink")として、完全な[関数型プログラミング言語](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")を提供することを意図している\[8\]。esの大部分の開発は1990年代の初頭に始まり、1993年冬の[サンディエゴ](../Page/サンディエゴ.md "wikilink")における[USENIX](../Page/USENIX.md "wikilink")の会議において紹介された後\[9\]、公式の リリースは1997年の0.9-beta-1以後やめられた\[10\]。また、esは、[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")や[bash](https://ja.wikipedia.org/wiki/bash "wikilink")などのポピュラーなシェルに比べて機能が欠けている\[11\]。の[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")な派生版は2019年現在でも開発されている\[12\]。

## 例

Bourne shellスクリプト

``` bash
if [ "$1" = "hello" ]; then
    echo hello, world
else
    case "$2" in
    1) echo $# 'hey' "jude's"$3;;
    2) echo `date` :$*: :"$@":;;
    *) echo why not 1>&2
    esac
    for i in a b c; do
        echo $i
    done
fi
```

はrcでは以下のように表記される。

``` text
if(~ $1 hello)
    echo hello, world
if not {
    switch($2) {
    case 1
        echo $#* 'hey' 'jude''s'^$3
    case 2
        echo `{date} :$"*: :$*:
    case *
        echo why not >[1=2]
    }
    for(i in a b c)
        echo $i
}
```

Rcはまた、より動的なパイプをサポートしている。

`a |[2] b    `*`#``   ``aの`[`標準エラー出力`](https://ja.wikipedia.org/wiki/標準エラー出力 "wikilink")のみbへパイプする`   ``—``   `[`Bourne``   ``shellにおける`](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink")`'3>&2``   ``2>&1``   ``>&3``   ``|``   ``b'と等価である`*\[13\]
`a <>b       `*`#``   ``aの`[`標準入力`](https://ja.wikipedia.org/wiki/標準入力 "wikilink")および[`標準出力`](https://ja.wikipedia.org/wiki/標準出力 "wikilink")としてファイルbを開く*
`a <{b} <{c} `*`#``   ``a``   ``{bの標準出力}``   ``{cの標準出力}となる。"``"という名前でよく知られている`*\[14\]

## 出典

## 外部リンク

  - \- Plan 9のmanページ

  - [Plan 9 from User Space](https://9fans.github.io/plan9port/) - [Linux](../Page/Linux.md "wikilink")や[mac OSなどの](https://ja.wikipedia.org/wiki/mac_OS "wikilink")[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")システム向けのrcなどのPlan 9由来のツールを含む

  - [Byron Rakitzis' rewrite for Unix](http://tobold.org/article/rc)

  - [es Official website](http://hawkwind.utcs.utoronto.ca:8001/mlists/es.html)

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink") [Category:Inferno_(オペレーティングシステム)](https://ja.wikipedia.org/wiki/Category:Inferno_\(オペレーティングシステム\) "wikilink")

1.   ([PDF](https://www.scs.stanford.edu/nyu/04fa/sched/readings/rc.pdf); [1990 version](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.41.3287))
2.
3.
4.
5.
6.
7.
8.
9.  [Es: A shell with higher-order functions](http://stuff.mit.edu/afs/sipb/user/yandros/doc/es-usenix-winter93.html) by Byron Rakitzis, [NetApp Inc](https://ja.wikipedia.org/wiki/NetApp "wikilink"),, and Paul Haahr, [Adobe Systems Incorporated](https://ja.wikipedia.org/wiki/Adobe_Systems_Incorporated "wikilink"); <u>Archived</u> at [Archive.Org](https://web.archive.org/web/20090415213858/http://192.220.96.201/es/es-usenix-winter93.html).
10. [](ftp://ftp.sys.utoronto.ca/pub/es/)
11.
12.
13.
14.