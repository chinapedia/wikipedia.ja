> この記事は[BINAC](https://ja.wikipedia.org/wiki/BINAC)から翻訳されています。


**BINAC**（バイナック、Binary Automatic Computer）は、[エッカート・モークリー・コンピュータ・コーポレーション](https://ja.wikipedia.org/wiki/エッカート・モークリー・コンピュータ・コーポレーション "wikilink")(EMCC)が[1949年](../Page/1949年.md "wikilink")に[ノースロップ](../Page/ノースロップ.md "wikilink")社のために設計・製造した電子式[コンピュータ](../Page/コンピュータ.md "wikilink")である\[1\]\[2\]。

[ジョン・プレスパー・エッカート](../Page/ジョン・プレスパー・エッカート.md "wikilink")と[ジョン・モークリー](../Page/ジョン・モークリー.md "wikilink")は[ペンシルベニア大学](../Page/ペンシルベニア大学.md "wikilink")で[EDVAC](../Page/EDVAC.md "wikilink")を設計していたが、知的所有権を大学に譲渡する契約を迫られたことから大学を離れ、世界初のコンピュータメーカーであるEMCCを設立した。EMCCでは[UNIVAC Iを受注して開発を行っていたが](../Page/UNIVAC_I.md "wikilink")、資金不足に陥り、ノースロップからの前払い金を運営資金とするためにBINACの開発を請け負った。よってBINACはEMCCの最初の製品であり、アメリカ合衆国初の[プログラム内蔵方式](../Page/プログラム内蔵方式.md "wikilink")のコンピュータである。BINACは「世界初の商用コンピュータ」と呼ばれることもあるが\[3\]\[4\]、機能の範囲が非常に限られており、完全に機能することはなく、継続して使用することはできなかった。BINACがほとんど名前を残していないのはそのためである。

## アーキテクチャ

BINACは、2つの[CPU](../Page/CPU.md "wikilink")を持つ[二進数のコンピュータであり](../Page/二進法.md "wikilink")、各CPUには独立した512[ワード](../Page/ワード.md "wikilink")の[水銀遅延線](https://ja.wikipedia.org/wiki/水銀遅延線 "wikilink")[メモリが装備されている](../Page/主記憶装置.md "wikilink")。CPUは互いの結果をチェックし合い、ハードウェア障害に起因するエラーがチェックできるようになっている。使用した[真空管](../Page/真空管.md "wikilink")の数は約700本である。512ワードのメモリは16チャネルに分割されていて、各チャネルは32ワード×31ビットで構成され、ワード間にはスイッチングの遅延に対応した11ビットのスペースが挟み込まれている。動作周波数は 4.25MHz（一説には 1MHz）で、1ワードの取り出しに約10マイクロ秒かかる。計算時間は加算で800マイクロ秒、乗算で1200マイクロ秒であった。プログラムやデータの入力は、8個のキーからなるキーパッドを使って[八進数で入力するか](../Page/八進法.md "wikilink")、磁気テープを使用した\[5\]\[6\]。BINACは二進数の高速演算を実現するよう設計されていたが、文字や[十進数](https://ja.wikipedia.org/wiki/十進数 "wikilink")の数値のことは全く考慮していない。

## 客先での受け入れ試験

1949年3月、BINAC上で23[命令からなるテストプログラムが実行されたが](../Page/命令セット.md "wikilink")、完全には動作しなかった。BINACではそれ以前に以下のようなテストプログラムが動作している。

  - 1949年2月7日 レジスタAからメモリに書き込む5行のプログラム
  - 1949年2月10日 メモリチェックをする5行のプログラム
  - 1949年2月16日 メモリに書き込む6行のプログラム
  - 1949年3月7日 数の平方を求める23行のプログラムを217回ループさせた。停止時にも正常に動作していた。
  - 1949年4月4日 メモリに書き込み、全種類の命令をチェックする50行のプログラム。エラーが発生するまで2.5時間動作した。その直後に再実行したところ31.5時間連続動作した。

ノースロップは1949年9月にBINACを受け取った\[7\]\[8\]。ノースロップの従業員は、BINACは、EMCCの施設内では正常に動作していたにもかかわらず、ノースロップへの納品後は適切に機能しなかったと主張している。いくつかの小さなプログラムは動作したが、製品として使おうとすると連続動作できなかった。

ノースロップでは、引き取りに行ったときに、出荷用に適切に梱包されていなかったのが原因であると考えた。EMCCは、出荷後の装置の再組み立てが正しく行われていないのが原因であると主張した。ノースロップは、セキュリティ上の理由から、EMCCの技術者が装置の再組み立てのためにノースロップの施設内に入ることを拒否した。その代わりに学校を卒業したばかりの新入社員に再組み立てを行わせた。EMCCは、設計の品質を証明した後で、それは完全に機能したと主張している\[9\]。

## 世界初のエンドユーザ向けマニュアル

それ以前のコンピュータは、大学の工学部の中で使用されるものであり、コンピュータを操作する人は装置のことをよく知っていた。BINACはエンドユーザが使用するものであるため、エンドユーザのためのマニュアル（取扱説明書）が必要となった。

当時、自動車のユーザーは、車両の整備にかなり慣れており、それを支援する「ユーザーマニュアル」が存在していた。BINACのマニュアル作成者は、BINACのユーザーマニュアルを作成するときに、自動車の整備マニュアルからインスピレーションを得た\[10\]。

## 関連項目

  - [真空管式コンピュータ一覧](../Page/真空管式コンピュータ一覧.md "wikilink")
  - [Short Code (プログラミング言語)](https://ja.wikipedia.org/wiki/Short_Code_\(プログラミング言語\) "wikilink")

## 脚注

## 参考文献

  -
## 外部リンク

  - (search YouTube for *1949 BINAC: Binary Automatic Computer, History Mauchly Eckert EMCC UNIVAC First Stored Program, U.S.*, the link is not allowed) Documentary film on the BINAC by the Computer History Archives Project, Sep 16 2018, with many pictures and original film sources.

  - [Oral history interview with Isaac Levin Auerbach](http://purl.umn.edu/59495) Oral history interview by Nancy B. Stern, 10 April 1978. [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota. Auerbach recounts his experiences at Electronic Control Company (later the [Eckert-Mauchly Computer Company](https://ja.wikipedia.org/wiki/エッカート・モークリー・コンピュータ・コーポレーション "wikilink")) during 1947–49. He evaluates BINAC, [UNIVAC](../Page/UNIVAC.md "wikilink"), and the roles of the [National Bureau of Standards](../Page/アメリカ国立標準技術研究所.md "wikilink"), [Northrop Aircraft](../Page/ノースロップ.md "wikilink"), [Raytheon](../Page/レイセオン.md "wikilink"), [Remington Rand](../Page/レミントンランド.md "wikilink"), and [IBM](../Page/IBM.md "wikilink").

  -
  - [Roger Mills' Description of the BINAC](https://web.archive.org/web/20080804005753/http://www.palosverdes.com/lasthurrah/binac-description.html)

  - [Picture of BINAC history sign in Northeast Philadelphia](http://moby.to/3yet86)

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:1940年代のコンピュータ](https://ja.wikipedia.org/wiki/Category:1940年代のコンピュータ "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink") [Category:個別のコンピュータ](https://ja.wikipedia.org/wiki/Category:個別のコンピュータ "wikilink")

1.
2.
3.
4.
5.
6.   102646200 {{\!}} Computer History Museum|website=www.computerhistory.org|language=en|access-date=2018-05-17}}
7.
8.
9.
10.