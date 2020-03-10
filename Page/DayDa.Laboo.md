> この記事は[DayDa.Laboo](https://ja.wikipedia.org/wiki/DayDa.Laboo)から翻訳されています。


**DAYDA.Laboo**(デイダ ラボー）とは、[株式会社ターボデータラボラトリー](http://www.turbo-data.co.jp/)(代表取締役：古庄晋二）により考案された[成分分解法](https://ja.wikipedia.org/wiki/成分分解法 "wikilink")を基礎とする[LFM](../Page/LFM.md "wikilink")(Leniar Filtering Method)と呼ばれる[アルゴリズム](../Page/アルゴリズム.md "wikilink")群を持つオンメモリ型[DBMSエンジンである](../Page/データベース管理システム.md "wikilink")。

## 特性

**DAYDA.Laboo**はその特殊な[データ](../Page/データ.md "wikilink")構造（FASTと呼ばれる）により[インデックスや事前設計無しに多様な処理](../Page/索引.md "wikilink")（一括更新・[データ](../Page/データ.md "wikilink")変換・計算・[ソート](../Page/ソート.md "wikilink")・検索・集計・マッチング等）が非常に高速であり、特に大量[データ](../Page/データ.md "wikilink")の一括処理では絶大な効果を発揮する。\[1\]

その一方、一件処理を積み上げる逐次更新処理はさほど速くないとされる。\[2\]

このような特性から既存の[RDBMSをそのまま置き換えるものではなく](../Page/関係データベース管理システム.md "wikilink")、[データベース](../Page/データベース.md "wikilink")というより巨大[データ](../Page/データ.md "wikilink")の表計算を実現するデータ処理エンジンと評されている。

事前設計無しに自由にデータ構造を変更しながら[バッチ処理](../Page/バッチ処理.md "wikilink")を進めてゆく様は、表計算のテーブル操作に類似している。

## 高速な理由

これまでの一般的なデータ処理方法では処理に関係する全ての[データ](../Page/データ.md "wikilink")がアクセスされ、処理結果は処理に関係した全ての[データ](../Page/データ.md "wikilink")が移動もしくは書き換えられていた（[テーブルの](../Page/テーブル_\(情報\).md "wikilink")[ソート](../Page/ソート.md "wikilink")を考えると良い）。

[成分分解法](https://ja.wikipedia.org/wiki/成分分解法 "wikilink")に基づく[アルゴリズム](../Page/アルゴリズム.md "wikilink")では処理に関係する成分のみが選択的にアクセスされ、処理結果は変化した成分のみが書き換えられて記録される。

このことにより、処理の実施コストと処理結果の記録コストが圧倒的に小さいため高速になる。また何段階も処理が進行しても成分分解された状態は維持されるため、多段階処理でも高速性が失われない。

## データ構造の種類

**DAYDA.Laboo**に用いられた特殊なデータ構造（FASTと呼ばれる）は、テーブル、ツリーなどの処理対象データの形式と稼働環境が、一般的な[コンピュータ](../Page/コンピュータ.md "wikilink")か[グリッドなどの分散並列処理環境での](../Page/グリッド・コンピューティング.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")システムによってバリエーションがある。

同社は2006年現在、6種のFASTが開発済みと発表している。

## アプリケーション・インターフェース

  - 専用API(CのDLL,SO)\[3\]
  - 専用API([JNI](https://ja.wikipedia.org/wiki/JNI "wikilink")形式)\[4\]

| 言語タイプ | リモート接続API                                                          | サポートエンジンタイプ | サポートOSビット数          |
| ----- | ------------------------------------------------------------------ | ----------- | ------------------- |
| C用    | MICO(Mini [CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")) | 旧バージョンエンジン  | 32bit /64bit（Winのみ） |
| Java用 | [RMI](../Page/Java_Remote_Method_Invocation.md "wikilink")         | 新バージョンエンジン  | 32bit/64bit         |

サーバータイプとの接続方法

## ライセンス形態

  - MACアドレス依存型のパーマネントライセンス(128bit暗号化レベル)
  - MACアドレス非依存の使用期限設定ライセンス\[5\]

使用期限は、インストール後1ヶ月等では無く、ライセンスキー中の指定日付を超えると使用できなくなる有効期限形式

## 現バージョンでの制限事項

  - エンジンの処理できる文字コードは、エンジンが動いているOSの文字コードに依存する\[6\]
  - 通貨型データの取り扱いがサポートされていない\[7\]
  - 加減乗除等一般的な計算式は組み込まれているが、特殊な関数演算等複雑な計算は全て計算式API(calc)で行う

## 用途

以下の形で実績がある。

  - 大量データの[バッチ処理](../Page/バッチ処理.md "wikilink")エンジン
  - [バッチ処理](../Page/バッチ処理.md "wikilink")の中間及び最終結果に対して即座に対話型分析を行うシステムのエンジン
  - 高速にデータマートを作成できる巨大なセントラルウェアハウスのエンジン
  - システム移行に伴う[データ](../Page/データ.md "wikilink")の変換とクレンジングを行うツールのエンジン

### さらに応用できると思われる分野

  - 大量データ上での「名寄せ」\[8\]
  - [COBOL](../Page/COBOL.md "wikilink")から[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に置き換えが進む[バッチジョブツールのエンジン](../Page/バッチ処理.md "wikilink")\[9\]\[10\]

## 適用製品

### 関連製品

「[RH-BOM](http://www.plm4eco.org/technology/solution019.html)」「[Oh-Pa 1/3](http://www.bsc.fujitsu.com/services/ohpa/)」 「[karearea](http://www.sec.co.jp/products/karearea/)」 「[InfoFrame DataBooster](http://www.nec.co.jp/pfsoft/databooster/)」

### 取扱い製品

「DAYDA.LabooⅡ」 「[LIFIT](../Page/LIFIT.md "wikilink")ⅡJava Studio」 「[Aktblitz](../Page/Aktblitz.md "wikilink")Ⅱ」

## その他

**DAYDA.Laboo**(デイダ ラボー）及びその理論的基盤である[成分分解法](https://ja.wikipedia.org/wiki/成分分解法 "wikilink")は、2003年[日経BP](../Page/日経BP.md "wikilink")技術賞の情報通信部門賞を受賞している。

### 参考文献

  - [汎用超高速データベース処理技術](http://www.creage.ne.jp/app/BookDetail?isbn=4902721015)
  - [超高速DBアルゴリズムの超並列環境下のシミュレータ開発](https://www.ipa.go.jp/SPC/report/02fy-pro/report/818/paper.pdf)
  - [ＣＩＯのための「使えるＩＴ」Ｗｅｂ講座:ザ・ターボ、Oh-Pa1/3](http://memdb.typepad.jp/weblog/s23ohpa13/index.html)

### 最近のプレスリリース

  - [2007年](../Page/2007年.md "wikilink")[7月12日](../Page/7月12日.md "wikilink")、「[LIFIT](../Page/LIFIT.md "wikilink")ⅡJava Studio」「[Aktblitz](../Page/Aktblitz.md "wikilink")Ⅱ」を発表。
  - [2007年](../Page/2007年.md "wikilink")[8月31日](../Page/8月31日.md "wikilink")、64ﾋﾞｯﾄOS対応の[Redhat Linux版を発表](../Page/Red_Hat_Enterprise_Linux.md "wikilink")
  - [2007年](../Page/2007年.md "wikilink")[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")、[北陸先端科学技術大学院大学](../Page/北陸先端科学技術大学院大学.md "wikilink")と汎用[超高速データベース](../Page/超高速データベース.md "wikilink")処理技術に関する共同研究を開始。

## 脚注

<div class="references-small">

<references />

</div>

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink")

1.  [RDBMSに比べて](../Page/関係データベース管理システム.md "wikilink")500-700倍(他社製品と比べても20-30倍程度性能差がある)
2.  列単位で情報を管理している為
3.  [Aktblitz](../Page/Aktblitz.md "wikilink")では直接API呼び出しを禁止するライセンス形態もあり
4.  javaインターフェース越しに上記のCのDLL,SOを呼び出す形式
5.  主に体験版・貸出用ライセンス
6.  WindowsならMS932,RedHatならUTF-8
7.  現在サポートされている型は数値,浮動小数点,日付/時刻/日付時刻,文字列<文字数制限有>)
8.  社会保険納付者の突合せなどには最適。
9.  [Redhat Linux版](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[Aktblitz](../Page/Aktblitz.md "wikilink")IIをそのまま使う選択肢もあり
10. ただし別途COBOL2Macro等のコンバータ対応が必要