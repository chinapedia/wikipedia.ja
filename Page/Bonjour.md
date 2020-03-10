> この記事は[Bonjour](https://ja.wikipedia.org/wiki/Bonjour)から翻訳されています。


**Bonjour**（ボンジュール）は、[米アップルが開発したゼロ](../Page/アップル_\(企業\).md "wikilink")・コンフィギュレーション技術の実装である。主に[LANにおいて](../Page/Local_Area_Network.md "wikilink")、何の設定も行わず機器を使用可能にすることができる。[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") / [Mac OS X Server](https://ja.wikipedia.org/wiki/macOS_Server "wikilink") v10.2より[OS標準の機能として搭載され](../Page/オペレーティングシステム.md "wikilink")、当時は**Rendezvous**（**ランデブー**）と呼ばれたが、[Mac OS X v10.4から](../Page/Mac_OS_X_v10.4.md "wikilink")**Bonjour**という名前になった。[Windows向けに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**Bonjour for Windows**もリリースされており、[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")、[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Vistaに対応している](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

## 概要

Bonjourは元は[IETFの中で検討されていた](../Page/Internet_Engineering_Task_Force.md "wikilink")「[Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf "wikilink")」という技術がベースになっている。アップルはこれを独自に発展させ、仕様を公開することにより、現在では「Zero Configuration Networking」としてIETFにより標準化されている。

ここで「ゼロ・コンフィギュレーション (Zero Configuration)」とは、「何の設定も行わず機器を使用可能にする」技術のことである。

アップルには元々、ゼロ・コンフィギュレーション技術として[AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")というプロトコルがあった。これは何らかの機器をLANに接続すると、アドレスと名前がその機器に自動的に割り振られ、ユーザは何の設定も行うことなくその機器へのアクセスが可能になるものである。配線すればすぐにネットワークプリンタなどが使用可能になるメリットはあったが、反面、LANに接続されている機器が常にネットワークに新しく接続された機器がないかどうかを探索し続けるため、ネットワークに負荷がかかりがちになるという欠点もあった。

LANの主流が[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")をベースとした[イントラネット](../Page/イントラネット.md "wikilink")に移行してくると、AppleTalkとTCP/IPを混在させるための[MacIP](https://ja.wikipedia.org/wiki/MacIP "wikilink")、[IPTalk](https://ja.wikipedia.org/wiki/IPTalk_\(通信\) "wikilink")、EtherTalkといった技術が登場した。結果としてユーザと管理者は複雑な設定を強いられることになった。その後アップルはAppleTalkを段階的に廃し、TCP/IP上でのファイル共有 ([AFP](https://ja.wikipedia.org/wiki/Apple_Filing_Protocol "wikilink") over TCP) やサービス発見([SLP](../Page/サービス・ロケーション・プロトコル.md "wikilink"))を導入したが、設定は複雑なままであった。

こうした経緯からアップルは、AppleTalk及びSLPを置き換える技術としてBonjourを開発した。BonjourはTCP/IP上で動作し、AppleTalkと同様の使い勝手を持ちながら、遥かに低い負荷しかネットワークに要求しない。

「何の設定も行わず機器を使用可能にする」ことを目指している点では、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[Jini](../Page/Jini.md "wikilink")や[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[UPnP](https://ja.wikipedia.org/wiki/UPnP "wikilink")と似ている。

なお、Bonjourは[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")で「こんにちは」の意味。旧称のRendezvousは同じくフランス語で「待ち合わせ」の意味。

## 機能

Bonjourの代表的な機能は[IPアドレス](../Page/IPアドレス.md "wikilink")と[ホスト名](../Page/ホスト名.md "wikilink")の自動割り当て、サービスの自動探索である。ネットワークに接続された機器は[DHCPサーバのようなIPアドレスを割り当てるサーバも](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、[DNSのようなネームサーバも](../Page/Domain_Name_System.md "wikilink")、[ディレクトリサーバも必要としない](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")。機器がBonjourネットワークへ接続するとIPアドレスは自動的に割り当てられ、ホスト名は各機器にあらかじめ設定されたものが利用され、提供可能なサービスはホスト名と共に通知される。

IPアドレスの割り当てには[AutoIP](https://ja.wikipedia.org/wiki/AutoIP "wikilink")の技術が使われる。[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")のネットワークへ接続された場合、Bonjour対応機器は169.254.0.0/16の中から空いているアドレスを探索し、それを自らのIPアドレスとする。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の場合、LANインターフェースに自動で割り当てられる[リンクローカルアドレス](https://ja.wikipedia.org/wiki/リンクローカルアドレス "wikilink")があるので、それを利用する。

ホスト名は基本的に、各機器が名乗るホスト名を利用する。名前のルールは「マシン名＋サービス名＋プロトコル名＋ドメイン名」である。マシン名はユーザがその機器に対して設定したものを使い、サービス名にはその機器が提供するサービスが、プロトコル名にはTCP/IPの場合「._tcp」が、ドメイン名には「.local」が入る。

ホスト名の探索には[マルチキャスト](../Page/マルチキャスト.md "wikilink")DNS（UDPポート5353）を用いる。ホスト名を探索する際にはネットワークに接続された機器全てに対してホスト名を問い合わせ、一致したホストに対して接続を行う。ただしそのまま実装したのではネットワークにかかる負荷が大きくなってしまうため、あらかじめホスト名を[キャッシュ](../Page/キャッシュ.md "wikilink")するなど負荷を減らす工夫が行われている。

提供可能なサービスの一覧は、ホスト名の問い合わせにマルチキャストDNSが用いられていることを利用し、DNS resource recordsに入れられて通知される。なおこの「サービス」には、プリント機能など[ハードウェア](../Page/ハードウェア.md "wikilink")が提供するサービスのみに留まらず、音楽や画像の配信、[インスタントメッセージ](https://ja.wikipedia.org/wiki/インスタントメッセージ "wikilink")ングなど、[ソフトウェア](../Page/ソフトウェア.md "wikilink")が提供するサービスも含まれる。

Bonjourの特色は、デバイスではなくサービスを中心に据えていることである。特定のデバイスに対し提供しているサービスを問い合わせるのではなく、目的とするサービスを提供しているデバイスを探索するのである。例えばあるサーバは[Webサーバ](../Page/Webサーバ.md "wikilink")かもしれないが、同時に[FTPサービスを提供しているかもしれない](../Page/File_Transfer_Protocol.md "wikilink")。ひとつのデバイスが複数のサービスを提供していることは珍しくないし、負荷の分散を目的にサービスを提供するサーバを別のデバイスに移動させることもある。重要なのはデバイスではなくサービスであるという考え方である。

まずホスト名を解決しIPアドレスを用いて特定デバイスにサービスを問い合わせるのではなく、いきなり目的とするサービスを提供しているデバイスを探す。ネットワークに接続されたデバイス全てに対しマルチキャストで「FTPサービスを提供しているサーバはどれ？」と訊ねれば、該当するデバイスは手を挙げるので、それからホスト名を解決してアクセスを試みるのである。

## 負荷を減らす工夫

AppleTalk最大の欠点は、何よりもまずネットワークにかかる負荷であった。Bonjourではその負荷を減らすべく、様々な工夫がこらされている。

Bonjour対応の機器が新たにネットワークへ接続されると、その機器はまず自らにIPアドレスを割り当てた後、自らのアドレスとホスト名、さらに提供しているサービスの種類をネットワークにマルチキャストする。他の機器ではその情報をキャッシュし、次回のホスト名やサービスの問い合わせの際には、まずそのキャッシュされたデータを参照するようになる。

ただしそのままではネットワークから機器が取り外された場合に対応できず、動的に再構成されるネットワークには対応できなくなってしまうので、データは常に更新され続ける必要がある。このため、ネットワークに接続された機器は一定時間ごとにマルチキャストで提供可能なサービスの一覧をネットワークの全デバイスに要求する。このマルチキャストは回を重ねるごとに間隔が長くなるように設定されており、最初のマルチキャストはネットワークに接続された時に、2回目はその1秒後に、3回目はさらにその2秒後、4回目は4秒後、5回目は8秒後、6回目は16秒後と、時間は指数関数的に長くなっていく。この間隔の最大値は4096秒で固定されており、それ以上には大きくならない。

このように間隔が段々と長くなっていく理由は、ネットワークへ接続される機器は短時間で取り外されるものと長時間接続されるものの二種類に大別することができ、その中間というものがほとんど存在しないからである。例えばネットワークプリンタなども使用する時だけ電源を入れるか、あるいは朝から晩まで接続しっ放しかの二種類であり、数分ごとに接続切断を繰り返すケースはまずない。

こうしてマルチキャストされたデータは各ホストにキャッシュされる。各機器はネットワークに対して問い合わせを行う前にまずこのキャッシュされたデータを参照するようになっている。キャッシュに目的のデータがなかった場合はネットワークに対してマルチキャストで問い合わせを行うが、該当するアドレスやホスト名、サービスを提供している機器はその返答をやはりマルチキャストで行う。該当しない機器はもちろん沈黙を守るが、マルチキャストされたデータはもちろん受信しており、同様にそのデータをキャッシュに加えてデータベースを更新する。

あるホストがネットワークに対してサービスの一覧を要求した場合、問い合わせのパケットにはそのホストが「すでに知っているサービスの一覧」が含まれる。例えばネットワークにはすでに10のプリントサービスが存在し、問い合わせを行うホストがそのことを知っている場合、問い合わせのパケットにはその旨が記述される。リストに載っているプリントサービスは沈黙を守り、リストに載っていないプリントサービスのみが返答を行う仕組みである。

このようにBonjourは、データを可能な限りキャッシュし、ネットワークを探索する際にはまずそのキャッシュを参照することでネットワークへかかる負荷をギリギリまで減らしている。もちろんマルチキャストによる問い合わせが行われない場合に比較して負荷は高くなる傾向にあるものの、問題ないレベルに収まることがほとんどである。

## 欠点と制限

Bonjourにはもちろん欠点や制限も存在する。まずBonjourは、基本的にLAN内でしか利用することができず、原則的に[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")を越えることができない。ただしこれは、[DHCPと](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")[ダイナミックドメインネームシステム](../Page/ダイナミックドメインネームシステム.md "wikilink")(DDNS)を用いることで解決可能であり、その二つを用意すればルータを越えた運用が可能になる。ただし、IPv6ではこの限りではない。 なお、[Mac OS X v10.5においてBack](../Page/Mac_OS_X_v10.5.md "wikilink") to My Mac（どこでも My Mac）と呼ばれる機能が導入され、MobileMeのアカウントを持つユーザは広域でもホスト/サービスを参照できるようになった。実際この機能はDDNS等の技術を用いて実現されている。

またBonjourは、イベント制御の機能が弱い。例えばUPnPではきめ細かいイベント制御が可能になっているものの、Bonjourではこの部分にマルチキャストDNSやDDNSしか利用できないため、細かなコントロールを行うことができない。プリンタの制御については[IPPや](https://ja.wikipedia.org/wiki/Internet_Printing_Protocol "wikilink")[LPR](https://ja.wikipedia.org/wiki/LPR "wikilink")を用いることが決まっているが、その他の機器についてはまだ仕様が策定されておらず、検討中となっている。

対応機器の少なさも悩みである。UPnPと比べ、Bonjourは対応している機器が少ない。アップルは"AirTunes"（無線LAN経由での音楽再生機能）を搭載した[AirMac Expressなど](https://ja.wikipedia.org/wiki/AirMac#AirPort_Express "wikilink")、Bonjourの機能を生かした製品をリリースしているが、サードパーティーでは、現在対応を表明しているメーカーはほとんどがプリンターメーカーである。

UPnPが基本的にハードウェアのみに用途が限られているのに対し、Bonjourはハードウェア・ソフトウェアを問わず利用することができる。Bonjour対応ソフトウェアとして最も普及しているのはアップルの[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")(iTunes同士で音楽共有ができる)と[Safari](../Page/Safari.md "wikilink")(Bonjourに対応したWebサーバを自動的に探索しリストアップする)であるが、アップル以外のソフトウェアではAirfoil（iTunes以外のソフトウェアで[AirTunesを可能にする](https://ja.wikipedia.org/wiki/AirMac#AirPort_Express "wikilink")）、[Camino](https://ja.wikipedia.org/wiki/Camino "wikilink")、[シイラ (ウェブブラウザ)](https://ja.wikipedia.org/wiki/シイラ_\(ウェブブラウザ\) "wikilink")、[RealPlayer](https://ja.wikipedia.org/wiki/RealPlayer "wikilink")程度であり、あまり活用されているとは言い難い現状である。

またUPnPも開発過程こそ非公開であるものの、仕様はロイヤリティフリーで公開されているので、Bonjourがオープンソースであることは現在のところあまり目立ったアドバンテージにはなっていない。

## 関連項目

  - [LAN (Local Area Network)](../Page/Local_Area_Network.md "wikilink")
  - [プロトコル](../Page/プロトコル.md "wikilink")
  - [AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")
  - [UPnP](https://ja.wikipedia.org/wiki/UPnP "wikilink")
  - [イントラネット](../Page/イントラネット.md "wikilink")
  - [IPアドレス](../Page/IPアドレス.md "wikilink")
  - [Domain Name System](../Page/Domain_Name_System.md "wikilink")
  - [ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")
  - [Avahi](../Page/Avahi.md "wikilink")
  - [APIPA](https://ja.wikipedia.org/wiki/APIPA "wikilink")

## 外部リンク

  - [Apple - Support - Bonjour](http://www.apple.com/jp/support/bonjour/)
  - [Apple Developer Connection](http://developer.apple.com/jp/index.html)
  - [Bonjour Overview](http://developer.apple.com/documentation/Cocoa/Conceptual/NetServices/index.html)

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:2002年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2002年のソフトウェア "wikilink")