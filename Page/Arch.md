> この記事は[Arch](https://ja.wikipedia.org/wiki/Arch)から翻訳されています。


**arch**（アーク）は、分散型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")である。ただし、archと書いた場合には、特定の[コマンドを指すものではなく](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")、archのプロトコルに沿ったリポジトリ（[アーカイブ](../Page/アーカイブ.md "wikilink")）操作を行えるツールの総称として扱われている。設計および主な実装はTom Lordが行った。

## archの種類

現在使われている主なarchの実装としては、

  - larch （[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")による実装）
  - GNU arch(tla) larchを[C言語](../Page/C言語.md "wikilink")で再実装したもの、現在の主流となっている

などがある。

## archの動作

archは[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversionと同様にバージョンを管理する場所](../Page/Apache_Subversion.md "wikilink")（リポジトリ）を持ち、それをアーカイブと呼ぶが、CVSやSubversionと異なり、集中させる必要がない。必要であれば、他人のアーカイブを分岐させた[ローカル](../Page/ローカル.md "wikilink")のアーカイブを作成し、開発に利用することができる。後になって、分岐したアーカイブでの成果を取り込む（[マージ](../Page/マージ.md "wikilink")）必要があれば、それを行うための補助機能が用意されている。

## archでの主な操作

GNU arch（tlaコマンド）での操作例を以下にあげる。

### アーカイブの作成

`$ tla make-archive foo@bar.net--2004 /home/foo/{archives}/2004`

これにより、アーカイブfoo@bar.net--2004が作成され、データの実体が/home/foo/{archives}/2004に配置される。例はローカルファイルであるが、それ以外に[WebDAV](../Page/WebDAV.md "wikilink")や[SSH](../Page/Secure_Shell.md "wikilink") ([SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink"))、[FTP越しに置くことも可能となっている](../Page/File_Transfer_Protocol.md "wikilink")。

### アーカイブに置かれたデータの参照

`$ tla categories -A foo@bar.net--2004`
`$ tla branches -A foo@bar.net--2004 libA`
`$ tla versions -A foo@bar.net--2004 libA--main`
`$ tla revisions -A foo@bar.net--2004 libA--main--X.Y.Z`

データにはカテゴリ名、[ブランチ](https://ja.wikipedia.org/wiki/ブランチ "wikilink")名、バージョン名、[リビジョン](https://ja.wikipedia.org/wiki/リビジョン "wikilink")名の4つが通常要求されるため、それぞれを確認するためのコマンドが用意されている。

### アーカイブからデータを取得する

libA--mainブランチの最新版を取得

`$ tla get -A foo@bar.net--2004 libA--main`

libA--main--X.Y.Zの最新リビジョンを取得

`$ tla get -A foo@bar.net--2004 libA--main--X.Y.Z`

libA--main--X.Y.Z--patch-nリビジョンを取得

`$ tla get -A foo@bar.net--2004 libA--main--X.Y.Z--patch-n`

### 編集したアーカイブを登録する

ログを作成

`$ tla make-log`

登録

`$ tla commit`

### ローカルコピーを最新版に更新する

ローカルの修正を考慮して試みる

`$ tla update`

ローカルの修正を無視して更新

`$ tla replay`

### 変更記録 (ChangeLog) を作成

`$ tla changelog`

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")