> この記事は[Mac](https://ja.wikipedia.org/wiki/Mac)から翻訳されています。


**Macバイナリ** (MacBinary) は[Classic Mac OSの](../Page/Classic_Mac_OS.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")中のファイルを、そのマルチフォーク（データフォークと[リソースフォーク](https://ja.wikipedia.org/wiki/リソースフォーク "wikilink")）とメタデータ（[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")）を全て含んだバイナリファイルにまとめる形式（フォーマット）のひとつ。かつては7ビットテキスト転送用の[BinHex](https://ja.wikipedia.org/wiki/BinHex "wikilink")と並んで[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上でも多用されたが、現在はあまり使われなくなってきている。

## 概要

Mac OSのファイルシステムでは、一般的なファイルシステムにおける「ファイルの中身」に相当する「データフォーク」の他、[リソースフォーク](https://ja.wikipedia.org/wiki/リソースフォーク "wikilink")という二つの[フォークがある](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")。またその他に、生成時刻などが含まれた[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")\[1\]である[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")がある。Finder情報には[クリエータとファイルタイプ](https://ja.wikipedia.org/wiki/Finder "wikilink")、Finderフラグ、ウインドウ位置等が含まれている。データフォークがない場合やリソースフォークがない場合(サイズがゼロ)もある。

パソコン通信の時代において、Ward Christensenによる[XMODEM](../Page/XMODEM.md "wikilink")やMODEM7、[Kermit](https://ja.wikipedia.org/wiki/カーミット_\(プロトコル\) "wikilink")、[CompuServe](https://ja.wikipedia.org/wiki/CompuServe "wikilink")でのAやBといったプロトコルで転送する事を仮定していた。日本でも[パソコン通信](../Page/パソコン通信.md "wikilink")等で多用された。これらには128[バイト単位でデータを転送するものがあるため](../Page/バイト_\(情報\).md "wikilink")、MacBinaryも128バイト単位で扱えるような工夫がされている。

以下は余談であるが、利用形態としては、送信元の端末がMacBinaryフォーマットで転送し、転送先の端末がそれを展開してローカルのファイルシステムに保存するような方法を想定していた。実際には[拡張子](../Page/拡張子.md "wikilink").binを付けたMacBinaryフォーマットのファイルに保存し、パソコン通信のサイトに置いたり電子メールで送信する方法も取られた。この場合は受信後に対応ソフトで展開した。

その後、[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")（当時）による[HFSの仕様拡張にあわせて](https://ja.wikipedia.org/wiki/Hierarchical_File_System "wikilink")、**MacBinary II**、**MacBinary III**が公開されている。

現在の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[HFS+ではMacBinary](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink") IIIでも不十分であるため、あまり使われなくなっている。

## フォーマットの遍歴

最初の**MacBinary**は、1985年にMacBinary Working Groupによって公開された。 先頭の128バイト (MacBinary Header) 内にファイル名、Finder情報、ファイル作成時刻、ファイル更新時刻等を詰め込み、その後にデータフォーク、リソースフォークが続くフォーマットである。データフォークとリソースフォークはパディングして128バイト単位で格納する。ファイル名は63バイト迄扱う事が出来たが、当時のClassic Mac OSには31バイト制限があったので必要以上であった。日本語環境ではファイル名は[MacJapanese](https://ja.wikipedia.org/wiki/MacJapanese "wikilink")で保管される。 この時点ではClassic Mac OSのファイルを8ビットで転送するためには十分なフォーマットであった。

7ビット経路でASCIIに変換して転送する方式としては[BinHex](https://ja.wikipedia.org/wiki/BinHex "wikilink")があり、MacBinaryとBinHexのどちらかを使えば十分であった。

**MacBinary II**は1987年にMacBinary II Conferenceで合意された。先頭128バイトの未使用だった領域に拡張されたFinderフラグを格納するようにし、更にリソースフォークの後にコメントを追加出来るように改良された。

**MacBinary III**は1997年に発行された。1996年11月にアップルが公開した[Mac OS 8の拡張Finder情報を先頭](https://ja.wikipedia.org/wiki/Mac_OS_8 "wikilink")128バイトの未使用領域に格納出来るようにしたものである。ファイル名の長さは31バイト以内でなければならないと明確化されたが、これは当時のClassic Mac OSと同じ制限であるため妥当であった。 このとき既にアップルコンピュータにより[AppleSingle](https://ja.wikipedia.org/wiki/AppleSingle "wikilink")の仕様が公開されていたが普及に至らなかったため、既に浸透しているMacBinaryを拡張したわけである。

## 問題点

日本製の[MacLHAという](../Page/LHA.md "wikilink")[アーカイバでは](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")、ファイルをMacBinaryフォーマットにしてから[LHA](../Page/LHA.md "wikilink")書庫に格納するという手法を取った。これを考慮しないLHA用ソフトで展開した場合、拡張子.binの付かないMacBinaryフォーマットのファイルが出力されてしまう。

MacBinaryフォーマットのファイルは拡張子.binを付けるのが一般的であるため、ユーザはこれを展開することで本来のファイルを得ることが出来る。しかし、拡張子.binを付けず元のファイル名のままで保存されるケースもある。前述のMacLHAもこのケースに当たる。こうした場合、ユーザはMacBinaryである事に気付かず、そのままアプリケーションで開こうとしてしまう。アプリケーションによってはMacBinaryであることを自動判別して先頭128バイトを読み飛ばしてデータフォークのみを読み取るが、通常のアプリケーションではエラーになってしまう。

MacBinaryを解除するソフトウェアが多数あったが、中には先頭128バイトのMacBinary Headerを取り除くだけのものがあった。この処理法だとデータフォークの後のパディングが残っており、更にその後にリソースフォークとコメントも残ったままになるため、正しい処理とは言えない。

データフォークのみを取り出して保存するソフトウェアも多数あった。また、データフォークの他にリソースフォークを別ファイルとして保存するソフトウェアも多数あった。処理方法としてこれらは正しいと言える。しかしながら、元々リソースフォークが重要なファイルであった場合、Classic Mac OS以外のOSでは正常に扱う事が出来ない。これはMacBinaryの問題というよりも、Classic Mac OSと他のOSとの間の互換性の問題と言える。

単にClassic Mac OS間でファイルの交換するという目的では、データフォークのみを取り出す必要はなく、如何にして全ての情報を転送出来るかが問題となる。この意味では[Compact Pro](https://ja.wikipedia.org/wiki/Compact_Pro "wikilink")、[StuffIt](https://ja.wikipedia.org/wiki/StuffIt "wikilink")、MacLHAといったアーカイバが有用であった。

MacBinaryではファイル名の長さは63バイト或は31バイト迄表現出来るが、現在のmacOSの[HFS+では更に長いファイル名を](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink")[Unicode](../Page/Unicode.md "wikilink")で扱っており、更に多くのメタ情報が追加されているため、たとえ最新のMacBinary IIIでも不十分である。この問題の打開策としては、アップルコンピュータが自ら作った[AppleSingle](https://ja.wikipedia.org/wiki/AppleSingle "wikilink")やAppleDoubleがある。これらはUnicodeファイル名や各種メタデータを取り扱う事が出来る。ただしAppleSingleは単一のファイルなので対応ソフトが必要となる。AppleDoubleはその名前が示す通りClassic Mac OS固有のデータとデータフォークの2つのファイルにわけてやりとりする方法なので、Classic Mac OS以外のOSではデータフォークのみを扱う事が出来る。

現在のmacOSでは、AppleDoubleをtarやzipでアーカイブしたり、HFS+をそのままイメージ化したdmgフォーマット等も使われている。

## 脚注

### 注釈

### 出典

## 関連項目

  - [AppleSingle](https://ja.wikipedia.org/wiki/AppleSingle "wikilink")
  - [AppleDouble](https://ja.wikipedia.org/wiki/AppleDouble "wikilink")
  - [BinHex](https://ja.wikipedia.org/wiki/BinHex "wikilink")
  - [リソースフォーク](https://ja.wikipedia.org/wiki/リソースフォーク "wikilink")

## 外部リンク

  - [MacBinarySpecs - theunarchiver - Mirror of the three MacBinary specs - Project Hosting on Google Code](http://code.google.com/p/theunarchiver/wiki/MacBinarySpecs)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:Classic_Mac_OS](https://ja.wikipedia.org/wiki/Category:Classic_Mac_OS "wikilink")

1.  マルチフォークと違い、ファイルに関してそのようなメタデータがあることは、他のOSのファイルシステムでも普通のことである。