> この記事は[CLIPS](https://ja.wikipedia.org/wiki/CLIPS)から翻訳されています。


**CLIPS**とは、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の名称であり[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")の一種である。***C** **L**anguage **I**ntegrated **P**roduction **S**ystem*([C言語](../Page/C言語.md "wikilink")統合型プロダクションシステム)の略。その文法と名称は[チャールズ・フォーギー](../Page/チャールズ・フォーギー.md "wikilink")の[OPS](https://ja.wikipedia.org/wiki/OPS5 "wikilink")(Official Production System、もっとも公式(Official)なものでは全くない)からインスパイアされたものである。CLIPSの最初のバージョンは[1984年](../Page/1984年.md "wikilink")に[NASAの](../Page/アメリカ航空宇宙局.md "wikilink")[ジョンソン宇宙センター](../Page/ジョンソン宇宙センター.md "wikilink")で(既存のシステム ART\*Inference の後継として)開発された。[1990年代](../Page/1990年代.md "wikilink")初めに国家予算問題で予算がつかなくなり、NASAは自力での開発をやめて一般の商用ソフトウェアを購入することになった。

CLIPSは高速で効率がよく無料であるため、最も広く使われているエキスパートシステム・ツールと言えるだろう。現在はパブリックドメインだが、それでもオリジナルの作者ゲーリー・ライリーがアップデートとサポートを続けている。

CLIPSはエキスパートシステムを記述するための完全な[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink") *COOL* を含んでいる。[C言語](../Page/C言語.md "wikilink")で書かれているが、そのインターフェイスは[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")に近い。拡張はC言語で行い、CLIPSをC言語から呼び出すこともできる。

他のエキスパートシステム用言語と同様、CLIPSは規則と事実を扱う。様々な事実によって規則が適用可能となり、適用可能となった規則はアサートされる。事実と規則は以下のように定義される。

`(deffacts trouble_shooting`
`    (car_problem (name ignition_key) (status on))`
`    (car_problem (name engine) (status wont_start))`
`    (car_problem (name headlights) (status work))`
` )`
`(defrule rule1`
`    (car_problem (name ignition_key) (status on))`
`    (car_problem (name engine) (status wont_start))`
`     =>`
`    (assert (car_problem (name starter) (status faulty))`
` )`

CLIPS言語の後継として[Jess](../Page/Jess.md "wikilink")([Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書き直されたルールベース部を持つが、その後異なる方向に成長)、[ECLiPSe](http://www.icparc.ic.ac.uk/eclipse/)、Haley Eclipse、FuzzyCLIPS (関連性の概念を導入した言語)などがある。

CLIPSに関する教科書として *Expert Systems: Principles and Programming* (ISBN 0-534-95053-1) がある。また、CLIPSはドキュメントを豊富に含んでいる。

## 外部リンク

すべて英文

  - [プロジェクトのページ](http://clipsrules.sourceforge.net/)
  - [CLIPS expert system tool: a candidate for the Diagnostic System engine](http://rd13doc.cern.ch/Atlas/Notes/108/Note108-1.html)

[Category:エキスパートシステム](https://ja.wikipedia.org/wiki/Category:エキスパートシステム "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ドメイン固有言語](https://ja.wikipedia.org/wiki/Category:ドメイン固有言語 "wikilink")