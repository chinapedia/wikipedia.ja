> この記事は[Common User Access](https://ja.wikipedia.org/wiki/Common_User_Access)から翻訳されています。


**Common User Access** (**CUA**) は[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) と[コンピュータプログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) についての標準である。CUA は [IBM](../Page/IBM.md "wikilink") によって開発され、同社の[Systems Application Architectureの一部として](../Page/Systems_Application_Architecture.md "wikilink")[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に公開された。

もともとは [OS/MVS](../Page/Multiple_Virtual_Storage.md "wikilink")、[VM/CMS](https://ja.wikipedia.org/wiki/z/VM "wikilink")、[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") や [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") といったOSで用いられ、CUA標準の一部は種々の[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")を含むそれ以外のOS用のプログラムでも実装されている。[Java AWT](../Page/Abstract_Window_Toolkit.md "wikilink") や [Swing](../Page/Swing.md "wikilink") でも用いられている。

## 目的と動機

CUAの仕様は詳細にわたっており、[アプリケーションの見た目や機能について厳しい規則を設定していた](../Page/アプリケーションソフトウェア.md "wikilink")。その目的の一部は、当時個別に異なるユーザインタフェースを実装していた[DOSアプリケーション間の調和をもたらすことであった](../Page/DOS_\(OS\).md "wikilink")。

例：[ファイルを開く場合のキー操作は](../Page/ファイル_\(コンピュータ\).md "wikilink")

  - [WordPerfect](https://ja.wikipedia.org/wiki/WordPerfect "wikilink"):\[F7\] - \[3\]
    [Lotus 1-2-3](../Page/Lotus_1-2-3.md "wikilink"):\[/\] (メニューを開く) - \[W\] (ワークスペース) - \[R\] (取り出し)
    [Microsoft Word](../Page/Microsoft_Word.md "wikilink"):\[Esc\] (メニューを開く) - \[T\] (転送) - \[L\] (読み出し)
    [WordStar](../Page/WordStar.md "wikilink"):\[Ctrl\]+\[K\]+\[O\]
    [emacs](https://ja.wikipedia.org/wiki/emacs "wikilink"):\[Ctrl\]+\[x\] その後 \[Ctrl\]+\[f\] (find-file 機能)

また\[ESC\]は、プログラムによって動作のキャンセルに用いるものもあり、動作を完了させるために用いるものもあった。[WordPerfect](https://ja.wikipedia.org/wiki/WordPerfect "wikilink")では\[ESC\]を文字の繰り返しに用いた。\[End\]を行末への移動に用いるものもあり、フォームへの入力を完了するために用いるものもあった。ヘルプは \[F1\] であることが多かったが、WordPerfect では\[F3\]であった。\[Ins\]は文字の挿入と上書きの切り替えに使う物と、「貼り付け」に使うものとがあった。

このように、それぞれのプログラムはそれぞれ別々に学習する必要があり、UIをすべて記憶している必要があった。新しいプログラムに接する初心者は、これまでの同様のアプリケーションについての知識が全く無意味であると気づいてしまうため、何十ものアプリケーションのUIを学習しておく必要があることを意味した。

CUAの詳細にわたる仕様には、[アップルコンピュータによって惜しげもなく精緻に書かれた](../Page/アップル_\(企業\).md "wikilink")[Human Interface Guidelines](https://ja.wikipedia.org/wiki/Human_Interface_Guidelines "wikilink") (HIG) から発想したと思しき部分もある。HIGは[Macintosh](../Page/Macintosh.md "wikilink")向け[ソフトウェア](../Page/ソフトウェア.md "wikilink")の見た目や機能を正確に定めた仕様書である。初めてこれが書かれたときMacintoshは生まれたばかりで、GUIソフトウェアは新しく、アップルはプログラムが統一された[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")に従うよう、非常な苦労をしたのである。CUA は同様な目的を持っていたが、繁栄しているものの混沌とした既存の業界にルールを押し付けるというさらに難しい課題に直面した。

## 記述内容

CUAは、[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")や、[メニュー](../Page/メニュー_\(コンピュータ\).md "wikilink")、[キーボードショートカットといった要素の操作についての標準を含んでおり](../Page/ショートカットキー.md "wikilink")、CUAを全く読んだことのない多数の[プログラマ](../Page/プログラマ.md "wikilink")によって、今日でも実装されるほど大きな影響力を持つようになった。

こうした標準の一部は、Windowそのものや、[MS-DOS](../Page/MS-DOS.md "wikilink") 5のフルスクリーンテキストエディタEDITのようなDOSベースのアプリケーションでも見ることができる。CUAの特徴としては 下記のようなものがある。

  - すべてのアプリケーションは、[マウスと](../Page/マウス_\(コンピュータ\).md "wikilink")[キーボードのいずれでも操作できなければならない](../Page/キーボード_\(コンピュータ\).md "wikilink")
  - メニューは、\[F10\] により選択されたり非選択になったりする。
  - メニューは [Altキー](https://ja.wikipedia.org/wiki/Altキー "wikilink")と、メニューの名前の中の下線の引かれた文字を押すことで開く。
  - パラメータが必要なメニューのコマンドには、[リーダーがつく](../Page/リーダー_\(記号\).md "wikilink")。
  - オプションの要求する場合には、二番目のウィンドウを用いる (よくダイアログボックスと呼ばれるもの）。
  - オプションは、ノートのタブを用いてセクションに分割される。
  - ダイアログボックスのフィールド内の移動はカーソルキーで行う。フィールド間の移動は[Tabキーを押すことで行う](../Page/タブキー.md "wikilink")。\[Shift\]+\[Tab\]で戻る。
  - ダイアログボックスは、\[\[Escキー|\[ESC\]キー\]\]を押すと選択され、変更を破棄する"キャンセル"ボタンと、\[Return\]キーを押すと選択され、変更を受け付ける'OK'ボタンを持つ。
  - アプリケーションは、メニューバーの最後の位置にあるHelpメニューからアクセスできる[オンラインヘルプ](https://ja.wikipedia.org/wiki/オンラインヘルプ "wikilink")を持ち、コンテキストを意識したヘルプは\[F1\]で呼び出すことができる。
  - 最初のメニュー項目は'File'と呼ばれファイルを操作する命令（新規、開く、保存、別名保存）や、プログラム終了の命令を含み、'Edit'メニューは取り消し、やり直し、切り取り、削除、[貼り付け](https://ja.wikipedia.org/wiki/貼り付け "wikilink")コマンドを含む。
  - '切り取り'コマンドは\[Shift\]+\[Del\]、コピーは\[Ctrl\]+\[Ins\]、貼り付けは\[Shift\]+\[Ins\]である。
  - ウインドウのサイズは、8方向の境界の一つをドラッグすることで変更できる。

CUAはDOSアプリケーションをカバーするだけでなく、OS/2のテキストモードと[Presentation Manager両方のGUIや](https://ja.wikipedia.org/wiki/Presentation_Manager "wikilink")、[Systems Application Architectureに準拠した](../Page/Systems_Application_Architecture.md "wikilink") IBMの[メインフレーム](../Page/メインフレーム.md "wikilink")同様、WindowsのConsistent User Interface標準 (CUI) の基礎となった。

CUAは単に DOSアプリケーションを合理的なものにする試み以上のものであり、[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")からメインフレームまでの IBMのコンピュータの範囲全体のソフトウェアと[ハードウェア](../Page/ハードウェア.md "wikilink")の機能をまとめて、合理的にものにし、調和させようとする大規模な計画の一部であった。おそらく、完全には成功しなかった理由の一部はこれであろう。

CUAの第3版は、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[ワークプレース](https://ja.wikipedia.org/wiki/ワークプレース "wikilink")を導入し、最初の2版から、急進的な飛躍を遂げた。第3版ではユーザーの操作において注目する点を、ユーザーが操作する文書や画像などといった[データ中心](https://ja.wikipedia.org/wiki/データ中心 "wikilink")に切り替えた。これまでの[アプリケーション中心](https://ja.wikipedia.org/wiki/アプリケーション中心 "wikilink")の注目点は、（プログラムを操作してドキュメントの作業するのではなく）プログラムを使ってドキュメント上で作業するというユーザーの期待に応え、コンピュータをより使いやすくする意図で、削除された（[オブジェクト指向ユーザインタフェース](https://ja.wikipedia.org/wiki/オブジェクト指向ユーザインタフェース "wikilink")参照）。

## CUAの影響

CUAはWindowsオペレーティングシステムにおいて、その初期の開発段階で強い影響を与えた。Windows 3.0のGUIはCUA '87準拠である。しかしWindows 3.1から[ショートカットキー](../Page/ショートカットキー.md "wikilink")がMacintosh風に変更された。そして[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")の[Windows 95のリリース以降はGUI全体も](../Page/Microsoft_Windows_95.md "wikilink")、WindowsはCUAの設計から離れていった。酷評されつつも[スタートメニュー](https://ja.wikipedia.org/wiki/スタートメニュー "wikilink")が導入され、CUA '91で採用されたオブジェクト指向デスクトップを重視することはなくなった。CUAで仕様化された基本的な[GUIウィジェットの標準キーストロークは](../Page/ウィジェット_\(GUI\).md "wikilink")、Windowsの1つの機能として残った。

## 参考文献

  - IBM, Systems Application Architecture: Common User Access: Panel Design and User Interaction, Document SC26-4351-0, [1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink").
  - IBM, Systems Application Architecture: Common User Access: Advanced Interface Design Guide, Document SC26-4582-0, [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink").
  - IBM, Systems Application Architecture: Common User Access: Basic Interface Design Guide, Document SC26-4583-0, [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink").
  - IBM, Systems Application Architecture: Common User Access: Guide to User Interface Design, Document SC34-4289-00 [1991年](../Page/1991年.md "wikilink")
  - IBM, Systems Application Architecture: Common User Access: Advanced Interface Design Reference, Document SC34-4290-00 [1991年](../Page/1991年.md "wikilink")

## 外部リンク

  - , by [Richard E. Berry](https://ja.wikipedia.org/wiki/Richard_E._Berry "wikilink"), [IBM Systems Journal](https://ja.wikipedia.org/wiki/IBM_Systems_Journal "wikilink"), Volume 27, Nº 3, 1988. [Citations](http://portal.acm.org/citation.cfm?id=49492.49495).

  - [The evolution of the Common User Access Workplace Model - Technical](http://findarticles.com/p/articles/mi_m0ISJ/is_n3_v31/ai_12547724), by Richard E. Berry, [Cliff J. Reeves](https://ja.wikipedia.org/wiki/Cliff_J._Reeves "wikilink"), IBM Systems Journal, September 1992. . [Citations](http://portal.acm.org/citation.cfm?id=137392.137393)

  - [The designer's model of the CUA workplace - Common User Access - Technical](http://findarticles.com/p/articles/mi_m0ISJ/is_n3_v31/ai_12547726), by Richard E. Berry, IBM Systems Journal, September 1992.

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:ユーザインタフェース](https://ja.wikipedia.org/wiki/Category:ユーザインタフェース "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink")