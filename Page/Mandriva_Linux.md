> この記事は[Mandriva Linux](https://ja.wikipedia.org/wiki/Mandriva_Linux)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Mandriva-2007-spring-ja.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Mandriva_2007_screenshot-ja.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Mandriva_2006_Screenshot.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Mandriva_Linux-LE2005.png "wikilink")

**Mandriva Linux**（マンドリーバ・リナックス）は、かつて存在した[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の一つである。旧名称はMandrakelinux。

## 概要

開発母体はフランスの [Mandriva](https://ja.wikipedia.org/wiki/Mandriva "wikilink")（旧MandrakeSoft）で、同社の共同創設者であるによって始められた。1998年7月、[Red Hat Linuxをベースにして](../Page/Red_Hat_Linux.md "wikilink")、最初のバージョンであるLinux Mandrake 5.1をリリースした。

[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")クラス以上のCPU用に最適化されるように設計されている。[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")は、2010.2までは[GNOME](../Page/GNOME.md "wikilink")と[KDE](../Page/KDE.md "wikilink")を標準でサポートし、インストール時にユーザーが選択することができる。[Xfce](../Page/Xfce.md "wikilink")もオプションで用意される。2011ではKDEのみのサポートとなった。

## 旧Mandrakeの名称

当初、バージョン5.1から8.0までは**Linux Mandrake**、8.1から9.2までは**Mandrake Linux**という名称であった。しかし、[商標権](https://ja.wikipedia.org/wiki/商標権 "wikilink")を侵害しているとの理由でMandrakeSoft（当時）が提訴されたため、同社は対策として10.0から10.1までの名称は、MandrakeとLinuxの間のスペースを取り除くとともにLinuxの"L"を小文字に変えて一つの単語にし、**Mandrakelinux**とした。

## MandrakeからMandrivaへ

MandrakeSoftがブラジルのLinuxディストリビューターであるConectiva社を買収したため、2005年4月7日、**Mandriva**に社名変更したことに伴いMandrakelinuxも**Mandriva Linux**へ名称変更する。「Mandriva」とは**Mandr**akeとConect**iva**の名称を掛け合わせたものである。この名称変更によって商標権の問題は沈静化する見込みである。開発ロードマップも変更され、Conectiva社のLinuxディストリビューションであったConectiva Linuxとの統合を図ることとなった。

旧MandrakelinuxとConectiva Linuxの統合ディストリビューションは2006年に完成する見込みであると発表された。完成するまでの臨時の措置として、2005年4月13日に「Mandriva Linux Limited Edition 2005」をリリースした。Limited Edition 2005は「Mandriva Linux」の名でリリースされたが、まだConectiva Linuxの統合部分は含まれておらず、旧Mandrakelinuxのシステムで構築されており、システム内では「Mandrakelinux」という名称が使われたままであった。旧Mandrakelinuxのシステムでのリリースはこれが最後となった。

同社創業者の一人であった Gaël Duval はその後解雇され、新たなLinuxディストリビューションの開発に従事している\[1\]。もともと開発者層が比較的厚いとされるMandrivaではあるが、近年では、Linux Mandrake 7.0からMandriva Linux 2007に至る7年間の間にリリースマネージャとして関わってきた Warly が2007年2月にMandrivaを去ったり、パッケージマネージャであった Texstar が[PCLinuxOS](../Page/PCLinuxOS.md "wikilink")というLinuxディストリビューションを開発してユーザーに影響を与えるなど、主要な開発者の異動が見られた。

2010年9月には主要な開発者やコミュニティがMandriva Linuxから独立し、[Mageia](https://ja.wikipedia.org/wiki/Mageia "wikilink")（マギア）という[フォークを立ち上げている](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。Mandriva Linux自体もフリー版は[OpenMandriva Lxとしてフォークし](https://ja.wikipedia.org/wiki/OpenMandriva_Lx "wikilink")、OpenMandriva Associationに移管している。Mandriva社は商用版に専念することとなった。

2015年5月にMandriva社は倒産したため、開発も、事実上終了した\[2\]。

## メンテナンスの容易さ

### urpmi

urpmi\[3\] は "User mode rpm install" というMandriva Linux独自の[パッケージ管理ツールであり](../Page/パッケージ管理システム.md "wikilink")、[APT](../Page/APT.md "wikilink")のようにパッケージ間の依存関係も自動的に解決しつつ、任意のパッケージのインストールや削除を行うことができる。urpmiには、グラフィカルな[フロントエンド](../Page/フロントエンド.md "wikilink")としてgurpmiが存在する\[4\]。

### rpmdrake

Mandriva Linuxには、rpmdrakeというグラフィカルなパッケージ管理ツールも用意されている。実質的にはurpmiによって内部処理が実行される。

さらに、デスクトップ上のパネルには、最新パッケージの更新を自動的に通知するアイコンが置かれている。2007 Springのバージョン以降は、Mandriva Clubの会員となってオンラインアップデートのサブスクリプションを購入しなくても、この[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")を利用して自動更新が行えるようになった。\[5\]

### Smartパッケージ・マネージャ

Smartパッケージ・マネージャとは、かつてブラジルに存在したConectiva社の技術者 Gustavo Niemeyerによって新規に開発されたパッケージ管理ツールである\[6\]。現在、Conectiva社はMandriva社に吸収合併されたため、SmartはオプションとしてMandriva Linuxでも公式に提供されるようになった。専用のグラフィカルなインターフェースも備えており、Mandriva Linux以外の多くのLinuxディストリビューションにおいても、このパッケージ・マネージャが配布されるようになった。

## 歴史

リリース年月日 / リリース名（※括弧内はコードネームあるいは正式名）

  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[7月23日](https://ja.wikipedia.org/wiki/7月23日 "wikilink") Linux Mandrake 5.1 （Venice） リリース
  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[12月1日](../Page/12月1日.md "wikilink") Linux Mandrake 5.2 （Leeloo） リリース
  - [1999年](../Page/1999年.md "wikilink")[2月11日](../Page/2月11日.md "wikilink") Linux Mandrake 5.3 （Festen） リリース
  - [1999年](../Page/1999年.md "wikilink")[5月27日](../Page/5月27日.md "wikilink") Linux Mandrake 6.0 （Venus） リリース
  - [1999年](../Page/1999年.md "wikilink")[9月14日](../Page/9月14日.md "wikilink") Linux Mandrake 6.1 （Helios） リリース
  - [2000年](../Page/2000年.md "wikilink")[1月14日](../Page/1月14日.md "wikilink") Linux Mandrake 7.0 （Air） リリース
  - [2000年](../Page/2000年.md "wikilink")[6月13日](../Page/6月13日.md "wikilink") Linux Mandrake 7.1 （Helium） リリース
  - [2000年](../Page/2000年.md "wikilink")[10月30日](../Page/10月30日.md "wikilink") Linux Mandrake 7.2 （Odyssey） リリース ※ベータ版でのコードネームは「Ulysses」
  - [2001年](../Page/2001年.md "wikilink")[4月19日](../Page/4月19日.md "wikilink") Linux Mandrake 8.0 （Traktopel） リリース
  - [2001年](../Page/2001年.md "wikilink")[10月22日](../Page/10月22日.md "wikilink") Mandrake Linux 8.1 （Vitamin） リリース
  - [2002年](../Page/2002年.md "wikilink")[3月18日](../Page/3月18日.md "wikilink") Mandrake Linux 8.2 （Bluebird）リリース
  - [2002年](../Page/2002年.md "wikilink")[11月7日](../Page/11月7日.md "wikilink") Mandrake Linux 9.0 （Dolphin） リリース
  - [2003年](../Page/2003年.md "wikilink")[3月25日](https://ja.wikipedia.org/wiki/3月25日 "wikilink") Mandrake Linux 9.1 （Bamboo） リリース
  - [2003年](../Page/2003年.md "wikilink")[10月14日](../Page/10月14日.md "wikilink") Mandrake Linux 9.2 （FiveStar） リリース
  - [2004年](../Page/2004年.md "wikilink")[3月4日](../Page/3月4日.md "wikilink") Mandrakelinux 10.0 （10.0 Community） リリース ※コミュニティによるフィードバックを目的としたリリース
  - [2004年](../Page/2004年.md "wikilink")[4月14日](../Page/4月14日.md "wikilink") Mandrakelinux 10.0 （10.0 Official） リリース ※Community版でのフィードバックを元に、改良した版のリリース
  - [2004年](../Page/2004年.md "wikilink")[9月16日](../Page/9月16日.md "wikilink") Mandrakelinux 10.1 （10.1 Community） リリース
  - [2004年](../Page/2004年.md "wikilink")[10月27日](../Page/10月27日.md "wikilink") Mandrakelinux 10.1 （10.1 Official） リリース
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[4月7日](../Page/4月7日.md "wikilink") **Mandriva Linux**に名称変更。
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[4月13日](../Page/4月13日.md "wikilink") Mandriva Linux Limited Edition 2005 （10.2 Official） リリース
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[10月6日](../Page/10月6日.md "wikilink") Mandriva Linux 2006 (2006 Official) リリース
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[11月14日](../Page/11月14日.md "wikilink") Mandriva Linux 2006 Free Download Edition リリース
  - [2006年](../Page/2006年.md "wikilink")[10月4日](https://ja.wikipedia.org/wiki/10月4日 "wikilink") Mandriva Linux 2007 (2007 Official) Commercial Edition リリース
  - [2006年](../Page/2006年.md "wikilink")[10月5日](../Page/10月5日.md "wikilink") Mandriva Linux 2007 Free Download Edition リリース
  - [2007年](../Page/2007年.md "wikilink")[4月17日](../Page/4月17日.md "wikilink") Mandriva Linux 2007 Spring (2007.1 Official) リリース
  - [2007年](../Page/2007年.md "wikilink")[10月9日](../Page/10月9日.md "wikilink") Mandriva Linux 2008 (2008.0 Official) リリース
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月9日](../Page/4月9日.md "wikilink") Mandriva Linux 2008 Spring (2008.1 Official) リリース
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[10月9日](../Page/10月9日.md "wikilink") Mandriva Linux 2009 (2009.0 Official) リリース
  - [2009年](../Page/2009年.md "wikilink")[4月29日](../Page/4月29日.md "wikilink") Mandriva Linux 2009 Spring (2009.1 Official) リリース
  - [2009年](../Page/2009年.md "wikilink")[11月3日](https://ja.wikipedia.org/wiki/11月3日 "wikilink") Mandriva Linux 2010 (2010.0 Official) リリース
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[7月8日](https://ja.wikipedia.org/wiki/7月8日 "wikilink") Mandriva Linux 2010 Spring (2010.1 Official) リリース
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月22日](../Page/12月22日.md "wikilink") Mandriva Linux 2010.2 (2010.2 Official) リリース
  - [2011年](../Page/2011年.md "wikilink")[8月29日](../Page/8月29日.md "wikilink") Mandriva Linux 2011 (2011 Official) リリース

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")
  - [Mageia](https://ja.wikipedia.org/wiki/Mageia "wikilink")
  - [PCLinuxOS](../Page/PCLinuxOS.md "wikilink")

## 注釈

<references />

## 外部リンク

  - [Mandriva Linux 公式ウェブサイト](http://www.mandriva.com/)（英語）

<!-- end list -->

  - [Mandriva Japan （コミュニティWiki）(Mandriva Community Wiki)](http://wiki.mandriva.com/ja/) （日本語）

<!-- end list -->

  - [Mandriva Development Community Wiki (Cooker)](http://qa.mandriva.com/twiki/bin/view/Main/MandrivaLinuxJa) （日本語アーカイブ）
  - [MandrivaLinuxインストールFAQ集 - 2ch-Linux-Beginners](http://www12.atwiki.jp/linux2ch/pages/33.html)（日本語）
  - [Mandriva Linux 10.1 メモ (サーバー運用中心の日本語解説サイト)](http://tkns.homelinux.net/memo/index.html#mandrivalinux10.1)
  - [Mandrivaへの社名変更に関するプレスリリース （英語）](http://www.mandriva.com/company/press/pr?n=/pr/corporate/2551)
  - <http://expert.mandriva.com/>
  - <http://store.mandriva.com/>
  - <http://club.mandriva.com/xwiki/bin/view/Main/>

[Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink")

1.  2007年からは 仮想デスクトップソフトウェア [Ulteo](https://ja.wikipedia.org/wiki/:en:Ulteo "wikilink") のCEOを務めている
2.  [かつて人気を誇った「Mandriva Linux」、開発母体が倒産](http://japan.zdnet.com/article/35065131/)ZDNet Japan 2015年5月28日
3.  <http://wiki.mandriva.com/en/Tools/urpmi>
4.  <http://wiki.mandriva.com/en/Tools/urpmi#gurpmi>
5.  <https://www.mandrivaonline.com/page.php> "From Mandriva Linux 2007 Spring, you can get instant updates notifications directly through the desktop applet icon, without subscribing to the service."
6.  <http://labix.org/smart>