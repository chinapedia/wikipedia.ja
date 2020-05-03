> この記事は[LHA](https://ja.wikipedia.org/wiki/LHA)から翻訳されています。


**LHA**（ラー）とは、[ファイルの圧縮と](../Page/ファイル_\(コンピュータ\).md "wikilink")[アーカイブを行う](../Page/アーカイブ_\(コンピュータ\).md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")のひとつ。また、圧縮ファイルの形式はその拡張子から**LZH**（エルゼットエイチ）と呼ばれる。ここではLZH形式についても述べる。

## プログラム

LHAは、[奥村晴彦](../Page/奥村晴彦.md "wikilink")が考案した[アルゴリズム](../Page/アルゴリズム.md "wikilink")をもとに、吉崎栄泰が実装したもので、1988年に[パソコン通信](../Page/パソコン通信.md "wikilink")で公開した。

登場当時はという名前で、1990年頃に全面的に作り直したのに併せ**LHA**に改称した。当初はLHに改称の予定で、実際にバージョン2.00はLHとして公開したが、[MS-DOS](../Page/MS-DOS.md "wikilink")バージョン5.0の内部コマンドLOADHIGHの略称LHと被ったため**LHA**とした。ごく初期には「LHx/LHa」という名称・表記だった。

発音は、初期バージョンではLHAを「**ラー**」とすると作者による説明があったが、後期バージョンではその説明はない。また、[RAR](../Page/RAR.md "wikilink")との混同を避けるためにも、「**エルエイチエー**」「**ルハー**」「**エルハ**」等といった発音が 大勢である。

## フォーマット

LZH形式の圧縮アルゴリズムは、[LZSS法で圧縮したデータをさらに](https://ja.wikipedia.org/wiki/Lempel–Ziv–Storer–Szymanski "wikilink")[ハフマン法を用いて圧縮するLZHUFアルゴリズムを用いる](../Page/ハフマン符号.md "wikilink")。LZHUFは奥村晴彦の[LZARI](https://ja.wikipedia.org/wiki/奥村晴彦#LZARI法 "wikilink")（LZSS + [算術符号](../Page/算術符号.md "wikilink")）の効率を向上するために吉崎栄泰が考案したものである。

LZSS法ではスライド窓や最大一致長を大きく取るほどに圧縮率の向上が見込めるが、一方でむやみに大きくすると最長一致列の探索に時間がかかり、また多くのメモリも必要になる。このため初期の版ではスライド窓や最大一致長の大きさは小さくとられていたが、探索アルゴリズムの改良や[コンピュータ](../Page/コンピュータ.md "wikilink")の性能向上などにより、次第に大きな値が採用されるようになった。

LZH圧縮形式は大きくlh0、lh1、lh4/5/6/7に分けられる。 [圧縮率](../Page/圧縮率.md "wikilink")を高めたlh6/7方式が公開されているが、開発途中ということで同形式を使ったファイルの配布は推奨されていない。

### lh0形式

lh0形式は一切の圧縮を行わない。[可逆圧縮](../Page/可逆圧縮.md "wikilink")では圧縮前よりも圧縮後のデータの方がサイズが大きくなる場合があり、lh0形式はそれを避けるために使用される。ユーザーが意図してこの形式を使う場合は、ファイルの破損のチェックに使ったり\[1\]、複数のファイルをまとめるだけの[アーカイバとして利用される](../Page/アーカイブ.md "wikilink")。

### lh1形式

lh1形式のスライド窓の大きさは4Kバイト、最大一致長は60バイト。文字と一致長は動的ハフマン法で符号化されるが、一致位置はハフマン法を用いずに符号化される。LHarc 1.xではこの形式。

### lh4/5/6/7形式

各形式はスライド窓の大きさのみが異なり、それぞれ4K/8K/32K/64Kバイトである。最大一致長は256バイト。

圧縮データの展開速度の向上を目的として、符号化がlh1形式の動的ハフマン法から静的ハフマン法に変更されている。また、一致位置も、文字、一致長とは別にハフマン法で符号化される。

### MacLHA形式

「**MacLHA**」（旧MacLHarc）は[Macintosh](../Page/Macintosh.md "wikilink")([Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink"))のファイルシステム上のファイルを、LHA形式で圧縮するフリーソフトとして、石崎一明によって開発され配布された[フリーウェア](../Page/フリーウェア.md "wikilink")。当時一般的であった他のアーカイバ（[StuffIt](../Page/StuffIt.md "wikilink")および[Compact Pro](https://ja.wikipedia.org/wiki/Compact_Pro "wikilink")）はシェアウェアであったり、クロスプラットフォームでなかったりしたため、国内では広く使われた。基本圧縮アルゴリズムはMS-DOS用のLHAと同じだが、Mac OSのファイルシステムで使用される[リソースフォーク](../Page/リソースフォーク.md "wikilink")を含んだ状態で圧縮する為に[MacBinary形式にエンコードするという機能が加えられている](../Page/Macバイナリ.md "wikilink")。このため、MacLHAの圧縮ファイルはMS-DOSや[Windows上のLHA及び互換ソフトでは正常に展開する事ができない](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。また、ソフトウェア次第ではMacで解凍してもMacBinary形式のファイルが出てくるという事態も起こる。実際、[StuffIt Expanderで解凍を行った場合はMacBinaryをデコードしないため混乱したユーザは多い](../Page/StuffIt.md "wikilink")。この場合、出てきたファイルを再度StuffIt Expanderに通せばMacBinaryがデコードされる。

この回避策としてMacBinaryに変換せずに圧縮するオプションが付随しているが、この方法で圧縮した場合、逆に解凍時に[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") (Classic Mac OS) ではファイル識別が出来ない状態になる。それが実行ファイルであった場合、正常に起動できなくなる場合もある。これを防ぐため、バージョンによっては、このオプションを有効にしてリソースフォークを含むファイルを追加しようとすると、MacBinaryで保存するか、データフォークのみ保存するか（リソースフォークと[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")は失われる）、処理を中止するかの選択を促すダイアログが表示される。

## 経緯

LHAとLZH形式は、1988年の登場以来、[パソコン通信](../Page/パソコン通信.md "wikilink")や[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")での[データ](../Page/データ.md "wikilink")やり取りが主流の時代に重宝されて、MS-DOSのみならず各種のOSに移植されて発展を続けた。[ZIP形式アーカイブを作成するためのPKZIPが有料の](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[シェアウェア](../Page/シェアウェア.md "wikilink")（展開用のPKUNZIPは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であった）だったこともあり、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国内はもとより海外でも広く使われるようになった。例えば、[id Softwareの初期のゲームである](https://ja.wikipedia.org/wiki/id_Software "wikilink")[DOOM](../Page/DOOM.md "wikilink")と[Quake](../Page/Quake.md "wikilink")のインストーラの圧縮形式として採用されている。[1990年代](../Page/1990年代.md "wikilink")に[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")や[インターネット](../Page/インターネット.md "wikilink")が広く普及する時代となっても、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国内では事実上のデータ圧縮の標準的な形式として浸透していた。海外でLHAが標準的な圧縮形式として普及したケースとしては[Amiga](../Page/Amiga.md "wikilink")がある。

MS-DOSの後継OSであるWindowsへの対応としては、1995年に[NIFTY-Serve](https://ja.wikipedia.org/wiki/NIFTY-Serve "wikilink")上でバージョン3.0に向けたテスト版の位置づけでバージョン2.67が公開されたが、作者である[吉崎栄泰](../Page/吉崎栄泰.md "wikilink")の本業（医師）が忙しくなった\[2\]ためなのか、その後のバージョンアップ版は公開されておらず、LHAならびにLZH形式の開発は事実上停止状態にある。このためWindowsでは、すでに公開されているソースコードや仕様を元に他の人物が開発したアプリケーション（unlha32.dll、[Lhaplus](../Page/Lhaplus.md "wikilink")、[Lhasa](../Page/Lhasa.md "wikilink")、[+Lhaca](../Page/+Lhaca.md "wikilink")など）によってLZH形式の圧縮・展開が行われた。バージョン2.67は[EXE形式として提供されたが](../Page/EXEフォーマット.md "wikilink")、正式バージョンである3.0ではエンジン部分のみを[DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")として提供する構想\[3\]\[4\]だった。結果的にその役割はMicco作のUnlha32.dllが担うことになる。

[21世紀](../Page/21世紀.md "wikilink")に入った頃からは、他の形式の方が圧縮率で上回ることが多くなった他、[ファイル名](../Page/ファイル名.md "wikilink")に[Unicode](../Page/Unicode.md "wikilink")が含まれたデータを扱えないこと、[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")機能がないなど不便さが目立ちつつある。またZIP形式の圧縮復元機能が[Mac OS Xや](https://ja.wikipedia.org/wiki/macOS "wikilink")[Windows Meおよび](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")[Windows XP以降に内蔵されたことにより](../Page/Microsoft_Windows_XP.md "wikilink")、特に理由がない限り圧縮形式としてはZIPが使われることが多くなっている\[5\]。

ただし、LZHアーカイブを展開する需要は、既存のアーカイブ（特に日本産[オンラインソフトウェア](../Page/オンラインソフトウェア.md "wikilink")）の展開など依然存在している。このためWindows XPの「Webサービスを使用して適切なプログラムを探す」機能では、LZHによるものが常に最多だったという\[6\]。それを受けて[マイクロソフト](../Page/マイクロソフト.md "wikilink")社はLZH展開アドオン「[Microsoft 圧縮 (LZH 形式) フォルダ](https://ja.wikipedia.org/wiki/Microsoft_圧縮_\(LZH_形式\)_フォルダ "wikilink")」（Windows XPおよび[Windows Server 2003用](../Page/Microsoft_Windows_Server_2003.md "wikilink")）を正式に配布し\[7\]、日本語版の[Windows 7ではZIP形式と同様に](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")「圧縮フォルダ」として利用できるようになった。ただし、いずれもLZH形式での圧縮機能は搭載されておらず、圧縮には別途ソフトが必要となる。また、[WinRAR](../Page/WinRAR.md "wikilink")、[PeaZip](https://ja.wikipedia.org/wiki/PeaZip "wikilink")、[7-Zip](../Page/7-Zip.md "wikilink")などの海外製のアーカイブツールでもLZHに対しては解凍のみ対応している場合が多い。

### エピソード

日本では、アーカイブから中のファイルを取り出したり、圧縮データを展開（伸張）すること（たいていの人が識別できず、混同している）を「解凍」と呼ぶことが多いが、これはLHAのマニュアルを通して広まった、という面がある（当時のパソコン通信に参加した人数はそれほど多くなかったが、LHAはフリーソフト等を使うために必須のツールとなったため、雑誌の付録ディスクなどを通して、多くの人が入手したツールとなったことから。アーカイブへの格納（同時に圧縮するかもしれない\[8\]）は「凍結」と呼んでいる。なお、英語メッセージも同様に、meltとfreezeとなっている）。LHAの開発にも関わっている[奥村晴彦](../Page/奥村晴彦.md "wikilink")によれば\[9\]この意味の「解凍」という表現自体は、LHAより古くからパソコン通信で広く使われていた。

## LZH形式の使用中止の呼びかけ

対応ツールの1つであるUnlha32.dllの作者は、[アンチウイルスソフトの多くが一部のLZHアーカイブ](../Page/アンチウイルスソフトウェア.md "wikilink")(新しい圧縮形式、巨大な拡張ヘッダー、多数の拡張ヘッダーのいくつか)を正しく検疫できないことを2006年に発見し\[10\]、[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")や各セキュリティベンダーに報告した。しかしZIPや[CAB](../Page/CAB.md "wikilink")といった他の形式では同様のケースに対応しているのにLZHについては4年後の[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")になっても対応が進まない\[11\]ことから、[6月5日](https://ja.wikipedia.org/wiki/6月5日 "wikilink")にLZH形式の利用を控えるよう呼びかけを行っている\[12\]。

これを受けて、[ベクターがLZH形式での新規受付を中止している](../Page/ベクター_\(企業\).md "wikilink")\[13\]。

この問題はLHAおよびLZH形式そのものの脆弱性ではない（問題点はアンチウイルスソフトが対応しない点である）ものの、LZH形式に含まれる[マルウェア](../Page/マルウェア.md "wikilink")をアンチウイルスソフトが検出できないケースが存在するため、注意が必要となる\[14\]。

日本語版[Windows 7から標準搭載されるようになったLZHの展開機能は引き続き](../Page/Microsoft_Windows_7.md "wikilink")[Windows 10にも標準搭載されたが](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")、[2017年](../Page/2017年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")にリリースされたWindows 10 Creators Update以降、この機能は削除されている。

## 脚注

<references/>

## 関連項目

  - [7z](../Page/7z.md "wikilink")
  - [ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")
  - [CAB](../Page/CAB.md "wikilink")
  - [DGCA](https://ja.wikipedia.org/wiki/DGCA "wikilink")
  - [GCA](../Page/GCA.md "wikilink")
  - [RAR](../Page/RAR.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")
  - [ハフマン符号](../Page/ハフマン符号.md "wikilink")

## 参考文献

  - 奥村晴彦・吉崎栄泰「圧縮アルゴリズム入門」『C MAGAZINE』1991年1月号、ソフトバンク、44-68頁、1991年。

## 外部リンク

  - [データ圧縮の昔話](https://oku.edu.mie-u.ac.jp/~okumura/compression/oldstory.html)（奥村晴彦のページでLHA開発の経緯や当時のパソコン通信におけるやりとりを読むことができる）

  - [統合アーカイバプロジェクト](https://www.madobe.net/archiver/index.html)

  - [Micco's HomePage](https://micco.mars.jp/micindex.html)（UNLHA32.DLL作者 "Micco" のウェブページ）

  - [Windows XP用 LZH形式圧縮フォルダ](http://go.microsoft.com/fwlink/?LinkId=41654)（リンク切れ）

      - 上記と同じものと思われる拡張機能は[サポート文書番号896133](https://support.microsoft.com/ja-jp/help/896133)「Microsoft 圧縮 (LZH 形式) フォルダの使い方」として継続掲載。 (2013年2月15日閲覧)

  - [LHa for UNIX](https://ja.osdn.net/projects/lha/) ([SourceForge](https://ja.wikipedia.org/wiki/SourceForge "wikilink").JP プロジェクトページ)

  - [lhasa](https://fragglet.github.io/lhasa/)

以下は吉崎栄泰作のLHAダウンロードページ

  - [LHA ver2.55](https://www.vector.co.jp/soft/dos/util/se002413.html)
  - [LHA32 ver 2.67](https://www.vector.co.jp/soft/win95/util/se347175.html)
  - [LHAソースファイル集](https://www.vector.co.jp/soft/dos/util/se002340.html)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:解凍ソフト](https://ja.wikipedia.org/wiki/Category:解凍ソフト "wikilink") [Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:1988年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1988年のソフトウェア "wikilink")

1.  CRC値のみでハッシュ値でのチェックは無いため、意図的な改竄は検出できず、破損の検出以上のチェックには使えない。
2.  [吉崎栄泰のLHAワールド - LHAの今とこれから](https://web.archive.org/web/19990506162851/www.clione.ne.jp/lha/lha4.html) - [インターネットアーカイブ](../Page/インターネットアーカイブ.md "wikilink")の1999年5月8日付のキャッシュ
3.
4.  バージョン2.67付属ドキュメント
5.  両者ではファイル名のエンコードが異なり、macOSの機能（[UTF-8](../Page/UTF-8.md "wikilink")でエンコード）で作成したアーカイブをWindowsの機能（[Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")でエンコード）で復元すると、ファイル名によっては文字化けする。内容には影響しない。Windows → macOSでは問題ない。
6.
7.
8.  全く圧縮できない場合など、lh0形式で格納する場合は圧縮しない。
9.  [Haruhiko, Okumura. (@h_okumura). "「解凍」はLHAより古くからパソコン通信で広く使われていました <https://t.co/Ln2jA65uvf> " 2017年1月9日, 20:42 (JST). Tweet.](https://twitter.com/h_okumura/status/818784959280205824)
10. [MHVI\#20061019：LZH 書庫のヘッダー処理における脆弱性について](http://micco.mars.jp/notes/headerBOF.htm)
11. [MHVI\#20100425：LZH 書庫のヘッダー処理における脆弱性について (2010 年版)](http://micco.mars.jp/vul/2010/mhvi20100425.htm)
12.
13. [LZH形式でファイルをご登録いただいている作者のみなさまへ](http://www.vector.co.jp/for_authors/upload/warn_lzh.html) - ベクター 2010年6月9日
14.