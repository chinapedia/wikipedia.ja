> この記事は[拡張ASCII](https://ja.wikipedia.org/wiki/拡張ASCII)から翻訳されています。


**拡張ASCII**(extended ASCIIもしくはhigh ASCII) は、他のものに加えて標準の7[ビット](../Page/ビット.md "wikilink")[ASCII](../Page/ASCII.md "wikilink")を含み、[8ビット](../Page/8ビット.md "wikilink")かそれより大きい[文字コード](../Page/文字コード.md "wikilink")を表す用語である。この用語の使用は批判されることがある。ASCII標準が128個より多くの文字を含むように更新されたとか、この用語は単一の符号化方式を曖昧さなしに識別するというような (どちらも真実ではない) 誤解を招きかねないためである。

## 拡張の理由

普及している[自然言語](../Page/自然言語.md "wikilink")で使われる文字の数はASCIIコードの制限された範囲をはるかに超えるため、それらの言語の処理を助けるために多数の拡張が使われてきた。英語圏外でのコンピュータと通信機器の市場は標準化団体がそれらに対応する最善の方法を熟考する時間が与えられるよりはるかに前から歴史的に開かれていたため、ASCIIへの互換性がない独自拡張は多数存在する。

ASCIIは7ビット符号でありほとんどのコンピュータはデータを8ビット[バイトで操作するので](../Page/バイト_\(情報\).md "wikilink")、多くの拡張は各バイトの8ビットすべてを使うことにより、追加で利用可能な128の符号を使用する。これは他の方法ではASCIIで容易に表現できない多くの言語を含む助けになるが、コンピュータが売られているすべての国の言語をカバーするにはまだ十分ではないため、これらの8ビット拡張でさえ多数の変種が必要だった。

## 独自拡張

非[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")メインフレームやミニコンには、とくに大学において各種の独自拡張が出現した。コモドールマイクロコンピュータは多くの図形記号を自社の非標準ASCII（[PETSCII](https://ja.wikipedia.org/wiki/PETSCII "wikilink")、1963年の最初のASCII標準に基づく）に追加した。IBMは異なる言語と文化のために、最初の[IBM PCと以後に製造された機種で](../Page/IBM_PC.md "wikilink")8ビット拡張ASCIIコードを導入した。IBMはそれらの文字集合を*[コードページ](../Page/コードページ.md "wikilink")*と呼び、自社で発明したものと他社で発明され使用されていた多くのものの両方に番号を割り当てた。そのため、文字集合をそれらのIBMコードページ番号で示すことが非常によくある。ASCII互換コードページにおいては、下位128個の文字は標準US-ASCIIの値を保持しており、異なったページ（もしくは文字の集合）を上位128個の文字で利用できた。たとえば、北米市場で組み立てられた[DOSコンピュータは](../Page/MS-DOS.md "wikilink")、フランス語、ドイツ語、および他の少数のヨーロッパ言語で必要なアクセント文字に加え、いくつかの罫線素片を含む[コードページ437](https://ja.wikipedia.org/wiki/コードページ437 "wikilink")を使っていた。より大きな文字集合は[英語](../Page/英語.md "wikilink")と[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")（フランスのコンピュータは通常[コードページ850](https://ja.wikipedia.org/wiki/コードページ850 "wikilink")を使うが）を組み合わせて書かれた文書の作成を可能にしたが、たとえば、英語と[ギリシア語](https://ja.wikipedia.org/wiki/ギリシア語 "wikilink")の組み合わせは不可能である（これにはコードページ737が必要である）。

[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) は[ISO 8859の草案に基づき](https://ja.wikipedia.org/wiki/ISO/IEC_8859 "wikilink")、字数を減らす代わりに文字とダイアクリティカルマークの組み合わせを増やした "Multinational Character Set" を開発した。これは[VT220](https://ja.wikipedia.org/wiki/VT220 "wikilink")および後継の DEC 製[端末](../Page/端末.md "wikilink")によってサポートされた。

## ISO 8859と独自拡張

最終的に、[ISOはこの標準を](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")8ビットASCII拡張の独自の集合を表す[ISO 8859としてリリースした](https://ja.wikipedia.org/wiki/ISO/IEC_8859 "wikilink")。もっとも有名なのはISOラテン1とも呼ばれる[ISO 8859-1だった](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")。これはほとんどの広く使われている西欧言語に十分な文字を含んでいた。他の言語用の変種も標準化された: 東欧言語用のISO 8859-2やキリル言語用のISO 8859-5などである。

ISO文字集合とコードページの注目に値する一つの違いは、ASCII[制御文字](../Page/制御文字.md "wikilink")の上位ビットをセットした値に対応する文字位置128から159が、ISO標準では明確に使われず未定義とされたことである。それらはしばしば独自拡張コードページでは印字可能文字に使われており、ほとんど汎用的なISO標準を破壊していた。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は後にISO 8859-1と互換性を保ちつつISOが未使用にしていた範囲に文字を追加した[上位集合](https://ja.wikipedia.org/wiki/上位集合 "wikilink")である[コードページ1252](https://ja.wikipedia.org/wiki/コードページ1252 "wikilink")を作成した。コードページ1252は英語版を含む西欧言語版[Microsoft Windowsの標準文字コードである](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。ISO 8859-1は[X Window Systemおよびほとんどの](../Page/X_Window_System.md "wikilink")[インターネット](../Page/インターネット.md "wikilink")標準で広く使われている文字コードである。

[アップルの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")は、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の下では、現在[Unicode](../Page/Unicode.md "wikilink")をデフォルトの文字コードとして使っている。[Classic Mac OSの下では](../Page/Classic_Mac_OS.md "wikilink")、[Mac OS Romanを使っていた](https://ja.wikipedia.org/wiki/Mac_OS_Roman "wikilink")。

## 文字集合の混乱

これらのASCII拡張は非常に多くの変種を持つため、ある特定のテキストでどの集合が使われているか識別することは、テキストを正しく解釈するために必要である。しかしながら、もっともよく使われる文字 (ASCIIの7ビット符号位置にあるもの) はすべての集合で共通なので（拡張ASCII以外でもほとんどの文字集合で共通である）、文字集合の正しい識別に失敗しても英文は問題なく読める。さらに、多くのインターネット標準はISO 8859-1を使い、OSシェアトップのWindowsの使うコードページ1252もISO 8859-1の上位集合であるため、多くの場合ISO 8859-1が予告なしに使われている。このため何も情報がなかった場合欧米ではISO 8859-1が使われている可能性が高く、デフォルトでこれを仮定すると多くの場合うまくいく。

多くのプロトコル、もっとも重要なのは[電子メール](../Page/電子メール.md "wikilink")と[HTTPにおいて](../Page/HyperText_Markup_Language.md "wikilink")、通信内容の文字コードは[IANAが割り当てた文字コード識別子でタグ付けしなければならない](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。

## Unicode

これらの問題の多くを解決するため[1991年](../Page/1991年.md "wikilink")に[Unicode](../Page/Unicode.md "wikilink")と呼ばれる提案がなされ、現在では広く受け入れられている。Unicodeは1,114,112 (= 2<sup>20</sup> + 2<sup>16</sup>) 個の符号位置を予約しており、現在それらの符号位置の101,000個以上に文字を割り当てている。最初の256個の符号は[ISO-8859-1](https://ja.wikipedia.org/wiki/ISO-8859-1 "wikilink")のものと正確に一致する。96,000個の符号位置の大多数は、現時点では、、およびの文字に使われている。

## 脚注

### 注釈

### 出典

## 関連項目

  - [IME](https://ja.wikipedia.org/wiki/IME "wikilink")

## 外部リンク

  - [Quick Key文字グリッド](http://quickkeydotnet.sourceforge.net/) あらゆる文字を1クリックで挿入できる
  - [Character Sets and Code Pages at the Push of a Button](http://www.i18nguy.com/unicode/codepages.html)
  - [AllCharsユーティリティ (Windows用)](http://allchars.zwolnet.com)
  - [Mac OS Xの国際化サポートに関するAppleのページ](http://developer.apple.com/intl/)
  - [Roman CzyborraによるUnicodeと拡張ASCIIの情報ページ](http://czyborra.com/)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink")