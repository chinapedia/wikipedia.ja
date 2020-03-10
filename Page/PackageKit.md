> この記事は[PackageKit](https://ja.wikipedia.org/wiki/PackageKit)から翻訳されています。


**PackageKit** とは、多数の[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")に対して、質の高い[フロントエンド](../Page/フロントエンド.md "wikilink")を提供することを目指したソフトウェアのことである。[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") のもとで提供されている。

[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")を謳っているが、実際には freedesktop.org による[相互運用性](https://ja.wikipedia.org/wiki/相互運用性 "wikilink")の規定に従った各種 [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") [ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")が最大のターゲットである。

[プロセス間通信](../Page/プロセス間通信.md "wikilink")、あるいは特権の必要な作業を処理するときは、[D-Bus](../Page/D-Bus.md "wikilink")や[PolicyKit](https://ja.wikipedia.org/wiki/PolicyKit "wikilink")を使用する。

## 歴史

Richard Hughes によって作成され、[2007年](../Page/2007年.md "wikilink")に[ブログ](../Page/ブログ.md "wikilink")で初めて提供された。現在は小規模なチームによって開発が続けられている。

[Fedora](../Page/Fedora.md "wikilink")が初めて[Yumのための標準のフロントエンドとして](https://ja.wikipedia.org/wiki/Yellowdog_Updater_Modified "wikilink")、バージョン9で採用した。

## 設計

PackageKit自体はpackagekitdとよばれる[デーモン](../Page/デーモン.md "wikilink")であり、異なるシステム間の相違点をまとめる。libpackagekitとよばれる[ライブラリ](../Page/ライブラリ.md "wikilink")は、他のプログラムがPackageKitと連携して動作することを可能にしている。

## 機能

  - [ローカル](https://ja.wikipedia.org/wiki/ローカル "wikilink")[ファイル](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")、[メディア](../Page/メディア.md "wikilink")、遠隔地からの提供物を[インストール](../Page/インストール.md "wikilink")
  - [PolicyKit](https://ja.wikipedia.org/wiki/PolicyKit "wikilink")の利用を証明
  - 既存の[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")を入れ替えない
  - ユーザが変わったことを瞬時に確認（危険な処理の最中に[シャットダウン](https://ja.wikipedia.org/wiki/シャットダウン "wikilink")を禁止）
  - 使われていないときには終了

## バックエンド

PackageKitが利用可能な[パッケージ管理システム](https://ja.wikipedia.org/wiki/パッケージ管理システム "wikilink")（[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")）は以下の通りである。

  - Arch Linux Package Management([Pacman](https://ja.wikipedia.org/wiki/Pacman "wikilink"))

  - [APT](https://ja.wikipedia.org/wiki/APT "wikilink")

  - [DNF](https://ja.wikipedia.org/wiki/DNF_\(ソフトウェア\) "wikilink")

  - [Entropy](https://ja.wikipedia.org/wiki/Entropy "wikilink")（[Sabayon Linux](https://ja.wikipedia.org/wiki/Sabayon_Linux "wikilink")）

  -
  - [PISI](https://ja.wikipedia.org/wiki/PISI "wikilink")

  - [poldek](https://ja.wikipedia.org/wiki/poldek "wikilink")

  - [Portage](https://ja.wikipedia.org/wiki/Portage "wikilink")

  -
  -
  - YUM([Yellowdog Updater Modified](https://ja.wikipedia.org/wiki/Yellowdog_Updater_Modified "wikilink"))

  - [ZYpp](https://ja.wikipedia.org/wiki/ZYpp "wikilink")

## フロントエンド

  - gnome-packagekit
    [GNOME](../Page/GNOME.md "wikilink") デスクトップで使われる[フロントエンド](../Page/フロントエンド.md "wikilink")。[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") のもとで提供されている。
  - KPackageKit
    [KDE](../Page/KDE.md "wikilink") デスクトップ環境で利用される。
  - pkcon
    コマンドラインで利用される。

## 脚注

## 外部リンク

  - [PackageKit](http://www.packagekit.org/)

[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink")