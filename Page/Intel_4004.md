> この記事は[Intel 4004](https://ja.wikipedia.org/wiki/Intel_4004)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:Intel_4004.jpg "wikilink") **4004**（よんまるまるよん、と読まれることが多い）は、[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社によって開発された1チップの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")であり、軍用の[MP944](https://ja.wikipedia.org/wiki/セントラル・エア・データ・コンピュータ "wikilink")\[1\]、組み込み用のTI製[TMS-1000](https://ja.wikipedia.org/wiki/TMS-1000 "wikilink")等とほぼ同時期の、世界最初期のマイクロプロセッサのひとつである。周辺ファミリ[ICを含めてMCS](../Page/集積回路.md "wikilink")-4 Micro Computer Set、あるいは略し単にMCS-4とも呼ぶ。

[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")発表、[4ビット](https://ja.wikipedia.org/wiki/4ビット "wikilink")マイクロプロセッサである。[クロック周波数](https://ja.wikipedia.org/wiki/クロック周波数 "wikilink")は、500[kHzから](../Page/ヘルツ.md "wikilink")741kHz\[2\]である。回路構成は[クロック同期設計](https://ja.wikipedia.org/wiki/クロック同期設計 "wikilink")で、pMOSプロセスで3[mm](../Page/ミリメートル.md "wikilink")×4mmのチップ（ダイ）の上に2,300個の[トランジスタ](../Page/トランジスタ.md "wikilink")を集積、10[μm](https://ja.wikipedia.org/wiki/マイクロメートル "wikilink") (0.01mm) ピッチの[プロセス・ルールで製造された](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")。当時のICとして標準的な16ピン[DIPの](https://ja.wikipedia.org/wiki/集積回路#DIP_\(Dual_Inline_Package\) "wikilink")[パッケージに収納するため](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\) "wikilink")、物理的に4ビット幅の[バスを](../Page/バス_\(コンピュータ\).md "wikilink")、アドレスとデータで時分割で使用している。

## 歴史

[Busicom_calculator.jpg](https://ja.wikipedia.org/wiki/File:Busicom_calculator.jpg "fig:Busicom_calculator.jpg") 141-PF」。[国立科学博物館](https://ja.wikipedia.org/wiki/国立科学博物館 "wikilink")の展示。\[3\]\]\] 4004は[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[ビジコン](https://ja.wikipedia.org/wiki/ビジコン "wikilink")社とインテルによる共同開発である。

1969年、ビジコンはプログラム制御\[4\]の[電卓](../Page/電卓.md "wikilink")を計画し、インテルにそのためのチップセットの開発を依頼していた。ビジコンの当初案では、マクロ命令による制御で、10個前後\[5\]のチップが必要というものだった。これは電卓としては汎用（プログラム次第でいろいろな電卓ができる）だが、電卓用という意味では専用のチップ、というものであった。

これに対し、当時のインテルの規模ではそれだけ多くの種類のチップを同時に開発するのは手に余るため、インテルの技術者[テッド・ホフは](https://ja.wikipedia.org/wiki/マーシャン・ホフ "wikilink")、ワード長が4ビットであることを除けば、汎用のコンピュータそのものという構成を提案した。複数桁の演算処理は、1桁（4ビット）の演算の反復で置き換えればよく、また、外部機器の制御も、ソフトウェアによる制御に置き換えればよい、というのである。これにより開発するチップの種類を削減した。1969年8月末のことで、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の原点となった。

このアイディアにもとづき、[嶋正利](https://ja.wikipedia.org/wiki/嶋正利 "wikilink")と[フェデリコ・ファジン](https://ja.wikipedia.org/wiki/フェデリコ・ファジン "wikilink")が中心となって、嶋が論理設計しファジンが物理設計（回路設計とマスクレイアウト）を行い、4004は完成した。

当初の契約では、このチップはビジコンに対する専売となっていたが、チップの汎用性に気付いたインテルが他への販売を希望し、一方でビジコン側は資金の要求があった事から、契約金の一部をビジコンに払い戻すことでインテルはチップの販売権を得て、 1971年[11月15日](../Page/11月15日.md "wikilink")に4004として出荷が開始された。

### 文献

  - [嶋正利](https://ja.wikipedia.org/wiki/嶋正利 "wikilink")『マイクロコンピュータの誕生 ──わが青春の4004』

## 特徴

[thumb](https://ja.wikipedia.org/wiki/ファイル:4004_arch.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:4004_dil.svg "wikilink")

  - 最高動作周波数 741kHz。ただし、命令アドレス出力に3クロック、命令読み出しに2クロック、命令実行に3クロックの計8クロックを要する。
  - プログラムのメモリ空間とデータのメモリ空間の分離（[ハーバード・アーキテクチャ](https://ja.wikipedia.org/wiki/ハーバード・アーキテクチャ "wikilink")）。近年のキャッシュのそれのような性能目的による物理的なバスの分離ではなく、命令セットアーキテクチャ的（論理的）にそれぞれの空間が異なる、というものである。
  - また、ピン数の節約のため、以下の信号は単一の4ビット物理バスを共用（時分割多重化）し、またデータ以外はそれぞれ順次送り出す方式である。
      - 12ビットのアドレス
      - 8ビットの命令
      - 4ビットのデータ
  - 46種の命令がある（うち41種は8ビット長、5種は16ビット長）。
  - 16個の4ビット長レジスタ
  - RAMのアドレスを指すようなスタックポインタは無く、プログラムカウンタ直結の、サブルーチン呼出時の退避専用のハードウェアスタックがある。深さは3段。

## MCS-4

[right](https://ja.wikipedia.org/wiki/ファイル:MCS-4.jpg "wikilink") 当初の周辺チップとしては、容量2048bitのマスクROM 4001、容量320bitのRAM 4002、10bit[シフトレジスタ](https://ja.wikipedia.org/wiki/シフトレジスタ "wikilink")兼10bit出力ポートの4003があった。これらを含めてMCS-4（Micro Computer Set）とした。

初期ファミリ内でのチップの組み合わせで、ROM 32768bit(2048bit×16)、RAM 1280bit(320bit×4)の構成が可能。

ビジコンの目的であった電卓における構成は、だいたい以下のようなものとなる。

1.  4001に関数などのプログラムが格納されている
2.  4003でキー入力をシフトしながら4004へ渡す
3.  4004で入力された数値を4002に書き込む
4.  4001にあるプログラムを使って4004で1桁ずつ演算を行い結果を4002に書き込む
5.  4003でシフトしながら表示板に出力する

## 脚注

<div class="references-small">

<references/>

</div>

## 関連項目

  - [Intel 8008](https://ja.wikipedia.org/wiki/Intel_8008 "wikilink")
  - [Intel 4040](https://ja.wikipedia.org/wiki/Intel_4040 "wikilink")

## 外部リンク

  - [インテル博物館](http://www.intel.co.jp/jp/intel/museum/hof/index.htm)
  - [嶋正利氏の4004開発回顧録](http://itpro.nikkeibp.co.jp/article/Watcher/20061219/257298/)
  - [4004 Dr嶋 ブログ](http://v-t.jp/premier/)（リンク切れ）

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  [F-14戦闘機用](../Page/F-14_\(戦闘機\).md "wikilink")[Central Air Data Computer](https://ja.wikipedia.org/wiki/セントラル・エア・データ・コンピュータ "wikilink")
2.  より:クロック周期最小1.35μsec（約741kHz）/最大2.0μsec（500kHz）。『マイクロコンピュータの誕生』によれば、先に周波数を750kHzと決め、そこからその周期内で動作するよう機能を決めている
3.  [国立科学博物館](http://www.kahaku.go.jp/exhibitions/vm/past_parmanent/rikou/Field_1/Detail_106.html)
4.  『[電子立国日本の自叙伝](https://ja.wikipedia.org/wiki/電子立国日本の自叙伝 "wikilink")』第5回「8ミリ角のコンピューター」ではこれを「ストアードプログラム」と説明しているが、普通のコンピュータのような汎用という訳ではない。また嶋は著書で「ランダム論理」（ワイヤード論理制御）に対するものとして「プログラム論理」という語を使っている。
5.  嶋の著書『マイクロコンピュータの誕生』によれば、何回か提案しており数は上下する。インテルは12種類としている。嶋は最終的にはプリンタ付きで8個、表示のみで6個まで削減できたと書いている。