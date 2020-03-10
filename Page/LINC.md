> この記事は[LINC](https://ja.wikipedia.org/wiki/LINC)から翻訳されています。


**LINC**(; 実験器具コンピュータ)は、[12ビット](https://ja.wikipedia.org/wiki/12ビット "wikilink")、2048ワードの[コンピュータ](../Page/コンピュータ.md "wikilink")。LINCは世界初の[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")であり、同時に世界初の個人用コンピュータ（[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")）と呼べるものであった\[1\]。

LINCおよびMITの Linc Computer（1980年\[2\]に[DECが開設した博物館によれば](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")\[3\]、DECがプロジェクトに参加する前はそのように呼ばれていた\[4\]）は、[MITで設計され](../Page/マサチューセッツ工科大学.md "wikilink")、最終的に[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) と Spear Inc. （後に Becton Dickinson and Company が子会社化）が製造した\[5\]。当時4万ドル以上の価格で販売された。6フィート×20インチのラックに格納された構成が多く、テープドライブ、小型ディスプレイ、制御パネル、キーボードが入っている4つのボックスから成る。

その命令セットは小さかったが、[PDP-8](../Page/PDP-8.md "wikilink")の命令セットに比べれば大きかった。

実験で使用するのに便利なインターフェイスを備えていた。アナログ入出力は基本設計の一部となっている。[1962年](../Page/1962年.md "wikilink")、[リンカーン研究所](https://ja.wikipedia.org/wiki/リンカーン研究所 "wikilink")の [Charles Molnar](https://ja.wikipedia.org/wiki/:en:Charles_Molnar "wikilink") と [Wesley Clark](https://ja.wikipedia.org/wiki/:en:Wesley_A._Clark "wikilink") が\[6\]、[アメリカ国立衛生研究所](../Page/アメリカ国立衛生研究所.md "wikilink") (NIH) のために設計したものである。LINCの設計が文字通りパブリックドメイン化されたことで、コンピュータ史上でもユニークなマシンとなっている。LINCの生産台数や誰が製造したかということはあまり問題にされない。ある文献によれば、24台のLINCがMITのサマーワークショップで組み立てられたという。[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")([1964年](../Page/1964年.md "wikilink")から)と Spear Inc.\[7\] が製品化し製造した。

[ゴードン・ベル](../Page/ゴードン・ベル.md "wikilink")は、LINCプロジェクトが1961年に始まり、1962年3月に1台目が完成したとしており、それが正式に撤収されたのは1969年12月のこととしている\[8\]。DEC製のモジュールと筐体を使って全部で50台が生産され、多くがリンカーン研究所で組み立てられた。1台目のLINCには2つのオシロスコープが表示装置として備えられていた。DECは製品版21台を43,600ドルで販売。標準の開発用ソフトウェア（アセンブラ/エディタ）は [Mary Allen Wilkes](https://ja.wikipedia.org/wiki/:en:Mary_Allen_Wilkes "wikilink") で、最終版は LAP6 (LINC Assembly Program 6) と呼ばれていた。

## 制御パネル

LINCの制御パネルの機能はプログラムのステップ実行機能だけではなく、あらゆる意味で[デバッガ](../Page/デバッガ.md "wikilink")機能を備えていた。例えば、[プログラムカウンタ](https://ja.wikipedia.org/wiki/プログラムカウンタ "wikilink")がスイッチで設定した値になったところで実行を停止することができた。より重要な機能として、プログラムがスイッチで指定したアドレスにアクセスしたときに停止させる機能もあった。シングルステップ実行や停止状態からの復帰は自動的に繰り返し行うことができた。繰り返しレートは毎秒1命令から最高速度の半分の速度まで、制御パネルにあるアナログノブとセレクトスイッチ(4位置)で選択可能だった。プログラムを毎秒1命令で実行開始して、徐々に加速させて最高速度まで持っていくこともでき、コンピュータの速度というものを体感することができたのである。

アナログノブは[マウスのような入力デバイスとして利用でき](../Page/マウス_\(コンピュータ\).md "wikilink")、例えばディスプレイでのグラフ表示の拡大縮小、ディスプレイでのカーソルの移動といった制御が行われていた。

## LINCTape

LINCの特筆すべき機能として**LINCtape**と呼ばれる[磁気テープ](../Page/磁気テープ.md "wikilink")装置がある。オプション装置ではなく基本スペックに含まれており、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")はLINCtapeに依存していた。LINCtapeは言ってみればシークが非常に遅い[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")のようなものである。当時の大型マシンの磁気テープ装置は大容量で全部を読み取るには長時間かかり、テープ上の特定の位置のデータブロックだけを書き換えるということができなかった。対照的にLINCtapeは小型で素早いデバイスであり、容量は約400Kで、個別書き換え可能な固定フォーマットになっていて、1分足らずで端から端まで読み取り可能であった。テープは固定サイズのブロックでフォーマットされ[ファイルシステム](../Page/ファイルシステム.md "wikilink")として使用された。1命令で指定箇所までシークし、そこで複数ブロックを読み/書きできた。

ファイル名は6文字である。このファイルシステムは[ソースファイルと対応する](../Page/ソースコード.md "wikilink")[実行ファイル](../Page/実行ファイル.md "wikilink")を同じファイル名で格納することができた。実際にはファイル名には1文字の[拡張子](../Page/拡張子.md "wikilink")があり、"S" と "B" でソースかバイナリかを示していた。LINCは標準スペックでは1024×12ビットワードのコアメモリしかなく（最大で2048ワード）、通常の操作でもLINCtapeへのスワップアウトが頻繁に発生した。DECは後に非常によく似た設計の****の特許を取得したが、後に裁判で無効とされた。

LINCtapeは非常に信頼性が高く、後にその代替となった[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")よりも信頼できた。LINCtapeには簡単な冗長性が備わっていて、データはテープの幅方向の2箇所に必ずコピーして記録された。これを確認するために[紙テープ](../Page/紙テープ.md "wikilink")のさん孔装置でLINCtapeに穴を空けてみると、全く問題なく読み込むことができるのである。装置にはキャプスタン(テープを定速で送るための回転軸)がなく、テープの回転は直接リールのモーターで制御された。早送りとか高速な巻き戻しは無く、ある意味で常に高速回転しながら読み書きしていたとも言える。操作モードによっては内蔵スピーカーでテープの内容を音として再生することもできる。

## キーボード

LINCの[キーボードは](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink") Soroban Engineering 社が製造したもので、各キーにはロック式[ソレノイド](https://ja.wikipedia.org/wiki/ソレノイド "wikilink")が使われている。ユーザーがキーを押下すると、LINCは全キーをロックしてその状態で動かないようにし、押されているキーをハードウェアレジスタに読み取り、プログラムがそのレジスタを読み取って、その後にソレノイドのロックを解除するという手順を踏んでいた。このため、キー入力は非常に遅くなってしまい、キーロールオーバーが全くできないのである。そのため、後述する LINC-8 や PDP-12 ではこのキーボードは使われなかった。

## ディスプレイ

LINCは12ビットワードを横4ピクセル×縦6ピクセルでディスプレイに高速かつ自動的に表示することができ、これによってちらつきの無いフルスクリーンテキスト表示を可能としていた。標準表示ルーチンは4×6ピクセルの文字を表示するもので、非常に粗くて見にくい表示だった。

ディスプレイは[テクトロニクス](https://ja.wikipedia.org/wiki/テクトロニクス "wikilink")製オシロスコープを流用した5インチのブラウン管で、特別な増幅器を接続していた。

## LINC-8 と PDP-12 コンピュータ

[thumb](https://ja.wikipedia.org/wiki/ファイル:PDP-12_VCF_2001.jpg "wikilink") [ゴードン・ベル](../Page/ゴードン・ベル.md "wikilink")によれば、LINCの設計からDECは初の18ビット機[PDP-4と初の](../Page/PDPシリーズ.md "wikilink")12ビット機[PDP-5の着想を得たという](../Page/PDPシリーズ.md "wikilink")。その後 [PDP-8](../Page/PDP-8.md "wikilink") で成功を収め、それにLINCとの互換性を加えたコンピュータ [LINC-8](https://ja.wikipedia.org/wiki/:en:LINC-8 "wikilink") を開発\[9\]。その後TTL化したPDP-8/Iをベースにし、LINCも再設計して結合した**PDP-12**を開発\[10\]。

LINC-8 は[PDP-8](../Page/PDP-8.md "wikilink")とLINCを結合したもので、PDP-8側の PROGOFOP(PROGram OF OPeration)というプログラムで(ゆっくり)起動された。**PDP-12**はLINCの後継としては最後の機種で最も広く使われた。様々な改善がなされていたが、根本的にはLINCとPDP-8を無理やり結合したアーキテクチャである。例えば、LINCにはオーバーフロービットがあり、アーキテクチャ上重要である。しかし、PDP-12ではPDP-8側の割り込みの際にこのオーバーフロービットをセーブ/リストアする機能がなかった。

## MINC-11 コンピュータ

DECのPDP-11/03はMINC-11\[11\]と呼ばれ、各種実験用入出力モジュールを実装できた。プログラミング言語としては、実験用I/Oをサポートする MINC BASIC がある。MINCという名称は "Multi-Instrument Computer"の略で、明らかにLINCを意識した命名だが、LINCとの互換性も無く、全くアーキテクチャ上の関係はない。

## 脚注

## 外部リンク

  - [The Last LINC](http://www.mit.edu:8001/people/ijs/epl/LINC.html)
  - [Lights Out for Last LINC](http://www.rle.mit.edu/media/currents/6-1.pdf)
  - [LINC Description](http://foldoc.doc.ic.ac.uk/foldoc/foldoc.cgi?Laboratory+Instrument+Computer)
  - [PDP-12 User Manual](http://users.rcn.com/crfriend/museum/doco/PDP-12/index.shtml)
  - [Oral history interview with Wesley Clark](http://purl.umn.edu/107217). [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - [LINC documentation at bitsavers.org](http://bitsavers.org/pdf/washingtonUniversity/linc)

[Category:ミニコンピュータ](https://ja.wikipedia.org/wiki/Category:ミニコンピュータ "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:トランジスタ・コンピュータ](https://ja.wikipedia.org/wiki/Category:トランジスタ・コンピュータ "wikilink")

1.  例えば William H. Calvin letter *The Missing LINC*, *BYTE* magazine April 1982 page 20
2.  B.I. Charles, The Charles Babbage Institute Newsletter, Palo Alto, Calif: The Institute. 2:1.
3.
4.
5.  W. Clark, “The LINC was early and small,” Proceedings of the ACM Conference on The history of personal workstations, Palo Alto, California, United States: ACM, 1986, pp. 133-155.
6.  presentations at The Computer Museum, Marlborough, in the hands of its successor, The Computer History Museum
7.  E.C. Toren, R.N. Carey, G.S. Cembrowski, and J.A. Schirmer, “Computer-Controlled Instrument System for Sequential Clinical Chemical Testing. I. Instrumentation and System Features,” Clin Chem, vol. 19, Oct. 1973, pp. 1114-1121.
8.  C. Gordon Bell writing in *Computer Engineering a DEC View of Hardware Systems Designs* (c) Copyright originally held by Digital Press, out of print but available at Bell's web sites, pp 176–177
9.  [LINC-8](http://research.microsoft.com/~gbell/Digital/timeline/1966-3.htm)
10. [PDP-12](http://research.microsoft.com/~gbell/Digital/timeline/1969-2.htm)
11. [Digital MINC-11](http://www.binarydinosaurs.co.uk/Museum/Digital/minc/index.php)