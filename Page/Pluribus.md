> この記事は[Pluribus](https://ja.wikipedia.org/wiki/Pluribus)から翻訳されています。


**Pluribus**は、[BBNテクノロジーズ](../Page/BBNテクノロジーズ.md "wikilink")が[アーパネット](https://ja.wikipedia.org/wiki/アーパネット "wikilink")のパケット交換機として使うために設計した初期の[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")。そのデザインは後の[BBN Butterflyに影響を与えた](../Page/BBN_Butterfly.md "wikilink")。

1972年、アーパネットでの第二世代の[Interface Message Processor](../Page/Interface_Message_Processor.md "wikilink")(IMP)の必要性が明白になり、Pluribusの開発が始まった。当時、BBNは既に35箇所以上のアーパネットのサイトにIMPを設置していた。これらのIMPには[ハネウェル](../Page/ハネウェル.md "wikilink")の 316 または 516 [ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")が使われている。ネットワークの成長は、ノード数、ホスト数、端末数などの面で著しく、それに伴ってトラフィックや地理的な広がりも急速に伸びていた(当時、ヨーロッパとハワイを衛星通信で接続する計画もあった)。

設計目標はモジュール化されたマシンであり、[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")では 316 や 516 よりも小型低価格で、必要に応じて516の最大10倍のバンド幅と最大5倍の入出力デバイスを接続できる能力を実現できるものである。関連して、メモリ[アドレス空間](../Page/アドレス空間.md "wikilink")の拡大と信頼性の向上が重要とされた。

設計者達は[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")方式を採用することにした。そうすることで[モジュール性](https://ja.wikipedia.org/wiki/モジュール性 "wikilink")、コストパフォーマンス、信頼性といった面で有利と考えられ、またIMPのパケット交換アルゴリズムは複数プロセッサで[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")するのに適していたからである。

## Pluribus のハードウェア

Pluribus は2台以上の標準的な19インチの電子機器用ラックで構成される(各ラックには4つのベイがある)。それぞれのベイには[バックプレーン](../Page/バックプレーン.md "wikilink")[バスがあり](../Page/バス_\(コンピュータ\).md "wikilink")、ベイ毎に電源が供給されている。ベイ毎にプロセッサバスの構成されたもの、共有メモリバスの構成されたもの、I/Oバスの構成されたものがある。ベイとベイの間は独自のカプラーで接続し、それによってプロセッサが共有メモリやI/O機器にアクセスできるようにする。

13プロセッサのPluribusをネットワーク交換機として使用して、BBNの5つの[TENEX](../Page/TENEX.md "wikilink")/"Tewnex"[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")を[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")で接続した。Pluribusのプロセッサは、[ロッキード](../Page/ロッキード.md "wikilink")の SUE と呼ばれるものであった。SUE のアーキテクチャはDECの[PDP-11](../Page/PDP-11.md "wikilink")に類似している。

## Pluribus のソフトウェア

Pluribus のソフトウェアは[MIMD](../Page/MIMD.md "wikilink")型の[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")である。[プリエンプション](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")のない[マルチタスク](../Page/マルチタスク.md "wikilink")を採用している。[プロセススケジューリングには](../Page/スケジューリング.md "wikilink") *pseudo-interrupt device*(PID、仮想割り込みデバイス)と呼ばれるハードウェア機構を使用しており、これにプログラムからもI/O機器からもアクセス可能になっていた。各プロセッサでそれぞれのスケジューラが動作し、スケジューラがPIDから整数値を読み取る。その値を使用して次に実行すべきプロセスを選択する。プログラムやデバイスが他のプロセスを動作させたいときは、そのプロセスの番号をPIDに書き込むのである。PIDは全プロセッサに対して要求のあったプロセス番号のうち最も優先度の高いプロセスから先に読み取られるようにしている。

Pluribusのソフトウェアの中でも "STAGE"システムは重要である。STAGEはシステムエラーを検出し、そこから回復させる処理を行う。各プロセッサのクロック[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")には[ウォッチドッグタイマ機能が組み込まれている](https://ja.wikipedia.org/wiki/タイマー#コンピュータ内部のタイマー "wikilink")。あるプロセッサが停止すると別のプロセッサがそれを検出し回復処理を開始する。回復処理では共有[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")にかかっている[ロックを全て外し](../Page/ロック_\(情報工学\).md "wikilink")、確保されていたストレージを解放し、全プロセッサの処理を再開させる。これが可能なのは、アーパネットのルーティングという特殊な処理に特化しているためで、失われたパケットは後で再送されるからである。

## 参考文献

  -
<!-- end list -->

  -
<!-- end list -->

  -
[Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:ネットワークハードウェア](https://ja.wikipedia.org/wiki/Category:ネットワークハードウェア "wikilink")