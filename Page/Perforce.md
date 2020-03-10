> この記事は[Perforce](https://ja.wikipedia.org/wiki/Perforce)から翻訳されています。


**Perforce** は、商用の[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")である。Christopher Seiwaldが[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に創設した Perforce Software, Inc. が開発した。

## 概要

Perforceは[クライアントサーバモデル](https://ja.wikipedia.org/wiki/クライアントサーバモデル "wikilink")に基づき、[サーバ](../Page/サーバ.md "wikilink")がソースファイル群のバージョンを1つ以上の*depots*で管理する。サーバは[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windowsといった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で動作する。

2019年5月現在、Perforce Softwareによれば15000以上の企業や組織\[1\]、40万人以上の開発者\[2\]がPerforceを使っており、顧客としては[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")や[セールスフォースが含まれる](https://ja.wikipedia.org/wiki/セールスフォース・ドットコム "wikilink")\[3\]。また、Perforceは[テレビゲーム](https://ja.wikipedia.org/wiki/テレビゲーム "wikilink")業界でもよく使われており、[ユービーアイソフト](https://ja.wikipedia.org/wiki/ユービーアイソフト "wikilink")や[スクウェア・エニックス](../Page/スクウェア・エニックス.md "wikilink")が採用している\[4\]。

クライアントの[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")、[グラフィカルなものと](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[コマンドラインとがあり](https://ja.wikipedia.org/wiki/キャラクターユーザインタフェース "wikilink")、各種[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で動作する。また、各種[統合開発環境](../Page/統合開発環境.md "wikilink")（Eclipse、Visual Studio、Codewrightなど）や[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")のアプリケーションへの[プラグイン](../Page/プラグイン.md "wikilink")もある\[5\]。

システムのその他の機能として、ファイル更新をユーザーに通知する機能、分岐や統合、[データベース](../Page/データベース.md "wikilink")のチェックポイント、[バグ管理システム](https://ja.wikipedia.org/wiki/バグ管理システム "wikilink")との連携などがある。

## 長所

  - 高速である。特にsync操作が高速である。
  - 分岐と統合は[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversionよりも柔軟だが](../Page/Apache_Subversion.md "wikilink")、システム構成の異なる[Git](https://ja.wikipedia.org/wiki/Git "wikilink")や[BitKeeper](../Page/BitKeeper.md "wikilink")ほどではない。
  - インストールやサーバの運用が単純。
  - 大規模構成が可能である。[2016年](../Page/2016年.md "wikilink")には935[TBのリポジトリを使った運用事例が報告されている](https://ja.wikipedia.org/wiki/テラバイト "wikilink")\[6\]。

## 短所

  - データは暗号化されない。サードパーティー製品（SSH tunnelやVPN）を使えば暗号化可能。
  - 高価である。ユーザー毎のライセンスとなっている\[7\]。

## 関連項目

  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")
  - [ソフトウェア構成管理](../Page/ソフトウェア構成管理.md "wikilink")

## 脚注

## 外部リンク

  - [Perforce Software](https://www.perforce.com/)
  - [東陽テクニカ - 高速ソフトウェア構成管理ツール Perforce Helix](https://www.toyo.co.jp/ss/products/detail/perforce)

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink")

1.
2.
3.
4.
5.  プラグイン可能なアプリケーションとしては、[Xcode](https://ja.wikipedia.org/wiki/Xcode "wikilink")、[オートデスク](https://ja.wikipedia.org/wiki/オートデスク "wikilink")、[3ds Max](https://ja.wikipedia.org/wiki/3ds_Max "wikilink")、[Maya](https://ja.wikipedia.org/wiki/Maya "wikilink")、[Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink")、[Microsoft Office](../Page/Microsoft_Office.md "wikilink")、[Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")、[GNU Emacsなどがある](https://ja.wikipedia.org/wiki/GNU_Emacs "wikilink")。
6.
7.