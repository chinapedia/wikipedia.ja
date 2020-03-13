> この記事は[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS)から翻訳されています。


**OpenVMS** (Open Virtual Memory System) は、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") （DEC、現在は[ヒューレット・パッカード・エンタープライズ](https://ja.wikipedia.org/wiki/ヒューレット・パッカード・エンタープライズ "wikilink")） によって設計された、[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")、[バッチ処理](../Page/バッチ処理.md "wikilink")および[トランザクション](../Page/トランザクション.md "wikilink")処理用の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。当初は単に**VMS**と一般的には呼ばれており、元々は[VAX](../Page/VAX.md "wikilink")システム上で動作していたが、後に[DEC Alphaと](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Itanium](../Page/Itanium.md "wikilink")に移植された。 [2014年](../Page/2014年.md "wikilink")、ヒューレット・パッカードは**VMS Software, Inc.**にOpenVMSの将来のリリースを開発する独占的な権利を与えると発表した。

## 経緯

### 起源と名前の変遷

[1975年](../Page/1975年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")、[PDP-11](../Page/PDP-11.md "wikilink")用に32[ビット](../Page/ビット.md "wikilink")の仮想アドレス拡張を設計するために、DECはコードネーム**Star**という[ハードウェア](../Page/ハードウェア.md "wikilink")のプロジェクトを開始した。それに伴って、Starファミリのプロセッサ用に[RSX-11](https://ja.wikipedia.org/wiki/RSX-11 "wikilink")Mを基にした全く新しい[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を開発すべく、コードネーム**Starlet**という[デヴィッド・カトラー](../Page/デヴィッド・カトラー.md "wikilink")率いる[ソフトウェア](../Page/ソフトウェア.md "wikilink")のプロジェクトも1975年7月に開始された。これら2つのプロジェクトは当初から緊密に統合されていた。Star・Starletの両プロジェクトは、[VAX](../Page/VAX.md "wikilink")-11/780コンピュータと**VAX-11/VMS**オペレーティング・システムとして結実した。

年を経るにつれて製品名は変化していった。[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")にはバージョン2.0のリリースに伴って**VAX/VMS**と改名された*（同時にVAX-11コンピュータは単にVAXと改名された\[最初のVAXコンピュータは[1984年](../Page/1984年.md "wikilink")発表のVAX8600である\]）*。[1991年](../Page/1991年.md "wikilink")には、[POSIX](../Page/POSIX.md "wikilink")や[UNIX](../Page/UNIX.md "wikilink")[互換性](../Page/互換性.md "wikilink")といった業界標準のサポートを示唆し、さらにはDECの64ビットDEC Alpha [RISC](../Page/RISC.md "wikilink") [CPU](../Page/CPU.md "wikilink")への移植が進行中であったので、特定の[アーキテクチャとの繋がりを断ち切るために](../Page/コンピュータ・アーキテクチャ.md "wikilink")、**OpenVMS**と再度改名された。OpenVMSの名前はバージョン5.5のリリースとともに最初に登場した。

### DEC Alphaへの移植

VMSのDEC Alphaへの移植は、32ビットと64ビットの各[アーキテクチャ向けに別々のコードの作成を必要とした](../Page/コンピュータ・アーキテクチャ.md "wikilink")。[1992年](../Page/1992年.md "wikilink")にはAlpha AXPシステム用の最初のバージョンのOpenVMSがリリースされ、**OpenVMS AXP V1.0**と名づけられた。その後、OpenVMS AXP 1.5がVAX/VMS 5.5相当としてリリースされた。''（OpenVMS AXPの試作品クオリティのリリースに1.xといったバージョン番号を使用したことは顧客に混乱をもたらし、その後の移植版では繰り返されなかった）

[1994年](../Page/1994年.md "wikilink")には、OpenVMSバージョン6.1のリリースに伴って、VAXとAlpha版の機能（とバージョン番号）が同等になった。その後のVAXとAlpha版の製品のバージョン番号は一貫している。

### Itaniumへの移植

[2001年](../Page/2001年.md "wikilink")、[DECを買収した](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[コンパック](../Page/コンパック.md "wikilink")が[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP) へ吸収される直前に、OpenVMSを[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Itanium](../Page/Itanium.md "wikilink")アーキテクチャへ移植することを発表した。この移植はAlphaのコードを利用して行われ、VAXコードの成熟もあって移植プロセスは大幅に簡略化された。VAXコードベースの「スナップショット」がAlphaリリースの基として使用されたVAX版のAlphaへの移植と異なり、OpenVMSのAlphaとItenium版は共通のコードベースを利用してビルドされている。

最初の試作品クオリティのリリースである**OpenVMS IA64 V8.0**は、[2003年](../Page/2003年.md "wikilink")に出荷された。最初の製品クオリティのItanium版リリースである**OpenVMS V8.2**は[2004年](../Page/2004年.md "wikilink")後期に出荷される予定だったが、OpenVMS/Itanium移植版は2005年1月18日に発表された。V8.4でHP Integrity VMのゲストOSとしてサポートされた。

## 機能

OpenVMSは3つのレイヤに分けることができる:

  - [入出力](../Page/入出力.md "wikilink")、[メモリ管理](../Page/メモリ管理.md "wikilink")および[プロセス管理](../Page/プロセス管理.md "wikilink")サブシステムからなる[カーネル](../Page/カーネル.md "wikilink")
  - [en:DCL](https://ja.wikipedia.org/wiki/:en:DIGITAL_Command_Language "wikilink")、[en:RMS](https://ja.wikipedia.org/wiki/:en:Record_Management_Services "wikilink")、[:en:DECwindows](https://ja.wikipedia.org/wiki/:en:DECwindows "wikilink")（OpenVMSの[X11](https://ja.wikipedia.org/wiki/X11 "wikilink")準拠ウィンドウ・システム）および[en:RTLからなるコア](https://ja.wikipedia.org/wiki/:en:Run-time_Library "wikilink")・サービス
  - サポート、システム管理および[プログラミングのためのユーティリティ](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")・プログラム

### クラスタリング

OpenVMSは[クラスタリング](../Page/コンピュータ・クラスター.md "wikilink") （VAXclusterと呼ばれ、後に[VMScluster](https://ja.wikipedia.org/wiki/VMScluster "wikilink")となった）をサポートし、これにより、特別なハードウェアまたは[イーサネット](../Page/イーサネット.md "wikilink")で接続された複数のシステムが、処理、ジョブ・キュー、プリント・キューおよびディスク・ストレージ、ファイルとファイルレコードを共有することができる。この場合の共有は、分散ロックマネジャを使用したShared Everythingと呼ばれクラスタ内のすべてのシステムから同時にアクセスが可能である。イーサネットによるクラスタは、[Local Area Network](../Page/Local_Area_Network.md "wikilink") VMSclusterを意味するLAVCと呼ばれる。OpenVMSは単一クラスタあたり96ノードまでサポートし、VAXとAlphaシステム、あるいはAlphaとItaniumシステムが単一のクラスタ内で共存するような混成[アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")・クラスタもサポートする。（OpenVMS Engieeringは理論上3アーキテクチャクラスタも可能であることを示唆していたが、HPはサポートしない）

### Common Language Environment

OpenVMSの特筆すべき機能の一つがCommon Language Environmentであり、これは[プログラミング言語](../Page/プログラミング言語.md "wikilink")から独立して、[スタック](../Page/スタック.md "wikilink")や[レジスタの使用も含めた](../Page/レジスタ_\(コンピュータ\).md "wikilink")[関数や](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[サブルーチン](../Page/サブルーチン.md "wikilink")の呼び出し方を定義する、厳格に定められた標準である。これにより、対象となる言語の実装の詳細を知ることなく、ある言語（例えば[FORTRAN](../Page/FORTRAN.md "wikilink")）で書かれたサブルーチンを他の言語（例えば[C言語](../Page/C言語.md "wikilink")）から呼び出すことが可能である。OpenVMS自体は多種の異なる言語（[BLISS](../Page/BLISS.md "wikilink")、[VAX Macro](https://ja.wikipedia.org/wiki/VAX_Macro "wikilink")、[Ada](../Page/Ada.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[C](../Page/C言語.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[BASIC](../Page/BASIC.md "wikilink")など）によって実装されており、ほぼ全体が[C言語](../Page/C言語.md "wikilink")によって実装されている[UNIX](../Page/UNIX.md "wikilink")などのシステムとは対照的である。

### ファイルシステム

OpenVMSは、[ストリームや](../Page/ストリーム_\(プログラミング\).md "wikilink")[レコード](../Page/レコード.md "wikilink")志向の[入出力](../Page/入出力.md "wikilink")、[アクセス・コントロール・リスト](https://ja.wikipedia.org/wiki/アクセス・コントロール・リスト "wikilink")、ファイル・バージョニング等をサポートする非常にリッチな[ファイルシステム](../Page/ファイルシステム.md "wikilink")を持っている。[:en:OpenVMS filesystemを参照のこと](https://ja.wikipedia.org/wiki/:en:OpenVMS_filesystem "wikilink")。

### 時刻の管理

VMSは、[エポック](https://ja.wikipedia.org/wiki/エポック "wikilink")からの経過[ナノ](https://ja.wikipedia.org/wiki/ナノ "wikilink")秒を64[ビット](../Page/ビット.md "wikilink")で保持することで時刻を管理している。OpenVMSのエポックは、[修正ユリウス日](https://ja.wikipedia.org/wiki/修正ユリウス日 "wikilink")が0となる1858年11月17日の真夜中である。

## OpenVMS ホビイスト・プログラム

商用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でありながら、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にはOpenVMSホビイスト・プログラムの一環として、OpenVMSと複数のレイヤ化された製品（レイヤード・ソフトウェア）が、ホビイストの非商用利用については無料で利用可能となった。それ以降、OpenVMS用[ソフトウェア](../Page/ソフトウェア.md "wikilink")を生産している複数の会社が、自社の製品を同様の条件で利用可能とした。

## 関連項目

  - [DECnet](../Page/DECnet.md "wikilink")

## 外部リンク

  - [VMS Software, Inc.](http://www.vmssoftware.com/)
  - [日本HPE OpenVMS](http://www.hpe.com/jp/openvms)
  - [日本HP OpenVMS on Itanium](http://h50146.www5.hp.com/products/software/oe/openvms/itanium/)
  - [OpenVMS.org](http://www.openvms.org)
  - [OpenVMS Hobbyist Program](http://www.openvmshobbyist.com)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:1977年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1977年のソフトウェア "wikilink") [Category:ヒューレット・パッカードの製品](https://ja.wikipedia.org/wiki/Category:ヒューレット・パッカードの製品 "wikilink")