> この記事は[Mizar](https://ja.wikipedia.org/wiki/Mizar)から翻訳されています。


自動証明検証システム <strong lang="en">Mizar</strong>（ミザー、ミザール）は、まったく厳密に形式的な形で数学的な[定義](https://ja.wikipedia.org/wiki/定義 "wikilink")や[証明](../Page/証明.md "wikilink")を記述するための[データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")（**-言語**）、実際にその言語で記述された証明の内容を検証することができる[計算機プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")（**証明検証プログラム**）、プログラムから参照して新たな証明の際に利用可能な定義と証明済みの[定理](../Page/定理.md "wikilink")からなる[ライブラリ](../Page/ライブラリ.md "wikilink") (****) の三者から構成される。

と同様の目的を持つプロジェクトに、[ロバート・ボイヤー](https://ja.wikipedia.org/wiki/ロバート・ボイヤー "wikilink")の[QEDプロジェクト](https://ja.wikipedia.org/wiki/QEDプロジェクト "wikilink")がある。

## 概要

システムの開発は1973年に[アンジェイ・トリブレッツ](https://ja.wikipedia.org/wiki/アンジェイ・トリブレッツ "wikilink")によって始められ、システムの保守を[ポーランド](../Page/ポーランド.md "wikilink")の、[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")の[アルバータ大学](https://ja.wikipedia.org/wiki/アルバータ大学 "wikilink")、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[信州大学](https://ja.wikipedia.org/wiki/信州大学 "wikilink")で行っている。

\-言語で記された証明文（以下、-論文）は普通の[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")コードで書かれている。-言語は、数学の通常の言葉遣いと書式がよく似ており、数学者ならば-論文を容易に読むことができる。また、証明を自動的に検証可能とするほど十分に形式化されたものである。-論文における証明の各段階は非常に自明なものである必要があり、そのため同等の内容を持つ通常の数学論文に比べ、長さにおいて4倍程度になると評価された。

の証明検証プログラムは[Pascal](../Page/Pascal.md "wikilink")でかかれ、[古典論理](https://ja.wikipedia.org/wiki/古典論理 "wikilink")を用いた証明を行うもので、非商用目的であれば無料でダウンロード、利用が可能である。これは[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")上の[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")および[Linux](../Page/Linux.md "wikilink")で、あるいは[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") / [Darwinで動く](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")。ソースコードは-ユーザ協会\[1\]のメンバーだけが入手できる。

の配布物には、新たに書かれる -論文で参照可能な種々の定義および定理から成る数学ライブラリが含まれる。レビューと自動検証を受けた新たな論文は、形式化数学ジャーナル\[2\]の関連刊行物で公表することができ、また然る後の一部に組み込まれる。

は[タルスキー・グロタンディーク集合論](https://ja.wikipedia.org/wiki/タルスキー・グロタンディーク集合論 "wikilink")の公理に基づいて構築される。2008年5月現在、8,800の定義と46,000の定理を含む\[3\]。例えば[ハーン・バナッハの定理](https://ja.wikipedia.org/wiki/ハーン・バナッハの定理 "wikilink")、[ケーニヒの補題](https://ja.wikipedia.org/wiki/ケーニヒの補題 "wikilink")、[ブラウワーの不動点定理](https://ja.wikipedia.org/wiki/ブラウワーの不動点定理 "wikilink")、[ゲーデルの完全性定理](../Page/ゲーデルの完全性定理.md "wikilink")、[カントール集合](https://ja.wikipedia.org/wiki/カントール集合 "wikilink")に関するいくつかの事実、などがに含まれる。

の扱う全ての対象は意味論的には集合であるけれども、にも拘らず-言語では統語論的な「型」を定義して使うことが許されている。つまり、ある変数がたとえば[自然数](../Page/自然数.md "wikilink")を表すものならば`Nat`-型を、あるいは[群を表すなら](https://ja.wikipedia.org/wiki/群論 "wikilink")`Group`-型を宣言することができる。このような記法は数学者にとっての記号の捉え方とより近く、-言語をより扱いやすいものにしている。

閲覧可能な-論文の概要は形式化数学ジャーナルのウェブサイト\[4\]から入手できる。また\[5\]は-[検索エンジン](../Page/検索エンジン.md "wikilink")を実装している。

## 注記

<references />

## 外部リンク

  - [Main Mizar site](http://www.mizar.org) - MML、Formalized Mathematics の刊行物へのリンクと、いくつかのシステムの入門書へリンクする参考文献一覧の項
  - [MML Query](http://merak.pb.bialystok.pl) - MMLの検索エンジン
  - [Freek Wiedijk's Mizar site](http://www.cs.kun.nl/~freek/mizar/) - このシステムについて話されたカンファレンスについてのスライドと40ページの入門的な論文
  - [Association of Mizar Users](http://mizar.uwb.edu.pl/sum/)
  - [A paper about Mizar history](http://mizar.org/people/romat/MatRud2005.pdf)
  - [マークンベア](http://markun.cs.shinshu-u.ac.jp/index-j.html)

[Category:形式言語](https://ja.wikipedia.org/wiki/Category:形式言語 "wikilink") [Category:理論計算機科学](https://ja.wikipedia.org/wiki/Category:理論計算機科学 "wikilink") [Category:形式手法](https://ja.wikipedia.org/wiki/Category:形式手法 "wikilink") [Category:大規模な数学的形式化プロジェクト](https://ja.wikipedia.org/wiki/Category:大規模な数学的形式化プロジェクト "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:数学教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:数学教育ソフトウェア "wikilink")

1.  [](http://mizar.uwb.edu.pl/sum/)
2.  [](http://fm.mizar.org/)
3.  最新の統計については\[[http://merak.pb.bialystok.pl\]を見よ](http://merak.pb.bialystok.pl%5Dを見よ)
4.
5.  [](http://merak.pb.bialystok.pl/)