> この記事は[Connected Limited Device Configuration](https://ja.wikipedia.org/wiki/Connected_Limited_Device_Configuration)から翻訳されています。


**Connected Limited Device Configuration** (**CLDC**)は[PDAや](../Page/携帯情報端末.md "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")のようなリソースが限られた機器を対象とした[Java MEアプリケーション向けのフレームワークの仕様である](../Page/Java_Platform,_Micro_Edition.md "wikilink")。CLDCよりも高機能な物が[CDCである](https://ja.wikipedia.org/wiki/Connected_Device_Configuration "wikilink")。

## 典型的な必要条件

16ビットCPU、160KBのメモリおよび[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")利用できる機器。

  - A 16-bit or 32-bit processor with a clock speed of 16MHz or higher
  - At least 160 KB of non-volatile memory allocated for the CLDC libraries and virtual machine
  - At least 192 KB of total memory available for the Java platform
  - Low power consumption, often operating on battery power
  - Connectivity to some kind of network, often with a wireless, intermittent connection and limited bandwidth

## プロファイル

### MIDP

携帯電話向けに設計され、GUI APIを持っており、MIDP2.0では2DゲームAPIが追加された。世界で広く利用され、日本でもDoCoMo以外のキャリアの携帯電話で採用されている。

### DoJa

[NTT DoCoMoによって](https://ja.wikipedia.org/wiki/NTT_DoCoMo "wikilink")[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")対応携帯電話向けに設計された。海外版のiモード搭載携帯電話にも採用されている。

### IMP

簡素なディスプレイまたはディスプレイがなく限られた2方向ネットワークアクセスを持ったネットワークカード、ルーターおよびその他の機器向けに設計されている。アプリケーションの生成、ストレージおよびネットワークアクセスに関するAPIだけが定義されている。IMPにはMIDPのjavax.microedition.io、rms and midletパッケージのサブセットがある。シーメンスモバイルおよびノキアがこの仕様を[JCPに提案した](../Page/Java_Community_Process.md "wikilink")。

詳細は[JSR 195](http://www.jcp.org/en/jsr/detail?id=195)を参照

## API

### java.io

J2SEにおける入出力操作を行うjava.ioパッケージの簡素化されたバージョンである。

### java.lang

Javaプログラムにおいてもっとも基本的なクラスを含む。このパッケージは基本的な例外、数値演算機能、システム機能、スレッド機能およびセキュリティ機能と同様にInteger、Stringのような基本なJavaの型を含む。

### java.util

java.utilの簡潔化されたバージョンである。このパッケージはVectorおよびHashtableのようなコレクションクラスを含み。ClaendarおよびDateクラスも含む。

## 歴史

  - CLDC 1.0 - [2000年](../Page/2000年.md "wikilink")[5月30日](../Page/5月30日.md "wikilink")承認
  - CLDC 1.1 - [2003年](../Page/2003年.md "wikilink")[3月27日](../Page/3月27日.md "wikilink")承認。浮動小数点(float, double)の演算のサポートやWeakReferenceの追加など。

## CLDCとMIDPの対応関係

  - CLDC 1.0 - MIDP 1.0
  - CLDC 1.1 - MIDP 2.0, 2.1
  - CLDC 1.1.1 - MIDP 3.0 (ただし、CLDC 1.1.1の仕様は策定中)

## 外部リンク

  - [CLDC ホームページ](http://www.oracle.com/technetwork/java/javame/tech/cldc-jsp-141864.html)
  - [JSR 30](http://www.jcp.org/en/jsr/detail?id=30) (CLDC 1.0)
  - [JSR 139](http://www.jcp.org/en/jsr/detail?id=139) (CLDC 1.1)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")