> この記事は[EDSAC](https://ja.wikipedia.org/wiki/EDSAC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:EDSAC_\(10\).jpg "wikilink") **EDSAC**（エドサック、**E**lectronic **D**elay **S**torage **A**utomatic **C**alculator\[1\]）は、初期の[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の[コンピュータ](../Page/コンピュータ.md "wikilink")のひとつ\[2\]。このマシンは[ジョン・フォン・ノイマン](../Page/ジョン・フォン・ノイマン.md "wikilink")がまとめた[EDVAC](../Page/EDVAC.md "wikilink")についてのレポート（[EDVACに関する報告書の第一草稿](https://ja.wikipedia.org/wiki/EDVACに関する報告書の第一草稿 "wikilink")）に刺激され、[モーリス・ウィルクス](https://ja.wikipedia.org/wiki/モーリス・ウィルクス "wikilink")と[ケンブリッジ大学](https://ja.wikipedia.org/wiki/ケンブリッジ大学 "wikilink")の数学研究所のチームが開発した。EDSACは、世界初の**実用的な**[プログラム内蔵方式](https://ja.wikipedia.org/wiki/プログラム内蔵方式 "wikilink")の[電子計算機であるが](../Page/コンピュータ.md "wikilink")、プログラム内蔵方式の世界初の稼働したマシンではない\[3\]。

プロジェクトは J. Lyons & Co. Ltd. が資金援助し、同社はEDSACのデザインに基づいた初の商用コンピュータ LEO I を開発した。[1949年](../Page/1949年.md "wikilink")[5月6日](../Page/5月6日.md "wikilink")、EDSAC上で最初に動作したプログラムは、0から99までの整数の二乗の表を作るプログラムと\[4\]、[素数](../Page/素数.md "wikilink")のリストを作るプログラムであった。

## 技術概要

### ハードウェア構成

EDSACが開発されると即座に大学の研究用に使われ始めた。3000本の[真空管](https://ja.wikipedia.org/wiki/真空管 "wikilink")を使用し、消費電力は12kW。[主記憶装置](../Page/主記憶装置.md "wikilink")には[水銀遅延管を使用している](../Page/遅延記憶装置.md "wikilink")。入力には5孔の[紙テープ](../Page/紙テープ.md "wikilink")を使用し、出力には[テレタイプ端末](https://ja.wikipedia.org/wiki/テレタイプ端末 "wikilink")を使用している。

当初、[レジスタとしては](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")[アキュムレータと乗算器用レジスタしかなかった](https://ja.wikipedia.org/wiki/アキュムレータ_\(コンピュータ\) "wikilink")。[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")、[デビッド・ホイーラー](https://ja.wikipedia.org/wiki/デビッド・ホイーラー "wikilink")が[イリノイ大学から戻ると](https://ja.wikipedia.org/wiki/イリノイ大学アーバナ・シャンペーン校 "wikilink")、[インデックスレジスタ](https://ja.wikipedia.org/wiki/インデックスレジスタ "wikilink")を設計してEDSACのハードウェアを拡張している。

### 記憶装置と命令

主記憶容量は1024ワード（1ワード（ショートワード）は17ビット）だが、実際にメモリが実装されたのは512ワードまでだった。ロングワードは35ビットで、偶数アドレスと奇数アドレスのショートワードを、真ん中に「サンドイッチビット」 と呼ばれるビット（記憶装置の都合によるスタートビット兼ストップビットのようなものがそのまま入る）を挟んで連続して使用する。数値は[2の補数](../Page/2の補数.md "wikilink")表現の[二進数である](../Page/二進法.md "wikilink")。

18個の[命令を備えていた](https://ja.wikipedia.org/wiki/命令_\(コンピュータ\) "wikilink")。17ビットのショートワード先頭5ビットが命令コードだが、紙テープの文字コードをそのまま使い、ニーモニックの文字コードを命令コードとしていた。例えば "Add" 命令の命令コードは "A" の文字コードだった。その後に1ビットの未使用ビットをはさみ、10ビットのメモリアドレスがあり、最後の1ビットはオペランドがショートワードなのかロングワードなのかを指定する。

[乗算器](https://ja.wikipedia.org/wiki/乗算器 "wikilink")は数値を[固定小数点数](../Page/固定小数点数.md "wikilink")として扱い、その範囲は -1 ≤ *x* \< 1 となるよう設計されている。すなわち、小数点は符号のすぐ後にある。[アキュムレータは](https://ja.wikipedia.org/wiki/アキュムレータ_\(コンピュータ\) "wikilink")71ビット幅で、35ビットのロングワード同士の乗算を行っても切捨てが起きないよう設計されている。

命令としては、加算、減算、乗算、照合\[5\]、左シフト、右シフト、乗算器用レジスタへのロード、アキュムレータの内容のストア（オプションでアキュムレータをクリア）、条件付スキップ、入力テープ読み込み、文字印字、アキュムレータを丸める、NOP、ストップなどがある。除算命令はなく（サブルーチンで実装）、アキュムレータに直接メモリからロードする命令もない（アキュムレータをストア命令でゼロクリアしてから\[6\]加算命令で「ゼロに該当の値を加算」することで、ロードと同様の結果になる）。

### システムソフトウェア

イニシャルオーダ (initial orders) はスイッチ群で実装されていて、起動時にメモリの先頭ワード群にロードされる。1949年5月には、上述したニーモニック設計を生かした初歩的な[アセンブラの機能がわずか](../Page/アセンブリ言語.md "wikilink")31ワードのイニシャルオーダに搭載されている\[7\]。これが世界初のアセンブラであり、ソフトウェア産業の出発点とも言える。

EDSACは同大学の様々な実際の問題を解くのに使われ、今日の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に含まれるような様々な技法が考案された。ユーザーはプログラムをアセンブリ言語で書くと、紙テープをさん孔して入力の準備をする。ユーザーは紙テープを見てコードを読み取れるようになった。準備ができると、紙テープを読取装置の近くにある紐に引っ掛ける。オペレータはその紐に引っ掛けられた紙テープ群から1つを選び、EDSACに読み込ませる。これがいわゆるジョブキューの役割を果たした。プログラムの実行によってプリントアウトされたものと紙テープはユーザーに返される。何も出力されない場合は停止したメモリ位置をユーザーに知らせる。[デバッガ](../Page/デバッガ.md "wikilink")はまだなかったが、ブラウン管を使って指定したメモリ位置の内容を表示することができた。これは例えば数値が収束しているかどうかを見るのに使われた。通常業務時間が終了すると、許可を得たユーザーが自らマシンを操作でき、真空管が故障しない限り夜遅くまで使っていたが、あるユーザーによれば真空管の故障はよく起きたという\[8\]。

### プログラミング技法

初期のプログラマは今日では推奨されない技法、特に[コード書き換えを使う必要があった](https://ja.wikipedia.org/wiki/自己書き換えコード "wikilink")。当初インデックスレジスタがなかったため、配列にアクセスするには命令内のアドレス部分を実行時に書き換えてやる必要があった。

[デビッド・ホイーラー](https://ja.wikipedia.org/wiki/デビッド・ホイーラー "wikilink")はこのプロジェクトで世界初の[計算機科学](../Page/計算機科学.md "wikilink")のPhDを取得したが、[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")の概念の発明者とされている。ルーチンにジャンプする命令のあるアドレスに1を加えたアドレスをレジスタに格納した状態でルーチンにジャンプする（これを Wheeler jump と呼ぶ）。サブルーチン側はその渡されたアドレスで最後尾のジャンプ命令のアドレス部を書き換える。この書き換えをサブルーチンの先頭で行えば、さらに別のサブルーチンコールを呼ぶ、入れ子を実現することもできる（再帰はできない、ということに注意）。

ただし当時は[リロケータブルバイナリ](https://ja.wikipedia.org/wiki/リロケータブルバイナリ "wikilink")などといったものがあるわけでは当然なく、プログラマがジャンプ先の位置を計算する必要があり、各ルーチンの長さを予め正確に知っている必要があった。サブルーチンはあらかじめマスターテープとして作られており、それをテープ上でプログラム本体の後ろに続けてコピーするというならば「人力リンク」のような作業が行われていた（そのため、サブルーチンの先頭位置はプログラムによって異なるが、コーディングの際には事前のアドレス計算により求めておく必要があった）。\[9\]

また重要なこととして、以上のような技法を初めとした、本機の利用によって得られた経験と、具体的にそのプログラムとを *The Preparation of Programs for an Electronic Digital Computer* という書籍として公刊し、世界的に広く読まれた、ということが挙げられる。当時は米国の一部のコンピュータのように、軍や兵器や米国の安全に関与しているため秘密にすることが強要され知見が全く共有されなかった等といった例もあった中で、同書は世界的に「プログラミング」の実例を広めたのみならず、その後に[プログラム内蔵方式](https://ja.wikipedia.org/wiki/プログラム内蔵方式 "wikilink")（乃至、[ノイマン型](../Page/ノイマン型.md "wikilink")）コンピュータを設計する者への指針ともなったなど、広く世界に貢献した。

### アプリケーションソフトウェア

サブルーチンの概念からライブラリができるようになった。1951年には次のような分野の87のサブルーチンが広く使われていた。

  - [浮動小数点演算](../Page/浮動小数点数.md "wikilink")、[複素数](../Page/複素数.md "wikilink")演算
  - 除算、べき乗
  - 各種関数（[三角関数](../Page/三角関数.md "wikilink")など）
  - [微分方程式](../Page/微分方程式.md "wikilink")
  - [冪級数](https://ja.wikipedia.org/wiki/冪級数 "wikilink")
  - [対数](../Page/対数.md "wikilink")
  - 印字レイアウト
  - [数値積分](https://ja.wikipedia.org/wiki/数値積分 "wikilink")
  - 入力
  - 反復処理（[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")、[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")）
  - ベクトル、[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")

## EDSACの利用例

  - 1950年、ウィルクスとホイーラーは[ロナルド・フィッシャー](https://ja.wikipedia.org/wiki/ロナルド・フィッシャー "wikilink")の論文\[10\]にあった遺伝子頻度に関する微分方程式をEDSACで解いた。これは生物学分野での世界初のコンピュータ利用である。
  - 1951年、ミラーとホイーラーは当時としては最大の79桁の素数を発見した\[11\]。
  - 1952年、大学院生だった[アレキサンダー・サンディ・ダグラスは](https://ja.wikipedia.org/wiki/アレキサンダー・ダグラス "wikilink")[三目並べ](https://ja.wikipedia.org/wiki/三目並べ "wikilink")のグラフィカルバージョンである 『[OXO](https://ja.wikipedia.org/wiki/OXO "wikilink")』 というプログラムをEDSAC上で作成した。これが画面写真が残っている世界初の[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")である。
  - 以下は後継機のEDSAC 2（[:en:EDSAC 2](https://ja.wikipedia.org/wiki/:en:EDSAC_2 "wikilink")）による（後継機 EDSAC 2 の稼働により、先代 EDSAC の稼働は終了した）
      - 1960年代、[楕円曲線](https://ja.wikipedia.org/wiki/楕円曲線 "wikilink")に関する数値演算に使われた。具体的には、[バーチ・スウィンナートン＝ダイアー予想](https://ja.wikipedia.org/wiki/バーチ・スウィンナートン＝ダイアー予想 "wikilink")（BSD予想）を導いた計算である。

## その後の開発

EDSACの後継機 EDSAC 2 は[1958年](../Page/1958年.md "wikilink")に動作を開始した。[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")、EDSAC 2 用の[Autocode](https://ja.wikipedia.org/wiki/Autocode "wikilink")（[ALGOL](../Page/ALGOL.md "wikilink")風の科学技術計算用[高水準言語](../Page/高水準言語.md "wikilink"))を D.F. Hartley が開発した。

1960年代半ばには EDSAC 2 の後継機が計画されたが、結局 Atlas 2 のプロトタイプである Titan が導入された。Atlas 2 は[マンチェスター大学](https://ja.wikipedia.org/wiki/マンチェスター大学 "wikilink")、[フェランティ](https://ja.wikipedia.org/wiki/フェランティ "wikilink")、Plessy の三者で開発した Atlas コンピュータの後継機である。

## 復元プロジェクト

2011年1月13日、[Computer Conservation Society](https://ja.wikipedia.org/wiki/:en:Computer_Conservation_Society "wikilink") がEDSACの実動するレプリカを[ブレッチリー・パーク](https://ja.wikipedia.org/wiki/ブレッチリー・パーク "wikilink")の[国立コンピューティング博物館](https://ja.wikipedia.org/wiki/国立コンピューティング博物館 "wikilink")にて製作すると発表した\[12\]。2015年の稼働を目指し、その後は定期的に動作させるデモンストレーションを行う予定だという。

プロジェクトを指揮する [Andrew Herbert](https://ja.wikipedia.org/wiki/:en:Andrew_Herbert "wikilink") はモーリス・ウィルクスの下で学んだことがある。

## 参考文献

  - *The Preparation of Programs for an Electronic Digital Computer* by Professor Sir [Maurice Wilkes](https://ja.wikipedia.org/wiki/モーリス・ウィルクス "wikilink"), [David Wheeler](https://ja.wikipedia.org/wiki/デビッド・ホイーラー "wikilink") and Stanley Gill, Addison–Wesley, Edition 1, 1951\[13\]

## 脚注

## 関連項目

  - [計算機の歴史](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink")
  - [真空管式コンピュータ一覧](https://ja.wikipedia.org/wiki/真空管式コンピュータ一覧 "wikilink")

## 外部リンク

  - [50th Anniversary of EDSAC Site](http://www.cl.cam.ac.uk/UoCCL/misc/EDSAC99/)
  - [An EDSAC simulator](http://www.dcs.warwick.ac.uk/~edsac/) — Developed by Martin Campbell-Kelly, Department of Computer Science, [University of Warwick](https://ja.wikipedia.org/wiki/ウォーリック大学 "wikilink"), England.
  - [Oral history interview with David Wheeler, 14 May 1987](http://purl.umn.edu/107711). [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota.
  - Nicholas Enticknap and Maurice Wilkes, [Cambridge's Golden Jubilee](http://www.cs.man.ac.uk/CCS/res/res22.htm#b) — in: RESURRECTION The Bulletin of the Computer Conservation Society. ISSN 0958-7403. Number 22, Summer 1999.

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:アセンブリ言語](https://ja.wikipedia.org/wiki/Category:アセンブリ言語 "wikilink")

1.  "delay storage" は使用している[遅延記憶装置](../Page/遅延記憶装置.md "wikilink")を指している
2.
3.  [Manchester Mark Iの](https://ja.wikipedia.org/wiki/Manchester_Mark_I "wikilink")[プロトタイプ](https://ja.wikipedia.org/wiki/プロトタイプ "wikilink")である*[Baby](https://ja.wikipedia.org/wiki/Manchester_Small-Scale_Experimental_Machine "wikilink")*の方が早い。ただし Baby は[ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")の評価用に製作されており、実用的ではなかった。[A brief informal history of the Computer Laboratory](http://www.cl.cam.ac.uk/conference/EDSAC99/history.html) を参照。マンチェスター大学では1949年4月から [Manchester Mark I](http://www.computer50.org/mark1/MM1.html) が稼働しはじめているが、完成したのは少し後である。
4.
5.  指定されたメモリワードと乗算器用レジスタの内容に[ビット単位のANDを施し](https://ja.wikipedia.org/wiki/ビット演算 "wikilink")、結果をアキュムレータに格納する命令
6.  ストア命令に、単にストアする命令と、ストアに引き続きアキュムレータをゼロクリアする命令の2種類があり、その後者を使う、ということ。
7.
8.  Professor David Barron, Emeritus Professor of the University of Southampton at a Cambridge Computer Lab seminar to mark the 60th anniversary May 6th 2009.
9.  当時の資料映像に、1976年にウィルクスが解説を付けた動画（ <https://www.youtube.com/watch?v=6v4Juzn10gM> ）にプログラミングの光景がある。4分から5分のあたりで設計、5分から5分30秒のあたりでコーディング、5分30秒から先のあたりで、紙テープへのパンチングと、該当するサブルーチンの編集等の作業が見られる。
10. [Gene Frequencies in a Cline Determined by Selection and Diffusion](http://www.jstor.org/stable/3001780), R. A. Fisher, Biometrics, Vol. 6, No. 4 (Dec., 1950), pp. 353-361
11. [Caldwell - largest known primes by year](http://primes.utm.edu/notes/by_year.html) One reference gives Miller, J. C. P. "Larger Prime Numbers" (1951) *Nature* 168(4280):838, ただし [こちら](http://www.nature.com/nature/journal/v168/n4280/abs/168838b0.html)には言及がない。
12.
13.