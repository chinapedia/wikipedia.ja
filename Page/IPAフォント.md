> この記事は[IPAフォント](https://ja.wikipedia.org/wiki/IPAフォント)から翻訳されています。


**IPAフォント**（アイピーエイ フォント）とは、[独立行政法人](../Page/独立行政法人.md "wikilink")[情報処理推進機構](../Page/情報処理推進機構.md "wikilink") (IPA) によって配布されている[コンピュータ](../Page/コンピュータ.md "wikilink")用の[フォント](../Page/フォント.md "wikilink")セットの1つであり、一般ユーザーの日常的な印刷に使用できる品位の日本語[アウトラインフォント](https://ja.wikipedia.org/wiki/アウトラインフォント "wikilink")である。

2009年（平成21年）公開の、IPAexフォントVer.001以降およびIPAフォントVer.003以降は、[オープンソースの定義](https://ja.wikipedia.org/wiki/オープンソースの定義 "wikilink")に合致したライセンスでライセンスされている。

## 種類

### IPAフォント

IPAフォントは以下の書体で構成されている（括弧内は英語環境での表記）。

  - IPA明朝 (IPAMincho) ……[固定幅フォント](../Page/等幅フォント.md "wikilink")。
  - IPA P明朝 (IPAPMincho) ……[可変幅フォント](../Page/プロポーショナルフォント.md "wikilink")。
  - IPAゴシック (IPAGothic) ……固定幅フォント。
  - IPA Pゴシック (IPAPGothic) ……可変幅フォント。

[TrueType](../Page/TrueType.md "wikilink")アウトラインの[OpenType](../Page/OpenType.md "wikilink")フォントであり、[JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2004に準拠している。ただし、一部のOSで正常に認識されないという問題があったためにVer.003.02からはフォントファイルの拡張子が".otf"から".ttf"に変更されている\[1\]。

なお、2008年（平成20年）2月にリリースされたバージョン 002 まではTrueTypeフォントであり、[ビットマップフォント](https://ja.wikipedia.org/wiki/ビットマップフォント "wikilink")のデータを含んでいた。また次の「IPA UIゴシック」が含まれていた。

  - IPA UIゴシック (IPAUIGothic) ……可変幅フォント。

### IPAexフォント

2010年2月26日には、「IPAexフォント」（IPAex明朝、IPAexゴシック）が公開された。[TrueType](../Page/TrueType.md "wikilink")アウトラインの[OpenType](../Page/OpenType.md "wikilink")フォントである。

固定幅と変動幅のフォントを分離していた従来のIPAフォントとは異なり、日本語文書作成時の慣例に沿って、和文文字（仮名、約物、漢字）を固定幅、欧文文字を変動幅として単一のフォントに統合されたのが特徴である\[2\]。初期状態では和文は等幅だが、対応アプリケーションではOpenTypeのレイアウトタグで和文も変動幅（プロポーショナル幅）に切り替えることができる。

Unicodeの[異体字セレクタ](../Page/異体字セレクタ.md "wikilink")であるIVS（[Adobe-Japan1](../Page/Adobe-Japan1.md "wikilink")コレクションの一部）にも対応しており、[JIS X 0213:2004で例示字形が変更される以前の字形](../Page/JIS_X_0213.md "wikilink")（いわゆるJIS90の字形）を、Ver.002.01の時点で352文字サポートしている。また、Ver.003.01ではIPAexフォントに収録している[CJK互換漢字](https://ja.wikipedia.org/wiki/CJK互換漢字 "wikilink")93文字に[SVSを実装した](https://ja.wikipedia.org/wiki/異体字セレクタ#種類 "wikilink")\[3\]。

### IPAmj明朝

2011年10月には、「IPAmj明朝」が公開された。[TrueType](../Page/TrueType.md "wikilink")アウトラインの[OpenType](../Page/OpenType.md "wikilink")フォントであり、文字情報基盤整備事業の文字情報基盤 文字情報一覧表（[MJ文字](https://ja.wikipedia.org/wiki/MJ文字 "wikilink")情報一覧表）にある、58,862文字に及ぶ漢字のグリフが収録されている。

[異体字セレクタ](../Page/異体字セレクタ.md "wikilink")のIVSを利用することで、Moji_Johoコレクションにある異体字約1万通りが利用できる。ただし利用するためには、[Microsoft Word 2007](../Page/Microsoft_Word.md "wikilink") 以降や[一太郎 2014](../Page/一太郎.md "wikilink") 以降などといった、IVSに対応したアプリケーションが必要である。

IPAはこのフォントを「人名の表記等で、細かな字形の差異を特別に使い分ける必要のある業務等での活用を想定」しているとしており、一般的な用途にはこれのかわりに IPAexフォントの使用を推奨している。

2017年12月には、[ISO/IEC 10646(UCS)の第](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")5版と[IVDの新版が発行され](https://ja.wikipedia.org/wiki/異体字セレクタ#種類 "wikilink")、文字情報基盤整備事業のすべての漢字の規格化が完了した\[4\]\[5\]\[6\]。2018年1月にはこれらの規格に対応したVer.005.01がリリースされた。なおこのバージョンでは、[変体仮名](../Page/変体仮名.md "wikilink")についてもUnicode 10.0で定義された符号位置に基づき符号付けが行われている\[7\]。

## 概要

IPAフォントは株式会社タイプバンクがIPAに納入したもので、フォントデザイナーの林隆男によってデザインされたTB明朝・ゴシックがベースとなっている\[8\]\[9\]。

### 開発の背景

2003年11月28日、情報処理推進機構の前身である情報処理振興事業協会は無償使用可能な日本語フォント一式の入札公告を行った\[10\]\[11\]。

2004年、IPAの2003年度オープンソフトウェア活用基盤整備事業「オープンソースGISプラットフォームの開発」\[12\]の成果物である[GRASS GIS](https://ja.wikipedia.org/wiki/GRASS_GIS "wikilink")、[MapServer](https://ja.wikipedia.org/wiki/MapServer "wikilink")、[PostGIS](https://ja.wikipedia.org/wiki/PostGIS "wikilink")に添付される形でIPAフォントが公開された\[13\]。当初のライセンスでは、再配布に当たっては、このフォントがIPAフォントであることを明示する必要があり、またその派生物を改変し再配布する場合にも適用された。IPAフォント自体の単体配布は認められておらず、IPAフォントが含まれているソフトウェア（GRASSなど）に同梱して配布する必要があった。なおIPAフォントは利用範囲について明記されていないが、GRASS開発元であるオークニーの担当者はGRASS以外からの利用についても問題ないとの見解を示している\[14\]。

### 単体配布版

2007年10月1日、一般利用者向けにIPAフォント単体の無償配布が開始された。新たに定められた一般利用者向けの使用許諾契約書（[エンド・ユーザ・ライセンス](https://ja.wikipedia.org/wiki/ソフトウェア利用許諾契約 "wikilink")）の条件では、（商用・非商用を問わず）そのままの形でフォントファイルの複製・再配布が可能となったものの、フォントのデザインを変更するなどの改変は認められていなかった\[15\]\[16\]。つまり、GRASSなどの成果物に添付されたフォントは改変したものを再同梱し配布することが可能だが、単体配布版については不可だった。

IPAはその後、2008年10月に「IPAフォント使用許諾契約書の改訂作業および英語版作成作業」事前確認公募を行い、ライセンスの改訂作業をおこなった\[17\]。

### OSI認定ライセンス版

2009年4月20日、IPAフォント Ver.003が配布開始された\[18\]\[19\]。この版から、[オープンソースの定義](https://ja.wikipedia.org/wiki/オープンソースの定義 "wikilink")に合致していると[Open Source Initiativeに認定された](../Page/Open_Source_Initiative.md "wikilink")「IPAフォントライセンス」が適用された。同ライセンスでは改変の条件として、派生物にはIPAの名称を使用してはならない、オリジナルのIPAフォントに戻せる方法を提供しなければならない、といった制約を課している\[20\]。

## Linux ディストリビューションでの収録など

### Debian GNU/Linux

まず、2009年5月、[Debian](../Page/Debian.md "wikilink") GNU/Linux不安定版の non-free セクションに単体配付版が収録され配布されるようになった\[21\]。2011年2月現在、IPAフォントはテスト版や安定版においても公式な配布が行われている。JIS X 0213:2004 版以外に、一部グリフが異なる [JIS X 0208](../Page/JIS_X_0208.md "wikilink"):1997 版も用意されている。さらに、IPAexフォントの配布が追加されている。Ubuntuで作られたTakaoフォントも入っている。

### Fedora

[Fedora](../Page/Fedora.md "wikilink") 11よりオープンソース版がipa-\*-fontsの名称の[rpmパッケージで収録されるようになった](../Page/RPM_Package_Manager.md "wikilink")\[22\]。デフォルトではインストールされず[yumなどを使いユーザーが任意でインストールを行う](https://ja.wikipedia.org/wiki/Yellow_dog_Updater,_Modified "wikilink")。

### Ubuntu

Ubuntu 10.04 以降の日本語ローカライズ版においては、IPAフォントから派生した「Takaoフォント」がインストールされている。

8.04 (Hardy Heron) 以前は[Ubuntu](../Page/Ubuntu.md "wikilink")の日本語ローカライズ版においてIPAフォントがデフォルトで収録され利用可能であったが、8.10 (Intrepid Ibex) から日本語フォントは「[VLゴシック](https://ja.wikipedia.org/wiki/VLゴシック "wikilink")フォントファミリ」が標準となり、IPAフォントはデフォルトでは収録されなくなった。これは、当時のIPAフォントが単体での改変・再配布を認めないことが理由であり、利用する場合はセットアップヘルパなどを通じてユーザ自身でインストールする必要があった\[23\]。

その後オープンソース版がリリースされたことにより、Ubuntuのリポジトリからインストールできるようになり、Ubuntu Japanese Teamで再び日本語標準フォントとしての採用が検討されたが、そのままでは「一部のアプリケーションで半角幅の文字が全角幅で表示される」「日本語変換の未確定文字列に下線が表示されない」などの問題があり、改変したフォントの再配布にあたってはライセンスの制限で「IPAフォント」の名称が使えないため、IPAフォントの採用そのものはまたも見送られることとなった。代替策として同プロジェクトは自身で派生フォント「Takaoフォント」の開発・保守を行うことにした。\[24\]

## 派生フォント

### Takaoフォント

Ubuntu Japanese Teamが開発・保守を行っている。名称はIPAフォントのベースであるTB明朝・ゴシックのデザイナー林隆男に由来する。2010年2月15日に最初のリリースが公開された\[25\]。

### MigMixフォント・Miguフォント

[M<sup>+</sup> FONTSにIPAゴシックのグリフを加えた](https://ja.wikipedia.org/wiki/M+_FONTS "wikilink")、「MigMix」「Migu」フォントがある\[26\]。

## 脚注

## 関連項目

  - [情報処理推進機構](../Page/情報処理推進機構.md "wikilink") (IPA)
  - [フォント](../Page/フォント.md "wikilink")
  - [IPAモナーフォント](https://ja.wikipedia.org/wiki/IPAモナーフォント "wikilink")（[アスキーアート](../Page/アスキーアート.md "wikilink")に対応するようにIPAフォントを改変したフォント）
  - [日本語フォントの比較](https://ja.wikipedia.org/wiki/日本語フォントの比較 "wikilink")

## 外部リンク

  - [IPAフォント 公式サイト](http://ipafont.ipa.go.jp/) - IPAフォントのダウンロードが可能
  - [文字情報基盤整備事業](http://mojikiban.ipa.go.jp/) - IPAmj明朝のダウンロードが可能
  - [IPA Font License (Open Source Initiative)](http://www.opensource.org/licenses/ipafont.html)
  - [IPAフォントプロジェクト OSDN](http://sourceforge.jp/projects/ipafonts/)
  - [Takaoフォント](https://launchpad.net/takao-fonts)

[Category:オープンソースの書体](https://ja.wikipedia.org/wiki/Category:オープンソースの書体 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21. <http://lists.debian.or.jp/debian-devel/200905/msg00001.html>
22.
23.
24.
25.
26. [M<sup>+</sup>とIPAの合成フォント](http://mix-mplus-ipa.sourceforge.jp/)