> この記事は[Sasser](https://ja.wikipedia.org/wiki/Sasser)から翻訳されています。


**Sasser**（サッサー）とは、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[2000の](../Page/Microsoft_Windows_2000.md "wikilink")[脆弱性](https://ja.wikipedia.org/wiki/セキュリティホール#脆弱性 "wikilink")「MS04-011」を悪用した[ワームの一種である](../Page/ワーム_\(コンピュータ\).md "wikilink")。

## 概要

[2004年](../Page/2004年.md "wikilink")[4月30日](../Page/4月30日.md "wikilink")に発見された\[1\]ワームで、[インターネット](../Page/インターネット.md "wikilink")に接続するだけで感染するという、[2003年](../Page/2003年.md "wikilink")8月に流行したBlasterタイプのワーム型ウイルスである。Blasterを上回る感染力で全世界に猛威を振るった\[2\]。Windows 2000の脆弱性「MS04-011」を悪用しており、Microsoft社が脆弱性「MS04-011」に対する対策プログラムを4月14日に発表してから約半月後に流行したというものである。感染すると、インターネット接続中に他のマシンに対してランダムに感染を試みるとともに、システムファイル「LSASS.exe」に作用しマシンをシャットダウンさせてしまう。また、一部の亜種では使用者を欺くために、lsasss.exeという類似のファイルを使用する。感染後のファイル削除などの破壊活動は行われないが、感染動作のために多数の[スレッドを作成するためにシステムリソースを消費し](../Page/スレッド_\(コンピュータ\).md "wikilink")、マシンスペックとSasserの種類（亜種にはより多くのスレッドを消費するものがある）によっては実用に耐えうることができないほどにシステム動作が低下する。

日本での被害状況の推移には、発覚時期が[ゴールデンウィーク](https://ja.wikipedia.org/wiki/ゴールデンウィーク "wikilink")に被っていたことも影響している。週休2日制の場合、2004年のゴールデンウィークは、間の平日である4月30日を休暇とすると7連続休暇となる状況であったが、[eEye Digital Securityによって発見された](https://ja.wikipedia.org/wiki/eEye_Digital_Security "wikilink")4月30日はゴールデンウィークの2日目近くであった。初期の感染者はコンシュマーPCが多く、その後、ゴールデンウィークが開ける5月6日に、感染マシンを企業ネットワークに接続するなどの形で急激に増えたと言われている\[3\]。

Microsoft社はウイルス作成に関する情報提供者に報奨金を用意するという方法を取り、これがSasser作者の逮捕に結びついたとされる。2004年5月7日に[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")で[逮捕](../Page/逮捕.md "wikilink")されたスベン・ヤシャンは17歳の時にSasserを作成した事を認め、2005年7月11日に[執行猶予](../Page/執行猶予.md "wikilink")付きの[禁固](../Page/禁錮.md "wikilink")1年9カ月と30時間の奉仕活動の判決が下りた\[4\]。

セキュリティ専門家によると、Sasserによる被害は数百万ドルに上るといわれている\[5\]。

## 動作原理

Sasserの動作原理は、eEye Digital Securityによって2004年5月1日時点でその詳細が明かされている\[6\]。

対象OSはWindows 2000、2003 Server、XP。感染すると、システム起動時に自動実行するプログラム群に自動登録される。2重感染は行われない。初回感染時および起動時にはTCPポート5554（亜種Eでは1023）で[FTPサーバーを起動し](../Page/File_Transfer_Protocol.md "wikilink")、128（亜種Cは1024）のスレッドを立ち上げ、それぞれが感染動作を行う。

感染先は[IPv4](../Page/IPv4.md "wikilink")ベースでランダムに決定されるが、大きく規則性がある。52%はランダムに決定され、23%は最初のオクテットが一致するもの、残りの27%は前半の2つのオクテットが一致するものを新たな感染先の候補とする。感染先が決まると、亜種Dは[ICMPエコーを用いた死活確認を行った後](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol#Echo_Message（エコー要求通知）・Echo_Reply_Message（エコー応答通知） "wikilink")、本家や他の亜種は死活確認なく、TCPポート445への接続の後、脆弱性「MS04-011」を用いた攻撃を行う。攻撃が成功すると、攻撃対象のマシンのTCPポート9996（亜種Eでは1022）にリモートシェルを実行可能な[バックドア](../Page/バックドア.md "wikilink")が設置されることになり、このバックドア経由でSasserプログラムが感染元のFTPサーバーからダウンロードされ、そのダウンロードされたプログラムが実行されることで、感染動作が完了する。

## 脚注

## 外部リンク

  - [Microsoft Windowsのセキュリティ修正プログラム (MS04-011)](http://www.microsoft.com/japan/technet/security/bulletin/MS04-011.asp)

[Category:コンピュータウイルス](https://ja.wikipedia.org/wiki/Category:コンピュータウイルス "wikilink")

1.
2.
3.
4.
5.
6.