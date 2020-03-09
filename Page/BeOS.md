> この記事は[BeOS](https://ja.wikipedia.org/wiki/BeOS)から翻訳されています。


{{ infobox OS | name = BeOS | screenshot = | caption = BeOS PR2 | developer = [Be社](https://ja.wikipedia.org/wiki/Be社 "wikilink") | family = BeOS | source_model = [クローズドソース](https://ja.wikipedia.org/wiki/クローズドソース "wikilink") | working_state = 既に終了 | kernel_type = [モジュラー](https://ja.wikipedia.org/wiki/モジュール "wikilink") [ハイブリッドカーネル](https://ja.wikipedia.org/wiki/ハイブリッドカーネル "wikilink") | license = [プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink") | website = <http://www.beincorporated.com/> }} **BeOS**（ビーオーエス）は、米[Be社](https://ja.wikipedia.org/wiki/Be社 "wikilink")が開発した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。

## 特徴

BeOSのコードは[UNIX](../Page/UNIX.md "wikilink")などの既存の[コードをベースとするのではなく](../Page/ソースコード.md "wikilink")、すべて新しく書き起こされた。

同社の[ワークステーション](https://ja.wikipedia.org/wiki/ワークステーション "wikilink")である[BeBox](https://ja.wikipedia.org/wiki/BeBox "wikilink")、または[Power Mac](https://ja.wikipedia.org/wiki/Power_Mac "wikilink")、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で動作し、メディアOSとして[マルチメディア](https://ja.wikipedia.org/wiki/マルチメディア "wikilink")を扱うことに長けていた。洗練された設計で、非常に高性能なOSである。発表当時同じ[PowerPC](../Page/PowerPC.md "wikilink")で動く[Mac OSよりも遥かに高速に動作し](../Page/Classic_Mac_OS.md "wikilink")、「PowerPCの真価を発揮した」とユーザーを驚かせた。

技術的な特徴として次のようなものがある。

  - [POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")と互換性がある。
  - [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")を採用。これは[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")対応を最初から意識した設計である。
  - [APIが](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインタフェース "wikilink")[オブジェクト指向の言語](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")[C++](../Page/C++.md "wikilink")で書かれている。
  - 全体が高度に[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")・[マルチタスク](https://ja.wikipedia.org/wiki/マルチタスク "wikilink")化されており、並列・並行処理のパフォーマンスに優れる。
  - [データベース](../Page/データベース.md "wikilink")のように動作する、[ジャーナルファイルシステム対応](https://ja.wikipedia.org/wiki/ジャーナリングファイルシステム "wikilink") [64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")ファイルシステム [BFS](https://ja.wikipedia.org/wiki/Be_File_System "wikilink")。
  - シングルユーザーのパーソナル指向OS。

OS単体での販売が終了した後でも、楽器メーカーの[ローランド](https://ja.wikipedia.org/wiki/ローランド "wikilink")が[エディロール](https://ja.wikipedia.org/wiki/エディロール "wikilink")のブランドでビデオ編集専用機のDV-7DLで組み込みOSとして使用\[1\]しており、単体のシステムとしてより若干長く現役で活躍していたOSでもある。

## 歴史

### PowerPCプラットフォームでの展開

[アップルのヨーロッパ部門で好成績を収め](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")、後にアップル本社で開発責任者を務めた[ジャン＝ルイ・ガセー](https://ja.wikipedia.org/wiki/ジャン＝ルイ・ガセー "wikilink")（）らが[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[スピンアウトしてBe社を設立](https://ja.wikipedia.org/wiki/スピンオフ "wikilink")、[ハードウェア](../Page/ハードウェア.md "wikilink")[BeBox](https://ja.wikipedia.org/wiki/BeBox "wikilink")とオペレーティングシステム **BeOS**の開発を開始する。初期のBeBoxの[プロトタイプ](https://ja.wikipedia.org/wiki/プロトタイプ "wikilink")は[AT\&T](https://ja.wikipedia.org/wiki/AT&T "wikilink")の[Hobbit](https://ja.wikipedia.org/wiki/Hobbit "wikilink")という[プロセッサーを使用していたが](https://ja.wikipedia.org/wiki/マイクロプロセッサー "wikilink")、後に[PowerPC](../Page/PowerPC.md "wikilink")ベースに変更され、その上で動くBeOSとともに[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に一般に公開された。

翌年にはBeOSは[Power Macintoshに移植され](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")、[Mac OSの次世代OS候補として注目を集めることになった](../Page/Classic_Mac_OS.md "wikilink")（BeBox事業は終了したが、サポートはその後数年間継続した）。旧弊なMac OSに代わる次世代OSを求めている事を知り得たガセーは、BeOSの良さをアピールすべくアップルに働きかけ、当時のアップル[CEOの](https://ja.wikipedia.org/wiki/最高経営責任者 "wikilink")[ギル・アメリオ](https://ja.wikipedia.org/wiki/ギル・アメリオ "wikilink")らに簡単な[デモを行った](https://ja.wikipedia.org/wiki/プレゼンテーション "wikilink")。ガセーはアメリオに買収に関する条件に付いて提示をしたが、アップルの見積ではBeOSの価値は5000万ドルであったのに対しガセーは3億ドルと法外に高額な金額を提示した\[2\]。当時、BeOSは6年かかっても未完成であり、完全な商用製品と呼べるシステムには至っておらず、更にMacに搭載した場合のコストとBeOS自体の開発費用等を含めるととてつもない金額となり、その上に急を要する次世代Mac用のOS開発に膨大な時間がかかる事が分かる。また[ギル・アメリオ](https://ja.wikipedia.org/wiki/ギル・アメリオ "wikilink")の腹心だった[エレン・ハンコック](https://ja.wikipedia.org/wiki/エレン・ハンコック "wikilink")が[IBM](../Page/IBM.md "wikilink")にソフトウェア担当上級副社長として勤めていた際に技術オンチだった幹部陣が[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")や[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")にいいようににしてやられる様を見てきたため、結論を急ぎ過ぎないよう進言した。

結果として、アップルは[NeXT](../Page/NeXT.md "wikilink")ソフトウェアの[OPENSTEP](https://ja.wikipedia.org/wiki/OPENSTEP "wikilink")を選択し、[スティーブ・ジョブズ](https://ja.wikipedia.org/wiki/スティーブ・ジョブズ "wikilink")率いるNeXTを買収する。金額的にはBeよりも高くはなったが、OPENSTEPは[金融機関](https://ja.wikipedia.org/wiki/金融機関 "wikilink")や研究機関などで既に実績を上げていた。

アップルへの売却に失敗したBe（ガセー）は徐々に業績が下がっていった。さらに、アップルがPower Macintosh G3以降のマシンの技術資料の公開を拒んだため、技術的にもMac[プラットフォーム上でのBeOSの発展は困難となったとし](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")、BeOSがG3以降の機種に対応することはなかった。これについては、Power Macintosh G3の仕様は[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")準拠であり公開されていたも同然であり、PowerPC用[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")等複数のOSがPower Mac G4以降でも動作していることから、単にMacに見切りをつけるための口実であったとも言われている。

そこで[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")等の協力を得て[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で作動するBeOSの開発に専念する事になった。

### Intelプラットフォームでの展開

このような状況で、BeOSはインテル ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) プラットフォームへ進出し、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にはBeOS Release 3 (R3) としてx86・Power Mac・BeBox対応でリリースされた。これによりBeOSはPCユーザーからも注目を集めることとなる。しかし、R3時点ではx86プラットフォームのハードウェアサポート（[チップセット](https://ja.wikipedia.org/wiki/チップセット "wikilink")・[ビデオ](../Page/ビデオ.md "wikilink")・[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")・[ネットワークなど](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")）はきわめて限定されており、BeOS専用にハードウェアを選択しなければ満足に動かすのは難しいほどであった。また、付属の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")NetPositiveは日本語の[エンコーディング](https://ja.wikipedia.org/wiki/エンコーディング "wikilink")に対応していたものの、日本語の[フォント](https://ja.wikipedia.org/wiki/フォント "wikilink")や[インプットメソッド](https://ja.wikipedia.org/wiki/インプットメソッド "wikilink")は付属しなかったため、日本のユーザーにとってはハードルが高かった。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")暮れにはRelease 4 (R4) がリリースされた。このリリースからは日本語のフォントやインプットメソッド(エルゴソフトの[EGBRIDGE](https://ja.wikipedia.org/wiki/EGBRIDGE "wikilink") ベース\[3\])も付属した。一方で、x86 の標準のコンパイラが[CodeWarrior](https://ja.wikipedia.org/wiki/CodeWarrior "wikilink")から[GCCに変更されたため](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")[バイナリフォーマット](https://ja.wikipedia.org/wiki/バイナリフォーマット "wikilink")が[PEから](https://ja.wikipedia.org/wiki/Portable_Executable "wikilink")[ELFに変わり](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、R3 x86の[バイナリ](https://ja.wikipedia.org/wiki/バイナリ "wikilink")は動かなくなった。このころは[Microsoft Windowsに代わる代替OSを求める動きが盛んになってきたころで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、BeOSもその波に乗って一定のユーザーを獲得した。日本では[日立製作所](https://ja.wikipedia.org/wiki/日立製作所 "wikilink")から[プレインストール](https://ja.wikipedia.org/wiki/プレインストール "wikilink")PC（[Windows 98との](https://ja.wikipedia.org/wiki/Microsoft_Windows_98 "wikilink")[デュアルブート](https://ja.wikipedia.org/wiki/デュアルブート "wikilink")）も発売された\[4\]。

翌年にはRelease 4.5（R4.5、コードネームGenki）がリリースされ、[PCカード](https://ja.wikipedia.org/wiki/PCカード "wikilink")サポートなどが追加された。

### フォーカスシフトとBeOSの終焉

[2000年](../Page/2000年.md "wikilink")にBeOSの第三の転機が訪れる。BeOS Release 5（R5、コードネームMaui）は、従来の個人ユーザー中心のパッケージ販売から、以下のような提供形態に切り替えることが発表された。

  - BeIA（コードネームStinger） - [インターネットアプライアンス](https://ja.wikipedia.org/wiki/インターネットアプライアンス "wikilink")（IA）向けのOEM供給。ビジネス的にはこれを主力とする。
  - BeOS Personal Edition (PE) - 個人非商用向け無料バージョン。[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")配布され、Windows上で[FAT](https://ja.wikipedia.org/wiki/File_Allocation_Table "wikilink")[パーティション](https://ja.wikipedia.org/wiki/パーティション "wikilink")内に[インストール](https://ja.wikipedia.org/wiki/インストール "wikilink")することができる（実際の動作は通常通り独立したOSとして動作する）。
  - BeOS Pro Edition - 従来のパッケージ販売の後継。PCで本格的に利用するユーザー向け。

これは、業績が芳しくない個人向け市場から、当時注目を集めていたIA市場へとシフトしたもので、米ソニーのIA「eVilla」などに採用された。また、無料でインストールも簡単なPEの存在も目を引いた。

しかし、IA市場そのものがそれほど発展しなかったこともあり、ビジネス的には苦しい状況が続いた。開発中のR5.1（コードネームDano）は日の目を見ることなく、[2001年](../Page/2001年.md "wikilink")にBe社の[知的資産](https://ja.wikipedia.org/wiki/知的資産 "wikilink")は[パーム](https://ja.wikipedia.org/wiki/パーム_\(企業\) "wikilink")（旧PalmSource、現[ACCESS Systems](https://ja.wikipedia.org/wiki/ACCESS_Systems "wikilink")）に売却され、Be社は解散した。これにより、Be社によるBeOSの歴史は終わりを告げた。

このように、BeOS の歩みはハードウェアを転々としてきた歴史でもある。これについても、BeOSの移植性の高さの賜物として肯定的にとらえる意見と、ユーザーを切り捨ててきた歴史として批判する意見とがある。

## BeOSと日本語

また、日本語関係のお遊びも盛り込まれていた。

  - NetPositiveでは日本語のエンコーディングがサポートされていた（非西洋圏の言語では唯一）。
  - R4以降、日本語のフォントとインプットメソッドが付属した（同上）。
  - BeBoxのカスタムI/OプロセッサはKasumiと呼ばれていた。これは『[らんま1/2](https://ja.wikipedia.org/wiki/らんま1/2 "wikilink")』の女性キャラクター・天道かすみにちなんだものといわれている。
  - NetPositiveの[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")は、英語による[俳句](https://ja.wikipedia.org/wiki/俳句 "wikilink")形式になっていた（BeOS後継プロジェクトの一つHaiku OSのネーミングは、これにちなんだものと思われる）。ただし、これはわかりづらかったため、後のバージョンでは通常の形式も選べるようになった。
  - R4.5のコードネームはGenki（元気）であった。

## 最近の動向

多くの人々に愛されたBeOSであり、[2002年](../Page/2002年.md "wikilink")以降、いくつかの[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトがBeOSを再構築するために動いている。BeOS 5をベースに[プロプライエタリなコードを排除すべく書き直され](https://ja.wikipedia.org/wiki/プロプライエタリ・ソフトウェア "wikilink")、機能が増強されている。BeOSのマイクロカーネルの仕組みがこの作業を簡単にした。

### ZETA

[ZETA](https://ja.wikipedia.org/wiki/ZETA "wikilink")は、[yellowTAB社がPalm社から](https://ja.wikipedia.org/wiki/:en:yellowTAB "wikilink")[ライセンス](https://ja.wikipedia.org/wiki/ライセンス "wikilink")を得て開発していた商用のBeOS後継OSである。yellowTAB社が[破産](https://ja.wikipedia.org/wiki/破産 "wikilink")したため、[magnussoft社支援のもと元CEOだったBernd](https://ja.wikipedia.org/wiki/:en:magnussoft "wikilink") Korzが中心となったチームで ZETA 開発が継続され、製品の販売は独magnussoft社に引き継がれた。しかし[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")に販売不振により支援打ち切りが決まり、開発終了および販売停止となった。

  - [2003年](../Page/2003年.md "wikilink") - yellowTAB社が Palm社からライセンスを得てBeOSの後継 OS ZETA を開発中。
  - [2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink") - yellowTAB社が ZETA の RC 版を発売。一家の中では複数の PC にインストール可能なファミリーライセンス形式を採用。この Zeta Neo は BeOS の後継として徐々に認知されつつある。
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")6月9日 - yellowTAB社がZETA 1.0を発表。
  - 2005年7月1日 - Berry Japan社がyellowTAB社と総代理店契約締結。ZETA の日本公式サイトを開設。
  - 2005年7月7日 - Berry Japan社が、ZETA 1.0 Multilingual Deluxe Version（15,800円）を販売開始。[セブン-イレブン](https://ja.wikipedia.org/wiki/セブン-イレブン "wikilink")経営の7dream.comでも販売。
  - 2005年 8月5日 -「ZETA 1.0 Deluxe Edition」が[秋葉原](https://ja.wikipedia.org/wiki/秋葉原 "wikilink")のショップに初登場。[ぷらっとホーム](https://ja.wikipedia.org/wiki/ぷらっとホーム "wikilink")が、ZETA 1.0 Multilingual Deluxe Versionを販売開始。
  - 2005年 10月15日 - yellowTAB社が「ZETA 1.1」をリリース、既存ユーザ向けアップデータを無料ダウンロードとして配布開始。
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink") 1月21日 - 長期間にわたるBerry Japan社の契約違反のため、yellowTAB社がBerry Japan社との日本総[代理店](https://ja.wikipedia.org/wiki/代理店 "wikilink")契約を破棄。
  - 2006年 4月4日 - ZETA 開発元 yellowTAB社が破産保護下に置かれる\[5\]\[6\]。
  - 2006年 10月14日 - 元CEOだったBernd Korzが中心となったチームでZETAが開発され、製品の販売は独magnussoft社が引き継ぐ。
  - [2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink") 　magnussoft社は販売不振に伴いZETAの開発支援打ち切り決定し、Bernd Korzも開発終了を発表\[7\]、販売も2007年度で終了する。

### Haiku プロジェクト

[Haiku プロジェクトは](https://ja.wikipedia.org/wiki/Haiku_\(オペレーティングシステム\) "wikilink")、オープンソース版 BeOS を目指して、Be 社解散後に発足した。当初のプロジェクト名は OpenBeOS と称しており、2004 年にコミュニティの投票によって選ばれた新しいプロジェクト名として Haiku と改名された。Haiku プロジェクトの第一目標は、BeOS と[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")（ソース / バイナリ共）を持つHaiku R1 (RはReleaseの頭文字) をリリースすることであり、R1 以降は、Haiku に新しい技術やアイディアを採り入れた最適な[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink") OS プラットフォームに発展させていくことを長期的な目標として掲げている。Haiku は x86 と PowerPC コンピュータを対象に開発が進められている。[Haiku のスクリーンショット集](https://www.haiku-os.org/slideshows/haiku-1)

  - [2001年](../Page/2001年.md "wikilink") 8月 OpenBeOS プロジェクト発足。
  - [2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink") 6月 第1回「WalterCon 2004」開催、新プロジェクト名「Haiku」が発表される。
  - 2004年 10月 CannaIM for BeOS が Haiku に寄付される。
  - [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink") 7月 日本語フォント「[小夏](http://www.masuseki.com/index.php?u=be/konatu.htm)」を標準フォントとして適用。
  - 2005年 8月 「WalterCon 2005」開催。
  - 2009年9月14日 初公式リリース Haiku R1/Alpha 1 が公開される [公式サイトでの発表](http://www.haiku-os.org/news/2009-09-13_haiku_project_announces_availability_haiku_r1alpha_1)、[sourceforge.jp](http://sourceforge.jp/magazine/09/09/14/0439229)、[BeOS互換OS「Haiku」の初となる公式開発版「Haiku R1/Alpha」を試す](http://sourceforge.jp/magazine/09/09/26/0812219/2)
  - 2010年5月9日 Haiku R1/Alpha 2 が公開される。
  - 2011年6月18日 Haiku R1/Alpha 3 が公開される。
  - 2012年11月12日 Haiku R1/Alpha 4 が公開される。
  - 2012年11月14日 Haiku R1/Alpha 4.1 が公開される。
  - 2018年9月28日 Haiku R1/Beta 1 が公開される。

## 脚注

## 外部リンク

  - 日本のユーザグループ(閉鎖): [日本 BeOS ネットワーク](http://www.jpbe.net/)

### 後継OS

  - [beunited.org](http://www.beunited.org/) - Be互換OSへのリンクと関連ニュース
  - [B.E.O.S](http://www.blueeyedos.com/) - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")カーネルベース、2003年以降開発が停止している

#### Haiku関連

  - [Haikuプロジェクト公式サイト](http://www.haiku-os.org) (英語)
  - [日本ユーザグループJPBE.netからのHaiku関連ニュース](http://web.archive.org/web/20071012170854/http://jpbe.net/news/archives/cat_haiku_os_openbeos.html) - 閉鎖。（2007年10月12日時点の[アーカイブ](https://ja.wikipedia.org/wiki/インターネットアーカイブ "wikilink")）

#### ZETA関連

  - ZETAの公式ホームページ(http://www.zeta-os.com/ zeta-os.com 消滅)
  - [yellowTAB社](http://www.yellowtab.com/) - ZETAの旧開発元
  - [Zeta 1.0の発表](http://www.yellowtab.com/news/article.php?id=130) - yellowTAB社ウェブサイト内の記事
  - [「BeOS」の後継OS「ZETA 1.0 Deluxe Edition」が秋葉原のショップに初登場](http://akiba.ascii24.com/akiba/news/2005/08/05/657395-000.html) - ニュースサイト内の記事

[Category:BeOS](https://ja.wikipedia.org/wiki/Category:BeOS "wikilink") [Category:PowerPCオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:PowerPCオペレーティングシステム "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink")

1.  [PCの技術で完璧な「専用機」を作る (1/3)](http://www.itmedia.co.jp/lifestyle/articles/0408/23/news005.html)
2.  参考　『アップル薄氷の500日』　1998年8月15日
3.  [BeOS Release 4に標準添付「EGBRIDGE」のエンジンや辞書をもとに開発 エルゴソフト、BeOSに標準添付される日本語入力システムを開発](http://pc.watch.impress.co.jp/docs/article/980528/ergo.htm) 1998年5月28日
4.
5.  [yellowTAB 社発表](http://yellowtab.com/news/article.php?id=192)
6.  [MYCOM PC WEB 関連記事](http://pcweb.mycom.co.jp/news/2006/04/17/004.html)
7.  [「ついにBeOS後継「Zeta」の開発が終了」](https://news.mynavi.jp/news/2007/04/03/006/) マイコミジャーナル 2007年4月3日