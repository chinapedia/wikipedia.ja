> この記事は[逆F型アンテナ](https://ja.wikipedia.org/wiki/逆F型アンテナ)から翻訳されています。


[Planar_Inverted_F-Shaped_DECT_Antenna.jpg](https://ja.wikipedia.org/wiki/File:Planar_Inverted_F-Shaped_DECT_Antenna.jpg "fig:Planar_Inverted_F-Shaped_DECT_Antenna.jpg")（[コードレス電話](../Page/コードレス電話.md "wikilink")などのデバイスに使用される技術）[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")の逆F型アンテナ\]\]

**逆F型アンテナ**（ぎゃくエフがたアンテナ、**逆Fアンテナ**とも、[英語](../Page/英語.md "wikilink")：inverted-F antenna）は、[無線通信](../Page/無線通信.md "wikilink")で使用される[アンテナ](../Page/アンテナ.md "wikilink")の一種。グランドプレーンに平行で一端が接地されたで構成される。接地された端から離れた中間点から給電される。この設計には単純なモノポールアンテナに比べて2つの利点がある。1つはモノポールアンテナよりも短くコンパクトである点であり、もう1つは[インピーダンス整合](../Page/インピーダンス整合.md "wikilink")が余分な整合部品を必要とせずに設計者が制御できる点である。

最初は1950年代に曲がったワイヤアンテナとして考案された。しかし、最も広く使用されているのはスペースの節約のためにモバイルの無線デバイスに使用される**板状逆F型アンテナ** (planar inverted-F antenna, **PIFA**) である。PIFAは[マイクロストリップ](https://ja.wikipedia.org/wiki/マイクロストリップ "wikilink")の方式を使用して印刷することができる。この技術は広く使用され、他の部品を取り付けるのに用いられる同じ[プリント基板](../Page/プリント基板.md "wikilink")の一部として、プリントした[RF部品を製造することができる](../Page/高周波.md "wikilink")。

PIFAは[パッチアンテナ](https://ja.wikipedia.org/wiki/パッチアンテナ "wikilink")の一種である。広帯域またはマルチバンドのアンテナを実装するために変形したものや他の形態が存在する。技術としては、結合共振器やスロットの追加などがある。

## 発展と歴史

<table>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:File:Inverted-F_antenna_evolution.svg" title="wikilink">逆F型アンテナの発展（英語版Wikipediaの図）</a></p></td>
</tr>
<tr class="even">
<td><p>A: 1/4波長モノポール B: 中間給電1/4波長モノポール<br />
C: 逆L型アンテナ D: 逆F型アンテナ</p></td>
</tr>
</tbody>
</table>

逆F型アンテナは、基本的な1/4波長[モノポールアンテナ](https://ja.wikipedia.org/wiki/モノポールアンテナ "wikilink")を発展させたものである。ワイヤF型アンテナは1940年代に発明された\[1\]。このアンテナでは給電点がベースではなく、アンテナの長さに沿った中間点に接続される。ベースは接地されている。この利点は、アンテナの入力インピーダンスが接地端から給電点への距離に依存することである。給電点とグランドプレーンの間にあるアンテナの部分は、本質的に短絡[スタブとして振る舞う](https://ja.wikipedia.org/wiki/スタブ_\(回路\) "wikilink")。したがって、設計者は給電点の位置を設定することでアンテナをシステムのインピーダンスに整合することができる（RFシステムは一般的にシステムインピーダンスが50 Ωであるのに対し、λ/4モノポールは36.5 Ωである)\[2\]。

逆L型アンテナは、モノポールアンテナを曲げ、グランドプレーンと平行にしている。これはλ/4モノポールよりもコンパクトで短いという利点があるが、インピーダンスが非常に低く一般的には数Ω程度である欠点がある。逆F型アンテナは、逆L型アンテナのコンパクト性とF型アンテナのインピーダンス整合性という両方の利点を兼ね備えている\[3\]\[4\]。

逆F型アンテナは1958年に[Ronold W. P. King率いる](https://ja.wikipedia.org/wiki/:en:Ronold_W._P._King "wikilink")[ハーバード大学](https://ja.wikipedia.org/wiki/ハーバード大学 "wikilink")のグループにより最初に提案された\[5\]。Kingのアンテナはワイヤ状であり、[テレメトリ用のミサイルでの使用を目的としていた](../Page/遠隔測定法.md "wikilink")\[6\]\[7\]。

## 平面への実装

<table>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/:en:File:PIFA_antennae.png" title="wikilink">PIFAアンテナ（英語版Wikipediaの図）</a></p></td>
</tr>
<tr class="even">
<td><p>A: プリント逆F型アンテナ B: 蛇行プリント逆F型アンテナ<br />
C: パッチアンテナ: D: 板状逆F型アンテナ(PIFA)</p></td>
</tr>
</tbody>
</table>

板状逆F型アンテナ (PIFA) は、[マイクロストリップ](https://ja.wikipedia.org/wiki/マイクロストリップ "wikilink")で実装された無線回路に使用される。マイクロストリップの方式は現代的な[RF電子工学に適した方式である](../Page/高周波.md "wikilink")。これは、フィルタなどの必要な分布要素RF部品を実装するために使用することができ、[プリント基板](../Page/プリント基板.md "wikilink")と同じ量産方式を採用しているため経済的である。

プリントした逆F型アンテナは古典的な逆F型の形状で実装することができ、通常はアンテナの下から[グランドプレーンが取り除かれた回路基板の片側に実装される](../Page/グランドプレーンアンテナ.md "wikilink")。しかし、別のアプローチとして変形した[パッチアンテナ](https://ja.wikipedia.org/wiki/パッチアンテナ "wikilink")である短パッチアンテナ(shorted patch antenna)がある。このアプローチでは、パッチの一端もしくは中間点を接地ピンもしくはビアで接地し、グランドプレーンに通す。これは逆F型と同じ原理で動作する。横から見るとF型を見ることができるが、アンテナ素子が水平面内で非常に広いということだけである\[8\]。短パッチアンテナは、放射面積が大きいため、細線型よりも広い帯域幅を持っている\[9\]。細線型と同様に、他の回路と同じ[プリント基板](../Page/プリント基板.md "wikilink")にプリントすることができる。ただし、それらは通常独自の基板、またはメインの基板に固定された[誘電体](../Page/誘電体.md "wikilink")に印刷される。これによりアンテナが浮き効果的に空気誘電体の中にあり、グランドプレーンからの距離が長くなるか、使用する誘電体がRF性能により適した材料になる\[10\]。

*PIFA*という単語は、アンテナ素子が幅広でグランドプレーンが下にある短パッチアンテナに対しては、多くの著者（例えばSánchez-Hernández\[11\]）が使用を控えている。図のAとBのようにグランドプレーンが片側にある細線型の逆F型アンテナは、平面の方式であっても*IFA*と呼ばれる。この種のIFAをプリント逆F型アンテナ(printed inverted-F antenna)と呼ぶこともできるが、それでも短パッチアンテナに対して*PIFA*を使用するのは控えられる（例えばHall and Wang\[12\]）。

短パッチアンテナの一般的な構成は、給電ピンを短絡ピンの比較的知覚にして、短絡ピンをできるだけ1つの隅の近くに配置することである。この構成では[共振周波数](https://ja.wikipedia.org/wiki/共振周波数 "wikilink")はおおよそ次のようになる。

\[f_0 = \frac {c} {4 (w + b) \sqrt \varepsilon_\mathrm r}\]

  -
    ここで
    *f*<sub>0</sub>は共振周波数
    *w*, *b*はパッチの幅
    *c*は光速
    ε<sub>r</sub>は基板の[比誘電率](../Page/比誘電率.md "wikilink")

この式は、アンテナがデバイスの筐体など近くの誘電体の影響を受けない場合にのみ当てはまる\[13\]\[14\]。

他に見られる変形は蛇行逆F型アンテナ(meandered inverted-F antenna, MIFA)がある。アンテナを必要な全長まで延ばすのに十分な基盤のスペースがない場合、アンテナは蛇行して設計された電気長を維持したまま高さを低くすることができる\[15\]。これはrubber duckyアンテナに見られるようなアンテナの螺旋と比較できる\[16\]。

逆F型アンテナの帯域幅は狭い。アンテナを長くすることで広い帯域幅が達成でき、放射抵抗が増加する。別の解決策は2つのアンテナを近接して配置することである。[結合共振器](https://ja.wikipedia.org/wiki/結合共振器 "wikilink")の帯域幅がいずれの共振器の帯域幅よりも広いため帯域幅が広くなる。マルチバンドアンテナを作成するための技術のほとんどは、帯域幅を広げるのにも効果的である\[17\]。

## マルチバンドアンテナ

[Double_F_antenna.png](https://ja.wikipedia.org/wiki/File:Double_F_antenna.png "fig:Double_F_antenna.png")用途からのデュアルバンド逆F型アンテナは、2.4GHzと5.2GHz帯域で[ネットワークインタフェースコントローラを提供する](../Page/ネットワークカード.md "wikilink")\[18\]\[19\]。\]\] マルチバンドアンテナの必要性は、使用する周波数帯が異なることが多い国やネットワーク間をローミングする必要があるモバイル機器で生じる。1997年に最初に報告されたおそらく最も概念的に単純な設計は\[20\]、2つのPIFAパッチアンテナのうち1つをもう1つの内側に入れ子にするものである。また、1本以上の引き込み線をパッチに挿入することで、結合共振器の効果で帯域を広げることができる。他の方法は複数のモードが生成されることに依存し、よりコンパクトな設計が可能になる。この例としては、それぞれ図のCとDに示すインターディジタルフィルタに似たパターンであるCスロットパターンや、強蛇行パターン(tightly meandered pattern)がある\[21\]。 [Multi-band_PIFAs.png](https://ja.wikipedia.org/wiki/File:Multi-band_PIFAs.png "fig:Multi-band_PIFAs.png")

## 用途

逆F型アンテナは、スペースが限られているコンパクトで手で持てる大きさの無線デバイスで広く使用されている。これには[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")、[Bluetooth](../Page/Bluetooth.md "wikilink")、[Wi-Fi](../Page/Wi-Fi.md "wikilink")などの無線伝送を使用する[携帯電話](../Page/携帯電話.md "wikilink")や[タブレットコンピュータが含まれる](../Page/タブレット_\(コンピュータ\).md "wikilink")\[22\]。板状逆F型アンテナは、携帯電話の設計で最もよく使用される内部アンテナである\[23\]。

これらのアンテナは車両の[テレマティクス](../Page/テレマティクス.md "wikilink")にも使用される。車両メーカーはスタイルと空力の理由から、車両の輪郭に沿ったアンテナを使用することを好む。マルチバンドPIFAを使用して、携帯電話、[衛星測位システム](../Page/衛星測位システム.md "wikilink")、[カーラジオ](https://ja.wikipedia.org/wiki/カーラジオ "wikilink")のアンテナ給電を組み合わせることができる\[24\]。

これらのアンテナは規格をサポートするアンテナを含む、軍事試験範囲でのテレメトリの用途で使用される\[25\]。

R形デュアルバンドPIFAは、軍用車両での使用が提案されている。対象となる帯域は、225 MHzと450 MHzである。これらの周波数は900 MHzと1.8 GHzである携帯電話のGSM帯域と同じ比率であるため、その設計がこの用途にも使用でき、寸法が縮小される場合も同様である\[26\]。

## 出典

## 関連文献

  - Ali, M.; Guangli Yang; Huan-Sheng Hwang; Sittironnarit, T., ["Design and analysis of an R-shaped dual-band planar inverted-F antenna for vehicular applications"](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=1262127), *IEEE Transactions on Vehicular Technology*, vol. 53, iss. 1, pp. 29–37, January 2004.
  - Barton, ["Nosecone Inverted-F (IFA) for S-Band Telemetry"](https://apps.dtic.mil/docs/citations/AD1039216), DTIC, 2017
  - Cohen, N., [Fractal antenna applications in wireless telecommunications"](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=605374), *Professional Program Proceedings: Electronics Forum of New England, 1997*, pp. 43–49, 6–8 May 1997, IEEE .
  - Hall, Peter S.; Lee, E.; Song, C. T. P., "Planar inverted-F antennas", pp. 197–227, in Waterhouse, Rod (ed), *Printed Antennas for Wireless Communications*, John Wiley & Sons, 2008 .
  - Hall, Peter S.; Yang Hao, *Antennas and Propagation for Body-Centric Wireless Communications*, 2nd ed., Artech House, 2012 .
  - Kervel, Fredrik, [*868 MHz, 915 MHz and 955 MHz inverted F Antenna*](http://www.ti.com/lit/an/swra228c/swra228c.pdf), Texas Instruments, Design Note DN023 30 September 2011.
  - Kin-Lu Wong, Yen-Yu Chen, Saou-Wen Su, Yen-Liang Kuo, ["Diversity dual-band planar inverted-F antenna for WLAN operation"](http://onlinelibrary.wiley.com/doi/10.1002/mop.11020/abstract), *Microwave and Optical Technology Letters*, vol. 38, iss. 3, pp. 223–225, 5 August 2003.
  - King, Ronold W. P.; Harrison, C. W., Jr.; Denton, D. H., Jr., "Transmission-line missile antennas", Sandia Corp Technical Memo 436-58, vol. 14, November 1958.
  - King, Ronold W. P.; Harrison, C. W., Jr.; Denton, D. H., Jr., ["Transmission-line missile antennas"](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=1144802), *IRE Transactions on Antennas and Propagation*, vol. 8, iss. 1, pp. 88–90, January 1960.
  - Liu, Z. D.; Hall, P. S.; Wake, D., ["Dual frequency planar inverted F antenna"](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=633849), *IEEE Transactions on Antennas and Propagation*, vol. 45, iss. 10, pp. 1451–1458, October 1997.
  - Petosa, Aldo, *Frequency-Agile Antennas for Wireless Communications*, Artech House, 2013 .
  - Prasad, Shiela; King, Ronold W. P., ["Experimental study of inverted L-, T-, and related transmission-line antennas"](http://nvlpubs.nist.gov/nistpubs/jres/65d/jresv65dn5p449_a1b.pdf), *Journal of Research of the National Bureau of Standards*, vol. 65, no. 5, pp. 449–454, September–October 1961.
  - Sánchez-Hernández, David A., *Multiband Integrated Antennas for 4G Terminals*, Artech House, 2008 .
  - Waterhouse, Rod; Novak, Dalma, "Wireless systems and printed antennas", pp. 1–36, in Waterhouse, Rod (ed), *Printed Antennas for Wireless Communications*, John Wiley & Sons, 2008 .
  - Yarman, Binboga Siddik, *Design of Ultra Wideband Antenna Matching Networks*, Springer, 2008 .

[Category:アンテナ](https://ja.wikipedia.org/wiki/Category:アンテナ "wikilink") [Category:マイクロ波](https://ja.wikipedia.org/wiki/Category:マイクロ波 "wikilink")

1.  Waterhouse & Novak, p. 19
2.  Hall *et al.*, pp. 197–198
3.  Hall *et al.*, pp. 197–198
4.  Yarman, p. 67
5.  King, Harrison & Denton, 1958, 1960)
6.  Petosa, p. 62
7.  Prasad & King, pp. 449, 452
8.  Hall *et al.*, pp. 198–199
9.  Yarman, p. 68
10. Hall *et al.*, pp. 200, 209
11. Sánchez-Hernández, pp. 16–22
12. Hall & Wang, p. 96
13. Hall *et al.*, pp. 199–200
14. Yarman, pp. 68–69
15. Kervel, pp. 1, 3–4
16. Cohen, p. 43: "Viewing the rubber duck as a 3-D meander line using a helix, it's easy to see that other attempts at miniaturization are possible".
17. Hall *et al.*, p. 200
18. Hall *et al.*, pp. 221–222
19. Kin-Lu *et al.*, pp. 223–225
20. Liu *et al.*, p. 1451
21. Hall *et al.*, pp. 203–204
22. Hall *et al.*, p. 197
23. Yarman, p. 67
24. Hall *et al.*, p. 222
25. Barton, 2017
26. Ali *et al.*, p. 29