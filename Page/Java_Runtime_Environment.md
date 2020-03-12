> この記事は[Java Runtime Environment](https://ja.wikipedia.org/wiki/Java_Runtime_Environment)から翻訳されています。


**Java Runtime Environment**（Java実行環境、**JRE**）とは、[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")上で[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")用の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")（[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")）を動かせるようにする[ソフトウェア](../Page/ソフトウェア.md "wikilink")群である。JREは[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（旧[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）による公式実装のほか、[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")のコミュニティによるオープン実装、[IBM](../Page/IBM.md "wikilink")などの正式にライセンス供与されたサードパーティによる実装などが存在する\[1\]。

## 概要

JREのソフトウェア群は[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) と[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) から成り立っている。APIはエディション（プロファイル）に応じて、標準[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")の集合や拡張ライブラリなどを提供する。仮想マシンとAPIは互いに互換性がなければならず、それゆえJREとして共にバンドルされている。これは仮想マシンがプロセッサであり、APIがユーザインタフェースであるような仮想的なコンピュータと考えることができる。

JREは、Javaアプリケーション開発に必要な[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")などを含む[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") (SDK) である[Java Development Kit](../Page/Java_Development_Kit.md "wikilink")（JDK、Java開発キット）にも同梱されている。

Javaアプリケーションは対応するJREがなければ動作させることができない。Java互換の組み込み機器では通例JREが標準インストールされているが、[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")マシンでは、JREが標準インストールされていないこともあり、その場合はJREを事前にインストールする必要がある。JDK 10までは、javapackagerと呼ばれるツールを利用し、JREをアプリケーションパッケージにプライベートモジュールとして同梱（バンドル）・再配布する形態もサポートされていた\[2\]。JREは基本的に後方互換性を保っており、古いJDKを利用して作成されたJavaアプリケーション（[JAR](../Page/JAR_\(ファイルフォーマット\).md "wikilink")）を新しいJRE上で動作させることもある程度可能であるが、新しいバージョンのJDK/JREで持ち込まれた非互換性により、アプリケーションが正常に動作しなくなることもある\[3\]。[Javaアプレット](../Page/Javaアプレット.md "wikilink")など、一部の[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")は古いバージョンのJDK/JREにしか含まれておらず、新しいバージョンのJDK/JREでは利用不可能であるものもある。[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")のように、かつてJDK/JREに標準で含まれていたものの、のちに分離・独立して個別提供されるようになったコンポーネントもある。

Java 10までのJREには[Java Web Startも同梱されていた](../Page/Java_Web_Start.md "wikilink")。インストール時に[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[Internet Explorerなどの](../Page/Internet_Explorer.md "wikilink")[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")にJava Plug-inをインストールするかどうかを尋ねられる。これはブラウザで[Javaアプレット](../Page/Javaアプレット.md "wikilink")を動かし、Java Web Start対応Javaアプリケーションを起動できるようにするために必要なものであり、単純に[Flashをブラウザ上で直接実行したり](https://ja.wikipedia.org/wiki/Adobe_Flash_Player "wikilink")、ブラウザ外部の[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")を起動したりといったものと同じ[プラグイン](../Page/プラグイン.md "wikilink")の一種である。

JREのアップデートには、旧バージョンを削除しないものがあった。セキュリティホールが発見されている、あるいはサポートが終了している旧バージョンのJava (JDK/JRE) をシステムに残しておくと、重大なセキュリティリスクが生じるため、旧バージョンを手動で削除することが強く推奨されている\[4\]。

## 関連項目

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")
  - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM)
  - [Java Development Kit](../Page/Java_Development_Kit.md "wikilink")（JDK、Java開発キット）
  - [IBM J9](https://ja.wikipedia.org/wiki/IBM_J9 "wikilink")

## 参照

<references />

## 外部リンク

  - [Java | Oracle](https://www.java.com/ja/)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink")

1.  [Android](../Page/Android.md "wikilink")のJava実行環境は正式にライセンスされたJREではなく、また[Dalvik仮想マシン](../Page/Dalvik仮想マシン.md "wikilink")/[Android Runtimeは正式なJava仮想マシンとの互換性がない](https://ja.wikipedia.org/wiki/Android_Runtime "wikilink")。
2.  [javapackager](https://docs.oracle.com/javase/10/tools/javapackager.htm#JSWOR719)
3.  [JDK 8の互換性ガイド](https://www.oracle.com/technetwork/jp/java/javase/overview/8-compatibility-guide-2156366-ja.html)
4.  [古いバージョンのJavaをシステムからアンインストールしなければならないのはなぜですか。](https://www.java.com/ja/download/faq/remove_olderversions.xml)