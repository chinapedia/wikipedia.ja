> この記事は[Linux-VServer](https://ja.wikipedia.org/wiki/Linux-VServer)から翻訳されています。


**Linux-VServer** は、[Linux](../Page/Linuxカーネル.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")に[OSレベルの仮想化](https://ja.wikipedia.org/wiki/OSレベルの仮想化 "wikilink")機能を追加することで実装された[バーチャル・プライベート・サーバ](https://ja.wikipedia.org/wiki/バーチャル・プライベート・サーバ "wikilink")。[オープンソース](../Page/オープンソース.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")として開発・配布されており、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) でライセンスされている。

## 概要

プロジェクトの創始者は Jacques Gélinas。現在は[オーストラリア](../Page/オーストラリア.md "wikilink")の Herbert Pötzl が保守しており、[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")の実装を行っている [Linux Virtual Server](../Page/Linux_Virtual_Server.md "wikilink") プロジェクトとは無関係である。

Linux-VServer は[jail](https://ja.wikipedia.org/wiki/jail "wikilink")機構であり、コンピュータシステムの各種[リソース](../Page/計算資源.md "wikilink")（[ファイルシステム](../Page/ファイルシステム.md "wikilink")、CPU時間、ネットワークアドレス、メモリなど）をセキュアに分割でき、[プロセス](../Page/プロセス.md "wikilink")は自身の存在するパーティション以外に対して[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")の影響を与えることができない。

各パーティションを「セキュリティコンテキスト」と呼び、その中で動作する[仮想化](../Page/仮想化.md "wikilink")されたシステムを「バーチャル・プライベート・サーバ」と呼ぶ。セキュリティコンテキストに下降するための [chroot](https://ja.wikipedia.org/wiki/chroot "wikilink") のようなユーティリティが用意されている。バーチャル・プライベート・サーバの[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")は、単に新しいセキュリティコンテキスト内で [init](https://ja.wikipedia.org/wiki/init "wikilink") を起動すればよい。同様にシャットダウンするには、そのセキュリティコンテキスト内の全プロセスを停止すればよい。各コンテキストで[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")を修正なしでブート可能であり、[Debian](../Page/Debian.md "wikilink") や [Fedora Core](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink") を並行動作させることができる。

バーチャル・プライベート・サーバは一般に[Webホスティングサービスに利用され](../Page/ホスティングサーバ.md "wikilink")、顧客アカウントの分離、リソースのプーリング、潜在的セキュリティ違反の封じ込めなどに有効である。インストールにあたって領域を節約するため、各バーチャル・サーバのファイルシステムは「テンプレート」ファイルシステムの[コピーオンライト](https://ja.wikipedia.org/wiki/コピーオンライト "wikilink")型[ハードリンク](https://ja.wikipedia.org/wiki/ハードリンク "wikilink")のツリーとして構築される。そのハードリンクはファイルシステムの特殊な属性付きであり、書き込み時にセキュアかつ透過的にファイルの実際のコピーに置換される。

## 同様の仮想化機構

[OSレベルの仮想化](https://ja.wikipedia.org/wiki/OSレベルの仮想化 "wikilink")技術の他の実装としては、[OpenVZ](../Page/OpenVZ.md "wikilink")、[Parallels Virtuozzo Containers](https://ja.wikipedia.org/wiki/Virtuozzo "wikilink")、[FreeBSD jail](../Page/FreeBSD_jail.md "wikilink") 機構、[Solaris Containers](https://ja.wikipedia.org/wiki/Solaris_Containers "wikilink")、[FreeVPS](https://ja.wikipedia.org/wiki/FreeVPS "wikilink")（Linux-VServer から初期に[フォーク](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")）などがある。

## 利点

  - バーチャル・サーバ間で[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")インタフェースは共通であり、[エミュレータ](../Page/エミュレータ.md "wikilink")のオーバーヘッドは生じない。
  - 各バーチャル・サーバに[ディスクイメージ](https://ja.wikipedia.org/wiki/ディスクイメージ "wikilink")を持つ必要はなく、ファイルシステムを共有できる（ただし、コピーオンライト型ハードリンク経由）。これにより、システムのバックアップが容易になり、バーチャル・サーバ間でディスク空き領域をプールできる。
  - バーチャル・サーバ内のプロセスは、ホストシステムの通常のプロセスと同じである。システム全体をエミュレートする仮想化よりもメモリやI/Oが効率化される。
  - バーチャル・サーバ内のプロセスは、ホストシステムのスケジューラで[スケジューリング](../Page/スケジューリング.md "wikilink")され、どのプロセスも[SMPシステム上で並行動作可能である](../Page/対称型マルチプロセッシング.md "wikilink")。システム全体のエミュレーションでは必ずしも簡単ではない。
  - ネットワークは仮想化というよりも分離されているだけであり、パケット送受信に余分なオーバーヘッドが生じない。

## 欠点

  - ホストカーネルにパッチをあてる必要がある。
  - 全バーチャル・サーバが同じカーネルを共有するため、バグやセキュリティホールも共有する可能性がある。
  - [クラスタリングや](../Page/コンピュータ・クラスター.md "wikilink")[プロセスマイグレーション](https://ja.wikipedia.org/wiki/プロセスマイグレーション "wikilink")機能がない。ホストカーネルおよびそのハードウェアで障害が発生すると、全バーチャル・サーバがダウンする危険性がある。
  - ネットワークは仮想化ではなく分離されているだけである。このため、バーチャル・サーバが独自にルーティング設定したり、ファイアーウォールを設定したりできない。
  - 一部のシステムコール（特にハードウェア関連、例えば[リアルタイムクロック](https://ja.wikipedia.org/wiki/リアルタイムクロック "wikilink")関連）、[/proc](https://ja.wikipedia.org/wiki/Procfs "wikilink") や [/sys](https://ja.wikipedia.org/wiki/Sysfs "wikilink") ファイルシステムの一部は仮想化されていない。
  - ディスクI/Oの帯域幅をバーチャル・サーバ毎に割り当てることができない。

## 外部リンク

  - [プロジェクトのホームページ](http://linux-vserver.org)
  - [公式リリース](http://www.13thfloor.at/vserver/project/)
  - [Implementation paper](http://linux-vserver.org/Linux-VServer-Paper)

[Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")