> この記事は[Intel i960](https://ja.wikipedia.org/wiki/Intel_i960)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:Intel_A80960CA25_L6395332_top.jpg "wikilink") **i960**（または**80960**）は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[RISC](../Page/RISC.md "wikilink")ベースの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。1990年代初めに[組み込みシステム](../Page/組み込みシステム.md "wikilink")用[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")として人気を集め、当時[AMD Am29000が市場で占めていた場所を奪った](../Page/AMD_Am29000.md "wikilink")。そのように成功したにもかかわらず、[1990年代](../Page/1990年代.md "wikilink")後半になるとインテルは[マーケティング](../Page/マーケティング.md "wikilink")上i960を捨てて[DECとの訴訟問題の和解案で購入した](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[StrongARM](../Page/StrongARM.md "wikilink")に乗り換えた。

## 開発経緯

i960の開発は[1980年代](../Page/1980年代.md "wikilink")初頭に[iAPX 432の失敗を受けて開始された](../Page/Intel_iAPX_432.md "wikilink")。iAPX 432はハードウェアで高級言語（例えば[Ada](../Page/Ada.md "wikilink")や[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")）を直接サポートすることを意識して、タグ付き・プロテクト付きで自動的に[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を行うメモリシステムを持たせようとしていた。しかし、[命令セット](../Page/命令セット.md "wikilink")が複雑になりすぎたことや他の設計上の問題のため、当時の他のプロセッサと比較してiAPX 432は非常に性能が低かった。

[1984年](../Page/1984年.md "wikilink")インテルと[シーメンス](../Page/シーメンス.md "wikilink")はAdaをシステム言語として使用する[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")・[フォールトトレラント](../Page/フォールトトレラントシステム.md "wikilink")・[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")コンピュータシステムを開発しようという共同プロジェクト（[BiiN](../Page/BiiN.md "wikilink")）を開始した。i432のチームメンバの多くがこれに参加したが、指揮官は[IBM](../Page/IBM.md "wikilink")から来たであった。BiiNシステムが想定した市場は[銀行](../Page/銀行.md "wikilink")、[産業システム](https://ja.wikipedia.org/wiki/産業システム "wikilink")、[原子力発電所](../Page/原子力発電所.md "wikilink")などの高信頼コンピュータを必要とするところであり、i432の保護されたメモリというコンセプトはBiiNシステムの設計に影響を与えた。

i432で苦しんだ性能問題を回避するため、中心となるi960の[命令セット](../Page/命令セット.md "wikilink")アーキテクチャ (ISA)はRISCとされ（**i960MX**でのみ完全に実装された）、メモリサブシステムは33ビット幅（32ビットのアドレスと保護されたメモリを表す1ビットのタグ）となった。他の様々な点ではi960はバークレーの[RISC](../Page/RISC.md "wikilink")を踏襲し、[レジスタ・ウィンドウ](../Page/レジスタ・ウィンドウ.md "wikilink")を採用した点が特筆される。対抗する[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")のデザイン（[MIPSとして商用化された](../Page/MIPSアーキテクチャ.md "wikilink")）では、[コンパイラの最適化に任せて](../Page/コンパイラ最適化.md "wikilink")、そのような機能は持たなかった。[メモリ管理](../Page/メモリ管理.md "wikilink")については、平坦な32ビット空間を採用し、[セグメント方式](../Page/セグメント方式.md "wikilink")は採用しなかった。i960は複数の命令を並行して複数のプロセッサ内ユニットで実行する[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")実装を期待されていた。

## 製品としての歴史

最初の960プロセッサ・**i960MC**は[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")10月に[テープアウト](../Page/テープアウト.md "wikilink")（チップ製造のためのマスクパターンが完成）して工場に送られ、最初の実動するチップが出来たのは1985年末から[1986年](../Page/1986年.md "wikilink")初にかけてであった。BiiNは市場の変化に伴って消滅し、960MXだけが使われずに残された。MyersはBiiNシステム向けのアーキテクチャからサブセットを抜き出した。Myersはインテル経営陣を説得し、i960を汎用プロセッサ市場に出そうとした。当時の市場は[80286が主力で](../Page/Intel_80286.md "wikilink")、同時期に[80386も市場に出ようとしていた](../Page/Intel_80386.md "wikilink")。また、[UNIX](../Page/UNIX.md "wikilink")システムなどのRISC市場もターゲットとし、[NeXT](../Page/NeXT.md "wikilink")で使ってもらうことも打診した。インテル内外のライバルとしては[i860もあった](../Page/Intel_i860.md "wikilink")。

Myersはインテル経営陣を十分に説得できず、i960を汎用あるいはUNIX市場に売り出すことはできなかったが、ハイエンド32ビット[組み込みシステム](../Page/組み込みシステム.md "wikilink")市場に活路を見出した。保護付きメモリ機能はBiiN特有とみなされ、製品の[説明書では触れられなかった](../Page/マニュアル.md "wikilink")。このため多くの人がi960MCが無駄に大きくて使わない[ピンが多いことをいぶかしんだ](https://ja.wikipedia.org/wiki/端子 "wikilink")。メモリ管理を省いたものは**i960KA**と名づけられ、[FPU](../Page/FPU.md "wikilink")を省いたものは**i960KB**と名づけられた。ただし、これらのバージョンはラベルが違うだけで中身は同じチップだった。

完全な**i960MX**は[軍用以外には販売されなかったが](../Page/軍需産業.md "wikilink")、i960MCはハイエンド組み込み用途で使われ、i960KAは[レーザープリンタ](https://ja.wikipedia.org/wiki/レーザープリンタ "wikilink")市場や初期のグラフィック端末などの組み込み用途で低価格32ビットプロセッサとして成功した。最初の純粋なRISC実装は**i960CA**で、スーパースケーラ方式であり、珍しいアドレスを持ったオンチップキャッシュを持っていた。i960CAは一般的に世界初のシングルチップのスーパースケーラRISCと考えられている。Cの付くシリーズはALUをひとつしか持っていないが、算術演算命令とメモリ参照命令と分岐命令を並行して実行できた。**i960CF**はFPUを内蔵したが、MMUは削除したままだった。

インテルはi960を[I2O](https://ja.wikipedia.org/wiki/I2O "wikilink")標準の入出力機器コントローラとして売り出して梃入れしようとしたが、あまり成功せず、結局開発を終了することになった。[1990年代](../Page/1990年代.md "wikilink")中盤、[価格性能比](https://ja.wikipedia.org/wiki/価格性能比 "wikilink")で後発のチップに抜かれるようになった。また、インテルは低電力版を出そうともしなかった。

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")、i960の設計チームは[i386の後継プロセッサの第二設計チームに移行し](../Page/Intel_80386.md "wikilink")、[Pentium Proの設計に携わることになる](../Page/Pentium_Pro.md "wikilink")。i960のプロジェクトはより小さなチームに引き継がれ、終焉を迎えることになる。

## 関連項目

  - [μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")