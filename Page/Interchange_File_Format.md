> この記事は[Interchange File Format](https://ja.wikipedia.org/wiki/Interchange_File_Format)から翻訳されています。


**Interchange File Format**（**IFF**）は、汎用[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")の一種。1985年に[エレクトロニック・アーツ](../Page/エレクトロニック・アーツ.md "wikilink")が、[コモドール](../Page/コモドール.md "wikilink")の [Amiga](../Page/Amiga.md "wikilink") 向けに異なるアプリケーション間でのデータ転送を容易にするために開発した。

IFF には典型的な[拡張子](../Page/拡張子.md "wikilink")は存在しない。*.iff* という拡張子のファイルは [ILBM](https://ja.wikipedia.org/wiki/ILBM "wikilink") フォーマットであることが多い。ILBM は IFF を使った画像フォーマットではあるが、IFFフォーマットを使っているのは ILBM だけではない（多くの場合、IFFファイルの拡張子はそれほど重要ではない）。

## 構造

IFFファイルは**チャンク**（chunk）から構成される。各チャンクの先頭には "Type ID" と呼ばれるフィールドがある（[Macintosh](../Page/Macintosh.md "wikilink") では OSType、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では [FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink") とも呼ばれる）。その次に32ビット符号なし[整数](../Page/整数.md "wikilink")があり（IFFでは全ての整数は[ビッグエンディアンで表される](https://ja.wikipedia.org/wiki/エンディアン "wikilink")）、その後のデータ（チャンクの中身）をバイト数で記述している。そのように各チャンクの長さを明示的に記述するため、解釈するときに処理に関係ないチャンクをスキップすることが可能である。

チャンクをグループ化する "FORM"、"LIST"、"CAT " といったチャンクもある。FORMチャンクは[構造体](../Page/構造体.md "wikilink")のようなもので、様々なチャンクの入れ子が可能である。LISTチャンクは、一連の PROP （プロパティ）チャンクとそのプロパティが適用される入れ子になったチャンクグループからなる。CAT  は単なる入れ子になったチャンクの集まりであって、特に意味は決められていない。グループチャンクには、必要に応じて他のグループチャンクを含むことができる。グループチャンクにも長さが記述される。したがって、グループチャンクをスキップするのも容易である。

チャンクは必ずファイル先頭からのオフセットが偶数の位置から始まる。これはIFFが元々は[MC68000](../Page/MC68000.md "wikilink")向けだったためで、MC68000では1バイトより大きい単位でのロードは偶数バイトからでないと不可能だった。そのため、必要に応じてパディングが行われる。

IFFファイルは全体として1つのグループチャンク（FORM か LIST か CAT ）になっている。

チャンクはタイプによって中身の構造が異なり、数値データだったり、テキストだったり、何らかのデータだったりする。IFF形式のファイルをチャンクとして中に含めることもできる。各種IFFファイルで使われている標準のチャンクもいくつかある。"AUTH"（作者情報を含むテキスト）、"ANNO"（アノテーション、通常はそのファイルを作ったプログラム名）、"NAME"（作品名などのテキスト）、"VERS"（ファイルバージョン）、"(c) "（コピーライト情報テキスト）などがある。その他にいくつかの形式でよく使われるチャンクとして、"CMAP"（[ILBM](https://ja.wikipedia.org/wiki/ILBM "wikilink")などの画像フォーマットでのパレット情報）がある。またチャンク名が同じでもフォーマットによって意味が異なるものもある。例えば "BODY" は ILBM では画像そのものを指すが、[8SVX](https://ja.wikipedia.org/wiki/8SVX "wikilink") では音声そのものである。具体的なファイルフォーマットに固有のチャンクもある。あるプログラムがIFFファイルを作るときに独自のチャンクを追加したとして、別のプログラムでそれを読むときでも問題は発生しない（知らないチャンクは単にスキップすればよいため）。これは、IFFや類似のフォーマットの大きな長所である。

入れ子可能で、説明を追加可能なファイルフォーマットであることから、[XMLとの類似性があると言われている](../Page/Extensible_Markup_Language.md "wikilink")。ただし、XMLがテキストフォーマットであるのに対して、IFFには必ずバイナリデータ（チャンクの長さのフィールド）が含まれている。IFFを機械的にXMLに変換することは可能だが、XMLの方が機能的に拡張されているため、逆方向の変換は簡単ではない。

## IFFベースの主なファイルフォーマット

  - 16SV （標本ごとに16ビットを使用する音声フォーマット）
  - [8SVX](https://ja.wikipedia.org/wiki/8SVX "wikilink") （標本ごとに8ビットを使用する音声フォーマット）
  - ACBM （**A**miga **C**ontiguous **B**it**M**ap - PCXに似た画像フォーマット。マイクロソフトの AmigaBasic で使われた）
  - [AIFF](../Page/AIFF.md "wikilink") （音声フォーマット）
  - ANBM （アニメーションフォーマット。[ILBM](https://ja.wikipedia.org/wiki/ILBM "wikilink")を複合した形式で、個々の画像を次々表示する）
  - [ANIM](https://ja.wikipedia.org/wiki/ANIM "wikilink") （アニメーションフォーマット）
  - BIFF8 （[Microsoft Excelでかつて使われていた形式](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")）
  - [Alias/Wavefront Maya](../Page/Maya.md "wikilink") ファイルフォーマット （画像およびシーン記述）
  - [Word 文書](../Page/Microsoft_Word.md "wikilink") （Word 97 までのフォーマット）
  - [DjVu](../Page/DjVu.md "wikilink") （高解像度の画像を埋め込める文書フォーマット）
  - DR2D （二次元ベクターフォーマット）
  - EMOD （QuadraComposer モジュールフォーマット）
  - FNTR （[ラスターフォントフォーマット](../Page/フォント.md "wikilink")）
  - FNTV （[ベクターフォントフォーマット](../Page/フォント.md "wikilink")）
  - FPBM （[LightWave](../Page/LightWave.md "wikilink") Flexible Precision Buffer Map 画像フォーマット）
  - FTXT （テキストフォーマット）
  - GSCR （楽譜フォーマット）
  - IFRS （Blorb とも。[インタラクティブフィクション](https://ja.wikipedia.org/wiki/インタラクティブフィクション "wikilink")用フォーマット）
  - IFZS （Quetzal とも。[ゾーク](../Page/ゾーク.md "wikilink")の内部インタプリタ用プログラムファイル）
  - [ILBM](https://ja.wikipedia.org/wiki/ILBM "wikilink") （[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")フォーマット）
  - LWOB （[LightWave](../Page/LightWave.md "wikilink") 3次元オブジェクトフォーマット）
  - LWO2 （[LightWave](../Page/LightWave.md "wikilink") 3次元オブジェクトフォーマット）
  - PDEF （Deluxe Print page definition）
  - PICS （Macintosh QuickDraw の画像をIFFフォーマットでカプセル化したもの）
  - PLBM （画像フォーマット）
  - SHRI （Shriアーカイブ）
  - SMUS （Simple Music format、MIDIに類似したフォーマット）
  - TDDD （3次元オブジェクトフォーマット）
  - USCR （楽譜フォーマット）
  - UVOX （音声フォーマット）
  - VDEO （動画フォーマット）
  - YAFA （アニメーションフォーマット）

## IFFフォーマットのクローンおよび派生フォーマット

  - [RIFF](../Page/Resource_Interchange_File_Format.md "wikilink") - [マイクロソフト](../Page/マイクロソフト.md "wikilink")と[IBM](../Page/IBM.md "wikilink")による派生フォーマット。違いは、先頭に "RIFF" という文字列がある点と、整数表現に[リトルエンディアンを使っている点である](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。例えば[AVIや](../Page/Audio_Video_Interleave.md "wikilink")[WAV](../Page/WAV.md "wikilink")はRIFFの一種である。ビッグエンディアン版の RIFX も定義されているが、ほとんど使われていない。
  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink") - [アルダス](../Page/アルダス.md "wikilink")が [PostScript](../Page/PostScript.md "wikilink") に高色深度の[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")を含めるべく設計したフォーマット。IFF のようなチャンク構造を持つが、画像のフォーマット自体は ILBM ではない。
  - 標準[MIDI](../Page/MIDI.md "wikilink")フォーマットはIFFの基本概念を取り入れているが、IFFの規格には従っていない。
  - [PNGもIFFからチャンクの概念を取り入れているが](../Page/Portable_Network_Graphics.md "wikilink")、構造は異なる。
  - [QuickTime](../Page/QuickTime.md "wikilink") (.mov) と [MP4](../Page/MP4.md "wikilink") もIFFのチャンクの概念を取り入れているが、それを「アトム」と呼んでおり、配置が異なる。また、4GBを超えるチャンクも扱える。
  - [3dstudio](../Page/3ds_Max.md "wikilink") (.3ds) はチャンク名に4バイトではなく2バイトを使った3次元シーンフォーマット
  - [Nero Burning ROMは](../Page/Nero_Burning_ROM.md "wikilink")、CDイメージファイルのフォーマットにIFFチャンクの概念を使っている。ただしチャンクデータは最後尾にある。また、用語もIFFとは異なる。

## 外部リンク

  - [About Interchange File Format](http://www.borg.com/~jglatt/tech/aboutiff.htm)
  - [“EA IFF 85”: Standard for Interchange Format Files](http://www.szonye.com/bradd/iff.html) - オリジナルのIFF仕様。EA の Jerry Morrison による（1985年1月14日）
  - [Interchange file format entries](http://www.file-extensions.org/search/?searchstring=interchange) at File Extensions Encyclopedia
  - [Amiga files formats](http://lclevy.free.fr/amiga/formats.html)
  - [IFF FORM AND CHUNK REGISTRY](http://amigan.1emu.net/reg/iff.html)
  - ["Standards and specs: The Interchange File Format (IFF)"](http://www.ibm.com/developerworks/power/library/pa-spec16/) IBM developerworks

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")