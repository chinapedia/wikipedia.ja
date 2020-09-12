> この記事は[Redux \(JavaScriptライブラリ\)](https://ja.wikipedia.org/wiki/Redux_\(JavaScriptライブラリ\))から翻訳されています。


**Redux**は、アプリケーションの[状態](../Page/状態.md "wikilink")管理のための[オープンソースの](../Page/オープンソースソフトウェア.md "wikilink")[JavaScriptライブラリ](https://ja.wikipedia.org/wiki/JavaScriptライブラリ "wikilink")である。[ユーザーインターフェイスを構築するために](../Page/ユーザインタフェース.md "wikilink")、[React](https://ja.wikipedia.org/wiki/React "wikilink")や[Angular](https://ja.wikipedia.org/wiki/Angular "wikilink")などのライブラリで最もよく使用される。Facebookの[Fluxアーキテクチャの影響を受けて](https://ja.wikipedia.org/wiki/React#Fluxアーキテクチャの使用 "wikilink")、Dan AbramovとAndrew Clarkによって作成された。

## 概要

Reduxは、アプリケーションの状態を予測できるコンテナになるように設計された、シンプルで限定的なAPIを備えた小さなライブラリである。[関数型プログラミングの概念である](../Page/関数型言語.md "wikilink")[reduce関数と同様に動作する](https://ja.wikipedia.org/wiki/高階関数#fold "wikilink")。

[関数型プログラミング言語](../Page/関数型言語.md "wikilink")[Elmの影響を受けている](https://ja.wikipedia.org/wiki/Elm_\(プログラミング言語\) "wikilink")\[1\]。

## 歴史

Reduxは、2015年にDan AbramovとAndrew Clarkによって作成された。Abramovは、React Europe\[2\]でのホットリロードに関するカンファレンストーク\[3\]の用意をしながら、最初のReduxの実装を開始した。Abramovは、「私はロジックが変更できるFluxのコンセプトを証明しようとした。そして、それは私にタイムトラベルをさせる。そして、それは私にコードの変更に対する未来のアクションを再適用させるだろう」と発言している\[4\]。

Abramovは、reduce関数とFluxパターンの類似性に心を打たれた。「私はFluxを時間の経過に伴うreduce操作と考えていた... ストアは、これらの行動に反応して状態を蓄積する。これをさらに進めることを考えていた。Fluxストアがストアではなく、reduce関数だった場合はどうなるか？」\[5\]

Abramovは、Andrew Clark（Fluxの実装であるFlummoxの作者）に協力者として連絡を取った。とりわけ、彼はツールのReduxエコシステムを可能にし、[ミドルウェア](../Page/ミドルウェア.md "wikilink")やストアエンハンサーなどの拡張ポイントを実装する一貫した[APIの作成を支援したことで](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Clarkの功績を認めている\[6\]。

2019年2月、useReducerは16.8リリースで[React](https://ja.wikipedia.org/wiki/React "wikilink")フックとして導入された。Reduxと一貫性のあるAPIを提供し、開発者がコンポーネントの状態にローカルなReduxのようなストアを作成できるようする\[7\]。

## 脚注

## 外部リンク

  -
  - [GitHub](https://github.com/reduxjs/redux)

[Category:フリーソフトウェアとオープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアとオープンソースソフトウェア "wikilink") [Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink")

1.
2.
3.
4.
5.
6.
7.  [React v16.8: The One with Hooks](https://reactjs.org/blog/2019/02/06/react-v16.8.0.html#react-1)