> この記事は[GD-ROM](https://ja.wikipedia.org/wiki/GD-ROM)から翻訳されています。


**GD-ROM**（Gigabyte Disk ROM）は、[セガと](https://ja.wikipedia.org/wiki/セガゲームス "wikilink")[ヤマハ](../Page/ヤマハ.md "wikilink")が共同で開発した[光ディスク](../Page/光ディスク.md "wikilink")[メディア](../Page/メディア_\(媒体\).md "wikilink")。直径は[CDと同じ](../Page/コンパクトディスク.md "wikilink")12cmであるが、記録密度を高めることにより約1[GBの容量を達成している](../Page/ギガバイト.md "wikilink")。セガの家庭用[テレビゲーム](https://ja.wikipedia.org/wiki/テレビゲーム "wikilink")機[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")や、後の[セガ・インタラクティブ](https://ja.wikipedia.org/wiki/セガ・インタラクティブ "wikilink")にあたる部門の業務用システム基板[NAOMI](../Page/NAOMI.md "wikilink") / [NAOMI2](https://ja.wikipedia.org/wiki/NAOMI2 "wikilink") / [chihiro](https://ja.wikipedia.org/wiki/chihiro "wikilink") / [Triforce](https://ja.wikipedia.org/wiki/Triforce "wikilink")に採用された（chihiroの次の世代の基板である[LINDBERGH](../Page/LINDBERGH.md "wikilink")は[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")を採用）。

## フォーマット

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gdrom.jpg "wikilink") GD-ROMでは、1GBの容量を実現するために、[CD-ROM](../Page/CD-ROM.md "wikilink")とは異なる独自のフォーマットを採用している。その実体は、[マルチセッション](https://ja.wikipedia.org/wiki/マルチセッション "wikilink")にした[CD-ROM](../Page/CD-ROM.md "wikilink")の 2セッション目を高密度フォーマットで記録したものであり、物理フォーマットとしては大別して3つの領域に分けることができる。

  - 内周の領域は音楽CD/CD-ROMと同じフォーマット（[ISO 9660](../Page/ISO_9660.md "wikilink")）であり、ドリームキャスト用ソフトの場合であればここにソフトの概要などを記述したテキストファイルが3つと、一般のCDプレイヤーで再生しないよう注意を喚起する音声が収録されている\[1\]。PC向けのおまけデータが入っている場合もある。内周部の容量は35MB程度、[CD-DA](../Page/CD-DA.md "wikilink")で約4分である
  - 外周部はGD-ROM独自の高密度フォーマットとなっており、一般のCD-ROMドライブで読むことはできない。外周部はCDでいう10分の位置から開始し、約984MB（112分）の容量を持つ。 この領域のフォーマットについては、 エラー訂正情報を減らしてその分データ量を増やしたという説 がある。
  - その間にある領域にはデータは格納されておらず、記録面には代わりに権利関係の2つの英文が書かれている。なおこの英文は[セガサターン](../Page/セガサターン.md "wikilink")用のCD-ROMでも使われていた。

GD-ROMでは読み出しの効率を高めるため、ディスクのピックアップ上の通過速度が速くなる最外周部から順にゲームデータを記録している。つまり、ゲームデータ自体のサイズが小さい場合でもデータは最外周まで記録されていることになる。第2セッション（高密度記録部）の内周側は通常「0」が延々と続くダミートラックで埋められており、実際のゲームデータはその後に続いている。

## 違法コピーとの関連

このような独自のフォーマットを採用した理由には、大容量化の他に不正コピー対策という側面もあった。しかし、ドリームキャストのシステムにプロテクトがかけられていない[CD-R](../Page/CD-R.md "wikilink")で任意のコードを実行できるセキュリティホールが発見され、シリアルポートやブロードバンドアダプタを経由したデータ転送を使用してGD-ROMからCD-Rへメディア変換を行う不正コピーが横行してしまった。

## 脚注

[Category:電子媒体](https://ja.wikipedia.org/wiki/Category:電子媒体 "wikilink") [Category:光ディスク](https://ja.wikipedia.org/wiki/Category:光ディスク "wikilink") [Category:セガのハードウェア](https://ja.wikipedia.org/wiki/Category:セガのハードウェア "wikilink") [Category:ドリームキャスト](https://ja.wikipedia.org/wiki/Category:ドリームキャスト "wikilink") [Category:コンピュータゲーム流通](https://ja.wikipedia.org/wiki/Category:コンピュータゲーム流通 "wikilink")

1.  標準の警告メッセージは、ドリームキャストは、「これは、ドリームキャスト用のゲームディスクです。1トラック目に、ゲームのデータが入っていますので、再生しないでください。」、NAOMIは「これはNAOMI用のGD-ROMゲームディスクです。ドリームキャストでは動作しません。1トラック目に、ゲームのデーターが入っていますので、再生しないでください。」、Triforceは「これは、GD-ROMゲームディスクです。1トラック目に、ゲームのデータが入っていますので、再生しないでください。」と流れる。ドリームキャストはゲームキャラによる専用の警告メッセージを用意している場合もある。