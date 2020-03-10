> この記事は[Harvard Mark I](https://ja.wikipedia.org/wiki/Harvard_Mark_I)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Harvard_Mark_I_Computer_-_Left_Segment.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Harvard_Mark_I_Computer_-_Right_Segment.JPG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Harvard_Mark_I_Computer_-_Input-Output_Details.jpg "wikilink") **Harvard Mark I** (ハーバード マーク ワン) は、[IBM](../Page/IBM.md "wikilink")の**ASCC**\[1\]とも呼ばれ\[2\]、[アメリカ初の電気機械式](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[計算機](../Page/計算機.md "wikilink")である。

電気機械式のASCCは[ハワード・エイケン](../Page/ハワード・エイケン.md "wikilink")が考案し、[IBM](../Page/IBM.md "wikilink")が製作し、[ハーバード大学](https://ja.wikipedia.org/wiki/ハーバード大学 "wikilink")に[1944年](../Page/1944年.md "wikilink")2月に出荷された。当初、アメリカ海軍の船舶局が計算に使用し、正式に大学に引き渡されたのは[1944年](../Page/1944年.md "wikilink")8月7日である。

## 設計と構成

ASCCを構成しているのは[スイッチ](../Page/開閉器.md "wikilink")、[リレー](../Page/継電器.md "wikilink")、歯車式の計算装置（タイガー計算器などの計算部分のような機構。英語版記事 [:en:Pinwheel calculator](https://ja.wikipedia.org/wiki/:en:Pinwheel_calculator "wikilink") などを参照）、[クラッチ](https://ja.wikipedia.org/wiki/クラッチ "wikilink")などである。765,000個の電気機械部品\[3\]と数百kmの電線を使って作られ、全長16m、高さ2.4m、奥行きは約60cmである。その重量は約4.5tであった。基本計算装置は機械的に同期して動作するため、15.5mの軸で接続されていて、4kW（5馬力）の電動モーターで駆動される。IBMのアーカイブには次のように記されている。

の筐体（フレームカバー）はインダストリアルデザイナーののデザインだった。エイケンはこのような精巧な筐体は資源の浪費だと考えており、戦時中の計算需要の高さから、筐体に払う金（[グレース・ホッパー](../Page/グレース・ホッパー.md "wikilink")によれば50万ドル）があったら追加の計算装置を構築できたのにと言っていた\[4\]。

## 動作

には、24個のスイッチが60セットあり、それらを使って手動でデータを入力する。23桁の十進数を72個格納でき\[5\]、一秒間に3回の加算または減算ができる。乗算には6秒かかり、除算は15.3秒、対数や三角関数の計算には1分以上かかった。

は24チャンネルの[さん孔テープから命令を順次読み取り](../Page/紙テープ.md "wikilink")、実行する。[条件分岐](https://ja.wikipedia.org/wiki/条件分岐 "wikilink")命令はなく、複雑なプログラムは物理的にも長いテープを必要とした。ループはプログラムの記されているテープの終端をテープの先端に物理的につなげて本当にループを形成させていた。このようにデータと命令を分離することを[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")と呼ぶ。Mark I の最初のプログラマはリチャード・ミルトン・ブロック、ロバート・キャンベル、[グレース・ホッパー](../Page/グレース・ホッパー.md "wikilink")であった\[6\]。

## 命令フォーマット

24チャンネルの入力テープは、それぞれ8チャンネルの3フィールドに分割されている。各[アキュムレータ](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")、各スイッチ群、[入出力](../Page/入出力.md "wikilink")に対応しているレジスタ群、[演算装置にはそれぞれ一意なインデックス番号が付与されている](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")。それらの番号が制御テープ上で[二進法](../Page/二進法.md "wikilink")で表現されている。第1フィールドは操作の結果が格納される場所のインデックス番号を二進法で表したもので、第2フィールドは操作の元となるデータが格納されている場所（のインデックス番号を二進法で表したもの）、第3フィールドは実行すべき操作に対応する「命令コード」である\[7\]。

## エイケンとIBM

エイケンは報道機関への発表で、自身が単独で  を「発明」したと記した。実際にはクレア・レイクやフランク・ハミルトンといったIBMの技術者も様々な部品の設計を助けていたが、エイケンが発表の中で触れたIBMの人物はだけだった。[トーマス・J・ワトソン](../Page/トーマス・J・ワトソン.md "wikilink")はこれに怒り、1944年8月7日の開所式にもしぶしぶ出席した\[8\]\[9\]。エイケンはその後、IBMの支援を得ずに後継機を構築することを決め、ASCCは一般に Harvard Mark I の名で知られるようになった。その後IBMは[SSEC](https://ja.wikipedia.org/wiki/SSEC "wikilink")\[10\]の開発に向かい、新技術の評価を行うと同時に世間の注目を集めようとした\[11\]。

## 後継

その後  の後継として、（1947年または1948年）、[Mark III/ADEC](https://ja.wikipedia.org/wiki/Harvard_Mark_III "wikilink")（1949年9月）、（1952年）が開発された。全てエイケンの仕事である。 は  を改良したものだが、相変わらず電気機械式のリレーを使っている。 は、大部分を真空管やクリスタル・ダイオードなどの電子部品で構成し、Mark IV では完全に電子化され[半導体](../Page/半導体.md "wikilink")部品を使っている。 と  は[磁気ドラムメモリ](https://ja.wikipedia.org/wiki/磁気ドラムメモリ "wikilink")を使い、 はさらに[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")を使っていた。 と  は[アメリカ海軍](../Page/アメリカ海軍.md "wikilink")の基地に納入された。Mark IV は[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")のために製作されたが、ハーバードに残された。

はすでに分解されているが、その一部はハーバードのキャボット・サイエンス・センター\[12\]に残されている。

## 脚注

## 参考文献

  -
  -
  -   - 日本語訳:山本 菊男（訳）『コンピューター200年史 — 情報マシーン開発物語 —』、海文堂、1999年、ISBN 4-303-71430-5

## 関連項目

  - [計算機の歴史](https://ja.wikipedia.org/wiki/計算機の歴史 "wikilink")
  - [ハワード・エイケン](../Page/ハワード・エイケン.md "wikilink")
  - 他の初期の計算機
      - [Zuse Z3](../Page/Zuse_Z3.md "wikilink") （ドイツ）
      - [Manchester Mark I](../Page/Manchester_Mark_I.md "wikilink") （イギリス）
      - [アタナソフ&ベリー・コンピュータ](../Page/アタナソフ&ベリー・コンピュータ.md "wikilink") （アメリカ）
      - [ENIAC](../Page/ENIAC.md "wikilink") （アメリカ）
      - [Colossus](../Page/Colossus.md "wikilink") （イギリス）
      - IBM [Selective Sequence Electronic Calculator](../Page/Selective_Sequence_Electronic_Calculator.md "wikilink") （アメリカ）

## 外部リンク

  - [Oral history interview with Robert Hawkins](http://purl.umn.edu/107348) at [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota, Minneapolis.
  - [Oral history interview with Richard M. Bloch](http://purl.umn.edu/107123) at Charles Babbage Institute, University of Minnesota, Minneapolis.
  - [Oral history interview with Robert V. D. Campbell](http://purl.umn.edu/107210) at Charles Babbage Institute, University of Minnesota, Minneapolis.
  - [IBMs ASCC Reference Room(英語)](http://www-1.ibm.com/ibm/history/exhibits/markI/markI_reference.html)
  - [ASCC operational manual(英語)](http://www.bitsavers.org/pdf/harvard/MarkI_operMan_1946.pdf) (PDF)
  - [ROBOT Mathematician Knows All the Answers](http://books.google.com/books?id=PyEDAAAAMBAJ&lpg=PP1&dq=popular%20science%201944&pg=PA86#v=onepage&q&f=true) Popular Science, October 1944, Page 86.

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:IBMのコンピュータ](https://ja.wikipedia.org/wiki/Category:IBMのコンピュータ "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink") [Category:ハーバード大学](https://ja.wikipedia.org/wiki/Category:ハーバード大学 "wikilink") [Category:電気機械式コンピュータ](https://ja.wikipedia.org/wiki/Category:電気機械式コンピュータ "wikilink")

1.
2.  ハードウェアそのものに掲げられている名称は  である。に掲載されている初期の写真には  とある。
3.
4.  [Computer Oral History Collection, 1969-1973, 1977](http://invention.smithsonian.org/downloads/fa_cohc_tr_hopp690107.pdf) *Grace Murray Hopper Interview, January 7, 1969*, Archives Center, National Museum of American History
5.
6.  Wexelblat, Richard L. (Ed.) (1981). *History of Programming Languages*, p. 20. New York: Academic Press. ISBN 0-12-745040-8
7.
8.
9.
10.
11.
12.