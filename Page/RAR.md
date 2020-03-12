> この記事は[RAR](https://ja.wikipedia.org/wiki/RAR)から翻訳されています。


**RAR**（ラー、アールエーアール）は[データ圧縮](../Page/データ圧縮.md "wikilink")の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")の一つ。元々は [MS-DOS](../Page/MS-DOS.md "wikilink") ベースのファイル圧縮ソフトウェアの名前及びファイルフォーマットである。

## 概要

[ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink") に比べ高い圧縮率であり、他の圧縮形式にはあまり見られない特色としてリカバリレコードが挙げられる。リカバリレコードとは、一種の[ハミング符号](../Page/ハミング符号.md "wikilink")を付加することで圧縮ファイルの破損をある程度まで修復可能とするものである。また、一定のサイズごとに分割して圧縮することができる。

[WinRAR](../Page/WinRAR.md "wikilink") や [MacRAR](https://ja.wikipedia.org/wiki/MacRAR "wikilink") などの[ソフトウェア](../Page/ソフトウェア.md "wikilink")で処理を行うことができる。

[2013年](../Page/2013年.md "wikilink")にリリースされたWinRAR5より新フォーマットRAR5が登場した。拡張子は.rarと同じであるが、古いバージョンのソフトウェアでは扱うことができない。

## 拡張子

通常のファイルは.rar、.RAR。マルチボリューム(分割）ファイルは古バージョンではrar、.r00、r01、r02のような拡張子の連番ファイルとなる（現在のバージョンでは.part1.rar、.part2.rarのようになる）。.revはリカバリーボリュームファイル。

## フォーマット

  - v1.3 (オリジナル、"Rar\!"のシグネチャーを持たない)
  - v1.5
  - v2.0 - WinRAR 2.0とMS-DOS2.0向けの Rarにてリリース。以下の特徴を持つ:
      - トゥルーカラービットマップ画像、非圧縮オーディオ向けのマルチメディア圧縮
      - 1MBまでの圧縮辞書サイズ
      - リカバリーレコード

<!-- end list -->

  - v2.9 - WinRAR 3.00にてリリース
      - 拡張子が従来の {ボリューム名}.rar, {ボリューム名}.r00, {ボリューム名}.r01, etc. から、{ボリューム名}.part001.rar, {ボリューム名}.part002.rar, etc. に変更
      - ファイルヘッダとファイルのデータ両方が暗号化されるようになった（従来はファイル名だけは閲覧可能だった）。
      - 圧縮方式として 4 MB の辞書を使用、テキストデータには Dmitry Shkarin の PPMII アルゴリズムが使用可能、他のデータにはプラットフォームとファイルタイプに応じた事前処理のためのフィルタを使用する。
      - 暗号化方式が[Cipher Block Chainingから](https://ja.wikipedia.org/wiki/暗号利用モード#CBC "wikilink")[AES](../Page/Advanced_Encryption_Standard.md "wikilink") の 128 ビット長の暗号鍵に変更可能
      - リカバリーボリューム(.rev)が作成可能。ボリュームセットの欠損ファイルを修復できる。
      - 9 GB以上の圧縮ファイルが作成可能。
      - [Unicode](../Page/Unicode.md "wikilink")対応、ファイル名は[UTF-16](../Page/UTF-16.md "wikilink")リトルエンディアンで保存。

<!-- end list -->

  - v5.0 - WinRAR 5.0以降でサポート
      - 最大圧縮辞書サイズが1GBにアップ。デフォルトが32MBに（WinRAR 4、v2.9フォーマットでのデフォルトは4MB）。
      - RAR、ZIPフォーマットでのファイル名の最大長が2048文字までにアップ。
      - [リード・ソロモン符号](../Page/リード・ソロモン符号.md "wikilink")によるリカバリーレコードにより、複数エリアに損傷があるアーカイブの復元性能がアップ。有効なリカバリーレコードサイズ上限が256MBから無制限に。
      - リカバリーボリュームの高速化。上限が通常ボリュームファイル含めて255個から65535個に
      - [UTF-8](../Page/UTF-8.md "wikilink")にてファイル名を保存
      - ファイルタイムスタンプを[UTC](https://ja.wikipedia.org/wiki/UTC "wikilink")で保存
      - 解凍時のマルチスレッドサポート
      - 256ビットAESによる暗号化.
      - 32ビットCRCに加えオプションで256ビット[BLAKE](https://ja.wikipedia.org/wiki/BLAKE "wikilink")2spチェックサムをサポート
      - 重複ファイルを検出し、重複ファイルのうち1つだけを保存する機能。解凍時に重複ファイルも復元される。
      - [NTFS](https://ja.wikipedia.org/wiki/NTFS "wikilink") ハードリンク、シンボリックリンク、リパース・ポイント保存に対応
      - クイックオープンレコード。アーカイブに格納されるファイルのヘッダーコピーをまとめて、アーカイブ末尾に加えることで、アーカイブファイルを高速に読み込むことが可能。ヘッダーサイズ分アーカイブ容量が増えるため、デフォルトではファイルサイズの大きなアーカイブのみ有効。
      -
      - テキスト圧縮、マルチメディア圧縮、Itanium実行ファイル圧縮アルゴリズムの削除。これにより一部のファイルはRAR5より従来フォーマットのほうが圧縮率が高い。

## 関連項目

  - [CBR](https://ja.wikipedia.org/wiki/CDisplay_RAR_Archived_Comic_Book_File "wikilink") - RAR を用いたデータフォーマット
  - [7-Zip](../Page/7-Zip.md "wikilink")
  - [ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")
  - [LHA](../Page/LHA.md "wikilink") - 同じく「ラー」と呼ぶユーザーがいる
  - [CAB](../Page/CAB.md "wikilink")
  - [DGCA](https://ja.wikipedia.org/wiki/DGCA "wikilink")
  - [GCA](../Page/GCA.md "wikilink")

## 外部リンク

  - [RARLAB](https://www.rarlab.com/) - 開発元
  - [WinRAR in Japan](https://www.winrarjapan.com/) - 日本オフィシャルページ
  - [MacRAR Project](https://osdn.net/projects/sfnet_macrar/) - SourceForge.jp
  - [BetterZip 2](https://macitbetter.com/) ([macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"))

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink")