> この記事は[Dalvik](https://ja.wikipedia.org/wiki/Dalvik)から翻訳されています。


**Dalvik仮想マシン**（ダルビックかそうマシン）は、[Android](../Page/Android.md "wikilink")プラットフォームで採用されていたレジスタベースの[仮想マシン](../Page/仮想機械.md "wikilink")\[1\]。および[Google](../Page/Google.md "wikilink")社のエンジニアによって設計・開発されていた。Android 5.0より[Android Runtime](https://ja.wikipedia.org/wiki/Android_Runtime "wikilink")（ART）に置き換えられた。

## 概要

Dalvikは低メモリ環境に対して最適化されており、オペレーティングシステムによるプロセス間の分離、メモリ管理、スレッドのサポートを用いて複数のVMインスタンスが同時に動作できるよう設計されている。Dalvikは[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")とされることもあるが、動作する[バイトコード](../Page/バイトコード.md "wikilink")が[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")ではないため、これは明らかに正確ではない。また、Java互換性テストを通過していないので、法的にもJavaを名乗れない。Android [SDKに含まれる](https://ja.wikipedia.org/wiki/ソフトウェア開発キット "wikilink") *dx* と呼ばれるツールが正規の[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")でコンパイルされた[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")を別のファイル形式（'.dex'形式）に変換する\[2\]。

Dalvik仮想マシンは、開発者のボーンスタインの先祖が居住していた、アイスランドの[エイヤフィヨルズル](https://ja.wikipedia.org/wiki/エイヤフィヨルズル "wikilink") (Eyjafjörður) にある[ダルビック](https://ja.wikipedia.org/wiki/ダールヴィーク "wikilink") (Dalvík) という漁村にちなんで命名された\[3\]\[4\]。

## アーキテクチャ

低メモリシステムに最適化されているため、Dalvik VMには通常のJava VMとは異なる特徴がある\[5\]:

  - Dalvik開発のために用いられた[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")は、より少ないメモリを使用するようスリム化された。[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")は再実装され、[C++](../Page/C++.md "wikilink")実装は[例外処理](../Page/例外処理.md "wikilink")をサポートしなくなった。
  - Dalvik VMの[定数プール](https://ja.wikipedia.org/wiki/定数プール "wikilink")は、[インタプリタ](../Page/インタプリタ.md "wikilink")を簡略化するため[32bitのインデックスのみ使用するよう改変された](../Page/32ビット.md "wikilink")。

Android 2.1までのDalvik VMは[ジャストインタイムコンパイルをサポートしていなかったが](../Page/実行時コンパイラ.md "wikilink")、2.2からは搭載されている。

新たな *.dex* フォーマットがより簡潔なアーキテクチャを可能にしたため、より制限も多くなった。[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")をDalvik VM上で実行させたり、JITコンパイルを行うことも簡単ではない。

Dalvikは[携帯電話](../Page/携帯電話.md "wikilink")メーカーがコアのVMの改変をソースコードの公開なしに行うことができるよう、[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink") ([GPLリンク例外](https://ja.wikipedia.org/wiki/GPLリンク例外 "wikilink")を用いている) ではなく[Apache Harmony](../Page/Apache_Harmony.md "wikilink") ([Apache Licenseで提供されている](https://ja.wikipedia.org/wiki/Apache_License "wikilink")) のサブセットを用いている。

## 参考文献

## 外部リンク

  - [Dalvik: how Google routed around Sun's IP-based licensing restrictions on Java ME](http://www.betaversion.org/~stefano/linotype/news/110/)
  - [Google and Sun may butt heads over Android](http://wireless.itworld.com/4269/071116googlesun/page_1.html)
  - [Dalvik Executable format](https://source.android.com/devices/tech/dalvik/dex-format.html)
  - [The town of Dalvik celebrates its namesake](http://www.kaktus.is/svanfridur/?f=1&o=533)

## 関連項目

  - [Android Runtime](https://ja.wikipedia.org/wiki/Android_Runtime "wikilink")

[Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:Java仮想マシン](https://ja.wikipedia.org/wiki/Category:Java仮想マシン "wikilink") [Category:Android](https://ja.wikipedia.org/wiki/Category:Android "wikilink")

1.
2.
3.  [Journal entry](http://uke.livejournal.com/25660.html)
4.
5.