> この記事は[Xojo](https://ja.wikipedia.org/wiki/Xojo)から翻訳されています。


**Xojo**は、Xojo社によって開発された[ソフトウェアの開発ツールであり](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")を採用した独自の[BASIC](../Page/BASIC.md "wikilink")言語を使用し、[統合開発環境](../Page/統合開発環境.md "wikilink")を備える。2013年までは「REALbasic」（1997年の買収以前製品名は「CrossBASIC」）と呼ばれた。

あらかじめ備えられている機能が豊富なことや[GUIのデザインが簡単であること](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、非常に理解しやすい言語仕様などから、とくに初心者に愛用される。日本では株式会社アスキーソリューションズが代理店となり販売およびサポートを提供していたが、2007年4月に開発元であるReal Software社に移管されることが発表された。

主に[Macintosh](../Page/Macintosh.md "wikilink")版が知られ、しばしば「[Macintosh](../Page/Macintosh.md "wikilink")版の[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")」と喩えられるが、[Windows版ならびに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")/x86版も存在する。また、利用している環境に関わらず、全てのプラットフォーム用の実行バイナリを出力することができるため、双方向の[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")開発が可能である。

なお、Xojoは、[Universal Binaryアプリケーションを作成することのできる](https://ja.wikipedia.org/wiki/Universal_Binary "wikilink")、[サードパーティー](../Page/サードパーティー.md "wikilink")開発ツールのひとつである。

## 主な機能

Xojoの主な機能は以下のとおり。

### 機能と特徴

  - [イベント駆動型の構造化された完全な](../Page/イベント駆動型プログラミング.md "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語
  - REALbasicやランタイムが不要な単独の[アプリケーションに](../Page/アプリケーションソフトウェア.md "wikilink")[ビルドできる](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")言語
  - [参照カウント](../Page/参照カウント.md "wikilink")方式の[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を採用
  - [マルチリンガル](https://ja.wikipedia.org/wiki/マルチリンガル "wikilink")に対応した豊富な文字列操作[メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")
  - [Perl](../Page/Perl.md "wikilink")と同等の[正規表現](../Page/正規表現.md "wikilink")による強力な文字列検索メソッド
  - 文字列は[Unicode](../Page/Unicode.md "wikilink") ([UTF-8](../Page/UTF-8.md "wikilink")) で処理するため、言語に依存しないアプリケーションが開発できる
  - 各プラットフォーム間で、[ソースコード](../Page/ソースコード.md "wikilink")は完全に互換（[OS依存の機能を使用している場合を除く](../Page/オペレーティングシステム.md "wikilink")）
  - [Macintosh Toolbox](https://ja.wikipedia.org/wiki/Macintosh_Toolbox "wikilink") (Toolbox) を学ぶ必要がない
  - ビジュアルインターフェースビルダによるGUIのグラフィカルなデザインが可能
  - [マルチメディア](../Page/マルチメディア.md "wikilink")機能に長けている
  - GUIを持たないコンソールアプリケーション、サービスアプリケーションも作成可能
  - アプリケーションサイズが大きい（後述）
  - 処理速度は他の開発環境で作成したアプリケーションに比べて遅い
  - ダブルクリックで起動できるアプリケーション以外のプログラム（[プラグイン](../Page/プラグイン.md "wikilink")や機能拡張など）は作成できない

#### 習得のしやすさ

Macでの[プログラミングを複雑にしているToolboxやその他の](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[APIを学ばずに済む点は初心者にとって非常にありがたい点であるが](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、同時に、複雑な機能を実現することが難しくなっている。それをカバーするためにプラグインシステムなどが採用されており、サードパーティーから優れたプラグインが多数開発されている。

言語仕様については、BASIC言語をベースにしているため、基本的な命令その他習得の容易さは他の追随を許さない。また、オブジェクト指向的実装についても、[クラスや](../Page/クラス_\(コンピュータ\).md "wikilink")[インタフェースなど](../Page/インタフェース_\(情報技術\).md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")相当の機能を実現している。

#### マルチメディア機能

マルチメディア機能については[QuickTime](../Page/QuickTime.md "wikilink")の機能をかなり引き出すことが可能であり、[ビルトイン](https://ja.wikipedia.org/wiki/ビルトイン "wikilink")の命令としてQuickTimeムービーを編集する機能も備える。グラフィック周りは、処理の遅さに目をつぶれば、ラスターイメージから[ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")、3DCGまでを扱え、256階調グレースケール[マスク](../Page/マスク.md "wikilink")による[アルファブレンド](../Page/アルファブレンド.md "wikilink")も簡単に実現でき、ソフトウェアレベルで[スプライト機能さえも有する](../Page/スプライト_\(映像技術\).md "wikilink")\[1\]。スプライトに関しては一切コーディングすることなくスプライト同士が接触したかを判定することまで可能。画像の透過に関しては、アルファブレンドを有しながら特定の色を透過したり[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")が使えないなど、中途半端な感もある。

比較的充実したグラフィックス機能を備える反面、サウンド機能は貧弱である。あらかじめ用意したサウンドファイルを読み込み、再生することしかできず、リアルタイムでの音声処理はプラグインに依存する必要が有る。

#### 巨大なアプリケーション

アプリケーションサイズが大きいというのはREALbasic製のアプリケーションのあまり望ましくない特徴といえるだろう。たとえば、何もコーディングを行っていない場合であっても[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に最適化されたコードである[Mach-O Carbon](../Page/Carbon.md "wikilink") [Universal Binaryでコンパイルすると](https://ja.wikipedia.org/wiki/Universal_Binary "wikilink")8.8MBのファイルサイズを消費する。これは、REALbasicのフレームワーク自体をアプリケーションに内蔵してしまうことと、[PowerPC](../Page/PowerPC.md "wikilink")と[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")の2つのアーキテクチャの実行ファイルが生成されるためである。また、アプリケーション内で特定のコントロールや機能（例えば[XML](../Page/Extensible_Markup_Language.md "wikilink")[パーサなど](../Page/構文解析器.md "wikilink")）を使用している場合、さらにファイルサイズは増加する。

とはいえ、今日の[PCにおいては](../Page/パーソナルコンピュータ.md "wikilink")[ハードディスクの容量も十分に大容量化されており](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、ファイルサイズの大きさが問題となる場面はあまりないと言える。

#### 処理速度

処理速度の遅さもREALbasic製のアプリケーションの特徴。とくにグラフィックや多言語関係の機能は比較的遅い。このため、処理速度を補う目的で、内蔵関数と同等の機能を備える高速なプラグインを作成することもしばしば行われる。

#### フロントエンドの開発

[サーバ](../Page/サーバ.md "wikilink")や[データベース](../Page/データベース.md "wikilink")の[フロントエンド](../Page/フロントエンド.md "wikilink")や、[UNIX](../Page/UNIX.md "wikilink")[シェル](../Page/シェル.md "wikilink")や[DOS](../Page/MS-DOS.md "wikilink")[コマンドラインのGUIフロントエンドの開発するための各種命令も豊富](../Page/コマンドラインインタプリタ.md "wikilink")。

#### Mac OSの機能への対応

  - [AppleScript](../Page/AppleScript.md "wikilink")や[AppleEvent](https://ja.wikipedia.org/wiki/AppleEvent "wikilink")のサポートにより、他のアプリケーションと連携することも可能
  - UNIXコマンドを実行可能
  - 「[Quartz](../Page/Quartz.md "wikilink")」を利用した平面画像の描画、「Quesa（オープンソースのQuickDraw 3D互換3Dグラフィックライブラリ）」による3D描画のサポート
  - [リソースフォーク](../Page/リソースフォーク.md "wikilink")、バイナリデータの[リトルエンディアンと](https://ja.wikipedia.org/wiki/エンディアン "wikilink")[ビッグエンディアンの使い分け](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、255文字までのロングファイルネームなどもサポート
  - キーチェーン・[Spotlight](../Page/Spotlight.md "wikilink")・アドレスブックへのアクセスをサポート
  - Toolbox、PowerPC共有ライブラリ（InterfaceLibなど、他のアプリケーションが共有できる[Power Mac用サブルーチン群](../Page/Power_Mac.md "wikilink")）へのアクセスの対応
  - GUI部品の[Aquaでの描画に対応](../Page/Aqua_\(コンピュータ\).md "wikilink")

#### Windowsの機能への対応

  - [OLE](../Page/Object_Linking_and_Embedding.md "wikilink") ([COM](../Page/Component_Object_Model.md "wikilink"))、[タスクトレイ](../Page/タスクトレイ.md "wikilink")の使用をサポート
  - [MDIのサポート](../Page/Multiple_Document_Interface.md "wikilink")
  - [Windows XPのサポート](../Page/Microsoft_Windows_XP.md "wikilink")、GUI部品の[Luna](../Page/Luna.md "wikilink")（Windows XP標準の外観）での描画に対応
  - Win32 APIへのアクセス、[レジストリ](../Page/レジストリ.md "wikilink")へのアクセスのサポート
  - DOSコマンドを実行可能

#### 自動メモリ管理

メモリは自動的に管理しているため、[プログラマ](../Page/プログラマ.md "wikilink")は[メモリに関して特に意識しせずに開発が可能である](../Page/記憶装置.md "wikilink")。参照カウントを用いたガベージコレクションも備える。

#### 優れた拡張性

[プラグイン](../Page/プラグイン.md "wikilink")を組み込むことによりIDE自体の拡張が行えるほか、Mac OS版では[XCMD](https://ja.wikipedia.org/wiki/XCMD "wikilink")やXFCN、AppleScript、AppleEvent、UNIXシェル、PowerPC共有ライブラリなどを利用することで、言語が備えていない機能を実現することも可能である。

## REALbasicの現状

2010r1バージョンよりIDEの名称がREAL Studioとなった。2010年12月14日現在、英語版、日本語版共にバージョン2010 Release 5がリリースされている。なお、Mac版についてはバージョン2010 Release 4 からIntelプロセッサを搭載したMac専用となったため、[PowerPC](../Page/PowerPC.md "wikilink")プロセッサを搭載したMacでは使用できなくなった。2010年9月にリリースされたバージョン2010 Release 3.2 がPowerPC搭載Mac上で動作する最後のバージョンである。なお、[Intel Mac上でPowerPC搭載Mac用のアプリケーションやUniversal](../Page/Intel_Mac.md "wikilink") Binaryを作成することは可能である。

2013年6月4日リリース予定の2013r1より、製品名および言語名が「Xojo」、会社名が「Xojo Inc.」に変更されることが発表された\[2\]。

## サンプルコード

`//コメントは“//”“'”あるいは“REM”を用い、改行までがコメントとみなされる`
`Dim result As Integer //変数宣言と型定義。変数名“result”を“Integer”（整数値）型として定義`
`result = Pow(10, 10) //10の10乗を計算し、resultに代入`
`MsgBox Str(result)     //メッセージボックスにresultの内容を文字列として表示`

## 脚注

## 外部リンク

  - [Real Software社（英語）](http://www.realsoftware.com/)
  - [Real Software 社（日本語）](http://www.realsoftware.com/index.php?lang=jp)
  - [Xojo社](http://www.xojo.com)

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink")

1.  3D CGを扱うRB3Dと、スプライトを扱うSpriteSurfaceは、開発終了となっている。
2.