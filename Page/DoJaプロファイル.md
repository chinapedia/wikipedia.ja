> この記事は[DoJaプロファイル](https://ja.wikipedia.org/wiki/DoJaプロファイル)から翻訳されています。


**DoJaプロファイル**（ドゥージャプロファイル）は[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")グループの[携帯電話](../Page/携帯電話.md "wikilink")（フィーチャーフォン）である[mova](https://ja.wikipedia.org/wiki/mova "wikilink")シリーズ及び[FOMA](../Page/FOMA.md "wikilink")シリーズに搭載される[Java実行環境の仕様である](../Page/Java_Runtime_Environment.md "wikilink")。後継の**Starプロファイル**（スタープロファイル）も本項で記載する。DoJaは開発者向けの用語であり、エンドユーザー向けには「[iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")」「iアプリDX」「メガiアプリ」などの名称となっている。

## 特徴

DoJaは[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink") （以下「サン」と略）の[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")構想において、[Java MEにおける](../Page/Java_Platform,_Micro_Edition.md "wikilink")、[CLDC上の](../Page/Connected_Limited_Device_Configuration.md "wikilink")1プロファイルとして位置づけられる。

携帯電話は一般に大画面の[ディスプレイや](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[マルチウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")、[マウスなどの](../Page/マウス_\(コンピュータ\).md "wikilink")[ポインティングデバイス](../Page/ポインティングデバイス.md "wikilink")を持たない上、[ハードウェア](../Page/ハードウェア.md "wikilink")スペック（[CPU](../Page/CPU.md "wikilink")スピード、[メモリ容量](../Page/主記憶装置.md "wikilink")）がデスクトップ・サーバに比べて比較的貧弱であるなど、デスクトップのJava環境と比べて大きな差がある。そのため、DoJaのJava APIも[Java SEと比べてかなりの違いがある](../Page/Java_Platform,_Standard_Edition.md "wikilink")。

ただ、Java MEのCLDCの仕様は、デスクトップのJava SEのサブセットであるが、[マルチスレッド処理を含めて](../Page/スレッド_\(コンピュータ\).md "wikilink")、本当のJava[プログラミングを行うことが可能である](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。ただし、DoJa 3.5まではCLDC 1.0のため、浮動小数点数処理がない、ファイナライザが動作しないなどの制約があった。

DoJaが動作する携帯電話上においては、[ファイルシステム](../Page/ファイルシステム.md "wikilink")を持たず、データの保存には「スクラッチパッド」と呼ばれる領域を用いる。また、iアプリを[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")したホストとのみ、ネットワーク通信を行うことができる。

## 実行形態

DoJaでは、[コンパイルした](../Page/コンパイラ.md "wikilink")[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")、および実行に必要な画像や音楽データを含めて、[Jar](https://ja.wikipedia.org/wiki/Jar "wikilink")形式でパッケージ化しておく。このように準備されたiアプリは[HTTPあるいは](../Page/Hypertext_Transfer_Protocol.md "wikilink")[HTTPS](../Page/HTTPS.md "wikilink")通信を通じて、携帯電話にダウンロードされ実行される。[メモリースティック](../Page/メモリースティック.md "wikilink")や[SDカードなどの外部記憶媒体を使って](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")[インストール](../Page/インストール.md "wikilink")する方法は公式に発表されていない。[セキュリティに関しては厳しく](../Page/コンピュータセキュリティ.md "wikilink")、他のアプリとスクラッチパッド上のデータを共有したり、電話帳やメールデータにアクセスするには、[iアプリDX](https://ja.wikipedia.org/wiki/iアプリDX "wikilink")仕様を使う必要がある。

尚、DoJaで実行するClassファイルは、パッケージする前に通常のコンパイルのほかに、preverifyというツールを使って前処理（事前検証）を行っておく必要がある。これはCLDCの制限（というより特徴）であり、実行時・ロード時のバイトコードベリファイの負荷を減らすために、あらかじめ型情報を調査し、その情報をJavaクラスファイル内に添付しておく必要があるためである。

## API

[CLDCは](../Page/Connected_Limited_Device_Configuration.md "wikilink")、組み込み向けの一般的な共通機能を絞り込んだ[API仕様を持っており](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[GUIなどを定義していない](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。Java MEの枠組みでは、それらはプロファイルで定義される。

DoJa APIにはiアプリ基本API、iアプリオプションAPI、iアプリ拡張APIの3種類がある。

  - iアプリ基本APIとは共通仕様で、全機種が標準にあり、APIおよび動作が規定されている。
  - iアプリオプションAPIとは共通仕様で、APIおよび動作が規定されているが端末ごとに搭載の有無はメーカーが決定している。
  - iアプリ拡張APIとはメーカーが独自にAPIおよび動作を規定したもので、ソースレベルで他のメーカーと互換性がないことを考慮する必要がある。

iアプリオプションAPI及びiアプリ拡張APIについては、対応している携帯電話でないと実行できない。

DoJaにおいて[UI処理には](../Page/ユーザインタフェース.md "wikilink")、com.nttdocomo.ui.\*パッケージに含まれる独自のUIクラス群を使用する。入出力においては、CLDCのジェネリックIOフレームワークに基づき、ネットワーク入出力処理(HTTP, HTTPS)、スクラッチパッドアクセス処理、Jarリソースに含まれたデータの入力処理などを行うことができる。

DoJa 2.0 (504i, 2051, 2701, 2102V)以降は、待ち受け画面のように常に常駐して動作する「待ち受けiアプリ」の機能や[赤外線通信機能が追加された](../Page/IrDA.md "wikilink")。また、DoJaオプション機能としてゲーム向けの機能（[スプライト](../Page/スプライト_\(映像技術\).md "wikilink")、[3Dの](../Page/3次元コンピュータグラフィックス.md "wikilink")[ポリゴン](../Page/ポリゴン.md "wikilink")など）、[カメラ機能などが定義された](../Page/デジタルカメラ.md "wikilink")。

DoJa 3.0 (505i, 506i, 900i)では、ゲーム向け機能の一部が標準機能になった。また、「[iアプリDX](https://ja.wikipedia.org/wiki/iアプリDX "wikilink")」として、携帯電話の電話帳にアクセスしたり、メールなどと連携できるような機能が追加された。これらのiアプリDX機能の詳細については一般には公開されていない（公式[コンテンツプロバイダ](https://ja.wikipedia.org/wiki/コンテンツプロバイダ "wikilink")向けにのみ提示されているものと思われる）。またオプション機能として[バーコード](../Page/バーコード.md "wikilink")の読み取り機能、[指紋](../Page/指紋.md "wikilink")認証機能などが追加されている。

DoJa 4.0では基本APIに[マスコットカプセル](../Page/MascotCapsule.md "wikilink")4.0を制御する3Dグラフィックス描画機能と3Dサウンド制御機能が追加され、またDoJa 2.0以降と同じくマスコットカプセル3.0を制御する拡張APIも削除されずに残された。つまり、マスコットカプセル3.0及び4.0が使用でき、それぞれの特徴として3.0は値として整数を使用するため高速で動作するが4.0は値として浮動小数点を使用するため3.0より描画が遅い。ただし、4.0LEではマスコットカプセル4.0を制御する3Dグラフィックス描画機能と3Dサウンド制御機能は標準APIは使用することはできない。

DoJa 4.1では基本APIにセキュリティ機能（デジタル署名）およびSDカードを制御するAPIが追加された。

DoJa 5.0では基本APIにメモリ管理、[GPS制御](../Page/グローバル・ポジショニング・システム.md "wikilink")、オプションAPIにハードウェアを使用するOpenGL ES 1.0相当の3D描画、[Bluetooth](../Page/Bluetooth.md "wikilink")制御のAPIが追加された。

DoJa 5.1ではOpenGL ES 1.1対応。

Star 1.0では、ウィジェットアプリ（iWidget）機能、iアプリオンライン機能、iアプリコール機能、iアプリ-Flash連携機能などが追加になった。

Star 1.1では、タッチパネル対応など。

Star 1.5では、オーディオ出力先イベント、各種デバイス（コンパス・加速度センサ・歩数計など）対応。

Star 2.0では、内部ストレージへのアクセス、1ドット単位でのフォントサイズの指定、PNG対応、iアプリ自動起動、MyFACEからのiアプリ起動、マナーモード中の音声出力、HTTPで受信可能なレスポンスボディを1MBに拡大などが追加・変更になった。

## 歴史

  - 最初の版のDoJa 1.0仕様は、デジタルムーバ503i及び503iSシリーズ並びにFOMA2001、2002、2101Vシリーズに搭載。[2001年](../Page/2001年.md "wikilink")[1月26日](https://ja.wikipedia.org/wiki/1月26日 "wikilink")発売開始\[1\]。
  - DoJa 2.0仕様は、mova 504i及び504iSシリーズに搭載。
  - DoJa 2.1仕様は、FOMA 2051、2701シリーズに搭載。
  - DoJa 2.2仕様は、FOMA 2102Vシリーズに搭載。
  - DoJa 3.0仕様は、mova 505i及び505iS、506iシリーズに搭載。
  - DoJa 3.5仕様は、FOMA 900iシリーズに搭載。
  - DoJa 4.0仕様は、FOMA 901iシリーズに搭載。
  - DoJa 4.0LE仕様は、FOMA 700i、701i及び702iシリーズに搭載。
  - DoJa 4.1仕様は、FOMA 902iシリーズに搭載。
  - DoJa 5.0仕様は、FOMA 903i及び904iシリーズに搭載。
  - DoJa 5.0LE仕様は、FOMA 703iシリーズに搭載。
  - DoJa 5.1仕様は、FOMA 905iシリーズに搭載。
  - Star プロファイル1.0は、2008年公開
  - Star プロファイル1.1は、2009年公開
  - Star プロファイル1.2は、2009年公開
  - Star プロファイル1.3は、2010年公開
  - Star プロファイル1.5は、2011年公開
  - Star プロファイル2.0は、2011年公開

※DoJa 1.0から3.5まではCLDC 1.0である。DoJa 4.0以降はCLDC 1.1であり浮動小数点が使用できる。

DoJaは携帯電話が新しいデバイスを装備することにそれに対応する制御APIとして拡張されてきた。携帯電話自身の性能もハードウェア技術の進歩により、503i登場当初に比べ飛躍的にその実行速度、容量（一回で送受できる通信量や、スクラッチパッドの容量）、画面サイズなどを増やしているため、登場当初と比較してはるかに高機能なアプリケーションを書くことができるようになって来ている。

特に、アプリケーションサイズの制約は当初10KB（Jar圧縮後（FOMAは30KB）、スクラッチパッド10KB）という極めて厳しいものであったが、DoJa 2.0以降は30KB（スクラッチパッド100KB（505i以降及びFOMAは200KB））まで拡張されている。DoJa 3.5以降は100KB（スクラッチパッド400KB）まで拡張された。ただし、DoJa 4.0LEはJARファイルが30KBまで、スクラッチパッドサイズが200KBまでに制限されている。DoJa 5.0ではプログラムとスクラッチパッドの境界がなくなり、あわせて1MBになった。Starプロファイル1.xは合計2MB。Starプロファイル2.xは合計10MB。

## 互換性

同様の携帯電話向けJava実行環境のプロファイルには、サン自身による[MIDPがあるが](../Page/Mobile_Information_Device_Profile.md "wikilink")、開発時期の違いからか、NTTドコモグループ（以下「ドコモ」と略）の携帯電話には採用されるには至らなかった。

[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")、[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")、[ウィルコム](../Page/ウィルコム.md "wikilink")の携帯電話もJava実行環境を搭載しているが、いずれも世界中で広く採用されているMIDPを採用しており、DoJaとの互換性はない。厳密には、CLDCの範囲内では同様に動作するプログラムを作ることはできるかもしれないが、アプリケーションのパッケージングなどの方法も異なる。いずれにせよ、画面表示などの機能に互換性はないのでそのまま同じものが動作するという意味での互換性は無いといってよい。同じCLDCに基づくJava環境ではあるのでコードの一部もしくは多くを共通化できる可能性はある。

もうひとつ考える必要があるのは、機種間の互換性の問題である。DoJaはJava実行環境の仕様であるため、下位層としての[Java VMの実装やあるいはハードウェアに関して統一がなされていない](../Page/Java仮想マシン.md "wikilink")。このことはJavaの思想からは正しいのだが、[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")の振る舞いに関して携帯電話各メーカ間の実装差異は決して小さくない。

特に商用コンテンツとしてiアプリを開発する場合、機種間の差異は深刻な問題である。版を重ねるにつれて仕様の詳細度も増し、実装差異は一般には解決されていく方向ではあるといえるものの、開発期間の短さや、次々と採用される新機能、新メーカーの参入、そして過去の機種との互換性などを考慮とすると今後とも非常に深刻な問題であるといえる。なお、auの携帯電話ではベースとなる[クアルコム](../Page/クアルコム.md "wikilink")社製のアプリケーションプロセッサチップおよび採用されるJava VMが統一されているため、メーカ間互換性の問題は原理的にはおき得ない。

## Starプロファイル

FOMA2008年秋冬モデル（X-0XA）のうち、iWdgt([iウィジェット](https://ja.wikipedia.org/wiki/iウィジェット "wikilink"))・[iアプリオンライン](https://ja.wikipedia.org/wiki/iアプリオンライン "wikilink")対応機種については、新たにドコモとサン・マイクロシステムズによって共同開発された[Starプロファイル](https://ja.wikipedia.org/wiki/Starプロファイル "wikilink")が定義された。ただし、DoJaとはAPIの互換性がないため、Star環境によって動作させるためには別途移植作業が必要となる。待ち受けiアプリなど、Starでは廃止される機能が存在する（iWdgtにて代替させる）。今後の仕様拡張はStarでのみ行われる予定。端末には当面の間はDoJa実行環境も並行して搭載される予定。

## 開発

ドコモにより無料で提供されているDoJa[エミュレータ](../Page/エミュレータ.md "wikilink")を使用して[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")上で開発し、携帯電話にダウンロードさせて実行するという[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")での開発形態である。DoJaエミュレータは Forte (Sun ONE Studio)などとの連動機能や、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")を使用し、[Eclipseとの連携を行うことができる](../Page/Eclipse_\(統合開発環境\).md "wikilink")。

## 参照

<references />

## 外部リンク

  - [iアプリ | サービス・機能 | NTTドコモ](http://www.nttdocomo.co.jp/service/iappli/index.html)
  - [開発者向け情報](http://www.nttdocomo.co.jp/service/developer/make/content/iappli/index.html)

[Category:携帯電話_(NTTドコモ)](https://ja.wikipedia.org/wiki/Category:携帯電話_\(NTTドコモ\) "wikilink") [Category:携帯電話アプリ](https://ja.wikipedia.org/wiki/Category:携帯電話アプリ "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")

1.  [ドコモ，Java搭載iモード端末503i発表──1月26日発売](http://plusd.itmedia.co.jp/mobile/0101/18/503i.html)