> この記事は[OS](https://ja.wikipedia.org/wiki/OS)から翻訳されています。


**セキュアOS**（Secure OS）とは、[セキュリティを強化した](../Page/コンピュータセキュリティ.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のことである。厳密な定義は存在していないが、[強制アクセス制御](https://ja.wikipedia.org/wiki/強制アクセス制御 "wikilink")(Mandatory Access Control:MAC)機能及び、[最小特権](https://ja.wikipedia.org/wiki/最小特権 "wikilink")を実現する機能を備えたものをそう呼ぶことが一般的である。

## 概要

セキュアOSは、その誕生の歴史を遡ると1970年代に考案された*[Trusted operating system](https://ja.wikipedia.org/wiki/w:Trusted_operating_system "wikilink")*に辿り着く。日本におけるセキュアOSは強制アクセス制御と最少特権にフォーカスされているが、本来はすべてのプロセスにおける資源に対するアクセスを仲裁する抽象的なマシンを意味する**リファレンスモニター**[1](http://www.ipa.go.jp/security/rfc/RFC2828-03RJA.html)（セキュアOSにおけるOSカーネルと捉えると理解が容易であろう）に注目すべきであり、このリファレンスモニターを実現するために強制アクセス制御や特権制御（最小特権は、特権制御機能の一部）が求められている。

リファレンスモニターには「利用する資源へのアクセスが迂回不可能なこと」「それ自身が改ざんできないこと」「実装が十分にシンプルで安全であることが証明できること」の３つが求められており、典型例としてはマイクロカーネルが該当すると言われている。このリファレンスモニターを含めて信頼できるコンピュータ処理基盤（ドライバ、ファームウェア、マイクロプロセッサを含めて）を*Trusted Computing base* (TCB)と呼ぶ。セキュアOSはTCBを構成しようとする時に不可欠な部分（カーネル）を提供する。

米国においては大学の講義でTrusted Operating Systemデザインというコースも存在するなど、情報を得る機会が多いのに比べて日本ではまだ正確な情報が殆ど存在しない（裏を返せば日本語の情報が少ないだけで、英語での情報は得られやすいということでもあるが）。

Trusted Operating Systemが各国の政府や軍需産業界が要求していたのと同じく、セキュアOSも各国の政府や軍需産業界で要求されているが、2000年から[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")が複数のオープンソース団体に経済的な支援を始めた結果、急速に開発が進んでいる。

なお、日本政府を中心として、仮想マシン技術をベースとした実装を模索する動きがある\[1\]。

## 名称

[日本語](../Page/日本語.md "wikilink")ではセキュアOSと呼ばれることがほとんどであり、セキュアオペレーティングシステムはほとんど使われていない。[英語](../Page/英語.md "wikilink")においては、*secure operating system*は不適切とされており、*[security focused operating system](https://ja.wikipedia.org/wiki/w:security_focused_operating_system "wikilink")* もしくは*[security-evaluated operating system](https://ja.wikipedia.org/wiki/w:security-evaluated_operating_system "wikilink")*が推奨されている。

## 実装

[Tailsなど](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink")、いくつかの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")がこのような用途向けにつくられている。商用では軍事レベルにも対応しているTrusted [Solaris](../Page/Solaris.md "wikilink")、Trusted [IRIX](../Page/IRIX.md "wikilink")、STOP OS、PitBull FSなどがある。

### BSDでの実装

  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [TrustedBSD](https://ja.wikipedia.org/wiki/TrustedBSD "wikilink")

### Linuxでの実装

  - [AppArmor](https://ja.wikipedia.org/wiki/AppArmor "wikilink") [2](http://en.opensuse.org/SDB:AppArmor)

  - [grsecurity](https://ja.wikipedia.org/wiki/grsecurity "wikilink")

  - (LIDS) [3](https://web.archive.org/web/20160124101504/http://www.lids.org/)

  - (RSBAC) [4](http://www.rsbac.org/)

  - [Security-Enhanced Linux](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink")

  - (Smack) [5](http://schaufler-ca.com/)

  - [TOMOYO Linux](https://ja.wikipedia.org/wiki/TOMOYO_Linux "wikilink") ([AKARI](https://ja.wikipedia.org/wiki/AKARI "wikilink"))

  - [Yama](https://ja.wikipedia.org/wiki/Yama "wikilink") [6](http://kernel.ubuntu.com/git?p=kees/linux-2.6.git;a=shortlog;h=refs/heads/yama)

### Windowsでの実装

  - [Windows NT系](../Page/Windows_NT系.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Linux Kernel Security](https://security.wiki.kernel.org/)

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:コンピュータセキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ "wikilink")

1.