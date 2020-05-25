> この記事は[Javaアプレット](https://ja.wikipedia.org/wiki/Javaアプレット)から翻訳されています。


**Javaアプレット**（Java Applet）は、ネットワークを通して[Webブラウザに読み込まれ実行される](../Page/ウェブブラウザ.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[アプリケーションの一形態](../Page/アプリケーションソフトウェア.md "wikilink")。Java 10までは[Java Runtime Environmentに搭載されていて](../Page/Java_Runtime_Environment.md "wikilink")、Java 9より非推奨になり、Java 11で廃止\[1\]。

## 概要

最初の実装は[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に公開された[HotJava](https://ja.wikipedia.org/wiki/HotJava "wikilink")へのもので、その後[1996年](../Page/1996年.md "wikilink")に[Netscape Navigatorに搭載されたことで普及した](../Page/Netscape_Navigator_\(ネットスケープコミュニケーションズ\).md "wikilink")。単に[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")とも言う。基本的にデスクトップ版Javaの全機能を持つが、Webページの一部として自動的に読み込まれて動作するため、セキュリティー上の観点から一般のアプリケーションプログラムと比べさまざまな制限（[サンドボックス](../Page/サンドボックス_\(セキュリティ\).md "wikilink")）が課せられている。ただし、このセキュリティー上の制限は、ユーザーの許諾により解除する事もできる。

Javaアプレットを実行するには[Webブラウザ](https://ja.wikipedia.org/wiki/Webブラウザ "wikilink")がをサポートしていることが必要である。[Google Chromeはバージョン](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")42(2015年4月)でNPAPIが標準状態で無効になりバージョン45(2015年9月)以降でNPAPIをサポートしなくなった。[Mozilla Firefoxはバージョン](../Page/Mozilla_Firefox.md "wikilink")52(2017年3月)以降で[Flash Player以外のすべてのNPAPIプラグインのサポートを打ち切った](https://ja.wikipedia.org/wiki/Flash_Player "wikilink")\[2\]。[オラクル社は](../Page/オラクル_\(企業\).md "wikilink")2017年9月22日にリリースされたJava 9でJavaアプレットを非推奨にし、Java 11\[3\]では廃止することを2016年1月27日に発表した\[4\]。JavaアプレットだけでなくFlashや[Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")といった類似技術も多数のWebブラウザがサポート廃止予定で今後は[HTML5](../Page/HTML5.md "wikilink")と[JavaScript](../Page/JavaScript.md "wikilink")などに移行する流れである。

## 歴史

Webの普及初期に、インタラクティブ性を高められる技術の一つとして注目を浴び、当時のWeb普及に寄与した。しかし、当時[Internet Explorerとシェアを二分していたNetscape](../Page/Internet_Explorer.md "wikilink") 4.xにおいて当時まだできたばかりの[JIT](https://ja.wikipedia.org/wiki/JIT "wikilink")コンパイルに時間がかかった等の理由により、Javaアプレットをロードすると数十秒から数分の間操作を受け付けなくなるという現象が起こり、この現象が影響してJavaアプレットを利用したサイトが敬遠されるようになってしまった。また、当初は以下のような技術的な問題もあり、[Shockwaveや](../Page/Adobe_Shockwave.md "wikilink")[Flashの台頭もあって](../Page/Adobe_Flash.md "wikilink")、ウェブ上でインタラクティブ性を実現する用途には、広く使われているとは言えない状況であった。

  - [ブロードバンドインターネット接続](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")の普及前は、Javaアプレットを快適に動作するのに必要な高速な回線を利用できるユーザが少なかった。
  - Javaがまだ生まれて間もない技術だったためWebブラウザ上の[Java VMの動作が遅かった](../Page/Java仮想マシン.md "wikilink")。
  - 最初の1 - 2年は、ベンダごとのJava仮想マシンの実装が仕様に合わず、[Microsoft社製のJava仮想マシンが](../Page/マイクロソフト.md "wikilink")[SUNのライセンスに違反した独自仕様の実装を進めたこともあり](../Page/サン・マイクロシステムズ.md "wikilink")、環境ごとの互換性を取るのが難しかった。

これらは主にJavaアプレットが登場したときまだ十分にWeb関連の技術や環境が発達していなかったことによるが、その後のJava VMの改良や、回線速度の向上、ハードウェア性能の向上により解消されているものが多い。その後は、利用シェアが大きいとは言えないものの、[オンライントレード](https://ja.wikipedia.org/wiki/オンライントレード "wikilink")の[ローソク足](https://ja.wikipedia.org/wiki/ローソク足 "wikilink")[チャート](https://ja.wikipedia.org/wiki/チャート "wikilink")表示、[チャット](../Page/チャット.md "wikilink")や[CG](../Page/コンピュータグラフィックス.md "wikilink")[アニメーション](../Page/アニメーション.md "wikilink")、[ゲーム](../Page/ゲーム.md "wikilink")、教育機関による学習システムなどでの利用を見ることができた。

## 利点

登場時には画期的であった、以下のような特徴がある。

  - ほぼ完全なJavaの環境であり、オブジェクト指向プログラミングで、高機能なアプリケーションを作成できる。実際に[JPEG2000](https://ja.wikipedia.org/wiki/JPEG2000 "wikilink")デコーダーや[SSHクライアント等の](../Page/Secure_Shell.md "wikilink")、通常は[C言語](../Page/C言語.md "wikilink")などで書かれるような高度なアプリケーションも存在する。
  - [HTML内に埋め込むことにより](../Page/HyperText_Markup_Language.md "wikilink")、シームレスに高機能デスクトップ・アプリケーションの配布が可能であり、アプリケーションの配布コストを低減できる。
  - サンドボックスと呼ばれる強力なセキュリティー機構を持つため、インターネットでのアプリケーション配布が可能である。
  - ポータブルな[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")環境である。同一の配布ファイルで、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[Linux](../Page/Linux.md "wikilink")等の処理系でアプリケーションを動作させることができる。

## 欠点

終盤においても以下の欠点があり、利用上の問題点となるときがあった。

  - Javaが得意としない動画やベクター描画の処理は、必然的にJavaアプレットでも得意とされない。[統合開発環境](../Page/統合開発環境.md "wikilink")でのこれらの処理の記述サポートが貧弱であった。
  - Java言語で書かれるので、専門的なプログラマー以外には難易度が高いとされる。この点を補うために[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")が登場しているが、認知度が高いとは言えなかった。
  - ブラウザーにインストールされていないことがあった。[Web Browser Plugin Market Share / Global Usage](http://www.statowl.com/plugin_overview.php)によればブラウザーのJava VMのインストール率は80%前後であり、同種の機能を持つAdobe Flashの95%超には及ばない。

## ブラウザー以外の用途

Webブラウザに組み込んで使うことを目指して作成され、その後の仕様変更・機能追加もWebブラウザ利用に焦点を置いたものであるが、Javaアプレットを動作させるアプリケーションが必ずWebブラウザでなければならないわけではない。例えば[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")では、文書内にJavaアプレットを埋め込むことができる。

## セキュリティー制限とその解除

Java アプレットには、インターネットでの配布を可能にするために以下のようなセキュリティー上の制限が設けられている。

  - [ローカル](../Page/ローカル.md "wikilink")の資源に[アクセス](../Page/アクセス.md "wikilink")できない（[クリップボード](../Page/クリップボード.md "wikilink")や[ディスクの読み書きができない](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、印刷機能を扱えないなど）。
  - アプレットの[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")元[サーバ](../Page/サーバ.md "wikilink")としか[通信](../Page/通信.md "wikilink")できない。

これらの制限は、ユーザーがポリシー・ファイルを作成し、これらの動作を許諾することによって外すことができる。ポリシー・ファイルは、[URI](https://ja.wikipedia.org/wiki/URI "wikilink")で指定されるコードベース（codeBase）、もしくは[電子署名](../Page/電子署名.md "wikilink")（signedBy）ごとに承諾する動作を規定する。なお、後者の場合はアプレット開発者がアプレットに[JarSigner](https://ja.wikipedia.org/wiki/JarSigner "wikilink")というツールを使って電子署名する必要があるが、署名に必要な鍵は他の処理系で使われる鍵と同一のもの、例えば[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")で生成したものが利用できる。

## 関連技術

アプリケーション配布システムとしては、Javaアプレットよりも便利で高度な[Java Web Startの登場により](../Page/Java_Web_Start.md "wikilink")、必要性が薄れてきている。

## 関連項目

  - [Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")
  - [Java Servlet](../Page/Java_Servlet.md "wikilink")
  - [サンドボックス](../Page/サンドボックス_\(セキュリティ\).md "wikilink")
  - [HotJava](https://ja.wikipedia.org/wiki/HotJava "wikilink")
  - [Java Web Start](../Page/Java_Web_Start.md "wikilink")
  - [JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")

## 参照

<references/>

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink")

1.  [Java Client Roadmap Update - An Oracle White Paper March 2018](http://www.oracle.com/technetwork/java/javase/javaclientroadmapupdate2018mar-4414431.pdf)
2.  <https://support.mozilla.org/ja/kb/npapi-plugins>
3.
4.  <https://blogs.oracle.com/java-platform-group/moving-to-a-plugin-free-web>