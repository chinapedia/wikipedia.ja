> この記事は[Unix](https://ja.wikipedia.org/wiki/Unix)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Unix_history-simple.svg "wikilink") **Unix系**（ユニックスけい、ユニックスライク）とは、[Unixに類似した振る舞いをする](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) を指す用語である。その判断基準や範囲には複数の議論がある。

## UNIXの商標問題

ベル研究所のUnixの設計や機能を模倣したオペレーティングシステムは多数存在するが（一般にUnixの専門家の間で「ベル研究所のUnix」と言えば、いわゆる[Research Unixを指す](https://ja.wikipedia.org/wiki/Research_Unix "wikilink")。従って、次に述べる商標としてのUNIXの代表格である[System Vですら](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")、以上のような表現からは「設計や機能を模倣したオペレーティングシステム」に相当する）、現在、UNIXの名称は、[オープン・グループが](../Page/The_Open_Group.md "wikilink")[商標](../Page/商標.md "wikilink")を所有しており、彼らの管理する[Single UNIX Specificationを満たすシステムのみが](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink")、その認証の証明として「UNIX」を名乗ることができる。そこで、正式には「UNIX」と呼ぶことができないが、それに類似するオペレーティングシステムを指す言葉として「UNIX系」を用いることがある。

なお、オープン・グループのガイドラインでは、「UNIX」はすべて大文字で記述されるか、あるいは周りの文章と明確に区別され、「system」などの一般的な言葉に対して商標であることを示す言葉として使用し、ハイフンのついた語句として使用しないよう推奨している。これに従えば「unix-like」という表現も適切なものではなく、オープン・グループでは商標の乱用であるとして認めていない。UNIX類似のオペレーティングシステムを指す言葉としてオープン・グループが正しいと考えるのに最も近い言葉は「UNIX system-like」である\[1\]。

ただし、「[ゼロックス](../Page/ゼロックス.md "wikilink")」を[複写機](../Page/複写機.md "wikilink")の一般名称として用いるのと同じように、「UNIX」を[商標が普通名称化したものとして扱い](https://ja.wikipedia.org/wiki/商標の普通名称化 "wikilink")、あえて「Unix系」という言葉を用いないこともある。

一般的にはUNIXと類似のオペレーティングシステム全体を指して「Unix系」と表現することもある。

Unix系オペレーティングシステムには、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[MINIX](https://ja.wikipedia.org/wiki/MINIX "wikilink")、[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")、[XENIX](../Page/XENIX.md "wikilink")などのように、Unixに似た名称がつけられていることが多いため、「Un\*x」や「\*nix」のように婉曲的な略記法として[ワイルドカードをつける人もいる](../Page/ワイルドカード_\(情報処理\).md "wikilink")（後者はアスタリスクがワイルドカードに用いられることに引っ掛けて「アスタニクス」と発音される）。こうしたパターンは、それほど多くの名前に当てはまるわけではないのだが、[Solaris](../Page/Solaris.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")といった全く異なる名前を持つものも含め、一般的にはいかなるUnixの末裔たちも示すと認識されている。これもオープン・グループのガイドラインに反している。

2007 年現在、とオープン・グループの間でUNIXの名称を商標として使うことについての法的な闘争が行われている\[2\]。の法廷文書によると、グレイの弁護団はオープン・グループに、商標の主張を裏付ける文書の提出を求めているようである。

また、。

## 分類

UNIXの元々の製作者の一人である[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")は、LinuxなどのUnix系のシステムが[デファクト](https://ja.wikipedia.org/wiki/デファクト "wikilink")のUNIXシステムであるという意見を述べている。[エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")は、Unix系のシステムには次の3つの種類があるという考えを提案している:

  - 「遺伝上」のUNIX
    これらのシステムは、AT\&Tのコードベースに歴史的なつながりがある。ほぼすべての商用のUNIXシステムはここに分類される。[BSD](../Page/BSD.md "wikilink")システムもその一例であり、1970年代後半から1980年代初頭にかけての[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")における開発成果を受け継いでいる。これらのシステムには元々のAT\&Tのコードは入っていないが、その設計はAT\&TによるUNIXの設計に起源を持つ。
  - 商標やブランド上のUNIX
    これらのシステムは（もともと大部分は商用のものであるが）オープン・グループによってSingle UNIX Specificationに準拠していると判断され、UNIXの名を名乗ることを許されたものである。こうしたのシステムのほとんどは[System Vコードベースからのさまざまな形態の派生物であり](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")、一部のシステムはPOSIX互換レイヤでUNIX商標をとった（IBMの[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")など）が、これらはそうでなければそもそもUnixシステムではない。[Ancient UNIXの多くはもはやこの定義に入らない](https://ja.wikipedia.org/wiki/Ancient_UNIX "wikilink")。
  - 機能上のUNIX
    広い意味で、UNIXの仕様に合った振る舞いのUnix系のシステムの事を指し、より具体的には、UNIXと同様に振舞うが、「血統」や商標の上でのAT\&Tコードベースとのつながりのない[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")や[MINIX](https://ja.wikipedia.org/wiki/MINIX "wikilink")のようなシステムのことを示す。しかしながら、「遺伝上」のUnixであろうとなかろうと、UNIX準拠のほとんどのフリーソフトウェア/オープンソース実装は、この第三のカテゴリーに分類される。オープン・グループ仕様への認証を獲得する費用は高額であるがゆえに、認証が不可能だったり、そうでなくても他のもっと有用なことに予算を投じる結果になるためである。

## Unix系システムの発展

**[Unixの歴史](https://ja.wikipedia.org/wiki/Unixの歴史 "wikilink")**も参照。

Unix系システムは 1970年代後半や1980年代初頭に登場し始めた。（1978年）、（1983年）、（1985年）などの多数の[プロプライエタリのシステムがUNIXの学術機関のユーザーに利用できる機能をもとにビジネスを行うことを目標としていた](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。

後に1980年代、AT\&TがUNIXの商用ライセンスを許可した時、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Tru64](https://ja.wikipedia.org/wiki/Tru64_UNIX "wikilink")、[Ultrix](https://ja.wikipedia.org/wiki/Ultrix "wikilink")、[XENIX](../Page/XENIX.md "wikilink")などの多数のプロプライエタリのシステムが開発された。これらのシステムの間で発生した相互運用性の問題が、後に[POSIX](../Page/POSIX.md "wikilink")やSingle UNIX Specificationなどの相互運用性の標準を策定することにつながった。

一方、1983年に、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")が、[GNU](../Page/GNU.md "wikilink")と呼ばれるいかなるコンピューターのユーザーも自由に使用でき、学習、改変、再配布も自由なオペレーティングシステムを作り上げるという目的で始まった。GNUと同じころ開発された多数のUnix系オペレーティングシステムには、GNUと相当な量のコンポーネントを共有しているものが多かった（結果的に、これらをGNUと呼ぶべきかで論争が起きた）。これらのOSはまず、UNIXの低コストで制約の少ない代替物としての役割を果たした。[4.4BSD](../Page/BSD.md "wikilink")、Linux、MINIXなどである。[BSD/OS](https://ja.wikipedia.org/wiki/BSD/OS "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のように、こうしたシステムの商用のUnix系システムの基となったものもある。特に、[Mac OS X v10.5はSingle](../Page/Mac_OS_X_v10.5.md "wikilink") UNIX Specificationの認証を受けている\[3\]"UNIX"である。

BSDの変種は、実はUNIXの子孫であり、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")でベル研究所のソースコードを用いて開発されたものである。しかし、BSDのコードはそれ以降進化し続け、すべてAT\&Tのコードを置換しようとしている。BSDの変種は（v10.5以降のmacOSを除き）Single UNIX Specification準拠の認証を受けていないため、Unix系と呼ばれる。

## 現行のシステムの例

[オープンソース](../Page/オープンソース.md "wikilink")のUnix系システムのベンダーは、認証のコストが法外に高いとみなされているため、仮に仕様に準拠していても、製品にUNIXのブランドを求めようとしていない。Freenixという用語がこうしたシステムを示すために用いられることがある。例としてGNU、Linux、MINIX、OpenSolaris、Plan 9、BSDとその変種がある。BSDのうち特に有名なものとして、FreeBSD、NetBSD、OpenBSDなどがある。

現在プロプライエタリのUnix系システムは多数あり、AIX、BeOS、HP-UX、IRIX、macOS（10.4 以前）、LynxOS、QNX、SCO OpenServer、Solaris、[Tru64](https://ja.wikipedia.org/wiki/Tru64_UNIX "wikilink")（OSF/1 に基づく）、UnixWare、XENIX、VxWorksなどが存在する。

## 参考文献

## 関連項目

  - [Berkeley Software Distribution](https://ja.wikipedia.org/wiki/Berkeley_Software_Distribution "wikilink")（BSD）
  - [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")
  - [POSIX](../Page/POSIX.md "wikilink")
  - [PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")

## 外部リンク

  - [Unix-like Definition](http://www.linfo.org/unix-like.html)
  - [UNIX history](https://www.levenez.com/unix/)
  - [Grokline's UNIX Ownership History Project](http://grokline.net/)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink")

1.  <http://www.opengroup.org/tm-guidelines.htm>
2.  [TTABVUE. Trademark Trial and Appeal Board Inquiry System](http://ttabvue.uspto.gov/ttabvue/v?qt=adv&pno=&qs=&propno=75680034&propnameop=&propname=&pop=&pn=&pop2=&pn2=&cop=&cn=)
3.  Apple - Mac OS X Leopard - Technology - UNIX. <http://www.apple.com/macosx/technology/unix.html>