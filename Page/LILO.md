> この記事は[LILO](https://ja.wikipedia.org/wiki/LILO)から翻訳されています。


**LILO**（リロ、ライロウ）は[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")に使われる[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")である。LInux LOaderからこの名が取られている。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")標準の[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")として昔から使用されている。[Windowsなど別の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")もブートできる。ブートイメージの保存場所をディレクトリ構造ではなくセクタ位置（[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")上の物理的な位置）として認識する。

そのため[カーネル](../Page/カーネル.md "wikilink")を再構築するなどしてブートイメージを作り直した場合やLILOの設定ファイル**lilo.conf**を変更した場合は、LILOへそれを報告しなければならない。そのための[コマンドが](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")**/sbin/lilo**コマンドである。このコマンドによってブートイメージの新しいセクタやlilo.confの内容がLILOへ報告される。このコマンドを実行し忘れるとブートイメージを読み込めなくなって起動に失敗したり、lilo.confの内容が全く反映されなかったりといったことが起こる。

LILOは[2000年](../Page/2000年.md "wikilink")以後主流の[GRUBと違い](../Page/GNU_GRUB.md "wikilink")[シェル](../Page/シェル.md "wikilink")を持っていない。

現LILO開発者は、2015年12月をもって開発を終了し、その後は後継者を募集している。

## 脚注

<references />

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink")