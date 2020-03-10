> この記事は[Display PostScript](https://ja.wikipedia.org/wiki/Display_PostScript)から翻訳されています。


**Display PostScript** (**DPS**) は、画面上の表示システムである。名前が示すとおり、Display PostScriptは[PostScript](../Page/PostScript.md "wikilink") (PS) のイメージモデルと言語を使って画面上のグラフィックスを生成する。

[NeXT](../Page/NeXT.md "wikilink")の一連の[UNIX](../Page/UNIX.md "wikilink")ベースのコンピュータで表示システムとして採用された。当初のバージョンは[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")が開発したが、Display PostScriptの完全実装はNeXTが主体となってアドビの協力を得て行った。NeXTの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")以外ではアドビが独自に標準化し、ライセンス条件を設定して製品化している。

## PostScriptからの変更点

対話機能をサポートし、画面表示に耐えうる性能にするため、以下のような変更が加えられた。

  - 複数実行コンテクスト
    逐次的に処理されるプリンタの場合とは異なり、DPSは複数の[ウィンドウ](../Page/ウィンドウ.md "wikilink")を同時に表示し、それぞれのウィンドウに様々な設定がある。そのため、ウィンドウ毎（プロセス毎）にコンテクスト（状態データのセット）をアクティブに保持するよう修正された。
  - 名前の符号化
    PostScriptでは、プロシージャやデータ構造の多くは名前で参照される。DPSでは名前を数値に置き換えて、参照を高速化した。
  - 対話機能サポート
    [当たり判定](https://ja.wikipedia.org/wiki/当たり判定 "wikilink")のような機能など、対話の制御のためのプロシージャが定義された。
  - ハーフトーン・フェーズ
    [スクロール](../Page/スクロール.md "wikilink")性能を向上させるため、DPSでは新たに見える部分だけを描画し、それ以外の部分はすでにある画像データを再描画せずにシフトさせている。しかし、そのために[ハーフトーンがうまく整わず](../Page/網点.md "wikilink")、画像に不要な線や矩形が見えるようになる。DPSはハーフトーンを整えるコードを追加している。ただし、最近のフルカラーのディスプレイではハーフトーンを使うことはないため、この技術は現在ではあまり重要ではない。
  - インクリメンタル・アップデート
    PSコードを解釈して印刷する場合、`showpage`に到達して初めて印刷が行われる。しかし、常に細かい更新が必要なディスプレイでは、この方式は不適切である。DPS では、ユーザープログラムから命令を受け取る度にほぼリアルタイムに描画するモードを追加した。
  - ビットマップフォントのサポート
    DPSでは、PS[フォント](../Page/フォント.md "wikilink")をビットマップフォントにマップし、その場で変換する機能が追加されている。PSのフォントは低解像度の機器で主にうまく機能するが、ここでいう「低解像度」とは300[dpi](https://ja.wikipedia.org/wiki/dpi "wikilink")程度のことであり、NeXTの画面の96dpiではない。その場合はビットマップフォントの方がよい出力が得られる。
  - プログラミング言語サポート
    DPSでは、"`pswrap`" という概念が導入された。これはPostScriptコードを[C言語](../Page/C言語.md "wikilink")の関数内に組み込み、アプリケーションから呼び出せるようにしたものである。

なお、DPSには[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")は組み込まれていない。ウィンドウシステムは別途実装する必要があり、これによってDPSを既存のウィンドウシステムと組み合わせて利用することができる。[X Window Systemと組み合わされることが多く](../Page/X_Window_System.md "wikilink")、そのような形で後に[IBM](../Page/IBM.md "wikilink")や[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink")がワークステーションにDisplay PostScriptを採用した。X WindowからDPSを呼び出す際のインタフェース部分のコードはDPS本体よりも複雑化することが多い。他にも選択肢はあるため、DPSは広く採用されるには至らなかった。

## NeXTでのDisplay PostScript

[NeXT](../Page/NeXT.md "wikilink")の開発者は、NeXTの[オブジェクト指向](../Page/オブジェクト指向プログラミング.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の利点を最大限生かすため、全く新しい[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")を開発した。DPSにウィンドウを生成するためのコマンドやイベントに対応するためのコマンドが追加された。これは[NeWS](https://ja.wikipedia.org/wiki/NeWS "wikilink")にも似ているが、より単純である。APIを統一することで高い抽象レベルでのプログラミングが容易になり、NeXTはDPSを多用した数少ないシステムのひとつとなった。ユーザー空間でのウィンドウシステムのライブラリである[NEXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")は、タイトルバーやスクロールバーなどのアイテムをPostScriptを使って描画している。これは、実際には`pswrap`を多用したもので、プログラマからはオブジェクトの形でアクセスできるようになっている。

## NeXT以後

アップルがNeXT後継システムとしてリリースした[Mac OS Xで採用した独自のウィンドウサーバ](https://ja.wikipedia.org/wiki/macOS "wikilink")[Quartz](../Page/Quartz.md "wikilink")は、PostScriptコードを格納し実行するのではなく、[ビットマップとしてウィンドウのグラフィックスをキャッシュする](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")。[Quartz 2Dというグラフィックスライブラリは](https://ja.wikipedia.org/wiki/Quartz_2D "wikilink")、PostScriptに似た[PDFのグラフィックス](../Page/Portable_Document_Format.md "wikilink")・プリミティブを提供するが、これはあくまでもアプリケーションのフレームワークであり、ウィンドウサーバ内ではPostScriptもPDFも存在しない。アップルがこのようなモデルを採用した理由はいろいろあるが、アドビがDPSのライセンス料として提示した金額が大きかったこと、[Carbon](../Page/Carbon.md "wikilink")や[Classicのコードをより効率的にサポートすること](https://ja.wikipedia.org/wiki/Classic_\(ソフトウェア\) "wikilink")、[QuickDraw](https://ja.wikipedia.org/wiki/QuickDraw "wikilink")ベースのアプリケーションがビットマップによる描画を行っていることなどが挙げられる。アドビのPDF規格のライセンス条件はずっと緩く、条件付きで無料でソフトウェアにPDFフォーマットを採用できるようになっている。

## 参考文献

  - 最新版 [PDF specification](http://partners.adobe.com/public/developer/en/pdf/PDFReference16.pdf), version 1.6
  - [PostScript Language Reference, Second Edition](http://partners.adobe.com/public/developer/en/ps/psrefman.pdf), Display PostScriptについての情報もある
  - [Display PostScript reference documents](http://partners.adobe.com/public/developer/ps/sdk/index_archive.html#dps)

## 外部リンク

  - [Description at C2 Wiki](http://c2.com/cgi/wiki?DisplayPostscript)
  - [GNU/BackBone](http://www.nongnu.org/backbone/)

[Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:NeXT](https://ja.wikipedia.org/wiki/Category:NeXT "wikilink")