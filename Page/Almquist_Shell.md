> この記事は[Almquist Shell](https://ja.wikipedia.org/wiki/Almquist_Shell)から翻訳されています。


**Almquist Shell**（アルムクィスト シェル、**ash**）は、Kenneth Almquistが最初の版を[SVR4用に書いた](../Page/UNIX_System_V.md "wikilink")[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")である。現在は、高速かつ小型で、[POSIX](../Page/POSIX.md "wikilink")による`/bin/sh`への要求を満たす[Bourne Shellの代替として良く広まっている](../Page/Bourne_Shell.md "wikilink")。もともとは、Almquistが行エディタやコマンド履歴といった機能は[端末](../Page/端末.md "wikilink")[ドライバで実現すべきと考えていたため](../Page/デバイスドライバ.md "wikilink")、そういった入力機能を持っていなかったが、現在は[emacs](https://ja.wikipedia.org/wiki/emacs "wikilink")モードと[vi](https://ja.wikipedia.org/wiki/vi "wikilink")モードを持った入力機能を備えている。

[\*BSDをはじめ多くのシステムで](../Page/BSDの子孫.md "wikilink")`/bin/sh`として使われている。[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")では`/bin/sh`が[bash](https://ja.wikipedia.org/wiki/bash "wikilink")であることも多いが、[組み込みLinux](../Page/組み込みLinux.md "wikilink")では軽さのためashがよく使われている。また、[Debian](../Page/Debian.md "wikilink")ではashを元にした[Debian Almquist shell](https://ja.wikipedia.org/wiki/Debian_Almquist_shell "wikilink") (dash) が使われている。

ソースコードは、現状では共通で唯一のupstreamのようなものはなく、各プロジェクトでのフォーク版が各プロジェクトのリポジトリで管理されている。

[Slackware](../Page/Slackware.md "wikilink") の ash パッケージ情報には以下の記述がある（試訳）:

  -
    *ash (Kenneth Almquist's ash shell)*
      -
        軽量（92K）なBourne互換シェル。メモリが少ないマシンには最適だが、bash、[tcsh](https://ja.wikipedia.org/wiki/tcsh "wikilink")、[zsh](../Page/Z_Shell.md "wikilink") などが持つ拡張機能を持たない。ほとんどのシェルスクリプトを Bourne Shell 互換に実行する。ただし、Linux 上のスクリプトは bash 固有の文法を使っていることが多いようなので注意が必要。Slackware のセットアップスクリプトは例外であり、インストールディスク上では ash を使っている。NetBSD は ash を /bin/sh として使っている。

## 外部リンク

  - [Ash (Almquist Shell) Variants](http://www.in-ulm.de/~mascheck/various/ash/)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")