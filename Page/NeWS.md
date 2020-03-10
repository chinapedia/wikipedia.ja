> この記事は[NeWS](https://ja.wikipedia.org/wiki/NeWS)から翻訳されています。


**NeWS**（*Network extensible Window System*）は、1980年代中ごろに[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が開発した[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")\[1\]。古くは "SunDew" と呼ばれ\[2\]、後に[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を設計した[ジェームズ・ゴスリン](https://ja.wikipedia.org/wiki/ジェームズ・ゴスリン "wikilink")が主任アーキテクトとして設計に当たった。NeWS インタプリタは [PostScript](../Page/PostScript.md "wikilink") に基づいている（後の [Display PostScript](../Page/Display_PostScript.md "wikilink") に似ているが、2つのプロジェクトに関係はない）。

NeWS はプリンタとは違って、複数の PostScript プログラムによって生成されたウィンドウ群を同時に画面に表示するため、PostScript インタプリタを[マルチタスク](../Page/マルチタスク.md "wikilink")化するところから出発した。また、*canvases* と呼ばれる表示域に基づいた完全な表示階層システムを追加した。多くの[GUIのビューシステムと同様](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、表示の[木構造の概念があり](../Page/木構造_\(データ構造\).md "wikilink")、それにしたがってイベントが渡される。NeWS には、タイマや他の自動イベント、[マウスと](../Page/マウス_\(コンピュータ\).md "wikilink")[キーボードなどのデバイスの入力キュー](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")、その他の対話処理に必要な機能など、完全なイベントのモデルが構築されている。

特に興味深いのは、[継承を伴う完全な](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")スタイルが追加されていた点である。このため、アプリケーション構築に外部のオブジェクト指向言語を必要としなかった。

これらの追加機能は全て PostScript への拡張として実装されたため、単純な PostScript のコードを書くだけで、ウィンドウを表示するインタラクティブなプログラムとして動作させることができた。よく知られたデモとして、約2ページのコードでできた時計のアプリケーションと、視線でカーソルを追いかける一対の目玉を描くプログラムがあった。目玉のプログラムは1988年の[SIGGRAPH](https://ja.wikipedia.org/wiki/SIGGRAPH "wikilink")で展示され、後に登場した有名な [X Window System](../Page/X_Window_System.md "wikilink") のアプリケーション [xeyes](https://ja.wikipedia.org/wiki/xeyes "wikilink") に影響を与えた。

NeWS にはユーザインタフェースの要素（[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")）のライブラリがいくつか含まれており、それら自身も NeWS で書かれていた。これらのウィジェットは NeWS インタプリタによって実行され、ウィジェットが要求したときだけ外部プログラム（または他のNeWSコード）と通信が必要になるだけである。例えば、トグル[ボタンの表示ルーチンはボタンが押されているかどうかの状態を問い合わせることができ](https://ja.wikipedia.org/wiki/ボタン_\(GUI\) "wikilink")、それに従って表示を変化させる。ボタンの PostScript コードは、マウスのクリックに反応することもできる。これらは全てウィンドウサーバ内でクライアントプログラムとやり取りせずに行われ、ボタンの上でマウスがリリースされたときだけ制御のためのイベントが送られる。

これは、[X Window System](../Page/X_Window_System.md "wikilink") のサーバモデルよりも洗練されている。X の場合、「マウスのボタンがここで押下された」、「マウスの現在位置はここ」、「マウスのボタンがここでリリースされた」といったイベントがクライアントに送られ、クライアント側でそれがボタンに関わるイベントかどうかを判断し、状態を変更し、新たな状態の描画をサーバに要求する。クライアントとサーバが同じマシンにない場合、これらのやり取りがネットワーク上を行き来し、性能が低下する。

そのようなライブラリの好例として TNT (*The NeWS Toolkit*) が1989年、サンによってリリースされた。サンは例として示すためにもっと小さいツールキットもリリースした。

NeWS は広く採用されることはなかったが、いくつかの企業がライセンスを受け、様々な用途に利用した。[SGIはこれを](../Page/シリコングラフィックス.md "wikilink") 4Sight と名づけ、従来使っていた独自の IRIS GL というウィンドウシステムの後継とした。NeWS 上で動作する数少ない商用製品としては、Frame Technology Corp. が開発した[DTP](../Page/DTP.md "wikilink")ソフトである [FrameMaker](../Page/Adobe_FrameMaker.md "wikilink") の [OPEN LOOK](https://ja.wikipedia.org/wiki/OPEN_LOOK "wikilink") 版がある。その開発には[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")と[NSAが資金提供していた](../Page/アメリカ国家安全保障局.md "wikilink")。また、 Arthur van Hoff の開発した HyperLook は対話型アプリケーション設計システムであった\[3\]。

自由に利用可能な X11 が既に一般化しつつあったため、NeWS の最初のバージョンでは呼び出しを NeWS PostScript に変換することで X11 をエミュレートしていた。性能に問題があり、X11 の正確なピクセル結果に依存しているプログラムがあったことから、サンはXサーバとインタプリタを並行動作させるハイブリッド型の [Xnews](https://ja.wikipedia.org/wiki/OpenWindows "wikilink") をリリースした。無理な統合をしたため、NeWS インタプリタの性能は大幅に低下し、Xサーバもよい実装とは言えなかった。サンはまた OPEN LOOK の[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")を実装した2種類のツールキットを開発している。1つは [OLIT](https://ja.wikipedia.org/wiki/OLIT "wikilink") であり、[Motif](../Page/Motif_\(GUI\).md "wikilink") と同様に [Xt](https://ja.wikipedia.org/wiki/Intrinsics "wikilink") (X Intrinsics) を使っている。もう1つは [XView](https://ja.wikipedia.org/wiki/XView "wikilink") で、サンの以前のウィンドウシステム [SunView](https://ja.wikipedia.org/wiki/SunView "wikilink") と同じ[APIを実装していた](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

OPEN LOOK が Motif に敗北したことが明らかになり、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")が FrameMaker を取得すると、NeWS 上のアプリケーション製品は皆無となった。現在では多くの[UNIX](../Page/UNIX.md "wikilink")システムが（サンの製品も含め） X Window System を使っている。

## 失敗の原因

NeWS の設計は色々な意味で[シンクライアント](https://ja.wikipedia.org/wiki/シンクライアント "wikilink")向きであり、ディスプレイ側に多くの処理を移動でき、クライアントプログラムの意味論からGUIの意味論を分離できる。PostScript の描画モデルを採用していたため、他のグラフィックスAPIよりもはるかに使い易くて強力である。従って、誰もが成功を信じて疑わなかった。

NeWS が市場に受け入れられなかった理由としては、以下のようなことが挙げられる。

  - NeWS を使うにはサンからライセンスを受ける必要があり、一方 X Window System は [MIT Licenseでソースコードが配布されていた](https://ja.wikipedia.org/wiki/MIT_License "wikilink")。NeWS ライブラリを使った製品を出荷する場合、サン、[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")、[パロアルト研究所](https://ja.wikipedia.org/wiki/パロアルト研究所 "wikilink")に対してライセンス料を支払う必要があった。
  - X Window System の勝利が明らかとなるころまで、NeWS には頑健な再利用可能コードのライブラリが存在しなかった。サンは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ではこの過ちを繰り返さなかった。問題をさらに悪化させたのは、サンが様々な種類のウィジェットセットを提供して開発者を混乱させた点である。
  - PostScript は[後置記法とスタックをベースとしていて](../Page/逆ポーランド記法.md "wikilink")、数式を記述するのが苦手な言語である。これは印刷では問題ではないが、ユーザインタフェースでは例えば、スライダーからどれだけ下の位置でマウスがクリックされたかなどを計算する必要があり、数式が重要だった。[C言語](../Page/C言語.md "wikilink")風の構文のコンパイラがいくつか登場したが（pdb、c2ps など）、これらは使いにくく、サンがサポートしたものでもなかった。
  - NeWS でアプリケーションを開発する場合、クライアント側とサーバ側を全く異なるプログラミング言語で書く必要があり、しかもそれらの間で非同期な通信が行われる。この通信の調整は難しいが、サンは若干のサポートしか提供していなかった。
  - NeWS のウィンドウサーバは競合する他のウィンドウシステムほど安定した実装になったことがない。NeWS と X11 のマージで事態はさらに悪化し、またそれと同時にリリースされた [Solaris](../Page/Solaris.md "wikilink") 2 にも性能問題が存在していた。
  - 経営陣は、X11 とどう対抗していったらいいか、NeWS に適した市場はどこかについて混乱していた。

NeWS と [Display PostScript](../Page/Display_PostScript.md "wikilink") (DPS) を比較すると、どちらも同じイメージングモデルと言語を基にしていながら、その手法は大きく異なる。DPSでは PostScript のコマンドは描画でのみ使用され、他の操作（ウィンドウ生成など）は別にシステムインタフェースとして実装されていた。DPS には NeWS のような面白い機能（例えば、PostScript コードでウィンドウの形状を描くなど）はなく、低レベルな [Xlib](https://ja.wikipedia.org/wiki/Xlib "wikilink") ライブラリを必要とし、DPS と X の調整のための扱いにくいグルーコードを必要としていた。しかし、そのためにDPSのコードの大部分はインタプリタで解釈実行されるのではなくコンパイルして実行されるので、作成とデバッグが容易で高速に動作した。結果として NeWS のように PostScript に基づいた表示であってもエンジン部分はかなり小さくなり、高速化され、「自然」なプログラミング環境になっていた。

## 脚注

## 外部リンク

  - [a short description of NeWS](http://starynkevitch.net/Basile/NeWS_descr_oct_1993.html)
  - [The NeWS eyeball program](http://groups.google.co.uk/group/comp.windows.news/msg/2adcf09ada55201d?dmode=source)

[Category:ウィンドウシステム](https://ja.wikipedia.org/wiki/Category:ウィンドウシステム "wikilink") [Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")

1.
2.
3.  [HyperLook (aka HyperNeWS (aka GoodNeWS))](http://www.art.net/studios/Hackers/Hopkins/Don/hyperlook/index.html)