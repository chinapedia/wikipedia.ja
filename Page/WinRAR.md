> この記事は[WinRAR](https://ja.wikipedia.org/wiki/WinRAR)から翻訳されています。


**WinRAR**（ウィンアールエーアール／ウィンラー）はと彼の兄弟であるアレクサンダー・ローシャルが開発を行っているWindowsに対応したシェアウェアの[アーカイバである](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。独自の[RAR](../Page/RAR.md "wikilink")ファイルとZIPファイルの作成に対応するほか、多くの圧縮フォーマットの[解凍](https://ja.wikipedia.org/wiki/解凍 "wikilink")をサポートしている。コマンドライン版は「RAR」と「UNRAR」と呼ばれ、Windowsのほか[MS-DOS](../Page/MS-DOS.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、Linux、FreeBSDに対応している。Linux用のコマンドライン版は、[GNOME](../Page/GNOME.md "wikilink")や[KDE](../Page/KDE.md "wikilink")、[MATEなどの](https://ja.wikipedia.org/wiki/MATE_\(デスクトップ環境\) "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")に標準搭載されているGUIアーカイバのプラグインとしても動作する。[Android](../Page/Android.md "wikilink")アプリであるRAR for Androidもリリースされている。 Mac用のコマンドライン版は、[BetterZip4](https://ja.wikipedia.org/wiki/BetterZip4 "wikilink")のプラグインとしても動作する。

## 特徴

[RAR](../Page/RAR.md "wikilink")形式の圧縮を行う。[ZIP形式](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")・[LHA](../Page/LHA.md "wikilink")などの圧縮フォーマットに比べて、比較的高い圧縮率を持つ。WinRARでは作成した[RAR](../Page/RAR.md "wikilink")形式のファイルなど、圧縮されたファイルのことを[書庫と呼ぶ](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。

WinRARは、[RAR](../Page/RAR.md "wikilink")形式のファイルを[解凍](https://ja.wikipedia.org/wiki/解凍 "wikilink")できない[Windowsユーザーに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[RAR](../Page/RAR.md "wikilink")形式を使えるように自己解凍形式で[RAR](../Page/RAR.md "wikilink")の圧縮ファイルを作成できる。また圧縮時にパスワードをかけることができる。

現在、Windows上で[RAR](../Page/RAR.md "wikilink")の圧縮ができるのは、WinRARとそれに付属する、rar.exeのみである。

WinRAR5より新しい圧縮フォーマットであるRAR5が使用可能になった。拡張子は.rarのままであるが従来のRAR対応ソフトウェアでは扱うことができない。

### リカバリレコード

[RAR](../Page/RAR.md "wikilink")形式のファイルには、「リカバリレコード」と呼ばれる特殊なデータを付与することができ、圧縮ファイルの一部が破損した場合にリカバリレコードを用いてファイルを修復することができる。WinRAR.exeを使用する場合、リカバリレコードは圧縮ファイル全体のサイズのうち1～10%のサイズで自由に設定することができ、このサイズが大きいほうが破損時に修復できる可能性が増す。Rar.exeではリカバリレコードの割合に上限はない。通常、5%程度のリカバリレコードが付与されていれば破損を修復することが可能である。

### リカバリーボリューム

ボリューム分割を使用した場合には、拡張子が.revのリカバリーボリュームを作成できる。これは分割ファイルが不足している場合にその代わりとなり、欠損ボリュームを復元する機能を持つ。revファイルの数が欠損分割ファイルの数より上回っている場合に復元が可能である。

### インストーラ作成

自己解凍形式の書庫に既定の書式に従ってコメントを付与することで、[ウィザードライクな](../Page/ウィザード_\(ソフトウェア\).md "wikilink")[インストーラを作成することができる](https://ja.wikipedia.org/wiki/インストール#インストーラ "wikilink")。これはインストール書庫と呼ばれている。ただし、ショートカットアイコン作成やレジストリ操作といった本格的な機能は備えていないため、自己解凍書庫をインストーラのように見せる程度のものでしかない。

### ボリューム分割

[FATなどで](../Page/File_Allocation_Table.md "wikilink")1つのファイルサイズに制約がある場合や、[CDなどの容量制限がある](../Page/コンパクトディスク.md "wikilink")[メディアに](../Page/メディア_\(媒体\).md "wikilink")[コピー](../Page/コピー.md "wikilink")する場合などは、圧縮ファイル単体のサイズを一定値以下に抑える必要がある。WinRARでは、[ボリューム](https://ja.wikipedia.org/wiki/ボリューム "wikilink")分割という機能が利用できる（自己解凍形式でも可能で、[RAR](../Page/RAR.md "wikilink")形式のファイルに限る）。

圧縮後のファイルサイズが指定のサイズ以上になるとファイル名末尾に「.part0.rar」のように[サフィックスを付与し](../Page/接尾辞.md "wikilink")、複数のファイルに分割する（古いバージョンではrar, .r00,.r01のような拡張子となる）。 解凍時は分割された全てのファイルを用意すれば解凍することができる。

## 対応拡張子

[RAR](../Page/RAR.md "wikilink")、[ZIPの圧縮と解凍](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")。

[ARJ](https://ja.wikipedia.org/wiki/ARJ "wikilink")・[BZ2](../Page/Bzip2.md "wikilink")・[CAB](../Page/CAB.md "wikilink")・[EXE](https://ja.wikipedia.org/wiki/EXE "wikilink")・[GZ](https://ja.wikipedia.org/wiki/GZ "wikilink")・[ISO](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")・[JAR](https://ja.wikipedia.org/wiki/JAR "wikilink")・[TAR](https://ja.wikipedia.org/wiki/TAR "wikilink")・[uuencode](https://ja.wikipedia.org/wiki/uuencode "wikilink")(UUE)・[XZ](https://ja.wikipedia.org/wiki/xz_\(ファイルフォーマット\) "wikilink")・[Z](https://ja.wikipedia.org/wiki/UNIX_Compress "wikilink")・[7Z](../Page/7-Zip.md "wikilink")・[LZH](https://ja.wikipedia.org/wiki/LZH "wikilink")・[TAR](https://ja.wikipedia.org/wiki/TAR "wikilink")・[GNU ZIPの解凍](../Page/Gzip.md "wikilink")。　

[ACEの解凍をかつてサポートしていたが](https://ja.wikipedia.org/wiki/ACE_\(ファイルフォーマット\) "wikilink")、セキュリティ上の問題によりバージョン5.70 Beta 1より削除された\[1\]。

## バージョンヒストリー

以下が、バージョン情報の概要である。 バージョン2.00は[1996年](../Page/1996年.md "wikilink")[9月6日](../Page/9月6日.md "wikilink")にリリースされた。

  - バージョン2.90　新たに、RAR3[アーカイブ](../Page/アーカイブ.md "wikilink")形式を実装する。 旧バージョンでは、この新しい形式で圧縮されたアーカイブを展開できない。
  - バージョン3.50　[Windows XP x64 Editionをサポートに追加](https://ja.wikipedia.org/wiki/Microsoft_Windows_XP_Professional_x64_Edition "wikilink")。
  - バージョン3.60　圧縮[アルゴリズム](../Page/アルゴリズム.md "wikilink")の[マルチスレッド化と圧縮速度を改良をする](../Page/スレッド_\(コンピュータ\).md "wikilink")。
  - バージョン3.70　[Windows Vistaをサポートに追加](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。
  - バージョン3.80　[UTF-8](../Page/UTF-8.md "wikilink")における[Unicode](../Page/Unicode.md "wikilink")ファイル名を含むZIPアーカイブのサポート。
  - バージョン3.90　Windows x64と[Windows 7をサポートに追加](../Page/Microsoft_Windows_7.md "wikilink")。
  - バージョン3.91　[7-Zip](../Page/7-Zip.md "wikilink")で作成されたアーカイブ[LZMA2](https://ja.wikipedia.org/wiki/LZMA2 "wikilink")をサポート。
  - バージョン4.00 (2011年3月)　最大30%解凍速度が向上。Windows98、ME、NTがサポート外に。
  - バージョン4.10　ZIPファイルのサポートを強化。2GBもしくは65535個を超えるZIPファイルが作成可能に。ZIPファイルのボリューム分割やユニコードファイル名の保存もサポート。
  - バージョン4.20　[SMPモード時の圧縮速度が大幅に向上した](../Page/対称型マルチプロセッシング.md "wikilink")。Windows2000のサポートを廃止。
  - バージョン5.00 (2013年9月)　新しいRAR5フォーマットをサポート。
  - バージョン5.01 (2013年12月14日)\[2\]\[3\]。
  - バージョン5.21 (2015年11月18日)
  - バージョン5.30 (2015年11月24日)
  - バージョン5.31 (2016年2月4日)　
  - バージョン5.40 (2016年8月16日)
  - バージョン5.50 (2017年8月17日)
  - バージョン5.60 (2018年6月26日)
  - バージョン5.61 (2018年10月1日)
  - バージョン5.70 (2019年2月26日)
  - バージョン5.71 (2019年4月29日)
  - バージョン5.80 (2019年12月11日)
  - バージョン5.90 (2020年3月30日)
  - バージョン5.91 (2020年6月29日)

()内の日付は英語版の発表日である。

## その他

元々は[MS-DOS](../Page/MS-DOS.md "wikilink")ベースのアーカイバであったRARのWindows対応版という意味でのWinRARであるが、WinRARの機能充実とDOS版の開発停止（[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")を用いた32ビット版RAR32はなお存続している）により、元々のRARアーカイバ（DOS以外のコマンドライン版もある）はWinRARの派生品となった。

[コマンドプロンプト](../Page/コマンドプロンプト.md "wikilink")や[バッチファイル](../Page/バッチファイル.md "wikilink")から圧縮・解凍を行うプログラム「rar.exe」が付属している。

## 脚注

## 関連項目

  - [ファイルアーカイバの比較（英語版）](https://ja.wikipedia.org/wiki/:en:Comparison_of_file_archivers "wikilink")

## 外部リンク

  - [WinRAR 日本語公式サイト](http://www.winrarjapan.com/) - 株式会社デジカ運営の、日本語公式サイト。
  - [RarLab](http://www.rarlab.com/) - 開発元の公式サイト

[Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:解凍ソフト](https://ja.wikipedia.org/wiki/Category:解凍ソフト "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink")

1.  [19年前から存在か ～圧縮・解凍ソフト「WinRAR」にゼロデイ脆弱性](https://forest.watch.impress.co.jp/docs/news/1170860.html) 2019年2月21日 [窓の杜](../Page/窓の杜.md "wikilink") 2019年8月19日閲覧
2.
3.