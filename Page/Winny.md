> この記事は[Winny](https://ja.wikipedia.org/wiki/Winny)から翻訳されています。


**Winny**（ウィニー）とは、[Peer to Peer技術を応用した](../Page/Peer_to_Peer.md "wikilink")[ファイル共有ソフト](https://ja.wikipedia.org/wiki/ファイル共有ソフト "wikilink")である。配布者の匿名性を強くアピールしていたため、[著作権侵害](../Page/著作権侵害.md "wikilink")のファイル交換に多用された。

## 概要

Winnyは元[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")大学院情報理工学系研究科助手の[金子勇によって](../Page/金子勇_\(プログラマー\).md "wikilink")2002年に開発が始まった。当時は既に[Napster](../Page/Napster.md "wikilink")やファイルローグなどのP2P型ファイル共有ソフトが存在していたが、多くはハイブリッド型であり、ファイル情報やノード情報を管理する中央サーバーが必要であった。そして、ファイル共有ソフトを用いて不正なファイルが多くやりとりされていたことから、中央サーバーがたびたび著作権法違反で摘発されるという事件が起きていた。一方で、完全なP2Pネットワークとしては既に[Freenet](../Page/Freenet.md "wikilink")が存在したが性能が低く、広く使われるまでには至っていなかった。WinnyはこのFreenetのアイデアを元に実用的で、かつ中央サーバーを必要としない完全なP2Pネットワークを作ることを目的としていた\[1\]。

金子は掲示板サイト[2ちゃんねる](../Page/2ちゃんねる.md "wikilink")の[ダウンロードソフト板](https://ja.wikipedia.org/wiki/ダウンロードソフト板 "wikilink")に匿名で書き込みを行い、ユーザーとやりとりしながら開発を進めた。彼は最初の書き込み番号である「47」を名前として使用していたことから利用者からは「47氏」と呼ばれていた。当時の日本では[WinMX](../Page/WinMX.md "wikilink")がP2Pファイル共有ソフトとして広く使われており、新しい共有ソフトはその後継を目指すという意味合いを込めて、MXの2文字をアルファベット順にそれぞれ1文字ずつ進めたWinNY（後にWinny）がソフトの名前として決まった\[2\]。

[2002年](../Page/2002年.md "wikilink")[5月6日](../Page/5月6日.md "wikilink")にベータ版が公開。以後、金子が[著作権侵害](../Page/著作権侵害.md "wikilink")行為[幇助](../Page/幇助.md "wikilink")の疑いで逮捕されるまで開発が続いた。不正なファイルのやりとりをした使用者ではなく、技術の開発者を逮捕するという事件は世間の耳目を集めたが、後に裁判の結果、無罪が確定している（詳細は[違法性の節を参照](https://ja.wikipedia.org/wiki/#違法性 "wikilink")）。なお、金子による最後のバージョンは逮捕前に公開された「Winny 2.0 Beta7.1」だが、第三者による[クラック版が開発](../Page/クラッキング_\(コンピューター用語\).md "wikilink")・配布されている。金子は無罪が確定後もWinnyの開発に戻ることはなく、2013年に急性心筋梗塞にて死去。開発は事実上終了した。

[ACCSの実態調査](../Page/コンピュータソフトウェア著作権協会.md "wikilink")\[3\]では、2006年6月調査でWinMXを初めて凌駕して国内最多の利用者率（主に利用している人が33.3%）となり、ネットエージェントの報道によると、[2006年](../Page/2006年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")現在のユーザー数は44万人から53万人程度であるという\[4\]。

## 特徴

Winnyは、ファイルの共有に中央[サーバ](../Page/サーバ.md "wikilink")ーを必要としない[ピュアP2P方式で動作する](https://ja.wikipedia.org/wiki/ファイル共有ソフト#ピュアP2Pモデル "wikilink")。それ以前のいわゆる「P2Pファイル交換ソフト」では、各クライアントの情報をサーバーに集積する様式（[ハイブリッドP2Pモデル](https://ja.wikipedia.org/wiki/ファイル共有ソフト#ハイブリッドP2Pモデル "wikilink")）が主流であったため、サーバー非稼動時には利用できないという問題を抱えていた。その意味でWinnyはシステム上の障害に対して非常に強く、一度稼働を始めたネットワークは止められないことが特徴である。Winnyでは中央サーバーの代わりに初期ノードと呼ばれるWinnyユーザーのIPアドレスのリストをWinnyに登録し、接続できたIPアドレスから他のクライアントの情報を交換することでネットワークを構成している。初期ノードの配布は専用のサーバーである必要はなくインターネット上の掲示板などでもよい。

また、Winnyには以下のような機能が備わっている。

  - 通信の暗号化
  - 転送機能
      - [データ](../Page/データ.md "wikilink")を拡散する際に、一定の確率で複数のコンピュータを仲介させるなどして各コンピュータに[キャッシュを残す機能](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。
  - [クラスタ機能](../Page/コンピュータ・クラスター.md "wikilink")
      - 似たような[ファイルを求めている](../Page/ファイル_\(コンピュータ\).md "wikilink")[ノード同士をつなぎやすくするための機能](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")。

このような機能の実装により、高い匿名性、効率のよいファイル共有の2点を高レベルなバランスにおいて実現させた。[匿名](../Page/匿名.md "wikilink")での電子掲示板機能も備えている。

ファイル共有機能ばかりが注目されたが、実際はこの掲示板機能の開発にも重点が置かれていた。電子掲示板機能では、[スレッドを立てた者のコンピュータにスレッドの内容が集約](../Page/スレッドフロート型掲示板.md "wikilink")・保存されるため、スレッド設置者のノードが停止している場合は、読み込みも書き込みも出来ない。なおこの電子掲示板機能は主要な[2ちゃんねるブラウザ](../Page/2ちゃんねるブラウザ.md "wikilink")に似た[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")を備えている。この「スレッド所有者のクライアントに直接アクセスする」という面は、容易にスレッドの所有者の[IPアドレス](../Page/IPアドレス.md "wikilink")を特定でき、構造上Winny本体より匿名性が低い。

### 暗号化通信と匿名性

Winnyが開発された当初は、どのようなファイルがネットワーク上で転送されているかを解析することは困難であると思われていたが、実際は通信の暗号化に使う鍵を平文でやり取りしており、全ての通信を傍受すれば解読できる状態であった。そのため、匿名性を向上させるために、Winnyの暗号化部分に改良を加えた「[Winnyp](https://ja.wikipedia.org/wiki/Winnyp "wikilink")」が匿名の開発者によって公開されている。金子自身は、暗号が解読されてしまったら、すぐに別のアルゴリズムに変えればよいと考えていたようである\[5\]。つまりWinnyのネットワークが成り立つためにはソースコードが非公開であることが大前提となっており、当時海外で普及し始めていた[BitTorrent](../Page/BitTorrent.md "wikilink")が当初からオープンソースである事と比較すると大きな欠点であり、Winnyに将来性がないことは明白であった。

暗号化という点に関しては、WinnyはピュアP2Pという特性上、[暗号鍵の認証局を持つことができない構造になっている](../Page/鍵_\(暗号\).md "wikilink")。

だが、[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")を使わないでいると、第三者のなりすまし攻撃を受ける可能性がある。そのためWinnyでは公開鍵暗号が使われており、同時に固定鍵がWinny内部に内蔵されている。

しかし[デバッガ](../Page/デバッガ.md "wikilink")を使えば、その固定鍵を取り出すことができる。Winnyの暗号は固定鍵の使用と通信文内に、XOR暗号法により暗号化された[RC4](../Page/RC4.md "wikilink")鍵を初期通信時に送っているため、リアルタイムで暗号化解読できるほどの弱さとなっている\[6\]。

これまでにWinnyの使用で逮捕された者たちは全員、何らかの外部要因が突破口になり、逮捕へと至っている。例えば、発信者の特定がたやすい[ウェブページ](../Page/ウェブページ.md "wikilink")や電子掲示板で、Winnyから入手したファイルを販売しようとしたり、Winnyの電子掲示板機能・WinnyBBSにスレッドを立て、違法ファイルを特定できる情報を記載し、実際に[アップロード](../Page/アップロード.md "wikilink")したりするなどである。

開発・配布者自身も、通信やキャッシュを暗号化したのは、プログラムが解析されてクラックが蔓延し、その結果ファイル共有の効率が低下するという事態を防ぐためであり、暗号がすべて解除されたからといって匿名性が失われるわけではないという趣旨の発言をしている\[7\]。

それによると、WinnyはキャッシュとUPフォルダ内のファイルが区別できない形でアップロードされるため、あるファイルを公開する者が一次配布者であるかは特定できないという。 さらに、こちらから見てアップロードしている者が単に他のノードから転送をしているだけである可能性も残されているため、WinnyBBSでスレッドの所有者が放流宣言をするなど確固たる根拠がない限り一次配布者を特定できない。しかし[Nyzilla](https://ja.wikipedia.org/wiki/Nyzilla "wikilink")\[8\]などの解析ソフトを用いて二次配布ノードを特定することができるため、**Winnyの二次配布ノードの匿名性は保証されない。** つまりWinnyの匿名性とは、一時配布者であることを特定しづらくするものであり、Winnyを利用していることや二次配布していることを匿名にするものではない。

また、Winnyネットワークを監視する[クローラ](../Page/クローラ.md "wikilink")などによって時間的・空間的に十分大規模な監視が可能ならば、ネットワーク内に存在するファイルがコピーされ増殖する過程をさかのぼることで、一次配布ノードを特定することができる。

### 解説書

[2005年](../Page/2005年.md "wikilink")1月に、Winny開発・配布者が[アスキー社から](../Page/アスキー_\(企業\).md "wikilink")『Winnyの技術』というWinnyの仕組み等をまとめた書籍を発売すると発表したが、何らかの事情により発売が延期され、2005年10月6日に正式に発売された\[9\]。

この書籍では、これまで非公開としていたWinnyの転送システム等を技術者向けに解説している。この書籍に関してはP2Pファイル共有技術を悪用するためではなく、P2Pファイル共有技術の進化のためにまとめたといわれている。

## 違法性

開発当初、Winnyの匿名性は、[著作権法](../Page/著作権法.md "wikilink")・[わいせつ物頒布罪](https://ja.wikipedia.org/wiki/わいせつ物頒布罪 "wikilink")・[児童ポルノ規制法](../Page/児童買春、児童ポルノに係る行為等の規制及び処罰並びに児童の保護等に関する法律.md "wikilink")・[個人情報保護法](https://ja.wikipedia.org/wiki/個人情報保護法 "wikilink")などに抵触する違法なファイル交換を行う場合に好都合なものであったため、利用者数は急速に拡大していった。

それに乗じて、Winnyで流通するファイルに[Antinny](../Page/Antinny.md "wikilink")などといった[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")が仕組まれるようになり、それによってファイルをダウンロードした者の[個人情報](../Page/個人情報.md "wikilink")がWinnyを媒体としてばらまかれるという問題を引き起こした。このウイルスは亜種も数々出現し、必ずしもWinnyを感染媒体とせず、[インターネット](../Page/インターネット.md "wikilink")でも感染被害が及んだ。

[2003年](../Page/2003年.md "wikilink")に、Winnyの利用者が[著作権](../Page/著作権.md "wikilink")法違反（[公衆送信権](../Page/公衆送信権.md "wikilink")の侵害）容疑で逮捕、起訴され、[2004年](../Page/2004年.md "wikilink")に開発・配布者の金子勇もこの事件の著作権侵害行為を幇助した共犯の容疑を問われ逮捕され、起訴された。ソフトウェアを開発すること自体について、刑事事件として違法性が問われたものと認識され、日本では非常に稀なケースであったが、2011年に開発者の無罪判決が確定した。

金子はWinny使用が著作権侵害に繋がることを認知しており、自身はダウンロード専用の特製Winnyを使用しており、アップロードはしておらず著作権侵害はしていないとされている\[10\]（事件当時は[ダウンロード違法化](https://ja.wikipedia.org/wiki/ダウンロード違法化 "wikilink")前であるため、ダウンロードだけであれば著作権侵害にはならなかった）。

## 情報流出

### 概要

2004年3月ごろより、Winnyを利用していたパソコンがWinnyなどで入手したファイルを閲覧したことにより、[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")の一種ともいえる[ワームに感染する事例が頻発し](../Page/ワーム_\(コンピュータ\).md "wikilink")、その結果、そのパソコン内に保存されていた本来公開されてはならないファイルが、Winnyのネットワーク上に流出するという事件が多発した。

このワームは特に「[暴露ウイルス](../Page/暴露ウイルス.md "wikilink")」と言われ、流出したものとしては、一般企業の業務データ、個人の[チャット](../Page/チャット.md "wikilink")ログや[電子メール](../Page/電子メール.md "wikilink")データ、[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")によって撮影された画像、[違法コピーデータを使用している最中の](../Page/ブートレグ.md "wikilink")[スクリーンショット](https://ja.wikipedia.org/wiki/スクリーンショット "wikilink")、漫画家の下書きの原稿、パスワードを書いたメモなど様々なものがある。

ワームはユーザーの[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")などに存在するデータを勝手に共有し、感染者に気づかぬうちにWinnyのネットワーク上に流出させる。これは特定のフォルダ（「[マイドキュメント](https://ja.wikipedia.org/wiki/Microsoft_Windows#ユーザーインターフェイス "wikilink")」など）や特定の[拡張子](../Page/拡張子.md "wikilink")（[\*.jpgや](../Page/JPEG.md "wikilink")[\*.docなど](../Page/Microsoft_Word.md "wikilink")）を検索して、これらから作成した複製や[書庫ファイルをWinnyのアップロード機能を使って共有ファイルに指定する](https://ja.wikipedia.org/wiki/アーカイブ#コンピュータ用語のアーカイブ "wikilink")。感染者に気付かれ難いこともあり、事件の発覚が遅れ、漏洩した情報回収のめどが立たなくなるケースが跡を絶たない。

初期のワームはデスクトップを[キャプチャしてアップロードする程度の働きしかなかったが](https://ja.wikipedia.org/wiki/ディスプレイ_\(コンピュータ\)#キャプチャ "wikilink")、その後改変が加えられ、デスクトップ上のデータの共有や、電子メール（[Outlook Expressの保存データ](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")）の共有まで行うようになった。

ワームのひとつ[山田オルタナティブ](../Page/山田オルタナティブ.md "wikilink")には、パソコン自体を[HTTPサーバとして立ち上げ](../Page/Hypertext_Transfer_Protocol.md "wikilink")、パソコンに保存されているデータすべてをインターネットを通じて世界中に公開してしまい、なおかつワームに感染した者同士をHTTPリンクで相互接続する機能が付加されている。

### 被害実態

ワームの被害は民間企業や個人だけにとどまらず、[警察](../Page/日本の警察.md "wikilink")、[陸上自衛隊](../Page/陸上自衛隊.md "wikilink")、[海上自衛隊](../Page/海上自衛隊.md "wikilink")、[航空自衛隊](../Page/航空自衛隊.md "wikilink")（のちに[防衛庁](https://ja.wikipedia.org/wiki/防衛庁 "wikilink")はWinny対策の為に、新しく[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")を調達し、40億円の費用を賄うこととなった）、[日本郵政公社](../Page/日本郵政公社.md "wikilink")、[刑務所](https://ja.wikipedia.org/wiki/日本の刑務所 "wikilink")、[裁判所](../Page/日本の裁判所.md "wikilink")、日本の原子力発電関連施設、一部の[地方公共団体](../Page/地方公共団体.md "wikilink")など官公庁でも流出事件が続発し、公務員が機密情報や職務上知りえた[個人情報](../Page/個人情報.md "wikilink")などを自宅に持ち帰り、あまつさえ私物のファイル交換ソフトをインストール・利用中のパソコンに入れていた、官公庁の杜撰な情報管理実態が露わになると伴に、不用意にWinnyを使用しているという実態が暴露され、日本国政府の問題となった。[嫌がらせ](https://ja.wikipedia.org/wiki/嫌がらせ "wikilink")のために、個人情報を盗み出して故意にWinnyに流出させるという手口も発覚した。

また、[ウイルスバスター](../Page/ウイルスバスター.md "wikilink")などの[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")対策ソフトを提供している[トレンドマイクロ](../Page/トレンドマイクロ.md "wikilink")からも、社員がAntinnyに感染しWinnyへ個人情報を流出させる事故を発生し、[住民基本台帳ネットワーク](https://ja.wikipedia.org/wiki/住民基本台帳ネットワーク "wikilink")に関する情報（パスワード・使用手順）も流出していたことが確認された。[北海道警察](../Page/北海道警察.md "wikilink")の事例においては、警察官に個人情報を流出させられたとして個人情報を漏洩された被害者が民事裁判を起こし、実際個人情報を流出させた北海道警察側が一審で敗訴している。

だが、二審、三審の最高裁ではこの感染を予知出来なかったとして原告側が敗訴した。

ひとたびWinnyで流出した情報は、キャッシュを保持するコンピュータが存在する限り、継続的にWinnyのネットワーク上に留まり続けることが分かっており、それらのデータを削除することは、Winny利用者の全端末のデータをすべて削除しない限り、消去は永久に不可能である。

### 対応

これらのワームに対しては、[ウイルス対策ソフト会社側が対策を講じており](../Page/アンチウイルスソフトウェア.md "wikilink")、こういったウイルスに感染する前に検出できる[パターンファイル](https://ja.wikipedia.org/wiki/パターンファイル "wikilink")を更新し、または感染後に駆除を行う[ワクチンツールを配布している](../Page/アンチウイルスソフトウェア.md "wikilink")。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")側でも、2005年10月の[Windows Updateプログラムの中にWinnyのウイルスを駆除できる](../Page/Microsoft_Update.md "wikilink")「[悪意のあるソフトウェアの削除ツール](https://ja.wikipedia.org/wiki/悪意のあるソフトウェアの削除ツール "wikilink")」を同梱した。マイクロソフトは、2005年11月に、1ヶ月間でこのWindows Updateにより20万件以上のウイルス除去に成功したと発表した。しかしながら、上記マイクロソフト配布の削除ツールは、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[2000にしか対応しなかった](../Page/Microsoft_Windows_2000.md "wikilink")。(後に[Windows Vista](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、[Windows 7](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")、[Windows 8](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")、[Windows 10にも対応](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")。)そのため、Windows2000より前の古いバージョンの[Windowsではマイクロソフト製の対策ツールを使用して駆除することは出来ない](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。また、「Winny」を使っているユーザーのほとんどが日本人であるため、これらウイルスに感染するユーザーもまた日本人が大半となる（事実、マイクロソフトが発表した駆除報告\[11\]においても、ワーム感染PCの99%は日本語Windowsであったことが報告されている）。そうすると、世界規模でのウイルスへの対応が優先される各ウイルス対策ソフト会社の対応はどうしても遅れがちになり、その後もWinnyを感染源とするウイルス感染者が続出した。とりわけ、官公庁でのウイルスによる機密データ流出が、立て続けに報じられた。

現状のウイルスについては、2006年3月11日に行われた講演で、金子勇はWinnyのプログラムを少し書き換えるだけでウイルスの拡散防止が出来るが、裁判で著作権幇助に関する罪状で係争中であり、Winnyの更新が出来ない現状であると述べた。ウイルスについて、もしWinnyのプログラムで対策を行ったとしても、それに対応しないウイルスが出てくる可能性があり、Winnyのバージョンアップを頻繁に行わなければならなくなるとも述べた。

なお[2006年](../Page/2006年.md "wikilink")4月21日[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")(IPA)は、[P2Pデータ交換ソフト](../Page/Peer_to_Peer.md "wikilink")**Winny**におけるバッファーオーバーランによる脆弱性を発表した。この発表に基づき、いくつかのセキュリティ調査会社はこの脆弱性が適切なデータを用意する事で任意のコードを実行する事が可能である事を報告した。しかし[ソースコード](../Page/ソースコード.md "wikilink")が京都府警ハイテク犯罪対策室によって押収されている為プログラムの修正が出来ないので、この脆弱性に対する対策は「Winnyを使用しない事」とされた（その後[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")によってWinny利用者による修正バージョンが配布された）。

結果、[ウイルス対策ソフトを提供している企業などでは](../Page/アンチウイルスソフトウェア.md "wikilink")、Winnyの起動を止める、またはWinnyを検出・削除するツールを無料で提供することになった。ただし、家族など1台のパソコンを数人で共有している利用者には効果があるものの、ほとんどの利用者は1人1台でパソコンを利用しており、そういった場合はWinnyを利用していると自覚しているために、この種のツールをインストールすることがないため、効果は薄い。

また、2006年2月以降になると、[海上自衛隊](../Page/海上自衛隊.md "wikilink")員が[防衛庁](https://ja.wikipedia.org/wiki/防衛庁 "wikilink")の機密情報を漏洩させてしまったため、当時の[小泉純一郎](https://ja.wikipedia.org/wiki/小泉純一郎 "wikilink")[総理大臣](https://ja.wikipedia.org/wiki/総理大臣 "wikilink")が、防衛庁や各省庁に情報漏洩に関して再発防止を指示するなど、Winnyによる情報漏洩事件が多相次いで発表された。これを受けて[警察庁](https://ja.wikipedia.org/wiki/警察庁 "wikilink")が2006年3月に警察官全員に対し公私関係なくWinnyの使用を全面禁止とする通達を発し、3月15日に[安倍晋三](https://ja.wikipedia.org/wiki/安倍晋三 "wikilink")官房長官（当時）が記者会見でWinnyの使用を自粛するよう国民に呼びかけた。

一部の官庁ではデータ流出をきっかけに、遅ればせながら予算の手配を始めている。[財務省が原案を作成した](../Page/財務省_\(日本\).md "wikilink")[2007年](../Page/2007年.md "wikilink")度[予算](../Page/予算.md "wikilink")の復活折衝で、ファイル共有ソフトによる情報漏洩を防ぐための技術開発費として、10億円を計上することが認められた。これは[総務省](../Page/総務省.md "wikilink")が要求していた予算である。

### 情報漏洩を防ぐ

前述のようにWinnyを利用することにより自らが情報漏洩などの被害を受けることもある。このため、「確実な方法はWinnyを使用しないことである」という意見が[内閣官房](../Page/内閣官房.md "wikilink")など各方面で呼びかけられた\[12\]。[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")（IPA）も、Winnyを導入しないことなどを対策として挙げている\[13\]。

## プロバイダによる規制

これまでに、違法なファイルの交換によるインターネット回線帯域の増大を理由に、2003年に[iTSCOM](https://ja.wikipedia.org/wiki/iTSCOM "wikilink")がWinnyによる帯域の使用の制限を報告。他にも幾つかの[インターネットプロバイダ](https://ja.wikipedia.org/wiki/インターネットプロバイダ "wikilink")が、事前告知あり・なしに限らず、Winnyによる帯域の使用を制限している。

そして流出事件を機に、2006年3月には[ぷらら](../Page/ぷらら.md "wikilink")や[nifty](https://ja.wikipedia.org/wiki/nifty "wikilink")がWinnyの使用を制限するサービスを、2006年5月頃を目処に始めるとしていた。ぷららやniftyの「Winnyによる帯域の使用制限」については、一部地域で2006年4月頃より始まっていた。

しかし、[総務省](../Page/総務省.md "wikilink")は2006年5月18日に、ぷららが2006年5月から開始する予定であった「Winnyの信号を感知すると通信を遮断する」措置について、利用者の通信を解読し、その内容に応じて通信を許可または禁止するという行為は、[通信の秘密](../Page/通信の秘密.md "wikilink")保護を定めた「[電気通信事業法](../Page/電気通信事業法.md "wikilink")」に抵触し、違法であるとの見解を示した\[14\]。これを受け、ぷらら側は「無断での通信遮断措置の発動」を停止した。なお、現在は[フレッツ](../Page/フレッツ.md "wikilink")光及びADSLのサービスとしてWinnyを遮断する機能を利用できる。

現在でも、実質的に切断に近いレベルの速度制限を続けているプロバイダがいくつかある。([Biglobe](https://ja.wikipedia.org/wiki/Biglobe "wikilink")等)

## 脚注

### 注釈

### 出典

## 参考文献

  -
## 関連項目

  - [WinMX](../Page/WinMX.md "wikilink")
  - [Antinny](../Page/Antinny.md "wikilink")
  - [Nyzilla](https://ja.wikipedia.org/wiki/Nyzilla "wikilink")
  - [Share (ソフトウェア)](../Page/Share_\(ソフトウェア\).md "wikilink")
  - [Perfect Dark](https://ja.wikipedia.org/wiki/Perfect_Dark "wikilink")
  - [ダウンロードソフト板](https://ja.wikipedia.org/wiki/ダウンロードソフト板 "wikilink")
  - [山田オルタナティブ](../Page/山田オルタナティブ.md "wikilink")
  - [原田ウイルス](../Page/原田ウイルス.md "wikilink")
  - [暴露ウイルス](../Page/暴露ウイルス.md "wikilink")
  - [WinnyCacheinfo](https://ja.wikipedia.org/wiki/WinnyCacheinfo "wikilink")
  - [パソコン遠隔操作事件](https://ja.wikipedia.org/wiki/パソコン遠隔操作事件 "wikilink")
  - [マキシマムザホルモン](https://ja.wikipedia.org/wiki/マキシマムザホルモン "wikilink") - 楽曲「え・い・り・あ・ん」後半部より“STOP STOP Winny”を繰り返す

## 外部リンク

  - [金子勇のソフトウェアページ](http://kaneko-isamu.la.coocan.jp/) - 作者サイト

  - \- 現在はWinny関連の記述は残っていない

  -
[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:著作権侵害](https://ja.wikipedia.org/wiki/Category:著作権侵害 "wikilink") [Category:2ちゃんねる関連事象](https://ja.wikipedia.org/wiki/Category:2ちゃんねる関連事象 "wikilink") [Category:匿名ネットワーク](https://ja.wikipedia.org/wiki/Category:匿名ネットワーク "wikilink")

1.  [byte2004 p.25](https://ja.wikipedia.org/wiki/#byte2004 "wikilink")
2.  WinMXはMXと略されていたが、それに倣ってWinnyはNYと呼ばれていた。
3.  [社団法人](../Page/社団法人.md "wikilink")[コンピュータソフトウェア著作権協会](../Page/コンピュータソフトウェア著作権協会.md "wikilink")（ACCS）による[「ファイル交換ソフト利用実態調査」](http://www2.accsjp.or.jp/) ホーム→ニュース→調査報告）より
4.  [Winnyノード数の推移分析](https://web.archive.org/web/20060713194310/http://www.onepointwall.jp/winny/winny-node.html)（2006年7月13日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
5.  [byte2004 p.26](https://ja.wikipedia.org/wiki/#byte2004 "wikilink")
6.  [Winnyの通信解読に挑戦！](http://itpro.nikkeibp.co.jp/article/COLUMN/20060511/237617/?ST=neteng&P=1) - Itpro
7.  [47氏発言集(手抜き版)](https://web.archive.org/web/20131022014942/http://winny.info/2ch/47.html)（2013年10月22日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
8.  [Winnyサイトブラウザ "Nyzilla"](http://takagi-hiromitsu.jp/Nyzilla/)
9.  [Winnyの技術](http://ascii.asciimw.jp/books/books/detail/4-7561-4548-5.shtml)（著：金子勇、編：アスキー書籍編集部） ISBN 4756145485
10. [【社会】特製ウィニーで摘発逃れか－東大助手、受信専用使う](https://web.archive.org/web/20040512063907/http://www.sanspo.com:80/sokuho/0511sokuho017.html)
11. [マイクロソフト、Telecom-ISAC Japan と協力し、20万を超えるAntinny ワームの駆除に成功](https://web.archive.org/web/20060206201727/http://www.microsoft.com/japan/presspass/detail.aspx?newsid=2504)（2006年2月6日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")） - マイクロソフト、2005年11月21日。
12. [Winnyを介して感染するコンピュータウイルスによる情報流出対策について](http://www.nisc.go.jp/press/inf_msrk.html)
13. [Winnyによる情報漏えいを防止するために](https://www.ipa.go.jp/security/topics/20060310_winny.html) - IPA
14. [ぷららのWinny規制は「違法」と総務省](http://www.itmedia.co.jp/news/articles/0605/18/news036.html) - Itmedia