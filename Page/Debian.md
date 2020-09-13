> この記事は[Debian](https://ja.wikipedia.org/wiki/Debian)から翻訳されています。


**Debian**（ **デビアン**）または**Debian Project**は[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")のひとつである**Debian GNU/Linux**を中心とする[Unix系](../Page/Unix系.md "wikilink")システムのディストリビューションを作成しているプロジェクトである。名前の通り、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の精神の尊重と（そのため、システム全体も単に[Linux](../Page/Linux.md "wikilink")と呼ばれる事が多いのに対し、「[GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")」という呼称を積極的に使っている。呼称が分かれる経緯については*[GNU/Linux名称論争](https://ja.wikipedia.org/wiki/GNU/Linux名称論争 "wikilink")*もご覧ください。）、同プロジェクトによるプロダクトの積極的な採用などが特徴である。Linuxディストリビューションの他、[カーネル](../Page/カーネル.md "wikilink")（核）を[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")から[GNU Hurdや](../Page/GNU_Hurd.md "wikilink")[FreeBSD](../Page/FreeBSD.md "wikilink")のカーネルに置き換えた、[Debian GNU/Hurdや](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")[Debian GNU/kFreeBSDなどがある](https://ja.wikipedia.org/wiki/Debian_GNU/kFreeBSD "wikilink")。

## 概要

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")、必須なユーティリティ類のutil-linux（[:en:Util-linux](https://ja.wikipedia.org/wiki/:en:Util-linux "wikilink")）、プログラムの[ビルドに必要な](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")[GCCや](../Page/GNUコンパイラコレクション.md "wikilink")[GNU Binutils](../Page/GNU_Binutils.md "wikilink")、[coreutilsなどのその他の](../Page/GNU_Core_Utilities.md "wikilink")[Unix系](../Page/Unix系.md "wikilink")[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")をはじめ、その他[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")向けや[サーバ](../Page/サーバ.md "wikilink")運用向けなど多数の、計51,000以上のパッケージを提供している\[1\]。対象環境として現在10の[アーキテクチャ（環境）向けに開発されており](../Page/コンピュータ・アーキテクチャ.md "wikilink")\[2\]、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")や[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[32ビット](../Page/32ビット.md "wikilink")・[64ビット](../Page/64ビット.md "wikilink")[プロセッサ](../Page/プロセッサ.md "wikilink")、組み込み機器で使われる[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")などがそれには含まれている。低水準のパッケージ管理システムは[dpkg](https://ja.wikipedia.org/wiki/dpkg "wikilink")、高水準のパッケージ管理システムは[APT](../Page/APT.md "wikilink")である。[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")は各種のものがパッケージにあるが、Debian 8では導入時に選べるのは[GNOME](../Page/GNOME.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[Cinnamon](https://ja.wikipedia.org/wiki/Cinnamon "wikilink")、[MATE](https://ja.wikipedia.org/wiki/MATE_\(デスクトップ環境\) "wikilink")、[LXDE](https://ja.wikipedia.org/wiki/LXDE "wikilink")、[LXQt](https://ja.wikipedia.org/wiki/LXQt "wikilink")である。

Debian-kde.png|300px|Debian 7 (wheezy) KDE4.8 Plasmaデスクトップ Debian-wheezy-xfce-ja.png|300px|Debian 7 (wheezy) Xfce4.8デスクトップ Debian10_Gnome.png|300px|Debian 10 (buster) GNOME デスクトップ XFCE 4.12.3 on Debian 9.3.png|300px|Debian 9 (stretch) XFCE デスクトップ

その他の特徴として、Debianを母体として、さらに[調整や変更を加えた派生Linuxディストリビューションの作成が考慮されている](https://ja.wikipedia.org/wiki/カスタム#パーソナルコンピュータにおけるカスタム "wikilink")、という点がある。派生先には[Ubuntu](../Page/Ubuntu.md "wikilink")他多くの派生ディストリビューションが存在する。

インストーラ用のCD/DVD[イメージはWebからのダウンロード](../Page/ISO_9660.md "wikilink")、[BitTorrent](../Page/BitTorrent.md "wikilink")・[jigdo](https://ja.wikipedia.org/wiki/jigdo "wikilink")・uNetBootInなどで取得できる。さらに、インストーラーをオンライン再販業者から購入する事も可能である\[3\]。

Debian10-installation-menu.png| Debian 10 のインストール・メニュー Debian10-text-installer.png| [Debianインストーラ](https://ja.wikipedia.org/wiki/Debianインストーラ "wikilink")のテキスト版 Debian10-graphical-installer.png| Debianインストーラの[グラフィカル版](../Page/視覚.md "wikilink") Debian10-console-login.png| Debian 10 のコンソール・ログイン画面

## 歴史

### 開発・公開履歴

  - [1993年](../Page/1993年.md "wikilink")[8月16日](../Page/8月16日.md "wikilink") [イアン・マードック](https://ja.wikipedia.org/wiki/イアン・マードック "wikilink")により開始。
  - [1996年](../Page/1996年.md "wikilink")[6月16日](https://ja.wikipedia.org/wiki/6月16日 "wikilink") Debian 1.1（コード名 buzz）を公開。
  - 1996年12月12日 Debian 1.2（rex）を公開。
  - 1997年6月5日 Debian 1.3（bo）を公開。
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[7月24日](../Page/7月24日.md "wikilink") Debian 2.0（hamm）を公開。
  - 1999年3月9日 Debian 2.1（slink）を公開。
  - 200年8月14−15日 Debian 2.2（potato）を公開。
  - [2002年](../Page/2002年.md "wikilink")[7月19日](../Page/7月19日.md "wikilink") Debian 3.0（woody）を公開。
  - [2003年](../Page/2003年.md "wikilink")[8月16日](../Page/8月16日.md "wikilink") プロジェクト発足10周年を迎えた。
  - 2005年6月6日 Debian 3.1（sarge）を公開。
  - [2007年](../Page/2007年.md "wikilink")[4月8日](../Page/4月8日.md "wikilink") Debian 4.0（etch）を公開。
  - [2009年](../Page/2009年.md "wikilink")[2月14日](../Page/2月14日.md "wikilink") Debian 5.0（lenny）を公開。
  - [2011年](../Page/2011年.md "wikilink")[2月6日](../Page/2月6日.md "wikilink") Debian 6.0（squeeze）を公開。
  - [2013年](../Page/2013年.md "wikilink")[5月4日](https://ja.wikipedia.org/wiki/5月4日 "wikilink") Debian 7.0（wheezy）を公開。
  - [2015年](../Page/2015年.md "wikilink")[4月25日](../Page/4月25日.md "wikilink") Debian 8.0（jessie）を公開。
  - [2017年](../Page/2017年.md "wikilink")[6月17日](../Page/6月17日.md "wikilink") Debian 9.0（stretch）を公開。
  - [2019年](../Page/2019年.md "wikilink")[7月6日](../Page/7月6日.md "wikilink") Debian 10.0（buster）を公開。

Debian の各版に付けられている開発用コード名は、ディズニー映画「トイ・ストーリー」の登場人物の名前に基づいている。Debian の不安定版は、おもちゃをいつも壊す悪ガキのキャラクターである Sid にちなんでいる。

### 1993年〜1998年

Debianは[1993年](../Page/1993年.md "wikilink")8月16日に当時[パデュー大学](../Page/パデュー大学.md "wikilink")の学生であった[イアン・マードック](https://ja.wikipedia.org/wiki/イアン・マードック "wikilink")により創設された。 マードックは当初"Debian Linux Release"という名称を付けた\[4\]。当時"Softlanding Linux System (SLS)"という初のGNU/Linuxディストリビューションが公開されていたが、SLSは保守がお粗末であったり不具合が頻発したためマードックは全く新しいディストリビューションを立ち上げた。

1993年、マードックは"Debianマニフェスト"というこの新しいオペレーティングシステムについての概要を公表した。その中で、このディストリビューションの保守は、LinuxおよびGNUの精神に基づき公開された手法で維持されることを求めた。彼はこのディストリビューションの名称を、ガールフレンドの名前Debra Lynnと自身の名前IanからDebianとした\[5\]。

Debianプロジェクトからは、[1994年](../Page/1994年.md "wikilink")から[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にかけて0.9版のシリーズが初めて公開された。この期間、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")が支援を行った。1995年には、インテルi386以外の環境に対しても対応が開始されることとなり、[1996年](../Page/1996年.md "wikilink")に最初の1.x版が公開された。

1996年には[ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink")がDebianプロジェクトのリーダーとしてマードックの後任に就いた。同年開発者のEan Schuesslerは、Debianプロジェクトがその利用者に対して社会的な契約を交わすべきであるとの提案を行った。これに関してDebianプロジェクトの[メーリングリスト](../Page/メーリングリスト.md "wikilink")で行われた議論は、プロジェクトについての「[Debian社会契約](https://ja.wikipedia.org/wiki/Debian社会契約 "wikilink")」と「[Debianフリーソフトウェアガイドライン](../Page/Debianフリーソフトウェアガイドライン.md "wikilink") (DFSG)」にまとめられた。ペレンズは、[Software in the Public Interest](../Page/Software_in_the_Public_Interest.md "wikilink") (SPI) というDebianプロジェクトを公式に支え、プロジェクトを統括する[非営利組織](https://ja.wikipedia.org/wiki/非営利組織 "wikilink")の創設にも関わった。

ペレンズは、[glibc移行後初めての版となったDebian](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") 2.0が公開される直前にDebianプロジェクトを引退した。

### 1999年〜2004年

この時期、Debianプロジェクトは新たなリーダーを選出し、2.x を公開した。この時期に[APT](../Page/APT.md "wikilink")が初めて導入され、[Debian GNU/HurdというLinuxカーネル以外の開発も始められた](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")。[1999年](../Page/1999年.md "wikilink")にはDebianを母体とするディストリビューションも現れ始めた。[Libranet](https://ja.wikipedia.org/wiki/Libranet "wikilink") ([2006年](../Page/2006年.md "wikilink")に開発停止\[6\])、[Corel Linux](https://ja.wikipedia.org/wiki/Corel_Linux "wikilink") そして Stormixによる[Storm Linuxである](https://ja.wikipedia.org/wiki/Storm_Linux "wikilink")。 特筆すべきは、[2000年](../Page/2000年.md "wikilink")に公開された2.2版（コードネーム: potato）で、この版はlibc等重要なパッケージの保守で、[デュシェンヌ型筋ジストロフィーのため亡くなった](https://ja.wikipedia.org/wiki/筋ジストロフィー#.E6.80.A7.E6.9F.93.E8.89.B2.E4.BD.93.E5.8A.A3.E6.80.A7.E9.81.BA.E4.BC.9D.E5.9E.8B.E7.AD.8B.E3.82.B8.E3.82.B9.E3.83.88.E3.83.AD.E3.83.95.E3.82.A3.E3.83.BC "wikilink")、Joel 'Espy' Kleckerに捧げられた\[7\]。

2000年後半には、プロジェクトはパッケージアーカイブとリリースマネージメントに関する大きな変革を行い、「パッケージプール」方式と次期stable版の土台となる"testing"版の導入が開始された。また同年には全世界のDebian開発者・技術者を集めて年1回開催される[DebConf](https://ja.wikipedia.org/wiki/DebConf "wikilink")（Debianカンファレンス）が開かれるようになった。

この頃[CorelはLinux部門を売却](../Page/コーレル.md "wikilink") (後に[Xandros](../Page/Xandros.md "wikilink")となっている) 、Stormixは[2001年](../Page/2001年.md "wikilink")破産を宣告されている。

[2002年](../Page/2002年.md "wikilink")7月、Debian 3.0 （コードネーム: woody）が公開された。（遡ることver.1.1から、Debianは公開の際に映画[トイ・ストーリー](../Page/トイ・ストーリー.md "wikilink")のキャラクター名をコードネームとして採用し現在に至る。）

3.0(woody)公開後、次期版3.1(sarge)まで、およそ3年という長期に渡る空白期間が存在する。主な理由として、potatoからwoody以後にかけて、パッケージ数が2倍程に増加、またwoodyでの対応環境も増加したため、公開直後からこれに伴うバグが飛躍的に増大した点がある。とりわけリリースクリティカルバグが事実上すべて解消されない限り公開できないため、公開日程に多大なる影響を与えた。パッケージメンテナのバグに対する考え方は温度差があり、たとえば特定の言語のみ発生するバグならば、そのメンテナがバグ対象の言語圏でも無い限りバグを修正することに対する意欲を持つことは少ない。コミュニティによるボランティアを作業基盤とするDebian特有の問題とも言える。

しかし、長くなっていく公開間隔について、フリーソフトウェアコミュニティから疑問の声が上がった。Debianのsargeリリース直前には、実際にDebian開発者の1人であった[Shuttleworthが主導して](../Page/マーク・シャトルワース.md "wikilink")[Ubuntu](../Page/Ubuntu.md "wikilink")というプロジェクトを派生させた。Shuttleworthが雇っているUbuntu開発者の多くは、かつてはDebianボランティアだったか、または今もDebianに関わっている人々である。多くの場合、Ubuntu開発者として（[Canonicalを通して](https://ja.wikipedia.org/wiki/カノニカル "wikilink")）雇われた人々はDebianでも同じパッケージの管理をしている\[8\]。この点については本人も公式サイト\[9\]で「Debian の開発者の中には、Ubuntu で仕事のほとんどをするようになった人も確かにいます。また、Ubuntu と Debian で同じように仕事をしている開発者もいます。」としてそれを認めている。Debian の創立者、Ian Murdochは、Ubuntu の人気が Debian 派生のディストロのために良い兆しだとは考えていない。それは、Ubuntu 用に作られたパッケージが Sarge上で動作しないことが多いことを挙げている。Murdochは、Ubuntuが本当にDebianと互換性があった場合、開発のための作業のエネルギーの全てをSargeに向けられる可能性があり、それが本当に全体として見た場合、Debianの開発システムに利益をもたらすと主張している\[10\]。したがって、当時のこうした混乱状況がsargeの開発をさらに遅らせることになったといえる。

その後、Debianから派生したUbuntuは多数の常勤の開発者によって開発されるところとなり、次第に影響力を増していった。しかし、ブラジル人のDebian開発者、Otavio Salvador は、「ユーザはUbuntuを信用しているが、ユーザには安定したパッケージを提供する必要がある」 という考えにUbuntuが[反映しているかどうか](https://ja.wikipedia.org/wiki/コミット#バージョン管理システムにおけるコミット "wikilink")、確信が持てない。」と述べている。また彼は、Shuttleworth個人に対しても不信感を抱いており、露骨に「言動が一致していない」と非難し、品質対公開日程の問題で溝が深まったことでUbuntuとDebianの関係はひどいものになっている。」と語っている\[11\]。このように、Ubuntuに対する評価は分かれている。

Debianのstable開発の長期化と派生であるUbuntuの誕生は、Debianコミュニティに対する意識を変化させ、Debian 4.0(コードネーム: etch)以降の版に対しての公開日程を含むいくつかの改善をもたらしたのは確かである。[2011年](../Page/2011年.md "wikilink")現在では両コミュニティにおいて、バグ修正の取扱いなど相互交流もある\[12\]。

### 2005年以降

[Debian_Etch-ja.png](https://ja.wikipedia.org/wiki/File:Debian_Etch-ja.png "fig:Debian_Etch-ja.png") [2005年](../Page/2005年.md "wikilink")6月、Debian 3.1（コードネーム: sarge）が公開された。小規模な改良（バージョン番号が小数部の増加に留まる）にも関わらず、この正式版では数多くの変更が実施されたが、それは一つ前の版woodyからsarge公開までの期間が長かったことが原因である。この版では70％以上のソフトウェアが更新の対象となっただけではなく、ソフトウェアの容量も増加した。新規のインストーラーが導入され、40ヶ国語にも及ぶ言語に対応するようになった。

このリリースでは、woody以前のインストーラである、"boot-floppies"を[Debianインストーラ](https://ja.wikipedia.org/wiki/Debianインストーラ "wikilink")と呼ばれる[モジュラー設計の新しいインストーラで置き換えた](https://ja.wikipedia.org/wiki/モジュール#ソフトウェア "wikilink")。この新しいインストーラは高度な導入方法に対応しており、[RAID](../Page/RAID.md "wikilink")、[XFS](../Page/XFS.md "wikilink") そして[LVMにも対応ている](../Page/論理ボリュームマネージャ.md "wikilink")。またハードウェア検知能力に優れるため、Linuxのインストールに不慣れな者でもインストールできるようになっている。インストーラは約40ヶ国の言語で完全なソフトウェアレベルでの国際化を実現している。インストール[マニュアル](../Page/マニュアル.md "wikilink")と包括的なリリースノートはそれぞれ10と15の言語に翻訳され公開されている。

このときの公開では、Debianプロジェクトの各サブプロジェクトの取り組みも含まれており、[Debian-Edu](https://ja.wikipedia.org/wiki/Debian-Edu "wikilink") ([Skolelinux](https://ja.wikipedia.org/wiki/Skolelinux "wikilink"))、[Debian-Med](https://ja.wikipedia.org/wiki/Debian-Med "wikilink")、[Debian-Accessibility](https://ja.wikipedia.org/wiki/Debian-Accessibility "wikilink")がそれに当たる。Skolelinuxは学校教育において有用なソフトウェアのパッケージを作成しDebianアーカイブに収録、また教育現場へのDebianの利用促進を行うプロジェクトである。Debian-Medは医療現場におけるDebianの利用促進や医療用ソフトウェアの作成、パッケージ化を担っている。Debian-AccessibilityはDebianシステムやDebianプロジェクトのWebサイトの[利便性向上や](../Page/アクセシビリティ.md "wikilink")[障害者](../Page/障害者.md "wikilink")に対するDebianの利用を支援するプロジェクトで、その一部は[視覚障害者](../Page/視覚障害者.md "wikilink")のための[ブライユ端末上における導入支援などがある](https://ja.wikipedia.org/wiki/点字ディスプレイ "wikilink")。 F [Iceweasel_icon.svg](https://ja.wikipedia.org/wiki/File:Iceweasel_icon.svg "fig:Iceweasel_icon.svg") logo\]\] [2006年](../Page/2006年.md "wikilink")、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")や[メーラー](https://ja.wikipedia.org/wiki/メーラー "wikilink")といった [Mozilla](../Page/Mozilla.md "wikilink")関連のソフトウェア名が商標上の問題によって変更された。[Firefox](../Page/Mozilla_Firefox.md "wikilink") は、[Iceweasel](../Page/Iceweasel.md "wikilink") へ、[Thunderbird](../Page/Mozilla_Thunderbird.md "wikilink") は [Icedove](https://ja.wikipedia.org/wiki/Icedove "wikilink") へといったように変わった。これはMozilla Foundationの要請によりDebianプロジェクトでMozilla Firefoxの名称が使えなくなったことによる。

[2007年](../Page/2007年.md "wikilink")4月8日、Debian 4.0（コードネーム: etch）が公開された。GUIインストールが公式に対応されている。この公開版では新たにAMD64に対応した一方、Debian初のx86以外の対応環境であったm68kは公式に非対応となった（但し非公式ながら動作する）。

[2009年](../Page/2009年.md "wikilink")2月14日、Debian 5.0（コードネーム: lenny）が公開された。開発期間は22ヶ月。25000以上のソフトウェア・パッケージが収録された。新たに[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")が販売しているARM基盤の[NAS](../Page/ネットワークアタッチトストレージ.md "wikilink")、[Orion](https://ja.wikipedia.org/wiki/:en:Orion_\(system-on-a-chip\) "wikilink")[プラットフォームと](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[Asus Eee PCのような](../Page/Eee_PC.md "wikilink")[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")に対応した。この版はMIPSアーキテクチャメンテナで[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")12月26日に交通事故で亡くなったThiemo Seuferに捧げられた\[13\]\[14\]。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")9月5日、公式にバックポートサービス (Debian Backport) を開始した。

[Debian_6.0.2.1.png](https://ja.wikipedia.org/wiki/File:Debian_6.0.2.1.png "fig:Debian_6.0.2.1.png") [Screenshot-debian_wheezy_ja.png](https://ja.wikipedia.org/wiki/File:Screenshot-debian_wheezy_ja.png "fig:Screenshot-debian_wheezy_ja.png")

5.0公開からほぼ2年経った[2011年](../Page/2011年.md "wikilink")2月6日、Debian 6.0（コードネーム: squeeze）が公開された。[FreeBSD](../Page/FreeBSD.md "wikilink")カーネル（[Debian GNU/kFreeBSD](https://ja.wikipedia.org/wiki/Debian_GNU/kFreeBSD "wikilink")）が「テクノロジープレビュー」としてこの版から正式に対応されたが、その一方でalphaとhppa、armの3つの環境がこの版から公式に非対応となった。

6.0公開から2年以上経過した[2013年](../Page/2013年.md "wikilink")5月4日、Debian 7.0（コードネーム: wheezy）が公開された。この版からarmhfとs390xの２つの環境に正式対応されることとなった。

[2014年](../Page/2014年.md "wikilink")4月24日、Debian 6.0の保守が2016年2月まで延長されることが発表され\[15\]、[2014年](../Page/2014年.md "wikilink")6月16日より長期サポート(LTS)期間に入った\[16\]。

[2015年](../Page/2015年.md "wikilink")4月25日、Debian 8.0（コードネーム: jessie）が公開された。この版よりAArch64（[64ビット](../Page/64ビット.md "wikilink")版ARM環境）とPOWER 64 ビットリトルエンディアン版が正式対応された。またs390 環境の対応が終了し、s390xに置き換えられた。なお、ia64 および sparc が、開発者不足から、正式版に含まれなくなった。

[2017年](../Page/2017年.md "wikilink")[6月17日](../Page/6月17日.md "wikilink")、Debian 9.0（コードネーム: stretch）が公開された。この版より64 ビットリトルエンディアン MIPSが対応環境に追加された。逆に[32ビット](../Page/32ビット.md "wikilink")版PowerPCがサポートされる対応環境から外れた（PowerPC 64ビット版は引き続き保守が継続される）。

[2019年](../Page/2019年.md "wikilink")[7月6日](../Page/7月6日.md "wikilink")、Debian 10.0（コードネーム: buster）が公開された。

## プロジェクトの組織構成

プロジェクトは、世界中の有志の開発者によって構成されている。プロジェクトには誰でも参加できるが、正規の開発者になるためには、技術的なチェックを受ける必要がある。、1000名以上\[17\]のメンバーがいる。日本人の開発者は40人ほどである。

プロジェクトの抱負として、Debian社会契約\[18\]を掲げている。Debian社会契約は、プロジェクトが遵守すべき事項を定めたもので、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[7月5日](../Page/7月5日.md "wikilink")に採択された。その中の[Debianフリーソフトウェアガイドライン](../Page/Debianフリーソフトウェアガイドライン.md "wikilink") (DFSG) は、Debianにおける[ソフトウェア](../Page/ソフトウェア.md "wikilink")評価基準となっており、このガイドラインに。合しない、

フリーではないと評価されたソフトウェアは、Debianの一部として提供されることはない。

プロジェクト内の意思決定はDebian憲章\[19\]の元で行なわれる。Debian憲章は、組織構成やその権限、投票にかけるまでの手続きなどを定めたもので、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[12月2日](../Page/12月2日.md "wikilink")に採択された。

このことから、Debianプロジェクトは独立した非中央集権的な組織である。また他のGNU/Linuxディストリビューション（例えば、Ubuntu、openSUSE、Fedora、そしてMandriva）のように企業が所有するものではない。 にも関わらず、プロジェクトの生産付加価値は極めて高く、Debian 4.0 (etch)版に含まれる全パッケージ開発コストを例にとると、コード総数2億8300万行、[COCOMO](https://ja.wikipedia.org/wiki/COCOMO "wikilink")モデル([:en:COCOMO](https://ja.wikipedia.org/wiki/:en:COCOMO "wikilink"))を使用した生産価値評価は130億米ドルにのぼるとされる\[20\]。[2009年](../Page/2009年.md "wikilink")4月2日、オンラインコミュニティサイト[Ohloh](https://ja.wikipedia.org/wiki/Ohloh "wikilink")はある時点でのDebian GNU/Linuxプロジェクトのコードベース（コード総数4500万行）をCOCOMOモデルを用いて評価したところ、開発コストは約8億1900万米ドルになると推計した\[21\]。Debian 5.0 (lenny) リリースに関して、Juan José Amorらの推計によると、有効なコード総数は324,000,000行、COCOMOモデルによる生産価値評価は61億ユーロにのぼるとされる\[22\]。

無論こうしたDebianに関するコミュニティの門戸の広さは、全く問題がないわけではなく、以前には、「一部ユーザによる礼儀知らずな行為」とコミュニティの意思決定の遅さが批判されたことがある\[23\]。

毎年、Debianカンファレンス\[24\] (通称[DebConf](https://ja.wikipedia.org/wiki/DebConf "wikilink")) が開催される。Debianカンファレンスは、世界中のDebian開発者が直接会談する場で、[2000年](../Page/2000年.md "wikilink")[7月5日](../Page/7月5日.md "wikilink")に初めて開催された。資金面などの多くの障害があるため、今のところ日本で開催されたことはないが、有志によって開催が検討されている\[25\]。

### プロジェクトリーダー

Debianプロジェクトリーダー(Debian Project Leader; DPL)はプロジェクトの公的な代表者であり、プロジェクトの現在の方向性を決める立場にある\[26\]。プロジェクトは次のリーダーを選出してきた:\[27\]

1.  [イアン・マードック](https://ja.wikipedia.org/wiki/イアン・マードック "wikilink") (1993年8月 – 1996年3月), Debianプロジェクト創設者
2.  [ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink") (1996年4月 – 1997年12月)
3.  [イアン・ジャクソン](https://ja.wikipedia.org/wiki/イアン・ジャクソン "wikilink") (1998年1月 – 1998年12月)
4.  [ウィヘルト・アッカーマン](https://ja.wikipedia.org/wiki/ウィヘルト・アッカーマン "wikilink") (1999年1月 – 2001年3月)
5.  [ベン・コリンズ](https://ja.wikipedia.org/wiki/ベン・コリンズ_\(プログラマー\) "wikilink") (2001年4月 – 2002年4月)
6.  [ビーデール・ガービー](https://ja.wikipedia.org/wiki/ビーデール・ガービー "wikilink") (2002年4月 – 2003年4月)
7.  [マーチン・マイケルメイヤー](https://ja.wikipedia.org/wiki/マーチン・マイケルメイヤー "wikilink") ([Martin Michlmayr](https://ja.wikipedia.org/wiki/:en:Martin_Michlmayr "wikilink")) (2003年3月 – 2005年3月)
8.  [ブランデン・ロビンソン](https://ja.wikipedia.org/wiki/ブランデン・ロビンソン "wikilink") ([Branden Robinson](https://ja.wikipedia.org/wiki/:en:Branden_Robinson "wikilink")) (2005年4月 – 2006年4月)
9.  [アンソニー・タウンズ](https://ja.wikipedia.org/wiki/アンソニー・タウンズ "wikilink") (2006年4月 – 2007年4月)
10. [サム・オセヴァール](https://ja.wikipedia.org/wiki/サム・オセヴァール "wikilink") ([Sam Hocevar](https://ja.wikipedia.org/wiki/:en:Sam_Hocevar "wikilink")) (2007年4月 – 2008年4月)
11. [スティーブ・マッキンタイアー](https://ja.wikipedia.org/wiki/スティーブ・マッキンタイアー "wikilink") (2008年4月 – 2010年4月)
12. [ステファノ・ザッキローリ](https://ja.wikipedia.org/wiki/ステファノ・ザッキローリ "wikilink") (2010年4月 – 2013年4月)
13. Lucas Nussbaum（2013年4月 – 2015年4月）
14. Neil McGovern（2015年4月 – 2016年4月）
15. Mehdi Dogguy（2016年4月 – 2017年4月）
16. Chris Lamb（2017年4月 – 現職）

補佐的な役職として、アンソニー・タウンズにより*Debian Second in Charge* (2IC; 副リーダー)が創設された。スティーブ・マッキンタイアーは2006年4月から翌2007年4月までこの役職に就いている。2009年4月からはLuk Claesがその地位にいる。現プロジェクトリーダー、ステファノ・ザッキローリは、2ICを選出しない旨DPL選挙の際に宣言していた\[28\]。

### 開発マネージャ

  - Brian C. White (1997–1999)
  - Richard Braakman (1999–2000)
  - [アンソニー・タウンズ](https://ja.wikipedia.org/wiki/アンソニー・タウンズ "wikilink") (2000–2004)
  - Steve Langasek, Andreas Barth そして Colin Watson (2004–2007)
  - Andreas Barth と Luk Claes (2007–2008)
  - Luk Claes と Marc Brockschmidt (2008–2009)
  - Luk Claes と Adeodato Simó (2009–2010)
  - Adam D. Barratt と Neil McGovern (2010–現職)<ref>

</ref>

注意すべきことに、上記リストにはアクティブな開発マネージャーのみ含まれている。[2003年](../Page/2003年.md "wikilink")から導入された、開発アシスタント、そして引退したマネージャー("release wizards"と呼ばれる)はここには含まれていない\[29\]。

## 保守の容易さ

### APT

[Debian_7_Aptitude_Package_Details.png](https://ja.wikipedia.org/wiki/File:Debian_7_Aptitude_Package_Details.png "fig:Debian_7_Aptitude_Package_Details.png") to view Debian package details\]\] [Debian-aptitude.png](https://ja.wikipedia.org/wiki/File:Debian-aptitude.png "fig:Debian-aptitude.png")

Debianの特長として、[保守の単純さがある](../Page/メンテナンス.md "wikilink")。[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")を備えており、ひとたび[導入が終了すれば](../Page/インストール.md "wikilink")、パッケージマネージャの*APT (Advanced Package Tool)* により、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の更新が行える。パッケージの導入は、[セキュリティ関連の更新や](../Page/コンピュータセキュリティ.md "wikilink")[プログラム相互の依存性確認も含めて](../Page/プログラム_\(コンピュータ\).md "wikilink")、[仮想端末](https://ja.wikipedia.org/wiki/仮想端末 "wikilink")（[コンソール](../Page/コンソール.md "wikilink")）より容易に操作できる。

パッケージの依存関係には、大きく分けて、*depends（依存）*、*recommends（推奨）*、*suggests（提案）* という3種類の項目が設定されており、動作に必須なものがdepends、動作に必須ではないが常識的に必要とするものがrecommends、組み合わせる事で更に便利に使えるものがsuggestsに指定されている。しかしapt-getでは、depends以外の項目を上手に扱えなかったため、これらの項目を最大限生かす事ができるaptitudeの使用がSarge以降では勧められていたが、Squeezeではこの点は改善された\[30\]\[31\]。さらに、自動削除に対応するようにも更新された\[32\]。

APTには補助的機能を追加する[フロントエンド](../Page/フロントエンド.md "wikilink")が数多く提供されており、以下ではaptitudeを含めた幾つかのフロントエンドを紹介する。

#### aptitude

#### GUIフロントエンド

[thumb](https://ja.wikipedia.org/wiki/ファイル:Screenshot-Synaptic_ja.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Screenshot-apt-watch_notification.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Updates-notification-icon.png "wikilink") 扱いやすい[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")は複数存在する。

一般的に良く知られる代表としては、Debianだけでなく RPM系のディストリビューションでも使われている [Synaptic](../Page/Synaptic.md "wikilink")（シナプティック）がある。Synapticは、apt-getコマンドを使用せずにシステムの更新が全てマウスで直感的に行えるだけでなく、ソフトウェアの削除機能も備えている。

「apt-watch（アプト-ウォッチ）」は、デスクトップで使用するユーザーにとって、アップデートの公開を直ちに通知してくれる[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")として極めて有効なツールである。apt-watch は、より簡易にパッケージの管理を実現するツールとして開発されたアプリケーションである。これは、ネットワークに接続し、アップデータを定期的に監視するアプレットであり、アップデータが利用可能となった時には、クライアントに自動的に更新の通知を行う。Windows Updatesや Red Hat Network と同様な機能を持っている。

4.0 (Etch) では、apt-watch に加えて新たに update-manager も用意された。これは、[GNOME](../Page/GNOME.md "wikilink")デスクトップ環境で利用可能なパッケージの管理ツールである。この update-manager は、Update Notifier と呼ばれるデスクトップ上のアプレットと組み合わせて利用することができる。機能的には apt-watch と似ているが、APT keyring を管理する仕組みが追加されている。なお、Update Notifier は GNOME や [KDE](../Page/KDE.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink") など [Freedesktop.org](../Page/Freedesktop.org.md "wikilink") 準拠の全てのデスクトップ環境で動作するように設計されている。

ただしこれらもアップデートの実際の内部処理は、APT が機能しているので、apt-get コマンドを実行することと大差は無い。

### gdebi

[thumb](https://ja.wikipedia.org/wiki/ファイル:Screenshot-Package_Installer.png "wikilink") Debian 4.0 では、グラフィカルなパッケージ・インストーラーが新たに提供された。このインストーラーを利用すれば、ローカルに保存した Debianパッケージがコマンド操作なしでインストール可能である。[Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") で初めて採用された GNOME-RPM\[33\] (あるいは gnorpm とも) というグラフィカルなインストーラーと好対照を成すツールであるが、GNOME-RPM がシェルプロンプトから RPMコマンドを実行するのと同じ機能を有するのに留まるのとは違い、gdebi は APTのようにパッケージ間の依存関係を自動的に解決する機能も併せ持っている点でより優れている。GDebi とも表記される。

### debconf

パッケージ管理には[debconfと呼ばれる](https://ja.wikipedia.org/wiki/debconf_\(ソフトウェアパッケージ\) "wikilink")[フレームワークが用意されており](../Page/アプリケーションフレームワーク.md "wikilink")、パッケージ作成者はユーザーに対して簡易のフロントエンドを提供できる。このフレームワークを積極的に利用しているパッケージでは、インストール後にユーザーが行うであろう初期設定の大半を、対話形式の質問に答えていくだけで、インストールと同時に終える事ができる。debconfパッケージ自身もdebconfの設定を有しており、利用するフロントエンドインターフェースと優先度を設定できる。debconfのインターフェースは、対話形式のものから、非対話形式（質問なしで自動設定）なもの、[キャラクタベースなものから](../Page/キャラクタ_\(コンピュータ\).md "wikilink")、[グラフィカルなもの](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、または設定ファイルを直接書き換える用途で使用するエディタまで、ユーザーが自由に選択可能である。優先度はパッケージの各質問毎に設定されており、ユーザが介在しないとシステムが動作しなくなる高レベルのものから、標準で問題ないような些細なものまである。（システムに不慣れなユーザのため）ある優先度より低い設定をすべて標準で済ませ、それらを一切質問させないことも可能である。

## 種類

[Debian10-CD-Cover.png](https://ja.wikipedia.org/wiki/File:Debian10-CD-Cover.png "fig:Debian10-CD-Cover.png")

公開は、4種類で行なわれている。

1.  安定版 (stable)：これは、厳密に安定性を検証した版で公式の公開となる。公開は2009年より2年の間隔をもっておこなわれ、日程を決定することにより奇数年の12月に固定し、翌年の偶数年前半に公開される\[34\]。
      - ソフトウェアの[セキュリティホール](../Page/セキュリティホール.md "wikilink")や[バグ](../Page/バグ.md "wikilink")の修正は、主に上流から修正コードをバックポートする事で行なわれる。そのため、ソフトウェアのメジャーバージョン（例: **1**.0.0→**2**.0.0）やマイナーバージョン（例: 1.**0**.0→1.**1**.0）が更新されることは滅多になく、ビルドバージョン（例: 1.0.**0**→1.0.**1**）かパッケージ番号（例: 1.0.0+deb8u**1**→1.0.0+deb8u**2**）が更新されることがほとんどである。
      - 安定版に含まれるソフトウェアは上述のとおりメジャー/マイナーバージョンアップされることが滅多にないが、テスト版や不安定版のパッケージを安定版向けにリビルドし、backportsパッケージとして提供されているソフトウェアが一部存在する。これにより、新版のソフトウェアをソースコンパイルすることなく、パッケージ管理下で使用することが可能になる。
      - 不定期に新しい[リビジョンが公開される](https://ja.wikipedia.org/wiki/バージョン#コンピュータ・ソフトウェア "wikilink")。この公開版はそれまでの更新を包含して提供される小規模バージョンアップデートであり、構成を変えるものではない。8.0、8.1、8.2に対して8.3公開時までの全ての更新を適用すると、8.3と同じものになる。
      - リビジョンは下記の形式で示される。
          - 4.0（etch）以前: バージョン番号の末尾の"r**N**"表記（N = 0, 1, 2, ...）。例えば、3.1版4回目のアップデートは、3.1**r3**。
          - 5.0（lenny）以降: バージョン番号の小数第二位の値。例えば、5.0版4回目のアップデートは、5.0.**4**。
          - 7.0（wheezy）以降: バージョン番号の小数第一位の値。例えば、7.0版4回目のアップデートは、7.**4**。
      - 次の安定版が公開されると、それまでの安定版は一般に「旧安定版」(oldstable) と呼ばれて区別される。
      - セキュリティアップデートは、次の安定版が公開された後も、そのまま一年間は継続して提供される。
          - 6.0（squeeze）以降は、旧安定版のLTS（Long Term Support）が実施されるようになった\[35\]。Debian LTS teamによって、安定版としての最初の公開日から少なくとも5年後までセキュリティサポートが提供される。
2.  テスト版 (testing)：次期の安定版となる公開テスト中の版である。次に説明する不安定版で一定期間致命的なバグが発見されなかったパッケージが、自動的にテスト版に組み入れられる。
      - デスクトップなどで使う分には支障のない程度の安定度を持っていると言われ、最新のデスクトップを使いたい場合は、このテスト版を使うことが多いようである。だがパッケージ更新が機械的に行なわれるため、依存関係が壊れやすい。
      - 公開が近付くと段階的に固定され、この自動処理が止められる。すべてのRCバグ (Release Critical Bug。安定版として致命的なバグ) が無くなったとき、テスト版は安定版として公開される。
      - テスト版が安定版として公開される時期が近付くとセキュリティアップデートの提供が始まる。それ以前は提供されない。だが、2005年9月より、Debian開発者の有志らがDebian Testing Security Teamを結成し、非公式な形でテスト版向けのセキュリティアップデートを提供している。
3.  不安定版 (unstable)：これは、開発者向けの版である。コードネームは不変で「*sid*」と呼ばれる。
      - 通常新規パッケージはこの版に投入される。セキュリティのアップデートは提供されないが、パッケージの更新サイクルが早いため、セキュリティの問題も比較的早く取り除かれる。またテスト版とは違い、DSA (Debian Security Advisory) によってどのバージョンから当該セキュリティホールが塞がれているか告知される。

<!-- end list -->

1.  実験版 (experimental)：これは、影響が大きなパッケージ群が、不安定版に入れる前に一時的に置かれて、不安定版との組合せによりしばらく実験が行われる。experimentalだけで全ての導入を行うことは出来ず、他の版との組み合わせにより動く。

Debianのコードネームは、[ディズニー配給の映画](../Page/ウォルト・ディズニー・カンパニー.md "wikilink")「[トイ・ストーリー](../Page/トイ・ストーリー.md "wikilink")」のキャラクタから取られている。これは、過去にDebianのプロジェクトリーダーを務めた[ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink")が、トイ・ストーリーを製作した[ピクサー・アニメーション・スタジオ](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")の社員であったためである。

## 公開/開発履歴

| 凡例         |
| ---------- |
| 保守終了（過去の版） |
| 保守継続       |
| 現行版        |

| バージョン | [コードネーム](../Page/コードネーム.md "wikilink")                                                                                                                         | 公開日                                                                      | [アーキテクチャ数](../Page/コンピュータ・アーキテクチャ.md "wikilink") | [カーネル](../Page/カーネル.md "wikilink")数 | パッケージ数   | 保守期限                        | 特記事項                                                                                   |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------ | ----------------------------------- | -------- | --------------------------- | -------------------------------------------------------------------------------------- |
| 通常    | LTS                                                                                                                                                            |                                                                          |                                                  |                                     |          |                             |                                                                                        |
| 1.1   | *buzz*                                                                                                                                                         | 1996年6月17日                                                               | 1                                                | 1                                   | 474      | No                          | `dpkg`、[ELFへ移行](../Page/Executable_and_Linkable_Format.md "wikilink")、Linux 2.0\[36\]  |
| 1.2   | *rex*                                                                                                                                                          | 1996年12月12日                                                              | 1                                                | 1                                   | 848      | No                          | \-                                                                                     |
| 1.3   | *bo*                                                                                                                                                           | 1997年6月2日                                                                | 1                                                | 1                                   | 974      | No                          | \-                                                                                     |
| 2.0   | *hamm*                                                                                                                                                         | 1998年7月24日                                                               | 2                                                | 1                                   | \~ 1500  | No                          | [glibcへ移行](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")、新アーキテクチャ: `m68k`\[37\] |
| 2.1   | *slink*                                                                                                                                                        | 1999年3月9日                                                                | 4                                                | 1                                   | \~ 2250  | No                          | `APT`、新アーキテクチャ: `alpha`, `sparc`\[38\]                                                 |
| 2.2   | *potato*                                                                                                                                                       | 2000年8月15日                                                               | 6                                                | 1                                   | \~ 3900  | No                          | 新アーキテクチャ: `arm`, `powerpc`\[39\]                                                       |
| 3.0   | *woody*                                                                                                                                                        | 2002年7月19日                                                               | 11                                               | 1                                   | \~ 8500  | 2006年6月30日<ref> {{cite web  | url = <https://www.debian.org/News/2006/20060601>                                      |
| 3.1   | *sarge*                                                                                                                                                        | 2005年6月6日                                                                | 11                                               | 1                                   | \~ 15400 | 2008年3月31日<ref> {{cite web  | url = <https://www.debian.org/News/2008/20080229>                                      |
| 4.0   | *etch*                                                                                                                                                         | 2007年4月8日                                                                | 11                                               | 1                                   | \~ 18000 | 2010年2月15日 <ref> {{cite web | url = <https://www.debian.org/News/2010/20100121>                                      |
| 5.0   | *lenny*\[40\]                                                                                                                                                  | 2009年2月14日                                                               | 11                                               | 1                                   | \~ 28000 | 2012年2月6日<ref> {{cite web   | url = <https://www.debian.org/News/2012/20120209>                                      |
| 6.0   | *squeeze*                                                                                                                                                      | 2011年2月6日                                                                | 9                                                | 2                                   | \~ 29000 | 2014年5月31日\[41\]            | 2016年2月29日<ref name="squeeze-lts-eol">{{Cite web                                       |
| 7.0   | *wheezy*<ref name="7.0 release">{{cite web | first = | last = | date = 2013-05-04 | accessdate = 2013-05-05 | url = <http://www.debian.org/News/2013/20130504> | title = Debian 7.0 Wheezy released | publisher = www.debian.org }}</ref> | 2013年5月4日                                        | 11                                  | 2        | \~ 37000                    | 2016年4月25日<ref name="wheezy-lts"> {{cite web                                           |
| 8.0   | *jessie*\[42\]                                                                                                                                                 | 2015年4月25日                                                               | 10                                               | 1                                   | \~ 43000 | 2018年6月17日\[43\]            | 2020年6月30日\[44\]                                                                       |
| 9.0   | *stretch*\[45\]                                                                                                                                                | 2017年6月17日                                                               | 10                                               | 1                                   | \~ 52000 | 2020年\[46\]                 | 2022年6月\[47\]                                                                          |
| 10.0  | *buster* \[48\]                                                                                                                                                | 2019年7月6日                                                                | 10                                               | 1                                   | \~ 59000 | 2022年                       | 2024年                                                                                  |
| 11.0  | *bullseye* \[49\]                                                                                                                                              | 2021年予定                                                                  | TBA                                              | TBA                                 | TBA      | TBA                         | \-                                                                                     |
| 12.0  | *Bookworm* \[50\]                                                                                                                                              | TBA                                                                      | TBA                                              | TBA                                 | TBA      | TBA                         | TBA                                                                                    |

  -

    Linuxカーネルの11アーキテクチャ + ARMアーキテクチャにおける追加のABI (`armel`) に対応している\[51\]。

    Linuxカーネルの9つのアーキテクチャ + FreeBSDカーネル（i386、amd64の2アーキテクチャのみ）に対応していることを示す<ref name="squeeze released">

</ref>。

## ロゴ

[Debian-OpenLogo.svg](https://ja.wikipedia.org/wiki/File:Debian-OpenLogo.svg "fig:Debian-OpenLogo.svg")を表している。\]\] Debian の「スワール」マーク（意匠）は 1999 年に Raul Silva によって考案された\[52\]\[53\]。これはその年に開催されたコンテスト用のものであって、それ以前に使われていた準公式のマークに替わるものとしてデザインされた\[54\]。 このコンテストの勝者に対して、@debian.org のメールアドレスと、希望するアーキテクチャ用の Debian 2.1 インストール CD のセットが贈られた。マークの意味について Debian プロジェクトから公式な声明は出ていなかったが、 このマークが選ばれた時点では、これはコンピュータを動作させる魔法の煙 (または精霊) を表していることがほのめかされた\[55\]\[56\]\[57\]。

Debian のこのマークの由来については、最初に命名された Debian のキャラクターとして選ばれた バズ・ライトイヤー(Buzz Lightyear)のあごに渦巻きがあるからだという説がある\[58\]。Stefano Zacchiroli も、この渦巻きが Debian のものであると示唆している。Debian のコードネームはトイ・ストーリーのキャラクターの名前を付けているので、 バズ・ライトイヤーのスワールが候補となった可能性が高いと思われる。Debian 開発者の Bruce Perens も Pixar の元で働いていた\[59\]\[60\]。

## 必要環境

[HP-HP9000-C110-Workstation_21.jpg](https://ja.wikipedia.org/wiki/File:HP-HP9000-C110-Workstation_21.jpg "fig:HP-HP9000-C110-Workstation_21.jpg") C110 [PA-RISC](../Page/PA-RISC.md "wikilink") [workstation](../Page/ワークステーション.md "wikilink") booting Debian Lenny\]\] Debianでは、以下のような環境に対応した[バイナリ](../Page/バイナリ.md "wikilink")版を作成している。括弧内はプロジェクトでの呼称である。

  - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink") (amd64/x86-64)
  - [ARM](../Page/ARMアーキテクチャ.md "wikilink") [EABI](https://ja.wikipedia.org/wiki/Application_binary_interface#EABI "wikilink") (armel)
  - Hard Float ABI [ARM](../Page/ARMアーキテクチャ.md "wikilink") (armhf)
  - 64ビット版[ARM](../Page/ARMアーキテクチャ.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") (i386/IA-32、ただし現行版では[80386には対応しない](../Page/Intel_80386.md "wikilink"))
  - [MIPS](../Page/MIPSアーキテクチャ.md "wikilink") (mips/mipsel)
  - 64ビット版リトルエンディアン[MIPS](../Page/MIPSアーキテクチャ.md "wikilink") (mips64el)
  - 64ビット版リトルエンディアン[PowerPC](../Page/PowerPC.md "wikilink") (ppc64el)
  - [System z](../Page/System_z.md "wikilink") (s390x)

以下の環境はかつて対応されていたが、現在では公式には対応されていない（一部の環境では非公式な対応が存在する）。

  - [MC68000](../Page/MC68000.md "wikilink") (m68k)（etchより開発対象から外された）
  - [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") (alpha)（squeezeより開発対象から外された）
  - [ARM](../Page/ARMアーキテクチャ.md "wikilink") (arm)（同上。armelにより置き換え）
  - [PA-RISC](../Page/PA-RISC.md "wikilink") (hppa)（同上）
  - [IA-64](../Page/IA-64.md "wikilink") (ia64)（jessieより開発対象から外された）
  - [SPARC](../Page/SPARC.md "wikilink") (sparc)（同上）
  - [IBM S/390及び](https://ja.wikipedia.org/wiki/IBM_S/390 "wikilink")[zSeries](https://ja.wikipedia.org/wiki/zSeries "wikilink")（同上。s390xに置き換え）
  - 32ビット版[PowerPC](../Page/PowerPC.md "wikilink") (powerpc)（stretchより開発対象から外された\[61\]）

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")以外を[カーネル](../Page/カーネル.md "wikilink")とするものもある。名称の通り、ユーザーランドは[GNU](../Page/GNU.md "wikilink")の成果物に依存している。

[Horned_logo.svg](https://ja.wikipedia.org/wiki/File:Horned_logo.svg "fig:Horned_logo.svg")

  - [Debian GNU/kFreeBSD](https://ja.wikipedia.org/wiki/Debian_GNU/kFreeBSD "wikilink") (kfreebsd-i386, kfreebsd-amd64) （jessieより開発対象から外された）

まだ正式公開されていない上記以外の環境やカーネル版もいくつかある。

*アーキテクチャ*

  - [SuperH](../Page/SuperH.md "wikilink") (sh4)
  - Motorola/IBM PowerPC64 (ppc64)
  - Linksys NSLU2 (armeb)
  - Renesas Technology M32R (m32r)
  - Sun UltraSPARC (sparc64)
  - 32ビットポインタ搭載[64ビットPC](https://ja.wikipedia.org/wiki/x64 "wikilink") (x32)

*カーネル*

  - [Debian GNU/Hurd](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink") (hurd-i386)

Debian-gnu-hurd-running-emacs.png|Debian GNU/Hurd Hurd-logo.svg|100px|Logo

  - Debian GNU/NetBSD (netbsd-i386, netbsd-alpha)
  - Debian GNU/Solaris (solaris-i386)

## Debian派生のディストリビューション

[DebianFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:DebianFamilyTree1210.svg "fig:DebianFamilyTree1210.svg")

### 派生物調査と協力体制について

Debian プロジェクトは派生ディストリビューションの重要性を完全に認めており、関係者間の協力を活発に支援している。通常これは、当初派生ディストリビューションで開発されていた改善を Debian が取り込むことを意味する。こうすることで、誰もが恩恵を受けることができ、長期におよぶ保守作業を減らすことになる。

このため、派生ディストリビューションは debian-derivatives@lists.debian.org メーリングリストの議論に参加し、派生物調査に参加するよう勧められている。派生物調査は、派生ディストリビューションの中でなされた作業に関する情報を集めることを目標にしている。こうすることで、公式の Debian 開発者が Debian 派生物内の自分のパッケージの状況をより良く追跡することが可能になる\[62\]。

### Debian (テスト版) 派生

[Debianテスト版の派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian_\(Testing\)_based "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/BackTrack" title="wikilink">BackTrack</a></p></td>
<td><p>Debian派生であり、Kali Linuxの前身。<a href="https://ja.wikipedia.org/wiki/ペネトレーションテスト" title="wikilink">侵入テスト目的に特化していることが特徴だった</a>。開発停止。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Kali_Linux" title="wikilink">Kali Linux</a></p></td>
<td><p>Debian派生の1DVD型。侵入テスト目的に特化していることが特徴。BackTrackから<a href="../Page/フォーク_(ソフトウェア開発).md" title="wikilink">派生した後継版</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/PureOS.md" title="wikilink">PureOS</a></p></td>
<td><p>完全に自由ソフトウェアだけで構成されている、<a href="../Page/プライバシー.md" title="wikilink">プライバシー</a>と<a href="https://ja.wikipedia.org/wiki/セキュリティ" title="wikilink">保安</a>、利便性に重点を置いているGNU/Linuxディストリビューション。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ロシア連邦" title="wikilink">ロシアの政府機関における</a><a href="https://ja.wikipedia.org/wiki/:ru:Astra_Linux" title="wikilink">制式OSのひとつ</a>[63]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Ubuntu.md" title="wikilink">Ubuntu</a></p></td>
<td><p>6ヶ月ごとの更新と商用の保守を掲げる。デスクトップ環境として<a href="../Page/GNOME.md" title="wikilink">GNOME</a>を採用している。<a href="../Page/パソコン雑誌.md" title="wikilink">パソコン雑誌</a>に雑誌社特製のLive CD/DVDとして付属される場合がある。<a href="https://ja.wikipedia.org/wiki/Ubuntu#派生品" title="wikilink">多彩な派生版が存在</a>。</p></td>
</tr>
</tbody>
</table>

### Ubuntu 派生

[Ubuntu派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Ubuntu-based "wikilink")。
ここでは割愛し、*詳細は[Ubuntu\#派生品](https://ja.wikipedia.org/wiki/Ubuntu#派生品 "wikilink")に記述。*

### Debian (安定板) 派生

[Debian安定板の派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian_\(Stable\)_based "wikilink")。

<table>
<thead>
<tr class="header">
<th><p>配布版</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ロシア連邦" title="wikilink">ロシアの政府機関における</a><a href="https://ja.wikipedia.org/wiki/:ru:Astra_Linux" title="wikilink">制式OSのひとつ</a>。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>企業向けディストリビューションで<a href="../Page/Eee_PC.md" title="wikilink">Eee PCに搭載されていた</a>、後継版の<a href="../Page/Xandros.md" title="wikilink">Xandros</a>に移行。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CrunchBang_Linux" title="wikilink">CrunchBang Linux</a></p></td>
<td><p>ウィンドウマネージャにOpenBoxを採用し、軽量、高速を重視したディストリビューション。開発停止。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Deepin.md" title="wikilink">Deepin</a></p></td>
<td><p>Wuhan Deepin Technology Co.が開発を手掛ける、Debianを母体とした中国産 Linux ディストリビューション。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Devuan" title="wikilink">Devuan</a></p></td>
<td><p>2014 に Debianから派生[64]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/gNewSense" title="wikilink">gNewSense</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GNU_FSDG" title="wikilink">GNU FSDGに適合し</a>、<a href="../Page/フリーソフトウェア財団.md" title="wikilink">フリーソフトウェア財団</a>の支援を受ける。<a href="https://ja.wikipedia.org/wiki/Linux-libre" title="wikilink">Linux-libre</a>を使用し、ファームウェアのレベルまで100%自由ソフトで構成される。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>Debian派生でCD起動/HDD導入共可能。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/KNOPPIX.md" title="wikilink">KNOPPIX</a></p></td>
<td><p>Debianを基にCD起動で利用できるようにしている。派生版は<a href="https://ja.wikipedia.org/wiki/#KNOPPIX_派生" title="wikilink">#KNOPPIX 派生を参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Maemo" title="wikilink">Maemo</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Nokia_N800" title="wikilink">Nokia N800</a>, <a href="https://ja.wikipedia.org/wiki/Nokia_N810" title="wikilink">N810など携帯端末のほか</a>、<a href="https://ja.wikipedia.org/wiki/Nokia_N900" title="wikilink">Nokia N900</a> タブレット端末とその他の Linux kernel派生の機器向けに開発された[65]。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/MEPIS.md" title="wikilink">MEPIS</a></p></td>
<td><p>デスクトップ環境に<a href="../Page/KDE.md" title="wikilink">KDE</a>を採用したディストリビューション。開発停止。派生版は<a href="https://ja.wikipedia.org/wiki/#MEPIS_派生" title="wikilink">#MEPIS 派生を参照</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Linux_Mint.md" title="wikilink">MintPPC</a></p></td>
<td><p>PowerPC 向け。MintPPC は Mint LXDE のコードを用いるが、Linux Mint ではない[66]。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/GNOME.md" title="wikilink">GNOME</a>やWindowマネージャーの<a href="https://ja.wikipedia.org/wiki/fluxbox" title="wikilink">fluxbox</a>を使用するが前身。[67]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenZaurus" title="wikilink">OpenZaurus</a></p></td>
<td><p><a href="../Page/シャープ.md" title="wikilink">Sharp</a> <a href="../Page/ザウルス.md" title="wikilink">Zaurus</a> <a href="../Page/携帯情報端末.md" title="wikilink">PDA向け</a> Debian パッケージと ROM イメージ。 後継[68]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Raspberry_Pi_OS" title="wikilink">Raspberry Pi OS</a></p></td>
<td><p>小型シングルボードコンピュータである<a href="https://ja.wikipedia.org/wiki/Raspberry_Pi" title="wikilink">Raspberry Pi向けに開発されたディストリビューション</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Skolelinux" title="wikilink">Skolelinux</a></p></td>
<td><p><a href="../Page/ノルウェー.md" title="wikilink">ノルウェー</a>産 Linux で、学校向け <a href="https://ja.wikipedia.org/wiki/thin_client" title="wikilink">thin clientディストリビューション</a>[69]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SolydXK" title="wikilink">SolydXK</a></p></td>
<td><p><a href="../Page/Xfce.md" title="wikilink">Xfce</a> and <a href="../Page/KDE.md" title="wikilink">KDE</a> desktop focused on stability, security and ease of use.[70]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/The_Amnesic_Incognito_Live_System" title="wikilink">The Amnesic Incognito Live System</a> (TAILS)</p></td>
<td><p>プライバシーと匿名性の保護に特化したディストリビューション。<a href="https://ja.wikipedia.org/wiki/Tor#Torの応用" title="wikilink">Tor#Torの応用</a>も参照。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Vyatta" title="wikilink">Vyatta</a></p></td>
<td><p>VyOSの前身[71]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/VyOS" title="wikilink">VyOS</a></p></td>
<td><p><a href="../Page/Virtual_Private_Network.md" title="wikilink">VPN</a> / <a href="../Page/ルーター.md" title="wikilink">ルーター</a> / <a href="../Page/コンピュータネットワーク.md" title="wikilink">ネットワーク</a><a href="../Page/ファイアウォール.md" title="wikilink">ファイアウォール</a>用ディストリビューション。</p></td>
</tr>
</tbody>
</table>

### MEPIS 派生

[MEPISの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#MEPIS-based "wikilink")。

| 配布版                                                     | 説明                                                     |
| ------------------------------------------------------- | ------------------------------------------------------ |
| [antiX](https://ja.wikipedia.org/wiki/antiX "wikilink") | Debian安定版から派生した軽量な Live CD かつインストール（導入）可能なディストリビューション。 |
| [MX Linux](../Page/MX_Linux.md "wikilink")              | 中量級。KNOPPIXのように Live CD としても利用可能。                      |

### KNOPPIX 派生

[KnoppixFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:KnoppixFamilyTree1210.svg "fig:KnoppixFamilyTree1210.svg") [KNOPPIXの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Knoppix-based "wikilink")。
*[KNOPPIX\#その他の派生版](https://ja.wikipedia.org/wiki/KNOPPIX#その他の派生版 "wikilink")も参照。*

| 配布版                                                        | 説明                                                                                                                |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| [Damn Small Linux](../Page/Damn_Small_Linux.md "wikilink") | 名刺大の[CDやUSB](../Page/コンパクトディスク.md "wikilink") pendrive向けの軽量なKNOPPIX[Live CD](../Page/Live_CD.md "wikilink")。開発停止。 |

### その他の派生版

上記のようにDebianはいくつかのディストリビューションの母体として利用されている。[Debianの派生品一覧に非掲載であるるものの](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Debian-based "wikilink")、以下もその一部である。

なお、[Ubuntuの派生版や](https://ja.wikipedia.org/wiki/Ubuntu#派生品 "wikilink")、他言語版を含めWikipediaに記事が存在しないものは掲載しない。

#### 現行（2020.4.1）のDebian派生ディストリビューション

  - [Clonezilla](https://ja.wikipedia.org/wiki/Clonezilla "wikilink") - [ディスクまたは](../Page/補助記憶装置.md "wikilink")[パーティション](../Page/パーティション.md "wikilink")の複製（クローニング）ならびに[イメージ作成](../Page/ディスクドライブ仮想化ソフト.md "wikilink")（イメージング）用。
  - [LinEx](https://ja.wikipedia.org/wiki/gnuLinEx "wikilink") - [スペイン](https://ja.wikipedia.org/wiki/スペイン "wikilink")の地方自治体、教育機関で利用するために開発されたディストリビューション。
  - [Linux Mint Debian Edition(LMDE)](../Page/Linux_Mint.md "wikilink") - [Linux MintプロジェクトがDebian安定版をベースに開発したディストリビューション](../Page/Linux_Mint.md "wikilink")。
  - [OpenMediaVault](https://ja.wikipedia.org/wiki/OpenMediaVault "wikilink") - 無償な[ネットワークアタッチトストレージ](../Page/ネットワークアタッチトストレージ.md "wikilink")(NAS)向けディストリビューション。
  - Pengwin\[72\] - Debian派生。前身は[Red Hat Enterprise Linuxと互換性があるとされる](../Page/Red_Hat_Enterprise_Linux.md "wikilink") WLinux\[73\]\[74\]\[75\]。
  - [Puppy Linux](../Page/Puppy_Linux.md "wikilink") - [ver.5 以降はDebian系もあり](https://ja.wikipedia.org/wiki/Puppy_Linux#バージョン_5_以降 "wikilink")。
  - [SLAX](../Page/SLAX.md "wikilink") - Slax 9からはDebian系。元は[Slackware](../Page/Slackware.md "wikilink")の派生ソフト。CD起動で利用可能。日本語化された\[<http://hatochan.dyndns.org/slax-ja/index.php>? SLAX-ja\]も存在する。
  - [Voyager](https://ja.wikipedia.org/wiki/Voyager_\(オペレーティングシステム\) "wikilink")\[76\]\[77\]\[78\]\[79\] - [フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")産のOS。MacOS風の画面が美しい。Debian (安定板) から派生\[80\]した[32bit版と](../Page/32ビット.md "wikilink")[64bit版のほか](../Page/64ビット.md "wikilink")、[Xubuntu派生版もある](https://ja.wikipedia.org/wiki/Xubuntu#Voyager "wikilink")。
  - [Whonix](../Page/Whonix.md "wikilink") - 保安面重視のOS。通信はすべて[Tor](../Page/Tor.md "wikilink")経由でおこなう。
  - [WindOS](https://ja.wikipedia.org/wiki/WindOS "wikilink") - Debian Squeeze派生で作られた軽量OS。起動時の初期メモリ消費量が60MB以下。開発が停滞している\[81\]。

#### 開発終了及び休止したDebian派生ディストリビューション

  - [aptosid](https://ja.wikipedia.org/wiki/aptosid "wikilink") - 旧名sidux。Debian sid派生のデスクトップ向けディストリビューション。CD起動/HDD導入共可能。

  - : [Linspire](../Page/Linspire.md "wikilink")の無料版。CD起動/HDD導入共可能。

  - [Linspire](../Page/Linspire.md "wikilink") - 企業向けディストリビューション（旧名Lindows）。

  - [Progeny Debian](../Page/Progeny_Debian.md "wikilink") - Redhat/Fedoraのインストーラ[Anaconda](https://ja.wikipedia.org/wiki/Anaconda "wikilink")を移植したGNU/Linux。

  - [UserLinux](../Page/UserLinux.md "wikilink") - 元Debianプロジェクトリーダー[ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink")により提唱され、企業向けディストリビューションの基幹となるべく開発されていたDebian母体のディストリビューション。開発停止。

### 日本発の派生版

  - [ARMA aka Omoikane GNU/Linux](https://ja.wikipedia.org/wiki/ARMA_aka_Omoikane_GNU/Linux "wikilink") : [ファイルシステム](../Page/ファイルシステム.md "wikilink")に[XFS](../Page/XFS.md "wikilink")を採用している。
  - 巫女 GNYO/Linux : [openMosix](https://ja.wikipedia.org/wiki/openMosix "wikilink")と[SCore](https://ja.wikipedia.org/wiki/SCore "wikilink")を利用した[PCクラスタが構築可能](../Page/コンピュータ・クラスター.md "wikilink")。CD起動/HDD導入共可能。開発停止。
  - [Ubuntu\#日本発の派生品](https://ja.wikipedia.org/wiki/Ubuntu#日本発の派生品 "wikilink")
  - [KNOPPIX\#日本発の派生版](https://ja.wikipedia.org/wiki/KNOPPIX#日本発の派生版 "wikilink")

## 注釈

## 外部リンク

  -
### プロジェクトの公式リソース

  - [Debian Project](https://www.debian.org/)
  - [プロジェクトの歴史](https://www.debian.org/doc/manuals/project-history/)

### コミュニティサイト

  - [Debian Wiki](https://wiki.debian.org/ja/FrontPage)
  - [Debian JP Project](https://www.debian.or.jp/)

### カスタムDebianディストリビューション

[Debian Pure Blends](https://wiki.debian.org/DebianPureBlends)に一覧などがある。

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Ubuntu](../Page/Ubuntu.md "wikilink")

[Category:Debian](https://ja.wikipedia.org/wiki/Category:Debian "wikilink") [Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.   OSDN Magazine|url=[https://mag.osdn.jp/06/05/25/0324244|website=OSDN|accessdate=2020-04-09|language=ja](https://mag.osdn.jp/06/05/25/0324244%7Cwebsite=OSDN%7Caccessdate=2020-04-09%7Clanguage=ja)}}
9.
10.
11.  OSDN Magazine|url=[https://mag.osdn.jp/06/05/25/0324244|website=OSDN|accessdate=2020-04-09|language=ja](https://mag.osdn.jp/06/05/25/0324244%7Cwebsite=OSDN%7Caccessdate=2020-04-09%7Clanguage=ja)}}
12.  Ubuntu Japanese Team | publisher = www.ubuntulinux.jp | accessdate = 2011-04-13 | quote = 開発コミュニティ }}
13.
14.
15.
16.
17. <http://db.debian.org/>
18. <http://www.debian.org/social_contract>
19. <http://www.debian.org/devel/constitution>
20.
21. [Ohloh.net](http://www.ohloh.net/p/debian), Debian GNU/Linux
22.
23.
24. <http://www.debconf.org/>
25. <http://wiki.debian.org/DebConfInJapan>
26. [What does a Debian Project Leader do](http://www.debian.org/devel/leader) www.debian.org
27.
28.
29.
30. <http://www.debian.org/releases/squeeze/i386/release-notes/ch-whats-new.ja.html#pkgmgmt>
31. <http://www.debian.org/releases/squeeze/i386/release-notes/ch-upgrading.ja.html#upgrading-full>
32. <http://www.debian.org/doc/manuals/debian-reference/ch02.ja.html>
33. <http://www.jp.redhat.com/support/manuals/RHL62/ref-guide/ch-gnorpm.html>
34. Debian -- ニュース -- Debian は時間ベースのリリースフリーズを採用します: <https://www.debian.org/News/2009/20090729>
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48. <https://lists.debian.org/debian-release/2014/11/msg00749.html>
49. <https://lists.debian.org/debian-devel-announce/2016/07/msg00002.html>
50.  ソフトアンテナブログ|url=[https://www.softantenna.com/wp/software/debian-10-mid-2019/|website=www.softantenna.com|accessdate=2020-05-09](https://www.softantenna.com/wp/software/debian-10-mid-2019/%7Cwebsite=www.softantenna.com%7Caccessdate=2020-05-09)}}
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62. <https://debian-handbook.info/browse/ja-JP/stable/derivative-distributions.html>
63.
64.
65.
66.
67.
68.
69.
70.
71. [Vyatta website](http://www.vyatta.org/)
72. <https://forest.watch.impress.co.jp/docs/news/1179710.html> WSL向けに最適化されたLinuxディストロ「WLinux」が改称、「Pengwin」に
73. <https://news.mynavi.jp/article/20181218-742626/> Winodws 10にRHEL互換の新しいLinux「WLinux Enterprise」登場
74. [Windows 10に最適化されたLinuxディストロ「WLinux」が爆誕 - 期間限定の50%オフでセール中](https://www.softantenna.com/wp/windows/wlinux/)
75. [Windows 10 now has its own exclusive Linux distro -- WLinux](https://betanews.com/2018/09/24/windows-10-now-has-its-own-exclusive-linux-distro-wlinux/)
76. [Live Voyager](https://voyagerlive.org/)
77. [DistroWatch.com: Voyager Live](https://distrowatch.com/table.php?distribution=voyager)
78. [Voyager download | SourceForge.net](https://sourceforge.net/projects/voyagerlive/)
79. [Voyager 日本語情報トップページ - OSDN](https://ja.osdn.net/projects/sfnet_voyagerlive/)
80. [Voyager Live 10](https://distrowatch.com/?newsid=10634)
81.