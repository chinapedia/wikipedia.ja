> この記事は[Software Package Data Exchange](https://ja.wikipedia.org/wiki/Software_Package_Data_Exchange)から翻訳されています。


**Software Package Data Exchange（SPDX**）\[1\]は、特定の[コンピュータソフトウェアが配布される](../Page/ソフトウェア.md "wikilink")[ソフトウェアライセンス](../Page/ソフトウェアライセンス.md "wikilink")に関する情報を文書化するために使用される[ファイル形式である](../Page/ファイルフォーマット.md "wikilink")。SPDXは、[Linux Foundationの後援のもと](../Page/Linux_Foundation.md "wikilink")、20以上の組織を代表するSPDXワーキンググループによって作成されている\[2\]。

SPDXは、組織がソフトウェアライセンスや[Bills of material](../Page/BOM_\(部品表\).md "wikilink")（BOM、部品表）に関する[メタデータ](../Page/メタデータ.md "wikilink")を公開する方法を標準化することを試みている\[3\]。

SPDXは、ソフトウェアがライセンスされる正確な条件を定義している。また、ライセンスをタイプ別に分類しようとはしておらず、たとえば、[BSDライセンス](../Page/BSDライセンス.md "wikilink")と同様の用語を使用したライセンスを「BSD-like」として説明したりはしない\[4\]。

この規格の現在のバージョンは2.1で、2016年11月に承認されている\[5\]。

## ライセンスの構文

各ライセンスは、「Mozilla Public License 2.0」などの完全な名前と、それに対する「MPL-2.0」などの短い識別子で識別される。ライセンスは、演算子`AND`と`OR`、およびグループ化`(`と`)`を組み合わせて表現することができる。

たとえば、`(Apache-2.0 OR MIT)`は、`Apache-2.0`（[Apache License](../Page/Apache_License.md "wikilink")）または`MIT`（[MITライセンス](../Page/MIT_License.md "wikilink")）から選択できることを意味する。一方、`(Apache-2.0 AND MIT)`は、両方のライセンスが適用されることを意味する。

「+」演算子もあり、これをライセンスに適用すると、同じライセンスの将来のバージョンも適用されることを意味する。たとえば、`Apache-1.1+`は、`Apache-1.1`および`Apache-2.0`（および将来のバージョン）が適用されることを意味する。

ライセンスのGNUファミリ（たとえば、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") 2.0）には、組み込みのライセンスの新しいバージョンを選択することもできる。これは、SPDXでの表現`GPL-2.0`が「厳密にGPLバージョン2.0」を意味するのか、「GPLバージョン2.0またはそれ以降のバージョン」を意味するのかが明確でない場合があったためである\[6\]。そのため、SPDXライセンスリストのバージョン3.0以降、ライセンスのGNUファミリには新しい名前が付けられている\[7\]。`GPL-2.0-only`は「正確にバージョン2.0のみ」を意味し、`GPL-2.0-or-later`は「GPLバージョン2.0以降のバージョン」を意味する。

2020年に、欧州委員会は、50を超えるライセンスの選択と比較を可能にする、Joinup Licensing Assistant発行し\[8\]、SPDX識別子と全文にアクセスできるようにしている。

## 関連項目

  - [ライセンスの氾濫](https://ja.wikipedia.org/wiki/ライセンスの氾濫 "wikilink")

## 参考文献

## 外部リンク

  -
  - [Linux Foundationオープンコンプライアンスプログラム](https://compliance.linuxfoundation.org/)

  - Nathan Willis: [A SPDX case study](https://lwn.net/Articles/568286/) LWN.net

[Category:フリーソフトウェアのプロジェクト](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアのプロジェクト "wikilink") [Category:標準](https://ja.wikipedia.org/wiki/Category:標準 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.