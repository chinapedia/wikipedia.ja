> この記事は[Pentium III](https://ja.wikipedia.org/wiki/Pentium_III)から翻訳されています。


**Pentium III**（ペンティアム・スリー）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[1999年](../Page/1999年.md "wikilink")2月に発売した第6世代[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))。

[Pentium II](../Page/Pentium_II.md "wikilink") と同様に、Pentium III をベースとして下位の低価格[パソコン向けの](../Page/パーソナルコンピュータ.md "wikilink")[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")、上位にあたる[サーバ](../Page/サーバ.md "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")向けの[Pentium III Xeonが発売された](https://ja.wikipedia.org/wiki/Xeon#Pentium_III_Xeon "wikilink")。後継は[Pentium 4](../Page/Pentium_4.md "wikilink")。

インテルは、このPentium IIIで競合する[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Athlon](../Page/Athlon.md "wikilink")と激しい製品競争を繰り広げ、駆動クロック周波数はついに1GHzを突破した。

## 第一世代“カトマイ” (Katmai)

[Intel_Pentium_III_Katmai.jpg](https://ja.wikipedia.org/wiki/File:Intel_Pentium_III_Katmai.jpg "fig:Intel_Pentium_III_Katmai.jpg") 製造プロセスは0.25µm。機能的には前世代製品にあたる[Pentium IIに](../Page/Pentium_II.md "wikilink")[SSE処理ユニットを追加している](../Page/ストリーミングSIMD拡張命令.md "wikilink")。設計当時の製造技術の制約と製造コストを低減する目的から、Pentium IIと同様にCPUモジュール基板の上にCPUコアと容量512KBの2次キャッシュメモリとを個別に実装している。 パッケージは、Pentium IIから継承したS.E.C.C.2 ([Slot 1](../Page/Slot_1.md "wikilink")) のみ。

同一のクロック周波数のPentium IIと比較すると、Pentium IIIは2次キャッシュメモリのアクセスレイテンシが減少されている分、若干高速である。また、パソコンの同一性検出を目的として、個々のCPUには[ソフトウェア](../Page/ソフトウェア.md "wikilink")から読み出し可能なプロセッサ・シリアル・ナンバ (PSN) と呼ばれる96ビット長の固有IDデータ\[1\]が追加されている。

  -
    {|class="wikitable" border="1"

|- align="center" \! 動作周波数 \!\! コア数 \!\! FSB \!\! 2次キャッシュ \!\! ソケット \!\! TDP |- | 600BMHz (133x4.5) || 1 || 133MHz || 512KB || Slot1 || 34.5W |- | 600MHz (100x6) || 1 || 100MHz || 512KB || Slot1 || 34.5W |- | 550MHz (100x5.5) || 1 || 100MHz || 512KB || Slot1 || 30.8W |- | 533MHz (133x4) || 1 || 133MHz || 512KB || Slot1 || 29.7W |- | 500MHz (100x5) || 1 || 100MHz || 512KB || Slot1 || 28W |- | 450MHz (100x4.5) || 1 || 100MHz || 512KB || Slot1 || 25.3W |}

## 第二世代“カッパーマイン” (Coppermine)

[Pentium_iii_cu-mine_slot1_naked.jpg](https://ja.wikipedia.org/wiki/File:Pentium_iii_cu-mine_slot1_naked.jpg "fig:Pentium_iii_cu-mine_slot1_naked.jpg") [thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_Pentium_III_733_MHz.jpg "wikilink") 0.18µmプロセスで製造された。製造技術の発達により、256KBの2次キャッシュメモリをCPUダイ上に実装する。 512KBの2次キャッシュメモリを搭載するKatmaiと比較して容量は半減したが、CPUダイ上に実装されてCPUコアと等速で動作するようになり、さらにキャッシュアクセスの際のレイテンシが大幅に減少可能となったためより高速なメモリアクセスを実現、性能が向上している。L2キャッシュの性能向上に伴い、L2キャッシュフィルバッファ、ライトバックバッファ、バスキューエントリーを増加している。また、L1データキャッシュとL2キャッシュ間の帯域を256Bitに拡張している。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_PIII_Coppermine_Backside.JPG "wikilink") 当初は、Katmai同様S.E.C.C.2パッケージを採用していたが、2次キャッシュを外に置く必要がなくなったため、[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")で採用された[Socket 370に対応した](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")、FC-PGAパッケージでも生産されるようになった。ただしこれは従来のPPGA版Celeronで採用されたSocket 370とは一部のピンの仕様が異なっており、必ずしも既存のシステムを流用できるものではなかった。その場合はサードパーティ製の変換下駄（とBIOSの対応）が必要になり、同様の問題は後述のようにTualatinの登場時にも生じている。

Intelのx86プロセッサとしては、初めて動作クロック1GHzを達成したアーキテクチャである。

この世代でインテルはAMDの「Athlon」に対抗し、動作クロックの向上を巡って熾烈な競争を演じた。当時出たばかりのCoppermineは当初品薄が続いたが、少数出荷で発表の前倒しを繰り返し、パソコン用マイクロプロセッサの動作クロックは遂に1GHzの大台に達することとなった。

一時は1.13GHzで動作する製品も極少数が出荷されたが、動作不安定が指摘され製品回収が行われた。1.13GHzを超える製品は第三世代を待つことになる。

  -
    {| class="wikitable" border="1"

\!モデルナンバー || 動作クロック || L2容量 || FSB ||逓倍率 || コア電圧 || TDP || ソケット |- | [Pentium III 500E](http://ark.intel.com/Product.aspx?id=27537) || 500 MHz || 256 KB || 100 MHz || 5× || 1.6 V || 13.2 W ||rowspan="14" |
[Slot 1](../Page/Slot_1.md "wikilink") |- | [Pentium III 533EB](http://ark.intel.com/Product.aspx?id=27539) || 533 MHz || 256 KB || 133 MHz || 4× || 1.65 V || 14 W |- | [Pentium III 550E](http://ark.intel.com/Product.aspx?id=27541) || 550 MHz || 256 KB || 100 MHz || 5.5× || 1.6-1.7 V || 14.5 W |- | [Pentium III 600E](http://ark.intel.com/Product.aspx?id=27543) || 600 MHz || 256 KB || 100 MHz || 6× || 1.7-1.75 V || 15.8 W |- | [Pentium III 600EB](http://ark.intel.com/Product.aspx?id=27544) || 600 MHz || 256 KB || 133 MHz || 4.5× || 1.65-1.7 V || 15.8 W |- | [Pentium III 650](http://ark.intel.com/Product.aspx?id=27547) || 650 MHz || 256 KB || 100 MHz || 6.5× || 1.65-1.7 V || 17 W |- | [Pentium III 667](http://ark.intel.com/Product.aspx?id=27548) || 666 MHz || 256 KB || 133 MHz || 5× || 1.65-1.7 V || 17.5 W |- | [Pentium III 700](http://ark.intel.com/Product.aspx?id=27549) || 700 MHz || 256 KB || 100 MHz || 7× || 1.65-1.7 V || 18.3 W |- | [Pentium III 733](http://ark.intel.com/Product.aspx?id=27550) || 733 MHz || 256 KB || 133 MHz || 5.5× || 1.65-1.75 V || 19.1 W |- | [Pentium III 750](http://ark.intel.com/Product.aspx?id=27551) || 750 MHz || 256 KB || 100 MHz || 7.5× || 1.65-1.75 V || 19.5 W |- | [Pentium III 800](http://ark.intel.com/Product.aspx?id=27552) || 800 MHz || 256 KB || 100 MHz || 8× || 1.65-1.75 V || 20.8 W |- | [Pentium III 800EB](http://ark.intel.com/Product.aspx?id=27553) || 800 MHz || 256 KB || 133 MHz || 6× || 1.65-1.75 V || 20.8 W |- | [Pentium III 850](http://ark.intel.com/Product.aspx?id=27554) || 850 MHz || 256 KB || 100 MHz || 8.5× || 1.65-1.75 V || 25.7 W |- | [Pentium III 866](http://ark.intel.com/Product.aspx?id=27555) || 866 MHz || 256 KB || 133 MHz || 6.5× || 1.65-1.75 V || 22.5/22.9 W |- |[Pentium III 900](http://ark.intel.com/Product.aspx?id=27556) ||900 MHz ||256 KB ||100 MHz ||9× ||1.7-1.75 V ||28.9 W || |- | [Pentium III 933](http://ark.intel.com/Product.aspx?id=27557) || 933 MHz || 256 KB || 133 MHz || 7× || 1.65-1.75 V || 24.5/27.3 W ||rowspan="3" |
Slot 1 |- | [Pentium III 1000](http://ark.intel.com/Product.aspx?id=27528) || 1 GHz || 256 KB || 100 MHz || 10× || 1.75 V || 29 W |- | [Pentium III 1000EB](http://ark.intel.com/Product.aspx?id=27529) || 1 GHz || 256 KB || 133 MHz || 7.5× || 1.7-1.76 V || 26.1 W |- |[Pentium III 1100](http://ark.intel.com/Product.aspx?id=27530) ||1.1 GHz ||256 KB ||100 MHz ||11× ||1.75 V ||33 W ||rowspan="2" |Socket 370 |- |[Pentium III 1133](http://ark.intel.com/Product.aspx?id=27531) ||1.133 GHz ||256 KB ||133 MHz ||8.5× ||1.75 V ||29.1 W |}

### Coppermine-T

次世代Pentium IIIであるTualatinとCoppermineとの間にはシステムバスの電気的な互換性が無いため、ストップギャップを目的として双方に互換性のあるCoppermine-Tが開発されていた。しかしPentium IIIからPentium 4へ販売の主体を急激にシフトすることを決断したIntelは、Coppermine-Tの互換性がPentium 4への移行の妨げとなると考えた。そのためこのCoppermine-TはTualatinとのシステムバスの互換性を削除して発売された。その結果、Coppermine-TはCoppermineとの互換性の低さだけが特徴に残ってしまった。

Coppermine-TはCoppermineのcD0ステップ、あるいは略してDステップと称する場合が多い。

Dステップ末期のCoppermineではTualatinと同様にヒートスプレッダ（IHS; Integrated Heat Spreader）を備えたFC-PGA2パッケージも出まわり\[2\]、FC-PGA版とFC-PGA2版が混在している。後のCoppermineコアのCeleronも同様であり\[3\]、ヒートスプレッダが付いているからといってTualatinとは限らない。

  -
    {| class="wikitable" border="1"

\!モデルナンバー ||クロック ||L2 容量 ||FSB ||逓倍率 ||コア電圧 ||TDP ||ソケット |- |[Pentium III 800](http://ark.intel.com/Product.aspx?id=27553) ||800 MHz ||256 KB ||133 MHz ||6× ||1.75 V ||38.2 W ||rowspan="5" |[Socket 370](https://ja.wikipedia.org/wiki/Socket_370 "wikilink") |- |[Pentium III 866](http://ark.intel.com/Product.aspx?id=27555) ||866 MHz ||256 KB ||133 MHz ||6.5× ||1.75 V ||38.2 W |- |[Pentium III 933](http://ark.intel.com/Product.aspx?id=27557) ||933 MHz ||256 KB ||133 MHz ||7× ||1.75 V ||27.3 W |- |[Pentium III 1000](http://ark.intel.com/Product.aspx?id=27529) ||1 GHz ||256 KB ||133 MHz ||7.5× ||1.75 V ||29 W |- |[Pentium III 1133](http://ark.intel.com/Product.aspx?id=27531) ||1.13 GHz ||256 KB ||133 MHz ||8.5× ||1.75 V ||29.1 W |}

## 第三世代“テュアラティン” (Tualatin)

[thumb](https://ja.wikipedia.org/wiki/ファイル:Pentium_III-S_Tualatin.JPG "wikilink") Coppermineの製造プロセスを0.13µmへ更新した製品である。今後の製品の性能向上を念頭に置いてシステムバスの仕様を変更している。また、CPUコアの動作電圧も低下した。そのためソケットの物理的なピンレイアウトこそ変更されなかったものの、Coppermineとの電気的な互換性は事実上無くなっている。パッケージはSocket370対応製品のみとなり、従来のFC-PGAパッケージに新しく[ヒートスプレッダ](https://ja.wikipedia.org/wiki/ヒートスプレッダ "wikilink")を被せたFC-PGA2パッケージで製品が発売された。

2次キャッシュ512kB搭載のPentium III-Sが先に登場し、続いて256kBのPentium IIIが登場した。 [FSBは](../Page/フロントサイドバス.md "wikilink")133MHzの製品のみになった\[4\]。

Pentium III-SはSMP動作が可能だが、Tualatin Pentium IIIではその機能は削除されている。

しかし、世界的不況からCPUの販売量が限られてくると予想したインテルは、歩留まりがPentium IIIに劣り製造量が下回るPentium 4でも十分に需要を賄えると判断し、競合していたAMD-Athlonプロセッサとの販売競争で優位に立つ次世代CPUの[Pentium 4の普及に力を入れるようになった](../Page/Pentium_4.md "wikilink")。そのためTualatinは本来の性能や魅力を発揮しないまま終わりを迎えた。ただし、Pentium 4が苦手とする低消費電力・低発熱用途として、[ノートパソコン](../Page/ノートパソコン.md "wikilink")向けのMobile Pentium III-Mや[ブレードサーバ](../Page/ブレードサーバ.md "wikilink")向けのPentium III-Sは同条件で使用可能な後継機種の開発が遅れたことから、Pentium 4世代のプロセッサが一般化した後も暫く現行製品として販売が継続された。

  -
    {| class="wikitable" border="1"

\!モデルナンバー ||クロック ||L2 容量 ||FSB ||逓倍率 ||コア電圧 ||TDP ||ソケット |- |[Pentium III 1000](http://ark.intel.com/Product.aspx?id=27529) ||1 GHz ||256 KB ||133 MHz ||7.5× ||1.475 V ||29.9 W ||rowspan="5"|[Socket 370](https://ja.wikipedia.org/wiki/Socket_370 "wikilink") |- |[Pentium III 1133](http://ark.intel.com/Product.aspx?id=27531) ||1.13 GHz ||256 KB ||133 MHz ||8.5× ||1.475 V ||29.1 W |- |[Pentium III 1200](http://ark.intel.com/Product.aspx?id=27532) ||1.2 GHz ||256 KB ||133 MHz ||9× ||1.475 V ||29.9 W |- |[Pentium III 1333](http://ark.intel.com/Product.aspx?id=27533) ||1.33 GHz ||256 KB ||133 MHz ||10× ||1.475 V ||29.9 W |- |[Pentium III 1400](http://ark.intel.com/Product.aspx?id=27534) ||1.4 GHz ||256 KB ||133 MHz ||10.5× ||1.5 V ||31.2 W |}

### Pentium III-S

2次キャッシュ量256kBを512kBへと倍増、[SMP対応したモデル](../Page/対称型マルチプロセッシング.md "wikilink")。

  -
    {| class="wikitable" border="1"

\!モデルナンバー ||クロック ||L2 容量 ||FSB ||逓倍率 ||コア電圧 ||TDP ||ソケット |- |[Pentium III 1000S](http://ark.intel.com/Product.aspx?id=31855)\[5\]\[6\] ||1 GHz ||512 KB ||133 MHz ||7.5× ||1.475 V ||29.9 W ||rowspan="4"|[Socket 370](https://ja.wikipedia.org/wiki/Socket_370 "wikilink") |- |[Pentium III 1133S](http://ark.intel.com/Product.aspx?id=27523) ||1.13 GHz ||512 KB ||133 MHz ||8.5× ||1.45 V ||28.7 W |- |[Pentium III 1266S](http://ark.intel.com/Product.aspx?id=27524) ||1.26 GHz ||512 KB ||133 MHz ||9.5× ||1.45 V ||30.4 W |- |[Pentium III 1400S](http://ark.intel.com/Product.aspx?id=27525) ||1.4 GHz ||512 KB ||133 MHz ||10.5× ||1.45 V ||32.2 W |}

## 脚注

## 関連項目

  - [P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")
  - [ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE)
  - [Intel SpeedStep テクノロジ](../Page/Intel_SpeedStep_テクノロジ.md "wikilink")

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  その内32ビットはいわゆるS-Specなどを識別するためのCPUIDが使用するため、個体識別に用いる固有のIDは残る64ビットを使用する。
2.
3.
4.  なお、TualatinコアのCeleronのFSBは100MHzであり、2次キャッシュはレイテンシがやや高いものの256kB搭載していたので、Pentium IIIとCeleronの性能差は小さかった。
5.  [Pentium III 1000S](http://www.cpu-world.com/sspec/SL/SL5PS.html)
6.  [Pentium III 1000S(OEM)](http://www.x86-guide.com/en/cpu/Intel-Pentium-III-S-1000-cpu-no3010.html)