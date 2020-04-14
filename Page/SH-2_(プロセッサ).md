> この記事は[SH-2 \(プロセッサ\)](https://ja.wikipedia.org/wiki/SH-2_\(プロセッサ\))から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:HD6417095_01.jpg "wikilink") **SH-2**は、[日立製作所](../Page/日立製作所.md "wikilink")（現[ルネサス エレクトロニクス](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink")）が開発した[32ビット](../Page/32ビット.md "wikilink")[RISC](../Page/RISC.md "wikilink") [CPU](../Page/CPU.md "wikilink")。[SuperH](../Page/SuperH.md "wikilink")（スーパー日立）シリーズの一つ。1994年6月に量産開始。

## 概要

SH-2は元々、組み込み用32ビット RISC[プロセッサ](../Page/プロセッサ.md "wikilink")であるSHシリーズ（SH-1）を、当時[セガ](https://ja.wikipedia.org/wiki/セガ "wikilink")が開発していた32ビット[ゲーム機](../Page/ゲーム機.md "wikilink")[セガサターン](../Page/セガサターン.md "wikilink")への搭載を念頭に改修した製品である。

SuperH RISC engine（SHシリーズ）は、当時の組み込み向け32ビットプロセッサと比較して、命令長を[16ビット](../Page/16ビット.md "wikilink")に縮小するなどメモリ効率を向上させた、高速かつ高機能なプロセッサであったが、採用用途が限られ知名度と実績はいまひとつであった。また、当時日立の研究所で開発中であった情報端末で採用したいとの要望が社内であり、当時としては実験的な意味合いが強かったが[マルチプロセッサ機能も組み込まれていた](../Page/マルチプロセッシング.md "wikilink")。

SH-2の量産に入る直前の1993年夏になって、競合ゲーム機\[1\]の3D[ポリゴン](../Page/ポリゴン.md "wikilink")性能を知ったセガから大幅な性能向上の要望が出された。日立はこのマルチプロセッサ機能を活用することでその要望に答えることとした。CPUの[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")値においても当時ライバルゲーム機の『[3DO](../Page/3DO.md "wikilink")』が採用していた[ARM60や](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#ARM6 "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[i960](../Page/Intel_i960.md "wikilink")、[NEC HE](../Page/日本電気ホームエレクトロニクス.md "wikilink")『[PC-FX](../Page/PC-FX.md "wikilink")』や[任天堂](../Page/任天堂.md "wikilink")『[バーチャルボーイ](../Page/バーチャルボーイ.md "wikilink")』などに採用された[NECの](../Page/日本電気.md "wikilink")[V810が](https://ja.wikipedia.org/wiki/NEC_Vシリーズ#V810.E7.B3.BB "wikilink")10 - 15MIPSであったため、セガも当初は10 - 20MIPS程度の数値的目標を予定していた。しかしSH-2はそれらを大きく上回る25MIPSであった事から\[2\]、セガサターンにはSH-2の採用が見送られるどころか2個搭載されることとなり、SHシリーズの知名度は大きく向上した。

また、[メガドライブ](../Page/メガドライブ.md "wikilink")の周辺機器である[スーパー32X](../Page/スーパー32X.md "wikilink")にも20[MHz仕様のSH](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")-2が2個搭載されただけでなく、セガサターンには[CD-ROM](../Page/CD-ROM.md "wikilink")ドライブの制御用チップとしてSH-1も一緒に搭載されたため、それまで月数千個だったSHシリーズの出荷数はセガサターン用だけで2,000万個近くに上り、一気に世界第2位のRISC型組み込みCPUに躍り出た。

設計コストの償却を早々に終えたことから価格を低下させ、その後[DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink")[インタフェースや入出力インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、周辺インタフェースの内蔵ラインナップを増加させることにより、組み込み用国産プロセッサの定番チップとしてシェアを確保することに成功している。大口顧客として当初は利益率の低かったセガサターン向けSH-2も、微細化や2個のSH-2を1チップにしたものなどの投入で改善させた。

後に高[クロック](../Page/クロック.md "wikilink")・高機能化したSH-3を経て、より高速なSH-4が登場し、これもセガの後継ゲーム機[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")に搭載された。その後、セガはコンシューマ市場へのハードウェア供給から撤退することになったため、SHシリーズもSH-5を最後に高クロック化を一時中断し、[携帯電話](../Page/携帯電話.md "wikilink")向けのシリーズにシフトしていった。

## 主な仕様

  - 汎用レジスタ ： 32ビット長16本
  - メモリバス ： 32ビット
  - 命令 ： 命令長16ビット、61命令
  - Dhrystone MIPS ： 25MIPS（28.5MHz時）
  - キャッシュ ： 4Kbytes、命令/データ混在、4-way set associative、Write-Thru、LRU、ラインサイズ16byte
  - インターフェイス ： Synchronous DRAMインターフェイス、DMAコントローラ×2、シリアルインタフェース、タイマなど
  - パッケージ ： 144ピンQuad Flat Package
  - トランジスタ数 ： 450,000個
  - 電源電圧 ： 3Vから5.5V
  - チップサイズ ： 9.52mm×8.66mm
  - プロセス ： 0.8μ2層アルミCMOS

## 応用製品

  - SHシリーズは本来組み込み向けであり、情報家電やカーナビゲーションシステムなどに搭載されている。
  - SH-2はSuperH RISC engineの中でも一番ラインナップが多く、アーケードゲーム基板をはじめ自動車のエンジン制御分野などでも採用され、各種制御機器、通信機器への採用例が多い。現在はSH-2Aなど高速版も発売されている。
  - SH-DSPは、HDD制御やHDD/DVDレコーダ制御などでも採用されている。

## 注釈

## 脚注

<references/>

## 関連項目

  - [SuperH](../Page/SuperH.md "wikilink")
  - [スーパー32X](../Page/スーパー32X.md "wikilink")
  - [セガサターン](../Page/セガサターン.md "wikilink")
  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink")
  - [ポリゴン](../Page/ポリゴン.md "wikilink")
  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")

## 外部リンク

  - [日経エレクトロニクス 1997年9月22日号開発ストーリ「SHマイコン開発-最終回](http://japan.renesas.com/products/mpumcu/superh/related_sh/theme/story/06.jsp) - ルネサスによる開発の裏話

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:日立製作所](https://ja.wikipedia.org/wiki/Category:日立製作所 "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink")

1.  この時点では[PlayStationではなく](../Page/PlayStation_\(ゲーム機\).md "wikilink")[NINTENDO64](../Page/NINTENDO64.md "wikilink")を指す。
2.  [ASCII](../Page/ASCII.md "wikilink")『月刊アスキー』1995年1月号 p.433 セガ・エンタープライゼスCSハードウェア研究開発部ゼネラル・マネージャー浜田和彦氏インタビュー 参照