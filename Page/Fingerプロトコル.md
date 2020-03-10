> この記事は[Finger](https://ja.wikipedia.org/wiki/Finger)から翻訳されています。


**Name/Fingerプロトコル**（ネームフィンガープロトコル）および **Finger ユーザー情報プロトコル**は、ユーザー情報など人間に纏わるステータスを交換するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")。

## Name/Fingerプロトコル

Name/Fingerプロトコルは、[RFC](../Page/Request_for_Comments.md "wikilink") 742（1977年12月）に基づいて David Zimmerman が *`name`*' および **`finger`** プログラムのインタフェースとして書いたもので、ネットワークサイト内の特定コンピュータまたは特定人物のステータスを表示するのに使われる。finger プログラムは1971年 Les Earnest が書いたもので、ネットワーク内の他のユーザーに関する情報を得たいという要望に応えたものであった。誰がログインしているかという情報は、その人にどこに行けば会えるかということを判断する材料となる。これは、ネットワーク上の[プレゼンス情報](https://ja.wikipedia.org/wiki/プレゼンス情報 "wikilink")技術の先駆けであった。

finger プログラム以前には、この種の情報を得るには **[`who`](https://ja.wikipedia.org/wiki/who_\(UNIX\) "wikilink")** プログラムを使ってログインユーザーのIDなどの情報を得て、そのリストを[指](../Page/指.md "wikilink")でたどって探す必要があった。Earnest が finger と名づけたのはこのためである\[1\]。

## Finger ユーザー情報プロトコル

Finger は[TCPのポート番号](../Page/Transmission_Control_Protocol.md "wikilink") 79 （十進）を使う。ローカルホストがリモートホストのFingerポートに対してTCPコネクションを確立する。リモートホストでは、そのコネクションの要求を処理するための RUIP (Remote User Information Program) が起動される。ローカルホストはRUIPにFingerクエリ仕様に基づいた1行の[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")を送信し、RUIPの応答を待つ。RUIPはそのクエリを受信して処理し、返答し、コネクションをクローズさせる。ローカルホストは答を受信すると、ローカル側のコネクションのクローズを行う。

Finger ユーザー情報プロトコルは **RFC 1288**（*The Finger User Information Protocol*、1991年12月）に基づいている。一般に、[サーバ](../Page/サーバ.md "wikilink")側の実装は **`fingerd`**（finger [daemon](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")）、[クライアント側の実装は](../Page/クライアント_\(コンピュータ\).md "wikilink") `name` と `finger` があり、その時点のシステムおよび特定人物に関するステータス情報を人間が読める形式で表示する。特にフォーマットは決まっておらず、コマンド行1行ぶんの内容をプロトコルの応答として返す。[UNIX](../Page/UNIX.md "wikilink")、[Unix系](../Page/Unix系.md "wikilink")システム、最近の[Windowsで実装されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

このプログラムは、あるユーザーがログインしているか、その[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")、フルネームなどの情報を提供する。そのような標準のユーザー情報以外に、そのユーザーの[ホームディレクトリ](https://ja.wikipedia.org/wiki/ホームディレクトリ "wikilink")に **`.project`** ファイルや **`.plan`** ファイルがあれば、その内容も表示する。これらのファイルの内容はユーザー自身が用意するもので、そのユーザーの現在の仕事などに関する便利な情報や、何らかの[ユーモア](https://ja.wikipedia.org/wiki/ユーモア "wikilink")を表す内容が含まれることが多い。

## セキュリティ上の懸念

メールアドレスやフルネームなどの詳細な情報は[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")黎明期には便利だったが、最近ではプライバシーやセキュリティ上の懸念が生じている。Finger 情報は[クラッカーに](../Page/クラッカー_\(コンピュータセキュリティ\).md "wikilink")[ソーシャル・エンジニアリング](../Page/ソーシャル・エンジニアリング.md "wikilink")攻撃の足がかりとして悪用されることが多い。Finger を利用して企業の従業員名、メールアドレス、電話番号などの一覧を得て、別の従業員のふりをして電子メールや電話で情報を聞きだすという手法が可能となる。また、fingerd 自身にもクラッカーが侵入に利用できる脆弱性がかつて存在した。[モリスワーム](https://ja.wikipedia.org/wiki/モリスワーム "wikilink")は fingerd などの脆弱性を利用して広まっていった。

以上のような理由で、かつてはよく使われていたが、1990年代にはほとんどのサイトがこのサービスを停止していった。よく知られている例外として、[ジョン・D・カーマック](https://ja.wikipedia.org/wiki/ジョン・D・カーマック "wikilink")と[ジャスティン・フランケル](https://ja.wikipedia.org/wiki/ジャスティン・フランケル "wikilink")は今でもステータス情報を時々更新している。2005年末、ジョン・カーマックは `.plan` サイトから[ブログ](../Page/ブログ.md "wikilink")に切り換えた。

## 関連項目

  - [モリスワーム](https://ja.wikipedia.org/wiki/モリスワーム "wikilink")

## 脚注

<references/>

## 外部リンク

  - RFC 742 （1977年12月）
  - RFC 1288 （1991年12月）
  - [finger(1)](https://linuxjm.osdn.jp/html/netkit/man1/finger.1.html) JM Project
  - [finger(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr0d/index.html) man page（SunOS リファレンスマニュアル）
  - [finger(1)](https://nixdoc.net/man-pages/HP-UX/man1/finger.1.html) man page（HP-UX リファレンス）
  - [History of the Finger protocol by Rajiv Shah](https://www.rajivshah.com/Case_Studies/Finger/Finger.htm)
  - \[<https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-xp/bb490908(v=technet.10>)?redirectedfrom=MSDN Microsoft TechNet Finger article\]

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink") [Category:1977年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1977年のソフトウェア "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.