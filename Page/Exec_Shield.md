> この記事は[Exec Shield](https://ja.wikipedia.org/wiki/Exec_Shield)から翻訳されています。


**Exec Shield** は[レッドハット](../Page/レッドハット.md "wikilink")が2002年後半に開始したプロジェクトであり、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")システムに対する[ワームなどの自動化された攻撃の危険性を低減することを目的としている](https://ja.wikipedia.org/wiki/ワーム_\(コンピュータ\) "wikilink")。最初の成果は、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")用[セキュリティ](../Page/コンピュータセキュリティ.md "wikilink")[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")であり、[NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")がハードウェアで実装されていない[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")でNXビットをエミュレートするものだった。Exec Shield には他にも多数のコンポーネントがあるが、この最初のパッチだけを Exec Shield と呼ぶ人もいる。

## 概要

この最初のExec Shieldパッチは、データ用メモリページを実行不可能とし、コード用メモリページを書き込み不能とする。これは[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")などの技法を使ってデータの中にコードを挿入するなどの試みを抑止する。Exec Shieldには他に [mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")() とヒープのベースアドレスの[ASLR](https://ja.wikipedia.org/wiki/ASLR "wikilink") (Address Space Layout Randomization) も行う。

このパッチは他に[シェルコード](https://ja.wikipedia.org/wiki/シェルコード "wikilink")の挿入と実行をより困難にする効果もある。Exec Shield を利用するにあたって、アプリケーションの再コンパイルは不要だが、一部のアプリケーション ([Mono](../Page/Mono_\(ソフトウェア\).md "wikilink"), [Wine](https://ja.wikipedia.org/wiki/Wine "wikilink"), [XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")) は動作が若干変わってしまう。

Exec Shieldプロジェクトから生まれた他の機能としては、いわゆるPosition Independent Executables (PIE) というLinuxカーネル用ASLRパッチ、[glibc](https://ja.wikipedia.org/wiki/glibc "wikilink")内部の広範囲なセキュリティチェック、GCC Fortify Source機能、GCCスタックプロテクタの移植とマージなどがある。

## 実装

Exec Shieldは、x86[CPU](../Page/CPU.md "wikilink")のコードセグメント境界を利用して動作する。そのため非常に軽量であるが、任意の[仮想記憶](../Page/仮想記憶.md "wikilink")配置を完全に保護するわけではない。[mprotect](https://ja.wikipedia.org/wiki/mprotect "wikilink")() で実行可能な範囲を広げると、その範囲内の保護は無効になる。Ingo Molnar は電子メールでの会話でこの点を指摘している。幸いにもほとんどのアプリケーションはその点で問題ない。特に重要な[スタック](../Page/スタック.md "wikilink")は、アプリケーションが明示的に指定しない限り実行可能にはならない。

[2004年](../Page/2004年.md "wikilink")8月現在、Exec Shieldプロジェクトの成果物は mprotect() を制限するわけではない。もっとも、初期状態で実行不可能なメモリであっても後から実行可能にすることはできるので、カーネルがアプリケーションに対してメモリページを同時に書き込み可能かつ実行可能にすることがある。しかし、[SELinuxと併用することで](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink") [Fedora Core](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink") ディストリビューションの標準ポリシーでは、互換性を理由とした一部の例外を除いて、ほとんどの実行ファイルのそのような動作を禁止している。

## 歴史

Exec Shield はレッドハットの様々な人々が開発に関わった。最初のパッチを2003年5月にリリースしたのはレッドハットの Ingo Molnar であった。これは [Fedora Core](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink") 1から6とRed Hat Enterprise Linux 3 (update 3) から4に採用された\[1\]\[2\]。他に関与した人々としては、Jakub Jelínek、Ulrich Drepper、Richard Henderson、Arjan van de Ven らがいる。

## 関連項目

  - [NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")
  - [PaX](../Page/PaX.md "wikilink")

## 脚注

## 外部リンク

  - [Ingo Molnar's Exec Shield patch web page](http://people.redhat.com/mingo/exec-shield/)
  - [Newsforge Feature Article](http://www.newsforge.com/os/03/05/02/1914223.shtml?tid=23)
  - [Red Hat Magazine Feature/Project Article](http://www.redhat.com/magazine/009jul05/features/execshield/)
  - [ExecShieldの問題点](http://lists.immunityinc.com/pipermail/dailydave/2007-May/004340.html)

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink")

1.
2.