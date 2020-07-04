> この記事は[Valgrind](https://ja.wikipedia.org/wiki/Valgrind)から翻訳されています。


**Valgrind**（ヴァルグリンド、）は、[メモリデバッグや](https://ja.wikipedia.org/wiki/メモリデバッガ "wikilink")、[メモリリーク](../Page/メモリリーク.md "wikilink")の検出、[スレッドエラーの検出](../Page/スレッド_\(コンピュータ\).md "wikilink")、[プロファイリングなどを行うための](../Page/性能解析.md "wikilink")[仮想機械](../Page/仮想機械.md "wikilink")を利用した[ソフトウェア開発ツールである](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。Valgrindという名前は、[北欧神話](../Page/北欧神話.md "wikilink")における[ヴァルハラ](../Page/ヴァルハラ.md "wikilink")への入り口の名に由来している\[1\]。

Valgrindは元々[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")上の[Linux](../Page/Linux.md "wikilink")用のメモリデバッグツールとして設計されたが、開発が進んだ結果、バグ検出やプロファイラといった動的解析ツールのための汎用のフレームワークとなっている。Valgrindは多数のLinux関連のプロジェクトで使用されている\[2\]。Valgrindは[GNU General Public Licenseの元でリリースされている](../Page/GNU_General_Public_License.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 概要

Valgrindは、本質的には[JIT](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")（[バイナリ変換](https://ja.wikipedia.org/wiki/バイナリ変換 "wikilink")）の技術を用いた[仮想機械](../Page/仮想機械.md "wikilink")である。元々のプログラムそのものがホストのプロセッサで直接実行されるわけではない。代わりに、VEXと呼ぶライブラリを使い、Valgrindはまずプログラムを中間表現（IR、Intermediate Representation）に変換する。中間表現自体はプロセッサ非依存であり、[SSAベースである](https://ja.wikipedia.org/wiki/静的単一代入 "wikilink")。変換の後、Valgrindが中間表現をマシンコードに再度変換してホストプロセッサで実行させるが、その前後で「ツール」（下記参照）はIRに対して自由に操作を行うことができる。かなりのパフォーマンスがこれらの変換の過程（およびツールが挿入するコード）で損なわれ、プログラムはValgrind上では（全くツールを使用しない場合でも）通常より4〜5倍低速に動作する。しかし、仮想機械によるIRの形態は計測・解析・デバッグには適している。これによりツールの開発が簡単になり、大半のプロジェクトでは、デバッグ中のこの程度の性能の低下は大きな問題とはならない。

[システムコール](../Page/システムコール.md "wikilink")も、ホストOSのシステムコールを呼び出す前にValgrindで一度ハンドリングされる。[仮想機械](../Page/仮想機械.md "wikilink")として[仮想化](../Page/仮想化.md "wikilink")するのはCPUとメモリのみであり、それ以外のハードウェアはホストOSのものをそのまま使う。

## ツール

Valgrindには、多数のツールが含まれている。また、外部から提供されているものもある。

### Memcheck

最もよく利用されている標準のツールは**Memcheck**である。Memcheckはほぼ全ての命令に特別な[計測用のコードを挿入し](https://ja.wikipedia.org/wiki/:en:instrumentation_\(computer_programming\) "wikilink")、「正当性」（初期化が行われるまでは、割り当て済みでないメモリは全て無効であるか、未定義である）があり、「アドレス可能」(メモリアドレスが割り当て済みで、解放されていないメモリブロックを指している）であるかという情報が、それぞれ*Vビット*および*Aビット*に格納されているかを追跡する。データは移動したり加工されたりするが、計測用のコードは1ビットレベルで正確であるようにA、Vビットを追跡する。他のメモリチェックツール（[IBM Rational Purify](https://ja.wikipedia.org/wiki/:en:IBM_Rational_Purify "wikilink")）などは、対象的に未初期化メモリのコピーの検出のみ行う（ただし、必ずしも問題があるわけではない）。

さらに、Memcheckは標準のCメモリアロケータを独自の実装に置き換え、割り当て済みブロックの前後にメモリガード（無効に設定されたAビットを持っている）を挿入する。この機能により、Memcheckはプログラムが割り当てられたブロックよりわずかに外側の領域を読み書きする[off-by-oneエラー](https://ja.wikipedia.org/wiki/off-by-oneエラー "wikilink")を検出できる（この問題に対する別の対応策として、コンパイラに[境界を持ったポインタを実装し](https://ja.wikipedia.org/wiki/:en:bounded_pointer "wikilink")、特に[ヒープではなく](../Page/動的メモリ確保.md "wikilink")[スタックに確保されたメモリのメモリエラーの検出漏れを低減させる方法があるが](https://ja.wikipedia.org/wiki/コールスタック "wikilink")、計測するバイナリコードを全てリコンパイルする必要がある）。Memcheckが検出や警告可能な問題には下記のものがある。

  - 初期化されていないメモリの使用
  - [`free`](../Page/Malloc.md "wikilink")されたメモリの読み書き
  - [`malloc`](../Page/Malloc.md "wikilink")されたブロックの終端以降への読み書き
  - [メモリリーク](../Page/メモリリーク.md "wikilink")

こうした機能への代償として性能が低下する。Memcheckの元で動作するプログラムはValgrindなしで動作する場合と比べて5倍から20倍遅く、より多くのメモリを使用する（メモリ確保ごとにかなりのメモリを追加で消費する）。したがって、ほとんどの開発者は常にMemcheck（あるいは他のValgrindツール）の元でコードを走らせることはしない。特定のバグを解析したり、（Memcheckが検出可能な種類の）潜在的なバグがないことを検証するために使用するのが最も典型的な方法である。

パフォーマンスのペナルティに加えて、Memcheckの重大な制約事項は、ヒープメモリに対するチェックツールであり、スタック変数・静的変数に対する境界違反を検出することができない点である\[3\]。下記のコードは、コメントに示すようなエラーが存在するにもかかわらずMemcheckでは合格となる。これらの問題を検出するためにSGCheckが開発中である。

``` c
int Static[5];

int main(void) {
    int Stack[5];
    Static[5] = 0;  /* Static[0] から Static[4] が存在し、Static[5] は境界外 */
    Stack [5] = 0;  /*  Stack[0] から  Stack[4] が存在し、Stack[5] は境界外 */
    return 0;
}
```

この種類のエラーが検出できないと、ソフトウェアが[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")を生じた場合、古典的な[スタック破壊の脆弱性攻撃に対して](https://ja.wikipedia.org/wiki/:en:Stack-smashing_protection "wikilink")[セキュリティホール](../Page/セキュリティホール.md "wikilink")になりうるため、注意が必要である。

### その他

Memcheck以外に、Valgrindには下記のツールが標準で同梱されている。

  - Cachegrind：[キャッシュプロファイラ](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")のKCacheGrindを含む。
  - Callgrind：コールグラフ生成。キャッシュとブランチ予測用のプロファイラ。
  - Helgrind：スレッドエラーの検出。マルチスレッドのコードにおける[競合状態](../Page/競合状態.md "wikilink")を検出可能なツール
  - DRD：スレッドエラーの検出
  - Massif：ヒーププロファイラ
  - DHAT：動的ヒープ解析
  - SGCheck：（実験的な）スタック配列とグローバル配列のオーバーラン検出
  - BBV：（実験的な）基本ブロックベクター生成ツール
  - Lackey：ツールのサンプルコード
  - Nulgrind：何もしないツール（ベンチマーク用およびサンプル用）

このツールはバージョン3.2.0の時点で削除された。

  - Addrcheck：Memcheckの軽量版であり、少ないメモリ消費で高速に動作するが、少ないメモリの問題しか検出できない。

## サポートされているプラットフォーム

バージョン3.10.0現在、Valgrindは以下のプラットフォームをサポートしている。

  - [Linux](../Page/Linux.md "wikilink") - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")（32ビット/64ビット）、[PPC32](../Page/PowerPC.md "wikilink")、PPC64、[s390x](../Page/System_z.md "wikilink")、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")32、MIPS64
  - [Android](../Page/Android.md "wikilink") - ARM（2.3以降）、x86（4.0以降）、MIPS32
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - x86、x86-64、（OS X 10.9以降。10.8は限定的なサポートのみ）

その他、[Unix系](../Page/Unix系.md "wikilink")プラットフォームへの非公式な移植版が存在する（[FreeBSD](../Page/FreeBSD.md "wikilink")\[4\]や[NetBSD](../Page/NetBSD.md "wikilink")\[5\]など）。

[Microsoft Windows向けの移植版は現時点では存在しない](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（また、短期的にも公式な計画はない）が、Linux上で動作するWindowsソフトウェアをデバッグするため[Wine](../Page/Wine.md "wikilink")と接続することができる実験的なバージョンが存在する。プラットフォームのサポートを増やすことは長期的な目標であるが、プロジェクトの性質から非常に多くの作業を必要とする。

## 開発者

Valgrindの元々の開発者は、[Julian Sewardであり](https://ja.wikipedia.org/wiki/:en:Julian_Seward "wikilink")、彼は[2006年](../Page/2006年.md "wikilink")にValgrindに関する功績で[Google](../Page/Google.md "wikilink")-[O'Reilly](../Page/オライリーメディア.md "wikilink") [Open Source](../Page/オープンソース.md "wikilink") Awardを受賞した\[6\]\[7\]。他にも多数の開発者も重要な貢献を行っており、Cerion Armour-Brown、Jeremy Fitzhardinge、Tom Hughes、Nicholas Nethercote、Paul Mackerras、Dirk Mueller、Josef Weidendorfer、Robert Walshなどが挙げられる。

## 参考文献

  -
## 脚注

## 外部リンク

  -
  - [Valgrind ドキュメント](http://valgrind.org/docs/manual/index.html)

  - [Valgrind Howto](http://www.faqs.org/docs/Linux-HOWTO/Valgrind-HOWTO.html)（2002年の古いドキュメント）

  - [Projects using Valgrind](http://valgrind.org/gallery/users.html)

[Category:デバッガ](https://ja.wikipedia.org/wiki/Category:デバッガ "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [Valgrind FAQ](http://www.valgrind.org/docs/manual/faq.html#faq.whence)
2.  [valgrind.org's list of users](http://valgrind.org/gallery/users.html)
3.  [Valgrind FAQ](http://www.valgrind.org/docs/manual/faq.html#faq.overruns)
4.  [Valgrind FreeBSD port](http://www.rabson.org/#valgrind)
5.  [Valgrind NetBSD port](http://vg4nbsd.berlios.de/)
6.  [valgrind.org's list of awards](http://valgrind.org/gallery/awards.html)
7.  [Google-O'Reilly Open Source Awards - Hall of Fame](http://code.google.com/events/osa-hall-of-fame.html)