> この記事は[ITRON](https://ja.wikipedia.org/wiki/ITRON)から翻訳されています。


**ITRON**（アイトロン、**Industrial TRON**）は、[TRONプロジェクト](../Page/TRONプロジェクト.md "wikilink")が策定・維持している[組み込みOS](../Page/組み込みオペレーティングシステム.md "wikilink")・[リアルタイムOSカーネルの仕様である](../Page/リアルタイムオペレーティングシステム.md "wikilink")。

仕様に準拠した実装を指して、ITRON OS等と呼ぶ場合もある。

トロンフォーラムが組込み総合技術展（主催:一般社団法人組込みシステム技術協会）で毎年実施している、「組込みシステムにおけるリアルタイムOSの利用動向に関するアンケート調査」によれば、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では長年組み込みOSのトップシェアを占めており、業界標準のOSとして採用されている。例えば2016年度の調査では、組み込み系において（ITORNやT-Kernelなどを含む）TRON系OSのシェアが全体の約6割を占めたが、（μITRONを含む）ITRON系OSのシェアだけで全体の43%に達し、TRONに続くシェア2位となった（POSIXを含む）UNIX系OSの20%を引き離している\[1\]。

なお、海外では2010年代の時点では[Android](https://ja.wikipedia.org/wiki/Android "wikilink")や[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")などの[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")系OSが組み込み用としては圧倒的で、ITRONやT-Kernelなどを含むTRON系OSは全く使われておらず、海外でも販売されている日本製家電製品やトヨタ自動車の車載用OSとして使われて来たという歴史的事実のみ知られている（[:en:Usage_share_of_operating_systems](https://ja.wikipedia.org/wiki/:en:Usage_share_of_operating_systems "wikilink")および[:en:ITRON projectを参照](https://ja.wikipedia.org/wiki/:en:ITRON_project "wikilink")）。

海外ではあまり知名度がないが、日本製家電に搭載されて世界に輸出されているため、OSのシェア自体は高い。2003年の時点でOSのシェアが世界1位とされた\[2\]。ライセンスが緩く、無料だったので、Linuxが普及する2000年代以前はアジアでもかなり使われていた。

## μITRON

極めて性能の低いシステムから、大規模なシステムにまで対応できることから、組み込み系OSで大きなシェアを占めるITRONのサブセット。μITRON3以降はITRONと言うとμITRONのことを指す。

## 歴史

TRONプロジェクトにおいて、インフラとなるシステムとして最初に設計が開始され、情報処理学会の第29回全国大会で基本設計の概要を発表している。

  - 1984年頃　TRONプロジェクトのサブプロジェクトとしてITRONの開発開始。

<!-- end list -->

  - 1987年　ITRON1の仕様が公開。

<!-- end list -->

  - 1989年　ITRONのバージョン2となるITRON2、およびそのサブセットとなるμITRON2の仕様が公開。
      - ITRON2では、32bitの大規模なシステム向けに策定されたITRONと、8～16bitの小規模な[ワンチップマイコン等を対象としたサブセット的な仕様である](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")とに分けて公開された（このため、μITRONにはバージョン1は存在せず、最初のバージョンがμITRON2.0である）。このうちμITRON2は、非常に性能の低いMCUでも利用できたことから、組み込み向けで主要なMCUのほぼすべてで採用されるほど極めて広範囲に使われ、32bitの大規模システムにまでμITRONが採用されることとなったため、それらの事例のフィードバックから、μITRON3では8-32bitまでに対応できるスケーラビリティを持った仕様が策定されることとなった。

<!-- end list -->

  - 1993年　μITRON3の仕様が公開。
      - μITRON3ではシステムコールのレベル分けによって、一つの仕様で小規模システムから大規模システムまでをカバーしている。ITRON2のフルセットにほぼ相当する機能を定めている。

<!-- end list -->

  - 1996年頃　ITRONサブプロジェクトの第2フェーズが開始。
      - この頃より組み込みシステムが急速に大規模化・複雑化していったため、アプリケーションの移植性を高めるための要望が高まった。また、組み込み向けシステムが高性能化し、ITRON仕様の策定時点ではオーバヘッドが大きすぎるために見送られた機能でも入れられるようになった。μITRON4の仕様書で紹介されているTRON協会のアンケートでは、当時の現場では「OSの使用リソースが大きすぎる」という悩みよりも「技術者が使いこなせない」「仕様の違いが大きく切り替えの負担が大きい」といった悩みの方が大きかったという。

<!-- end list -->

  - 1999年　μITRON4の仕様が公開。
      - 従来のITRONでは性能の低いCPUでも利用できるように「弱い標準化」の思想だったが、ITRON上でのミドルウェアの利用が広まるとともに、ソフトウェアの移植性を高める「強い標準化」の要望が出てきたことから、仕様の互換性や厳密性が高められた。

<!-- end list -->

  - 2000年　T-Engineプロジェクト開始。
      - ITRONの標準化を進め、「より強い標準化」を志向した次世代リアルタイムOSであるT-Kernelプロジェクトが開始された。

### 現状

2016年現在のμITRON仕様の最新は、1999年公開のμITRON4仕様で、μITRON4仕様の最新は、2006年12月公開の4.03.03である。仕様書では、μITRONからT-Kernelへの移行がスムーズに果たせるような仕様を今後策定したいという予定が語られている。

坂村曰く、μITRONは2000年の時点ですでに「成熟した技術」とのこと。[ユビキタス・コンピューティング](https://ja.wikipedia.org/wiki/ユビキタス・コンピューティング "wikilink")時代にはITRONプロジェクトよりもT-Kernelプロジェクトに注力すべきとの立場で、従来μITRONが得意とした小規模システム向けにもμT-Kernelが用意され、[IoT](https://ja.wikipedia.org/wiki/IoT "wikilink")時代に向けたμT-Kernel 2.0も用意されている。

T-Kernelは高度な情報処理を必要とする組み込み系システムで主に採用されているが、それほどでもないシステムでは依然としてμITRONが使われている。

## 主要な実装

[Toyota_Land_Cruiser_Prado_120_003.JPG](https://ja.wikipedia.org/wiki/File:Toyota_Land_Cruiser_Prado_120_003.JPG "fig:Toyota_Land_Cruiser_Prado_120_003.JPG")(2005年)\[3\]\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:Nintendo_Switch_Console.png "wikilink")(2017年)\[4\]\]\] 組み込み用として、一般消費者の身近にはない機器や、エアコン・電子レンジ・炊飯器・テレビやゲーム機のリモコンなど、身近ではあっても見えないところのOSとして採用されている。テレビ録画サーバーや自動車と言った高度な機器にも採用されており、これらの機器ではシステム全体を制御する高度なOSの下に、複数のMCUとそれらを制御する複数のOSが搭載されている場合があるので、メインOSとしてはLinuxやWindows Embeddedを採用していても、録画サーバーのメディア書き込み用MCUや自動車のエンジン制御用MCUなどその下の見えないところではμITRONが稼働している場合がある。

一般消費者の見えるところのOSとしては、特に2000年代前半から後半にかけて日本だけで普及していた高機能携帯電話（[ガラケー](https://ja.wikipedia.org/wiki/ガラケー "wikilink")）のOSとして使われていたのが有名で、特に[第2世代移動通信システム](https://ja.wikipedia.org/wiki/第2世代移動通信システム "wikilink")（2G）用携帯電話が主流の中に[第3世代移動通信システム](https://ja.wikipedia.org/wiki/第3世代移動通信システム "wikilink")（3G）用携帯電話が登場する2000年代前半の時点ではシェアをほぼ独占していたが、ITRONを各社で各携帯電話ごとにカスタマイズして使っていたため、ソフトウェア規模が大きくなる3G携帯ではOSのカスタマイズ費用や手間が大きすぎることが問題となった\[5\]。そのため、例えば[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")は2003年に、[FOMA](../Page/FOMA.md "wikilink")では[Symbian OSとLinuxが推奨されることを明言するなど](https://ja.wikipedia.org/wiki/Symbian_OS "wikilink")、3Gではガラケーにおいても汎用性のあるOSが使われるようになったため、ITRONのシェアは次第に少なくなった。メインOSとして使用されなくなった後も、カメラ制御用などとしてSH-MobileなどのMCUとともに搭載されていたが、2017年のガラケー生産終了とともにシェアは0%となり全てAndroidに移行する（予定）。

カメラ付きスマホの普及前となる2000年代において多くの人がガラケーと同時に所有していた、[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")のカメラ制御用OSとしての採用例も多く、その点でも2000年代当時はITRONを採用した多くの製品が一般消費者の文字通り「手の中」に存在した。2010年代でも[EXILIM](https://ja.wikipedia.org/wiki/EXILIM "wikilink")などがITRONを採用している。

ITRONによって、2000年代の日本では動画処理やネット通信をリアルタイムで並列的に制御するような高機能な携帯機器が存在しえたが、一方で技術者の負担が非常に大きく、実際はこのような高機能な機器にITRONを使うことは推奨されない。トロンフォーラムではT-Kernelを推奨しており、実際に同時期の一般消費者向け組み込み機器でも2005年ローンチのゲーム機[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")（2012年の[Wii Uでも採用](https://ja.wikipedia.org/wiki/Wii_U "wikilink")\[6\]）や[セイコーエプソン](https://ja.wikipedia.org/wiki/セイコーエプソン "wikilink")のプリンター[カラリオ](https://ja.wikipedia.org/wiki/カラリオ "wikilink")ではT-Kernelの実装eCROSをOSとして採用していた。

  - 富士通 FRシリーズ
      - FR
          - [Milbeaut](https://ja.wikipedia.org/wiki/Milbeaut "wikilink")（ミルビュー） - デジカメ用の画像処理エンジン。そのモバイル版である[Milbeaut Mobileは](https://ja.wikipedia.org/wiki/Milbeaut_Mobile "wikilink")、2000年代前半に日本で普及したカメラ付き高機能携帯電話の多くに採用されていた。
      - FR-V
          - [EXPEED](https://ja.wikipedia.org/wiki/EXPEED "wikilink")（エクスピード） - ニコンのデジカメに搭載された画像処理エンジン。

<!-- end list -->

  - 日立(後のルネサス) [SuperH](https://ja.wikipedia.org/wiki/SuperH "wikilink")シリーズ
      - SH-Mobile3 - 2004年発売。2000年代中頃に日本で発売された高機能携帯電話の多くでメインCPUとして採用。これによって携帯電話でビデオメールやテレビ電話などの動画処理が可能となった。
          - HI7000/4 - SuperHシリーズ向けμITRON4.0の実装

## 発展

### T-Kernel

[T-Engine](https://ja.wikipedia.org/wiki/T-Engine "wikilink")フォーラムによる[T-Kernel](https://ja.wikipedia.org/wiki/T-Kernel "wikilink")はμITRON3.0仕様の発展版である。

ITRONでは「弱い標準化」の思想から、極めて性能の低いシステム（安価で大量に製造される組み込み系システム）から大規模な組み込みシステムにも対応できる柔軟性を持ったシステムであったが、そのぶん実装がハードウェアに依存する部分が大きく、システム自体のコストよりも技術者の教育や開発にかかる人的コストが相対的に重視される大規模な組み込みシステムでは「ソフトウェアの移植性が低い」「ミドルウェアの導入ができない」「技術者の負担が大きい」といった問題があった。

その反省から、T-Kernelは「より強い標準化」の思想でITRONの標準化を進め、互換性や移植性を高めることでミドルウェアの流通を推進し、大規模組み込みシステムにおける開発の効率を高めることを目的としている。

### TOPPERS

[TOPPERS](https://ja.wikipedia.org/wiki/TOPPERS "wikilink")はITRONの主要な実装のひとつで、[TOPPERS/JSPカーネル](https://ja.wikipedia.org/wiki/TOPPERS/JSPカーネル "wikilink")は[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様4.03に基づいている。TOPPERS新世代カーネルは、ITRON仕様に必ずしも準拠させないとしているが、ITRONベースである。

## 脚注

### 文献

  - μITRON 4.0仕様 等 <http://www.t-engine.org/ja/specifications#d>
  - μITRON4.0標準ガイドブック <http://www.personal-media.co.jp/book/tron/191.html>

### 出典

<references />

## 関連項目

  - [はやぶさ (探査機)](../Page/はやぶさ_\(探査機\).md "wikilink")

[Category:TRONプロジェクト](https://ja.wikipedia.org/wiki/Category:TRONプロジェクト "wikilink") [Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:組み込みOSの製品](https://ja.wikipedia.org/wiki/Category:組み込みOSの製品 "wikilink")

1.  [TEP160405_u01.pdf](http://www.tron.org/ja/wp-content/uploads/sites/2/2016/04/TEP160405_u01.pdf)トロンフォーラム
2.  [The Most Popular Operating System in the World | Software | LinuxInsider](http://www.linuxinsider.com/story/31855.html)
3.  [TRON PROJECT 30th Anniversary](http://30th.tron.org/products.html)
4.  [「Nintendo Switch」がμITRON4.0仕様準拠リアルタイムOSを採用 - MONOist（モノイスト）](http://monoist.atmarkit.co.jp/mn/articles/1707/07/news029.html)
5.  [Mobile：ドコモ、FOMA向けLinuxの仕様を確定](http://www.itmedia.co.jp/mobile/0312/03/n_linux.html) ITmedia
6.  [任天堂のゲーム機 「Wii U」 にイーソルの FAT ファイルシステムが採用 | ニュースリリース | eSOL - イーソル株式会社](http://www.esol.co.jp/news/news_12.html)