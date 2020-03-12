> この記事は[SPIN](https://ja.wikipedia.org/wiki/SPIN)から翻訳されています。


**SPINモデルチェッカ**（[英](../Page/英語.md "wikilink"): **SPIN model checker**）は、ソフトウェアの[モデル検査](../Page/モデル検査.md "wikilink")のためのツールである。Gerard J. Holzmann らが開発し、15年以上に渡って改良を続けてきた。[2001年](../Page/2001年.md "wikilink")に[Association for Computing Machinery](../Page/Association_for_Computing_Machinery.md "wikilink") (ACM) の[ソフトウェアシステム賞を受賞している](https://ja.wikipedia.org/wiki/ACMソフトウェアシステム賞 "wikilink")。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")以来、ほぼ毎年[モデル検査](../Page/モデル検査.md "wikilink")に興味のある SPIN ユーザーや研究者による SPIN ワークショップが開催されている。

## 概要

SPIN(Simple Promela INterpreter)は、オートマトンに基づく模型検査器(model checker)。検査対象のシステムは専用の言語[Promela](https://ja.wikipedia.org/wiki/SPINモデルチェッカ#Promela "wikilink") (**Pro**cess **Me**ta **La**nguage) で記述される。Promela は、非同期[分散アルゴリズムを非決定的](../Page/分散コンピューティング.md "wikilink")[オートマトン](../Page/オートマトン.md "wikilink")としてモデル化する。検証される属性は[線形時相論理](../Page/線形時相論理.md "wikilink")の論理式で表される。この論理式の否定形を[Büchiオートマトン](https://ja.wikipedia.org/wiki/Büchiオートマトン "wikilink")に変換して Promela のモデルと合成し、モデル検査アルゴリズムの一部とする。モデル検査の他に、SPIN はシミュレータとしても操作可能であり、システムのとりうる実行経路の1つを実行し、そのトレース結果をユーザーに示す。

多くのモデルチェッカとは異なり、SPIN はモデル検査そのものを実施するわけではなく、その問題に固有のモデルチェッカの[C言語](../Page/C言語.md "wikilink")ソースを生成する。このような若干古い技法を使うことでメモリ使用量を削減し、性能を向上させると共に、モデルにユーザーが自由にCのコードを追加できるという利点がある。SPIN では性能向上やメモリ使用量削減のために以下のような様々なオプションを用意している。

  - [半順序法](https://ja.wikipedia.org/wiki/半順序法 "wikilink")（partial order reduction）
  - 状態[データ圧縮](../Page/データ圧縮.md "wikilink")
  - ビット状態[ハッシング](../Page/ハッシュ関数.md "wikilink")（状態情報全体を格納するのではなく、ハッシュコードを[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")で記憶する。完全性は犠牲になるが、メモリを大幅に削減できる）
  - 弱い公平性の施行（weak fairness enforcement）

GUI として XSpin，JSpin，iSpin が準備されている。

## Promela

その名前(Process Meta Language)が示すように、元来通信プロトコルの検証のために設計された言語である。検査対象であるシステムは非同期並行動作するプロセスの集まりとして記述される。[C言語](../Page/C言語.md "wikilink")に似た文法を持ち、各プロセスの振る舞いを[手続き的に記述する](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")。プロセス間通信、非決定的な振る舞いを明示的に記述する文法要素を備えている。

コード内に[アサーションをおくことができる](../Page/表明.md "wikilink")。線形時相論理で記述される検証項目はモデル全体に関する性質を記述するのに対して、アサーションはそれが置かれた場所で満たすべき条件を記述する。

## 参考文献

  - ジェラード・J.ホルツマン, 水野忠則 (訳) "コンピュータプロトコルの設計法―正しいプロトコルの設計と検証へ導く総合解説書 "カットシステム 1994/11 ISBN 978-4906391103

<!-- end list -->

  - Holzmann, G. J., *The SPIN Model Checker: Primer and Reference Manual*. [Addison-Wesley](../Page/ピアソン_\(企業\).md "wikilink"), [2004年](../Page/2004年.md "wikilink"). ISBN 0-321-22862-6.
  - 中島震, *SPINモデル検査―検証モデリング技法*, 近代科学社, 2008年. ISBN 978-4764903531.
  - Basic Spin Manual – <http://www.asahi-net.or.jp/~hs7m-kwgc/> spin/Man/Manual_japanese.html
  - [産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")システム検証研究センター, 4日で学ぶモデル検査, エヌ・ティー・エス 2006/07 ISBN 978-4860431198

## 外部リンク

  - [SPIN website](http://www.spinroot.com/)

[Category:形式手法](https://ja.wikipedia.org/wiki/Category:形式手法 "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:モデルチェッカ](https://ja.wikipedia.org/wiki/Category:モデルチェッカ "wikilink")