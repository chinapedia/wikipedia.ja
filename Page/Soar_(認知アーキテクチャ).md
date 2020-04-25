> この記事は[Soar \(認知アーキテクチャ\)](https://ja.wikipedia.org/wiki/Soar_\(認知アーキテクチャ\))から翻訳されています。


**Soar**(**SOAR**)とは、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の John Laird、[アレン・ニューウェル](../Page/アレン・ニューウェル.md "wikilink")、Paul Rosenbloom が作成した[認知アーキテクチャ](../Page/認知アーキテクチャ.md "wikilink")の一種。[認識](../Page/認識.md "wikilink")とは何かという観点と、それに基づいた[人工知能](../Page/人工知能.md "wikilink")用の[プログラムアーキテクチャの観点から構成される](../Page/プログラム_\(コンピュータ\).md "wikilink")。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に最初に作成され、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に論文として発表されて以来、多くの人工知能研究者が人間の行動の様々な観点の[認知モデル](https://ja.wikipedia.org/wiki/認知モデル "wikilink")を作成するのに Soar を用いている。

Soar プロジェクトの主な目的は、高度なルーチン処理から非常に難しい開放型問題を解くことまで可能な[知的エージェント](../Page/知的エージェント.md "wikilink")の能力を完全に扱うことができるようにすることである。そのため、Soar では[知識表現](../Page/知識表現.md "wikilink")を生成し、適切な形式の知識（[手続き的知識](../Page/手続き的知識.md "wikilink")、[宣言的知識](../Page/宣言的知識.md "wikilink")、[エピソード的知識](../Page/エピソード記憶.md "wikilink")、さらには象徴的知識）を扱えなければならない。さらに Soar プロジェクトは[精神](../Page/精神.md "wikilink")の仕組みを集積しようとしている。また、Soar を支えるアーキテクチャには[知能](../Page/知能.md "wikilink")を支えるのに十分な記号システムが必要である。 Soar の根底にある認識に関する見方は[アレン・ニューウェル](../Page/アレン・ニューウェル.md "wikilink")の著書 *Unified Theories of Cognition* で述べられている心理学的理論に基づいている。

Soar の最終目標は真の人工知能を生み出すことであるが、今のところそれが達成された様子はない。Soar 支持者は、このシステムが知能の何か重要な部分で間違っていると認めている。現在、Soar にエピソード記憶と意味論的記憶を追加するプロジェクトが進行中であり、他にも感情を与えるプロジェクトも進行中である。他に足りない機能として、階層的クラスタリングなどを通して自身の新たな表現を自動生成する能力などが考えられている。

Soar は[プロダクションシステム](../Page/プロダクションシステム.md "wikilink")に基づいている。すなわち、明示的なプロダクションルール（生成規則）によって振る舞いを制御する（[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")の 「もし…ならば、…」という規則と類似）。問題解決を大まかに説明すると、「問題空間」（システムがある時間内にとりうる状態の集合）を検索し「ゴール状態」（問題の解決した状態）を見つけ出すのである。システムは徐々にゴールに近い状態を取るよう検索していく。状態から状態への移動は、推敲フェーズ（問題に関連する様々な知識の断片を Soar の[ワーキングメモリ](../Page/ワーキングメモリ.md "wikilink")に持ってくる）と決定手順（前のフェーズで見つかったものを考慮し、最終的に次の行動を決定する）から構成される決定サイクルでなされる。

この決定手順が唯一の行動指針を決定できない場合、Soar は他の戦略を試みる。それらは *weak methods* と呼ばれ、袋小路となった状態からの脱出に使われる。このような手法は知識が豊富でない場合には適切である。例えば、[手段目標分析](../Page/手段目標分析.md "wikilink")や[山登り法](../Page/山登り法.md "wikilink")が考えられる。そのような手法で解法が見つかると Soar は[チャンキング](https://ja.wikipedia.org/wiki/チャンキング "wikilink")と呼ばれる学習手法を使い、この状態遷移を新たなルールに変換する。新たなルールは Soar が同様の状況に直面したときに利用される（つまり、次回からは袋小路に陥らない）。

[ACT-R](../Page/ACT-R.md "wikilink")は[ジョン・R・アンダーソン](../Page/ジョン・R・アンダーソン.md "wikilink")の開発した別の認知アーキテクチャである。他の認知アーキテクチャとして、CLARION、ICARUS、DUAL、Psi などがある。

## 外部リンク

  - [Soar Homepage](http://sitemaker.umich.edu/soar)
  - [Soar: Frequently Asked Questions List](http://acs.ist.psu.edu/projects/soar-faq/soar-faq.html)

## 参考文献

  - Lehman, Laird, and Rosenbloom, 2006年 [A Gentle Introduction to Soar: 2006 update](http://ai.eecs.umich.edu/soar/sitemaker/docs/misc/GentleIntroduction-2006.pdf)
  - Rosenbloom, Laird, and Newell, 1993年 [The Soar Papers: Readings on Integrated Intelligence](http://www.isi.edu/soar/papers/soar-papers-book/soar-papers.html)
  - Newell, 1990年, Unified Theories of Cognition, [Harvard University](https://ja.wikipedia.org/wiki/ハーバード大学 "wikilink") Press
  - Laird, John, Newell, Allen and Rosenbloom, Paul (1987年). "Soar: An Architecture for General Intelligence". *[Artificial Intelligence](https://ja.wikipedia.org/wiki/:en:Artificial_Intelligence_\(journal\) "wikilink")*, 33: 1-64.

[Category:認知科学](https://ja.wikipedia.org/wiki/Category:認知科学 "wikilink") [Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:心理学](https://ja.wikipedia.org/wiki/Category:心理学 "wikilink") [Category:エージェントベース・プログラミング言語](https://ja.wikipedia.org/wiki/Category:エージェントベース・プログラミング言語 "wikilink")