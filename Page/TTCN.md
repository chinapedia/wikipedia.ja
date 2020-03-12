> この記事は[TTCN](https://ja.wikipedia.org/wiki/TTCN)から翻訳されています。


**TTCN** とは、[通信プロトコル](../Page/通信プロトコル.md "wikilink")や[Webサービス](../Page/Webサービス.md "wikilink")のテストに特化した[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。TTCN Test Suite には TTCN で書かれた多数の[テストケース](https://ja.wikipedia.org/wiki/テストケース "wikilink")から構成される。バージョン2まで、この言語は扱いにくい表形式で書かれており、その名称は ***Tree and Tabular Combined Notation***（[木構造と表を組み合わせた記法](../Page/木構造_\(データ構造\).md "wikilink")）の略とされていた。この言語を読み書きするには特別な TTCNエディタが必要であった。バージョン3で、TTCN は ***Testing and Test Control Notation***（テストおよびテスト制御記法）の略に変更され、一般的なプログラミング言語に近くなり、普通のエディタで読み書きできるようになった。TTCN-3 は TTCN-2 よりも柔軟性があり、通信プロトコルのテストだけでなく、他のソフトウェアの[テストにも使えるようになっている](../Page/ソフトウェアテスト.md "wikilink")。

各バージョンの実行にはそれぞれ別の[コンパイラ](../Page/コンパイラ.md "wikilink")または[インタプリタ](../Page/インタプリタ.md "wikilink")を必要とする。

TTCN は、[欧州電気通信標準化機構](../Page/欧州電気通信標準化機構.md "wikilink")(ETSI)や[国際電気通信連合](../Page/国際電気通信連合.md "wikilink")(ITU)で通信プロトコルのテストに広く使われている。ETSIでは、[ISDN](../Page/ISDN.md "wikilink")、[DECT](../Page/DECT.md "wikilink")、[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")、[EDGE](../Page/Enhanced_Data_Rates_for_GSM_Evolution.md "wikilink")、[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")、[DSRC](../Page/DSRC.md "wikilink")といった標準規格の適合試験のテストケースが TTCN で書かれている。最近では[Bluetooth](../Page/Bluetooth.md "wikilink")や[IPといった他のプロトコル標準のテストにも使われている](../Page/Internet_Protocol.md "wikilink")。

製品（電話、携帯電話、ネットワーク機器）に対してテストケースを実施することによって、それらの機器でのプロトコルの実装が通信規格に定義された要求仕様に合っているかを検証する。

TTCN は [ASN.1](https://ja.wikipedia.org/wiki/ASN.1 "wikilink") と組み合わせて使われることが多い。

## バージョン

  - TTCN-1: 最初の TTCN。あまり使われなかった。
  - TTCN-2: 第二世代の TTCN。TTCN-1 の修正版であり、今日でも広く使われている。
  - TTCN-3: 第三世代の最新の TTCN。

## 背景

適合試験（Conformance Test）では、（例えば TTCN で書かれた）よく定義された[テストケース](https://ja.wikipedia.org/wiki/テストケース "wikilink")を実施することでテストを行う。一方、[相互運用](https://ja.wikipedia.org/wiki/相互運用 "wikilink")試験（Interoperability Test）ではテスト対象製品とその逆の役割をする機器を接続してテストを行う（例えば、メールクライアントに対してはメールサーバ、電話に対しては電話網、Bluetooth付きヘッドホンに対してはBluetooth付き電話など）。

[IETFなどによるインターネット標準規格は今のところ相互運用試験を主に行っている](../Page/Internet_Engineering_Task_Force.md "wikilink")。

適合試験と相互運用試験は互いに補完する関係である。例えば、相互運用試験で問題が見つかれば、それを新たな適合試験のテストケースに応用して問題を発見できるように改良できる。

## 外部リンク

  - [ETSI PTCC](http://etsi.org/ptcc)
  - [ITU TTCN Studygroup](http://itu.int/ITU-T/studygroups/com07/ttcn.html)
  - [TTCN-3 community homepage](http://www.ttcn-3.org)
  - [TTCN-3 language reference](http://wiki.openttcn.com/media/index.php/OpenTTCN/Language_reference)
  - [TTCN-3 Quick Reference Card](http://www.blukaktus.com/TTCN3-QRC.html)

[Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:ソフトウェアテスティング](https://ja.wikipedia.org/wiki/Category:ソフトウェアテスティング "wikilink")