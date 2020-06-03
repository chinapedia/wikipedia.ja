> この記事は[Avahi](https://ja.wikipedia.org/wiki/Avahi)から翻訳されています。


**Avahi**（アバヒ）は、[Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf "wikilink")の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")実装であり、[マルチキャスト](../Page/マルチキャスト.md "wikilink")[DNS](../Page/Domain_Name_System.md "wikilink")/DNS-SD サービスディレクトリのためのシステムを含む。

## 概要

Avahi は、特定の構成情報のないローカルネットワーク上のサービスホストの発行と発見を可能とする。例えば、ネットワークに接続したとき、即座にプリンタを検出し、ファイルを探し出し、他者と会話できるようにする。[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) の条件でライセンス提供される。

Avahi は[Bonjour](../Page/Bonjour.md "wikilink")のZeroconf仕様の実装であり、マルチキャストDNS、DNS-SD、RFC 3927/IPv4LL を実装している。各種[言語バインディング](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")を提供しており（[Python](../Page/Python.md "wikilink")、[Monoなど](../Page/Mono_\(ソフトウェア\).md "wikilink")）、多くの [Linux](../Page/Linux.md "wikilink") や [BSD](../Page/BSD.md "wikilink") 系のディストリビューションに付随して出荷されている。[モジュール化](https://ja.wikipedia.org/wiki/モジュール化 "wikilink")されているため、Avahi は [GNOME](../Page/GNOME.md "wikilink")の[GNOME VFSや](https://ja.wikipedia.org/wiki/GNOME_VFS "wikilink")[KDE](../Page/KDE.md "wikilink")の[KIO](https://ja.wikipedia.org/wiki/KIO "wikilink")などに組み込まれている。

Avahi プロジェクトは、[Bonjour](../Page/Bonjour.md "wikilink")のライセンスに関する論争から開始された。その後、Bonjour のライセンスは問題のない[Apache Licenseで提供されるようになった](../Page/Apache_License.md "wikilink")。しかし、そのころには既に Avahi が GNU/Linux などのフリーな[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でのデファクトスタンダードの地位を築いていた。

[アップルでの](../Page/アップル_\(企業\).md "wikilink") Zeroconf 技術開発に携わった Stuart Cheshire は Avahi の状況について「アップルの実装に取って代わる」勢いであると述べた\[1\]。

## 歴史

Avahi の開発は [Lennart Poettering](https://ja.wikipedia.org/wiki/レナート・ポッターリング "wikilink") と Trent Lloyd が当初行った。Poettering は 2004 年後半から FlexMDNS という名称で Zeroconf 機能の実装を行っていた。また、Lloyd は2004年前半から Avahi という名称で同様のプロジェクトを開始していた。両者のプロジェクトが2005年に合併し、名称としては Avahi が存続したが、コードの多くは FlexMDNS のものが存続している。

当初、Avahi は [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") 傘下のプロジェクトとして開発が行われていたが、2006年1月リリースの 0.6.2 より The Avahi Project として独立した\[2\]。ただし、Avahi は freedesktop.org の [D-Bus](../Page/D-Bus.md "wikilink") を利用している。

*Avahi* とは、[キツネザル下目](../Page/キツネザル下目.md "wikilink")・[インドリ科](https://ja.wikipedia.org/wiki/インドリ科 "wikilink")の[ウーリーキツネザル(アバヒ属)のことであり](https://ja.wikipedia.org/wiki/:en:Woolly_lemur "wikilink")、マダガスカルだけに棲む霊長類である。Trent Lloyd がこの名前を気に入って採用した。ロゴもこれを反映してキツネザルの顔になっている。\[3\]

## 関連項目

  - [Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf "wikilink")
  - [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")
  - [Lightweight Directory Access Protocol](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")(LDAP)
  - [ネットワーク・インフォメーション・サービス](../Page/ネットワーク・インフォメーション・サービス.md "wikilink")(NIS)
  - [OSGi](../Page/OSGi.md "wikilink")

## 脚注

<references />

## 外部リンク

  - [Avahi project](http://avahi.org/)

[Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  Stuart Cheshire (November 2,2005) "[Zero Configuration Networking with Bonjour](http://video.google.com/videoplay?docid=-7398680103951126462)" Google TechTalks.(flash形式のビデオ)
2.  [Milestone Avahi 0.6.2 – Avahi](http://avahi.org/milestone/Avahi%200.6.2)
3.  [Avahi talk](http://mirror.linux.org.au/linux.conf.au/2007/video/monday/monday_1150_GNOME.ogg) by Poettering/Lloyd at [linux.conf.au](https://ja.wikipedia.org/wiki/linux.conf.au "wikilink") 2007.（OGG形式のビデオ）