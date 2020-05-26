> この記事は[7-Zip](https://ja.wikipedia.org/wiki/7-Zip)から翻訳されています。


**7-Zip**（**セブンジップ**）は、[Microsoft Windowsを主な対応OSとする](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[ファイルアーカイバである](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。

## 概要

7-Zip は、基本的に [7z](../Page/7z.md "wikilink") 書庫形式を操作するファイルアーカイバであるが、他の様々な種類の書庫形式にも対応している(Windows以外のOSには、対応する書庫形式の限られた[CUI版が移植されている](../Page/キャラクタユーザインタフェース.md "wikilink"))。

当初は [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 用に設計され、後にCUI版が他の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) でも利用可能となった。[UNIX](../Page/UNIX.md "wikilink")\[1\]、[UNIX 互換システム](../Page/Unix系.md "wikilink")\[2\]、および[AmigaOS](../Page/AmigaOS.md "wikilink")では[p7zipの形で移植され](https://ja.wikipedia.org/wiki/#p7zip "wikilink")、利用可能である。また、7-Zipは、DOS移植版、または[HX DOS ExtenderでWindows](https://ja.wikipedia.org/wiki/HX_DOS_Extender "wikilink")[コマンドライン版を走らせることにより](../Page/コマンドラインインタプリタ.md "wikilink")、DOSとも互換性がある。

7-Zipの操作は、コマンドライン（全システム）、[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（Windows のみ）、もしくはシームレスな Windows シェル環境の、いずれの方式を用いることができる。

[プロプライエタリな競争相手であり市場を先導する](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[WinZip](../Page/WinZip.md "wikilink")や[WinRAR](../Page/WinRAR.md "wikilink")と異なり、7-Zipは[GNU LGPLの下で](../Page/GNU_Lesser_General_Public_License.md "wikilink")（ただし[RAR](../Page/RAR.md "wikilink")ライセンスの制限がある）、[AESのコードは修正](../Page/Advanced_Encryption_Standard.md "wikilink") [BSDライセンス](../Page/BSDライセンス.md "wikilink")の下で配布されている[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 歴史

7-Zipの開発は[2000年](../Page/2000年.md "wikilink")に始まり、()により活発に開発されている。

[2007年](../Page/2007年.md "wikilink")に[SourceForge.net](../Page/SourceForge.net.md "wikilink")のコミュニティにより「技術デザイン」賞と「ベストプロジェクト」賞に選ばれた\[3\]。

2016年5月11日にバージョン「v16.00」に2件の脆弱性が存在することを米Ciscoのセキュリティ部門Talosが発表。「v16.04」では修正されている。\[4\]\[5\]

## 形式

### 7z 書庫形式

既定では、7-Zipは7z形式の書庫を作成する。[拡張子](../Page/拡張子.md "wikilink")は `.7z` である。各書庫は複数の[ディレクトリ](../Page/ディレクトリ.md "wikilink")（フォルダ）と[電子ファイルを含むことができる](../Page/ファイル_\(コンピュータ\).md "wikilink")。**コンテナ**形式として、積層的に組み合わせられたフィルタを使うことによりセキュリティやサイズの縮小が達成される。これらはプリプロセッサ、圧縮[アルゴリズム](../Page/アルゴリズム.md "wikilink")および暗号化フィルタからなる。

7z圧縮の中心段階では各種のアルゴリズムを使用する。もっともよく使われるのは[Bzip2](../Page/Bzip2.md "wikilink")と[LZMAである](../Page/Lempel-Ziv-Markov_chain-Algorithm.md "wikilink")。イーゴリ・パヴロフによって開発されたLZMAは比較的新しいシステムであり、7z形式の一部として初公開された。LZMAは[Range Coderによって符号化された大きな](https://ja.wikipedia.org/wiki/Range_Coder "wikilink")（サイズ 4 [GiB](https://ja.wikipedia.org/wiki/ギビバイト "wikilink") までの）LZベースのスライド辞書からなる。

LZMAの[圧縮比は非常に高くなる傾向がある](https://ja.wikipedia.org/wiki/データ圧縮比 "wikilink")。圧縮されたサイズは、どちらもプロプライエタリである[RAR](../Page/RAR.md "wikilink")や[ACEを含む](https://ja.wikipedia.org/wiki/ACE_\(ファイル形式\) "wikilink")、他の高圧縮率の形式に匹敵する。

ネイティブの7zファイル形式はオープンでモジュール化されており、すべてのファイル名を[Unicode](../Page/Unicode.md "wikilink")で格納する。

### 他のサポート書庫形式

Windows版の7-Zip は[7z](../Page/7z.md "wikilink")の他にも多数の[データ圧縮](../Page/データ圧縮.md "wikilink")形式および圧縮を行わない[書庫形式をサポートする](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。圧縮と展開（解凍）をサポートする形式には[tar](https://ja.wikipedia.org/wiki/tar "wikilink")、[xz](https://ja.wikipedia.org/wiki/xz_\(ファイルフォーマット\) "wikilink")\[6\]\[7\]、[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")、[ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、[WIMが含まれる](https://ja.wikipedia.org/wiki/Windows_Imaging_Format "wikilink")。展開のみをサポートする形式には[UNIX Compress](https://ja.wikipedia.org/wiki/UNIX_Compress "wikilink") (`.Z`)、[Cabinet](../Page/CAB.md "wikilink")、[RAR](../Page/RAR.md "wikilink")、[LZH](../Page/LHA.md "wikilink")、[ARJ](https://ja.wikipedia.org/wiki/ARJ "wikilink")、[cpio](https://ja.wikipedia.org/wiki/cpio "wikilink")、[RPMおよび](https://ja.wikipedia.org/wiki/RPM_\(ファイルフォーマット\) "wikilink")[deb書庫などが含まれる](https://ja.wikipedia.org/wiki/deb_\(ファイルフォーマット\) "wikilink")。また、[ISO 9660形式や](../Page/ISO_9660.md "wikilink")[UDF](../Page/ユニバーサルディスクフォーマット.md "wikilink")（[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") / [IEC](../Page/国際電気標準会議.md "wikilink") 13346 形式）の [CD/DVD イメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink") (`.iso`) の展開もサポートする。

これらの形式のいくつかを含んでいることは、パッケージを実質的に[非フリーにする各種の使用条件に従わせることに注意すべきである](../Page/プロプライエタリ・ソフトウェア.md "wikilink")（たとえばプロプライエタリな[RAR](../Page/RAR.md "wikilink")圧縮を含む）。

7-Zipは一部の[MSIファイルを開くことができ](../Page/Microsoft_Windows_Installer.md "wikilink")、ファイル内容に伴うメタファイルにもアクセスできる。一部の Microsoft CAB（[LZX](https://ja.wikipedia.org/wiki/LZX "wikilink")圧縮）と [NSIS](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink") (LZMA) インストーラ形式を開くこともでき、7-Zipは与えられたバイナリファイルが実際には書庫であるかどうかのチェックツールとして使える。

ZIPやgzipの電子ファイルを圧縮するとき、7-Zipは自家製の[Deflate](../Page/Deflate.md "wikilink")エンコーダを使用する。このエンコーダは圧縮速度と引き替えに、広く使われている[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")のDEFLATE実装よりも圧縮率の高い書庫を作成できることが多い。7-ZipのDeflateエンコーダ実装は[AdvanceCOMP](https://ja.wikipedia.org/wiki/AdvanceCOMP "wikilink")スイートのツールの一部として独立に入手可能である。

## 派生物

[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") [x64 Edition](https://ja.wikipedia.org/wiki/Microsoft_Windows#64_ビット_オペレーティング_システム "wikilink") 用の[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink") [CPU](../Page/CPU.md "wikilink")（[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink") や [Intel 64](https://ja.wikipedia.org/wiki/x64 "wikilink")、および [IA-64](../Page/IA-64.md "wikilink")）対応版が存在する。これは巨大なメモリのマップをサポートすることにより圧縮を高速化できる。すべてのバージョンがマルチ[スレッドをサポートする](../Page/スレッド_\(コンピュータ\).md "wikilink")。

### CUI 版

2つのCUI版（コマンドライン版）が提供されている。外部ライブラリを使用する 7z.exe と、モジュールが組み込まれている[スタンドアローン](../Page/スタンドアローン.md "wikilink")版の7za.exeである。しかし、7zaの圧縮・展開（解凍）サポートは[7z](../Page/7z.md "wikilink")、[ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、[tar](https://ja.wikipedia.org/wiki/tar "wikilink")、[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")および[UNIX Compress](https://ja.wikipedia.org/wiki/UNIX_Compress "wikilink") (`.Z`) 形式に限られている。

#### p7zip

[UNIX](../Page/UNIX.md "wikilink")\[8\]、および[Unix系](../Page/Unix系.md "wikilink")システム\[9\]で使うために移植されたがv16.02以降長期にわたり更新が途絶えている。

### 7-Zip Portable

[ポータブル版の](../Page/ポータブルアプリケーション.md "wikilink")7-Zip。[PortableApps.com](https://ja.wikipedia.org/wiki/PortableApps.com "wikilink")\[10\] がパッケージ化し、自サイトで配布している\[11\]。

## 機能

7-Zipは多くの機能をサポートする。いくつかは有名な商用圧縮ソフトウェアにも見あたらないものである。

  - [暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")方式として、[7z](../Page/7z.md "wikilink")書庫は256[ビット](../Page/ビット.md "wikilink")の[AESをサポートする](../Page/Advanced_Encryption_Standard.md "wikilink")。暗号化は電子ファイルと 7z ディレクトリ構造の両方に対して有効にできる。ディレクトリ構造が暗号化された場合、利用者は書庫内に含まれるファイル名を見るために[パスワード](../Page/パスワード.md "wikilink")を与える必要がある。WinZipが開発したAESによるZIP書庫暗号化の規格も利用可能だが、7z 書庫のようなファイル名の暗号化は提供されていない\[12\]。
  - 7-Zipは動的にサイズの変わる[ボリュームを柔軟にサポートする](https://ja.wikipedia.org/wiki/ボリューム_\(圧縮\) "wikilink")。これは書き換え可能[CDや](../Page/コンパクトディスク.md "wikilink")[DVD](../Page/DVD.md "wikilink")などのリムーバブルメディアへのバックアップに有用である。
  - 2分割画面モードのとき、7-Zipは基本的な伝統的[ファイルマネージャ](../Page/ファイルマネージャ.md "wikilink")であるとみなせる。
  - 7-Zipは壊れたファイル名を含む書庫を展開（解凍）し、必要に応じて改名する機能を持つ。
  - 自己解凍書庫を作成すれば、7z展開ソフトウェアを持たない利用者も圧縮された電子ファイルを展開（解凍）できる。

## 脚注

## 関連項目

  - [7z](../Page/7z.md "wikilink")
  - [ファイルアーカイバの比較（英語版）](https://ja.wikipedia.org/wiki/:en:Comparison_of_file_archivers "wikilink")
  - [PeaZip](https://ja.wikipedia.org/wiki/PeaZip "wikilink")

## 外部リンク

  - [7-zip.org](https://www.7-zip.org/)（公式サイト）
  - [the P7ZIP Home](http://p7zip.sourceforge.net/)
  - [SourceForge.net](https://sourceforge.net/)
      - [SourceForge.net: 7-Zip](https://sourceforge.net/projects/sevenzip/)
      - [SourceForge.net: p7zip](https://sourceforge.net/projects/p7zip/)
  - [sevenzip.osdn.jp](https://sevenzip.osdn.jp)（日本語公式サイト）
  - [OSDN](https://osdn.jp/)
      - [7-Zip — OSDN.JP](https://osdn.jp/projects/sevenzip/)
          - [7-Zip Wiki — OSDN.JP](https://osdn.jp/projects/sevenzip/wiki/)
  - [PortableApps.com](https://portableapps.com/)
      - [7-Zip Portable | PortableApps.com](https://portableapps.com/apps/utilities/7-zip_portable)
  - [7-Zip .NET wrapper](https://archive.codeplex.com/?p=sevenzipsharp)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:解凍ソフト](https://ja.wikipedia.org/wiki/Category:解凍ソフト "wikilink") [Category:1999年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1999年のソフトウェア "wikilink")

1.  [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Solaris](../Page/Solaris.md "wikilink") など。
2.  [Linux OS](../Page/Linux.md "wikilink")、[BSD系OS](../Page/BSDの子孫.md "wikilink")、[OpenSolaris](../Page/OpenSolaris.md "wikilink")などのOSや、[Cygwin](../Page/Cygwin.md "wikilink")など。
3.  [SourceForge.net: 7-Zip](http://sourceforge.net/projects/sevenzip/)
4.  <http://forest.watch.impress.co.jp/docs/news/757356.html>　
5.  <http://gblogs.cisco.com/jp/2016/05/multiple-7-zip-vulnerabilities-html/>
6.  [The .xz file format — The Tukaani Project](http://tukaani.org/xz/format.html)
7.  [:en:xz](https://ja.wikipedia.org/wiki/:en:xz "wikilink")
8.
9.
10. [:en:PortableApps.com](https://ja.wikipedia.org/wiki/:en:PortableApps.com "wikilink")
11. [7-Zip Portable | PortableApps.com](http://portableapps.com/apps/utilities/7-zip_portable)
12. [AES Encryption Information: Encryption Specification AE-1 and AE-2](http://www.winzip.com/aes_info.htm)