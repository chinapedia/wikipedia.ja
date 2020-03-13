> この記事は[Plain Old Java Object](https://ja.wikipedia.org/wiki/Plain_Old_Java_Object)から翻訳されています。


**Plain Old Java Object** (**POJO**) は、ある[Java](https://ja.wikipedia.org/wiki/Java "wikilink")オブジェクトが[EJB](../Page/Enterprise_JavaBeans.md "wikilink")（特にEJB 3より前のEJB）のように特殊なものではなく、ごく普通のJavaオブジェクトであることを強調した名称。設計はシンプルであればあるほど良いと主張する人たちが好んで使用する。

## 概要

[2000年](../Page/2000年.md "wikilink")9月に[マーティン・ファウラー](../Page/マーティン・ファウラー.md "wikilink")と[レベッカ・パーソンズ](https://ja.wikipedia.org/wiki/レベッカ・パーソンズ "wikilink")、[ジョシュ・マッケンジー](https://ja.wikipedia.org/wiki/ジョシュ・マッケンジー "wikilink")がこの用語を使い始めた。「システムに普通のオブジェクトを使うことに強い抵抗を持つ人が多いのはなぜかと考えたとき、それは単純なオブジェクトに良い名前がついていないのが原因だという結論に達した。そこで我々が名前をつけたら、それがとても流行りだした。」[1](http://www.martinfowler.com/bliki/POJO.html) この命名法は、[テレフォニーにおけるPOTS](https://ja.wikipedia.org/wiki/電気通信役務 "wikilink") ([Plain Old Telephone Service](https://ja.wikipedia.org/wiki/Plain_Old_Telephone_Service "wikilink")) や、[C++](../Page/C++.md "wikilink")で書かれているが[C言語](../Page/C言語.md "wikilink")の機能しか使わないPODS () など、高級な新機能を使わない技術に対する既存の用語と同じパターンに従っている。

この用語が広く受け入れられた背景には、複雑で特殊なオブジェクト[フレームワークと対照的な](../Page/アプリケーションフレームワーク.md "wikilink")、一般的で理解しやすい用語が求められていたことがあると思われる。この用語は、[JavaBeans](../Page/JavaBeans.md "wikilink")と[Enterprise JavaBeansの名前が衝突しているJava](../Page/Enterprise_JavaBeans.md "wikilink") "bean"用語よりも魅力的である。JavaBeansは、厳格な命名規約を持つ[シリアライズ](../Page/シリアライズ.md "wikilink")可能なPOJOであるとほぼ言える一方、Enterprise JavaBeansは単一クラスではなく、まったくの[コンポーネントモデルである](https://ja.wikipedia.org/wiki/ソフトウェア部品 "wikilink")（ただしEJB 3以降は差が減っている）。

POJOの概念は、明らかにPOJOという用語より前から存在する。なぜなら、オブジェクトクラスの自然なありさまとは、何ら特別なものではないからである。この用語の功績は、何らかのフレームワークを使う利点がその複雑さを補ってあまりあるかどうかということを開発者に考えさせるという点にある。シンプルな設計の方が優れている場合もあるということを思い出させる明確な用語がなくては、複雑なフレームワークが十分な理由のないまま[システムアーキテクチャ](../Page/システムアーキテクチャ.md "wikilink")に含まれてしまいやすい。POJOによる設計が一般的になるにつれて、大規模フレームワークの機能の一部はPOJOでも実現できることが明らかになってきており、実際に必要な機能領域に対する選択肢は増えている。[Hibernate](../Page/Hibernate.md "wikilink")と[Springがその例である](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")。

## 曖昧さの可能性

[2005年](../Page/2005年.md "wikilink")11月時点で、"POJO"という用語は主に、いかなる（主要な）Javaオブジェクトモデル、規約、フレームワーク（たとえばEJB）にも従わないJavaオブジェクトを指して使われている。しかし、モデルやフレームワークが将来的に変化する可能性や、またこのような分類自体が文脈に依存するという事実を考慮すると、その定義は本質的に不安定で曖昧である。

厳密に言えば、POJOは全てのJavaオブジェクトを指す用語とも言える。この解釈に基づけば、POJOに関連する記述は全てのJavaオブジェクトに例外なく当てはまらなければならない。しかし、多くの人はこの意見に反対している。

EJB 3の仕様はPOJOプログラミングモデルであることを宣言しており、EJB3 Session BeanをPOJOとして記述している。ただし、通常は[アノテーション](../Page/アノテーション.md "wikilink")を必要とする。

## 関連項目

  - [JavaBeans](../Page/JavaBeans.md "wikilink")
  - [Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink") (EJB)

## 外部リンク

  - [IT用語辞典e-Words - POJO](http://e-words.jp/w/POJO.html)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")