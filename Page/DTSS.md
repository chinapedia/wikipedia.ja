> この記事は[DTSS](https://ja.wikipedia.org/wiki/DTSS)から翻訳されています。


**DTSS**(Dartmouth Time-Sharing System、**ダートマス・タイムシェアリングシステム**)は、世界で初めて成功裏に実装された大規模[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")である。[Bolt, Beranek and Newman](../Page/BBNテクノロジーズ.md "wikilink") で[PDP-1](../Page/PDP-1.md "wikilink")上で構築されたタイムシェアリングシステムに影響を受けている。1962年、[ダートマス大学](../Page/ダートマス大学.md "wikilink")の[ジョン・ケメニーと](https://ja.wikipedia.org/wiki/ジョン・ジョージ・ケメニー "wikilink")は新たなタイムシェアリングシステム開発の資金援助を[NSFに申請した](../Page/アメリカ国立科学財団.md "wikilink")（実際に出資されたのは1964年）\[1\]。[1963年](../Page/1963年.md "wikilink")、大学の全メンバーに計算設備への容易なアクセスを提供する目的で\[2\]、ケメニーとカーツの指揮下で学生のチーム\[3\]によって実装が開始された。1964年5月1日午前4時、システムが運用開始された。なお、このシステムは1999年末まで運用された\[4\]\[5\]。DTSSは当初、[GE 235](../Page/GE-200シリーズ.md "wikilink") コンピュータ上に実装され、端末プロセッサ GE Datanet 30 が235を制御する形態だった。後に [GE 635](../Page/GE-600シリーズ.md "wikilink") 上に再実装されているが\[6\]、端末制御には相変わらず Datanet 30 を使用していた。635版のDTSSは1970年代に300台弱の端末によるタイムシェアリングを実現しており、これは当時としては非常に大規模である。

その目的（あらゆる学科の学生の教育）のため、DTSSは使い易さを優先して設計された。

DTSSには世界初の[統合開発環境](../Page/統合開発環境.md "wikilink")が実装された。これはコマンドベースのシステムで以下のようなコマンドが実装されていた。

  - **NEW** -- 新たなプログラムに名前を付け、プログラム作成を開始する
  - **OLD** -- 以前に作成したプログラムを検索して取り出す
  - **LIST** -- 現在のプログラムを表示する
  - **SAVE** -- 現在のプログラムを保存する
  - **RUN** -- 現在のプログラムを実行する

多くのユーザーはこれらのコマンドを[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")言語の一部と思い込んでいたが、実際にはタイムシェアリングシステムの一部であり、[ALGOL](../Page/ALGOL.md "wikilink")\[7\]や[FORTRAN](../Page/FORTRAN.md "wikilink")のプログラムをDTSS端末経由で使用する場合にもこれらのコマンドが使われたのである。

ユーザーが入力した先頭に行番号のある行はプログラムに追加され、もし以前に同じ行番号の行を入力していたら、それを置き換える。それ以外の入力行は即座にコンパイルされ実行される。行番号のみの入力は保存されないが、同じ行番号で入力済みの行があればそれを削除する効果がある。このような入力方法になっているのは、DTSSで使用された[端末](../Page/端末.md "wikilink")が[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")だったからである。

1968年から1970年代中ごろにかけて、黎明期のネットワークによって東海岸の他の学校や研究機関もDTSSに接続された。例えば、、[フィリップス・アカデミー](../Page/フィリップス・アカデミー.md "wikilink")、[海軍兵学校などで](../Page/海軍兵学校_\(アメリカ合衆国\).md "wikilink")、テレタイプ端末[ASR-33](../Page/ASR-33.md "wikilink")とモデムを使って接続した。ユーザー間で[電子メール](../Page/電子メール.md "wikilink")的なメッセージのやり取りが可能で、[UNIX](../Page/UNIX.md "wikilink")の[talk](https://ja.wikipedia.org/wiki/talk "wikilink")コマンドの前身となったリアルタイム[チャット](../Page/チャット.md "wikilink")機能も存在した。

[2000年](../Page/2000年.md "wikilink")、DTSSシステムをシミュレータ上で再生するプロジェクトが行われ、[Microsoft Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")上でDTSSが利用可能となっている\[8\]。

## 脚注

## 関連項目

  - [ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")
  - [オペレーティングシステムの歴史](https://ja.wikipedia.org/wiki/オペレーティングシステムの歴史 "wikilink")

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:1964年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1964年のソフトウェア "wikilink")

1.
2.  <http://www.bitsavers.org/pdf/dartmouth/DTSS_descr_Oct64.pdf> | DTSS user manual October 1964
3.  [Kemeny's Kids](http://web.archive.org/web/20071009062028/http://www.kemenyskids.com/)
4.  <http://dtss.dartmouth.edu/timeline.php> |Dartmouth Time-Sharing System (DTSS) timeline.
5.  <http://www.bitsavers.org/pdf/dartmouth/The_Dartmouth_Time-Sharing_System_1980.pdf> | Description of DTSS c. 1977
6.  <http://www.dartmouth.edu/comp/about/archive/history/timeline/1960s.html> | Dartmouth Computing in the 1960s
7.  <http://dtss.dartmouth.edu/scans/> Scans of original documentation and software
8.  [DTSS reborn site](http://dtss.dartmouth.edu/)