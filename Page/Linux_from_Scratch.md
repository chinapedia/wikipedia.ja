> この記事は[Linux from Scratch](https://ja.wikipedia.org/wiki/Linux_from_Scratch)から翻訳されています。


**Linux From Scratch** (リナックス フロム スクラッチ、LFS) は、ユーザが自分自身で「スクラッチから（from Scratch）」[Linuxシステムをビルドする](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")、という一風変わった特徴を主旨とする、（一種の）[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。最初のインストール（クリーンインストール）に、[Live CDのようなライブイメージとバイナリパッケージを使って](https://ja.wikipedia.org/wiki/Live_CD "wikilink")、最低限の機能が備わったシステムを一気に用意してしまう一般的なディストリビューションとは異なり、全てを[ソースコード](../Page/ソースコード.md "wikilink")で入手して、一種のクロスビルドによってシステムを準備してゆく。

具体的にもう少し詳細には以下のようである。

まず、現在動作しているLinuxシステムを用意する。その中に、[クロスコンパイルの準備の要領で](https://ja.wikipedia.org/wiki/クロスコンパイラ "wikilink")ビルド環境を用意し、カーネルやカーネルモジュール等をはじめ、いわゆるベースシステム等と呼ばれる[システムソフトウェア](https://ja.wikipedia.org/wiki/システムソフトウェア "wikilink")類をビルドする。

次に、インストール対象となるマシンのためのディスク（ないしディスクイメージ）にパーティションを作り、extファイルシステムなどで論理フォーマットし、/usr など、基本的なインストールに必要なディレクトリツリーを構築してインストールし、/etc の中の設定ファイルなどを編集する。また、/boot など、ブートに必要な設定も行う。その他にも多くの作業があるが、全てを行えば、最低限の起動可能なシステムができあがる。

基本的な構築が完了した後は、Beyond Linux From Scratch (BLFS) に従って、応用的なライブラリや[X Window Systemを使用するような](../Page/X_Window_System.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")などを導入することができる。

LFSのサイトで最新の安定版及び開発版を入手することができる。

## LFSソフトウェア一覧

LFS 7.8 に含まれたソフトウェアのリスト

## 注釈

## 外部リンク

  - [Linux From Scratch](http://www.linuxfromscratch.org/) プロジェクトサイト

<!-- end list -->

  - [LFSブック日本語版 (lfsbookja)](http://lfsbookja.osdn.jp/) OSDN LFSブックの日本語訳

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")