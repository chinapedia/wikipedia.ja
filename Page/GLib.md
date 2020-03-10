> この記事は[GLib](https://ja.wikipedia.org/wiki/GLib)から翻訳されています。


**GLib** とは、[C言語](../Page/C言語.md "wikilink")で書かれた[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[ユーティリティライブラリの一種である](../Page/ライブラリ.md "wikilink")。[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")プロジェクトの一部としてスタートしたが、現在では他のアプリケーションでも使われている。当初は低レベルなコードを入れるためのライブラリとされていたが、現在では[プラットフォーム間の差異を吸収する機能も加えられ](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、異なる[CPU](../Page/CPU.md "wikilink")、[OS間でのアプリケーションの移植性を確保するライブラリとしても利用されている](../Page/オペレーティングシステム.md "wikilink")。

## 機能

GLib に含まれる代表的な機能としては、以下のものがある。

  - 基本的な[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")とその上下限値の定義
      - [型変換](https://ja.wikipedia.org/wiki/型変換 "wikilink")
      - [エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")変換
  - 標準[マクロ](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")
  - [動的メモリ確保](https://ja.wikipedia.org/wiki/動的メモリ確保 "wikilink")
  - 警告、[アサーション](https://ja.wikipedia.org/wiki/表明 "wikilink")
  - メッセージ[ロギング](https://ja.wikipedia.org/wiki/ロギング "wikilink")
  - [タイマー](https://ja.wikipedia.org/wiki/タイマー "wikilink")
  - [文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")操作
      - [文字コード](../Page/文字コード.md "wikilink")変換
      - 簡易[XMLパーサ](../Page/Extensible_Markup_Language.md "wikilink")
      - 正規表現
      - [字句解析](../Page/字句解析.md "wikilink")スキャナ
  - [gettext](https://ja.wikipedia.org/wiki/gettext "wikilink")による国際化
  - [擬似乱数](../Page/擬似乱数.md "wikilink")生成
  - [フック関数](../Page/フック_\(プログラミング\).md "wikilink")
  - [プラグイン](../Page/プラグイン.md "wikilink")モジュールの動的ローディング
  - [スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")
  - [メモリプール](https://ja.wikipedia.org/wiki/メモリプール "wikilink")
  - 文字列の[自動補完](https://ja.wikipedia.org/wiki/自動補完 "wikilink")
  - [型システム](https://ja.wikipedia.org/wiki/型システム "wikilink") [GType](https://ja.wikipedia.org/wiki/GType "wikilink")
  - [オブジェクトシステム](../Page/オブジェクト指向プログラミング.md "wikilink") [GObject](https://ja.wikipedia.org/wiki/GObject "wikilink")
  - [Windowsにおける](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[UNIX](../Page/UNIX.md "wikilink")向けプログラムとの互換機能

## データ構造

頻繁に利用されるデータ構造とそれに対する操作が定義されている。以下に主なものを列挙する。

  - メモリチャンク
  - 双方向および片方向[線形リスト](https://ja.wikipedia.org/wiki/線形リスト "wikilink")
  - [連想配列](../Page/連想配列.md "wikilink")（[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")方式の実装）
  - 可変長文字列
  - [可変長配列](https://ja.wikipedia.org/wiki/可変長配列 "wikilink")
  - 文字列チャンク（文字列のグループ）
  - [動的配列](https://ja.wikipedia.org/wiki/配列#動的配列 "wikilink")
  - [平衡2分探索木](https://ja.wikipedia.org/wiki/平衡2分探索木 "wikilink")
  - N分[木](../Page/木構造_\(データ構造\).md "wikilink")
  - quarks（文字列とユニークな整数識別子を対応付けるもの）
  - keyed data lists（文字列や整数識別子でアクセス可能なデータ要素群）
  - リレーションと[タプル](https://ja.wikipedia.org/wiki/タプル "wikilink")
  - [構造体](../Page/構造体.md "wikilink")の[キャッシュ](../Page/キャッシュ.md "wikilink")

## 外部リンク

  - [GLib リファレンスマニュアル](https://developer.gnome.org/glib/stable/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:GTK+](https://ja.wikipedia.org/wiki/Category:GTK+ "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink")