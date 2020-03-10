> この記事は[COFF](https://ja.wikipedia.org/wiki/COFF)から翻訳されています。


**COFF** (Common Object File Format) は[Unixシステムで用いられる](../Page/UNIX.md "wikilink")[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")、[オブジェクトファイル](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")、[共有ライブラリ](https://ja.wikipedia.org/wiki/共有ライブラリ "wikilink")の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")仕様である。[Unix System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") で導入され、[SVR4で導入された](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[ELFによって広く置き換えられる前に](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、[XCOFFや](https://ja.wikipedia.org/wiki/:en:XCOFF "wikilink")[ECOFFなどの拡張仕様の基礎を形作った](https://ja.wikipedia.org/wiki/:en:ECOFF "wikilink")。COFFとその派生種はその後も[Unixライクシステムや](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[Microsoft Windows上で使われ続けている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 歴史

元々のUnixのオブジェクトファイルフォーマット[a.outは非常に単純な設計であり](https://ja.wikipedia.org/wiki/A.outフォーマット "wikilink")、たとえば シンボリック[デバッグ](../Page/デバッグ.md "wikilink")情報や[共有ライブラリなどを十分にサポートすることができなかった](../Page/ライブラリ.md "wikilink")。AT\&Tの内外でUnixライクシステムの開発が進むにつれ、これらの問題への別の解決策や、異なる問題が生じ始めた。

COFFは[AT\&T](../Page/AT&T.md "wikilink")のVAX以外の32bitプラットフォーム向けの[UNIX System Vで導入された](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")。既存のAT\&Tの*a.out*フォーマットに対する改善点として、COFFは元からシンボリックデバッグ情報や共有ライブラリ、拡張の機構をサポートしていた。

しかし、COFFは*a.out*の改善版であると同時に、その設計にも制限があった。セクションの最大数や、セクション名の長さ、シンボリックデバッグ情報を[C++](../Page/C++.md "wikilink")のような新しい言語でサポートすることができない、などの制約があった。SVR4のリリースとともに、AT\&TはCOFFを[ELFで置き換えた](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")。[IBM](../Page/IBM.md "wikilink")は[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")でXCOFFフォーマットを使用し、[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[SGIなどの会社はECOFFを使用した](../Page/シリコングラフィックス.md "wikilink")。それ以外のシステムは互換性のない方法でそれぞれ実行ファイルのフォーマットを拡張してこれらの問題点を克服した。

拡張されたCOFFはいくつかのUnixライクなプラットフォームで使用され続け、まずは組み込みシステムにおいて、そしておそらく今日でもっとも広く普及したCOFFの用途は[Microsoftの](../Page/マイクロソフト.md "wikilink")[Portable Executable](https://ja.wikipedia.org/wiki/Portable_Executable "wikilink") (PE) フォーマットである。

[Windows NTのために開発されたPEフォーマット](../Page/Microsoft_Windows_NT.md "wikilink")（PE/COFF と表記されることもある） \[1\]は、オブジェクトファイルに COFF ヘッダを使用し、実行ファイル内のPEヘッダのコンポーネントとして使用する。\[2\]

## 特徴

COFFの*a.out*に対する主要な改善点はオブジェクトファイル内に名前のついた複数の*[セクション](https://ja.wikipedia.org/wiki/:en:section "wikilink")*を導入したことであった。オブジェクトファイルはそれぞれ異なる数と種類のセクションを持つことができた。

### シンボリックデバッグ情報

COFFのシンボリックデバッグ情報は、プログラムの関数と変数の（文字による）シンボル名称と、実行のトレースや[ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")の設定に用いられる行番号情報からなっている。*a.out*は元々シンボリックデバッグ情報をサポートしていないが、スタブのような機構を用いることでこの欠点をある程度は克服することができた。

シンボル名称はCOFFのシンボルテーブルに格納される。シンボルテーブルの各エントリーには名前、記憶クラス、型、値およびセクション番号が含まれる。短い名前（8文字以下）はシンボルテーブルに直接格納され、長い名前はCOFFオブジェクトの末端にある文字列テーブルに対するオフセットとして格納される。

記憶クラスは外部変数(C_EXT)、自動（スタック）変数(C_AUTO)、レジスタ変数(C_REG)、関数(C_FCN)などのシンボルが表現する型の実体を示す。シンボルの種類はシンボルの実体の値を説明するもので、すべての[C言語](../Page/C言語.md "wikilink")のデータ型を含んでいる。

適切なオプションとともにコンパイルされた場合、COFFオブジェクトファイルはオブジェクトファイルのテキストセクションのとりうる各ブレークポイントの行番号情報を格納する。行番号情報は二つの形態をとる。一番目の形態では、コード内のとりうる各ブレークポイントについて、行番号のエントリーがアドレスと対応する行番号を格納する。二番目の形態では、関数の開始を示すシンボルテーブルのエントリーを識別し、関数の名前でブレークポイントを有効にする。

### 相対仮想アドレス

COFFファイルが生成される際には、通常ファイルがメモリのどこにロードされるかは不明である。ファイルの最初のバイトがロードされた[仮想アドレスは](../Page/仮想記憶.md "wikilink")、イメージ[ベースアドレス](https://ja.wikipedia.org/wiki/ベースアドレス "wikilink")と呼ばれる。ファイルの残りは必ずしも連続した領域にロードされる必要はなく、異なる**セクション**にロードされる。

相対仮想アドレス(RVA)は、標準的な仮想アドレスと混同してはならない。**相対仮想アドレス**はメモリにロードされたオブジェクトの[仮想アドレスから](../Page/仮想記憶.md "wikilink")、ファイルイメージのベースアドレスを引いたものである。仮にファイルが文字通りディスクからメモリに（そのまま）割り当てられると、RVAはファイルについてのオフセットと同一になるが、実際にはそのようなことはめったにない。

RVAという用語はイメージファイル内のオブジェクトについてのみ用いられる。メモリにロードされると、イメージのベースアドレスが加算され、通常の仮想アドレスとなって使用される。

## 脚注

<references/>

## 参考文献

  - [DJGPP COFF Spec](http://delorie.com/djgpp/doc/coff/)

  -
<!-- end list -->

  -
[Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")

1.  [1](http://support.microsoft.com/?id=121460)
2.