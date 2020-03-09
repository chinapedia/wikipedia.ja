> この記事は[UTF-8](https://ja.wikipedia.org/wiki/UTF-8)から翻訳されています。


**UTF-8**（ユーティーエフはち、ユーティーエフエイト）は[ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink") (UCS) と[Unicode](../Page/Unicode.md "wikilink")で使える8ビット符号単位（1～4 byte の可変長）の[文字符号化形式及び文字符号化スキーム](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")。

正式名称は、ISO/IEC 10646では “UCS Transformation Format 8”、Unicodeでは “Unicode Transformation Format-8” という。両者はISO/IEC 10646とUnicodeのコード重複範囲で互換性がある。[RFCにも仕様がある](../Page/Request_for_Comments.md "wikilink")\[1\]。

2バイト目以降に「/」などの[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字が現れないように工夫されていることから、**UTF-FSS** (File System Safe) ともいわれる。旧名称はUTF-2。

UTF-8は、データ交換方式・ファイル形式として一般的に使われる傾向にある。

当初は、[ベル研究所](../Page/ベル研究所.md "wikilink")において[Plan 9で用いるエンコードとして](../Page/Plan_9_from_Bell_Labs.md "wikilink")、[ロブ・パイク](https://ja.wikipedia.org/wiki/ロブ・パイク "wikilink")による設計指針のもと、[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")によって考案された\[2\]\[3\]。

## エンコード体系

[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字と互換性を持たせるために、ASCIIと同じ部分は1バイト、その他の部分を2-6バイトで符号化する。4バイトのシーケンスでは21bit (0x1FFFFF) まで表現することができるが、Unicodeの範囲外となる17面以降を表すもの（U+10FFFFより大きなもの）は受け付けない。

また、5-6バイトの表現は、ISO/IEC 10646による定義\[4\]と[IETFによるかつての定義](https://ja.wikipedia.org/wiki/Internet_Engineering_Task_Force "wikilink")\[5\]で、Unicodeの範囲外を符号化するためにのみ使用するが、Unicodeによる定義\[6\]とIETFによる最新の定義\[7\]では、5-6バイトの表現は不正なシーケンスである。

後述の[セキュリティの項に詳細はあるが](https://ja.wikipedia.org/wiki/UTF-8#セキュリティ "wikilink")、符号化は最少のバイト数で表現しなければならない。そのため、バイト数ごとにUnicodeの符号位置の最小値（下限）も設けている。

例えば、1バイトで表現するASCII文字は2バイト以上でも表現できるが、バイト数ごとの下限によってこれを回避している。

ビットパターンは以下のようになっている。

<table>
<thead>
<tr class="header">
<th><p>バイト数</p></th>
<th><p>有効ビット</p></th>
<th><p>Unicode</p></th>
<th><p>2進数表記</p></th>
<th><p>16進数表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>7 bit</p></td>
<td></td>
<td><p>xxx-xxxx</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>上限</p></td>
<td><p>U+007F</p></td>
<td><p>111-1111</p></td>
<td><p>7F</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>下限</p></td>
<td><p>U+0000</p></td>
<td><p>000-0000</p></td>
<td><p>00</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>11 bit</p></td>
<td></td>
<td><p>y-yyyx</p></td>
<td><p>xx-xxxx</p></td>
</tr>
<tr class="odd">
<td><p>上限</p></td>
<td><p>U+07FF</p></td>
<td><p>1-1111</p></td>
<td><p>11-1111</p></td>
<td><p>DF</p></td>
</tr>
<tr class="even">
<td><p>下限</p></td>
<td><p>U+0080</p></td>
<td><p>0-0010</p></td>
<td><p>00-0000</p></td>
<td><p>C2</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>16 bit</p></td>
<td></td>
<td><p>-yyyy</p></td>
<td><p>yx-xxxx</p></td>
</tr>
<tr class="even">
<td><p>上限</p></td>
<td><p>U+FFFF</p></td>
<td><p>-1111</p></td>
<td><p>11-1111</p></td>
<td><p>11-1111</p></td>
</tr>
<tr class="odd">
<td><p>下限</p></td>
<td><p>U+0800</p></td>
<td><p>-0000</p></td>
<td><p>10-0000</p></td>
<td><p>00-0000</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>21 bit</p></td>
<td></td>
<td><p>-yyy</p></td>
<td><p>yy-xxxx</p></td>
</tr>
<tr class="odd">
<td><p>上限</p></td>
<td><p>U+10FFFF</p></td>
<td><p>-100</p></td>
<td><p>00-1111</p></td>
<td><p>11-1111</p></td>
</tr>
<tr class="even">
<td><p>下限</p></td>
<td><p>U+10000</p></td>
<td><p>-000</p></td>
<td><p>01-0000</p></td>
<td><p>00-0000</p></td>
</tr>
</tbody>
</table>

Unicodeの符号位置を2進表記したものを、上のビットパターンのx, yに右詰めに格納する（最少のバイト数で表現するため、yの部分には最低1回は1が出現する）。符号化されたバイト列は、[バイト順に関わらず左から順に出力する](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。

1バイト目の先頭の連続するビット "1"（その後にビット "0" が1つ付く）の個数で、その文字のバイト数がわかるようになっている。また、2バイト目以降はビットパターン "" で始まり、1バイト目と2バイト目以降では値の範囲が重ならないので、文字境界を確実に判定できる。すなわち、任意のバイトの先頭ビットが "" なら1バイト文字、"" なら2バイト以上の文字の2番目以降のバイト、"" なら2バイト文字の先頭バイト、"" なら3バイト文字の先頭バイト、"" なら4バイト文字の先頭バイトであると判定できる。

7バイト以上の文字は規定されないため、`0xFE、0xFF`は使用されない。このため、[バイト順マーク](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink") (BOM) に`0xFEと0xFF`を使用するUTF-16やUTF-32が、UTF-8と混同されることはない。

## 特徴

### メリット

  - バイトストリーム中の任意の位置から、その文字、前の文字、あるいは次の文字の先頭バイトを容易に判定することができる。
  - 文字列の検索を単なるバイト列の検索として行っても、文字境界と異なる個所でマッチしてしまうことがない。たとえば[Shift_JIS](../Page/Shift_JIS.md "wikilink")で「¥」(0x5C) を検索すると「表」(0x95 0x5C) の2バイト目にマッチしたり、[EUC-JP](../Page/EUC-JP.md "wikilink")で「海」(0xB3 0xA4) を検索すると「ここ」(0xA4 0xB3 0xA4 0xB3) にマッチしたりするのと同様のことが起きない。このため、[マルチバイト文字](https://ja.wikipedia.org/wiki/マルチバイト文字 "wikilink")を意識せず、[ISO 8859-1などの](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")8bit文字向けに作られた膨大なプログラム資産を、比較的少ない修正で再利用できる。
      - ただし、他のUnicodeの符号化と同様に、単にバイト列の比較では文字列が同一か判断できない場合がある。詳細は、[Unicodeの等価性](https://ja.wikipedia.org/wiki/Unicodeの等価性 "wikilink")及び[正規化を参照のこと](https://ja.wikipedia.org/wiki/Unicode正規化 "wikilink")。
  - [UTF-16](https://ja.wikipedia.org/wiki/UTF-16 "wikilink")や[UTF-32](https://ja.wikipedia.org/wiki/UTF-32 "wikilink")と異なり、バイト単位の入出力を行うため、[バイト順の影響がない](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。
  - 21bitまで表現できるため、[サロゲートペア](https://ja.wikipedia.org/wiki/サロゲートペア "wikilink")を使用する必要がない。
  - ASCII文字が主体の文書であれば、ほとんどデータサイズを増やさずにUnicodeのメリットを享受できる。UTF-16やUTF-32では、データサイズはほぼ2倍、4倍となる。
  - 複数のUTF-8文字列を、単なる符号なし8ビット整数の配列とみなして辞書順ソートした結果は、Unicodeの符号位置の辞書順のソート結果（すなわちUTF-32に変換した後にソートした結果）と等しくなる。これに対して、サロゲートペアを含むUTF-16文字列を符号なし16ビット整数の配列とみなしてソートした結果は、Unicodeの符号位置の辞書順のソート結果と異なりうる。

### デメリット

  - UTF-8による符号化では、[漢字](../Page/漢字.md "wikilink")や[仮名などの表現に](https://ja.wikipedia.org/wiki/仮名_\(文字\) "wikilink")3[バイトを要する](https://ja.wikipedia.org/wiki/バイト_\(情報\) "wikilink")。このように、東アジアの従来文字コードでは[マルチバイト符号を用いて](https://ja.wikipedia.org/wiki/マルチバイト文字 "wikilink")1文字2バイトで表現されていたデータが、1.5倍かそれ以上のサイズとなる。同様に、[ISO/IEC 8859-1では](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")1バイトで表現できた非ASCIIのラテン文字（[ウムラウト](https://ja.wikipedia.org/wiki/ウムラウト "wikilink")付きの文字など）も2バイトとなるし、その他の[ISO/IEC 8859シリーズに属する文字符号ではデータ量がさらに増大しうる](https://ja.wikipedia.org/wiki/ISO/IEC_8859 "wikilink")。

      - なお、1バイトが9ビットである処理系では、この問題をあまり発生させずに符号化できるはずである。このアイディアに基づいた[ジョークRFC](https://ja.wikipedia.org/wiki/ジョークRFC "wikilink")がRFC 4042 “UTF-9” として[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")の[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")（[4月1日](../Page/4月1日.md "wikilink")）に公開された。

  - ただし、Unicodeでは一部の文字を合成によって表現することもできるから（例：「ぱ」は、U+3071のほかにもU+306F U+309Aでも表現できる）、Unicodeを採用する場合、文字列の文字数をその文字列のバイト数から計算できないことは、UTF-8に限ったことではない。

  - 最短ではない符号やサロゲートペアなど、UTF-8の規格外だがチェックを行わないプログラムでは一見正常に扱われるバイト列が存在する。これらのバイト列を入力として受け入れてしまうと、プログラムが予期しない範囲のデータを生成するため、セキュリティ上の脅威となりうる\[8\]。

## サロゲートペアの扱い

[UTF-16](https://ja.wikipedia.org/wiki/UTF-16 "wikilink")では[サロゲートペアで表されるような](https://ja.wikipedia.org/wiki/Unicode#サロゲートペア "wikilink")、[基本多言語面](https://ja.wikipedia.org/wiki/基本多言語面 "wikilink")外の符号位置をUTF-8で表す時は、変換元がUTF-16でサロゲートペアの時には U+D800 〜 U+DBFF, U+DC00 〜 U+DFFF を表すUTF-8にそのまま変換したりはせず、U+10000 〜 U+10FFFF の符号位置にデコードしてから変換する。そのままUTF-8で符号化したような列は不正なUTF-8とされる。

サロゲートペアのままUTF-8と同等の符号化を行う符号化は、**CESU-8**  として別途定義されている。実用に供されている例としては、[Oracle Databaseのバージョン](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")8以前において、UTF-8として3オクテットまでのオクテット列しか扱えなかったために定義されたものである。本来のUTF-8における4オクテット列の代わりに、サロゲート符号位置を表す3オクテット列のペア（上位が ED A0 80 〜 ED AF BF、下位が ED B0 80 〜 ED BF BF）で表現される。

現在のOracle Databaseでも、CESU-8を「UTF8」として、「普通のUTF-8」を「AL32UTF8」として扱っているため注意を要する。[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")でも「utf8」を指定した場合は4オクテット列が扱えず、CESU-8相当の符号化を必要とする（4オクテット列対応のUTF-8は「utf8mb4」として別途定義されているが、MySQL 5.5.3以降でないと使用できない\[9\]）。

また、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の一部の内部実装で用いられている**Modified UTF-8**も、サロゲートペアをそのまま残す仕様となっている。ただし、NULL文字を`C0 80`とエンコードする（これもUTF-8規格外）点で、CESU-8とも異なる実装となっている。

## セキュリティ

UTF-8のエンコード体系には[冗長性があり](https://ja.wikipedia.org/wiki/冗長性_\(情報理論\) "wikilink")、同じ文字を符号化するのに複数の表現が考えられる（例: スラッシュ記号である「/」を 0x2F という1バイトで表現するのではなく、0xC0 0xAF という2バイトもしくはそれより大きなバイト数で表現する）。かつてはそのような表現も許容されていたが、[ディレクトリトラバーサル](https://ja.wikipedia.org/wiki/ディレクトリトラバーサル "wikilink")などの対策として行われる文字列検査を冗長な表現によりすり抜ける手法が知られるようになったため、現在の仕様では最少のバイト数による表現以外は不正なUTF-8シーケンスとみなさなければならない\[10\]。

ISO/IEC 10646の定義が5バイト以上の表現を許容していることにより、正しくない実装を行った[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")のあるシステムにおいてエンコード時に[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")が発生する可能性も指摘されている。

## 文字種

<table>
<thead>
<tr class="header">
<th><p>B</p></th>
<th><p>Unicode</p></th>
<th><p>スクリプト</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/JIS_X_0201" title="wikilink">JIS X 0201</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/JIS_X_0208" title="wikilink">JIS X 0208</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/JIS_X_0212" title="wikilink">JIS X 0212</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/JIS_X_0213" title="wikilink">JIS X 0213</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>U+0000 - U+007F</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ASCII" title="wikilink">ASCII</a></p></td>
<td><p>Roman（<a href="https://ja.wikipedia.org/wiki/円記号" title="wikilink">円記号</a>・<a href="https://ja.wikipedia.org/wiki/オーバーライン" title="wikilink">オーバーライン</a>以外）</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>U+0080 - U+07FF</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ラテン文字" title="wikilink">ラテン</a>、<a href="https://ja.wikipedia.org/wiki/ダイアクリティカルマーク" title="wikilink">ダイアクリティカル</a>、<a href="https://ja.wikipedia.org/wiki/ギリシャ文字" title="wikilink">ギリシャ</a>、<br />
<a href="https://ja.wikipedia.org/wiki/キリール文字" title="wikilink">キリール</a>、<a href="https://ja.wikipedia.org/wiki/アルメニア文字" title="wikilink">アルメニア</a>、<a href="https://ja.wikipedia.org/wiki/ヘブライ文字" title="wikilink">ヘブライ</a>、<a href="https://ja.wikipedia.org/wiki/アラビア文字" title="wikilink">アラビア</a>、<br />
<a href="https://ja.wikipedia.org/wiki/シリア文字" title="wikilink">シリア</a>、<a href="https://ja.wikipedia.org/wiki/ターナ文字" title="wikilink">ターナ</a>、<a href="https://ja.wikipedia.org/wiki/ンコ文字" title="wikilink">ンコ</a></p></td>
<td><p>円記号</p></td>
<td><p>非漢字の一部</p></td>
<td><p>非漢字の一部</p></td>
<td><p>非漢字の一部</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>U+0800 - U+FFFF</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/アブギダ" title="wikilink">インド系諸文字</a>、<a href="https://ja.wikipedia.org/wiki/句読点" title="wikilink">句読点</a>、<a href="https://ja.wikipedia.org/wiki/学術記号" title="wikilink">学術記号</a>、<br />
<a href="https://ja.wikipedia.org/wiki/絵文字" title="wikilink">絵文字</a>、<a href="https://ja.wikipedia.org/wiki/東アジア" title="wikilink">東アジア</a>の諸文字、<a href="https://ja.wikipedia.org/wiki/全角と半角" title="wikilink">全角半角形など</a></p></td>
<td><p>オーバーライン、Kana</p></td>
<td><p>残りの全て</p></td>
<td><p>残りの全て</p></td>
<td><p>大半</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>U+10000 - U+1FFFFF</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/古代文字" title="wikilink">古代文字</a>、3に含まれない漢字</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>第3・第4水準漢字の一部</p></td>
</tr>
</tbody>
</table>

## バイト順マークの使用

UTF-8で符号されたテキストデータは[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")に関わらず同じ内容になるので、[バイト順マーク](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink") (BOM) は必要ない。しかし、テキストデータがUTF-8で符号化されていることの標識として、データの先頭にEF BB BF（16進。UCSでのバイト順マークU+FEFFのUTF-8での表現）を付加することが許される。一部のテキスト処理アプリケーション（[テキストエディタ](https://ja.wikipedia.org/wiki/テキストエディタ "wikilink")など）がBOMを前提とした動作をすることがある。[TeraPad](https://ja.wikipedia.org/wiki/TeraPad "wikilink")、[EmEditor](https://ja.wikipedia.org/wiki/EmEditor "wikilink")、[MIFES](https://ja.wikipedia.org/wiki/MIFES "wikilink")のようにBOMを付加するかどうかを選択できるものもある。

なお、日本の特殊事情として、このシーケンスがある方を**UTF-8**、ない方を特に**UTF-8N**と呼ぶこともある\[11\]が、このような呼び分けは日本以外ではほとんど知られておらず、また公的規格などによる裏付けもない\[12\]。

このシーケンスを通常の文字と認識するプログラムでは、先頭に余分なデータがあるとみなされて問題となることがある。例えば、[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSにおける実行可能[スクリプトは](../Page/スクリプト言語.md "wikilink")、ファイル先頭が「[\#\!](https://ja.wikipedia.org/wiki/シバン_\(Unix\) "wikilink")」から始まるとき、それに続く文字列を[インタプリタ](../Page/インタプリタ.md "wikilink")のコマンドとして認識するが、多くのシステムでは、このシーケンスが存在するとこの機能が働かず実行できない。PHPでは、`<?PHP`の前に出力されるため、`header()`関数の実行に失敗する原因となる。[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")や[GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")の[シェーダー](https://ja.wikipedia.org/wiki/シェーダー "wikilink")プログラム[コンパイラ](../Page/コンパイラ.md "wikilink")（fxcやglslangValidator）はBOMを処理できず、コンパイルエラーとなる。

逆にこのシーケンスがない場合、UTF-8と認識できないプログラムも存在する。たとえば、[Microsoft Excelでは](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[CSVファイルを開くとき](https://ja.wikipedia.org/wiki/Comma-Separated_Values "wikilink")、このシーケンスが付加されていないUTF-8の場合は正常に読み込むことができない\[13\]\[14\]。[Microsoft Windowsに付属する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[メモ帳](https://ja.wikipedia.org/wiki/メモ帳 "wikilink") (Windows 10 May 2019 Updateより前\[15\])、[ワードパッド](https://ja.wikipedia.org/wiki/ワードパッド "wikilink")も同様である。[Microsoft Visual C++は既定でBOMなしUTF](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")-8を認識せず、システムロケール設定に応じたマルチバイトエンコーディングとみなすが、Visual C++ 2015以降ではコンパイルオプションを指定することでBOMなしUTF-8を認識することができるようになっている\[16\]。

また、BOMがなくともエンコード自動推定によってUTF-8とShift_JISなどを区別することのできるプログラムもあるが、ASCII部以外の文字が少ない場合に誤認することが多い。

プロトコルが常にUTF-8であることを強制しているものである場合はこのシーケンスを禁止するべきで、この場合ファイル先頭にこのシーケンスが現れると “ZERO WIDTH NO-BREAK SPACE” と見なされる。逆にプロトコルがそれを保証しない場合このシーケンスは禁止されずファイル先頭のそれはバイト順マークと見なされる\[17\]。

## 脚注

## 参考資料

  - 用語の日本語表記は原則として「」にならった。

  -
## 関連項目

  - [文字コード](../Page/文字コード.md "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [RFC 3629](http://tools.ietf.org/html/rfc3629) UTF-8, a transformation format of ISO 10646
2.  [RFC 3629 Page-3](http://tools.ietf.org/html/rfc3629#page-3)
3.  [Rob Pike's UTF-8 history](http://www.cl.cam.ac.uk/~mgk25/ucs/utf-8-history.txt)
4.  [ISO/IEC 10646:2003](http://std.dkuug.dk/jtc1/sc2/wg2/) Information technology -- Universal Multiple-Octet Coded Character Set (UCS)
5.  RFC 2279 UTF-8, a transformation format of ISO 10646
6.  [The Unicode Standard, Version 5.2](http://www.unicode.org/versions/Unicode5.2.0/)
7.  RFC 3629 UTF-8, a transformation format of ISO 10646
8.  RFC 3629, pp.9f.
9.  [10.1.10.6 The utf8mb4 Character Set (4-Byte UTF-8 Unicode Encoding)](https://dev.mysql.com/doc/refman/5.5/en/charset-unicode-utf8mb4.html) - MySQL 5.5 Reference Manual
10. Windowsにおける有名な[ワームである](https://ja.wikipedia.org/wiki/ワーム_\(コンピュータ\) "wikilink")[Nimda](https://ja.wikipedia.org/wiki/Nimda "wikilink")ウイルスは、[IISにおけるUTF](../Page/Internet_Information_Services.md "wikilink")-8の脆弱性をもちいたものである。
11.
12. このため、UTF-8という呼び名を使っていれば情報交換の相手が文書先頭にこのシーケンスがあると見なすと期待すべきではないし、また、UTF-8Nという呼び名は情報交換の際に用いるべきではない。
13.
14.
15.
16. [/source-charset (Set Source Character Set) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/source-charset-set-source-character-set?view=vs-2015)
17. RFC 3629 [6. Byte order mark (BOM)](http://tools.ietf.org/html/rfc3629#section-6)