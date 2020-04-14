> この記事は[OCFフォント](https://ja.wikipedia.org/wiki/OCFフォント)から翻訳されています。


**OCFフォント**（Original Composite Font）は、[Macintosh](../Page/Macintosh.md "wikilink")（[Mac OS 9まで](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS "wikilink")）で使用できる和文（[2バイト文字](https://ja.wikipedia.org/wiki/2バイト文字 "wikilink")の言語用の）[フォント](../Page/フォント.md "wikilink")（[PostScriptフォント](../Page/PostScriptフォント.md "wikilink")）で、欧文用フォントファイルを多数積み重ねた構造をしている。[DTP](../Page/DTP.md "wikilink")の発達とともに普及し、一時代を成した。現在は後継の[CIDフォント](https://ja.wikipedia.org/wiki/CIDフォント "wikilink")や[OpenTypeフォント](https://ja.wikipedia.org/wiki/OpenTypeフォント "wikilink")に主流の座を譲っているが、OCFのFとはフォントの意味なので、**OCFフォント**という表現は Original Composite Font Font となってしまい、重複していると言える。

## 誕生の経緯

PostScriptフォントのうち、（狭義の）Type1やType3フォントは当初の仕様として欧文を前提としており、扱える文字数は256文字（=1バイト）までだった。しかしこれでは[常用漢字](../Page/常用漢字.md "wikilink")と[仮名](../Page/仮名_\(文字\).md "wikilink")・記号類だけに限っても数千文字が必要な日本語[組版](../Page/組版.md "wikilink")には不充分であるため、複数のType1フォントを積み重ねた構造のComposit（コンポジット=複合の、合成の）フォントとして策定されたのがOCF形式である。

## 導入と普及

日本語DTPはOCFフォントによって黎明を告げた。その時点で標準に躍り出た[モリサワ](../Page/モリサワ.md "wikilink")のフォントは、当初文字の輪郭情報（アウトライン情報）の抽出が不可能という仕様であった。これには、コピープロテクト（コピー防止機能）とアウトラインプロテクトが同一のプログラムとして提供されていたためでもあった。のちのNew-CIDと呼ばれる製品では、アウトライン抽出は問題なくおこなえる。

フォント製品として当初提供されたのは、モリサワの[リュウミン](../Page/リュウミン.md "wikilink")と中ゴシックのみであったが、他社も含めて次第にラインナップは増大し、日本語DTPのスタンダードとして広く普及した。

その後、データ構造を改善し軽量・高速化した（といわれる）CIDフォントが登場し、ベンダー（販売社）はこちらへの交換を利用者に促した。しかし、交換手数料に比してその利便性が高くないなどといった理由 から、そののちもOCFというフォントフォーマットは事実上の標準でありつづけた。

OCFフォントから撤退するための影響は個人運営やSOHOでは予算・規模共に軽微だが、商業印刷では仕事のシステム全体に大きな影響が及ぶ。DTP導入時に大変な労力を割いてOCFベースの運用で安定させたシステムを、敢えて崩す必要性を多くのユーザー（印刷会社、出版社など）は認めなかったといった説明がなされる。またその背景として、日本国内における組版料金の単価低下という要素も見逃せないであろう。[写植の時代に比して相対的に売り上げが低下する中](https://ja.wikipedia.org/wiki/写真植字 "wikilink")、交換せずとも使用できる製品を既に持っているユーザーは、経済的理由からも既存のOCFフォントを使い続けたのである。

## 後継規格への移行

PostScriptフォントの主流は既にCIDフォントに移り、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")ではOSの仕様上、インストールからして不可能である。 また、OCFフォントは筆頭ベンダーのモリサワなどでは販売やサポート、新フォーマットへの交換などが終了しており、現在新規に入手するのは、[フォントワークス](../Page/フォントワークス.md "wikilink")のLETSプログラムなどの例外を除いて困難と言える。

そのため、新たにDTP設備を導入するところなどでは、必然的にCIDやOpenTypeフォントとなる。もっとも、規格が異なるとはいえ運用上必要なPostScript名が一致していれば、諸々の注意をはらえば混用は可能ではある。

## 関連項目

  - [PostScript](../Page/PostScript.md "wikilink")
  - [Adobe Font Metrics](../Page/Adobe_Font_Metrics.md "wikilink")

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink")