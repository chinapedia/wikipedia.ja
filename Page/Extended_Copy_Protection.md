> この記事は[Extended Copy Protection](https://ja.wikipedia.org/wiki/Extended_Copy_Protection)から翻訳されています。


**XCP**（）とは、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の First 4 Internet社によって開発された[コンピュータソフトウェア](https://ja.wikipedia.org/wiki/コンピュータソフトウェア "wikilink")パッケージで、[コンパクトディスク](../Page/コンパクトディスク.md "wikilink")の[コピーガード](../Page/コピーガード.md "wikilink")及び[デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink") (DRM) 方式として販売されているものである。これは[ソニー・ミュージックエンタテインメント (米国)により販売されたCDの一部で使用されており](../Page/ソニー・ミュージックエンタテインメント_\(米国\).md "wikilink")、[2005年](../Page/2005年.md "wikilink")に起こった[2005年ソニーCDコピーガードスキャンダルの火種となったが](../Page/ソニーBMG製CD_XCP問題.md "wikilink")、この文脈においては**ソニー[ルートキット](../Page/ルートキット.md "wikilink")**としても知られている。

## 概要

[マーク・ルシノビッチ](https://ja.wikipedia.org/wiki/マーク・ルシノビッチ "wikilink")を初めとするコンピュータセキュリティの研究者たちは 、2005年10月、このプログラムが機能的に[ルートキット](../Page/ルートキット.md "wikilink")と同等であると発表した。ルートキットとは、コンピュータ犯罪者がコンピュータシステムでの不正な活動を隠蔽するために使用する[マルウェア](../Page/マルウェア.md "wikilink")である。ルシノビッチが、彼の*[Sysinternals blog](http://www.sysinternals.com/blog/2005/10/sony-rootkits-and-digital-rights.html)*で事実を公表すると、すぐに[マスメディア](../Page/マスメディア.md "wikilink")や他の研究者たちの注目を集めるところとなった。これが知れ渡ると、事態は民事訴訟や犯罪捜査などに発展した。このため[ソニー](../Page/ソニー.md "wikilink")は、直ちにこのコピープロテクションシステムの使用中止に追い込まれた。

ソニーが最終的にXCPシステムが含まれたCDの回収に至るには、著名なコンピュータセキュリティ研究者である[Ed Feltenと](https://ja.wikipedia.org/wiki/:en:Ed_Felten "wikilink")[J. Alex Haldermanによる](https://ja.wikipedia.org/wiki/:en:J._Alex_Halderman "wikilink")、WEBベースの[アンインストーラ](https://ja.wikipedia.org/wiki/アンインストーラ "wikilink")の[詳しい調査があった](http://www.freedom-to-tinker.com/?p=927)。彼らは、問題のソフトウエアを除去するために使われている[ActiveX](../Page/ActiveX.md "wikilink")コンポーネントが、ユーザーをさらにもっと著しいセキュリティのリスクに晒すことを発見した。これには、[インターネット](../Page/インターネット.md "wikilink")上にある任意の[ウェブサイト](../Page/ウェブサイト.md "wikilink")から、任意のコードを実行させられる可能性も含まれていた。

## 解説

このソニーのCDで使われているのは “XCP-Aurora” として販売されているソフトウエアのあるバージョンである。ユーザーが初めてこの種のCDを[Microsoft Windowsシステムで再生しようとした時](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")がユーザーに対して使用許諾に同意するように促した後、プログラムがインストールされる。するとこのプログラムはユーザーのシステムに常駐して、CDドライブに対するすべてのアクセスを横取りする。そうしてXCP-Auroraに含まれるもの以外の、あらゆるメディアプレーヤーやリッピングソフトウエアによるソニーCDの音楽トラックへのアクセスを阻止する。このプログラムを取り除くための明快な方法は用意されていない。このソフトウエアを削除しようとして関連するファイルを手作業で削除すると、プログラムによって改変された[レジストリ](../Page/レジストリ.md "wikilink")の設定のためCDドライブの動作不能という結果を招く。

付属するプレーヤーソフトウエアは音楽を再生することができるが、これ以外の操作は非常に限定されたものだけが許される。たとえば曲をある決まった回数だけ別のCDに焼くとか、それを、ほんの2〜3種類のポータブルプレーヤーのような、特定のサポートされているデバイスにダウンロードするなど。人気の[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")（ソニーの商売敵である[アップルが販売している](../Page/アップル_\(企業\).md "wikilink")）はサポートされていない。

XCP.Sony.RootkitはDRM executableをWindowsサービスとしてインストールするが、"Plug and Play Device Manager" という誤解しやすい名前をこのサービスに与えている。これは一般のユーザーたちに、それが Windowsの一部であると信じさせてたぶらかすために[マルウェア](../Page/マルウェア.md "wikilink")の作者たちに広く使われている手法である。おおよそ1.5秒ごとにこのサービスはマシンの上で実行されているすべてのプロセスに関連するprimary executablesを問い合わせる。この結果ほとんど連続的な読み取り要求がハードディスクドライブに対して生じる。これはドライブの寿命を縮める。

XCP.Sony.RootkitはCD-ROMフィルタドライバをインストールする。このドライバはプロセス、ディレクトリ、レジストリの一覧を要求するコールを、たとえソニーBMGアプリケーションに無関係であったとしても、すべて横取りする。

XCP付属のミュージックプレイヤー (player.exe) 以外のプロセスがCDのオーディオトラックを読もうとすると、このフィルタドライバはランダムな[ノイズ](../Page/ノイズ.md "wikilink")をデータに重畳して返すことにより、音楽を聞くに堪えなくする。この[ルートキット](../Page/ルートキット.md "wikilink")ドライバはどの情報がオペレーティングシステムから見えるかということを、ソニーBMGソフトウエアを隠蔽するために改変する。これが一般にルートキットとして知られている技術である。

さらに、このルートキットはXCP.Sony.Rootkitだけに影響を与えるのではない。これはWindowsオペレーティングシステムにパッチを当てることで、それ自身をユーザーから隠蔽する。これが隠蔽するのは$sys$で始まる名前を持つすべての[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、[プロセス](../Page/プロセス.md "wikilink")および[レジストリ](../Page/レジストリ.md "wikilink")キーである。これはシステムに脆弱性を与える。執筆の時点ですでに[World of Warcraft](../Page/World_of_Warcraft.md "wikilink") [RING0ハックを隠すために悪用されている](https://ja.wikipedia.org/wiki/:en:Kernel_mode "wikilink")。また、ひとたび改変されたシステムに入り込まれてしまえば、攻撃者のファイルやプロセスを隠蔽することのできる可能性を持っている。

このパッチは`$sys$`で始まる名前を持つプロセス、レジストリのエントリ、ファイルなどの表示も停止させる。"Plug and Play Device Manager" などのこれ以外のXCPコンポーネントは、コンピュータ上で実行されている他のすべてのプロセスを常時監視する。

## セキュリティの調査

短期間のうちにXCPは広く知れ渡ることとなり、セキュリティの研究者たちは調査と、調査結果の発表を急がなくてはならなかった。発見の多くはソニーとFirst 4 Internetの製品の高い危険性を示すものであった。具体的には、このソフトウエアはその活動を[ルートキット](../Page/ルートキット.md "wikilink")（コンピューター犯罪者がその証拠を隠蔽するための汎用ツールキット）の手法で隠蔽する。そのうえユーザーを[ウイルス](../Page/ウイルス.md "wikilink")や[トロイの木馬による追い討ちの被害にあう危険にさらすことがわかった](../Page/トロイの木馬_\(ソフトウェア\).md "wikilink")。

XCPの隠蔽手法（すべての`$sys$`で始まる名前を持つプロセスを不可視にする）は、これ以外の[マルウェア](../Page/マルウェア.md "wikilink")が便乗して不可視になることができ、それらの[マルウェア](../Page/マルウェア.md "wikilink")も等しくユーザーの目から隠蔽してしまう。アンチ・ウイルス会社[BitDefender](../Page/BitDefender.md "wikilink")の報告によると、この手法を用いた最初の悪意あるトロイの木馬は 2005年11月10日にインターネット上で発見されている[1](http://news.bitdefender.com/NW193-en--First-Trojan-Using-Sony-DRM-Detected.html)。

[Edward Feltenと](https://ja.wikipedia.org/wiki/:en:Edward_Felten "wikilink")[Alex Haldermanは追跡調査により](https://ja.wikipedia.org/wiki/:en:J._Alex_Halderman "wikilink")、後にソニーが提供したWEBベースの[アンインストーラそれ自体がさらに重大なセキュリティの問題を抱えていることを明らかにした](../Page/アンインストール.md "wikilink")[2](http://www.freedom-to-tinker.com/?p=928)。このソフトウエアがインストールする[ActiveX](../Page/ActiveX.md "wikilink")コンポーネントは、任意のWEBサイトからユーザーのコンピュータに対してプログラムを制限なしに実行させることを許容する。このコンポーネントはFirst 4 InternetのWEBサイトにおいて、アンインストーラーをダウンロード、実行するために使用されていたが、作業完了後もアクティブなまま---どんなWEBサイトでも訪れたユーザーのコンピュータを乗っ取ることができる状態であった。

XCPはMicrosoft Windowsに特化しているため、[Linux](../Page/Linux.md "wikilink")、[BSD](../Page/BSD.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[SkyOS](https://ja.wikipedia.org/wiki/SkyOS "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のようなこれ以外の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")には影響を与えない。つまり、これらのユーザーはこのソフトウエアの脆弱性の影響をこうむることも、またCDの通常のオーディオトラックからの[リッピング](../Page/リッピング.md "wikilink")（あるいは[コピー](../Page/コピー.md "wikilink")）を妨害されることも無い。しかしながら、少なくとも一部のXCPディスクには、[SunnComm社の](https://ja.wikipedia.org/wiki/:en:SunnComm "wikilink")[MediaMaxというプログラムが含まれているものがあり](https://ja.wikipedia.org/wiki/:en:MediaMax "wikilink")、このプログラムはmacOSにおいて[カーネル](../Page/カーネル.md "wikilink")拡張のインストールを試みる。

## アンチウイルス業界の反応

独立系の研究者が事実を公表すると、セキュリティソフトウエアベンダーはすばやく追従した。`$sys$*`隠蔽コンポーネント削除プログラムの公開と同時にXCPのコンポーネントに関する詳細な解説を公開した。その一方でいまだにCD-ROMフィルタドライバコンポーネントを削除するためのプログラムは公開されていない。アンチスパイウエアプログラムの[PestPatrolのメーカーである](https://ja.wikipedia.org/wiki/:en:PestPatrol "wikilink")[コンピュータ・アソシエイツ](https://ja.wikipedia.org/wiki/コンピュータ・アソシエイツ "wikilink")はXCPソフトウエアをトロイの木馬であり、かつ[ルートキット](../Page/ルートキット.md "wikilink")であると定義した[3](http://www3.ca.com/securityadvisor/pest/pest.aspx?id=453096362)。

[コンピュータ・アソシエイツ](https://ja.wikipedia.org/wiki/コンピュータ・アソシエイツ "wikilink")のアンチスパイウエアプログラムであるPestPatrolは、現在ではこのソニーのソフトウエアを検出して削除するようになった[4](http://www3.ca.com/securityadvisor/pest/pest.aspx?id=453096362)[5](http://blogs.zdnet.com/Spyware/index.php?p=698) 。Microsoft Anti-Malware Engineering Teamは次期[Windows DefenderではソニーXCP製品の隠蔽用コンポーネントを](../Page/Windows_Defender.md "wikilink")[マルウェア](../Page/マルウェア.md "wikilink")として識別して削除するとアナウンスした[6](http://blogs.technet.com/antimalware/archive/2005/11/12/414299.aspx)。

しかし、一部のアンチウイルス会社の幾分のんびりとした、そして不完全な対応について、[Bruce Schneier](https://ja.wikipedia.org/wiki/:en:Bruce_Schneier "wikilink")（Counterpane社の情報保安専門家にしてセキュリティのバイブルともいうべき「[暗号の秘密とウソ](https://ja.wikipedia.org/wiki/暗号の秘密とウソ "wikilink")」の著者）が質問を発している。[ワイアードニューズの記事の中で](../Page/WIRED_\(雑誌\).md "wikilink")、Schneier氏はこう問うている「[マルウェア](../Page/マルウェア.md "wikilink")の作者たちが、[マルウェア](../Page/マルウェア.md "wikilink")から私たちを守るために雇われたその会社と結託したとき、何が起こるのか？」彼の答えは、「Linux を使いなさい。そして自分のしていることをしっかり理解しなさい」である[7](http://wired-vig.wired.com/news/privacy/0,1848,69601,00.html)。

## XCP の衝撃

始まりは、2005年8月の初め、Windowsのユーザーたちがaries.sysと呼ばれるプログラムに関連したクラッシュを報告したことだった[8](http://www.saintsreport.com/forums/printthread.php?s=6d58ebd7f894333e767120b73ed32782&threadid=169497) 。不可解なことに彼らのコンピュータにそのファイルは見つからないのにもかかわらず、である。問題のファイルは現在ではXCPの一部であることがわかっている。TVシリーズ *[Call for Help](https://ja.wikipedia.org/wiki/:en:Call_for_Help_\(TV_series\) "wikilink")* のホスト、[Leo Laporteは](https://ja.wikipedia.org/wiki/:en:Leo_Laporte "wikilink")、CD-ROMドライブ「喪失」の報告の増加を経験したと述べた。これは XCP を削除しようとして失敗したことによる症状である[9](http://www.grc.com/sn/SN-012.htm)。

セキュリティ研究者の[Dan Kaminskyは](https://ja.wikipedia.org/wiki/:en:Dan_Kaminsky "wikilink")、[DNSキャッシュ解析を使って](../Page/Domain_Name_System.md "wikilink")、全世界で568,000のネットワークが、最低でもひとつはXCPに感染したコンピュータを含んでいることを確認した。Kaminskyの方法は、DNSネームサーバが最近のフェッチの結果をキャッシュしていることと、XCP が特定の[ホスト名](../Page/ホスト名.md "wikilink")にあてて「おうちに電話」するという事実を利用している。問題のホスト名をキャッシュしているDNSサーバを見つけることで、Kaminskyは感染したネットワークの数を概算することができる[10](http://www.doxpara.com/?q=sony)。このデータを発表した後Kaminskyは、いまだに総数不明のルートキットを含まない「強化型CD」が同様に、ルートキットに感染したディスクが使っているアドレス宛に「おうちに電話」していることを発見した。したがって、感染率はいまだに活発な調査の対象である。

## XCP の欠点

アナリスト会社の[Gartner](https://ja.wikipedia.org/wiki/Gartner "wikilink")によれば、XCPはDRMのインプリメントにおいて、（現在であれ将来であれ、DRMをスタンドアローンのCDプレイヤーのために作られたオーディオCDに適用しようと試みる）他のすべてのDRM技術と同様の欠点を抱えている。Gartnerによれば、XCPやその他のDRMソフトウエアのインストールは、CDがマルチセッションであることに依存しているため、透明な粘着テープの切れ端をディスク外周の部分に貼り付けて、CDのデータトラックを読み取り不能にしてしまえば、PCにこのディスクを通常のシングルセッションの音楽CDとして扱わせることができる。

## 法的な問題

このソフトウエアが、不正なコンピュータへの干渉を禁じたさまざまな法律や、[スパイウエアがプライバシーの侵害であるとみなす法律などに抵触することに対して](https://ja.wikipedia.org/wiki/スパイウェア "wikilink")、どのような範囲の行動が起こされるのか、そしてどのようにソニーとFirst 4 Internetの法的責任を問うのかなどに関しては推測の域を出ない。イタリアと同様に、カリフォルニア州、ニューヨーク州、テキサス州はすでに二つの会社に対して法的な動きを始めており、さらにもっと多くの集団訴訟が予想される。しかしながら、単にWindowsの改変を確認する、または防止するために、このソフトウエアを調べるか、除去しようと試みる行為が、特定の著作権保護技術の回避を禁じた法律（たとえば、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")で論争が続いている[Digital Millennium Copyright Actのような](../Page/デジタルミレニアム著作権法.md "wikilink")）のもとでは仮説上、民事事件または刑事事件を構成する可能性がある。

[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink")のFred von LohmannはXCPの[使用許諾契約](https://ja.wikipedia.org/wiki/使用許諾契約 "wikilink")（ソフトウエアのインストールに先立ってユーザーの承諾を求めるために表示される）についても、それを「法律学的ルートキット」と呼んで厳しく 批判している[11](http://www.eff.org/deeplinks/archives/004145.php)。

### GPLとLGPLの侵害

研究者の [Sebastian Porst](http://www.the-interweb.com/serendipity/index.php?/archives/55-Proof-that-F4I-violates-the-GPL.html)、[Matti Nikki](http://hack.fi/~muzzy/sony-drm/)と多数のソフトウエア専門家たちは、XCPソフトウエアが[LAME](../Page/LAME.md "wikilink") [mp3](https://ja.wikipedia.org/wiki/mp3 "wikilink") エンコーダー、[mpglib](https://ja.wikipedia.org/wiki/mpglib "wikilink")[12](http://www.the-interweb.com/serendipity/index.php?/archives/54-Breakthrough-after-breakthrough-in-the-F4I-case.html), [FAAC](https://ja.wikipedia.org/wiki/FAAC "wikilink")[13](http://www.the-interweb.com/serendipity/index.php?/archives/56-Two-new-F4I-license-infringements-found.html) [id3lib](https://ja.wikipedia.org/wiki/id3lib "wikilink")[14](http://the-interweb.com/bdump/misc/id3lib.png) （[ID3タグ](../Page/ID3タグ.md "wikilink")読み取りと書き込み）、[mpg123](https://ja.wikipedia.org/wiki/mpg123 "wikilink")および[VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink")\[[http://sam.zoy.org/blog/2005-11-21-suspicious-activity-indeed\]の著作権を侵害している証拠を公開した](http://sam.zoy.org/blog/2005-11-21-suspicious-activity-indeed%5Dの著作権を侵害している証拠を公開した)。

プリンストン大学の研究者である[Alex Halderman](http://www.freedom-to-tinker.com/?p=940)は、ほぼすべてのXCP CDが、[Jon Johansenの](../Page/ヨン・レック・ヨハンセン.md "wikilink")[DRMS](https://ja.wikipedia.org/wiki/DRMS "wikilink")ソフトウエアの改変版を使用したコードを含んでいることを発見した。このコードは[アップルの](../Page/アップル_\(企業\).md "wikilink")[FairPlay](../Page/FairPlay.md "wikilink") DRMを開くことができる。彼は、このコードが起動しないようになっているが完全に機能し、このコードを使って曲にFairPlay DRMを施せることを発見した。DRMSとmpg123は[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) のもとにライセンスされている。そのほかに見つかったソフトウエア、たとえばLAMEは[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) のもとにライセンスされており、しかも[フリーソフトウエア](https://ja.wikipedia.org/wiki/フリーソフトウエア "wikilink")である。もしこれらの主張が正しいとするなら、ソニーBMGは著作権の存在する事物を、著作者の権利を侵害して販売していたことになる。

[Jon Johansenは彼のブログのなかで](../Page/ヨン・レック・ヨハンセン.md "wikilink")、弁護士と話し合った結果、彼は裁判を起こすことはできないと思うと書いている[15](http://nanocrew.net/2006/01/31/sony-bmg-infringement/)。あるいは彼の受けた法律的なアドバイスは間違っているという意見もある[16](http://www.techdirt.com/articles/20060201/0313222_F.shtml)。LAMEの開発者たちはソニーBMGに対してオンラインで公開質問状を出している[17](http://lame.sourceforge.net/open_letter_sony_bmg.html)。

### ソニーが提訴されうる著作権侵害の項目

cf. [18](http://www.anselsbrain.com/?p=25)

  - GPLまたはLGPLソフトウエアへの “prominent notices” の記載が無いこと
  - プログラム中にGPLコードへの静的リンクが含まれるのにGPLに基づくプログラム全体のソースコードの開示がなされていないこと
  - プログラム中にLGPLコードへの静的リンクが含まれるのに該LGPL部のソースコードおよび非LGPL部のバイナリコード開示が無いこと（LGPLコードのアップデートの際に非LGPL部へのリンクを取り直すことができるようにするため）
  - GPL/LGPLが許可する範囲を超えるコードの使用制限を定めたこと、例：GPL/LGPLで定める「サードパーティーへの無償ライセンス供与」に反する規定

ソニーは既にあるバージョンのid3libのソースコードをそのWEBサイトで公開しているが[19](http://www.sony.net/Products/OpenMG/overview/tech.html)、XCP にリンクは張られていない。上の記述が正しいと仮定したとき、ソニーがGPLとLGPLに基づくソースコードの開示を拒絶したならば、誰であれその種のCDを入手した者は、それゆえに完全なソースコードをGPLに基づいて入手する権利を持ち、法的な行動を起こし、それを要求することができる。

## ソニーの反応

ソニーBMGのglobal digital business division社長の[Thomas Hesseは](https://ja.wikipedia.org/wiki/:en:Thomas_Hesse "wikilink")[ナショナル・パブリック・ラジオ](https://ja.wikipedia.org/wiki/ナショナル・パブリック・ラジオ "wikilink")の番組の中でこう語っている。「私が思うに、大部分の人たちは[ルートキット](../Page/ルートキット.md "wikilink")が何であるかさえ知らないだろう。それなのに彼らがそれについて気にするわけは無いだろう？」彼はこう説明している。「このソフトウエアは私たちの[CDを非合法の複製や](../Page/コンパクトディスク.md "wikilink")[リッピング](../Page/リッピング.md "wikilink")から守るために作られている」[20](http://www.npr.org/templates/story/story.php?storyId=4989260)

### 不完全なパッチ

ソニーはさらにこう主張する。「コンポーネントは悪意を持ったものではなく、セキュリティを損なうものでもありません」しかし「プログラムがもたらしている潜在的なセキュリティの脆弱性に関して、ユーザーが抱くかもしれない如何なる懸念も軽減するために、ユーザーがそのコンピュータから[ルートキット](../Page/ルートキット.md "wikilink")コンポーネントを削除できるよう、このアップデートがリリースされました」

ソフトウエアの隠蔽機能を取り除くためのパッチがリリースされたが、このパッチはXCPを完全に除去するものではなく、単にそれ自身を不可視にしている手法を停止させるだけである。[21](http://cp.sonybmg.com/xcp/english/updates.html)

First 4 Internetは、今後の如何なる新しいバージョンのXCPもこの種の技術は使わないと報告している。

### 危険なアンインストーラ

XCP-Auroraのアンインストーラは現在ソニーBMGのWEBサイトから入手できる[22](http://cp.sonybmg.com/xcp/english/updates.html)。このアンインストーラの調査結果が[マーク・ルシノビッチ](https://ja.wikipedia.org/wiki/マーク・ルシノビッチ "wikilink")――XCP の存在を最初に暴露した人物――により「[またもソニー：危険な非隠蔽化パッチ、使用許諾契約と密告電話](http://www.sysinternals.com/blog/2005/11/more-on-sony-dangerous-decloaking.html)」というタイトルで公開されている。アンインストーラを入手するためには、所定のブラウザ（[Microsoft Internet Explorer](../Page/Internet_Explorer.md "wikilink")）を使用することが要求され、オンラインで申込書に電子メールアドレスを記入して、メールを受け取り、パッチをインストールし、第二のオンラインフォームに記入し、それからやっとアンインストーラへのリンクを受け取ることができる。このリンクはパーソナライズされており、一度しかアンインストールすることができない。なおその上に、[ソニーのプライバシーポリシー](http://www.sonybmg.com/privacypolicy.html)は、このアドレスはプロモーションか、提携業者に供与されるか、または「真っ当なサードパーティーがあなたに直接コンタクトする」目的に使われる場合がある、と謳っている。

さらにこのアンインストーラには遠隔コード実行を許す、セキュリティ上の問題が発生しうることが報告されている[23](http://hack.fi/~muzzy/sony-drm/)。ソニーのアンインストールページはInternet Explorerにこのページが表示されるとActiveXコントロールをインストールしようとする。このActiveXコントロールは “Safe for scripting” とマークされている。これはどんなWEBページであれ、このコントロールとそのメソッドを利用できることを意味している。このコントロールにより提供されるメソッドの中には、攻撃者に対して任意のコードのダウンロードと実行を許可してしまうような危険なものも含まれている。

### 広がる波紋と製品の回収

2005年11月11日の時点で、ソニーはXCPシステムを使用した CD の製造を一時的に停止すると発表した[24](http://today.reuters.co.uk/news/newsArticle.aspx?type=technologyNews&storyID=2005-11-11T183106Z_01_MOL166114_RTRIDST_0_TECH-SONY-COPYPROTECTION-DC.XML&archived=False)

これには[アメリカ合衆国国土安全保障省](../Page/アメリカ合衆国国土安全保障省.md "wikilink")のStewart Baker次官補によりコメントがつけられている。この中で次官補はDRM製造業者を非難している。[ワシントンポスト](https://ja.wikipedia.org/wiki/ワシントンポスト "wikilink")紙は以下のように伝えている：

[ニューヨーク・タイムズ](../Page/ニューヨーク・タイムズ.md "wikilink")紙によれば、「このソフトウエアが含まれている CD 約470万枚が出荷されており、210万枚がすでに販売されています」とソニーBMG は語った。おおよそ 50種類の XCP を含むアルバムが Sony-BMG によって販売されている[25](http://www.nytimes.com/2005/11/14/business/14rights.html)[26](http://www.bloomberg.com/apps/news?pid=10000101&sid=aVhY_TwrFjQI&refer=japan)。

2005年11月14日、ソニーは感染しているCDを市場から回収すること、このディスクを購入した顧客に対して代品の提供を計画していることを発表した[27](http://www.usatoday.com/tech/news/computersecurity/2005-11-14-sony-cds_x.htm?csp=34)。

XCPタイトルを持っている消費者がこのCDを返送してDRMがかけられていない、またXCPを含んでいないCDに交換するために、ソニーBMGは無料の[UPS配送サービスを提供している](../Page/ユナイテッド・パーセル・サービス.md "wikilink")[28](http://www.upsrow.com/sonybmg/)。

## XCP が使用されているアルバム

  -
    *すべてのリスト: [:en:List of compact discs sold with XCP](https://ja.wikipedia.org/wiki/:en:List_of_compact_discs_sold_with_XCP "wikilink")*

<!-- end list -->

  -
    ''参照: [CD’s Containing XCP Content Protection Technology](http://cp.sonybmg.com/xcp/english/titles.html)

[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink")は2005年11月9日に、19タイトルを含む独自のリストを公開した[29](http://www.eff.org/deeplinks/archives/004144.php)。2005年11月15日には[ザ・レジスター](https://ja.wikipedia.org/wiki/ザ・レジスター "wikilink")紙がそれが47タイトルにも及ぶかもしれないとする記事を掲げた[30](http://www.theregister.co.uk/2005/11/15/sony_bmg_bodycount/)。ソニーBMGはXCP CDが52種類であると述べた[31](http://cp.sonybmg.com/xcp/english/titles.html)。

[アマゾンはXCP](../Page/Amazon.com.md "wikilink") CDを欠陥商品として扱い、顧客が要求すればいつでも送料無料で払い戻しに応ずると発表した[32](http://www.usatoday.com/tech/news/computersecurity/2005-11-15-sony-qa_x.htm)。

## 関連項目

  - [コピーガード](../Page/コピーガード.md "wikilink")
  - [ソニーBMG製CD XCP問題](../Page/ソニーBMG製CD_XCP問題.md "wikilink")
  - [デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink")
  - [デジタルミレニアム著作権法](../Page/デジタルミレニアム著作権法.md "wikilink")
  - [MagicGate](../Page/MagicGate.md "wikilink")
  - [SonicStage](https://ja.wikipedia.org/wiki/SonicStage "wikilink")

<!-- end list -->

  - [:en:MediaMax](https://ja.wikipedia.org/wiki/:en:MediaMax "wikilink")
  - [:en:OpenMG](https://ja.wikipedia.org/wiki/:en:OpenMG "wikilink"), Sony DRM used by [:en:Sony Connect](https://ja.wikipedia.org/wiki/:en:Sony_Connect "wikilink")
  - [en:StarForce copy protection](https://ja.wikipedia.org/wiki/:en:StarForce "wikilink")

## 参照

  - [ソニーが音楽CDに組み込んだ “Rootkit” とは何者か？](http://www.atmarkit.co.jp/fwin2k/insiderseye/20051109rootkit/rootkit_01.html) （[マーク・ルシノビッチ](https://ja.wikipedia.org/wiki/マーク・ルシノビッチ "wikilink")氏が最初に XCP の存在を暴露したブログ記事の日本語訳）
  - [ソニーCDが明らかにしたセキュリティー業界の本質的問題(上)](http://hotwired.goo.ne.jp/news/culture/story/20051118204.html) （[Bruce Schneierによる日本語版ホットワイアードの記事](https://ja.wikipedia.org/wiki/:en:Bruce_Schneier "wikilink")）
  - [コピープロテクションCDが招く災い](http://pc.watch.impress.co.jp/docs/2005/1115/hot393.htm) （「元麻布春男の週刊PCホットライン」の記事）
  - [続・コピープロテクションCDが招く災い](http://pc.watch.impress.co.jp/docs/2005/1116/hot394.htm) （「元麻布春男の週刊PCホットライン」の記事）
  - [交換に追い込まれたコピープロテクションCD問題](http://pc.watch.impress.co.jp/docs/2005/1121/hot395.htm) （「元麻布春男の週刊PCホットライン」の記事）
  - [BMGの米国内向けCCCDにルートキット](http://slashdot.jp/security/article.pl?sid=05/11/03/0859246&from=rssSony) （[スラッシュドット](../Page/スラッシュドット.md "wikilink")・ジャパンの記事）

## 外部リンク

  - [Sony BMG XCP Help Page](http://cp.sonybmg.com/xcp/)
  - [Bruce Schneier for Wired news on "the real story"](http://wired-vig.wired.com/news/privacy/0,1848,69601,00.html)

[Category:著作権管理技術](https://ja.wikipedia.org/wiki/Category:著作権管理技術 "wikilink") [Category:ソニー](https://ja.wikipedia.org/wiki/Category:ソニー "wikilink") [Category:Windowsのトロイの木馬](https://ja.wikipedia.org/wiki/Category:Windowsのトロイの木馬 "wikilink")