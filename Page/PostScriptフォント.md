> この記事は[PostScriptフォント](https://ja.wikipedia.org/wiki/PostScriptフォント)から翻訳されています。


**PostScriptフォント**は[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")が開発した[アウトラインフォント](https://ja.wikipedia.org/wiki/アウトラインフォント "wikilink")の仕様である。フォント情報のエンコードに[PostScript](../Page/PostScript.md "wikilink")ファイル形式を使用する。

## フォントの種類

### Type 0

Type 0はPostScript Language Reference Manual, 2nd Editionに記述されているように、「合成」フォント形式である。合成フォントは複数の子孫フォントを参照する高レベルフォントからなる。

  -
    OCF (Original Composite Font) 形式 (Type 0のファイル構造を使う) は大きな文字集合を持つフォントをサポートするために設計した形式。その後、複雑なアジア言語の符号化の問題を解決するため、より柔軟な構造を持つCID形式へとフォントフォーマットを移行する。

### Type 1

Type 1 (別名***[PostScript](../Page/PostScript.md "wikilink")***、***PostScript Type 1***, <span style="font-size:90%;">***PS1***</span>、<span style="font-size:90%;">***T1***</span>もしくは***Adobe Type 1***) は1バイト欧文フォントのためにAdobe Type ManagerソフトウェアとPostScriptプリンタで使われるフォント形式である。[フォントヒンティング](https://ja.wikipedia.org/wiki/フォントヒンティング "wikilink")のサポートが可能である。

当初は[プロプライエタリな仕様であったが](../Page/プロプライエタリ・ソフトウェア.md "wikilink")、アドビはすべてのType 1フォントが遵守しなければならないという条件付きで、サードパーティのフォント製造業者に仕様を開示した。

#### 歴史

*Type 1*はアウトライン情報のみを格納するよう効率的にPSシステムを単純化したものであり、完全な言語ではなかった (この点は[PDFも同様である](../Page/Portable_Document_Format.md "wikilink"))。アドビはそれからType 1テクノロジのライセンスを極めて高額だが、[ヒンティングのサポートを付け加えて売った](https://ja.wikipedia.org/wiki/フォントヒンティング "wikilink")。Type 1のより安価な実装であるType 3フォントはPostScript言語の洗練された機能すべてを使えたが、ヒンティングのための標準化された手段がなかった。その他の違いがさらに混乱を増やした。

この時点ではライセンス価格は非常に高額であると考えられており、アドビは値引きに頑として応じなかった。この問題によりアップルは独自のシステムである[TrueType](../Page/TrueType.md "wikilink")を1991年ごろに設計した。TrueTypeがアナウンスされると直ちに、アドビはType 1フォント形式の仕様を公開した。Altsys社の[Fontographer](https://ja.wikipedia.org/wiki/Fontographer "wikilink") (1995年1月に[マクロメディア](../Page/マクロメディア.md "wikilink")に買収され、2005年5月から[FontLab](https://ja.wikipedia.org/wiki/FontLab "wikilink")に保有された) のような小売されるツールにはType 1フォントの作成機能が追加された。それ以降、多くのフリーのType 1フォントがリリースされた。たとえば、[TeX](../Page/TeX.md "wikilink")組版システムで使われるフォントがこの形式で利用可能である。

#### テクノロジ

[PostScript](../Page/PostScript.md "wikilink") (PS) 言語を使うことにより、グリフは ([TrueType](../Page/TrueType.md "wikilink")の[2次曲線とは対照的に](../Page/二次関数.md "wikilink")) [3次](https://ja.wikipedia.org/wiki/3次曲線 "wikilink")[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")で記述され、そしてそれゆえ1つのセットのグリフを単純な数学的変換を通してサイズ変更し、PostScript対応の[プリンタに送ることができる](https://ja.wikipedia.org/wiki/プリンター "wikilink")。Type 1のデータは[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")ではなくグリフのアウトラインを記述しているので、Type 1フォントはよく「アウトラインフォント」と呼ばれる。これらの書体を電子ディスプレイ上で事前に確認したい利用者のために、フォントの小型版は余分な[ヒントと](https://ja.wikipedia.org/wiki/フォントヒンティング "wikilink")[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")によって画面上で見やすくきれいに表示する必要がある。このためにしばしば追加されたのが、画面表示のために最適化された同じ書体の[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")フォント形式であった。さもなければ、Type 1フォントを組版アプリケーションでプレビューするためには、[Adobe Type Managerが必要だった](https://ja.wikipedia.org/wiki/Adobe_Type_Manager "wikilink")。

### Type 2

Type 2は、アウトラインフォントファイルにおける文字記述の手続きにコンパクトな表現を提供する、character string形式である。この形式は Compact Font Format (CFF) と組み合わせて使うように設計されている。CFF/Type2形式はType 1 OpenTypeフォントの基礎であり、Acrobat 3.0 PDFファイル (PDF形式バージョン1.2) へのフォント埋め込みに使われる。

### Type 3

Type 3フォント (別名、***PostScript Type 3***、<span style="font-size:90%;">***PS3***</span>、<span style="font-size:90%;">***T3***</span>もしくは***Adobe Type 3***) はサブセットではなく完全なPostScript言語を使って定義されたグリフからなる。これにより、Type 3フォントはType 1フォントでは不可能な[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")、色、フィルパターンの指定などが行える。しかしながら、ヒンティングはサポートしていない。Adobe Type ManagerはType 3フォントをサポートしない。

### Type 4

Type 4はプリンタフォントカートリッジとプリンタのハードディスク上の永続的なストレージ用のフォントを作るために使われた形式である。文字の記述はType 1形式で表現される。アドビはこのプロプライエタリな形式を文書化していない。

### Type 5

Type 5はType 4形式に似ているが、PostScriptプリンタのROMへ格納されるフォントのために使われる。CROMフォント (圧縮ROMフォント) という別名でも知られている。

### Types 9, 10, 11

[Ghostscript](../Page/Ghostscript.md "wikilink")はアドビの補足文書に記されているCIDフォントType 0, 1, 2をそれぞれこう呼んでいた。Type 9, 10, 11はそれぞれType 1, 3, 42を格納するためのCIDフォントである。

### Type 14

Type 14、もしくはChameleonフォント形式は、多数のフォントを少量の格納空間で表現するために使われる。Chameleonフォントのコアセットは1つのMaster Fontと、特定の書体の望んだ字形の集合を与えるためにMaster Fontを補正する方法を指定したフォント記述子の集合からなる。

アドビはType 14形式を文書化していない。

### Type 32

Type 32はバージョン番号2016かそれ以降のPostScriptインタプリタにビットマップフォントをダウンロードするために使われる。ビットマップ文字は直接インタプリタのフォントキャッシュへ転送され、そのためプリンタのメモリを節約できる。

### Type 42

Type 42フォント形式はPostScriptファイル形式に埋め込まれた[TrueType](../Page/TrueType.md "wikilink")フォントである。これによりTrueTypeラスタライザを含むPostScript対応プリンタが可能になる。PostScriptインタプリタにはバージョン2010でオプション機能として初めて実装された。複数バイトCJK TrueTypeフォントのサポートはバージョン2015で追加された。

## ファイル形式

### CID

**CIDフォント** (、別名***CID-keyed Font***、***CID-based Font***) は多数の[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")を扱うために設計された[PostScript](../Page/PostScript.md "wikilink")フォントファイル形式である。欧文以外の文字集合はほとんどの欧文[フォント](../Page/フォント.md "wikilink") (Identity-HとIdentity-Vフォントも含まれる) を作り上げる欧文[書体](../Page/書体.md "wikilink")より多くの文字を含むので、それらをサポートするために開発された。

アドビは複雑なアジア言語 ([CJK](../Page/CJKV.md "wikilink")) の符号化と非常に大きな文字集合の問題を取り扱うOCF/Type 0フォントの問題を解決するためにCIDフォント形式を開発した。

CIDフォント形式標準[Type 1フォント形式と組み合わせてCIDフォントで](https://ja.wikipedia.org/wiki/#Type_1 "wikilink")、もしくは[Type 2と組み合わせてCID](https://ja.wikipedia.org/wiki/#Type_2 "wikilink")-keyed [OpenType](../Page/OpenType.md "wikilink")フォントで使うことができる。

### Compact Font Format

**Compact Font Format** (別名**CFF**フォント形式、**Type 2**フォント形式、もしくは**CFF/Type 2**フォント形式) は複数引数のオペレータ、各種の定義済みデフォルト値、符号化された値のより効率的な割り当ておよびにFontSet (フォントのファミリ) 間で共有されるサブルーチンを使うことにより、Type 1より少ない格納空間を使うように設計されている。[OpenType](../Page/OpenType.md "wikilink")フォントはCFFテーブルにグリフのアウトラインを含むこともできる。

CFFはType 2 charstring形式と組み合わせて使うように設計されている。CFFはType 1 OpenTypeフォント形式の基礎となっている。

CFFフォントは[PDFバージョン](../Page/Portable_Document_Format.md "wikilink")1.2から、PDFファイルに埋め込むことができるようになった。Type 2 charstringフォント形式と[CIDフォント形式は](https://ja.wikipedia.org/wiki/#CID "wikilink")、ともにCID-keyed OpenTypeフォントのために使うことができる。

Type 1フォントは品質を一切落とすことなしに、CFF/Type2形式に変換し、またType 1に戻すことができる。

### マルチプルマスター

**マルチプルマスターフォント** (もしくは**MMフォント**) は、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")の[Type 1](https://ja.wikipedia.org/wiki/#Type_1 "wikilink") [PostScript](../Page/PostScript.md "wikilink")[フォントの拡張である](../Page/書体.md "wikilink") (*であった*)。現在では[OpenType](../Page/OpenType.md "wikilink")の出現によりほとんどとってかわられた。マルチプルマスターフォントは1つかそれ以上の「マスター」 — すなわち、オリジナルのフォントスタイル — を含み、利用者がそれらのフォントスタイルをに連続する範囲の「軸」に沿って織り交ぜることを可能にする。

### OpenType

PostScriptのグリフデータはOpenTypeフォントファイルに埋め込むことができるが、OpenTypeフォントはPostScriptアウトラインを使うものに限られない。

### Adobe Font Metrics

**Adobe Font Metrics** (AFM) [ファイルは一般的な](../Page/ファイル_\(コンピュータ\).md "wikilink")[フォント情報とフォントメトリック情報を含む](../Page/書体.md "wikilink")。AFMファイルは通常[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")環境でのみ直接使われる。

### Printer Font ASCII

**Printer Font ASCII** (PFA) は[ASCII](../Page/ASCII.md "wikilink")バージョンのPFBで、通常ファイル名に".PFA"という拡張子が付く。フォントの字形データを含む。PFAはPostScript言語のインタプリタが使うフォントの形式であり、UNIX環境で使われるType 1フォントの推奨される形式でもある。

### Printer Font Binary

**Printer Font Binary** (PFB) は[アドビが作成したバイナリPostScript](../Page/アドビシステムズ.md "wikilink")[フォント](../Page/フォント.md "wikilink")形式であり、通常ファイル名に".PFB"という拡張子が付く。フォントの字形データを含む。

### Printer Font Metric

**Printer Font Metric** (PFM) はバイナリ版のAFMであり、通常ファイル名に".PFM"という拡張子が付く。フォントのメトリック情報を含む。

### .INF

**.inf** (INFormation) ファイルはWindowsやDOSベースのアプリケーションにおけるフォントメニューでの名前など、アプリケーション固有の情報をプレーンASCIIテキストで含む。フォントがWindowsにインストールされるとき、ATMのインストーラソフトウェアはAFMとINFファイルを入力にとり、必要なPFMファイルをインストール時に生成する。AFMとINFファイルは利用者のシステムにインストールされない。

### .MMM

**.MMM** ファイルはマルチプルマスターフォントがWindows環境で必要とし、メトリックデータに使われる。 CIDは、アドビ社のCIDフォントが内蔵するすべての文字（文字コレクション）を識別するため、文字ごとに振られる一連の番号。

文字コレクションは言語ごとに定義され、その言語の主要な文字集合をサポートするために必要な文字をすべて含む。文字コレクションには「登録者-配列（-追補番号）」の形式で名前が付けられる。たとえばアドビ社が定めた日本語の表記に使われる文字コレクションの名称はAdobe-Japan1である。

Adobe-Japan1は、JIS X 0208やISO/IEC 10646(≒Unicode)などの公的な文字コード規格では（異体字セレクタを使わない限り）同じコードが与えられている異体字の字形1つ1つに別々のCIDを割り当てている。実際のOS・アプリケーションとのやりとりは通常フォントに内蔵されている CMAPテーブル（CIDとUnicodeを相互に関連付けた対応表）を参照して行われるが、Acrobat・InDesign（いずれもアドビシステムズ社製品）・日本語LaTeX\[1\]（フリーソフト）などのソフトはCID番号を直接利用することがある

### .OFM

**.OFM** は[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン2.1から、そのバイナリ版のフォントメトリックファイルに使われる拡張子である。

## 文字集合

PostScriptフォントはあらゆる[文字集合](../Page/文字集合.md "wikilink")を符号化できるが、アドビが開発したフォントで使うために、アドビが特に開発した文字集合が存在する。

### Adobe Western 2

これは大文字と小文字の[字母](https://ja.wikipedia.org/wiki/字母 "wikilink")、[図形](https://ja.wikipedia.org/wiki/図形 "wikilink")記号、[アクセント](../Page/アクセント.md "wikilink")文字、および[約物](../Page/約物.md "wikilink")からなる基本的な文字集合を含む。これらのフォントは[通貨記号](../Page/通貨記号.md "wikilink") ([セント](../Page/セント_\(通貨\).md "wikilink")、[ドル](../Page/ドル.md "wikilink")、[ユーロ](../Page/ユーロ.md "wikilink")、[フローリン](https://ja.wikipedia.org/wiki/フローリン "wikilink")、[ポンド](../Page/ポンド_\(通貨\).md "wikilink")、[円](../Page/円記号.md "wikilink"))、標準的な[合字](../Page/合字.md "wikilink") (fi, fl)、よく使われる[分数](../Page/分数.md "wikilink") (1/4, 1/2, 3/4)、よく使われる[数学記号](../Page/数学記号の表.md "wikilink")、[上付き](https://ja.wikipedia.org/wiki/上付き "wikilink")数字 (1,2,3)、よく使われる区切り文字や連結文字、その他の記号 ([短剣符](../Page/短剣符.md "wikilink")、[商標](../Page/商標.md "wikilink")、登録商標、[著作権](../Page/著作権.md "wikilink")、[段落記号](../Page/段落記号.md "wikilink")、[リットル](../Page/リットル.md "wikilink")、[estimated symbolなど](https://ja.wikipedia.org/wiki/estimated_symbol "wikilink")) も含む。Western 2 はさらに17種類の記号文字を追加した: ユーロ、リットル、estimated、[オメガ](../Page/Ω.md "wikilink")、[パイ](../Page/Π.md "wikilink")、[偏微分](../Page/偏微分.md "wikilink")、[デルタ](../Page/Δ.md "wikilink")、[積算](../Page/積算.md "wikilink")、[総和](https://ja.wikipedia.org/wiki/総和 "wikilink")、[根号](../Page/根号.md "wikilink")、[無限](../Page/無限.md "wikilink")大、[積分](../Page/積分記号.md "wikilink")、[近似](../Page/近似.md "wikilink")、[不等号](../Page/不等号.md "wikilink")、以下、以上、および[菱形](../Page/菱形.md "wikilink")。

Adobe Western 2 文字集合を含むフォントは[アフリカーンス語](../Page/アフリカーンス語.md "wikilink")、[バスク語](../Page/バスク語.md "wikilink")、[ブルトン語](../Page/ブルトン語.md "wikilink")、[カタルーニャ語](../Page/カタルーニャ語.md "wikilink")、[デンマーク語](../Page/デンマーク語.md "wikilink")、[オランダ語](../Page/オランダ語.md "wikilink")、[英語](../Page/英語.md "wikilink")、[フィンランド語](../Page/フィンランド語.md "wikilink")、[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")、[ゲール語](../Page/ゲール語.md "wikilink")、[ドイツ語](../Page/ドイツ語.md "wikilink")、[アイスランド語](https://ja.wikipedia.org/wiki/アイスランド語 "wikilink")、[インドネシア語](../Page/インドネシア語.md "wikilink")、[アイルランド語](../Page/アイルランド語.md "wikilink")、[イタリア語](../Page/イタリア語.md "wikilink")、[ノルウェー語](../Page/ノルウェー語.md "wikilink")、[ポルトガル語](https://ja.wikipedia.org/wiki/ポルトガル語 "wikilink")、[サーミ語](../Page/サーミ語.md "wikilink")、[スペイン語](https://ja.wikipedia.org/wiki/スペイン語 "wikilink")、[スワヒリ語](https://ja.wikipedia.org/wiki/スワヒリ語 "wikilink")および[スウェーデン語](../Page/スウェーデン語.md "wikilink")を含む、ほとんどの西欧言語をサポートする。

この標準はアドビがOpenTypeフォントに実装する新しい最小の文字集合標準である[ISO-Adobeに取って代わられた](https://ja.wikipedia.org/wiki/#ISO-Adobe "wikilink")。

### Adobe CE

Adobe CE 文字集合を含むフォントには以下の中央ヨーロッパ言語のサポートに必要な文字も含まれている: [クロアチア語](../Page/クロアチア語.md "wikilink")、[チェコ語](../Page/チェコ語.md "wikilink")、[エストニア語](../Page/エストニア語.md "wikilink")、[ハンガリー語](../Page/ハンガリー語.md "wikilink")、[ラトビア語](../Page/ラトビア語.md "wikilink")、[リトアニア語](https://ja.wikipedia.org/wiki/リトアニア語 "wikilink")、[ポーランド語](../Page/ポーランド語.md "wikilink")、[ルーマニア語](../Page/ルーマニア語.md "wikilink")、[セルビア語](../Page/セルビア語.md "wikilink") ([ラテン文字](../Page/ラテン文字.md "wikilink"))、[スロバキア語](../Page/スロバキア語.md "wikilink")、[スロベニア語](../Page/スロベニア語.md "wikilink")および[トルコ語](../Page/トルコ語.md "wikilink")。

### Adobe-GB1

この[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")の文字コレクションはGB 1988-89、[GB 2312](../Page/GB_2312.md "wikilink")-80、GB/T 12345-90、GB 13000.1-93、および[GB 18030](../Page/GB_18030.md "wikilink")-2005文字コード規格のサポートを提供する。サポートされる[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")には[ISO-2022](https://ja.wikipedia.org/wiki/ISO-2022 "wikilink")、EUC-CN、GBK、[UCS-2](https://ja.wikipedia.org/wiki/UCS-2 "wikilink")、[UTF-8](../Page/UTF-8.md "wikilink")、[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-32](../Page/UTF-32.md "wikilink")、およびGB 18030-2005で公開されている1、2、4バイトコードを組み合わせた文字符号化方式が含まれる。

### Adobe-CNS1

この[繁体字](../Page/繁体字.md "wikilink")中国語の文字コレクションは[Big5](../Page/Big5.md "wikilink")と[CNS 11643](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink")-1992文字コード規格のサポートを提供する。おもに香港ロケールで使われる文字を含んだ、多数のBig5拡張のサポートも含んでいる。サポートされるBig5拡張の主要なものには[HKSCSが含まれる](../Page/香港増補字符集.md "wikilink")。

サポートされる文字符号化方式にはISO-2022、EUC-TW、Big Five、UCS-2、UTF-8、UTF-16、およびUTF-32が含まれる。

### Adobe-Japan1

日本語フォントのために開発された文字集合である。アドビの集合は[JIS X 0208](../Page/JIS_X_0208.md "wikilink"), [ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")、[Microsoft Windows 3.1 J](../Page/マイクロソフト標準キャラクタセット.md "wikilink")、[JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2004、[JIS X 0212](../Page/JIS_X_0212.md "wikilink")-1990、[共同通信](https://ja.wikipedia.org/wiki/共同通信 "wikilink")の[U-PRESS](../Page/U-PRESS.md "wikilink")などに由来する文字集合をサポートする。

### Adobe-Japan2

当初JIS X 0212-1990文字コード規格の実装およびそのMacintosh拡張として Adobe-Japan2-0 が存在したが、Adobe-Japan1-6 規格の導入とともに、Adobe-Japan2-0は廃止された（Adobe-Japan2-1以降は元々存在しない）。

### Adobe-Korea1

この[朝鮮語](../Page/朝鮮語.md "wikilink")用の文字コレクションは[KS X 1001](../Page/KS_X_1001.md "wikilink"):1992とKS X 1003:1992文字コード規格、およびいくつかの選定されたメーカー拡張のサポートを提供する。サポートされる文字符号化方式にはISO-2022-KR、EUC-KR、Johab、UHC、UCS-2、UTF-8、UTF-16、およびUTF-32が含まれる。

### ISO-Adobe

ISO-Adobe文字集合を含むフォントは、以下のようなほとんどの西欧言語をサポートする: アフリカーンス語、バスク語、ブルトン語、カタルーニャ語、デンマーク語、オランダ語、英語、フィンランド語、フランス語、ゲール語、ドイツ語、アイスランド語、インドネシア語、アイルランド語、イタリア語、ノルウェー語、ポルトガル語、サーミ語、スペイン語、スワヒリ語およびスウェーデン語。これはアドビ製のほとんどのPostScript Type 1における標準文字集合である。

## Windowsサポート

[Windows 95](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")、[Windows 98](https://ja.wikipedia.org/wiki/Windows_98 "wikilink")、[Windows NTおよび](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")[Windows MeはType](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink") 1フォントをネイティブにサポートしない。これらのオペレーティングシステム上でこれらのフォントを使うには[Adobe Type Managerが必要である](https://ja.wikipedia.org/wiki/Adobe_Type_Manager "wikilink")。[Windows 2000](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")、[Windows XPおよび](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Windows Vistaは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[GDI呼び出しを通してType](../Page/Graphics_Device_Interface.md "wikilink") 1フォントをネイティブにサポートする。しかしながら[Windows Vistaで導入され](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、[Windows XPでも利用可能な](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Windows Presentation FoundationはType](../Page/Windows_Presentation_Foundation.md "wikilink") 1フォントのサポートを捨て、[Type 2フォントに乗り換えている](https://ja.wikipedia.org/wiki/#Compact_Font_Format "wikilink")。

PostScriptをネイティブにサポートするWindowsプラットフォームでは、バイナリ形式のPostScriptとOpenTypeファイル形式のみがサポートされている。

[Windows Vistaにおいて](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink")（かつてのコードネームAvalon）はOpenType CFF/Type 2フォントのラスタライズをサポートする一方、Type 1フォントはまだ[GDIでサポートされているがGDI](../Page/Graphics_Device_Interface.md "wikilink")+ではサポートされていない。

## コアフォントセット

フォントの種類に加え、PostScript仕様は最小数のフォントと各フォントがサポートすべき文字集合を指示するCore Font Setも定義している。PostScript 3では、136種類のフォントが規定され、そのうちの35種類が標準フォントであり、Windows 95、Windows NTおよびMacintoshのコアフォントである。選ばれたフォントはMicrosoft OfficeとHP 110フォント集合に由来する。

## 関連項目

  - [フォント](../Page/フォント.md "wikilink")
  - [OpenType](../Page/OpenType.md "wikilink")
  - [TrueType](../Page/TrueType.md "wikilink")
  - [ページ記述言語](../Page/ページ記述言語.md "wikilink")
  - 英語版[ウィキブックス](../Page/ウィキブックス.md "wikilink")の[PostScript FAQ](https://ja.wikipedia.org/wiki/Wikibooks:en:PostScript_FAQ "wikilink")。

## 外部リンク

### Typeの情報

  - [PostScript Type 1 and Type 3 Fonts General Information](http://kb.adobe.com/selfservice/viewContent.do?externalId=328509&sliceId=2) (英語)
  - [Adobe Tech. Note 5176, The CFF (Compact Font Format) Spec., (PDF: 251 KB)](http://partners.adobe.com/public/developer/en/font/5176.CFF.pdf) (英語)
  - [Adobe Tech. Note 5177, Type 2 Charstring Format (PDF: 212 KB)](http://partners.adobe.com/public/developer/en/font/5177.Type2.pdf) (英語)
  - [The Type 42 Font Format Specification](http://www.adobe.com/devnet/font/pdfs/5012.Type42_Spec.pdf) (英語)

### ファイル形式の情報

  - [Adobe CID fonts](http://www.adobe.com/products/postscript/pdfs/cid.pdf) (英語)
  - [Font Formats, File Types and Q\&A](http://partners.adobe.com/public/developer/opentype/index_font_formats.html) (英語)

### 文字集合の情報

  - [Adobe Technical Note \#5094 Adobe CJKV Character Collections and CMaps for CID-Keyed Fonts](http://www.adobe.com/devnet/font/pdfs/5094.CJK_CID.pdf) (英語)
  - [Adobe - Fonts : Character Sets](http://www.adobe.com/type/browser/info/charsets.html) (英語)
  - [Adobe Tech Note \#5078 Adobe-Japan1-6 Character Collection for CID-Keyed Fonts](http://partners.adobe.com/public/developer/en/font/5078.Adobe-Japan1-6.pdf) (英語)
  - [Technical Note \#5097 Adobe-Japan2-0 Character Collection for CID-Keyed Fonts](http://www.adobe.com/devnet/font/pdfs/5097.Adobe-Japan2-0.pdf) (英語)

### コアフォントの情報

  - [PostScript 3 Core Font Set Overview](http://partners.adobe.com/public/developer/en/ps/sdk/TN5609.PS3_Fonts.pdf) (英語)
  - [The Adobe PostScript 3 Font Set](http://www.adobe.com/products/postscript/pdfs/ps3fonts.pdf) (英語)

### その他

  - [comp.fonts FAQ: OS/2 2.1 and beyond](http://nwalsh.com/comp.fonts/FAQ/cf_70.htm) (英語)
  - [comp.lang.postscript FAQ](http://www.postscript.org/FAQs/language/FAQ.html) (英語)
  - [About Fonts](http://www.asy.com/fonts.htm) (英語)
  - [Fonts, Fonts, and more Fonts\!](http://www.ntg.nl/eurotex/KacvinskyFonts.pdf) (英語)

[Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink")