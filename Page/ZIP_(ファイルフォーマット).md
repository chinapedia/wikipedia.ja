> この記事は[ZIP \(ファイルフォーマット\)](https://ja.wikipedia.org/wiki/ZIP_\(ファイルフォーマット\))から翻訳されています。


**ZIP**（ジップ）は、[データ圧縮](../Page/データ圧縮.md "wikilink")や[アーカイブの](../Page/アーカイブ_\(コンピュータ\).md "wikilink")[フォーマット](../Page/ファイルフォーマット.md "wikilink")。[Windowsでよく使用されるフォーマットである](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[1\] 。

## 概要

ZIPファイルフォーマット（以下ZIPフォーマット、またはZIP）は複数のファイルを一つのファイルとしてまとめて取り扱うアーカイブフォーマットであり、1つ以上のファイルが格納されているものである。必要に応じて各種ある圧縮アルゴリズムを選択・使用し、ファイルサイズを圧縮して格納することも可能である。

ZIPフォーマットは1989年に[フィル・カッツ](../Page/フィル・カッツ.md "wikilink")が考案したもので、[トム・ヘンダーソンが考案したそれまでの](https://ja.wikipedia.org/wiki/:en:Thom_Henderson "wikilink")[ARCフォーマットに置き換わるものとして](https://ja.wikipedia.org/wiki/:en:ARC_\(file_format\) "wikilink")、[PKWAREの](https://ja.wikipedia.org/wiki/:en:PKWARE "wikilink")[PKZIPユーティリティ](https://ja.wikipedia.org/wiki/:en:PKZIP "wikilink") \[2\]に実装された。 ZIPフォーマットは現在多くのユーティリティによってサポートされている（[ファイルアーカイバのリストを参照](https://ja.wikipedia.org/wiki/:en:List_of_file_archivers#Archive_format_support "wikilink")）。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でのサポートとしては、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Windows 98以降の各バージョンに](../Page/Microsoft_Windows_98.md "wikilink")「圧縮フォルダー」という名前でZIPの機能を組み込んでいるほか、[アップルも](../Page/アップル_\(企業\).md "wikilink")[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") [v10.3以降に他の圧縮フォーマットも含めてZIPの機能を組み込んでいる](../Page/Mac_OS_X_v10.3.md "wikilink")。

ZIPファイルは一般的に ".zip" か ".ZIP" といった[拡張子](../Page/拡張子.md "wikilink")が付けられる。[MIMEタイプは](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")`application/zip`。ZIPフォーマットは、圧縮伸長を主目的としない多くのアプリケーションでも使用されているが、その際、拡張子には個々のアプリケーション固有に ".zip" とは異なる名前が用いられていることが多い。例えば、[Java Archiveの拡張子は](../Page/JAR_\(ファイルフォーマット\).md "wikilink") ".jar"であるが、このフォーマットの実態はZIPフォーマットである。他の具体例については「[\#ソフトにおける固有の拡張子](https://ja.wikipedia.org/wiki/#ソフトにおける固有の拡張子 "wikilink")」節を参照のこと。

## 歴史

"zip" （「速さ」を意味する） という名前はフィル・カッツの友人であるロバート・マホーニーの提案によるものであり、従来から有るARCやその他の圧縮フォーマットの圧縮時間よりも、自分たちのプロダクトの方が速いということをほのめかすという意図を持っていた。

ZIPファイルフォーマット仕様は、PKZIP0.9のパッケージに同梱されていた "APPNOTE.TXT" で初めて公開された。

ZIPフォーマットは[オープンフォーマット](../Page/オープンフォーマット.md "wikilink")として[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")でリリースされたものであり、ZIPフォーマットは誰しもが自由に利用でき、個人、団体、組織、あらゆる形態の利用において法的にもモラル的にも全くは制約はない\[3\]。

PKWAREもまた基本フォーマットをパブリックドメインとしており、誰でもZIPファイルを扱うアプリケーションを開発することができる。同じ見解が[FLOSS](https://ja.wikipedia.org/wiki/FLOSS "wikilink") [Info-ZIP](https://ja.wikipedia.org/wiki/Info-ZIP "wikilink")バージョンのプロダクトに付属するUNIX/LINUXドキュメント内でも見られる。そのドキュメントではzipファイルフォーマット、圧縮フォーマット、.ZIPの拡張子やファイルフォーマットへの小さな変更をパブリックドメインに置いたフィル・カッツへの感謝の念を示している。

## 起源

ZIPファイルフォーマットはPKWAREのフィル・カッツが考案し、PKZIPで実装された。ちなみにカッツは以前に「PKXARC」なるアーカイブ・ユーティリティーを公開していたが、システム・エンハンス・アソシエイツ社の[ARC](../Page/ARC.md "wikilink")というユーティリティの著作権を著しく侵害しているとして[民事訴訟](../Page/民事訴訟.md "wikilink")を起こされている。

## よく似た名前のフォーマット

名前の一部に "zip" という名前を使った標準化仕様やフォーマットがたくさんある。フィル・カッツはどんなアーカイブ種別でも "zip" という名前を使って良いと表明した。同じ[Deflate](../Page/Deflate.md "wikilink")圧縮アルゴリズムを使用していながら、ヘッダー・フッターの異なる物としては、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink") (RFC 1952) や [zlib](https://ja.wikipedia.org/wiki/zlib "wikilink") (RFC 1950) などがある。その他、よく似た名前の異なるファイルフォーマットや圧縮アルゴリズムとして[7z](../Page/7z.md "wikilink")、[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")、[rzipなどがある](https://ja.wikipedia.org/wiki/:en:rzip "wikilink")。

## バージョン履歴

.ZIPファイルフォーマット仕様にはバージョン番号がある。しかし、それは必ずしもPKZIPツールのバージョン番号とは対応せず、特にPKZIPバージョン 6以降がそれに該当する。PKWAREは、 PKZIP製品が先進的な機能を利用してアーカイブを展開できるように予備的な機能を幾度も追加している。しかし、そのようなアーカイブを作成するPKWARE仕様はPKZIPの次の主要なリリースまで公開されない。他の会社や組織は自分たちのペースでPKWAREの仕様をサポートしている。

PKWARE仕様による各バージョンの主な機能は以下の通り。

  - 2.0: ファイルエントリを[Deflate](../Page/Deflate.md "wikilink")で圧縮可能となった。
  - 4.5: 64ビットZIPフォーマットが記載された。
  - 5.0: DES、Triple DES、RC2、RC4を暗号化のためにサポートした。
  - 5.2: RC2-64を暗号化のためにサポートした。
  - 6.1: 承認されたストレージについて記載した。
  - 6.2.0: セントラルディレクトリの暗号化について記載した。
  - 6.3.0: Unicode (UTF-8) ファイル名のストレージについて記載した。サポートされるハッシュ、圧縮、暗号化アルゴリズムが追加された。
  - 6.3.1: SHA-256 / 384 / 512の標準的なハッシュ値に訂正した。
  - 6.3.2: 圧縮メソッド 97 ([WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")) について記載した。

[WinZip](../Page/WinZip.md "wikilink")のバージョン12.1からDeflateよりも新しい圧縮メソッド、特にBZipや[LZMA](../Page/Lempel-Ziv-Markov_chain-Algorithm.md "wikilink")、PPMd、Jpeg、Wavpackのメソッドを使用したファイルの拡張子に**`.zipx`**が使用されている。JpegとWavPackは「最適メソッド」圧縮が選択されたときに適切なファイル種別に対して適用されている\[4\]\[5\]。

## 標準化

2010年4月[ISO/IEC JTC 1で](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")、ZIP互換のISO / IECの国際標準フォーマットを作成するために開始されるプロジェクトを決めるための投票が行われた\[6\]。「ドキュメントパッケージング」という表題で提案されたプロジェクトは[OpenDocument](../Page/OpenDocument.md "wikilink")、[Office Open XMLや](../Page/Office_Open_XML.md "wikilink")[EPUB](https://ja.wikipedia.org/wiki/EPUB "wikilink")を含む既存の標準規格の利用に適したZIP互換の最小圧縮アーカイブフォーマットと考えられる。

現在のZIPフォーマットは[オープンフォーマット](../Page/オープンフォーマット.md "wikilink")の要求仕様にあわないことがある。それは目に見える形で公開されたコミュニティ駆動開発を通して開発されていないからである。オープンな産業機構や標準化団体が賛同してメンテナンスされているものでもない。現在の ZIP フォーマットの一部は [フリー](../Page/フリーソフトウェア.md "wikilink") なファイルフォーマットの要求仕様にあっていない。誰もが ZIP フォーマットを、如何なる目的であっても金銭的な負担がなく利用できるようにするため、著作権、特許、商標などの制約がない。 [1](http://www.linfo.org/free_file_format.html) PKWARE サイトにある最新の資料は、著作権表示があるが、フォーマット仕様とその機能拡張がパブリックドメインに置かれていることを認めている。[2](http://www.pkware.com/security-software-company/philkatz)

## 技術的な情報

ZIPは複数のファイルを格納するシンプルなアーカイブフォーマットである。圧縮はzipアーカイブのオプションであり、圧縮が行われる場合はファイル単位に圧縮される。

ZIPは、データの破損に備えて優れた保護機構を提供するため、32ビットのCRCアルゴリズムを利用し、またアーカイブのディレクトリ構造を2箇所に含んでいる。

### 構造

ZIPファイルはファイルの最後に置かれるセントラルディレクトリの終端レコード（EOCD）の存在によって正しく認識される。この仕組みにより、新たなファイルを追加することが容易である。ZIPファイルに格納されているエントリ（ファイルまたはディレクトリ）数がゼロで無い場合、格納されている各エントリの名前、エントリに関するその他のメタデータ、ZIPファイル内でエントリデータが位置するオフセットが、セントラルディレクトリエントリに記載される。これにより、ファイルリストを参照するためにアーカイブ全体を読み込む必要がないため、アーカイブのファイルリストを比較的速く表示することが可能である。また冗長性の確保のため、各エントリも、エントリ情報をローカルファイルヘッダとして保持している。zipファイルが追加されることもあるため、ファイルの最後にあるセントラルディレクトリに載っているファイルだけが、正しいファイルである。セントラルディレクトリが、いくつかのファイルは削除された、あるい更新された、と宣言していることもありうるため、ZIPファイル全体を検索してローカルファイルヘッダを探しても、正しい情報は得られない（ただし、アーカイブが破損している場合は、そのような探索は役に立つだろう）。

セントラルディレクトリ内でのファイルエントリの順番は、アーカイブの中での実際のファイルエントリの順番と同じである必要はない。

ZIPファイル内のそれぞれのエントリは、ローカルファイルヘッダ（コメント、ファイルサイズやファイル名などの情報を含む）と、オプションの **「拡張」** データフィールドと、ファイルデータそのもの（圧縮されたり暗号化されている場合もある）で構成されている。「拡張」フィールドは、ZIP64フォーマット、WinZip互換のAES暗号化、ファイル属性やより詳細な[NTFSやUnixファイルのタイムスタンプをサポートするために使用される](../Page/NT_File_System.md "wikilink")。その他にも「拡張」フィールドを使用して機能拡張することが可能。認識しない拡張フィールドを無視するための機能をZIPツールに組み込む必要がある。

[ZIPformat_ja.jpg](https://ja.wikipedia.org/wiki/File:ZIPformat_ja.jpg "fig:ZIPformat_ja.jpg")

ZIPフォーマットはファイル内の様々な構造を表すために、特定の4バイトの「シグネチャ」を使用する。それぞれのファイルエントリは、ある特定のシグネチャによって目印が付けられる。セントラルディレクトリの終端レコードは、それ用のシグネチャでマークされ、セントラルディレクトリ内の各エントリは別の特定の4バイトシグネチャによって目印が付けられる。

ZIPの仕様にはBOFもしくはEOFといった目印がない。慣例として、ZIPファイルの最初にはZIPエントリが置かれ、そのシグネチャによって簡単にそれとわかる。しかし、ZIPの仕様においては、ZIPエントリで始まる必要はなく、特に、自己解凍型のアーカイブは、実行可能なファイルヘッダで始まる。

ZIPアーカイブを正しく読み込むには、まず初めにセントラルディレクトリの終端レコードのシグネチャを探し、次に、適宜、他のセントラルレコードを探索する必要がある。ファイルチャンクが開始する場所を特定するのはセントラルディレクトリのみであるため、ZIPファイルの頭からエントリを検査すべきではない。ZIPフォーマットは、チャンク間に他のデータを含めることや、シグネチャと同じ4バイト列を含むようなデータを禁止していないため、そのようなスキャンは誤検出（フォールス・ポジティブ）を起こすだろう。  ただし、破損したZIPアーカイブからデータを修復するためのツールは、ローカルヘッダシグネチャを探索するのが普通である。この場合、ファイルチャンクの後ろにファイルチャンクの圧縮サイズが格納されることが、シーケンシャルな処理を困難にしている。

また ZIPの仕様では、複数のファイルシステムにまたがって分散したアーカイブを扱うこともサポートしている。もともとは、複数の1.44MB[フロッピーディスク](../Page/フロッピーディスク.md "wikilink") にまたがった大きなzipファイルの格納を目的としていた。現在この機能は、ZIPアーカイブを分割してメールなどで送ったり、リムーバブルメディアで持ち運ぶのに使用されている。

DOSの[FATファイルシステムは](../Page/File_Allocation_Table.md "wikilink")2秒単位でタイムスタンプを保持し、ZIPファイルレコードはこれを模倣している。結果として、ZIPアーカイブ内にあるファイルのタイムスタンプも2秒単位で丸められる。但し、より正確なタイムスタンプを格納するために拡張フィールドを使用することができる。なお、ZIPフォーマットにはタイムゾーンという概念がないため、タイムスタンプが意味を持つのは、作成されたタイムゾーンを知っている場合だけである。

2007年9月にPKZIPは、[UTF-8](../Page/UTF-8.md "wikilink")のファイル名を格納するための仕組みを含むZIP仕様のリビジョンをリリースした。それは最終的にZIPに対するユニコード互換を追加するものである\[7\]。

#### ファイルヘッダ

全てのヘッダ内の複数バイトの値は、[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")で格納される。全ての長さを示すフィールドは、バイト単位で数える。

| オフセット  | サイズ | 内容\[8\]                                      |
| ------ | --- | -------------------------------------------- |
| 0      | 4   | ローカルファイルヘッダのシグネチャ = 0x504B0304（PK\\003\\004） |
| 4      | 2   | 展開に必要なバージョン (最小バージョン)                        |
| 6      | 2   | 汎用目的のビットフラグ                                  |
| 8      | 2   | 圧縮メソッド                                       |
| 10     | 2   | ファイルの最終変更時間                                  |
| 12     | 2   | ファイルの最終変更日付                                  |
| 14     | 4   | CRC-32                                       |
| 18     | 4   | 圧縮サイズ                                        |
| 22     | 4   | 非圧縮サイズ                                       |
| 26     | 2   | ファイル名の長さ (*n*)                               |
| 28     | 2   | 拡張フィールドの長さ (*m*)                             |
| 30     | *n* | ファイル名                                        |
| 30+*n* | *m* | 拡張フィールド                                      |

ZIPローカルファイルヘッダ

拡張フィールドはOSに特化した属性のような様々なオプションデータを含む。それは16ビットIDと16ビット長のチャンクに分割される。

このヘッダの直後には圧縮データのデータが続く。

汎用目的のビットフラグフィールドの3ビット目がセットされている場合、ヘッダの書き込み時にはCRC-32とファイルサイズが不明である。ローカルヘッダのCRC-32とファイルサイズのフィールドにはゼロが書き込まれ、CRC-32とファイルサイズは圧縮データの後ろに12バイトのデータとして追加される。（オプションの4バイトのシグネチャが前に付く場合もある。）

| オフセット | サイズ | 内容 \[9\]                                    |
| ----- | --- | ------------------------------------------- |
| 0     | 0/4 | （オプショナル） data descriptor シグネチャ = 0x08074b50 |
| 0/4   | 4   | CRC-32                                      |
| 4/8   | 4   | 圧縮サイズ                                       |
| 8/12  | 4   | 非圧縮サイズ                                      |

Data descriptor

セントラルディレクトリエントリはローカルファイルヘッダを拡張したものである。

| オフセット      | サイズ | 内容\[10\]                                         |
| ---------- | --- | ------------------------------------------------ |
| 0          | 4   | セントラルディレクトリエントリのシグネチャ = 0x504B0102（PK\\001\\002） |
| 4          | 2   | 作成されたバージョン                                       |
| 6          | 2   | 展開に必要なバージョン (最小バージョン)                            |
| 8          | 2   | 汎用目的のビットフラグ                                      |
| 10         | 2   | 圧縮メソッド                                           |
| 12         | 2   | ファイルの最終変更時間                                      |
| 14         | 2   | ファイルの最終変更日付                                      |
| 16         | 4   | CRC-32                                           |
| 20         | 4   | 圧縮サイズ                                            |
| 24         | 4   | 非圧縮サイズ                                           |
| 28         | 2   | ファイル名の長さ (*n*)                                   |
| 30         | 2   | 拡張フィールドの長さ (*m*)                                 |
| 32         | 2   | ファイルコメントの長さ (*k*)                                |
| 34         | 2   | ファイルが開始するディスク番号                                  |
| 36         | 2   | 内部ファイル属性                                         |
| 38         | 4   | 外部ファイル属性                                         |
| 42         | 4   | ローカルファイルヘッダの相対オフセット                              |
| 46         | *n* | ファイル名                                            |
| 46+*n*     | *m* | 拡張フィールド                                          |
| 46+*n*+*m* | *k* | ファイルコメント                                         |

セントラルディレクトリエントリ

全てのセントラルディレクトリエントリの後に、ZIPファイルの終わりを表すセントラルディレクトリの終端レコードが続く。

| オフセット | サイズ | 内容\[11\]                                            |
| ----- | --- | --------------------------------------------------- |
| 0     | 4   | セントラルディレクトリの終端レコードのシグネチャ = 0x504B0506（PK\\005\\006） |
| 4     | 2   | このディスクの数                                            |
| 6     | 2   | セントラルディレクトリが開始するディスク                                |
| 8     | 2   | このディスク上のセントラルディレクトリレコードの数                           |
| 10    | 2   | セントラルディレクトリレコードの合計数                                 |
| 12    | 4   | セントラルディレクトリのサイズ (バイト)                               |
| 16    | 4   | セントラルディレクトリの開始位置のオフセット                              |
| 20    | 2   | ZIPファイルのコメントの長さ (*n*)                               |
| 22    | *n* | ZIPファイルのコメント                                        |

ZIPセントラルディレクトリの終端レコード(EOCD)

この順番により、ZIPファイルをワンパスで作成することができるが、通常、展開では最後のセントラルディレクトリを最初に読み込むことになる。

### 圧縮メソッド

現在のZIPファイルフォーマット仕様では次のメソッドの詳細が記載されている。stored（無圧縮）、Shrunk、Reduced（メソッド 1-4）、Imploded、Tokenizing、Deflated、Deflate64、[BZIP2](https://ja.wikipedia.org/wiki/BZIP2 "wikilink")、LZMA (EFS)、[WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")、[PPMd](../Page/Prediction_by_Partial_Matching.md "wikilink")。最も一般的な圧縮メソッドは[DEFLATEでIETF](../Page/Deflate.md "wikilink") RFC 1951に記載されている。

圧縮メソッドに挙げられていても、PKWARE Data Compression Library (DCL) Imploding (old IBM TERSE), IBM TERSE (new), IBM LZ77 z Architecture (PFS) の仕様の詳細は記載されていない。

### 暗号化

ZIPはシンプルな[パスワード](../Page/パスワード.md "wikilink")ベースの[共通鍵暗号](../Page/共通鍵暗号.md "wikilink")をサポートすると仕様に記載されている。但し、重大な脆弱性があることが知られている。特に、既知平文攻撃に対して脆弱性があり、貧弱な[ランダム数生成器の実装によってさらに安全性が低くなる場合もある](https://ja.wikipedia.org/wiki/:en:random_number_generator "wikilink")\[12\]。

バージョン5.2以降の.ZIPファイルフォーマット仕様には、[圧縮](../Page/データ圧縮.md "wikilink") と [暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink") (例えば [AES](../Page/Advanced_Encryption_Standard.md "wikilink")) を含む新しい機能のメソッドが追加されている、と記載されている。WinZipはAESベースの標準規格を使用し、それは[7-Zip](../Page/7-Zip.md "wikilink")、XCeedやDotNetZipでも使用されている。しかし、ベンダによっては他のフォーマットを使用するものである\[13\] PKZIP また、SecureZIP は RC2, RC4, DES, Triple DES 暗号メソッド, 電子証明書ベースの暗号 / 認証 ([X.509](../Page/X.509.md "wikilink")) やアーカイブヘッダ暗号化をサポートする\[14\]。

### ZIP64

オリジナルのZIPフォーマットは、ZIPアーカイブ内のエントリに 65535 の制限があるのと同様に、様々なサイズ（ファイルの圧縮/非圧縮サイズ、アーカイブの合計サイズ）に4 GiBの制限があった。仕様のバージョン4.5（それは特定ツールのバージョン4.5と同じではない） では、PKWAREはこういった制限を回避するために16 EiB（2<sup>64</sup> バイト）まで増加させた "ZIP64" フォーマット拡張を導入した。ZIP64サポートは新規に発生したものである。例えば、Windows XPのファイルエクスプローラーはZIP64をサポートしないが、 Windows Vistaのエクスプローラーではサポートする。同様にDotNetZipやPerlのIO::Compress::Zip、PythonのzipfileのようなライブラリはZIP64をサポートする。Javaの組み込みモジュールjava.util.zipは 2010年9月現在ではサポートしていない。今後、[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")に追加されて[Java 7への同梱を予定している](https://ja.wikipedia.org/wiki/:en:Java_version_history#Java_SE_7.0 "wikilink")\[15\]。

### 長所と短所

ZIPファイルのようにファイルを分割して圧縮するとランダムアクセスが可能である。他のデータを読み込むことなく個々のファイルを取り出すことができる。DEFLATE圧縮の可能性を限定するときでさえ、それぞれのファイルのために違う辞書圧縮を利用するとアーカイブ全体のサイズをより小さくできることがある。

この圧縮の手法は一般的に小さなファイルが大量にあるときのアーカイブとしては適切ではない。ZIPアーカイブフォーマットでは、個々のエントリに関する情報を持つメタデータは圧縮しない。これは、特に個々のエントリのサイズを小さくして、そのエントリ向けのメタデータのサイズを扱うようにアーカイブ可能な最大圧縮比率を設けて制限されているためである。

別の手法としては [圧縮されたtarアーカイブ（`.tar.gz` または `.tgz`）](https://ja.wikipedia.org/wiki/tar "wikilink") が使用される。 それはファイルデータとメタデータが[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")で圧縮される1つの単位として圧縮される。この手法の欠点はランダムアクセスの効率が悪くなってしまうことである。

### ZIPと他のファイルフォーマットとの組み合わせ

ZIPファイルフォーマットでは、セントラルディレクトリの後（ファイルの末尾）に、65,535バイト以下のデータを入れることのできるコメント欄がある\[16\]。また、セントラルディレクトリがアーカイブ内の各ファイルの開始位置を表すオフセットを指定しているため、最初のエントリがオフセットゼロの位置から開始していなくてもよい。（gzipのようないくつかのツールでは、ファイルエントリがオフセットゼロで始まらないようなZIPファイルを処理できないが。）つまり、ZIPアーカイブの前や後に任意のデータを配置しても、ZIPアプリケーションはそのアーカイブを読み込むことができる。

この事実を利用すると、ZIPアーカイブとしても、別のフォーマットとしても扱えるようなファイルを作成することができる。ただし、別のフォーマットでは、ファイルの最初か末尾かあるいは中ほどに任意のデータを配置できる必要がある。WinZipやDotNetZipがサポートする[Self-extracting archives](https://ja.wikipedia.org/wiki/:en:Self-extracting_archives "wikilink") (SFX) はこの利点を活用している。そういったファイルはPKZIP AppNote.txtの仕様に準拠した.exeファイルであり、規格に準拠したzipツールやライブラリで読み込むことができる。

ZIPフォーマットやZIPの亜種であるJARフォーマットが持つこのような特性は、一見普通のファイルに見えるが、コンピューター内部に害を及ぼすJavaクラスを隠すことに悪用できてしまう。例えば、ウェブにアップロードされるGIFイメージがある。これは[GIFAR](https://ja.wikipedia.org/wiki/GIFAR "wikilink")と呼ばれる手法で、Facebookのようなウェブアプリケーションに対して効率的な攻撃として知られている\[17\]。

### 実装

多くのZIPツールとZIPライブラリは様々なプログラミング環境の上で利用できる。ライセンスは商用や[オープンソース](../Page/オープンソース.md "wikilink")のものがある。例えば、WinZipはWindows上で動作する有名なZIPツールである。他にも様々なプラットホームで[WinRAR](../Page/WinRAR.md "wikilink")、[IZarc](https://ja.wikipedia.org/wiki/:en:IZarc "wikilink")、[Info-ZIP](https://ja.wikipedia.org/wiki/Info-ZIP "wikilink")、[7-Zip](../Page/7-Zip.md "wikilink")、[PeaZip](https://ja.wikipedia.org/wiki/PeaZip "wikilink")やDotNetZip等が利用できる。これらのツールのいくつかはライブラリ、またはプログラミングインタフェースを持つ。

オープンソースで開発されているライブラリの例としては[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")や[Info-ZIP](https://ja.wikipedia.org/wiki/Info-ZIP "wikilink")がある。Javaでは[Java Platform, Standard Editionに標準的なzipファイルを扱う](../Page/Java_Platform,_Standard_Edition.md "wikilink") "java.util.zip" パッケージがある。Zip64Fileライブラリは特別に4GBを超える巨大なファイルをサポートして、ランダムアクセスを使用してZIPファイルを扱う。[Apache Antツールには](../Page/Apache_Ant.md "wikilink")[Apache Software Licenseでより完全なツールが実装されている](../Page/Apache_License.md "wikilink")。

.NETアプリケーションでは、.NET Framework 4.5で追加されたSystem.IO.Compression名前空間のZipArchiveクラスやZipFileクラスなどが使用できる\[18\]。それ以前の場合、Microsoft Public License \[19\] でソースとバイナリが利用できる DotNetZip\[20\]と呼ばれる無償のオープンソースライブラリがある。従来のパスワードを用いたZIP暗号化、WinZip互換のAES暗号化、ユニコード、ZIP64、コメント、分割アーカイブ、自己展開アーカイブといった多くのZIP機能をサポートする。[Microsoft .NET 3.5](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") ランタイムライブラリはZIPフォーマットをサポートするクラスSystem.IO.Packaging.Package\[21\]を含む。主として[ISO](https://ja.wikipedia.org/wiki/International_Organization_for_Standardization "wikilink")/[IEC国際標準](https://ja.wikipedia.org/wiki/International_Electrotechnical_Commission "wikilink")[Open Packaging Conventionsを使用するドキュメントフォーマットのために設計されている](https://ja.wikipedia.org/wiki/:en:Open_Packaging_Conventions "wikilink")。

ZIPフォーマットの[Info-ZIP](https://ja.wikipedia.org/wiki/Info-ZIP "wikilink")実装は、ユーザやグループID、ファイルパーミッション、シンボリックリンクのようなUnixファイルシステムの機能のサポートを追加する。[Apache Antの実装はUnixパーミッションが事前に定義されたファイルを作成できる範囲に対して注意を払っている](../Page/Apache_Ant.md "wikilink")。Info-ZIPの実装もZIP圧縮フォーマットに組み込まれたエラー訂正機能の使用方法が分かっている。（[IZarcのような](https://ja.wikipedia.org/wiki/:en:IZarc "wikilink")）一部のプログラムはエラーがあるファイルの処理中に失敗する可能性がある。

また Info-ZIP Windowsツールも[NTFS](../Page/NT_File_System.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")パーミッションをサポートする。展開時にNTFSパーミッションをUnixパーミッションへ、もしくはその逆へ変換しようとする。これは潜在的な意図しない結果をもたらすことがある。例として、NTFSボリューム上で実行権限を付けて作成された[.exeファイルは拒否されることなどが挙げられる](../Page/EXEフォーマット.md "wikilink")。

## Windows 圧縮フォルダー

Windowsでは、Windows 98のためにリリースされたPlus\!パック以降、エクスプローラーからZIP形式の圧縮と展開をサポートしている。マイクロソフトはこの機能を「圧縮フォルダー」と呼んでいる。圧縮フォルダーはZIPの機能を全てサポートしているわけではなく、例えばWindows 10ではAES暗号化、分割アーカイブ、パスワードを付き圧縮などが行えない。また圧縮時にはシステムロケールが日本語に設定されたWindowsではファイル名に[Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")を使用している。（[Windows NT系の内部文字コード及びファイルシステムの文字コードは](../Page/Windows_NT系.md "wikilink")[Unicode](../Page/Unicode.md "wikilink")であるが、互換性のために[Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")に変換している。変換できない文字が含まれるファイル名は圧縮できない。）展開時はhotfix\[22\]を適用したWindows 7もしくはWindows 8以降で[UTF-8](../Page/UTF-8.md "wikilink")に対応したため、ファイル名が[Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")と[UTF-8](../Page/UTF-8.md "wikilink")のどちらであっても問題なく展開できる。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のFinderでは原則として圧縮・展開ともに[UTF-8](../Page/UTF-8.md "wikilink")を想定しているため、macOSで作成したZIPファイルはhotfixを適用したWindows 7以降であればで問題なく展開できるが、逆にWindowsで作成したZIPファイルをmacOSで展開するとファイル名によっては文字化けもしくはエラーとなる。（これはファイル名の話でファイルの内容には影響しない。）

## 強力な暗号化についての議論

2003年に [WinZip](../Page/WinZip.md "wikilink") 9.0パブリックベータをリリースしたとき、WinZipは独自の[AES-256暗号を導入した](../Page/Advanced_Encryption_Standard.md "wikilink")。それは違うファイルフォーマットを用いた新たな仕様としてドキュメントに記載された\[23\]。暗号の標準規格は [プロプライエタリ](../Page/プロプライエタリ・ソフトウェア.md "wikilink") では無いが、 PKWARE は2001年以降、PKZIP 5.0や6.0では使用されていた強力な暗号化仕様 (SES) を含めるようにAPPNOTE.TXTを更新しなかった。WinZipの[技術コンサルタント](https://ja.wikipedia.org/wiki/技術コンサルタント "wikilink") Kevin Kearneyや[スタッフイット](../Page/StuffIt.md "wikilink") プロダクトマネージャ Mathew CovingtonはSESを差し控えるようにPKWAREを非難。これに対し、PKZIPチーフ技術オフィサーのJim Petersonは承認に基づく暗号化規格はまだ完全ではないと主張。しかし、バージョン 4.5の頃（PKWARE の FTP サイトで確認できる）に公開された最新のAPPNOTE.TXTには、SESだけではなく、同時期に存在したPKZIPプロダクトで作成された.ZIPファイルが用いたDeflate64、DCL Implode、BZip2も除外された。

この欠点を克服するために[PentaZip](https://ja.wikipedia.org/wiki/PentaZip "wikilink")のような同時期に存在したプロダクトは違うファイルフォーマットにZIPアーカイブを暗号化する強力なZIP暗号化を実装した\[24\]。

また別の議論では、PKWAREは2003年7月16日に安全な.ZIPファイルを作成するために強力な暗号と.ZIPを組み合わせるための方法を記載した特許を適用した\[25\]。

結局PKWAREとWinZipはお互いのプロダクトをサポートすることに同意した。2004年1月21日にPKWAREはWinZipベースのAES互換フォーマットをサポートするとアナウンスした\[26\]。WinZipベータの次のバージョンではSESベースのZIPファイルのサポートが行われた\[27\]。PKWAREは最終的にSESを記載した.ZIPファイルフォーマット仕様のバージョン 5.2を公式にリリースした。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink") プロジェクト [7-Zip](../Page/7-Zip.md "wikilink")も（その[POSIX](../Page/POSIX.md "wikilink") [移植された](../Page/移植_\(ソフトウェア\).md "wikilink") [p7zip](https://ja.wikipedia.org/wiki/:en:p7zip "wikilink") が行うことで）ZIPファイルのAESをサポートしている。

## ソフトにおける固有の拡張子

[アプリケーション固有のファイル形式のなかには](../Page/アプリケーションソフトウェア.md "wikilink")、あるファイルを一定の[ディレクトリ](../Page/ディレクトリ.md "wikilink")の[階層構造](../Page/階層構造.md "wikilink")に格納しZIP形式で圧縮したものが存在する。そのようなファイルの大半はそのアプリケーション固有の物であることを示すために専用の拡張子を定義しており、以下に示す例はその一部である。ただし、圧縮アルゴリズムにzlibを使っているものでも、ZIP互換の格納方式を使っていないものは掲載しない。

  - [apk](https://ja.wikipedia.org/wiki/APK_\(ファイル形式\) "wikilink")
    [Android](../Page/Android.md "wikilink") のアプリケーションアーカイブ
  - crx
    [Google Chromeや](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")[Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")の[拡張機能](https://ja.wikipedia.org/wiki/拡張機能 "wikilink")のアーカイブファイル
  - [docx, xlsx, pptx](../Page/Office_Open_XML.md "wikilink")
    [Microsoft Office 2007で新たに採用された文書フォーマット](../Page/Microsoft_Office.md "wikilink") ([Office Open XML](../Page/Office_Open_XML.md "wikilink"))
  - [epub](https://ja.wikipedia.org/wiki/EPUB "wikilink")
    [IDPF](https://ja.wikipedia.org/wiki/IDPF "wikilink")が提唱する[電子書籍](../Page/電子書籍.md "wikilink")の標準フォーマット
  - [ipa](https://ja.wikipedia.org/wiki/IPA_\(ファイルフォーマット\) "wikilink")
    [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")シリーズをはじめとした[iOS搭載デバイス向けのアプリケーションアーカイブ](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")
  - ipg
    [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")ゲームのアーカイブファイル
  - [jar](https://ja.wikipedia.org/wiki/jar "wikilink")
    [Java](https://ja.wikipedia.org/wiki/Java "wikilink")のアーカイブファイル
  - kmz
    [Google Earthの標準ファイル形式](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")。[kml](https://ja.wikipedia.org/wiki/kml "wikilink")をZIP圧縮したもの。
  - nar
    [伺か](../Page/伺か.md "wikilink")のINSTALL/1.x仕様に準拠したアーカイブファイル
  - [odt, ods, odp, odb, odg, odf](../Page/OpenDocument.md "wikilink")
    [OpenDocument](../Page/OpenDocument.md "wikilink")の文書フォーマット
  - smzip
    [StepMania](../Page/StepMania.md "wikilink")の各種の自動インストール型パッケージファイル
  - wgt
    [W3C Packaged Web Apps](https://ja.wikipedia.org/wiki/W3C_Packaged_Web_Apps "wikilink") (W3C Widgets) のパッケージファイル。[Bada](https://ja.wikipedia.org/wiki/Bada "wikilink") widget、[Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink") Web application、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") widget など。
  - wsz
    [Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")用のスキンファイル
  - wmz
    [Windows Media Player用のスキンファイル](../Page/Windows_Media_Player.md "wikilink")
  - xpi
    [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")（及びそれをベースとする[Netscapeシリーズ](../Page/Netscapeシリーズ.md "wikilink")のウェブブラウザなど）や[Mozilla Thunderbirdなどの](../Page/Mozilla_Thunderbird.md "wikilink")[拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")（アドオン）のインストーラファイル ([XPInstall](../Page/XPInstall.md "wikilink"))

## 脚注

### 注釈

### 出典

## 関連項目

## 外部リンク

  - RFC 1950 (zlib)
  - RFC 1951 (Deflate)

<!-- end list -->

  - [Judgment in favor of SEA in *SEA v. PKWARE and Phil Katz*](http://www.bbsdocumentary.com/library/CONTROVERSY/LAWSUITS/SEA/judgment.txt)
  - [Current file format specification from PKWARE (including many recent features that are not widely supported)](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
  - [Comparison of the performances of various methods of data compression (french)](http://rlwpx.free.fr/WPFF/comploc.htm)
  - [ZIP2 file format specification](http://www.dlugosz.com/ZIP2/index.html)
  - [Zip Files All The Way Down](https://research.swtch.com/zip)
  - [ZIP File Quine](https://alf.nu/ZipQuine)
  - [Limitations of `java.util.zip`](https://www.mindprod.com/jgloss/zip.html#GOTCHAS)

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.
2.
3.
4.
5.
6.  <http://www.itscj.ipsj.or.jp/sc34/open/1414.pdf>
7.  <http://www.pkware.com/documents/casestudies/APPNOTE.TXT>
8.
9.
10.
11.
12. Stay, Michael. "ZIP Attacks with Reduced Known Plaintext". <http://math.ucr.edu/~mike/zipattacks.pdf>
13. [AES Encryption Information: Encryption Specification AE-1 and AE-2](http://www.winzip.com/aes_info.htm)
14. [Application Note on the .ZIP file format](http://www.pkware.com/index.php?option=com_content&task=view&id=64&Itemid=107)
15.
16.
17. [A photo that can steal your online credentials](http://www.infoworld.com/article/08/08/01/A_photo_that_can_steal_your_online_credentials_1.html)
18.
19. <http://www.codeplex.com/DotNetZip/license>
20. <http://www.codeplex.com/DotNetZip>
21. <http://msdn.microsoft.com/en-us/library/system.io.packaging.package.aspx>
22. [File names are corrupted after you decompress a .zip file in Windows 7 or in Windows Server 2008 R2](http://support.microsoft.com/kb/2704299/en-us)
23. [WinZip - AES Encryption Information](http://www.winzip.com/aes_info.htm)
24. [The .zip standard splinters | InfoWorld | News | 2003-06-10 | By Lincoln Spector, PC World.com](http://www.infoworld.com/article/03/06/10/HNzipsplinters_1.html)
25. [PKWare seeks patent for .zip file format | InfoWorld | News | 2003-07-25 | By Robert McMillan, IDG News Service](http://www.infoworld.com/article/03/07/25/HNpkware_1.html)
26. [Software makers patch Zip tiff - CNET News.com](http://www.news.com/2100-1012_3-5145491.html?tag=fd_nbs_ent)
27. <http://www.theregister.co.uk/2004/01/21/zip_file_encryption_compromise_thrashed/>