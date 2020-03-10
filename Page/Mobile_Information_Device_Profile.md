> この記事は[Mobile Information Device Profile](https://ja.wikipedia.org/wiki/Mobile_Information_Device_Profile)から翻訳されています。


**Mobile Information Device Profile**（略称**MIDP**）は、[携帯電話](../Page/携帯電話.md "wikilink")や[PDAのような](../Page/携帯情報端末.md "wikilink")[組み込み](https://ja.wikipedia.org/wiki/組み込み "wikilink")機器での[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の利用について記述した仕様である。MIDPは [Java ME](../Page/Java_Platform,_Micro_Edition.md "wikilink") フレームワークの一部である。MIDPは[CLDCと組み合わせて利用する](https://ja.wikipedia.org/wiki/Connected_Limited_Device_Configuration "wikilink")。

## 歴史

MIDPは以下の三種類が[JCPの下で開発された](../Page/Java_Community_Process.md "wikilink")。

  - JSR 37(MIDP 1.0) - [2000年](../Page/2000年.md "wikilink")[9月19日](../Page/9月19日.md "wikilink")承認
  - JSR 118(MIDP 2.0, 2.1) - [2002年](../Page/2002年.md "wikilink")[11月20日](../Page/11月20日.md "wikilink")承認
  - JSR 271(MIDP 3.0) - [2009年](../Page/2009年.md "wikilink")[12月9日](../Page/12月9日.md "wikilink")承認

## 日本での採用

日本では[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（ezplus、[EZアプリ (Java)](../Page/EZアプリ_\(Java\).md "wikilink")、[オープンアプリプレイヤー](https://ja.wikipedia.org/wiki/オープンアプリプレイヤー "wikilink")）、[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")（[S\!アプリ](../Page/S!アプリ.md "wikilink")）、[ウィルコム](../Page/ウィルコム.md "wikilink")で採用されている。[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")はMIDPでは無く、[DoJaプロファイル](../Page/DoJaプロファイル.md "wikilink")である。

## Lightweight User Interface Toolkit

MIDP上で動く、高レベルなUIライブラリとして、[Lightweight User Interface Toolkit](https://ja.wikipedia.org/wiki/:en:Lightweight_User_Interface_Toolkit "wikilink") (LWUIT)も提供されている。[Swing](../Page/Swing.md "wikilink")風のAPIと機能を提供している。

## 開発ツール

SDK としては、Java ME 全体の SDK として、Java ME SDK 3.0 が配布されている。

MIDPアプリケーションを開発するにはいくつかの異なった方法がある。コードはメモ帳のようなテキストエディタで記述するか、またGUIを持ったNetBeansまたはEclipse(適切なプラグインを組み込む)のような高度な統合環境を利用できる。また、[Motorola](https://ja.wikipedia.org/wiki/Motorola "wikilink")によってEclipseベースの統合開発環境「MOTODEV」が無償配布されている。

## MIDP 1.0から存在するAPI

コアAPIはConnected Limited Device Configuration(CLDC)コンフュギレーションを基礎として定義されている。

### javax.microedition.io

I/O操作に関してJava ME仕様クラスを含む。

### javax.microedition.lcdui

GUIで使用されるJava ME仕様クラスを含む。通常、携帯電話は液晶ディスプレイ(LCD)を使用するためLCD UIと呼ばれる。 このAPIは固有のディスプレイ技術用に特化しているわけではない。

### javax.microedition.rms

Java ME用の永久ストレージの操作を含む。

### javax.microedition.midlet

Java MEアプリケーションの基本クラスを含む。

## MIDP 2.0で追加されたAPI

MIDP 2.0ではゲームおよびマルチメディアAPIの導入といくつかのオプションパッケージが追加された。

### javax.microedition.media

マルチメディア再生に関する基本クラスを含む。おそらくJSR 135であるJava Mobile Media APIのサブセットがある。

### javax.microedition.lcdui.game

簡単な2Dスプライトをベースとしたゲームを支援するゲームAPI。

### javax.microedition.pki

セキュアな接続に関する証明API。

## MIDP 1.0 の制約

MIDP 1.0はキー状態の取得ができない。MIDP 1.0はアクティブレンダリングAPIを持っていない。MIDP 1.0はオーディオをサポートしていない。MIDP 1.0はHTTPだけサポートしている。仕様に実装の自由があるため、実装において違いが生じる。

## 外部リンク

  -
  - [JSR 37](http://www.jcp.org/en/jsr/detail?id=37) (MIDP 1.0)

  - [JSR 118](http://www.jcp.org/en/jsr/detail?id=118) (MIDP 2.0)

  - [JSR 271](http://www.jcp.org/en/jsr/detail?id=271) (MIDP 3.0)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:携帯電話アプリ](https://ja.wikipedia.org/wiki/Category:携帯電話アプリ "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")