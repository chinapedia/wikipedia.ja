> この記事は[AppleSingle](https://ja.wikipedia.org/wiki/AppleSingle)から翻訳されています。


**AppleSingle**と**AppleDouble**は、[Mac OSのファイルシステム](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[HFS及び](../Page/Hierarchical_File_System.md "wikilink")[HFS+上のファイルを他の](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")と交換する際に、様々なファイル属性(特に[リソースフォーク](../Page/リソースフォーク.md "wikilink"))が欠落するのを防ぐ目的で[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")（当時）が考案したフォーマットである。バージョン1とバージョン2が存在するが、現在の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")は互換性のない拡張をおこなったバージョン2のAppleDoubleを用いる。

## 概要

Mac OSではひとつのファイルに、[データフォーク](../Page/リソースフォーク.md "wikilink")、[リソースフォーク](../Page/リソースフォーク.md "wikilink")という2つの[フォークがあり](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")、更に様々な[メタデータ](../Page/メタデータ.md "wikilink")(コメント、ファイル時刻、[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")等)がある。特にファイル時刻には作成時刻、変更時刻、バックアップ時刻、アクセス時刻がある。Finder情報は[クリエータとファイルタイプを含んでいる](../Page/Finder.md "wikilink")。

これらを扱えるのはHFSやHFS+といったファイルシステムやファイル共有プロトコルの[AFPしかない](../Page/Apple_Filing_Protocol.md "wikilink")。それ以外のファイルシステムではデータフォーク程度しか扱えない。

**AppleSingle**は2つのフォークと様々なメタデータを1つのファイルにまとめて保存するフォーマットである。

**AppleDouble**は2つのファイルに分離して保存するフォーマットである。1つ目はAppleDouble Data fileといい、データフォークそのものである。2つ目はAppleDouble Header fileといい、データフォーク以外を全て含む。これはAppleSingleからデータフォークを除き、[マジックナンバーを変えただけのものである](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")。

## 利点と欠点

Mac OSではデータフォーク以外の情報が必要とされる場合があるため、AppleSingleまたはAppleDoubleで転送及び保存することには大きな利点がある。

Mac OS以外では事情が複雑である。AppleSingleの場合、ファイルが1つであるため情報の欠落がない。しかしながら、AppleSingleを理解するソフトウェアでなければ取り扱う事が出来ない。AppleDoubleの場合、AppleDouble Data fileの方でデータフォークを扱うことが出来る。しかしながら運用に注意しなければAppleDouble Header fileを損失してしまう危惧がある。

## 歴史

初期のバージョン1は、AppleComputer社(当時)の最初の[UNIX系OSである](../Page/Unix系.md "wikilink")[A/UX](https://ja.wikipedia.org/wiki/A/UX "wikilink")上のファイルシステムで使うために考案された\[1\]。

AppleSingleと似たフォーマットに[Macバイナリ](../Page/Macバイナリ.md "wikilink")があり、当時はこちらの方が多用された。しかしながらHFS+の拡張に伴い、Macバイナリでは不十分になってきた。

バージョン2はHFS+の拡張にあわせて[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に発行された\[2\]。

[2005年](../Page/2005年.md "wikilink")に発売された[Mac OS X v10.4以降では](../Page/Mac_OS_X_v10.4.md "wikilink")、バージョン2を拡張し互換性のなくなったAppleDoubleを用いる。これの仕様書は発行されていないが、アップルの公開する[カーネル](../Page/カーネル.md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")で仕様を知ることができる\[3\]。

## 実装例

### macOS

macOSがHFS、HFS+、AFP以外のファイルシステム、すなわち[UFS](../Page/Unix_File_System.md "wikilink")、[FAT](../Page/File_Allocation_Table.md "wikilink")、[SMB](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink")、[NFS](../Page/Network_File_System.md "wikilink")、[WebDAV](../Page/WebDAV.md "wikilink")といったファイルシステムにファイルを保存する際、AppleDouble バージョン2を用いる。すなわちAppleDouble Data file (データフォーク)を本来のファイル名で保存し、AppleDouble Header fileを「._」を先頭に付けたファイル名で保存する\[4\]。

[Mac OS X v10.3 Panther以降のFinderの機能](../Page/Mac_OS_X_v10.3.md "wikilink")(BOMArchiveHelper)で[ZIP圧縮した場合](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、__MACOSXという名前のフォルダを作ってその中にAppleDouble Header fileを保存する。ただしコマンドラインの/usr/bin/zipだとデータフォークのみが扱われる。

[Mac OS X v10.4 Tiger以降の](../Page/Mac_OS_X_v10.4.md "wikilink")/usr/bin/tarコマンドでは、AppleDouble Header fileを「._」を先頭に付けたファイル名で保存する。また、このバージョン以降は[拡張属性 (EA)を使うことができるため](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink")、AppleDouble バージョン2を拡張してEAも保存できるようになった。これは本来32バイトである[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")の保存領域を拡張し、Finder情報の後ろにEAを追加記録するというものである。これにより従来のバージョン2と互換性がない。

[Mac OS X v10.5迄は](../Page/Mac_OS_X_v10.5.md "wikilink")、拡張属性をサポートしない[AFPサーバにファイルを保存すると拡張属性が失われた](../Page/Apple_Filing_Protocol.md "wikilink")。[Mac OS X v10.6では](../Page/Mac_OS_X_v10.6.md "wikilink")、こうしたサーバに保存する際、先頭に「._」を付けたファイル名でバージョン2のファイルをつくり、これに拡張属性を格納する。

### 電子メール

RFC 1740 では、主に[電子メール](../Page/電子メール.md "wikilink")で使われるフォーマット[MIMEでAppleSingle及びAppleDouble](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink") バージョン2を扱う方法を定義している。これはMac OS用の[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")の多くで実装されている。

AppleSingleの[MIMEタイプはapplication](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")/applefileを用いる。AppleDoubleの場合、MIMEタイプはmultipart/appledoubleを用いてマルチパート化し、AppleDouble Headerの方にapplication/applefileを用いる。 Mac同士でメールをやりとりする分にはなんら問題は生じないが、ほかの[OSを相手にするとデータフォーク以外が邪魔になって本来のデータが得られなくなってしまう場合が多い](../Page/オペレーティングシステム.md "wikilink")。そのため、Mac以外とやりとりする際はデータフォークのみを送信するか、multipart/appledoubleを用いるのが望ましいだろう。

### netatalk

[Unix系](../Page/Unix系.md "wikilink")OSでAFPサーバ機能を提供する[netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")では、AppleDoubleを用いている。 netatalk 1.xでは、AppleDouble Data file（データフォーク）を本来のファイル名で保存し、.AppleDoubleなるディレクトリを作成してその中に同じファイル名でバージョン1のAppleDouble Header fileを保存する。netatalk 2.xではこれをバージョン2のAppleDouble Header fileにおきかえた。netatalk 3.xでは[拡張属性の中にAppleDouble](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink") Header fileのデータを保存するが、[リソースフォーク](../Page/リソースフォーク.md "wikilink")が拡張属性に入りきらない場合は別途「._」を前置したファイル名で保存する。

## 参照

<references/>

## 関連項目

  - [Macバイナリ](../Page/Macバイナリ.md "wikilink")
  - [BinHex](../Page/BinHex.md "wikilink")

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [AppleSingle and AppleDouble format internals](http://kaiser-edv.de/documents/Applesingle_AppleDouble_v1.html)
2.  [AppleSingle/AppleDouble Formats for Foreign Files Developer's Note (pdf)](http://kaiser-edv.de/documents/AppleSingle_AppleDouble.pdf)
3.  [カーネルxnu-792に含まれるvfs_xattr.cのソースコード](http://opensource.apple.com/source/xnu/xnu-792/bsd/vfs/vfs_xattr.c)
4.  [Mac OS X: Apple Double フォーマットは接頭辞に「._ 」を持つファイル名を作成します](http://docs.info.apple.com/article.html?artnum=106510-ja)