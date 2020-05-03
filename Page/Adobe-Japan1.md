> この記事は[Adobe-Japan1](https://ja.wikipedia.org/wiki/Adobe-Japan1)から翻訳されています。


**Adobe-Japan1**（アドビジャパンワン\[1\]\[2\]、略称: AJ1, A-J1）は、[アドビが定めた](../Page/アドビシステムズ.md "wikilink")[日本語](../Page/日本語.md "wikilink")の文字コレクション（[文字集合](../Page/文字集合.md "wikilink")）で、[フォント](../Page/フォント.md "wikilink")メーカー各社の製品が準拠する[DTP](../Page/DTP.md "wikilink")市場の[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっている\[3\]。2019年時点で八つの追補があり、最新版の**Adobe-Japan1-7**は、2万3060[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")（字形、文字）を収録する。収録する全ての文字に**CID**（Character IDentifier, Character ID）と呼ばれる一連の識別番号を振る。

## 文字コレクション

**文字コレクション**（character collection）は、CIDと文字の標準化されたセット\[4\]を指し、言語・書記体系（用字系）ごとに定義される。[モリサワ](../Page/モリサワ.md "wikilink")フォント用語集によると「[文字セットとほぼ同義](../Page/文字集合.md "wikilink")」だが、「公的な規格としてよりは、プライベートな規格を指していうことが多いよう」\[5\]だとされる。

文字コレクションには「登録者-配列（-追補番号）」の形式で名前が付けられる。Adobe-Japan1-7の場合、Adobeが登録者、Japan1が配列、7が追補番号を示す。

## 公的規格との違い

出版・印刷業界には、[JIS X 0208や](../Page/JIS_X_0208.md "wikilink")[ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")≒[Unicode](../Page/Unicode.md "wikilink")といった公的規格の文字セットが区別せず[包摂している](../Page/包摂_\(文字コード\).md "wikilink")[異体字](https://ja.wikipedia.org/wiki/異体字 "wikilink")を区別して使う需要が根強くある。JIS X 0208や[JIS X 0213では](../Page/JIS_X_0213.md "wikilink")、国の漢字施策の影響などで規格の改正の際に例示字形を変更したことがたびたびあった。このほか[IBM拡張文字](https://ja.wikipedia.org/wiki/IBM拡張文字 "wikilink")などのベンダ拡張文字セットや、印刷業界で使われてきた文字セットでは、例示字形にない異体字やそもそもJIS漢字にない文字を取り込んでいる。Adobe-Japan1ではこれらの字形を収集し、公的規格の[コードポイントとは別にCIDを割り振って区別できるようにしている](https://ja.wikipedia.org/wiki/符号点 "wikilink")。

## CIDの参照法

実際の[OS](../Page/オペレーティングシステム.md "wikilink")・アプリケーションとのやりとりは通常[フォント](../Page/フォント.md "wikilink")に内蔵されたCMapテーブル（CIDと[Unicode](../Page/Unicode.md "wikilink")を相互に関連付けた対応表）を参照して行われるが、[Acrobat](../Page/Adobe_Acrobat.md "wikilink")・[InDesign](../Page/Adobe_InDesign.md "wikilink")（いずれもアドビ製品）・[日本語LaTeX](../Page/LaTeX.md "wikilink")\[6\]（フリーソフト）などの[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")はCID番号を直接利用することがある。

## 追補

Adobe-Japan1の追補ごとの詳細は以下の通り。

  - Adobe-Japan1-0 : 1993年6月11日発表。8284[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")。JIS X 0208-1983まで、[OCFフォント](../Page/OCFフォント.md "wikilink")で利用\[7\]。Adobe-Japan1-4でJIS X 0208-1983の規格票字形が追加されたことに伴いAdobe-Japan1-0の範囲にはJIS X 0208-1990の規格票字形を実装することになったが、当初は厳密な規格票字形の実装を求められていなかった。このためAdobe-Japan1-4以前から存在するフォントで互換性の問題が生じる場合がある\[8\]。
    Adobe-Japan1-1 : 1994年10月4日発表。8359グリフ。富士通やNECのJIS X 0208実装に使われていた字体（おおむねJIS C 6226-1978に基づく）の拡張およびJIS X 0208-1990で追加された漢字の追加。
    Adobe-Japan1-2 : 1994年10月4日発表。8,720グリフ（CIDフォント）。IBM外字などの拡張により[マイクロソフト標準キャラクタセット](../Page/マイクロソフト標準キャラクタセット.md "wikilink")をサポートした。
    Adobe-Japan1-3 : 2000年3月31日発表。9354グリフ ([OpenType](../Page/OpenType.md "wikilink") Std / StdN)。縦書き字形の拡張。漢字の追加はない。
    Adobe-Japan1-4 : 2000年3月31日発表。1万5444グリフ (OpenType Pro / ProN\[9\])。[Mac OS X v10.0で利用可](../Page/Mac_OS_X_v10.0.md "wikilink")。過去のJIS X 0208の規格票字形すべてや、[JIS X 0221附属書](../Page/JIS_X_0221.md "wikilink")1の[追加漢字集合に対応](https://ja.wikipedia.org/wiki/JIS_X_0221#日本文字部分レパートリ "wikilink")。
    Adobe-Japan1-5 : 2002年9月20日発表。2万0317グリフ (OpenType Pr5 / Pr5N\[10\])。[アップル拡張](../Page/アップル_\(企業\).md "wikilink")（APGS）の取り込み、[JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2000、国語審議会「[表外漢字字体表](https://ja.wikipedia.org/wiki/表外漢字字体表 "wikilink")」などに対応。[Mac OS X v10.2](../Page/Mac_OS_X_v10.2.md "wikilink"), [10.3](../Page/Mac_OS_X_v10.3.md "wikilink"), [10.4で利用可](../Page/Mac_OS_X_v10.4.md "wikilink")。
    Adobe-Japan1-6 : 2004年6月11日発表。2万3058グリフ (OpenType Pr6 / Pr6N)。[JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2004および[JIS X 0212への対応](../Page/JIS_X_0212.md "wikilink")。[U-PRESS](../Page/U-PRESS.md "wikilink")の文字を追加\[11\]。[Mac OS X v10.5で利用可](../Page/Mac_OS_X_v10.5.md "wikilink")。
    Adobe-Japan1-7 : 2019年4月1日発表。2万3060グリフ (OpenType Pr**6** / Pr**6**N\[12\])。[元号](../Page/元号.md "wikilink")「[令和](https://ja.wikipedia.org/wiki/令和 "wikilink")」を表す漢字2文字からなる合字（「㋿」 U+32FF）の横組み用・縦組み用2グリフが追加された。

Adobe-Japan1-4とAdobe-Japan1-5の間に[アップルが](../Page/アップル_\(企業\).md "wikilink") Mac OS X (10.1)でJIS X 0213文字を拡張した**Apple Publishing Glyph Set** (APGS)もあるが、Adobe-Japan1-5と同じものということになっている（実際にはAdobe-Japan1-5との間には僅かに違いがある\[13\]）。

## Adobe-Japan1以外のCJK文字コレクション

古いもので**Adobe-Japan2**もある。Adobe-Japan2-0はJIS X 0212に相当するが、Adobe-Japan1-6に統合され廃止された。Adobe-Japan2-1以降はもともと存在しない。なお実際には Adobe-Japan2-0には含まれ、Adobe-Japan1-6には含まれないグリフとして、漢字3字（暀、殩、汴のJIS X 0212規格票例示字形）が存在する。これについては、Adobe-Japan1-7で追補される見込みであった\[14\]が、前述の通り、Adobe-Japan1-7では「令和」合字のみが追加された。

日本語以外の[CJK圏で使われる文字コレクションに](../Page/CJKV.md "wikilink")、Adobe-GB1（[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")）・Adobe-CNS1（[繁体字](../Page/繁体字.md "wikilink")中国語）・Adobe-KR（[朝鮮語](../Page/朝鮮語.md "wikilink")）がある。最新版はそれぞれ次の通り。

  - Adobe-GB1-5 : 3万0284グリフ、2005年12月4日\[15\]
    Adobe-CNS1-7 : 1万9179グリフ、2017年7月4日\[16\]
    Adobe-KR-9 : 2万2897グリフ、2018年7月19日\[17\]

## 脚注

## 関連項目

  - [OpenType](../Page/OpenType.md "wikilink")
  - [異体字セレクタ](../Page/異体字セレクタ.md "wikilink")
  - [小塚明朝](https://ja.wikipedia.org/wiki/小塚明朝 "wikilink")…Adobe-Japan1に関する資料でグリフを示すのに使われるアドビの[明朝体](../Page/明朝体.md "wikilink")フォント
  - [U-PRESS](../Page/U-PRESS.md "wikilink")…[共同通信社](../Page/共同通信社.md "wikilink")による文字セット

## 外部リンク

  - [Adobe - Font and Type Technology Center](http://www.adobe.com/devnet/font/#ckf)
    「Adobe-Japan1-6」の全収録文字一覧表が “Adobe-Japan1-6 Character Collection for CID-Keyed Fonts” として公開されている
  - [安岡 孝一. “Adobe-Japan1-6とUnicode─異体字処理と文字コードの現実”. 情報管理. Vol. 48, No. 8, (2005), 487-495 .](http://kanji.zinbun.kyoto-u.ac.jp/~yasuoka/publications/JST2005-11.pdf)
  - [Adobe-Japan1規格 - フォント専門サイト fontnavi](https://fontnavi.jp/zakkuri/303-adobe-japan1.aspx)
  - [Adobe-Japan1 漢字データベースプロジェクト](http://kanji-database.sourceforge.net/ivd/adobe-japan1.html)
  - [Adobe Technical Note \#5078: The Adobe-Japan1-6 Character Collection](https://www.adobe.com/content/dam/acom/en/devnet/font/pdfs/5078.Adobe-Japan1-6.pdf)
  - [The Adobe-Japan1-7 Character Collection](https://github.com/adobe-type-tools/Adobe-Japan1/raw/master/Adobe-Japan1-7.pdf)
  - [aj16-kanji.txt GitHub](https://github.com/adobe-fonts/source-han-serif/blob/release/Resources/aj16-kanji.txt)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink")

1.  『一〇〇年目の書体づくり : 「秀英体平成の大改刻」の記録』大日本印刷、2013年 ISBN 978-4-88752-257-2 138ページ
2.  『デジタル大辞泉』「Adobe-Japan1」項 [コトバンク『デジタル大辞泉』「Adobe-Japan1」項](https://kotobank.jp/word/AdobeJapan1-1824513)
3.  [モリサワ フォント用語集「文字セットとAdobe Japan」](https://www.morisawa.co.jp/culture/dictionary/1983)
4.  [Ken Lunde著](https://ja.wikipedia.org/wiki/ケン・ランディ "wikilink")、小松章・逆井克己訳『CJKV 日中韓越情報処理』[オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、2002年 ISBN 9784873111087、293ページ
5.  [モリサワ フォント用語集「文字コレクション」](https://www.morisawa.co.jp/culture/dictionary/1947)
6.  [OTFパッケージ](http://psitau.kitunebi.com/)の利用で可能。
7.  OCFフォントのグリフはCIDを持たないが、グリフの内訳はAdobe-Japan1-0と等価
8.
9.  [ヒラギノ](../Page/ヒラギノ.md "wikilink")のPro（バージョン7.11以降）/ ProNは、Adobe-Japan1-5(Pr5 / Pr5N)に対応する。[ヒラギノOpenTypeのFAQ - 千都フォント](http://www.screen.co.jp/ga_product/sento/otffaq.html#a16)より。
10.
11. フリーダイヤル記号などの収容されていない字形も存在するため、完全な対応ではない。
12. [Adobe-Japan1-7 文字コレクション OpenType/CFF フォント命名規則](https://github.com/adobe-type-tools/Adobe-Japan1/blob/master/README-JP.md#opentypecff-フォント命名規則)
13. [Adobe-Japan1-4 & APGS実践情報](http://hp.vector.co.jp/authors/VA000964/aj14ziss.htm)
14. [The Adobe-Japan1-6 Character Collection](https://www.adobe.com/content/dam/acom/en/devnet/font/pdfs/5078.Adobe-Japan1-6.pdf) 60ページ
15. [Adobe-GB1](https://github.com/adobe-type-tools/Adobe-GB1/)
16. [Adobe-CNS1](https://github.com/adobe-type-tools/Adobe-CNS1/)
17. [Adobe-KR](https://github.com/adobe-type-tools/Adobe-KR/)