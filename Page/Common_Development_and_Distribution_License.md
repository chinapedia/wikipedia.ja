> この記事は[Common Development and Distribution License](https://ja.wikipedia.org/wiki/Common_Development_and_Distribution_License)から翻訳されています。


**Common Development and Distribution License**（**CDDL**）は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が [Mozilla Public License](../Page/Mozilla_Public_License.md "wikilink")(MPL) version 1.1 をベースとして策定した[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")向け[ライセンス](../Page/ライセンス.md "wikilink")規定。

## 概要

CDDLでライセンスされたソフトウェアは、使用料が無料であり、無保証で非独占的な利用が可能である。対象ソフトウェアの品質、及び性能に関するリスクは、すべて利用者が負う。また、頒布にあたり、ソフトウェアを実行可能なコード形式で提供する場合は、CDDLに従ってソースコードの提供が義務づけられており、CDDLのコピーを添付しなくてはならない。ソースコードの提供は、ソフトウェア交換に一般的に使われているメディアや妥当な方法でなくてはならない。

CDDLでは、特許による規定が定められており、またソフトウェアを修正、拡張するの開発者（CDDLの元ではコントリビュータと呼ぶ）の規定を明確に定めている。ソフトウェアを修正した場合もCDDLが適用され、自分が修正したコードのコントリビュータであることを明記しなくてはならない。

ただし修正とは異なり、全く別のライセンスのコードを組み合わせて拡大配布物を作成し、それを単一のライセンスとして頒布することも可能としている。組み合わされる別のライセンスのコードは、CDDLが適用されなくても構わないが、CDDLで元々配布されたコードには、CDDLの要件を満たす必要がある。

CDDL は[2004年](../Page/2004年.md "wikilink")[12月1日](../Page/12月1日.md "wikilink")、[Open Source Initiative](../Page/Open_Source_Initiative.md "wikilink") の承認を受けるべく提出され、2005年1月にオープンソースライセンスとして承認された。License Proliferation Committee （非互換なライセンスが数々出現することでオープンソース・コミュニティが分断されるという問題を検討するOSIの委員会）の当初のドラフトでは、CDDLを9つの主要なライセンスの1つとしていた\[1\]。

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が以前に[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")/[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトに使っていたライセンスは [Sun Public License](https://ja.wikipedia.org/wiki/Sun_Public_License "wikilink") (SPL) であり、これも [Mozilla Public License](../Page/Mozilla_Public_License.md "wikilink") をベースとしていた。CDDL はサン内部では SPL version 2 と見なされている。

CDDL でリリースされている製品の例:

  - [OpenSolaris](../Page/OpenSolaris.md "wikilink")（[ZFS](../Page/ZFS.md "wikilink")、[DTrace](../Page/DTrace.md "wikilink") も含む）
  - [NetBeans](../Page/NetBeans.md "wikilink") IDE および RCP
  - [GlassFish](../Page/GlassFish.md "wikilink")
  - [JWSDP](../Page/Java_Web_Services_Development_Pack.md "wikilink")
  - [Project DReaM](https://ja.wikipedia.org/wiki/Project_DReaM "wikilink")

CDDL 提案書第2版は、2005年1月に提出された。このとき、[欧州の著作権法とかみ合わない点が修正され](https://ja.wikipedia.org/wiki/著作権法_\(欧州連合\) "wikilink")、単独の開発者もCDDLを使えるようにした。

## GPLとの非互換性

上記の通り、CDDLでライセンスされた配布物は、修正されたものに関してはCDDLを継承する必需性があるものの、組み合わせた拡大配布物に関しては、CDDLで元々配布していた部分がCDDLを満たしさえすれば、オープンソースかプロプライエタリかに関わらず、他のライセンスのファイルと組み合わせて配布することが可能である\[2\]。これはプロプライエタリなコードを持つ企業が、フリーソフトである部分と、そうでない部分を明確に区別して配布する事ができるように考慮されていると考えることができるが、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")は、このライセンスは [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) とは非互換であるとしている\[3\]。非互換は、MPLから継承したいくつかの複雑な条文に起因している\[4\]。

かつてサンで働いていた Danese Cooper は、CDDL が MPL をベースとしている理由として、MPL が GPL 非互換だからだと述べた。第6回 [Debian](../Page/Debian.md "wikilink") 会議で Cooper は、Solaris カーネルを書いた技術者らが OpenSolaris が GPL 非互換となるよう要求したと述べている。「Mozilla が選ばれた理由のひとつとして、GPL非互換だからというのがある。それは、OpenSolaris リリース時の設計の一部だった。\[...\] Solaris を書いた技術者らは \[...\] どうリリースすべきかという考えがあったのであって、それは尊重されるべきだ」\[5\]

サンの Chief Open Source Officer である Simon Phipps は、当時これについてコメントしなかった。Phipps はCDDL策定当時を知る人物であり、Cooper を「CDDL を実際に書いた人」と紹介している\[6\]。その後 2006年9月になって、Phipps は Cooper の言ったことを否定した\[7\]

[cdrtools](https://ja.wikipedia.org/wiki/:en:cdrtools "wikilink") はかつて全てGPLでライセンスされていたが、一部をCDDLに変更したことから、非互換部分が論争の火種となった。[Debian](../Page/Debian.md "wikilink")プロジェクトは[ビルドシステムがCDDLでライセンスされているため](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")、それが法的に配布不可能になっていると宣言した。すなわち、GPLではソフトウェアをビルドするのに必要な全スクリプトもGPLでライセンスされることを要求しているためである\[8\]。したがってcdrtoolsは[著作権侵害](../Page/著作権侵害.md "wikilink")となるようなライセンス非互換状態になっているとした\[9\]。cdrtoolsのビルドシステムである smake の作者は、それが独立したプロジェクトであり、GPLv3に違反していないと主張している\[10\]。

## 関連項目

  - [GNU Free Documentation License](../Page/GNU_Free_Documentation_License.md "wikilink")
  - [GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink")
  - [GNAT Modified General Public License](../Page/GNAT_Modified_General_Public_License.md "wikilink")
  - [Mozilla Public License](../Page/Mozilla_Public_License.md "wikilink")
  - [BSDライセンス](../Page/BSDライセンス.md "wikilink")
  - [デュアルライセンス](../Page/デュアルライセンス.md "wikilink")

## 脚注

### 注釈

### 出典

## 外部リンク

  -   -
      -
      -
      -
  - \- Open Solaris 公式サイト

  - [The Common Development and Distribution License](https://lwn.net/Articles/114839/) - Linux Weekly News Editorial

  - [さまざまなライセンスとそれらについての解説](https://www.gnu.org/licenses/license-list.ja.html#CDDL) - FSF

  - [OSI承認オープンソースライセンス 日本語参考訳](https://ja.osdn.net/projects/opensource/wiki/licenses%2FCommon_Development_and_Distribution_License) - OSG-JP

[Category:オープンソースライセンス](https://ja.wikipedia.org/wiki/Category:オープンソースライセンス "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.