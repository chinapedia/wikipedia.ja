> この記事は[Ark Linux](https://ja.wikipedia.org/wiki/Ark_Linux)から翻訳されています。


**Ark Linux**は、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つ。デスクトップ環境には[KDE](../Page/KDE.md "wikilink")を採用している。 発音の問題で、よく[Arch Linuxと混同される](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")。

**Ark Linux**は[インストール](../Page/インストール.md "wikilink")可能な[OS](../Page/オペレーティングシステム.md "wikilink")、または[Live CDとして利用可能である](../Page/Live_CD.md "wikilink")。 [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のプロジェクトであり、ボランティアによって管理されている。

## 思想

Ark Linuxの基本的な目標は以下のとおりである。 \* 簡単にインストールして使えるようになること\[1\]。 \* デスクトップ環境に一般的に必要とされるツールとアプリケーションを含むこと\[2\] \* 一般的に必要とされるツール・アプリケーション“のみ”を含むこと\[3\] \* できる限り簡単かつ高速にソフトウェアを追加できるようにすること\[4\]。 \* 技術的にまともな開発環境であること\[5\]。 \* 100パーセントの[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であること\[6\]。

## 内容

Ark Linuxのコアシステムは、オフィススイート、インターネット接続ツール、インスタントメッセンジャーなど典型的なデスクトップ環境に必要とされる各種ソフトウェアを含み、1枚のCDにまとめられている\[7\]。 サーバシステム等はコアシステムには含まれていない。 コアシステムに含まれていないアプリケーションは[APT](https://ja.wikipedia.org/wiki/APT "wikilink")を用いるか、アドオンCDで手に入れることが出来る。 また、サポートされていないソフトウェア（[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")の3Dドライバや[Adobe Flashなどオープンでない](../Page/Adobe_Flash.md "wikilink")[フリーウェア](../Page/フリーウェア.md "wikilink")も含まれる）は、別のオンラインリポジトリから入手できる。

## パッケージの管理

Ark Linuxはパッケージの管理に[APT](https://ja.wikipedia.org/wiki/APT "wikilink")と[RPM](https://ja.wikipedia.org/wiki/RPM_Package_Manager "wikilink")、フロントエンドに[Kynaptic](https://ja.wikipedia.org/wiki/Kynaptic "wikilink")（[KDE](../Page/KDE.md "wikilink")に移植された[Synaptic Package Manager](https://ja.wikipedia.org/wiki/Synaptic_Package_Manager "wikilink")）を用いている\[8\]。

各リリースに加え、Ark Linuxには4つのパッケージツリーがある。

  - Dockyard: コアシステムに属する、テストされたパッケージ。
  - Dockyard contrib: ライセンスの制限等によってコアシステムに属さない、テストされたパッケージ。
  - Dockyard-devel: 開発ツリー（コアシステム）。うまく動作しない場合のあるソフトウェアが含まれている。
  - Dockyard-devel contrib: 開発ツリー（コアシステムに属さない）。

一般的なインストールでは、アップデート・追加パッケージはDockyard、Dockyard contribツリーから取得される。

Ark Linuxパッケージを作成する開発者のために、主にv\* toolchain（全てのツールの名称がvで始まるわけではないが）として知られる数多くのツールが含まれている。それらを用いることによってRPMソースパッケージに対するパッチやスペックファイルの生成を行うことが出来る\[9\]。

## リリース

全てのリリースはテストされたDockyardツリーのスナップショットである。標準インストールでは Dockyard・Dockyard contribツリーからアップデートがなされる。

新しいリリースがなされたとき、ユーザーは再インストールする必要は無い。Dockyardツリーがアップデートされるので、[apt-get](https://ja.wikipedia.org/wiki/APT "wikilink") dist-upgrade を実行することによってユーザーは自動的に新しいリリースを取得することが出来る。

これまでなされたリリースは以下のとおりである。

  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[3月19日](../Page/3月19日.md "wikilink") - Ark Linux 2005.1
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[3月31日](../Page/3月31日.md "wikilink") - Ark Linux 2005.1-SR1
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[12月10日](../Page/12月10日.md "wikilink") - Ark Linux 2005.2
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[8月2日](../Page/8月2日.md "wikilink") - Ark Linux 2006.1, Ark Linux Live 2006.1
  - [2007年](../Page/2007年.md "wikilink")[8月17日](../Page/8月17日.md "wikilink") - Ark Linux 2007.1, Ark Linux Live 2007.1

しかし、よく Dockyard では以前のリリースよりも一層アップデートされている ISO ファイルが利用可能になる。例えば、Ark Linux 2007.1 ではいくつかのハードウェアサポートに問題があった（例えばAHCI SATAを認識しないことなどを含む）。この機能を含む[ホットフィックス](https://ja.wikipedia.org/wiki/ホットフィックス "wikilink")の ISO ファイルがリリースされたが、他のエラーはまだ修正されていないためバージョン番号は変化していない。すなわち、現在推奨されているインストール ISO (Dockyard) は最新版の公式リリースではない。

## 脚注

<references />

## 関連項目

  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")

## 外部リンク

  - [Ark Linux 公式ウェブサイト](http://www.arklinux.org/)（英語）

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.