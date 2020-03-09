> この記事は[CID \(\)](https://ja.wikipedia.org/wiki/CID_\(\))から翻訳されています。


**CID**は、[アドビ社の](https://ja.wikipedia.org/wiki/アドビシステムズ "wikilink")[CIDフォント](https://ja.wikipedia.org/wiki/CIDフォント "wikilink")が内蔵するすべての文字（[文字コレクション](https://ja.wikipedia.org/wiki/文字コレクション "wikilink")）を識別するため、文字ごとに振られる一連の番号。

文字コレクションは言語ごとに定義され、その言語の主要な[文字集合](https://ja.wikipedia.org/wiki/文字集合 "wikilink")をサポートするために必要な文字をすべて含む。文字コレクションには「登録者-配列（-追補番号）」の形式で名前が付けられる。たとえばアドビ社が定めた日本語の表記に使われる文字コレクションの名称はAdobe-Japan1である。

## Adobe-Japan1

Adobe-Japan1は、[JIS X 0208や](https://ja.wikipedia.org/wiki/JIS_X_0208 "wikilink")[ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")(≒[Unicode](../Page/Unicode.md "wikilink"))などの公的な[文字コード](../Page/文字コード.md "wikilink")規格では（[異体字セレクタ](https://ja.wikipedia.org/wiki/異体字セレクタ "wikilink")を使わない限り）同じコードが与えられている[異体字](https://ja.wikipedia.org/wiki/異体字 "wikilink")の字形1つ1つに別々のCIDを割り当てている。実際のOS・アプリケーションとのやりとりは通常[フォント](https://ja.wikipedia.org/wiki/フォント "wikilink")に内蔵されている CMAPテーブル（CIDとUnicodeを相互に関連付けた対応表）を参照して行われるが、[Acrobat](https://ja.wikipedia.org/wiki/Adobe_Acrobat "wikilink")・[InDesign](https://ja.wikipedia.org/wiki/Adobe_InDesign "wikilink")（いずれも[アドビシステムズ](https://ja.wikipedia.org/wiki/アドビシステムズ "wikilink")社製品）・[日本語LaTeX](https://ja.wikipedia.org/wiki/LaTeX "wikilink")\[1\]（フリーソフト）などの[ソフトはCID番号を直接利用することがある](../Page/アプリケーションソフトウェア.md "wikilink")。

Adobe-Japan1の追補ごとの詳細は以下の通り。

  - Adobe-Japan1-0 : 1993年6月11日発表。8,284グリフ。JIS X 0208-1983まで、[OCFフォント](https://ja.wikipedia.org/wiki/OCFフォント "wikilink")で利用\[2\]。Adobe-Japan1-4でJIS X 0208-1983の規格票字形が追加されたことに伴いAdobe-Japan1-0の範囲にはJIS X 0208-1990の規格票字形を実装することになったが、当初は厳密な規格票字形の実装を求められていなかった。このためAdobe-Japan1-4以前から存在するフォントで互換性の問題が生じる場合がある\[3\]。
    Adobe-Japan1-1 : 1994年10月4日発表。8,359グリフ。富士通やNECのJIS X 0208実装に使われていた字体（おおむねJIS C 6226-1978に基づく）の拡張およびJIS X 0208-1990で追加された漢字の追加。
    Adobe-Japan1-2 : 1994年10月4日発表。8,720グリフ（CIDフォント）。IBM外字などの拡張により[マイクロソフト標準キャラクタセット](https://ja.wikipedia.org/wiki/マイクロソフト標準キャラクタセット "wikilink")をサポートした。
    Adobe-Japan1-3 : 2000年3月31日発表。9,354グリフ ([OpenType](https://ja.wikipedia.org/wiki/OpenType "wikilink") Std / StdN)。縦書き字形の拡張。漢字の追加はない。
    Adobe-Japan1-4 : 2000年3月31日発表。15,444グリフ (OpenType Pro / ProN)\[4\]。[Mac OS X v10.0で利用可](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.0 "wikilink")。過去のJIS X 0208の規格票字形すべてや、[JIS X 0221](https://ja.wikipedia.org/wiki/JIS_X_0221 "wikilink") 附属書1の[追加漢字集合に対応](https://ja.wikipedia.org/wiki/JIS_X_0221#日本文字部分レパートリ "wikilink")。
    Adobe-Japan1-5 : 2002年9月20日発表。20,317グリフ (Opentype Pr5 / Pr5N)\[5\]。Apple拡張（APGS）の取込み、[JIS X 0213](https://ja.wikipedia.org/wiki/JIS_X_0213 "wikilink"):2000、国語審議会「[表外漢字字体表](https://ja.wikipedia.org/wiki/表外漢字字体表 "wikilink")」など対応。[Mac OS X v10.2](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.2 "wikilink"), [10.3](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.3 "wikilink"), [10.4で利用可](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.4 "wikilink")。
    Adobe-Japan1-6 : 2004年6月11日発表。23,058グリフ (Opentype Pr6 / Pr6N)。[JIS X 0213](https://ja.wikipedia.org/wiki/JIS_X_0213 "wikilink"):2004\[6\]および[JIS X 0212への対応](https://ja.wikipedia.org/wiki/JIS_X_0212 "wikilink")。[U-PRESS](https://ja.wikipedia.org/wiki/U-PRESS "wikilink")の文字を追加\[7\]。[Mac OS X v10.5で利用可](https://ja.wikipedia.org/wiki/Mac_OS_X_v10.5 "wikilink")。

Adobe-Japan1-4 と Adobe-Japan1-5 の間に Apple が Mac OS X (10.1) で JIS X 0213 文字を拡張した **Apple Publishing Glyph Set**(APGS) もあるが、Adobe-Japan1-5 と同じものということになっている（実際にはAdobe-Japan1-5との間には僅かに違いがある\[8\]）。

## Adobe-Japan2

古いものでAdobe-Japan2もある。Adobe-Japan2-0はJIS X 0212に相当するが、Adobe-Japan1-6に統合され廃止された\[9\]。

## 日本語以外

Adobe-GB1（[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")）・Adobe-CNS1（[繁体字](https://ja.wikipedia.org/wiki/繁体字 "wikilink")中国語）・Adobe-Korea1（[朝鮮語](https://ja.wikipedia.org/wiki/朝鮮語 "wikilink")）など日本語以外の[CJK圏で使われる文字コレクションもあるが](https://ja.wikipedia.org/wiki/CJKV "wikilink")、Adobe-Japan1以外はおおむね公的な文字コード規格の文字をそのまま含んでいるだけであるため、Adobe-Japan1に比べると、さほど注目されていない（最新版はそれぞれAdobe-GB1-5（30,284グリフ）・Adobe-CNS1-6（19,156グリフ）・Adobe-Korea1-2（18,352グリフ））。

## 脚注

## 関連項目

  - [OpenType](https://ja.wikipedia.org/wiki/OpenType "wikilink")
  - [異体字セレクタ](https://ja.wikipedia.org/wiki/異体字セレクタ "wikilink")
  - [日本語フォントの比較](https://ja.wikipedia.org/wiki/日本語フォントの比較 "wikilink")
  - [游書体](https://ja.wikipedia.org/wiki/游書体 "wikilink")（游明朝体、游ゴシック体）
  - [花園フォント](https://ja.wikipedia.org/wiki/花園フォント "wikilink")
  - [源ノ明朝](https://ja.wikipedia.org/wiki/源ノ明朝 "wikilink")、[源ノ角ゴシック](https://ja.wikipedia.org/wiki/源ノ角ゴシック "wikilink")
  - [小塚明朝](https://ja.wikipedia.org/wiki/小塚明朝 "wikilink")、[小塚ゴシック](https://ja.wikipedia.org/wiki/小塚ゴシック "wikilink")
  - [ヒラギノ](https://ja.wikipedia.org/wiki/ヒラギノ "wikilink")
  - [リュウミン](https://ja.wikipedia.org/wiki/リュウミン "wikilink")
  - [金剛黒体](https://ja.wikipedia.org/wiki/金剛黒体 "wikilink") [1](https://www.dynacw.co.jp/king/)
  - [イワタU-PRESS](https://ja.wikipedia.org/wiki/イワタU-PRESS "wikilink") [2](https://www.iwatafont.co.jp/press/upress.html)
  - [新ゴ](https://ja.wikipedia.org/wiki/新ゴ "wikilink")、UD新ゴ
  - [ゴシックMB101](https://ja.wikipedia.org/wiki/ゴシックMB101 "wikilink")
  - [和田研フォント](https://ja.wikipedia.org/wiki/和田研フォント "wikilink")（和田研細丸ゴシック）

## 外部リンク

  - [Adobe - Font and Type Technology Center](http://www.adobe.com/devnet/font/#ckf)
    「Adobe-Japan1-6」の全収録文字一覧表が "Adobe-Japan1-6 Character Collection for CID-Keyed Fonts" として公開されている
  - [Adobe-Japan1-6文字コレクションに対応する日本語OpenType®フォントについて](http://www.adobe.com/jp/support/type/aj1-6.html)
  - [安岡 孝一. “Adobe-Japan1-6とUnicode─異体字処理と文字コードの現実”. 情報管理. Vol. 48, No. 8, (2005), 487-495 .](http://kanji.zinbun.kyoto-u.ac.jp/~yasuoka/publications/JST2005-11.pdf)
  - [Adobe-Japan1規格 - フォント専門サイト fontnavi](https://fontnavi.jp/zakkuri/303-adobe-japan1.aspx)
  - [Adobe-Japan1 漢字データベースプロジェクト](http://kanji-database.sourceforge.net/ivd/adobe-japan1.html)
  - [Adobe Technical Note \#5078: The Adobe-Japan1-6 Character Collection](https://www.adobe.com/content/dam/acom/en/devnet/font/pdfs/5078.Adobe-Japan1-6.pdf)
  - [aj16-kanji.txt GitHub](https://github.com/adobe-fonts/source-han-serif/blob/release/Resources/aj16-kanji.txt)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:Unicodeに存在しない文字](https://ja.wikipedia.org/wiki/Category:Unicodeに存在しない文字 "wikilink")

1.  [OTFパッケージ](http://psitau.kitunebi.com/)の利用で可能。
2.  OCFフォントの[グリフはCIDを持たないが](https://ja.wikipedia.org/wiki/字体 "wikilink")、グリフの内訳はAdobe-Japan1-0と等価
3.  [jfonts_Topics](http://www.jfonts.or.jp/main/seminar/to_070406_1.htm)
4.  [ヒラギノ](https://ja.wikipedia.org/wiki/ヒラギノ "wikilink")のPro（バージョン7.11以降）/ ProNは、Adobe-Japan1-5(Pr5 / Pr5N)に対応する。[ヒラギノOpenTypeのFAQ - 千都フォント](http://www.screen.co.jp/ga_product/sento/otffaq.html#a16)より。
5.
6.  [マイクロソフト](../Page/マイクロソフト.md "wikilink")は[Windows 8から](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、和文フォントについてはJIS X 0208-1990 (Pr6) には対応せず、JIS X 0213:2004 (Pr6N) にのみ対応することとなった。
7.  フリーダイヤル記号などの収容されていない字形も存在するため、完全な対応ではない。
8.  [Adobe-Japan1-4 & APGS実践情報](http://hp.vector.co.jp/authors/VA000964/aj14ziss.htm)
9.  Adobe-Japan2-1以降は元々存在しない。なお、実際には Adobe-Japan2-0 には含まれるグリフで、Adobe-Japan1-6 には含まれないグリフとしては、漢字3字が存在する。これについては、Adobe-Japan1-7 で追補される予定。