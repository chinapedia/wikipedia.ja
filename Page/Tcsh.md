> この記事は[Tcsh](https://ja.wikipedia.org/wiki/Tcsh)から翻訳されています。


**tcsh**（ティーシーシェル）は、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で使われる[コマンドシェルの一つ](../Page/シェル.md "wikilink")。

[C言語](../Page/C言語.md "wikilink")に似た文法特性を持つ[csh](../Page/C_Shell.md "wikilink")（シーシェル）の[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")の部分を中心に拡張されたシェルでcshとの[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")を持つ、ヒストリ編集などの機能に優れ、簡単な[C言語](../Page/C言語.md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")の文法チェックに使われることもある。Unix系OSで用いられる他のシェルに比べて、NLS (Native Language System) などの国際化対応にいち早く対応したことで知られる。

なお、tcshの頭文字のTは、[TENEXならびに](https://ja.wikipedia.org/wiki/TOPS-20#TENEX "wikilink")[TOPS-20](../Page/TOPS-20.md "wikilink")に由来するという\[1\]。

## 環境

[FreeBSD](../Page/FreeBSD.md "wikilink") 4.1-RELEASE以降には標準シェルとして組み込まれている。

FreeBSDの流れを汲む[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")でもOSに組み込まれている (/bin/tcsh)。[Mac OS X v10.2まではtcshがデフォルトのシェルであったが](../Page/Mac_OS_X_v10.2.md "wikilink")、[v10.3からは](../Page/Mac_OS_X_v10.3.md "wikilink")[Linux](../Page/Linux.md "wikilink")の標準シェルである[Bash](../Page/Bash.md "wikilink")がデフォルトのシェルとなっている。

## Native Language System

tcshの6.06以降では、NLS (Native Language System) カタログに対応している\[2\]。これは、各種メッセージの各国語化をプログラム修正なしで行うというものである。但し、日本語化においては6.07.11まではパッチが必要であった。6.07.11においてパッチが本体に取り込まれ、それ以降は日本語のカタログファイルを用いる場合でもパッチ不要でメッセージを表示することができるようになった。

なお、日本語化パッチ提供者は当時、[サンソフト](https://ja.wikipedia.org/wiki/サンソフト "wikilink")の格闘ゲーム『[ギャラクシーファイト ユニバーサル・ウォーリアーズ](../Page/ギャラクシーファイト_ユニバーサル・ウォーリアーズ.md "wikilink")』の登場キャラクターであるルーミに[萌え](../Page/萌え.md "wikilink")ており、ルーミの口調を真似たカタログファイルを正しく扱えるようにする目的でパッチを作成したという\[3\]。このカタログファイルをはじめ、[マルチや](https://ja.wikipedia.org/wiki/To_Heart#メイドロボ "wikilink")[ホシノ・ルリなど](https://ja.wikipedia.org/wiki/機動戦艦ナデシコの登場人物#ナデシコ搭乗員 "wikilink")、いくつかの萌系キャラクター口調のカタログファイルは過去に FreeBSD [portsコレクションに含まれていたことがあった](https://ja.wikipedia.org/wiki/FreeBSD#ports "wikilink")\[4\]。他にも、メッセージが関西弁や土佐弁などで示される方言シリーズなど、多彩なカタログファイルが作成されている。

## 脚注

## 外部リンク

  - [公式サイト](http://www.tcsh.org/Home)
  - Manpage
      - [FreeBSD 日本語マニュアル](http://www.jp.freebsd.org/cgi/mroff.cgi?subdir=man&lc=1&cmd=&man=tcsh&dir=jpman-5.4.0%2Fman&sect=0)

      -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")

1.   - manページの「tcsh の T の由来」節に記載。
2.  配布ファイルのNewThings（更新履歴に相当）に記載。
3.   - パッチ提供者によるオリジナルカタログ配布ページ
4.   - ルーミ口調のカタログファイル ja.roomi.cat のports