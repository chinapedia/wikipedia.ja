> この記事は[BBN Butterfly](https://ja.wikipedia.org/wiki/BBN_Butterfly)から翻訳されています。


（BBN バタフライ）は、[BBNテクノロジーズ](../Page/BBNテクノロジーズ.md "wikilink")によって（の設計に基づいて）[1980年代](../Page/1980年代.md "wikilink")に開発された[超並列マシン](../Page/超並列マシン.md "wikilink")。その名称は基盤となるバタフライ式マルチステージ交換ネットワークに由来する。各マシンは最大512個のプロセッサ（[CPU](../Page/CPU.md "wikilink")）で構成され、各プロセッサにローカルメモリが付属し、各プロセッサが他の全プロセッサのローカルメモリにアクセス可能となっている（ただし、そのレイテンシはローカルメモリに比較して15倍）。プロセッサには一般の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を使用した。メモリアドレス空間は共有されている。

第一世代はモトローラの[MC68000](../Page/MC68000.md "wikilink")を使用し\[1\]、その後[MC68010](https://ja.wikipedia.org/wiki/MC68010 "wikilink")版が続いた。バタフライ接続はこのコンピュータのために開発された。第二世代と第三世代の GP-1000 は[MC68020](https://ja.wikipedia.org/wiki/MC68020 "wikilink")を使用し最大256CPUとした。後期の TC-2000 はモトローラの[88100を採用し](https://ja.wikipedia.org/wiki/MC88000 "wikilink")、最大512CPUとしている\[2\]。

元々は、音声や動画を広帯域ネットワーク上で転送するための ST-II プロトコルのルーターとして開発された。バタフライはその後、[国防高等研究計画局](../Page/国防高等研究計画局.md "wikilink")のの後継である高速な衛星広帯域ネットワーク\[3\]のルーターとしても使われた。このネットワークは後に惑星広帯域ネットワーク\[4\]となった。

バタフライ上では当初独自[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")「クリサリス」\[5\]が動作していたが、1989年にオペレーティングシステムに移行した。ハードウェアはだが、理論上[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")として動作する。

実際の最大構成のシステムは、[ローレンス・リバモア研究所](https://ja.wikipedia.org/wiki/ローレンス・リバモア研究所 "wikilink")の123プロセッサ以上を搭載したシステム（フォールトトレラント性のために冗長性を持たせている）である。ほとんどのシステムは16プロセッサ程度の規模だった。[DARPA内にも少なくとも](../Page/国防高等研究計画局.md "wikilink")1システムが納入された。

バタフライ向けに開発された並列プログラム用[デバッガ](../Page/デバッガ.md "wikilink")はプラットフォームより長生きし、他の様々な超並列マシンにも移植された。

## 脚注

## 関連項目

  -
## 外部リンク

  - [](http://www.paralogos.com/DeadSuper/Misc/BBN.html)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")

1.  Rettberg, R„ С Wyman, D. Hunt, M. Hoffman. P. Carvey, B. Hyde. W. Clark, and M. Kraley, August 1979, Development of a Voice Funnel, Bolt Beranek and Newman Inc., Report No. 4098 ,, System: Design Report.
2.
3.
4.
5.