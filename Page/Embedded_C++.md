> この記事は[Embedded C++](https://ja.wikipedia.org/wiki/Embedded_C++)から翻訳されています。


**Embedded C++**（エンベデッドシープラスプラス、エンベッディドシープラスプラス）は[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一種である。EC++と略記される。

## 特徴

[1990年代](../Page/1990年代.md "wikilink")後半、組み込み用途への適用を目指して、肥大化した[C++](../Page/C++.md "wikilink")の仕様を必要最低限のものに絞り込んだサブセットが考案された。

一般的には、Embedded C++を用いた場合、C++より[プログラムをコンパクトにできる傾向がある](../Page/プログラム_\(コンピュータ\).md "wikilink")。これは主に[例外処理](../Page/例外処理.md "wikilink")や[実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")に関わる[ランタイムと](../Page/ランタイムライブラリ.md "wikilink")[データ](../Page/データ.md "wikilink")が減少するためである。

C++から削減された機能

  - [テンプレート](../Page/テンプレート_\(プログラミング\).md "wikilink")
  - [例外処理](../Page/例外処理.md "wikilink")
  - [実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")
  - [多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")
  - [名前空間](../Page/名前空間.md "wikilink")
  - [ワイド文字](../Page/ワイド文字.md "wikilink")ライブラリ
  - 新しい[型変換](../Page/型変換.md "wikilink")の[演算子](../Page/演算子.md "wikilink")（const_cast, dynamic_cast, reinterpret_cast, static_cast）
  - mutable（const修飾の付いた[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")の[メンバ変数を変更可能にする](../Page/フィールド_\(計算機科学\).md "wikilink")）

C++のサブセットという位置付けから、Embedded C++で記述された[ソースコード](../Page/ソースコード.md "wikilink")がそのままC++でも利用できることを目指したが、その目標は必ずしも達成されていない。

C++との互換性を妨げる要因には以下のものがある。

  - 名前空間がサポートされないため、シンタックス（文法）が統一できない。具体的には、size_t型を使う場合に、C++ではstd::size_tと記述し、Embedded C++では単にsize_tと記述しなければならない。
  - 例外処理をサポートしないため、Embedded C++で記述されたプログラムは[例外安全](https://ja.wikipedia.org/wiki/例外安全 "wikilink")に配慮されていないが、C++ではそうした設計には問題がある。
  - 組み込み用途ということから、[フリースタンディング環境](../Page/フリースタンディング環境.md "wikilink")を対象とすることになるが、Embedded C++にはC++のフリースタンディング環境ではサポートされないライブラリ機能が多く存在する。

## 外部リンク

  - [Embedded C++ Homepage](http://www.caravan.net/ec2plus/)

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")