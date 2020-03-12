> この記事は[MBus](https://ja.wikipedia.org/wiki/MBus)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Mbus_mit_modul.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Sun_SuperSPARC_II_SM71_501-3001.jpg "wikilink")

**MBus**は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によって、高速なコンピュータシステムの部品(たとえば、[CPU](../Page/CPU.md "wikilink")や[マザーボード](../Page/マザーボード.md "wikilink")、[メインメモリ](../Page/主記憶装置.md "wikilink"))間通信用[コンピュータバスとして設計](../Page/バス_\(コンピュータ\).md "wikilink")、実装された。対して[SBus](../Page/SBus.md "wikilink")は、同じマシン上にあるマザーボードと[拡張カード](../Page/拡張カード.md "wikilink")を接続するために用いられた。

MBusは、SPARCserver-690のような初期の[SPARC](../Page/SPARC.md "wikilink")をベースとしたマルチプロセッサシステムで最初に用いられ、1980年代後半には、[SPARCstation](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")シリーズのような、SPARCベースのワークステーションにも見られた。MBusはひとつのマザーボード上にいくつものマイクロプロセッサを載せることを許しており、CPUの載った取り外し可能なMBusモジュール(例えばSPARCstation10やSPARCstation20)を使って、8CPUまでのマルチプロセッサ構成をとることができた。シングルプロセッサシステムでも内部的にはMBusプロトコルを使用していたが、生産コストを抑えるため、CPUはマザーボードに直付けされていた。

MBusの仕様は64bitデータ幅で、36bit物理アドレスを使い、アドレス空間は64GBの広さがあった。転送速度は80MB/s(最大転送速度320MB/s)であった。バスの制御は[アービタ](https://ja.wikipedia.org/wiki/アービタ "wikilink")が行い、[割り込みやリセット](../Page/割り込み_\(コンピュータ\).md "wikilink")、タイムアウトも仕様化された。

MBusに関連して、いくつかのバスも開発された。**XBus**は、回路切り替え型MBusに対応したパケット交換型バスであり、MBusと同じ電気的特性と物理形状を持っていたが、信号プロトコルは非互換であった。また、**KBus**は複数のMBusを結ぶための高速な接続システムであって、Solbourne Series 6とSeries 7で使われた。

MBusを使ったコンピュータシステムを生産したメーカーは、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、ROSS Technologies、ヒュンダイ/Axil、[富士通](../Page/富士通.md "wikilink")、Solbourne、Tatung、GCS、Auspex、ITRI、ICL、[クレイ](../Page/クレイ.md "wikilink")、[アムダール](../Page/アムダール.md "wikilink")、テミス、DTKであった。

## 外部リンク

  - [The rough guide to MBus modules, at sunhelp](http://mbus.sunhelp.org/)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")