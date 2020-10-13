> この記事は[Portable Network Graphics](https://ja.wikipedia.org/wiki/Portable_Network_Graphics)から翻訳されています。


**Portable Network Graphics**（ポータブル・ネットワーク・グラフィックス、**PNG**）は[コンピュータ](../Page/コンピュータ.md "wikilink")で[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")を扱う[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。[圧縮アルゴリズム](https://ja.wikipedia.org/wiki/圧縮アルゴリズム "wikilink")として[Deflate](../Page/Deflate.md "wikilink")を採用している、圧縮による画質の劣化のない[可逆圧縮](../Page/可逆圧縮.md "wikilink")の[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")である。

1996年に登場し、可逆圧縮の画像フォーマットとして既に普及していた[GIFに対しネットワーク経由での使用を想定した機能や透過処理など](../Page/Graphics_Interchange_Format.md "wikilink")、多くの機能をサポートした。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")や[グラフィックソフト](https://ja.wikipedia.org/wiki/グラフィックソフト "wikilink")でのサポートも進み、インターネットを中心に普及した。

英語でと発音されることから\[1\]、「**ピング**」や「**ピン**」と多く読まれる。

## 概説

画像のとして、最大16ビットの[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")、24ビットと 48ビットの[RGB](../Page/RGB.md "wikilink")、または8ビットまでのインデックスカラーモード（[パレットカラー](https://ja.wikipedia.org/wiki/パレットカラー "wikilink")) を利用することができる。透過についてはクロマキーによる透過指定、および8ビットから16ビットの[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")をサポートする。また、画像に付属するテキストなどの[メタデータ](../Page/メタデータ.md "wikilink")や[ガンマ値なども画像ごとに記録できる](https://ja.wikipedia.org/wiki/ビットマップ画像#ガンマ補正 "wikilink")。

GIFと異なり、PNGには[アニメーション](../Page/アニメーション.md "wikilink")機能はない。ただし、PNGはチャンク（データのブロック）で自由に拡張できるようになっていて、1ファイルに複数の画像を含めることができる。これを使ってアニメーション機能を追加した [MNG](../Page/Multiple-image_Network_Graphics.md "wikilink") と [APNG](../Page/Animated_Portable_Network_Graphics.md "wikilink") が別のフォーマットとして開発されている。他の拡張として、立体視用にステレオPNG (PNS) フォーマット\[2\]がある。

## 歴史

PNGが開発された動機は、1995年の初めに、GIFに使われていた圧縮アルゴリズム[LZWについて米](../Page/Lempel–Ziv–Welch.md "wikilink")[ユニシス](../Page/ユニシス.md "wikilink")が特許を保有しているとし、GIFを使ったソフトウェアに特許権を行使すると発表したことによる。実際、PNGの頭文字は非公式に "**P**NG is **N**ot **G**IF" という意味が込められている\[3\]\[4\]（[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")）。また、当時256色以上表示可能なコンピュータが主流になってきたため、GIFフォーマットにある256色までという制限を解消する必要もあった。[1999年](../Page/1999年.md "wikilink")8月、ユニシスが非商用ソフトについても特許使用料を請求することを決めると、PNGはさらに注目を集めるようになった。

  - [1996年](../Page/1996年.md "wikilink")10月1日 - PNG Version 1.0の仕様リリース。後にとして承認。同日、[W3Cによる勧告](../Page/World_Wide_Web_Consortium.md "wikilink")。
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")12月31日 - Version 1.1リリース。小規模な変更と三種類の新しいチャンクを追加。
  - [1999年](../Page/1999年.md "wikilink")8月11日 - Version 1.2リリース。一種類の追加チャンク。
  - [2002年](../Page/2002年.md "wikilink")8月20日 - 日本において[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink") JIS X4242 『コンピュータグラフィクス及び画像処理－ネットワーク用画像形式(PNG)』が制定される\[5\]。
  - [2003年](../Page/2003年.md "wikilink")11月10日 - 国際標準化 ([ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 15948:2003) 。このバージョンは 1.2 とわずかな差異あり。新規追加チャンクはなし。
  - [2004年](../Page/2004年.md "wikilink")3月3日 - 国際標準化 (ISO/IEC 15948:2004) \[6\]

## 技術詳細

詳しくは、仕様書\[7\]\[8\]\[9\]を参照。

### ファイルヘッダ

PNG ファイルはヘッダに 8 バイトのシグネチャ（[マジックナンバー](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")）を持つ。16進数の値は89 50 4E 47 0D 0A 1A 0Aとなる（制御文字で表すとHTJ "PNG" CR LF SUB LF）。各値の意味は次の通り。

| |値       | 説明                                                                                    |
| -------- | ------------------------------------------------------------------------------------- |
| 89       | 8ビットデータをサポートしない転送システムを検知するためのハイビット値。また、テキストファイルが誤ってPNGと認識されるのを防ぐ。                     |
| 50 4E 47 | [アスキー文字で](../Page/ASCII.md "wikilink")**PNG**を表す。テキストエディタで開いた場合などに、フォーマットをわかりやすくするため。 |
| 0D 0A    | [DOSスタイルの改行](../Page/MS-DOS.md "wikilink") (CR+LF)。DOS → UNIXでの行末データ変換が行われていないかを検知する。 |
| 1A       | DOSでTYPEコマンドを使ってファイル表示をさせた場合、SUB (EOF) として表示を停止させるバイト。                                |
| 0A       | UNIXスタイルの行末 (LF) 。UNIX → DOSでの行末変換が行われていないかを検知する。                                     |

ファイルヘッダの後にはIHDRチャンクが必ず来て、IHDRチャンクのサイズは13バイト固定なため、シグネチャの次の8バイトも00 00 00 0D 49 48 44 52で固定されている。

### チャンク

ファイルヘッダに続いて、チャンクと呼ばれる複数のデータブロックが続く。各チャンクは画像についての様々な情報を保持するもので、**必須**チャンクと**補助**チャンクに分けられる。補助チャンクは任意的なもので、処理プログラム側によっては必ずしも処理されない。このチャンク構造により、PNGフォーマットは拡張性と前方互換性を両立する。

チャンクの構造は、

1.  チャンクサイズ。ビッグ[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")（4バイト）
2.  チャンクの種類（4バイト）
3.  実際のデータ
4.  データの[CRC-32](../Page/巡回冗長検査.md "wikilink")（4バイト）

の順番で配置される。

チャンクの種類は、大文字と小文字が区別されるアルファベット4文字で表される。

  - 1 文字目が大文字のときは、必須チャンクに分類される。必須チャンクには、その画像ファイルを読み込むために必要な情報が含まれ、デコーダが解析不可能な必須チャンクに遭遇した場合、エラーとなる。
  - 2 文字目の大文字小文字は、そのチャンクがパブリックかプライベートかを示す。大文字がパブリック。パブリックチャンクはその仕様が公開、定義されたもので、公開チャンクともいう。
  - 3 文字目は将来的な拡張のためにリザーブされている。現在は常に大文字にしなければいけない。
  - 4 文字目の大小は、そのチャンクがそのままコピーできるかどうかを示す。小文字の場合、ファイルへの変更内容に関わらず、そのチャンクをコピーして継続的に使用できる。大文字の場合、他の必須チャンクへの変更の影響を受けることを表す。

#### 必須チャンク

PNGファイルの読み込みと表示に必要なチャンクで、デコーダが適切に処理する必要がある。

  - IHDR - 最も先頭に配置されるチャンクで、以下の順番で13バイトの情報が含まれる。
      - 画像の幅（4バイト）
      - 画像の高さ（4バイト）
      - [色深度](../Page/色深度.md "wikilink")（1バイト）
      - カラータイプ（1バイト）
      - 圧縮形式（1バイト）
      - フィルタ形式（1バイト）
      - [インターレース](../Page/インターレース.md "wikilink")形式（1バイト）
  - PLTE - カラーパレット定義。
  - IDAT - zlibにより圧縮されたイメージデータ。複数のIDATチャンクに分割することもできる。この場合ファイルサイズは若干増えるが、PNGをストリームとして生成することができるようになる。
  - IEND - イメージの終端を示す。

PLTEチャンクはカラータイプ 3 （[インデックスカラー](../Page/インデックスカラー.md "wikilink")）を使用するときに必須となる。カラータイプ 2 と 6 （トゥルーカラー及び、アルファ情報付きトゥルーカラー）の場合は任意、さらにカラータイプ0と4（[グレースケール](https://ja.wikipedia.org/wiki/グレースケール "wikilink")及び、アルファ情報付きグレースケール）の場合は存在してはいけない。

#### 補助チャンク

イメージについての付加情報を保持するための任意チャンク。

  - acTL - アニメーテッドPNGである事を示し、総フレーム数やループ回数を保持する。
  - bKGD - デフォルトの背景色を指定する。これは、単独のイメージビューアで表示するときなど、背景色が特に定まらない場合を想定している。ただし、Internet Explorer 6以前はアルファ値による透過表示をサポートせず、この値を背景色として使用する。
  - cHRM - [ホワイトバランス](../Page/ホワイトバランス.md "wikilink")を指定する。
  - fcTL - アニメーテッドPNGのフレーム制御情報を保持する。
  - fdAT - アニメーテッドPNGのフレーム画像データを保持する。
  - gAMA - [ガンマ補正](https://ja.wikipedia.org/wiki/ガンマ補正 "wikilink")値を指定する。
  - hIST - [ヒストグラム](../Page/ヒストグラム.md "wikilink")、またはイメージ内で使用されている各色の総量を保持する。
  - iCCP - [ICCカラープロファイルを保持する](https://ja.wikipedia.org/wiki/ICCプロファイル "wikilink")。
  - iTXt - [UTF-8](../Page/UTF-8.md "wikilink")フォーマットのテキストを保持する。圧縮・非圧縮、[IETF言語タグ](https://ja.wikipedia.org/wiki/IETF言語タグ "wikilink")を伴うことができる。
  - pHYs - ピクセルの物理サイズ、またはイメージの[アスペクト比](../Page/アスペクト比.md "wikilink")を指定する。
  - sBIT - 元データの有効なビット数を示す。
  - sPLT - イメージが使用する色を全てカバーできない時に、代替となるパレットを提示する。
  - sRGB - 標準的な[sRGBの色空間が使われていることを示す](../Page/色空間.md "wikilink")。
  - tEXt - [ISO 8859-1形式のテキストを保持する](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")。キーワードと対になるチャンクを複数持つことができる。テキストの圧縮は行われない。
  - tIME - イメージの最終更新日時を保持する。
  - tRNS - 透過色情報を保持する。ピクセル単位のアルファ値指定が必要ない場合に使用する。インデックスカラーのイメージについてはインデックスに結びつけるアルファ値、トゥルーカラーやグレースケールのイメージについては、完全に透過とみなす色を指定する。
  - zTXt - tEXtチャンクと同じ制限の圧縮テキスト。

### フィルタ処理

PNGのイメージデータはzlibにより圧縮されるが、画像の特徴を利用して圧縮の効率を良くするために、フィルタで事前に処理を行えるようになっている。（展開時には、逆のフィルタがかかる)

例えば、ピクセルの値が次のように並んでいたとする。

`100,101,102,103,104,105`

このデータには冗長な値が無く、このままDeflate圧縮を行っても効果は得られない。しかし例えば「左の値との差」をとると、データは以下のようになる。

`100,1,1,1,1,1`

この状態で圧縮すれば、最初の状態よりも高い効果が得られる。上記は極端な例であるが、このように事前に簡単な演算を行うことは、データによっては圧縮率の改善に役立つ。

PNGでは5種類のフィルタを定義している。

  - Sub
    左隣のピクセル値との差をとる（上記）。
  - Up
    真上のピクセル値との差をとる。
  - Average
    左隣と真上のピクセルの平均値との差をとる。
  - Paeth
    左隣、真上、左上の3つのピクセルからPaeth値を計算し、その値との差をとる。
  - None
    何もしない。

このフィルタは横一ライン毎に変更できる。どのフィルタをどこに使うかは使用する圧縮プログラムが選択できるため、プログラムによって同じ画像でも異なるサイズになりうる。

### 圧縮

圧縮アルゴリズムは[Deflate](../Page/Deflate.md "wikilink") (RFC 1951) を使用し、フォーマットは[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")形式 (RFC 1950) と定められている。DeflateのアルゴリズムそのものはPNGの仕様書には書かれていない。圧縮後のデータは、そのまま IDAT チャンクに格納される。

なおPNGはDeflate以外の圧縮形式もサポート出来るように設計されており、IHDRチャンクやiTXtチャンクには、使用する圧縮形式を明示するCompression methodフィールドがある。ただしVer1.2時点ではCompression methodフィールドで使える値はDeflateを示す一種類だけである。

### 開発者向けのツール

PNGを処理するための開発者向けライブラリとして[libpng](https://ja.wikipedia.org/wiki/libpng "wikilink")がある。これはPNG公式のライブラリであり、最も広く利用されている。C言語で開発されており、多くのプラットフォームで動作する。ライセンスはGPLよりも制限が緩やかである。

## 他のフォーマットとの比較

[thumbで作られたPNGの画像](https://ja.wikipedia.org/wiki/ファイル:Glasses_800_edit.png "wikilink")\]\]

### GIF との比較

GIF の代替物として開発された経緯があるため、GIFと比較されることが多い。主な差異は以下の通り。

  - ほとんどの画像でPNGはGIFより圧縮率が高い。
  - GIFは1色透過だが、PNGはアルファチャンネルを持ち半透明の表現が可能。
  - PNGはフルカラーが可能なため256色のGIFより精細な色表現が可能。
  - GIFはアニメーションをサポートしているが、PNGはサポートしていない（アニメーションにはPNGの発展フォーマットであるMNG/APNG形式を用いる）。
  - GIFと比較すると圧縮・展開に多少時間が掛かる（ただし前述の通り容量はGIFより小さいため、転送時間の短縮を加味すれば劣点とはならない。[サーバ側のプログラムが動的に画像を生成するような使用法では注意を要する](../Page/Webサーバ.md "wikilink")）。
  - インターレースGIFとインターレースPNG を比較すると、インターレースPNGの方が圧縮率が低い。
  - インターレース形式のアルゴリズムが異なり、GIFよりも早い段階で全体像が見える。

### JPEGとの比較

[thumb](https://ja.wikipedia.org/wiki/ファイル:Comparison_of_JPEG_and_PNG.png "wikilink")

[JPEG](../Page/JPEG.md "wikilink")は、主に写真的なイメージデータを[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")することでPNGよりも小さなファイルサイズに収めることができる。そのため、高画質に設定したJPEGと比較すると、ファイルサイズはJPEGの数倍（大抵は5〜10倍程度）になる。

PNGは、テキストや線画など色の境界がはっきりしたイメージに適している。線画と写真が混在している場合では、目的に応じてシャープな部分を重視する場合はPNG、ファイルサイズを重視する場合はJPEGを選ぶことができる。

JPEGは、不可逆圧縮方式でありが生じるため、編集中の一時データの保存には向かない。JPEGで保存をする段階で画像は劣化し、それを繰り返すたびに更に画像は劣化していく。

PNGは[Exifをサポートしていないが](../Page/Exchangeable_image_file_format.md "wikilink")、JPEGはExifをサポートしている。

### TIFFとの比較

PNGと[TIFFは](../Page/Tagged_Image_File_Format.md "wikilink")、画像を可逆圧縮または無圧縮により劣化なしで画像の保存が可能という点は共通している。PNGまたはTIFFはその可逆性を生かして、編集やレタッチイメージの一時保存に利用し、最終イメージのみをJPEGで出力すれば、複数のアプリケーションで画像編集を繰り返したとしても、ジェネレーションロスは1世代にとどめることができる。

PNGは[Exifをサポートしていないが](../Page/Exchangeable_image_file_format.md "wikilink")、TIFFはExifをサポートしている。

同じ画像を保存する際、ファイルサイズでは一般的にPNGに利点があるとされる。

## ブラウザの対応

前述の特許権問題によりGIF排斥運動が起こったが、GIFは依然として広く使われている。それは主に以下の理由からである。

  - 当時の[WebブラウザでPNGに正しく対応していないものがあった](../Page/ウェブブラウザ.md "wikilink")。
  - [広告](../Page/広告.md "wikilink")（[バナー](../Page/バナー.md "wikilink")）には当時、[GIFアニメ](https://ja.wikipedia.org/wiki/GIFアニメ "wikilink")がよく用いられたが、PNGの仕様そのものにはアニメーション機能が含まれていないため、代替することができない（MNGは多くのブラウザで未対応である）。
  - PNGの機能はweb上でフルに使われていない。例えば[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 6及びそれ以前のバージョンは複数のアルファチャンネルに対応していない。
  - GIFで間にあった。

Internet Explorerはバージョン6までアルファチャンネルを持つPNG画像を正しく描画できない。2006年11月にリリースされたバージョン7で、正確に描画できるようになった。（ただし[Photoshopで生成したPNG画像の場合](../Page/Adobe_Photoshop.md "wikilink")、gAMAチャンクへの不適切な記述のため正常に表示されないことがある）

PNGはGIFと同様な1色透過も扱え、こちらはInternet Explorer 5でも対応している。なお、IE5.5はアルファチャンネル付きPNGを正しく表示できる[ActiveX](../Page/ActiveX.md "wikilink")プラグイン (AlphaImageLoader) を搭載しているため、この機能を使うようHTMLファイルに記述すれば表示できる。ただしIEの設定によってはアルファチャンネルとして機能せず、また他ブラウザとの互換を考えると、わざわざこの機能を利用する価値はほとんど無い。

ユニシスの主張するLZW圧縮アルゴリズムに関する特許は、米国時間2003年6月20日をもって無効（期限切れ）になった。PNGはLZW圧縮アルゴリズム特許の有効期間内で全てのGIFファイルを代替するには至らなかった。特許問題が事実上消失したため、「**特許に抵触しない**GIFを代替可能なフォーマットのひとつ」としての存在意義は消失した。 結果としてPNGは「GIFを代替可能なフォーマットのひとつ」という見方ができる。

## ファイルサイズ

正しくエンコード処理を行ってメタデータを含まないように作成したPNG画像は、同じように処理して作成したGIF画像より小さくなるはずである。しかしPNGはGIFより機能が多いため、大きなサイズになってしまうことがある。

GIFは256色に制限されているため、多くのソフトはフォーマットの変換を行うとき自動的に256色に減色して保存する。そのためフルカラーの画像をPNGとGIFに保存した場合、GIFの方がサイズが小さくなる（かわりに画質は落ちている）。GIF同様256色のPNGを作ればGIFよりサイズが小さくなるにも関わらず、PNGは256色より多い色数を利用できるため変換時に自動で減色されない場合がある。その結果同じ画像をGIFにした場合よりサイズが大きくなってしまう。

[インターレース](../Page/インターレース.md "wikilink")PNGは[インターレース](../Page/インターレース.md "wikilink")GIFに比べ、圧縮率が低くファイルサイズが大きくなる場合が多い。また、インターレースPNGは通常のPNGより、ファイルサイズが大きくなりがちである。

ソフトウェアによっては、出力されるPNGファイルのサイズは必ずしも最適化されないため、ファイルサイズを減らすためにはPNG最適化ソフトウェアなどでPNGファイルを最適化するとよい。最適化のためのソフトウェアとしては、 [OptiPNG](http://optipng.sourceforge.net/)、[PNGOUT](http://advsys.net/ken/utils.htm)、[pngrewrite](https://entropymine.com/jason/pngrewrite/)、[Pngcrush](http://pmt.sourceforge.net/pngcrush/)などがある。また、Windows用ながらも[BlastPNG](http://omoikane.my-sv.net/BlastPNG.htm)のような複数の最適化ソフトウェアを一度に扱えるフロントエンドなどもある。

PNGは[JPEG](../Page/JPEG.md "wikilink")に取って代わるものではない。JPEGは[写真](../Page/写真.md "wikilink")の圧縮に適した非可逆圧縮方式であり、写真画像に限ってはJPEGのほうがファイルサイズが小さくなる。一方で、文字や線画などの保存はJPEGだと圧縮ノイズが目立ってしまうのでPNGのほうが適している上、ファイルサイズもかなり小さくなる。また、加工を繰り返す予定のある画像はJPEGでは劣化が進んでしまうのでPNG保存が望ましい。

## 出典

### 仕様書

## 関連項目

  - [MNG](../Page/Multiple-image_Network_Graphics.md "wikilink")
  - [APNG](../Page/Animated_Portable_Network_Graphics.md "wikilink")
  - [libpng](https://ja.wikipedia.org/wiki/libpng "wikilink")
  - [ICO (ファイルフォーマット)](https://ja.wikipedia.org/wiki/ICO_\(ファイルフォーマット\) "wikilink")

## 外部リンク

  - [PNGの公式サイト](http://www.libpng.org/pub/png/)
  - [GNU のウェブページに GIF ファイルが一つも無い理由](https://www.gnu.org/philosophy/gif.ja.html)（GNUプロジェクト）

[Category:ラスターグラフィックス・ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ラスターグラフィックス・ファイルフォーマット "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:可逆圧縮アルゴリズム "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  [Intro to PNG Features](http://www.libpng.org/pub/png/pngintro.html)
2.
3.
4.
5.  『[日本産業標準調査会：廃止規格検索 X4242](https://www.jisc.go.jp/app/jis/general/GnrDisuseJISStandardList?show&jisStdNo=X4242) [日本工業標準調査会](https://ja.wikipedia.org/wiki/日本工業標準調査会 "wikilink")。
6.
7.
8.   (リンク切れ - [Web Archiveによる過去の版](https://web.archive.org/web/20050624081635/http://tech.millto.net/~pngnews/kndh/PngSpec1.2/PNGcontents.html))
9.  （英語）