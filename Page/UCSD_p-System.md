> この記事は[UCSD p-System](https://ja.wikipedia.org/wiki/UCSD_p-System)から翻訳されています。


**UCSD p-System** または **UCSD Pascal System** とは、[UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") に基づいた移植性の高い[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、[カリフォルニア大学サンディエゴ校](../Page/カリフォルニア大学サンディエゴ校.md "wikilink")（UCSD）で開発された。

## 概要

UCSD p-System は、[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")から学内の[DEC製](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink") [PDP-11](../Page/PDP-11.md "wikilink") まで共通の[OSを学生が使えるようにすることを目的としていた](../Page/オペレーティングシステム.md "wikilink")。SofTech 製の Version VI は、[IBM](../Page/IBM.md "wikilink") がオリジナルの [IBM PC](../Page/IBM_PC.md "wikilink") 用OSとして提供した3つのOS（他は [PC-DOS](https://ja.wikipedia.org/wiki/PC-DOS "wikilink") と [CP/M-86](https://ja.wikipedia.org/wiki/CP/M-86 "wikilink")）の1つである。しかし、p-System 向けのアプリケーションが少なく、価格も他より高めだったため、あまり売れなかった。それ以前には、IBM は[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink")専用機 Displaywriter の OS として UCSD p-System を採用していた。

[1977年](../Page/1977年.md "wikilink")ごろ、UCSD の Kenneth Bowles は、コンピュータの新機種の数が多くなり、新しい[プログラミング言語](../Page/プログラミング言語.md "wikilink")が受け入れられにくくなる（処理系の移植が追いつかなくなる）と考え、UCSD p-System の開発を開始した。彼はプログラミングの教育用として [Pascal](../Page/Pascal.md "wikilink") に注目していた。UCSD は Pascal に重要な2つの改良を施した。それは、可変長文字列と個別にコンパイル可能なコードの単位（ユニット）である（これは当時新たに登場した [Ada](../Page/Ada.md "wikilink") から発想された）。[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")は p-System と UCSD Pascal が Pascal の普及に貢献するとして支持した。UCSD Pascal が Pascal ユーザーの間で最も人気があったのは [Turbo Pascal](../Page/Turbo_Pascal.md "wikilink") がリリースされるまでだった。

UCSD p-System は *p-Machine*（pseudo-machine）と呼ばれる[仮想機械](../Page/仮想機械.md "wikilink")によってハードウェアからの独立性を保っている。[Pコードと呼ばれる](../Page/Pコードマシン.md "wikilink")[命令セット](../Page/命令セット.md "wikilink")を持つ。[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")の教え子 Urs Ammann が博士論文 *On Code Generation in a Pascal Compiler*（1977年）で最初のPコードを発表した。このPコードは Pascal 向けに最適化されており、初期の開発は全て [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") で行われた。各ハードウェアプラットフォームにはPコードの[インタプリタ](../Page/インタプリタ.md "wikilink")さえあれば、p-System全体を動作させることが可能だった。その後のバージョンでは、Pascal 以外の言語もPコードにコンパイルされる処理系を実装した。例えば、TeleSoft はPコードを生成する Ada 処理系を開発した。これは、（[MC68000](../Page/MC68000.md "wikilink")から[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")まで）様々なプラットフォームで動作した。

UCSD p-System の考え方は、[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")と同じである。どちらも仮想機械(VM)を使ってOSやハードウェアの違いを隠蔽し、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")サポートのためにそのVM向けに書かれたプログラムを使用する。また、どちらのシステムもVMを[OSとして扱うこともできるし](../Page/オペレーティングシステム.md "wikilink")、別のOS上で動作するボックスとしても扱える。

## バージョン

UCSD Pコード・エンジンには4つのバージョンがあり、それぞれに p-System と UCSD Pascal のいくつかのバージョンが対応している。Pコード・エンジンのバージョンが変わるということは、Pコードの仕様が変わるということであり、バージョンの異なる p-Machine 向けのコードは実行できなくなる。Pコード・エンジンのバージョンはローマ数字で表され、p-System のバージョンはローマ数字（対応するエンジンのバージョン）にドット付きでアラビア数字を付けたものになっていた。例えば、II.3 は p-Machine 第2版で動作する p-System 第3版を意味する。

  - Version I
    最初の版であり、公式には UCSD 以外には配布されなかった。しかし、I.3 と I.5 の Pascal のソースコードは自由にユーザー間で交換されていた。特にパッチをあてた I.5a は安定していることで知られていた。
  - Version II
    各種[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")向けに広く配布された。対象プラットフォームは、[Apple II](../Page/Apple_II.md "wikilink")、[PDP-11](../Page/PDP-11.md "wikilink")、[Z80](../Page/Z80.md "wikilink") と [MOS 6502](../Page/MOS_6502.md "wikilink") を使ったマシン、[MC68000](../Page/MC68000.md "wikilink")、[IBM PC](../Page/IBM_PC.md "wikilink") などである。PC 向けはコードセグメントが 64KB、スタック/ヒープも含めたデータセグメントが 64KB に制限されていた。Version VI ではこの制限がなくなったが、価格が上がった。
  - Version III
    [ウェスタン・デジタル](https://ja.wikipedia.org/wiki/ウェスタン・デジタル "wikilink")の [Pascal MicroEngine](https://ja.wikipedia.org/wiki/Pascal_MicroEngine "wikilink") 向け専用のバージョン。
  - Version IV
    商用版。SofTech が開発・販売を行った。Version II に基づいており、Version III での変更点は含んでいない。価格設定が高かったことと、Pコード・エンジンをかませているせいで性能が悪かったため、あまり売れなかった。後に p-System のファンが集まって設立された Pecan Systems が SofTech から買い取った。価格を安く設定したことである程度売り上げは改善したが、徐々に p-System と UCSD Pascal は市場から姿を消していった。

## 関連項目

  - [Pascal](../Page/Pascal.md "wikilink")
  - [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink")
  - [Pコードマシン](../Page/Pコードマシン.md "wikilink")
  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")

## 参考文献

  - *UCSD PASCAL System II.0 User's Manual March 1979* — Institute for Information Systems, UCSD. Copyright 1978 Regents of the University of California.

## 外部リンク

  - 2007年12月現在、UCSD は[1979年](../Page/1979年.md "wikilink")[6月1日](../Page/6月1日.md "wikilink")以前に書かれた [p-System](http://invent.ucsd.edu/technology/cases/1995-prior/SD1991-807.htm) の一部を非商用利用に限ってリリースしている。
  - 2004年、UCSD Pascal 開発チームのメンバーが30周年を記念して親睦会を開催した。
      - [An article in UCSD's alumni magazine](http://alumni.ucsd.edu/magazine/vol1no3/features/pascal.htm)
      - [The UCSD Pascal Reunion website](http://www.jacobsschool.ucsd.edu/Pascal/)
  - [The UCSD p-System Museum](http://www.threedee.com/jcm/psystem/index.html) Jefferson Computer Museum
  - [Pascal](http://www.hansotten.com/pascal.html) Hans Otten
  - [The Pascal Users' Group Newsletter Archive](http://www.moorecad.com/standardpascal/pug.html)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:1978年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1978年のソフトウェア "wikilink")