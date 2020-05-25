> この記事は[Aptitude](https://ja.wikipedia.org/wiki/Aptitude)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Screenshot-aptitude-ja.png "wikilink") **aptitude**は、[Debian](../Page/Debian.md "wikilink")などが採用する[APT](../Page/APT.md "wikilink")システムにおける[CUI](../Page/キャラクタユーザインタフェース.md "wikilink")[フロントエンド](../Page/フロントエンド.md "wikilink")の一つ。[APT](../Page/APT.md "wikilink")システムにおける代表的なコマンドであるapt-getなどに比べて、より強力なパッケージ管理機能（高機能な検索、対話的なソフトウェアの追加・削除ができる）を有する。

また、引数をつけずに'aptitude'を起動すればフルスクリーンモードで起動できる。

`aptitude [ Enter ]`

aptitudeはapt-getと同じ感覚のコマンドラインコマンドとしても使用できる。

`aptitude update [ Enter ]`
`aptitude upgrade [ Enter ]`
`aptitude install `*`パッケージ名`*` [ Enter ]`

## イースターエッグ

aptitudeには隠し機能があり、[apt-getの隠し機能と対になっている](https://ja.wikipedia.org/wiki/APT#イースターエッグ "wikilink")（""は[バックスラッシュ](../Page/バックスラッシュ.md "wikilink")である）。

`$ aptitude -h`
`aptitude 0.4.11.11`
`使用方法: aptitude [-S ファイル名] [-u|-i]`
`   ~ ~ ~ ~`
`   ~ ~ ~ ~`
` -i             : 起動時にインストールを行います。`

`                  この aptitude にはスーパー牛さんパワーなどはありません。`
`$ aptitude moo`
`このプログラムにはイースターエッグ (隠し機能) はありません。`
`$ aptitude -v moo`
`このプログラムには本当にイースター・エッグはありませんよ。`
`$ aptitude -vv moo`
`このプログラムにイースターエッグはないって言わなかったかい?`
`$ aptitude -vvv moo`
`やめてくれ!`
`$ aptitude -vvvv moo`
`わかった、わかった。あんたにイースターエッグをあげればどっか行ってくれるかい?`
`$ aptitude -vvvvv moo`
`わかったよ。あんたの勝ちだ。`

`                               /----`
`                       -------/      `
`                      /               `
`                     /                |`
`   -----------------/                  --------`
`   ----------------------------------------------`
`$ aptitude -vvvvvv moo`
`これが何なのか? もちろんウワバミに食べられた象だよ。`

「[ウワバミに食べられた象](https://ja.wikipedia.org/wiki/うわばみ "wikilink")」というのは[星の王子さま](../Page/星の王子さま.md "wikilink")の一節に由来する。

## 外部リンク

  -
[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink") [Category:Debian](https://ja.wikipedia.org/wiki/Category:Debian "wikilink")