> この記事は[ISO-2022-JP](https://ja.wikipedia.org/wiki/ISO-2022-JP)から翻訳されています。


**ISO-2022-JP**は、[インターネット](../Page/インターネット.md "wikilink")上（特に[電子メール](../Page/電子メール.md "wikilink")）などで使われる日本の文字用の[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")。[ISO/IEC 2022の](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")[エスケープシーケンス](../Page/エスケープシーケンス.md "wikilink")を利用して[文字集合](../Page/文字集合.md "wikilink")を切り替える7[ビット](../Page/ビット.md "wikilink")のコードであることを特徴とする (アナウンス機能のエスケープシーケンスは省略される)。俗に「**JISコード**」と呼ばれることもある。

## 概要

[日本語](../Page/日本語.md "wikilink")表記への利用が想定されている[文字コード](../Page/文字コード.md "wikilink")であり、日本語の利用されるネットワークにおいて、日本の規格を応用したものである。また文字集合としては、日本語で用いられる[漢字](../Page/漢字.md "wikilink")、[ひらがな](https://ja.wikipedia.org/wiki/ひらがな "wikilink")、[カタカナ](https://ja.wikipedia.org/wiki/カタカナ "wikilink")はもちろん、[ラテン文字](../Page/ラテン文字.md "wikilink")、[ギリシア文字](../Page/ギリシア文字.md "wikilink")、[キリル文字](../Page/キリル文字.md "wikilink")なども含んでおり、[学術](https://ja.wikipedia.org/wiki/学術 "wikilink")や[産業](../Page/産業.md "wikilink")の分野での利用も考慮したものとなっている。規格名に、ISOの日本語の[言語コードである](https://ja.wikipedia.org/wiki/ISO_639#言語コード一覧 "wikilink")`ja`ではなく、[国・地域名コードの](../Page/国名コード.md "wikilink")`JP`が示されているゆえんである。

文字集合として[JIS X 0211のC](https://ja.wikipedia.org/wiki/JIS_X_0211 "wikilink")0集合（[制御文字](../Page/制御文字.md "wikilink")）、JIS X 0201のラテン文字集合、[ISO 646の国際基準版](https://ja.wikipedia.org/wiki/ISO/IEC_646 "wikilink")[図形文字](https://ja.wikipedia.org/wiki/図形文字 "wikilink")、[JIS X 0208の](../Page/JIS_X_0208.md "wikilink")[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")版 (JIS C 6226-1978) と[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")および[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")版が利用できる。JIS X 0201の片仮名文字集合は利用できない。[1986年](../Page/1986年.md "wikilink")以降、日本の電子メールで用いられてきた[JUNET](../Page/JUNET.md "wikilink")コードを、[村井純](../Page/村井純.md "wikilink")、[Mark Crispinおよび](https://ja.wikipedia.org/wiki/w:Mark_Crispin "wikilink")[Erik van der Poelが](https://ja.wikipedia.org/wiki/Erik_van_der_Poel "wikilink")1993年に[RFC化したもの](../Page/Request_for_Comments.md "wikilink") (RFC 1468)。後にJIS X 0208:1997の附属書2として[JISに規定された](../Page/日本産業規格.md "wikilink")。[MIMEにおける文字符号化方式の識別用の名前として](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink")[IANAに登録されている](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。

なお、符号化の仕様については[ISO/IEC 2022\#ISO-2022-JPも参照](https://ja.wikipedia.org/wiki/ISO/IEC_2022#ISO-2022-JP "wikilink")。

## 類似の符号化方式

「ISO-2022-JP」に類似した符号化方式として以下のようなものがある。なお、一部は MIME で用いる文字符号化方式として IANA が登録している。

  - ISO-2022-JP-1
    RFC 2237。ISO-2022-JPを拡張し、ISO-2022-JPの文字集合に加え、[JIS X 0212を利用できるようにしたもの](../Page/JIS_X_0212.md "wikilink")。
  - ISO-2022-JP-2
    RFC 1554。ISO-2022-JPを拡張し、ISO-2022-JPの文字集合に加え、JIS X 0212、[KS X 1001](../Page/KS_X_1001.md "wikilink")、[GB 2312](../Page/GB_2312.md "wikilink")、[ISO 8859-1](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")、[ISO 8859-7を利用できるようにしたもの](https://ja.wikipedia.org/wiki/ISO/IEC_8859-7 "wikilink")。
  - ISO-2022-JP-3
    [JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2000の附属書2に記述される符号化表現で、ISO-2022-JPの漢字集合をJIS X 0213に変えるなどしたもの。IANA登録簿への登録が提案されたが、RFC 2278（当時。RFC 2978により廃止された）の手続きに従っていない（いっぺんに複数の文字コードを登録する手続きは存在しないのに6つ同時に申請されている）などの理由により却下された\[1\]。
  - [ISO-2022-JP-2004](https://ja.wikipedia.org/wiki/ISO-2022-JP-2004 "wikilink")
    JIS X 0213:2004の附属書2に記述される符号化表現。ISO-2022-JP-3の漢字をJIS X 0213:2004に改めたもの。IANA登録簿への登録はまだされていない。

## ISO-2022-JPと非標準的拡張使用

「JISコード」（または「ISO-2022-JP」）というコード名の規定下では、その仕様通りの使用が求められる。しかし、[Windows OS上では](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、実際には[CP932コード](../Page/Microsoftコードページ932.md "wikilink")（[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[Shift_JIS](../Page/Shift_JIS.md "wikilink")を拡張した亜種。ISO-2022-JP規定外文字が追加されている。）による独自拡張（の文字）を断りなく使う[アプリケーションが多い](../Page/アプリケーションソフトウェア.md "wikilink")。 この例として[Internet Explorerや](../Page/Internet_Explorer.md "wikilink")[Outlook Expressがある](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")。また、[EmEditor](../Page/EmEditor.md "wikilink")、[秀丸エディタ](../Page/秀丸エディタ.md "wikilink")や[Thunderbirdのようなマイクロソフト以外のWindowsアプリケーションでも同様の場合がある](../Page/Mozilla_Thunderbird.md "wikilink")。この場合、ISO-2022-JPの範囲外の文字を使ってしまうと、異なる製品間では未定義不明文字として認識されるか、もしくは[文字化け](../Page/文字化け.md "wikilink")を起こす原因となる。そのため、Windows用の[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")であっても独自拡張の文字を使用すると警告を出したり、あえて使えないように制限しているものも存在する。さらにはISO-2022-JPの範囲内であってもCP932は非標準文字（FULLWIDTH TILDE等）を持つので[文字化け](../Page/文字化け.md "wikilink")の原因になり得る。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")はバージョン6以降で、通常のISO-2022-JP形式の実装のほか、「x-windows-iso2022jp」というコード名でマイクロソフトCP932ベースの拡張ISO-2022-JPに対応している\[2\]。

また、符号化方式名をISO-2022-JPとしているのに、文字集合としてはJIS X 0212（補助漢字）や[JIS X 0201の片仮名文字集合](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")（いわゆる[半角カナ](../Page/半角カナ.md "wikilink")）をも符号化している例があるが、ISO-2022-JPではこれらの文字を許容していない。これらの符号化は独自拡張の実装であり、中には[ISO/IEC 2022の仕様に準拠すらしていないものもある](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")\[3\]。従って受信側の[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")がこれらの独自拡張に対応していない場合、その文字あるいはその文字を含む行、時にはテキスト全体が文字化けすることがある。

## 参考資料

  -
  -
  -
  -
  -

<references/>

[Category:ISO標準](https://ja.wikipedia.org/wiki/Category:ISO標準 "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.   - ISO-2022-JP-3登録の却下の経緯。
2.
3.