> この記事は[Colossus](https://ja.wikipedia.org/wiki/Colossus)から翻訳されています。


**Colossus**（コロッサス、本来の意味は**[ロードス島の巨像](https://ja.wikipedia.org/wiki/ロードス島の巨像 "wikilink")**の名）は、[第二次世界大戦](https://ja.wikipedia.org/wiki/第二次世界大戦 "wikilink")の期間中、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[暗号](../Page/暗号.md "wikilink")通信を読むための[暗号解読](../Page/暗号解読.md "wikilink")器としてイギリスで使われた、[専用計算機](https://ja.wikipedia.org/wiki/専用計算機 "wikilink")である。[電子管](https://ja.wikipedia.org/wiki/電子管 "wikilink")（[真空管](../Page/真空管.md "wikilink")と[サイラトロン](https://ja.wikipedia.org/wiki/サイラトロン "wikilink")）を計算に利用していた。

Colossus は、[ブレッチリー・パーク](https://ja.wikipedia.org/wiki/ブレッチリー・パーク "wikilink")の数学者[マックス・ニューマン](https://ja.wikipedia.org/wiki/マックス・ニューマン "wikilink")が提起した問題を解くため、の技術者[トミー・フラワーズ](https://ja.wikipedia.org/wiki/トミー・フラワーズ "wikilink")を中心としたチーム（Sidney Broadhurst、William Chandler、Allen Coombs、[Harry Fensom](http://www.guardian.co.uk/theguardian/2010/nov/08/harry-fensom-obituary) ら）が設計した\[1\]。プロトタイプの **Colossus Mark I** は 1943年12月に完成し、1944年2月から[ブレッチリー・パーク](https://ja.wikipedia.org/wiki/ブレッチリー・パーク "wikilink")で動作した。改良版の **Colossus Mark II** は[ノルマンディー上陸作戦](../Page/ノルマンディー上陸作戦.md "wikilink")直前の1944年6月1日に完成した。戦争が終わるまでに10台の Colossus が製造された。

Colossus は  という機械を使って[暗号](../Page/暗号.md "wikilink")化された[テレタイプ端末](../Page/テレタイプ端末.md "wikilink")のメッセージを解読する際に使われた。イギリスの暗号解読者らはこの暗号化されたテレタイプ通信トラフィックを "" と呼び、SZ40/42 という機械とその暗号を "" と呼んだ。Colossus はふたつの[データ](../Page/データ.md "wikilink")列を比較し、プログラム可能な[ブール関数](../Page/ブール関数.md "wikilink")に基づいて一致する箇所を数える。一方のデータは紙テープから高速に読み込まれ、もう一方は内部でローレンツ暗号機の電子的シミュレーションにより生成される。そして、様々な設定でローレンツ暗号機の[エミュレーション](https://ja.wikipedia.org/wiki/エミュレーション "wikilink")を電気的に実行する。ある設定での一致箇所数が所定の閾値を越えると電気式タイプライタにその結果を出力する。

Colossusはローレンツ暗号機の鍵の組み合わせを探すのに使われたもので、傍受した暗号メッセージを完全に解読したわけではない。

プロジェクトの機密保持のため、Colossus のハードウェアと設計図はほとんど破棄され、1970年代まで機密が保持された。そのため、一部の開発関係者はデジタル電子計算機開発の先駆者としての栄誉を生前に受けることがなかった。2007年、Colossusの機能を復元したレプリカが完成している。

## 目的と起源

[thumb](https://ja.wikipedia.org/wiki/ファイル:SZ42-6-wheels-lightened.jpg "wikilink") Colossus は、 暗号機によって暗号化されたドイツの通信メッセージを[解読するために使われた](../Page/暗号解読.md "wikilink")。Colossusの仕事の一部はローレンツ暗号機の電気機械的機能を電子的にエミュレートすることである。ローレンツ暗号機でのメッセージの暗号化手順は、[平文](../Page/平文.md "wikilink")と一連の鍵[ビット](../Page/ビット.md "wikilink")とを結合させ、5つに分割する。鍵ビット列は12個のピン[歯車](../Page/歯車.md "wikilink")で生成する。このうち5個の歯車は（イギリス側で）[Χ](../Page/Χ.md "wikilink")（chi）ホイールと呼ばれ、別の5個は [Ψ](../Page/Ψ.md "wikilink")（psi）ホイールと呼ばれた。残り2個は駆動用歯車である。Χホイールは暗号化された文字毎に規則正しく回転し、Ψホイールは駆動用歯車によって制御されて不規則に回転する。

[ブレッチリー・パーク](https://ja.wikipedia.org/wiki/ブレッチリー・パーク "wikilink")の暗号解読士は、そのマシンが生成する鍵ビット列が、統計的に見て、完全な[乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink")であれば満たされるはずの振舞からはずれた偏向を示す振舞を発見し、その偏向が暗号を解読してメッセージを読むのに使えると考えた。メッセージを読むためには、ふたつの仕事を実行する必要があった。第一の仕事は「歯車のパターン解読」つまり全ての歯車のピンのパターンを発見することである。それらのパターンはローレンツ暗号機を設定変更するまでの一定期間、複数の異なるメッセージの送信で使われていた。第二の仕事は、発見したピンのパターンに基づいて「歯車を設定する」ことである。各メッセージは歯車の異なる位置から暗号化を開始される。「歯車を設定する」とは、あるメッセージの歯車の開始位置を探すことである。当初、Colossus は「歯車の設定」に使われたが、後に「歯車のパターン解読」にも使えることがわかった。

Colossus は、ブレッチリー・パークのローレンツ暗号機に対する機械的解読手法を研究した *Newmanry*（数学者[マックス・ニューマン](https://ja.wikipedia.org/wiki/マックス・ニューマン "wikilink")が指揮する部門）が運用した。

Colossus は **[Heath Robinson](https://ja.wikipedia.org/wiki/:en:Heath_Robinson_\(codebreaking_machine\) "wikilink")** と呼ばれる特殊用途の光学機械式比較器を開発するプロジェクトからの派生として開発された。Heath Robinson で問題となったのは、電気機械式リレーの遅さと2つの[紙テープ](../Page/紙テープ.md "wikilink")の同期をとる方法である。一方の紙テープは暗号化されたメッセージをさん孔されており、もう一方はローレンツ暗号機のホイールによって生成されたパターンを示している。これを一秒間に2000文字程度読むようにしたところ、テープがずれて計算が不安定になってしまった。このため英国中央郵便本局研究所のトミー・フラワーズを呼びよせ、Heath Robinson の比較機構の設計を調べさせた。フラワーズはこの機械に感心せず、自らが主導して紙テープの一方のデータを内部で生成する電子装置を設計した。フラワーズはその設計を1943年2月にマックス・ニューマンに提示したが、1000から2000本の熱イオン管（[真空管](../Page/真空管.md "wikilink")）を使って計算するというアイデアは信用されず、Heath Robinson の台数を増やすことになった。しかしフラワーズは自身のアイデアに固執し、研究所の上司から開発資金を獲得した。

## Colossus の開発

トミー・フラワーズは英国中央郵便本局研究所で Colossus の設計・製作に11カ月（1943年2月から12月）を費やした。1943年12月の機能試験の後、分解してブレッチリー・パークに移送され、試験運用が開始されたのが[1944年](../Page/1944年.md "wikilink")1月18日である。ブレッチリー・パークでの組み立ては Harry Fensom と Don Horwood が行った\[2\]。そして 1944年2月5日から Colossus は暗号解読士らに使用された\[3\]。

Mark I に続いて 9台の Colossus Mark II が1944年6月以降、順次使用された。最初の Mark I は後に Mark II に改造されている。終戦時には11台めの Colossus が組み立てをほぼ完了した状態であった。Colossus Mark I は1500本の真空管を使用している。Colossus Mark II は2400本の真空管を使用しており、Mark I の5倍の性能で操作も改善されていた。Mark II の設計は Mark I の製作と並行して行われた。トミー・フラワーズは他のプロジェクトに異動となったため、Allen Coombs が Mark II のプロジェクト責任者となった。比較すると、他の初期のコンピュータ [Manchester Mark I](../Page/Manchester_Mark_I.md "wikilink") (1949) は 4200本、[ENIAC](../Page/ENIAC.md "wikilink") (1946) は 17468本の真空管を使用している。

Colossus は電子的に歯車パターンを生成することで第二の紙テープを不要とし、一秒間に5000文字を処理することができた（紙テープの速度では毎秒12.2m）。回路の同期は紙テープのスプロケットホールによって生成される[クロック](../Page/クロック.md "wikilink")信号で行われた。従って計算速度はテープリーダーの機構によって制限されている。トミー・フラワーズは限界速度を試験し、最高で毎秒9700文字の処理速度を記録した。彼は、その試験を元に通常の運用にふさわしい速度として毎秒5000文字に設定した。場合によっては複数台の Colossus を使って今で言う[並列計算](../Page/並列計算.md "wikilink")のような使い方をすることもあり、約2倍の性能を発揮した。

Colossus には世界初の[シフトレジスタ](../Page/シフトレジスタ.md "wikilink")とが使われている。さん孔テープ上の5チャネルに対応して、最大100回の[論理演算から構成されるテストを](../Page/ブール論理.md "wikilink")5つ並行して実施できる（ただし、通常 1回の走行では1本か2本のチャネルだけを調べた）。

当初 Colossus は与えられたメッセージの最初の歯車の位置をつきとめるために使われた（「歯車の設定」）が、Mark II はピンのパターンをつきとめる（「歯車のパターン解読」）のを助けるための機構が含まれていた。どちらの機種もスイッチ群とプラグ盤を使ってプログラム可能であり、これは Heath Robinson には無い機能である。

## 設計と操作

[right](https://ja.wikipedia.org/wiki/ファイル:ColossusRebuild_11.jpg "wikilink")（右）率いるチームがブレッチリー・パークでColossusの復元を開始した。写真は、2006年のもので、完成したマシンでの暗号解読をセールが監督しているところ。\]\] Colossus は先端技術であった[真空管](../Page/真空管.md "wikilink")、[サイラトロン](https://ja.wikipedia.org/wiki/サイラトロン "wikilink")（熱陰極格子制御放電管）、[光電子増倍管](../Page/光電子増倍管.md "wikilink")（紙テープ読み取りに使用）を使っている。そしてプログラムされた論理関数を各文字に適用して、どれだけ "[真](https://ja.wikipedia.org/wiki/真 "wikilink")" が返ってくるかをカウントする。真空管は故障しやすかったが、ほとんどの故障は電源のON/OFF時に起きるので、Colossus マシンは一度電源を入れたら故障で働かなくなるまで電源を入れっぱなしにして使われた\[4\]。

Colossus はプログラム可能な電子デジタルマシンだが、そのプログラム機能は次のような点で限定されたものだった\[5\]。

  - プログラムは内蔵式ではない。新たなタスクを設定するには、オペレータがプラグ盤とスイッチ群を操作して配線を変更する。
  - 汎用性はなく、計数とブール演算という暗号解読に特化した設計である。

したがって、 ある程度の柔軟性はあるが、自由にプログラム可能とは言えず、ある種の[専用計算機](https://ja.wikipedia.org/wiki/専用計算機 "wikilink")である、ということになる。

「世界初のコンピュータはどれか」という議論（本質は「コンピュータ」の定義次第であるが）で本機とよく比較される機械について以下に述べる。[コンラート・ツーゼ](../Page/コンラート・ツーゼ.md "wikilink")の [Zuse Z3](../Page/Zuse_Z3.md "wikilink") は世界初のプログラム制御式の完全機能する[コンピュータ](../Page/コンピュータ.md "wikilink")であり、[ベル研究所](../Page/ベル研究所.md "wikilink")で[ジョージ・スティビッツ](../Page/ジョージ・スティビッツ.md "wikilink")らによって1930年代後半に開発されたマシンと同様、電気機械式リレーを使用していた。[アタナソフ&ベリー・コンピュータ](../Page/アタナソフ&ベリー・コンピュータ.md "wikilink")は電子式で2進数を使用していたが、プログラム可能ではなかった。[ヴァネヴァー・ブッシュ](../Page/ヴァネヴァー・ブッシュ.md "wikilink")らが1930年代以前から開発していた[アナログコンピュータ](https://ja.wikipedia.org/wiki/アナログコンピュータ "wikilink")は半プログラム可能であった。[チャールズ・バベッジ](../Page/チャールズ・バベッジ.md "wikilink")の[解析機関](../Page/解析機関.md "wikilink")はこれら全てに先行していたし（19世紀中盤）、デジタル式でプログラム可能だったが、部分的にしか制作されず、当時は機能しなかった（ただし、[階差機関](../Page/階差機関.md "wikilink")のレプリカは1991年に製作され動作した）。Colossus は、「デジタル」式で「プログラム可能」で「電子」式であるという組合せでは世界初であるが、汎用性は低かった。より高い汎用性は1946年に開発された[ENIAC](../Page/ENIAC.md "wikilink")で実現された。いずれにしろ[プログラム内蔵方式](../Page/プログラム内蔵方式.md "wikilink")ではなく、同方式により実現されるような柔軟なプログラム可能性もない。

## 影響とその後

Colossus の用途は国家機密であったため、その存在も戦後何年も極秘扱いのままだった。したがって、[コンピュータ史に](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink") Colossus が出てくることも無く、フラワーズらも口を噤まなければならなかった。

広く知られなかったため、直接影響を受けて開発されたコンピュータも少ない。[EDVAC](../Page/EDVAC.md "wikilink")は初期の設計としては最も後世のコンピュータ・アーキテクチャに影響を与えたと言えよう。

しかし、Colossusで培われた技術、特に信頼性のある高速電子デジタル計算デバイスはイギリスでの初期のコンピュータの開発に大きな影響を与えた。Colossus 開発に関係した人々は当然その大きな役割を理解していた。1972年、[ハーマン・ゴールドスタイン](https://ja.wikipedia.org/wiki/ハーマン・ゴールドスタイン "wikilink")（ENIAC開発者の一人）は以下のように記している。

これを書いたとき、ゴールドスタインは Colossus のことを知らなかった。それらのプロジェクトに Colossus の技術を持ち込んだ人々には、[アラン・チューリング](../Page/アラン・チューリング.md "wikilink")（[Pilot ACE](../Page/ACE_\(コンピュータ\).md "wikilink")）、マックス・ニューマン、I・J・グッド（[Manchester Mark I](../Page/Manchester_Mark_I.md "wikilink") 他）などがいる。計算機科学者は後にこう記している。

Colossusのハードウェアと関連文書は戦後しばらくは機密扱いでそのまま保持されていたが、[ウィンストン・チャーチル](../Page/ウィンストン・チャーチル.md "wikilink")が Colossus を手のひらより小さい破片に破壊するよう特別に命令した。トミー・フラワーズは青写真を暖炉で燃やした。いくつかの部品は引き抜かれ、ニューマンが[マンチェスター大学](../Page/マンチェスター大学.md "wikilink")の[王立協会](../Page/王立協会.md "wikilink")計算機研究所に持ち込んだ\[6\]。Colossus Mark I は分解され、その部品は中央郵便本局に返却された。しかし、2台の Colossus は[GCHQが](../Page/政府通信本部.md "wikilink")1952年から1954年に[チェルトナム](../Page/チェルトナム.md "wikilink")に移転したとき Eastcoate で保管された\[7\]。*Colossus Blue* と呼ばれた Colossus は 1959年に分解され、残る1つも1960年に分解された\[8\]。晩年、Colossus は訓練目的で使われたが、それ以前に他の目的に転用する試みがなされた\[9\]。I・J・グッドは[NSAを説得して](../Page/アメリカ国家安全保障局.md "wikilink") Colossus が彼らの計画していた特殊用途のマシンとして使えるとして、戦後最初にそれを使うプロジェクトに関与した\[10\]。また、Colossus は[ワンタイムパッド](../Page/ワンタイムパッド.md "wikilink")テープのランダム性を確認するために文字を種類毎に数えるという処理にも使われた\[11\]。

その間Colossusは機密とされたままだった。これはイギリスの諜報部門がエニグマ風の暗号機を使っており、それを同盟国へ売り込んでいたためで、暗号解読機の存在が知られると、誰もその暗号機を買ってくれなくなると考えたのである。しかし1960年代になると通信のデジタル化が進み、デジタル暗号システムが一般的となり、そのような暗号機の必要性は低くなっていった。

Winterbotham が *The Ultra Secret* という本 (1974) で秘密を暴露すると、Colossusに関する情報が1970年代後半に開示され始めた。[2000年](../Page/2000年.md "wikilink")10月、Tunny暗号（ローレンツ暗号機の生成する暗号）とその解読に関する500ページの技術リポート *General Report on Tunny* が[GCHQから国立公文書館に引き渡された](../Page/政府通信本部.md "wikilink")。その内容はオンラインで閲覧が可能で\[12\]、それには共に働いた暗号解読士の Colossus への賞賛の言（[ピーアン](../Page/ピーアン.md "wikilink")）が載っている\[13\]。

## 復元

[thumb](https://ja.wikipedia.org/wiki/ファイル:ColossusRebuild_12.jpg "wikilink") [2003年](../Page/2003年.md "wikilink")3月、[トニー・セール](https://ja.wikipedia.org/wiki/トニー・セール "wikilink")率いるチームが Colossus Mark II の完全動作するレプリカを組み立てた\[14\]。設計図と実物は破棄されたが、技術者のノートなど驚くほど大量の資料が主にアメリカ合衆国に現存していた。光学式紙テープリーダーが最大の問題だったが、元の設計者 Arnold Lynch が自身の元々の仕様を再現した。[バッキンガムシャー](../Page/バッキンガムシャー.md "wikilink")州[ミルトン・キーンズ](https://ja.wikipedia.org/wiki/ミルトン・キーンズ "wikilink")の[ブレッチリー・パーク](https://ja.wikipedia.org/wiki/ブレッチリー・パーク "wikilink")にある[国立コンピューティング博物館](https://ja.wikipedia.org/wiki/国立コンピューティング博物館 "wikilink")（元の Colossus 9号機が実際に置かれていた場所に開設された博物館）で組み立てられた。

2007年11月、プロジェクト完了の祝賀と博物館創設のための募金をかねて Cipher Challenge というイベントが開催された\[15\]。Lorenz SZ42 で暗号化した3つのメッセージをドイツの無線局 DL0HNF から発信し、復元したColossusと世界中のアマチュア無線家が解読を競うというイベントである。事前に注意深く準備し、[Ada](../Page/Ada.md "wikilink")で暗号解読ソフトウェアを完成させていたアマチュア無線家 Joachim Schüth が勝利した\[16\]\[17\]。Colossusチームは[第二次世界大戦](https://ja.wikipedia.org/wiki/第二次世界大戦 "wikilink")当時の無線機を使うことにこだわり\[18\]、受信状態がよくなかったため、ちゃんと受信するのに1日かかってしまった。いずれにしても、勝者は1.4GHzのパソコンを使っており、12個の歯車の設定を特定するのに1分もかからなかった。その勝者は「私のラップトップは毎秒120万文字を処理でき、Colossusの240倍の性能だった。CPUのクロック周波数を単純にその割合で算定すれば、Colossusのクロックは5.8MHzになる。これは1944年に作られたコンピュータとしては驚異的だ」と述べている\[19\]。

Cipher Challenge により、復元プロジェクトの成功が確認された。トニー・セールは「今回の性能を見ると、60年前とほぼ同等といえる。この素晴らしいマシンが暗号を解読することで戦争を何カ月も短縮した。それを生み出したブレッチリー・パークで働いていた人々にふさわしい賛辞を引き起こしたことを嬉しく思う」とコメントした\[20\]。

## 脚注

## 参考文献

  - W. W. Chandler, *The Installation and Maintenance of Colossus* (*IEEE Annals of the History of Computing*, Vol. 5 (No. 3), 1983, pp. 260–262)

  - Allen W. M. Coombs, *[The Making of Colossus](http://www.ivorcatt.com/47d.htm)* (*Annals of the History of Computing*, Vol. 5 (No. 3), 1983, pp. 253–259)

  - Jack Copeland, *Colossus: Its Origins and Originators* (*IEEE Annals of the History of Computing*, 26(4), October–December 2004, pp. 38–45).

  - Jack Copeland, *Colossus and the Dawning of the Computer Age*, in *Action This Day*, 2001, ISBN 0-593-04982-9.

  -
  - I. J. Good, *Early Work on Computers at Bletchley* (*IEEE Annals of the History of Computing*, Vol. 1 (No. 1), 1979, pp. 38–48)

  - I. J. Good, *Pioneering Work on Computers at Bletchley* (in Nicholas Metropolis, J. Howlett, Gian-Carlo Rota, (editors), *A History of Computing in the Twentieth Century*, Academic Press, New York, 1980)

  - T. H. Flowers, *[The Design of Colossus](http://www.ivorcatt.com/47c.htm)* (*Annals of the History of Computing*, Vol. 5 (No. 3), 1983, pp. 239–252)

  -
  - Brian Randell, *Colossus: Godfather of the Computer*, 1977 (reprinted in *The Origins of Digital Computers: Selected Papers*, [Springer-Verlag](https://ja.wikipedia.org/wiki/シュプリンガー・サイエンス・アンド・ビジネス・メディア "wikilink"), New York, 1982)

  -
  - Albert W. Small, [*The Special Fish Report*](http://www.codesandciphers.org.uk/documents/small/smallix.htm) (December, 1944)

  - Harvey G. Cragon, *From Fish to Colossus: How the German Lorenz Cipher was Broken at Bletchley Park* (Cragon Books, Dallas, 2003; ISBN 0-9743045-0-6) – Tunnyによる暗号解読についての詳細と Colossus についてのいくつかの詳細 (細かな間違いがある)

  - Ted Enever, *Britain's Best Kept Secret: Ultra's Base at Bletchley Park* (Sutton Publishing, Gloucestershire, 1999; ISBN 0-7509-2355-5) – ブレッチリーパークの歴史と観光案内

  - Tony Sale, *The Colossus Computer 1943–1996: How It Helped to Break the German Lorenz Cipher in WWII* (M.\&M. Baldwin, Kidderminster, 2004; ISBN 0-947712-36-4) – 薄い (20ページ) 小冊子。下記の筆者によるサイトと同じ内容を含む

  - Michael Smith, *Station X*, 1998. ISBN 0-330-41929-3.

  -
  - R. Rojas, U. Hashagen (eds.): *The First Computers: History and Architectures*. MIT Press 2000. ISBN 0-262-18197-5. – 初期のコンピュータの比較。Colossusとその復元についての章がある。

## 関連項目

  - [エニグマ (暗号機)](../Page/エニグマ_\(暗号機\).md "wikilink")
  - [計算機の歴史](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink")
  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")
  - [Zuse Z3](../Page/Zuse_Z3.md "wikilink")
  - 小説『コロッサス』（映画・邦題『[地球爆破作戦](../Page/地球爆破作戦.md "wikilink")』の原作）

## 外部リンク

  - [The National Museum of Computing](http://www.tnmoc.org)
  - [Tony Sale's WW II Codes and Ciphers](http://www.codesandciphers.org.uk/index.htm) Colossusに関する多くの情報を含む
      - [Colossus, the revolution in code breaking](http://www.codesandciphers.org.uk/virtualbp/fish/colossus.htm)
      - [Lorenz Cipher and the Colossus](http://www.codesandciphers.org.uk/lorenz/index.htm)
          - [The machine age comes to Fish codebreaking](http://www.codesandciphers.org.uk/lorenz/colossus.htm)
          - [The Colossus Rebuild Project](http://www.codesandciphers.org.uk/lorenz/rebuild.htm)
          - [The Colossus Rebuild Project: Evolving to the Colossus Mk 2](http://www.codesandciphers.org.uk/lorenz/mk2.htm)
          - [Walk around Colossus](http://www.codesandciphers.org.uk/lorenz/colwalk/colossus.htm) 復元したColossusの詳細な紹介。それぞれの写真にある "More Text" というリンクをクリックすると、各部分について詳細な説明が表示される。
      - [IEEE lecture](http://www.codesandciphers.org.uk/lectures/ieee.txt) – Tony Sale がColossus復元プロジェクトについて行った講演の記録
  - ["Return of Colossus marks D-Day"](http://news.bbc.co.uk/1/hi/technology/3754887.stm) BBCの記事 (2004-06-01)
  - ["Colossus cracks codes once more"](http://news.bbc.co.uk/1/hi/technology/7094881.stm) BBCの記事 (2007-11-15)
  - ["Bletchley's code-cracking Colossus"](http://news.bbc.co.uk/1/hi/technology/8492762.stm) BBCの記事。インタビュー動画付き (2010-02-02)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:暗号解読装置](https://ja.wikipedia.org/wiki/Category:暗号解読装置 "wikilink")

1.  [Bletchley's code-cracking Colossus](http://news.bbc.co.uk/1/hi/technology/8492762.stm)
2.  [The Colossus Rebuild](http://www.tnmoc.org/colossus-rebuild.aspx)
3.
4.
5.  [A Brief History of Computing](http://www.alanturing.net/turing_archive/pages/Reference%20Articles/BriefHistofComp.html#Col). Jack Copeland, June 2000
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.