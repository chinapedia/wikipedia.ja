> この記事は[Wake-on-LAN](https://ja.wikipedia.org/wiki/Wake-on-LAN)から翻訳されています。


**Wake-on-LAN**（ウェイク・オン・ラン、略称**WoL**あるいは**WOL**）は、コンピュータネットワーク（主にLAN）に繋がっているコンピュータの電源を遠隔で投入する技術あるいはその行為を指す。

## 概要

コンピュータネットワークに特定のパケットを送信させることにより、そのパケットの内容に該当するコンピュータが自ら電源を投入させる仕組みである。自明に、ネットワークの特性を生かしたコンピュータの電源操作が可能となる。

たとえば、次のような利点が考えられる。

  - 遠隔地\[1\]や、人間が立ち入ることが困難な場所（危険な場所、狭小な場所、高所など）にあるコンピュータの電源を投入することができる。
  - コンピュータプログラムが、他のコンピュータの電源を投入させることができる（人力を介さずに電源投入できる）。
  - 会社の営業所で数十台から数百台までのコンピュータが置かれている場合、従来の方法ではシステム管理者などが一台ずつ電源を投入しなければならず、台数や社屋が大きいほど非効率な作業となるが、Wake On LAN を利用した電源操作では、該当コンピュータを対象にしたマジックパケットをネットワークに送信することにより、複数台のコンピュータを一斉に電源投入できる。

Wake On LAN を利用するには マザーボード、ネットワークカード、BIOS、オペレーティングシステムなどが Wake On LAN に対応している必要がある。また、制御に用いるパケット（マジックパケット）にブロードキャスト送信を利用することから、異なるサブネットへの利用には構成の考慮が必要である。

## マジックパケット

マジックパケットは、FF:FF:FF:FF:FF:FFに続けて起動したい装置のMACアドレスを16回繰り返したデータパターン(AMD Magic Packet Format) が[ペイロードのどこかに含まれているようなパケットである](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。例えば、起動したい装置の[MACアドレス](../Page/MACアドレス.md "wikilink")が EE:EE:EE:00:00:01 の場合、

`FF:FF:FF:FF:FF:FF EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01`
`EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01`
`EE:EE:EE:00:00:01 EE:EE:EE:00:00:01 EE:EE:EE:00:00:01`

このような102バイトの信号が含まれるパケットが送られ、ターゲット機器にそのパケットが届くと、102バイトの信号を認識して電源ステート（例えば ACPI S ステート）が切り替えられ、装置の電源が入る。

最初の6バイトのFFは[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")を表すあて先 MAC アドレスではない。[Ethernet フレームの先頭からこのパターンを開始すると](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink") [EtherType](https://ja.wikipedia.org/wiki/EtherType "wikilink") フィールドが本来の意味ではなくなってしまう。通常は[ポート](../Page/ポート_\(コンピュータネットワーク\).md "wikilink") 7 または 9 の [UDP](https://ja.wikipedia.org/wiki/UDP "wikilink") パケット、あるいは [EtherType](https://ja.wikipedia.org/wiki/EtherType "wikilink")=0x0842 の Ethernet フレームのペイロードに埋め込まれる。

ターゲット機器はネットワークアダプタに通電こそされているものの、マジックパケットを待ち受けることしかしない状態であり、通常の IP や ARP に反応することはない。そのため、[IPアドレス](../Page/IPアドレス.md "wikilink")や MACアドレスでの到達性が保障されないため、マジックパケットは Ethernet ブロードキャストフレームとして送信されなければならない。

## 問題点

Wake On LAN を利用には、いくつか問題点が存在している。

### ネットワーク構成

マジックパケットは通常ブロードキャストとして送信される。ブロードキャスト送信では、送信する機器と受信する機器は同じブロードキャストドメインに所属しなければならないため、[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")を超えることはできない。Subnet directed broadcast送信\[2\]を行う方法もあるが 、ルータは通常これを許さない設定になっていることが多い。従って、サブネットの異なる装置の電源操作に、通常 WOL は使用できない\[3\]。

### コンピュータ側の問題

Wake-on-LAN の利用には、コンピュータ本体がシャットダウンしていても、[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")に対して電源を供給し続ける必要がある\[4\]。また、ネットワークカードがマジックパケットを認識した際の動作を、[BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") で設定しなければならない場合がある。これらの設定が不可能な場合、WOL による電源操作は利用できない（これらは電源操作を受ける側の設定であり、マジックパケットを送信する側には不要）。

とくに、ワイヤレスLANは接続の際にOS上での設定が必要なものが大半である為、PCの電源を切ったときにマジックパケットを受信できず、WOLによる電源操作が不可能なものが多い。この場合、ワイヤレスイーサネットコンバータ（ブリッジ）等を利用し、PCの電源状態に関わらずマジックパケットを受信させる必要がある。近年ではWake on Wireless LAN (WoWLAN) という仕組みも登場し、対応機器ではワイヤレスLANによる電源操作が可能な場合もある。

## Wake On LANの利用

マジックパケットを送信し、目標のPCを起動させ、[Secure Shellを使ってでそのPCに保存したファイルをネットワーク越しに取り出したり](../Page/Secure_Shell.md "wikilink")、[VNCや](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink")[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")などを利用して[GUIそのものを遠隔操作することが出来る](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

システム管理者にとってはメンテナンスなど、時間やコストの削減となるため重宝される。 複数のPCを同時に使う必要のある研究室などで、一人で複数台のPCを操作する場合、[CPU切替器で三台の本体に対して一組のモニタ](https://ja.wikipedia.org/wiki/KVMスイッチ "wikilink")、キーボード、マウスで操作する方法が採られることがあるが、環境によってはWOLで電源を操作し、VNCで様々な操作をすることで作業効率をあげる手段になりうる。

ブロードキャストドメイン単位に管理コンピュータを設置し、そこから起動対象となるコンピュータを一斉起動し、装置のメンテナンスを自動的に実行するソリューションがある。その一例として、[Microsoft Systems Management Serverがある](../Page/Microsoft_Systems_Management_Server.md "wikilink")。管理コンピューターにエージェントをインストールしておき、Systems Management Serverからメンテナンススクリプトを起動すると、エージェントは管理対象のコンピュータを順次起動し、[Microsoft Updateやシステム設定の変更等を実施し](https://ja.wikipedia.org/wiki/Microsoft_Update "wikilink")、最後にシャットダウンを行う。System Management Serverは管理対象に企業や学校といった大規模設備を想定しているシステムであるが、同様のことは[UNIX](../Page/UNIX.md "wikilink")でシェルスクリプトとリモートシェル（SSH等）、wolコマンドを組み合わせることで実現することができる。[アップルの](../Page/アップル_\(企業\).md "wikilink")[macOS Serverには前述のUNIXにおけるメンテナンスを行う機能が搭載されている](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")。

## 脚注

<references />

## 関連項目

  - [LAN](../Page/Local_Area_Network.md "wikilink")
  - [ATX電源](../Page/ATX電源.md "wikilink")
  - [マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")
  - [Wake-on-Modem](https://ja.wikipedia.org/wiki/Wake-on-Modem "wikilink")
  - [Wake-on-Ring](https://ja.wikipedia.org/wiki/Wake-on-Ring "wikilink")
  - [Advanced Configuration and Power Interface](../Page/Advanced_Configuration_and_Power_Interface.md "wikilink")(ACPI)

## 外部リンク

  - [Wake On LANでコンピュータを起動する － ＠IT](http://www.atmarkit.co.jp/fwin2k/win2ktips/715wol/wol.html)

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:有線通信](https://ja.wikipedia.org/wiki/Category:有線通信 "wikilink")

1.  他でも言及がある通り、同じサブネットに存在していない場合は、パケットが対象のコンピュータに届くよう間接的に送出させるしくみが必要である。
2.  異なるサブネットへのブロードキャスト送信を行う。
3.  対象のサブネット内で常時起動しているサーバなどにエージェントを起動させておき、処理を仲介させる構成を設けるなどにより対処する例がある。
4.  BIOS の設定で[サスペンド](https://ja.wikipedia.org/wiki/サスペンド "wikilink")の電源管理を S1 から S1\&S3 に変更するなど。