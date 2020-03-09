> この記事は[BSD](https://ja.wikipedia.org/wiki/BSD)から翻訳されています。


**BSDの子孫**（ビーエスディーのしそん）では、[BSD](https://ja.wikipedia.org/wiki/BSD "wikilink")をもとに開発が行われている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) について解説する。主要なものに[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")、[BSD/OS](https://ja.wikipedia.org/wiki/BSD/OS "wikilink") などがある。一部では[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")も含める場合がある。これはmacOSの基礎部分に、[Mach](../Page/Mach.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")と[FreeBSD](../Page/FreeBSD.md "wikilink")の環境を組み合わせた[Darwinを利用しているからである](https://ja.wikipedia.org/wiki/Darwin_\(オペレーティングシステム\) "wikilink")。

FreeBSD、NetBSD、OpenBSD、DragonFly BSD、Darwinはフリーで提供されているが、BSD/OS、macOSは商用製品として提供されている。

かつてはBSDをもとに各ベンダが提供していた[UNIX](../Page/UNIX.md "wikilink")（BSD系UNIX）もあったが、現在のところ上記のOSをさす場合が多い。

## 概要

これらのOSは、[カリフォルニア大学バークレー校](https://ja.wikipedia.org/wiki/カリフォルニア大学バークレー校 "wikilink")の[Computer Systems Research Group](https://ja.wikipedia.org/wiki/Computer_Systems_Research_Group "wikilink") (CSRG) で開発されたBSDから派生している。なお、BSD自体の開発は4.4BSD Lite Release 2を最後にすでに終了しており、開発およびメンテナンスを行っていたCSRGは解散している。

非商用のBSD系Unixの多くは[AT\&T](../Page/AT&T.md "wikilink")のライセンスに抵触する部分をのぞいたBSDである4.3BSD Net/2より[386BSD](../Page/386BSD.md "wikilink")を経て派生している。386BSDの直系の子孫としては[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")があり、今でも精力的に開発されている。 [OpenBSD](../Page/OpenBSD.md "wikilink")や[DragonFly BSDは開発方針の違いや開発グループの諍いによってそれぞれ](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")[NetBSD](../Page/NetBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")から派生したOSで、OpenBSDはセキュリティー、DragonFly BSDはスレッド機構のFreeBSDと異なる方針での実装をそれぞれの目標にしている。

このほかにも、[ジュニパーネットワークス](https://ja.wikipedia.org/wiki/ジュニパーネットワークス "wikilink")のルーターに入っているJUNOS、[NEXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")、[OPENSTEP](https://ja.wikipedia.org/wiki/OPENSTEP "wikilink")、[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink")、[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")、[NEWS](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")-OSなどもBSDの子孫のOSとして知られている。

## 歴史

  - 1978年 1BSDがリリースされる
  - 1981年 4.1BSDがリリースされる
  - 1982年 SunOS 1.0がリリースされる
  - 1991年 4.3BSD Net/2がリリースされる
  - 1992年 386BSD、BSD/386（後のBSD/OS）がリリースされる
  - 1992年 USL vs BSDiの裁判が起きる
  - 1993年 NetBSD 0.8、FreeBSD 1.0がリリースされる
  - 1994年 USL vs BSDiの裁判の判決に沿って4.4BSD-Liteがリリースされる
  - 1994年 4.4BSD-Liteを元にNetBSD 1.0がリリースされる
  - 1995年 4.4BSD-Liteを元にFreeBSD 2.0がリリースされる
  - 1996年 喧嘩別れしてNetBSD 1.2を元に開発されたOpenBSD 2.0がリリースされる
  - 2004年 SMPにおける設計方針の違いによりFreeBSD 4.8から分岐して開発されたDragonFly BSD 1.0がリリースされる
  - 2014年 高い安全性維持のために厳格に保守的な開発を続けるOpenBSDに対して、安全性への制限を緩めて新しい機能を取り入れようとする設計方針の違いにより、OpenBSDから分岐して開発されたBitrig 1.0がリリースされる

## BSDの子孫達の棲み分け

各々のBSDの子孫達は[セキュリティー](https://ja.wikipedia.org/wiki/セキュリティー "wikilink")や[ファイルシステム](../Page/ファイルシステム.md "wikilink")、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")などで交流があり、複数のBSD系の[コミッター](https://ja.wikipedia.org/wiki/コミッター "wikilink")となっている開発者も存在する。 そんな中で、おのおのが目指すところの相違によりある種の棲み分けがなされている。

最近では[\*BSD Usage Statics](http://bsdstats.org/)にてBSD系の子孫達の利用者数などの統計を取るというプロジェクトが始まっており、これを見るとBSDの子孫達の利用者の分布がわかる。しかしながら、このプロジェクトはFreeBSDから始まったのでその分の下駄があることを考慮して見るべきである。

  - [FreeBSD](../Page/FreeBSD.md "wikilink")
    元々は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサーでのサポートの充実を念頭に置いて開発されており、x86環境でサポートしているハードウェアの数は多い。また、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")など複数のプロセッサをサポートするという方向性もある。
    newbus vs newconfigの争いに対する不公平な決着への反省から、選挙により選ばれた[コアチーム](https://ja.wikipedia.org/wiki/コアチーム "wikilink")がプロジェクトの今後の開発の方向性などを決めるというシステムを採用している。
    かつて[Computer Systems Research Group](https://ja.wikipedia.org/wiki/Computer_Systems_Research_Group "wikilink") (CSRG) でBSDの開発に参加していた[マーシャル・カーク・マキュージック](https://ja.wikipedia.org/wiki/マーシャル・カーク・マキュージック "wikilink") (Marshall Kirk McKusick) も[Soft updatesや](https://ja.wikipedia.org/wiki/Soft_updates "wikilink")[background fsckなどの](https://ja.wikipedia.org/wiki/background_fsck "wikilink")[UFSまわりの実装で参加している](https://ja.wikipedia.org/wiki/Unix_File_System "wikilink")。
  - [NetBSD](../Page/NetBSD.md "wikilink")
    多くの[コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")でBSD系Unixを動かすというのを念頭に置いて開発されているプロジェクトで、30種類以上のアーキテクチャで動作する。元々BSDがPDP-11からVAXに移植される際にアーキテクチャ依存なところ (machine dependent、略して MD) とアーキテクチャ非依存なところ (machine independent、略して MI) に分けられているが、NetBSDはこれをさらに推し進めていったものと言えよう。
    また、NetBSDは将来まで見越して拡張性のあるしっかりした設計をすることでも知られている。
    シャープ製パーソナルコンピュータ「[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")」シリーズ上でNetBSDが動くようにしたのは日本人であり、日本人の開発者も多い。
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
    NetBSDから分岐してセキュリティーに注意して開発が進められているBSD系Unixであり、最新版のリリースにおいてはインストール直後の標準状態にて10年で2つしかリモートから攻撃可能な[セキュリティホール](../Page/セキュリティホール.md "wikilink")が発見されていなかった。
    [OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH "wikilink")や[OpenNTPD](https://ja.wikipedia.org/wiki/OpenNTPD "wikilink")などセキュリティーに注力したソフトウェアの開発もよく行っている。
  - [DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")
    DragonFly BSDはFreeBSDとは異なったSMP対応をするためにFreeBSD 4.8Rから分岐したBSD系Unixであり、スケーラブルで理解しやすいカーネルを開発することを目指している。
    FreeBSDは共有する資源に対してロックを行うというモデルを採用しているのに対し、DragonFly BSDはカーネルサービス同士がメッセージをやりとりするというモデルをとっている。
    このような実装だとロックのために開発者が気を遣わなくともよいため、共有資源を使うような箇所の実装において、FreeBSDでカーネル開発をするのに比べて簡単に開発が行えるという利点がある。なお、FreeBSDでの実装とDragonFly BSDでの実装のどちらの実装が良いかという決着はまだ出ていない。
    DragonFly BSDはこのほかにも[プロセス](../Page/プロセス.md "wikilink")のチェックポイントを作成するという機能などFreeBSDにはない様々な興味深い機能が実装されている。
  - [Bitrig](https://ja.wikipedia.org/wiki/Bitrig "wikilink")
    OpenBSDはセキュリティ重視であり高い安全性を持つが、一方で新機能の導入に消極的という意見もあった\[1\]\[2\]。Bitrigは、過剰とも言われる安全性に対する制限を緩和することで新しい機能を積極的に取り入れていくという開発方針を採るとしている。

## 一覧

並び順は公開された日時に従う。

  - [386BSD](../Page/386BSD.md "wikilink")
      - [NetBSD](../Page/NetBSD.md "wikilink")
          - [OpenBSD](../Page/OpenBSD.md "wikilink")
              - [Bitrig](https://ja.wikipedia.org/wiki/Bitrig "wikilink")
      - [FreeBSD](../Page/FreeBSD.md "wikilink")
          - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
          - [DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")

## 脚注

<references/>

[Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.