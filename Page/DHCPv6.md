> この記事は[DHCPv6](https://ja.wikipedia.org/wiki/DHCPv6)から翻訳されています。


**Dynamic Host Configuration Protocol for IP Version 6**（DHCP for IPv6、**DHCPv6**）とは、[コンピュータ](../Page/コンピュータ.md "wikilink")が[ネットワーク接続する際に必要な情報を自動的に割り当てる](../Page/コンピュータネットワーク.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")の [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") と共に用いられる版のことをいう。

[IPv4](../Page/IPv4.md "wikilink") と共に用いられる版は DHCPv4 と呼ばれるが、現在のところは単に [DHCP](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink") というときは DHCPv4 を指すことが多い。

IPv6 においては、ステートレス・アドレス自動設定によって、DHCP を使わなくてもインタフェースにアドレスを与えることができる。しかし、インタフェースにそれ以外のアドレス（[DNS](https://ja.wikipedia.org/wiki/DNS "wikilink")サーバのアドレスなど）を与えることが必要な場合もある。DHCPv6 \[RFC 3315\] を使用することによって、このような場合に DHCPv4 と同様に DHCP サーバからインタフェースにアドレスを配布することができる。また、ステートレス・アドレス自動設定とは違って、[IPアドレス](../Page/IPアドレス.md "wikilink")だけでなく [DNS](../Page/Domain_Name_System.md "wikilink") サーバ、ドメイン名や他のサーバのアドレスを合わせて配布することができる。

DHCPv6 と DHCPv4 との間に互換性はない。DHCPv4 においては DHCP を使用して設定するかどうかはホストが決定するが、DHCPv6 においてはルータ広告のオプションによって通知される。一つのインタフェースに異なる情報源から異なる設定情報が届くこともある。

## ガイドライン

DHCPv6 開発の初期に次のようなガイドラインが決められた \[Hag 07\]。

  - DHCP とステートレス・アドレス自動設定機能を組み合わせることができなければならない。
  - DHCP の設定と他の機構 (例えばステートレス・アドレス自動設定機能) との組み合わせ方は管理者が決められる。
  - クライアントを手作業で設定する必要がない。
  - DHCP によって 1 つのインタフェースに複数のアドレスを設定できなければならない。
  - サブネットごとに DHCP サーバがなくてもよい。リレー・エージェントは DHCP [パケット](../Page/パケット.md "wikilink")を転送できなければならない。
  - 複数の DHCP サーバから返される複数の応答をクライアントが処理できなければならない。
  - DHCP によって一部のクライアントだけに設定することができるサブネットが作れなければならない。
  - DHCP はルータの存在・不在に依存しない。ルータが必要になるのはステートレス・アドレス自動設定機能を利用するときだけである。
  - DHCP は割り当てられたアドレスを DNS の動的更新時に登録できなければならない。また、管理者は手動による DNS 更新を選択することもできる。
  - DHCP はネットワークのアドレス変更をサポートするとともに、この作業が容易に実現できるようにしなければならない。

## DUID (DHCP 固有識別子)

DHCP のクライアントとサーバには、それぞれ DUID (DHCP Unique Identifier, DHCP 固有識別子) が与えられる。DUID はすべてのサーバとクライアントの間で一意でなければならない。また、DUID は変更してはならない。DUID は 2 [オクテットのコードとそれにつづく可変長の識別子とで構成されている](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。つぎのような 3 種類の異なる DUID が定義されている \[RFC 3315\]。

  - DUID-LLT - リンク層アドレス + 時刻 (LLT = Link-Layer-Time)
  - DUID-EN - インタフェースの製造者番号を元にしたベンダ固有の一意な ID (EN = Enterprise Number)
  - DUID-LL - リンク層アドレス (LL = Link Layer)

## アイデンティティ・アソシエーション

アイデンティティ・アソシエーション (IA, Identity Association) とは、サーバとクライアントがアドレスの集合を識別・管理するために使用するオブジェクトである。IA はオブジェクトに対応する IAID によって識別される。IA は個々の識別情報を格納している。クライアントは DHCP によって設定されるインタフェース 1 個について、少なくとも 1 個の IA を持ち、それに対応する IAID を一意に決めなければならない。IA はクライアントがそのインタフェースに合わせた設定をサーバから受信するときに使用される。

## ヘッダ形式

DHCPv6 のヘッダ形式は DHCPv4 と比べるとかなり簡略化されている。クライアントとサーバとの間で交換される DHCP メッセージのヘッダ形式は次の通りである。

`      0                   1                   2                   3`
`      0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1`
`     +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`     |    msg-type   |               transaction-id                  |`
`     +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`     |                                                               |`
`     .                            options                            .`
`     .                           (variable)                          .`
`     |                                                               |`
`     +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

## メッセージ種別

メッセージ種別 (msg-type) フィールドは次のようなメッセージ種別を含む。

  - 要請 (Solicit, 1) - サーバの場所を突き止める要請メッセージをクライアントが送信する。

<!-- end list -->

  - 広告 (Advertise, 2) - クライアントから受信した要請メッセージに応えて、DHCP サービスで利用可能であることを示す広告メッセージをサーバが送信する。

<!-- end list -->

  - 要求 (Request, 3) - 特定のサーバの IP アドレスを含む設定パラメータを要求する要求メッセージをクライアントが送信する。

<!-- end list -->

  - 確認 (Confirm, 4) - クライアントに割り当てられたアドレスがクライアントが接続されたリンクにおいてまだ適切であるかどうかを決定するため、利用可能なサーバにクライアントが確認メッセージを送信する。

<!-- end list -->

  - 更新 (Renew, 5) - クライアントに割り当てられたアドレスのリース期間を延長し、他の設定パラメータを更新するために、クライアントのアドレスと設定パラメータを供給したサーバにクライアントが更新メッセージを送信する。

<!-- end list -->

  - 再結合 (Rebind, 6) - クライアントに割り当てられたアドレスのリース期間を延長し、他の設定パラメータを更新するために利用可能なサーバにクライアントが再結合メッセージを送信する。このメッセージはクライアントが更新メッセージに対する応答を受け取らなかった後に送信する。

<!-- end list -->

  - 応答 (Reply, 7) - 次のうちのいずれかである。サーバがクライアントから受け取った要請、要求、更新、再結合メッセージに応えて、割り当てられたアドレスと設定パラメータを含む応答メッセージを送信する。サーバが情報要求メッセージに応えて、設定パラメータを含む応答メッセージを送信する。サーバが確証メッセージに応えて、クライアントが接続されているリンクにクライアントに割り当てられたアドレスが適切であるかによって、確認か否認の応答メッセージを送信する。サーバが解放あるいは辞退メッセージの受領を確認する応答メッセージを送信する。

<!-- end list -->

  - 解放 (Release, 8) - クライアントに割り当てられたアドレスを使わなくなったことを示すため、アドレスをクライアントに割り当てたサーバにクライアントが解放メッセージを送信する。

<!-- end list -->

  - 辞退 (Decline, 9) - サーバがクライアントに割り当てたアドレスに対し、クライアントが接続されているリンク上においてそのアドレスがすでに使用されていることを認識したときに、クライアントがサーバに辞退メッセージを送信する。

<!-- end list -->

  - 再設定 (Reconfigure, 10) - サーバがクライアントに新規の設定パラメータまたは更新された設定パラメータがあることを通知するのに使用される。更新情報の受信のためには、クライアントがサーバに更新メッセージまたは情報要求メッセージを送信しなければならない。

<!-- end list -->

  - 情報要求 (Information request, 11) - クライアントへの IP アドレスの割り当てなしに設定パラメータを求めるため、サーバへの情報要求メッセージをクライアントが送信する。

<!-- end list -->

  - リレー転送 (Relay-forward, 12) - リレー・エージェントが直接或いは他のリレー・エージェントを通してサーバにメッセージを中継するリレー転送メッセージを送信する。受信メッセージ、クライアント・メッセージ或いは他のリレー・エージェントからのリレー転送メッセージはリレー転送メッセージにカプセル化される。

<!-- end list -->

  - リレー応答 (Relay-reply, 13) - リレー・エージェントがクライアントに配送するメッセージを含むリレー応答メッセージをサーバがエージェントへ送信する。リレー応答メッセージは宛先リレー・エージェントに配送のために他のリレー・エージェントに中継されるかもしれない。

DHCP サーバから設定情報交換を開始する手順は、DHCPv4 にはなかった、新しい機能である。例えば、DHCP ドメイン全体のアドレスを変更する、或いは新規のサービスやアプリケーションの追加に伴って全クライアントを再設定する必要が生じたときなどに、この機能を使用することができる。

## DHCPv6 オプション

DHCPv6 ヘッダのオプション・フィールドによって設定情報や設定パラメータを表す。その形式は次の通りである。

`    0                   1                   2                   3`
`    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1`
`   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`   |          option-code          |           option-len          |`
`   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`   |                          option-data                          |`
`   |                      (option-len octets)                      |`
`   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

オプション・コード (option-code) フィールドがオプションの種別を示す。オプション長 (option-length) フィールドがこのオプションの長さをオクテット単位であらわす。そして、オプション・データ (option-data) フィールドにこのオプションの内容が格納される。利用可能なオプションは次の通りである (RFC 3315 以外の RFC において記述されているものについては、その RFC の番号を記述した)。

  - クライアント識別子 (Client Identifier, 1) - クライアントとサーバの間でクライアントを識別する DUID を運ぶために使用する。

<!-- end list -->

  - サーバ識別子 (Server Identifier, 2) - クライアントとサーバの間でサーバを識別する DUID を運ぶために使用する。

<!-- end list -->

  - 非臨時アドレス・アイデンティティ・アソシエーション (IA_NA, Identity Association for Non-temporary Addresses, 3) - 非臨時アドレス・アイデンティティ・アソシエーション (IA_NA) と IA_NA に関連するパラメータと IA_NA に関連する非臨時 (一時的ではない) アドレスとを運ぶために使用する。

<!-- end list -->

  - 臨時アドレス・アイデンティティ・アソシエーション (IA_TA, Identity Association for Temporary Addresses, 4) - 臨時アドレス・アイデンティティ・アソシエーション (IA_TA)、IA_TA に関連するパラメータと IA_TA に関連するアドレスを運ぶために使用する。

<!-- end list -->

  - IA アドレス (IA Address, 5) - IA_NA か IA_TA と関連した IPv6 アドレスを指定するために使用する。

<!-- end list -->

  - オプション要求 (Option Request, 6) - オプション要求オプションはクライアント-サーバ間のメッセージでオプションのリストを確認するために使用する。

<!-- end list -->

  - 優先度 (Preference, 7) - クライアントがサーバを選択する際に影響を与えるためにサーバからクライアントに送信される。

<!-- end list -->

  - 経過時間 (Elapsed Time, 8) - クライアントが DHCP トランザクションを開始してからの時間を 1/100 秒単位で示す。

<!-- end list -->

  - リレー・メッセージ (Relay Message, 9) - リレー転送メッセージあるいはリレー応答メッセージによって DHCP メッセージをカプセル化する。

<!-- end list -->

  - 認証 (Authentication, 11) - DHCP メッセージの身元 (identity) と内容を認証するための認証情報を運ぶ。

<!-- end list -->

  - サーバ・ユニキャスト (Server Unicast, 12) - クライアントがサーバへ[ユニキャスト](https://ja.wikipedia.org/wiki/ユニキャスト "wikilink")・メッセージを送れることを示すために、サーバはクライアントにこのオプションを送信する。

<!-- end list -->

  - 状態コード (Status Code, 13) - このオプションを含む DHCP メッセージやオプションと関係する状態表示を返す。

<!-- end list -->

  - 急速コミット (Rapid Commit, 14) - アドレス配布のために常の 4 個のメッセージの交換によるシーケンスのかわりに 2 個だけのメッセージの交換によるシーケンスを使用することを通知するのに使用する。

<!-- end list -->

  - ユーザ・クラス (User Class, 15) - そのユーザ・クラス・オプションが表すユーザやアプリケーションの種類を指定するためにクライアントによって使用される。

<!-- end list -->

  - ベンダ・クラス (Vendor Class, 16) - クライアントが実行されているハードウェアを生産したベンダを識別するためにクライアントによって使用される。

<!-- end list -->

  - ベンダ固有情報 (Vendor-specific Information, 17) - ベンダ固有の情報を交換するためにクライアントとサーバによって使用する。

<!-- end list -->

  - インタフェース識別子 (Interface-Id, 18) - リレー・エージェントはクライアント・メッセージを受信したインタフェースを識別するインタフェース識別子オプションを送信するかもしれない。

<!-- end list -->

  - 再設定メッセージ (Reconfigure Message, 19) - クライアントが更新メッセージや情報要求メッセージに応答するかどうかを示すため、サーバが再設定メッセージに再設定メッセージオプションを含める。

<!-- end list -->

  - 再設定受入 (Reconfigure Accept, 20) - クライアントがサーバに再設定メッセージの受信ができる事を示すために使用する。また、サーバがクライアントに再設定メッセージを受け入れるべきかどうかをつたえるためにも使用する。

<!-- end list -->

  - SIP サーバ・ドメイン名リスト (SIP Servers Domain Name List, 21) - 1 個以上の [SIP](../Page/Session_Initiation_Protocol.md "wikilink") サーバのドメイン名を通知するために使用する \[RFC 3319\]。

<!-- end list -->

  - SIP サーバ IPv6 アドレス・リスト (SIP Servers IPv6 Address List, 22) - 1 個以上の SIP サーバの IPv6 アドレスを通知するために使用する \[RFC 3319\]。

<!-- end list -->

  - DNS Recursive Name サーバ (DNS Recursive Name Server, 23) - 1 個以上の DNS Recursive Name サーバの IPv6 アドレスを通知するために使用する \[RFC 3646\]。

<!-- end list -->

  - ドメイン検索リスト (Domain Search List, 24) - クライアントがホスト名の解決に使用するドメイン検索リストを指定する。このオプションは他の名前解決機構には適用されない \[RFC 3646\]。

<!-- end list -->

  - プレフィクス委譲のためのアイデンティティ・アソシエーション (IA_PD, Identity Association for Prefix Delegation, 25) - プレフィクス委譲アイデンティティ・アソシエーション、IA_PD に関連するパラメータと IA_PD に関連するプレフィクスとを運ぶために使用する \[RFC 3633\]。

<!-- end list -->

  - IA_PD プレフィクス (IA_PD Prefix option, 26) - IA_PD に関係づけられた IPv6 アドレス・プレフィクスの指定のために使われる \[RFC 3633\]。IA_PD プレフィクス・オプションは IA_PD オプション・フィールドのなかにカプセル化されなければならない。

<!-- end list -->

  - ネットワーク情報サービス (NIS) サーバ IPv6 アドレス・リスト (Network Information Service (NIS) Servers, 27) - 1 個以上の [NIS](../Page/ネットワーク・インフォメーション・サービス.md "wikilink") サーバの IPv6 アドレスを通知するために使用する \[RFC 3898\]。

<!-- end list -->

  - ネットワーク情報サービス V2 (NIS+) サーバ IPv6 アドレス・リスト (Network Information Service V2 (NIS+) Servers, 28) - 1 個以上の NIS+ サーバの IPv6 アドレスを通知するために使用する \[RFC 3898\]。
  - ネットワーク情報サービス (NIS) サーバ・ドメイン名リスト (Network Information Service (NIS) Domain Name, 29) - 1 個以上の NIS+ サーバの IPv6 アドレスを通知するために使用する \[RFC 3898\]。

<!-- end list -->

  - ネットワーク情報サービス V2 (NIS+) サーバ・ドメイン名リスト (Network Information Service (NIS) Domain Name, 30) - 1 個以上の NIS+ サーバの IPv6 アドレスを通知するために使用する \[RFC 3898\]。

<!-- end list -->

  - SNTP サーバ IPv6 アドレス・リスト (Simple Network Time Protocol (SNTP) Servers, 31) - 1 個以上の [SNTP](../Page/Simple_Network_Time_Protocol.md "wikilink") サーバの IPv6 アドレスを通知するために使用する \[RFC 4075\]。
  - 情報更新時間 (Information Refresh Time, 32) - DHCPv6 によって得られる情報を更新する時間の上限を指定する \[RFC 4242\]。

<!-- end list -->

  - リレー・エージェント遠隔 ID (Relay Agent Remote-ID, 37) - ATM などの回路を終端するリレー・エージェントが回路端点の遠隔ホストを識別するために使用する \[RFC 4649\]。

<!-- end list -->

  - リレー・エージェント購読者 ID (Relay Agent Subscriber-ID, 38) - リレー・エージェントが購読者に安定な識別子を与えるために使用する \[RFC 4580\]。

<!-- end list -->

  - DHCPv6 クライアント FQDN (DHCPv6 Client FQDN, 39) - DHCP サーバがクライアントの FQDN ([Fully Qualified Domain Name](../Page/Fully_Qualified_Domain_Name.md "wikilink")) を知るため、または FQDN の更新の交渉のために使用される \[RFC 4704\]。

## 関連 RFC

  - RFC 3315 - Dynamic Host Configuration Protocol for IPv6 (DHCPv6)
  - RFC 3319 - Dynamic Host Configuration Protocol (DHCPv6) Options for Session Initiation Protocol (SIP) Servers
  - RFC 3633 - IPv6 Prefix Options for Dynamic Host Configuration Protocol (DHCP) version 6
  - RFC 3646 - DNS Configuration options for Dynamic Host Configuration Protocol for IPv6 (DHCPv6)
  - RFC 3898 - Network Information Service (NIS) Configuration Options for Dynamic Host Configuration Protocol for IPv6 (DHCPv6)
  - RFC 4075 - Simple Network Time Protocol (SNTP) Configuration Option for DHCPv6
  - RFC 4242 - Information Refresh Time Option for Dynamic Host Configuration Protocol for IPv6 (DHCPv6)
  - RFC 4580 - Dynamic Host Configuration Protocol for IPv6 (DHCPv6) Relay Agent Subscriber-ID Option
  - RFC 4704 - The Dynamic Host Configuration Protocol for IPv6 (DHCPv6) Client Fully Qualified Domain Name (FQDN) Option

## 参考文献

  - \[Hag 07\] Silvia Hagen, “IPv6Essentials, Second Edition”, O'Reilly, 2007. (邦訳: 市原 英也 監訳, “IPv6 エッセンシャルズ 第 2 版”, オライリー・ジャパン, 2007).

[de:Dynamic Host Configuration Protocol\#DHCPv6](https://ja.wikipedia.org/wiki/de:Dynamic_Host_Configuration_Protocol#DHCPv6 "wikilink")

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:IPv6](https://ja.wikipedia.org/wiki/Category:IPv6 "wikilink")