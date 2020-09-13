> この記事は[APT](https://ja.wikipedia.org/wiki/APT)から翻訳されています。


**APT** (\[1\]、あるいは \[2\]\[3\]ともいう) とは、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[インストール](../Page/インストール.md "wikilink")と[アンインストール](../Page/アンインストール.md "wikilink")（削除）を自動的に行ない、ソフトウェアの管理を簡単に行えるようにするための仕組みの1つ。

## 概要

もともと [Debian](../Page/Debian.md "wikilink")用に開発された[コマンドラインベースの](../Page/コマンドラインインタプリタ.md "wikilink")[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")である。現在では多数の Debian系の [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で採用されている。[dpkg](https://ja.wikipedia.org/wiki/dpkg "wikilink")のフロントエンドとして作動するように設計されたが、現在は[RPMに対応するように移植された](../Page/RPM_Package_Manager.md "wikilink") apt-rpmもある。[コンパイル済みのソフトウェアを管理する機能に加え](../Page/コンパイラ.md "wikilink")、[ソースコード](../Page/ソースコード.md "wikilink")からソフトウェアをコンパイルする際の依存関係を解決する機能も備えている。

## フロントエンド

APT には複数のフロントエンドが用意されている。コマンドライン（CUI）で作動するフロントエンドとして apt や apt-get、[aptitude](https://ja.wikipedia.org/wiki/aptitude "wikilink") がある\[4\]。またDebian系やRPM系ともに、[Synaptic](../Page/Synaptic.md "wikilink")\[5\] というグラフィカルな（[GUI）](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[フロントエンド](../Page/フロントエンド.md "wikilink")がある。

## 機能

APTでは、コンパイル済みパッケージ（バイナリパッケージと呼ぶ）同士の関係を主に下の4つにわけて管理する。これらの関係を用いて、目的のパッケージをインストールするために必要なパッケージもしくは削除する必要があるパッケージを自動計算する。

  - 依存 : パッケージを導入するのに欠かすことのできないパッケージ。
    推奨 : 無くてもよいが、プログラムの機能を利用するために通常は導入するパッケージ。
    提案 : 無くてもよいが、導入することによってプログラムの機能を向上させるパッケージ。
    衝突 : パッケージを導入することで、同一の機能を有するなどの理由で削除されるパッケージ。

代表的なコマンドは次のとおり。

### 追加・ダウンロード

  - 新しいソフトウェアのインストール（root権限が必要）

    ``` bash
    apt install パッケージ名 [ Enter ]
    ```

  - ソースパッケージのダウンロード

    ``` bash
    apt source パッケージ名 [ Enter ]
    ```

  - ソースパッケージをコンパイルする為に必要なパッケージのインストール（root権限が必要）

    ``` bash
    apt build-dep パッケージ名 [ Enter ]
    ```

### 更新（アップデート）

  - リポジトリの更新（root権限が必要）

    ``` bash
    apt update [ Enter ]
    ```

  - インストール済みのソフトウェアの更新（root権限が必要）

    ``` bash
    apt upgrade [ Enter ]
    ```

  - ディストリビューションのアップグレード（root権限が必要）

    ``` bash
    apt full-upgrade [ Enter ]
    ```

（ただし、apt dist-upgrade コマンドも agt-get からの移行用としてサポートされている。)

またこれら*apt*コマンドを使用すると、システムに必要なパッケージが存在しない場合、その不足している依存性パッケージを自動的に判別し、そのパッケージも同時にインストールしてくれる。*dist-upgrade*を指定した場合、更新可能なすべてのパッケージに対して依存関係を解析し、重要なアップデートを更新するが、依存関係の問題から重要でないパッケージは削除される場合もある。

### 検索・情報表示

  - パッケージの検索

    ``` bash
    apt search 検索キーワード [ Enter ]
    ```

  - 特定パッケージの情報表示

    ``` bash
    apt show パッケージ名 [ Enter ]
    ```

### 削除

  - 特定パッケージの削除（root権限が必要）

    ``` bash
    apt remove パッケージ名 [ Enter ]
    ```

  - 特定パッケージの設定ファイルを含めた削除（root権限が必要）

    ``` bash
    apt purge パッケージ名 [ Enter ]
    ```

  - 不要なパッケージの自動削除(依存されていないライブラリ等)（root権限が必要）

    ``` bash
    apt autoremove [ Enter ]
    ```

Debian系もRPM系も設定ファイル（大抵は/etc/apt/sources.list）を書き換えることでダウンロード先の変更・パッケージリストの指定変更が可能である。Debian GNU/LinuxやVine Linuxをはじめ、この設定の変更でディストリビューションのバージョンアップを行うことができるディストリビューションも存在する。

またSynapticと同様に、パッケージのリポジトリを変更しやすくするためのGUI[フロントエンド](../Page/フロントエンド.md "wikilink")も存在する。

### 新旧コマンド対応の概要

以下におもなコマンドの新旧対応一覧を参考として示す\[6\]\[7\]。関連項目の [Aptitude](../Page/Aptitude.md "wikilink") も参照のこと。

`apt-get update             ->  apt update           ->  aptitude update`

`apt-get upgrade            ->  apt upgrade          ->  aptitude safe-upgrade`

`apt-get dist-upgrade       ->  apt full-upgrade     ->  aptitude full-upgrade`

`apt-get install package    ->  apt install package  ->  aptitude install package`

`apt-get remove package     ->  apt remove package   ->  aptitude remove package`

`apt-get autoremove         ->  apt autoremove       ->  N/A `

`apt-cache search package   ->  apt search package   ->  aptitude search package`

`apt-cache policy package   ->  apt list -a package  ->  aptitude list -a package`

`apt-cache show package     ->  apt show package     ->  show package`

`apt-cache search `<regex>`   ->  apt search `<regex>`   ->  aptitude search `<regex>

## イースターエッグ

apt や apt-get には隠し機能があり、[aptitudeの隠し機能と対になっている](https://ja.wikipedia.org/wiki/aptitude#イースターエッグ "wikilink")。(""は[円記号](../Page/円記号.md "wikilink")ではなく[バックスラッシュ](../Page/バックスラッシュ.md "wikilink")である)

`$ apt moo`
`         (__) `
`         (oo) `
`   /------``/ `
`  / |    ||   `
` *  /``---/`
`    ~~   ~~   `
`...."Have you mooed today?"...`

## 脚注

## 関連項目

  - [dpkg](https://ja.wikipedia.org/wiki/dpkg "wikilink")
  - [apt-rpm（英語版）](https://ja.wikipedia.org/wiki/:en:apt-rpm "wikilink")
  - [Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")
  - [RPM](../Page/RPM_Package_Manager.md "wikilink")

## 外部リンク

  -
[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink") [Category:Debian](https://ja.wikipedia.org/wiki/Category:Debian "wikilink")

1.
2.
3.
4.
5.
6.
7.