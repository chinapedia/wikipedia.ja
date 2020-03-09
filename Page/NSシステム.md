> この記事は[NS](https://ja.wikipedia.org/wiki/NS)から翻訳されています。


**NSシステム（Numerical Simulatorシステム）**は[航空宇宙技術研究所](https://ja.wikipedia.org/wiki/航空宇宙技術研究所 "wikilink")が研究用に構築した数値シミュレーション向けの[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")システムである。また特にその第2世代の愛称**NWT**（**Numerical Wind Tunnel**、**数値風洞**）でも知られる。

## 概要

同研究所のコンピュータを年代順に辿ると、1960年8月に、測定部の断面が2m×2mの大型遷音速風洞（[YS-11](../Page/YS-11.md "wikilink")には間に合わなかったという）のデータ処理のために導入された[バロース](https://ja.wikipedia.org/wiki/バロース "wikilink")のDatatron 205、次いで1960年代中頃に導入された[HITAC](https://ja.wikipedia.org/wiki/HITAC "wikilink") 5020、5020Fが続く\[1\]。HITAC 5020(F)は1975年に撤去されたという\[2\]。

研究所では1960年代以来、風洞実験などの実験を[数値計算による](https://ja.wikipedia.org/wiki/数値解析 "wikilink")[シミュレーション](../Page/シミュレーション.md "wikilink")「[数値流体力学](https://ja.wikipedia.org/wiki/数値流体力学 "wikilink")」でおこなう、数値シミュレーション技術の研究開発に取り組んで来た。1977年に、[富士通](../Page/富士通.md "wikilink")の[ベクトル型](../Page/ベクトル計算機.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")VPシリーズの原型である[FACOM](../Page/FACOM.md "wikilink") 230-75 APU（アレイプロセッサの意）を導入しているが、同機は「日本スパコンの父」とも呼ばれる当研究所の[三好甫](https://ja.wikipedia.org/wiki/三好甫 "wikilink")と富士通が協力して建造したものである\[3\]。

NSの名が付くのは1987年、富士通に特別発注し開発・納入されたFACOM VP-400（[FACOM\#VPシリーズ](https://ja.wikipedia.org/wiki/FACOM#VPシリーズ "wikilink")）を中核とする第1期数値シミュレータNSI（Numerical Simulator I）からである。

並行して並列ベクトル機の研究開発が開始され、1993年には第2世代数値シミュレータNSIIとして、[VPP](https://ja.wikipedia.org/wiki/VPP "wikilink")シリーズがベースの、世界初の分散主記憶型ベクトルスーパーコンピュータ「**NWT**（**Numerical Wind Tunnel**、**数値風洞**）」が稼働を開始し、1993年11月と1994年11月～1995年11月の[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")で世界一を記録した（その後、SR-2201・[CP-PACSにより引き続き日本勢の世界一が続いた](https://ja.wikipedia.org/wiki/PACS "wikilink")）。NSIIでは、100万格子点規模の粘性流計算を10分程度で行うことを可能としたが、それでも導入後3年目以降には稼働率90%という状態が続き、航空宇宙における計算需要を十分に満たせなくなった。NWTは、実用計算機としては数少ない[GaAsトランジスタの使用例である](https://ja.wikipedia.org/wiki/ヒ化ガリウム "wikilink")。前述の三好甫は、当世代の開発まで官民を先導し、1993年の当所退官後も[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")（初代）のリーダーをつとめるなど、日本の[HPCを先導した](https://ja.wikipedia.org/wiki/高性能計算 "wikilink")。

第3世代数値シミュレータNSIIIは2002年に導入され、128個の[CPU](../Page/CPU.md "wikilink")を搭載した「富士通[PRIMEPOWER](https://ja.wikipedia.org/wiki/PRIMEPOWER "wikilink")」14台を高速インターコネクト[InfiniBand](https://ja.wikipedia.org/wiki/InfiniBand "wikilink")で接続することにより、ベクトルからスカラーへの移行であったものの、従来システムと比較した演算性能は30倍以上（理論ピーク性能9.3TFLOPS）、主記憶容量は80倍以上（3.6TB）となった。

[JAXA統合後](https://ja.wikipedia.org/wiki/宇宙航空研究開発機構 "wikilink")、旧各組織の各コンピュータは、情報・計算工学（JEDI）センターによる運用となり、NSシステムは同センターの計算機運用・利用技術チームにより、JAXAスーパーコンピュータ（JSS）ネットワークに接続されて運用されている\[4\]。NSシステム他、調布航空宇宙センターの計算機は、計算能力的に同システムの主力となっている。

2009年には、クアッドコアCPU [SPARC64 VIIを採用した富士通のテクニカルコンピューティングサーバFX](https://ja.wikipedia.org/wiki/SPARC#SPARC64 "wikilink")1を高機能インターコネクトで3392台接続した新システム（理論ピーク性能135TFLOPS）が導入され、[LINPACK](https://ja.wikipedia.org/wiki/LINPACK "wikilink")ベンチマークで110.6[T](../Page/テラ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")（実行効率91.19％）を記録した。これは2008年11月発表の[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")リストで実行効率世界1位、実行性能日本1位、世界ランキング17位に相当する\[5\]\[6\]。

JAXAのスーパーコンピュータシステムはその後、2014年から設置の始まった、JAXAとしては二代目のスーパーコンピュータシステムであるJSS2\[7\]に移行している。JSS2は計算システムの他、大メモリシステム、ファイルシステム、リアルタイム可視化などを支援するプレポストシステム等から成るが、計算システムSORA-MAはPRIMEHPC FX100である。

## 脚注

<references/>

## 関連項目

  - [航空宇宙技術研究所](https://ja.wikipedia.org/wiki/航空宇宙技術研究所 "wikilink")
  - [富士通](../Page/富士通.md "wikilink")
  - [宇宙開発事業団](../Page/宇宙開発事業団.md "wikilink") （NASDA)
  - [宇宙開発](https://ja.wikipedia.org/wiki/宇宙開発 "wikilink")

## 外部リンク

  - [JAXA総合技術研究本部](http://www.iat.jaxa.jp/)
  - [NWT（数値風洞、Numerical Wind Tunnel）](http://museum.ipsj.or.jp/computer/super/0020.html)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:日本のスーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:日本のスーパーコンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:JAXA](https://ja.wikipedia.org/wiki/Category:JAXA "wikilink")

1.  <http://www.roguewave.jp/company/eNews/yomoyama/30.html>
2.  <http://homepage2.nifty.com/Miwa/7_F230-75/7_7.html#7.7%281%29>
3.  <http://homepage2.nifty.com/Miwa/7_F230-75/7_7.html>
4.  <http://stage.tksc.jaxa.jp/jedi/infla/team01.html>
5.  [JAXAの新スパコンが稼働，110.6TFLOPSを実現し「実行効率で世界1位」](http://techon.nikkeibp.co.jp/article/NEWS/20090402/168289)、日本経済新聞、2009年4月2日
6.  [JAXAが新スパコンシステムを公開！富士通の「FX1」を採用](http://www.rbbtoday.com/news/20090404/59088.html)、RBB Today、2009年4月2日
7.  <https://www.jss.jaxa.jp/introjss2/>