> この記事は[Csound](https://ja.wikipedia.org/wiki/Csound)から翻訳されています。


**Csound**は音響を扱う[データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")であり、「サウンドコンパイラ」あるいは音楽プログラミング言語とも呼ばれる。名称の由来は、それまでの類似ソフトウェアとは異なり、[C言語](../Page/C言語.md "wikilink")で書かれていたためである。[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")の Barry Vercoe が Music360 という言語をベースとして設計し、[ベル研究所](../Page/ベル研究所.md "wikilink")の[マックス・マシューズ](https://ja.wikipedia.org/wiki/マックス・マシューズ "wikilink")が処理系を開発した。[LGPLライセンスで提供される](../Page/GNU_Lesser_General_Public_License.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。開発は1990年代から続いており、バス大学の John Fitch の主導の下で2005年2月に Csound 5 がリリースされた。主な開発関係者は、Istvan Varga、Gabriel Maldonado（画像処理機能を追加した CsoundAV を開発）、Robin Whittle、Richard Karpen、Michael Gogins、Matt Ingalls、Steven Yi、Victor Lazzarini である。

Csound は2種類の特別な形式の[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")を入力として使用する。*orchestra* ファイルは楽器の性質などを記述し、*score* ファイルは楽譜などの時系列パラメータを記述する。Csound はこれらのファイルにある命令群を実行し、[音声ファイル](https://ja.wikipedia.org/wiki/音声ファイル "wikilink")を生成したり、リアルタイムで音声を出力したりする。

*orchestra* ファイルと *score* ファイルは [XML](../Page/Extensible_Markup_Language.md "wikilink") タグを使って1つにまとめることも可能である。そのような統合された Csound ファイルの例を以下に示す。これは、1[kHzの](../Page/ヘルツ.md "wikilink")[正弦波](https://ja.wikipedia.org/wiki/正弦波 "wikilink")を[サンプリング周波数](../Page/サンプリング周波数.md "wikilink") 44.1 kHz で1秒間鳴らす[WAV](https://ja.wikipedia.org/wiki/WAV "wikilink")ファイルを生成するものである。

    <CsoundSynthesizer>;

      <CsOptions>
        csound -W -d -o tone.wav
      </CsOptions>

      <CsInstruments>
        sr     = 44100           ; サンプリング周波数
        kr     = 4410            ; 制御信号周波数
        ksmps  = 10              ; それらの比
        nchnls = 1               ; 出力チャネル数

        instr 1
        a1     oscil p4, p5, 1   ; 単純な発振器
               out a1            ; 出力
        endin
      </CsInstruments>

      <CsScore>
        f1 0 8192 10 1           ; 正弦波を表すテーブル
        i1 0 1 20000 1000        ; 1kHzの音を1秒間発生させる
        e
      </CsScore>

    </CsoundSynthesizer>

長年に渡って開発されてきたため、様々なモジュールが存在している。Csound の利点はそのモジュール性とユーザーによる拡張性の高さにある。

Csound の[MPEG-4](../Page/MPEG-4.md "wikilink")への拡張機能と （SAOL）との間には密接な関係がある。

他の多くのプログラミング言語と同様、Csound で大きなプログラムを開発する場合、[統合開発環境](../Page/統合開発環境.md "wikilink")が役立つ。最新の Csound 5 は、Linux、Windows、MacOS X でバイナリとソースコードが利用可能である。当初から見ればかなりの改善と拡張がなされており、他のソフトウェアから利用可能な[ライブラリ](../Page/ライブラリ.md "wikilink")とその[APIも提供している](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。C言語のAPIだけでなく、[Python](../Page/Python.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[C++](../Page/C++.md "wikilink") のAPIもある。

## 関連項目

  - [OpenMusic](https://ja.wikipedia.org/wiki/OpenMusic "wikilink") - Csoundの[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")となる[ライブラリ](../Page/ライブラリ.md "wikilink")(OM2Csound)が存在する。
  - [MUSIC-N](https://ja.wikipedia.org/wiki/MUSIC-N "wikilink")
  - [音響信号処理](https://ja.wikipedia.org/wiki/音響信号処理 "wikilink")
  - [ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/ソフトウェア・シンセサイザー "wikilink")
  - [デスクトップミュージック](../Page/デスクトップミュージック.md "wikilink")

## 外部リンク

  - [公式サイト](http://www.csounds.com/)
  - [CSound Wiki](http://www.electrowiki.com/wiki/index.php?title=Csound) 関連文書
  - [Project site](http://sourceforge.net/projects/csound) （[SourceForge.net](https://ja.wikipedia.org/wiki/SourceForge.net "wikilink")）
  - [MacCsound](http://www.csounds.com/matt/MacCsound/) は、Macintosh 向けの CSound プログラミング環境
  - [Csound for MacOS Classic](http://www.anthonykozar.net/csound-macos/)
  - [Csound Editor](http://gomba.sourceforge.net/flavio/csound-editor.html) Windows 向けの Csound プログラミング環境
  - [Dex Tracker](https://sourceforge.net/projects/dex-tracker)
  - [blue](http://www.csounds.com/stevenyi/blue)
  - [CsoundWiki](http://www.tobiah.org/csoundwiki)
  - [Bol Processor](http://bolprocessor.sourceforge.net/)

[Category:音声処理ソフト](https://ja.wikipedia.org/wiki/Category:音声処理ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/Category:ソフトウェア・シンセサイザー "wikilink")