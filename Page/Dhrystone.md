> この記事は[Dhrystone](https://ja.wikipedia.org/wiki/Dhrystone)から翻訳されています。


**Dhrystone**（どらいすとーん）は、1984年に Reinhold P. Weicker が開発した合成[ベンチマーク](../Page/ベンチマーク.md "wikilink")プログラムであり、システム（整数）プログラムのパフォーマンスに注目したベンチマークである。Dhrystoneは、[SPECint](../Page/Standard_Performance_Evaluation_Corporation.md "wikilink") として知られている CPU89ベンチマークが現れるまで、汎用プロセッサの性能を表すものとしてよく使われた。

Dhrystoneベンチマークは[浮動小数点演算を含まない](../Page/浮動小数点数.md "wikilink")。それは名前にもあらわれていて、浮動小数点演算のベンチマークとしてDhrystoneより以前からある有名な[Whetstone](../Page/Whetstone.md "wikilink")をもじったものである。ベンチマークが出力するのは一秒間のDhrystone数（[メインループ](https://ja.wikipedia.org/wiki/メインループ "wikilink")を一秒間に何回回ったか）である。

Whetstone も Dhrystone も「合成」ベンチマークである。つまり一般的なプログラムを統計的に分析して、その負荷を再現するよう注意深く設計された単純なプログラムである。Whetstone は 1976年に開発された。1970年ごろから一般的な ALGOL 60 のプログラムの負荷を再現するよう調整されていたが、FORTRANバージョンが一般化した。Whetstone は 1960 年代の数値演算の負荷を再現したものと言える。

Dhrystone では、Weicker は様々なプログラムから情報を集めた（FORTRAN、PL/1、SAL、ALGOL 68、Pascal）。そして、それらのプログラムの基本構造（プロシージャ呼び出し、ポインタ操作、代入など）を抽出した。そしてそこから得られた使用頻度を元にして Dhrystone ベンチマークを作成したのである。オリジナルの Dhrystone は [Ada](../Page/Ada.md "wikilink") で書かれていた。[UNIX](../Page/UNIX.md "wikilink")向けの [C言語](../Page/C言語.md "wikilink")版は Rick Richardson が開発し（バージョン 1.1）、Dhrystone の普及に大きく貢献した。

Dhrystone はコンピュータの性能指標としての地位を確立し、商用コンパイラ作者はこれを目標として技術を磨いていった（あるいは、ベンチマーク的なパターンを見つけると、丸ごと予め用意した特別にチューニングされたコードを出力するといったような、チート技術を磨いた者たちもいた）。様々な手法が開発され、合成ベンチマークの設計は困難になっていった。Weicker と Richardson が 1988年に開発したバージョン 2.0 では、そのようなコンパイラの技法の裏をかく大幅な改造がなされた。基本的なベンチマークとしての性格は残すよう、注意深くコーディングされている。コンパイラの裏をかくという目的は部分的にしか成功しなかった。同年の5月にリリースされた Dhrystone 2.1 が現在も使われ続けている。

コンパイラの最適化以外にも問題はある。その大部分は 1984年当時から指摘されていたことで、コードとデータのサイズが極めて小さいことも含まれる。もっと細かい話では文字列操作が言語に深く依存している点に問題があると言われている。Ada や Pascal は文字列を[基本データ型](https://ja.wikipedia.org/wiki/基本データ型 "wikilink")としているが、C言語ではそうではない。従って、文字列変数への代入は C ライブラリでは単なるバッファのコピーになってしまう。

Dhrystone ベンチマークの測定結果は D[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")（*Dhrystone million instructions per second*）で表されることも多い。これはDhrystoneの値を[VAX 11/780のDhrystone値である](../Page/VAX.md "wikilink") 1757 で割ることで得られる。すなわちいわゆるVAX MIPSである。定義から同機は1DMIPSである。これはVAX 11/780が MIPSマシンと呼ばれたことによる（同機の命令実行速度は不明だ ）。同様にその他のベンチマークによるVAX MIPSも存在する。単なる命令実行数によるMIPS値では、命令セットの違いによる命令の機能の違いにより比較できないので、ベンチマーク値を元にした相対的なMIPS値という考え方である。

Dhrystone は単純なベンチマークとして根強く生き残っている。扱いやすく、文書もそろっていて、単独で使うことができ、どんなシステムでも測定可能だからである。特に組み込み市場ではよく使われているが、CPU89 が汎用のコンピュータ市場でその役割を奪ったように EEMBC ベンチマークが最近取って代わろうとしている。20年も使われ続けたのはWeickerの設計の良さと先見性を証明してもいるが、最も強い理由は比較のためには同じベンチマークが必要だからである。HPCの分野で著名な[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")が、最初の設計は1970年代にまで遡る[LINPACK](../Page/LINPACK.md "wikilink")によるベンチマーク「HPL」を今でも利用しているのと同じようなものである。

## 注

<references/>

[Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink")