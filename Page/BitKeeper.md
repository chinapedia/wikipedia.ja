> この記事は[BitKeeper](https://ja.wikipedia.org/wiki/BitKeeper)から翻訳されています。


**BitKeeper** は、コンピュータの[ソースコード](../Page/ソースコード.md "wikilink")の[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")（[構成管理](../Page/構成管理.md "wikilink")、[SCMなど](../Page/ソフトウェア構成管理.md "wikilink")）の一種である。[Rational ClearCase](../Page/Rational_ClearCase.md "wikilink") や [Perforce](../Page/Perforce.md "wikilink") と競合している。BitMover Inc. が開発した（[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")キャンベル、かつて  を設計した[ラリー・マクボイ](https://ja.wikipedia.org/wiki/ラリー・マクボイ "wikilink")が[CEOを務める](../Page/最高経営責任者.md "wikilink")）。

BitKeeper は TeamWare のコンセプトに基づいて構築された。最大の利点は、分散開発において、各開発者の手元のローカルなリポジトリと中心のリポジトリの整合を取りつつ開発が進められる点である。

BitKeeper は元々[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")であるが、開発開始から15年以上を経た[2016年](../Page/2016年.md "wikilink")5月リリースの7.2-ossをもって[オープンソース](../Page/オープンソース.md "wikilink")化された。以後は[Apache License 2.0で提供されている](../Page/Apache_License.md "wikilink")。\[1\]

## OSSコミュニティとの対立

BitKeeperはその高い性能から、[2002年](../Page/2002年.md "wikilink")から[2005年](../Page/2005年.md "wikilink")にかけて[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のソースコード管理にも用いられた。しかし、そのライセンス条件を巡ってOSSコミュニティとの間で大きな議論を引き起こすこととなった。

### 背景

BitMover 社は[オープンソース](../Page/オープンソース.md "wikilink")や[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のプロジェクトに BitKeeper の利用を無料で提供していた。これには有名な（そして物議をかもした）[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のソースコード管理も含まれていた。この際のライセンスには BitKeeper をオープンソースやフリーソフトウェアのプロジェクトで無料で利用する際の条件がつけられていた。それは、BitKeeper を無料で利用した開発者は利用をやめてから1年間まで競合するツール（[CVS](../Page/Concurrent_Versions_System.md "wikilink")、[GNU Arch](../Page/Arch.md "wikilink")、[Subversion](../Page/Apache_Subversion.md "wikilink")、[ClearCase](https://ja.wikipedia.org/wiki/ClearCase "wikilink")など）の開発に関わってはならないというものであった。この条件は競合ツールがオープンソースであってもフリーであってもプロプライエタリであっても適用される。また、このバージョンのBitKeeperでは、利用を許諾していないプロジェクトで使われることがないよう、BitMover 社が運営するサーバ ([www.openlogging.org](http://www.openlogging.org)) と一種のメタ情報をやり取りするようになっていた。

### ライセンス問題

Linux カーネル開発に BitKeeper を採用するという決定（2002年）には異論があった。例えば、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の創始者[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は最も有名なフリーソフトウェアプロジェクトで商用ツールを利用することに懸念を表明した。Linux のリーダーである[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")や主要な開発者は BitKeeper 採用に積極的だったが、一部の主要開発者（[アラン・コックス](https://ja.wikipedia.org/wiki/アラン・コックス "wikilink")など）は BitMover によるライセンス条件がプロジェクトの方向性をある程度制限する（あるいは企業によってLinux開発が管理される）ものであるとして反対した。このような懸念を払拭するため、BitMover は Linux の BitKeeper サーバ（BitMover が管理）と CVS や Subversion を使っている開発者との間にゲートウェイを追加した。その後も主要な開発者と自らも Linux 開発者である BitMover の CEO Larry McVoy を巻き込んだ論争が起きた。\[2\]。

### 価格変更

[2005年](../Page/2005年.md "wikilink")4月、BitMover は無料での BitKeeper 提供をやめると発表した。これは、[アンドリュー・トリジェル](https://ja.wikipedia.org/wiki/アンドリュー・トリジェル "wikilink")がやったことが原因であった。彼は、[OSDL](../Page/Open_Source_Development_Labs.md "wikilink") で Linuxカーネルとは関係ないプロジェクトにも関わっており、BitKeeper の最新版以外のメタデータ（差分を含むリビジョンデータ）を見られるクライアントを開発しようとしていた。メタデータを参照して過去のバージョンとの差分を見ることはバージョン管理システムの根幹の機能であり、BitKeeper のライセンスが提供されない者には見ることができない。これは、ライセンスを持たない Linux カーネル開発者にとっては非常に不便だった。BitMover は一部のカーネル開発者には商用 BitKeeper を無料で提供することを決定したが、OSDL の従業員には無料提供も販売もしないとした。これには、[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")や[アンドリュー・モートンも含まれる](https://ja.wikipedia.org/wiki/アンドリュー・モートン_\(プログラマ\) "wikilink")。このため、Linux のソース管理ソフトウェアとして [Git](../Page/Git.md "wikilink") プロジェクトが開始されることとなった。

無償提供の期限は[2005年](../Page/2005年.md "wikilink")7月1日までとされ、ユーザーはそれまでに商用版への移行かバージョン管理システムを別のものにする必要が生じた。商用版のユーザーも競合ツールを開発しないことを要求される。2005年10月、McVoy は BitKeeper 商用版を利用しているある顧客に対して、同企業の従業員が GPL のソース管理ツール [Mercurial](../Page/Mercurial.md "wikilink") の開発に参加しているのをやめさせるよう求めた。当の従業員 Bryan O'Sullivan はこれに対して「競合の可能性を避けるため、私は BitKeeper の商用版を使い続ける限り、Mercurial の開発に関与しないことを Larry に申し出た」としている\[3\]。

### オープンソース化

BitMoverは一連の騒動から11年を経た[2016年](../Page/2016年.md "wikilink")5月に、BitKeeperを[オープンソース](../Page/オープンソース.md "wikilink")の下でリリースした。

## 関連項目

  - [Git](../Page/Git.md "wikilink")

## 脚注

## 外部リンク

  - [bitkeeper.org](http://www.bitkeeper.org/)
  - [bitkeeper.com](http://www.bitkeeper.com/)
  - ["Not quite Open Source"](http://lwn.net/1999/features/BitKeeper.php3) Linux Weekly News（1999年ごろ）の記事。機能、ライセンス、Larry McVoy、OSI について。
  - [嵐の後のBitkeeper（パート1）](https://osdn.jp/magazine/04/05/13/0115228) [OSDN](../Page/OSDN.md "wikilink") Magazine
  - [嵐の後のBitkeeper（パート2）](https://osdn.jp/magazine/04/05/16/1130243) [OSDN](../Page/OSDN.md "wikilink") Magazine
  - ["No More Free BitKeeper"](http://archive.is/20120523214930/kerneltrap.org/node/4966) BitMover が無料版の提供をやめることについての議論
  - ["BitKeeper and Linux: The end of the road?"](http://www.linux.com/archive/articles/44147) BitKeeper の失敗について、[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")、Larry McVoy、 [アンドリュー・トリジェル](https://ja.wikipedia.org/wiki/アンドリュー・トリジェル "wikilink")の三者の観点で論じている。
      - [BitKeeperとLinux――蜜月の終わり](https://osdn.jp/magazine/05/04/13/0232209) 上記の翻訳記事。[OSDN](../Page/OSDN.md "wikilink") Magazine提供。
  - [SourcePuller](http://sourceforge.net/projects/sourcepuller/) トリジェルの成果
  - [News Forge](http://software.newsforge.com/article.pl?sid=05/04/25/130207) [リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")
      - [RMS: BitKeeperとの決別はハッピーエンド](https://osdn.jp/magazine/05/04/28/0243241) 上記の翻訳記事。[OSDN](../Page/OSDN.md "wikilink") Magazine提供。
  - [The Age](http://www.theage.com.au/news/Soapbox/Crunch-time-for-Linus/2005/04/14/1113251731624.html) Crunch time for Linus
  - [BitKeeper at the "Better SCM" Site](http://better-scm.berlios.de/bk/) - BitKeeper とその歴史について
  - [BitKeeper紛争を受け、トーバルズ氏が新プロジェクト](http://www.itmedia.co.jp/enterprise/articles/0504/20/news075.html) [ITmedia](../Page/ITmedia.md "wikilink") エンタープライズ、2005年4月20日

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink")

1.
2.
3.