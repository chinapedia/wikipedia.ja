> この記事は[SMIT](https://ja.wikipedia.org/wiki/SMIT)から翻訳されています。


**SMIT**（System Management Interface Tool）は、[IBM](../Page/IBM.md "wikilink")の[AIX](../Page/AIX.md "wikilink")でのメニューベースの[システム管理](../Page/システム管理.md "wikilink")（特に[構成管理](../Page/構成管理.md "wikilink")）ツール。

## 特徴

  - 2つの操作モード（テキストとグラフィカル）がある。
  - 対話型、メニュー方式のインタフェース
  - ユーザー補助機能
  - システム管理活動の[ロギング](https://ja.wikipedia.org/wiki/ロギング "wikilink")
  - システム管理タスクへの高速パス
  - SMIT画面をユーザー定義可能

## 操作モード

SMIT はテキストモードと [X Window System](../Page/X_Window_System.md "wikilink") 上のグラフィカルモードがある。一般にどこでも使えるテキストモードの方が好まれる。テキストモードで起動するには、`smitty` または `smit -a` とコマンド入力する。グラフィカルモードで起動するには、`msmit` または `smit -m` とコマンド入力する。単に `smit` と入力すると、自動的に入力端末がグラフィカル機能を持つかどうかを判断し、可能ならばグラフィカルモードで起動する。

## エンドユーザインタフェース

SMIT は対話型メニュー方式の[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を持ち、[AIX](../Page/AIX.md "wikilink")における日々のシステム管理が容易に行えるよう設計されている。システム管理業務は分類され、一連のメニュー、セレクター、ダイアログ画面で表示される。例えば、一般的なソフトウェアインストール作業は Software Installation and Management に分類されている。

選択したタスクを実行中の場合、画面には `RUNNING` というメッセージが表示される。タスクが終了すると `OK` または `FAILED` というメッセージで結果を知らせる。グラフィカルモードでは、タスク実行中は人間が走っている様子をアニメーション表示する。タスクが成功するとその人間が飛び跳ねて喜び、失敗するとうなだれる。

SMIT 画面にはシステムの実際の構成が表示できる。その内容はインストールされているものによって異なる。また、カスタマイズも可能となっている。デバイス画面では、デバイスの種類（ネットワーク、ストレージアダプター、ディスクドライブなど）毎に適用可能なシステム管理タスクが選択できるようになっている。

## 関連項目

  - [AIX](../Page/AIX.md "wikilink")
  - 他の[Unix系](../Page/Unix系.md "wikilink")システム上の同様の機能を持つツール
      - [linuxconf](https://ja.wikipedia.org/wiki/linuxconf "wikilink")
      - [Webmin](../Page/Webmin.md "wikilink")
      - [YaST](https://ja.wikipedia.org/wiki/YaST "wikilink")

## 外部リンク

  - [System Management Interface Tool (SMIT)](http://www-03.ibm.com/servers/aix/products/aixos/whitepapers/smit.html)

[Category:ユーザインタフェース](https://ja.wikipedia.org/wiki/Category:ユーザインタフェース "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")