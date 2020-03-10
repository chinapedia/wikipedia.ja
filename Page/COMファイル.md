> この記事は[COM](https://ja.wikipedia.org/wiki/COM)から翻訳されています。


**COMファイル** (コムファイル、COM file) は、[実行可能ファイル](https://ja.wikipedia.org/wiki/実行可能ファイル "wikilink")形式の一つ。語源はcommand（[命令](../Page/命令_\(コンピュータ\).md "wikilink")）。[拡張子](../Page/拡張子.md "wikilink")は「.COM」（本来は[大文字](../Page/大文字.md "wikilink")）だが、[トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")の[.com](https://ja.wikipedia.org/wiki/.com "wikilink") ([commercial](../Page/商業.md "wikilink")) とは無関係。

実行時の[メモリイメージがそのままファイルとなっている](../Page/主記憶装置.md "wikilink")、最も単純な実行可能ファイル形式である。

MS-DOSのCOMファイルは[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")[Cascadeに感染する](../Page/Cascade_\(コンピュータウイルス\).md "wikilink")。

## 歴史

拡張子.COMの実行ファイルは古くからあったが、現在の形式のものは[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")で使われ、CP/Mを元にした[MS-DOS](../Page/MS-DOS.md "wikilink")にも採用された。ただし、[CPU](https://ja.wikipedia.org/wiki/中央処理装置 "wikilink")（CP/Mは[8080系](../Page/Intel_8080.md "wikilink")、MS-DOSは[8086系](../Page/Intel_8086.md "wikilink")）や[割り込みの仕様の違いのため](../Page/割り込み_\(コンピュータ\).md "wikilink")、[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")は乏しい。CP/MとMS-DOSの両方で実行できるファイルも作れるが、両方のコードを収録するため[ファイルサイズ](https://ja.wikipedia.org/wiki/ファイルサイズ "wikilink")が大きくなる。また、8086系CPUを対象にしたCP/M-86では拡張子は.COMではなく.CMDである（[Windows NT系の](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink").CMDファイルとは無関係）。

MS-DOSには、ほかに2つの実行可能ファイル形式、[EXEファイルと](https://ja.wikipedia.org/wiki/EXEフォーマット "wikilink")[BATファイルがあった](https://ja.wikipedia.org/wiki/バッチファイル "wikilink")。EXEとBATは[Microsoft Windowsにも採用されたが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、COMファイルは廃止された（[仮想DOSマシン](https://ja.wikipedia.org/wiki/仮想DOSマシン "wikilink")上では実行可能）。

## 内容

実行時のメモリイメージがそのままファイルとなっており、ファイルの内容を0100[番地からメモリに展開](https://ja.wikipedia.org/wiki/メモリアドレス "wikilink")（ロード）し先頭に[ジャンプすれば](https://ja.wikipedia.org/wiki/分岐命令 "wikilink")、直ちに実行が始まる。[ファイルヘッダ](https://ja.wikipedia.org/wiki/ファイルヘッダ "wikilink")などいっさいの[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")を含まず、これは、EXEヘッダからファイルが始まるEXEファイルとの大きな違いである。ファイルの内容全部をロードしてから実行する点も、全部を一度にロードするとは限らないEXEファイルとの違いである。

[セグメントがコードもデータも含め](../Page/セグメント方式.md "wikilink")1つであり、これは複数のセグメントを持つことができるEXEファイルとは異なる。このため、ファイルサイズは最大で65279[バイト](../Page/バイト_\(情報\).md "wikilink")（8086系CPUのセグメントサイズである64[キロバイト](https://ja.wikipedia.org/wiki/キロバイト "wikilink")からメモリ展開時のオフセットの256バイトとスタックの1バイトを引いた値）である。ファイルサイズがこれを超える場合は、メモリの空きがいくらあっても「プログラムが大きすぎてメモリに入りません」(Program too big to fit in memory) または「(ファイル名) は実行できません」(Cannot execute (ファイル名)) とエラー表示され実行されない（この制限はロード時であり、実行中にセグメントを変更したり64キロバイトを超えるプログラムやデータを読み込むことは可能である）。8080系CPUのCP/Mの場合も同様に0100番地にロードされるが、メモリの上位にCP/Mのシステムが常駐しているため、ロードできるファイルサイズの上限はさらに小さくなる。

また、メタデータがないため極小の実行可能ファイルを作ることができる。これらの理由で、一般に、EXEファイルより小さいことが多い。最小は1バイトで、0バイトではエラーになる。

[Windows 9x系にある](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink") [COMMAND.COM](../Page/COMMAND.COM.md "wikilink") は、拡張子は.COMであるが内容はEXEファイルであり、ファイルサイズも64キロバイトを超えている。

## 実行優先順位

MS-DOSの実行可能ファイル形式のうち、デフォルトでは最も実行優先順位が高い。したがって、MS-DOSバージョン4以降で拡張子を省略して[コマンド](../Page/命令_\(コンピュータ\).md "wikilink")「notepad」を[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")に入力した時、他の実行可能形式「notepad.exe」「notepad.bat」が存在する場合でも、「notepad.com」があればこれが実行される。バージョン3まででは拡張子を指定しても、「notepad.com」があればこれが実行される。

COMファイルを作成するには、[コンパイラ](../Page/コンパイラ.md "wikilink")などでEXEファイルとして作成し、（MS-DOS外部コマンド）やEXE2COM（フリーソフト）のようなプログラムで変換することができる。アブソリュート[アセンブラで直接作成することもできる](../Page/アセンブリ言語.md "wikilink")。

[Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink") [Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink")