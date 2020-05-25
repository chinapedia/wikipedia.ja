> この記事は[BitTorrent DNA](https://ja.wikipedia.org/wiki/BitTorrent_DNA)から翻訳されています。


**BitTorrent DNA**（ビットトレント・ディエヌエー、bittorrent delivery network accelerator）は、米ビットトレント社の開発した[インターネット](../Page/インターネット.md "wikilink")環境で使用される[P2P](https://ja.wikipedia.org/wiki/P2P "wikilink")（ピア・トゥー・ピア、peer to peer）型のコンテンツ配信用ソフトウェアである。すでに世界中で広汎に利用されているP2P用ソフトウェアである**[BitTorrent](../Page/BitTorrent.md "wikilink")**をベースに、主に[動画共有サービス](../Page/動画共有サービス.md "wikilink")で使用されることを想定し商業利用も可能なように改良され、2007年末に現れた新しいインターネット用P2Pソフトウェアである。 [280px](https://ja.wikipedia.org/wiki/ファイル:BitTorrent_DNAの動作説明1.PNG "wikilink") [350px](https://ja.wikipedia.org/wiki/ファイル:BitTorrent_DNAの動作説明2.PNG "wikilink")

## 特徴

  - 動画[サーバ](../Page/サーバ.md "wikilink")に[アクセス](../Page/アクセス.md "wikilink")が集中しない
      - [コンテンツ](../Page/コンテンツ.md "wikilink")・データは細分化されハッシュ値で管理された「ピース」となって、分散された「[ピア](../Page/ピア.md "wikilink")」PC上に格納されている
      - 「DNAクライアント」は多数のピアPCとの間で多数のセッションを張って、同時に複数のピースをダウンロードする
  - 動画サーバからはオリジナル・データの一部ピースが各ピアPCに送信されるように設定できるので、特定の断片だけが欠けるといった従来のBitTorrentでの問題が発生しない
  - ユーザーPC上にDNAクライアント・ソフトをインストールした後は、ポート開放や「トレント・ファイル」といったP2Pでの動作を意識する必要がなくなり、（無料の場合は）Webページをクリックするだけで済む
      - 80番ポートを使う
      - DNAクライアントはHTTPのローカル・プロキシとしてバックグランドで動作する
  - DNAクライアントへの配信開始は、トレント・ファイルを送信する「トラッカ」側で管理できる

## 動画配信の現状と今後

### これまでの動画配信サービス環境

[アクトビラ](../Page/アクトビラ.md "wikilink")や[GyaOのような商業ベースでの有料](https://ja.wikipedia.org/wiki/GYAO!#GyaO "wikilink")・無料の動画配信サービスはいくつかあり、また、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")や[ニコニコ動画](../Page/ニコニコ動画.md "wikilink")のような投稿動画コンテンツの配信もインターネット・ユーザーの支持を集めている。これら大容量ファイルの配信環境は、通信路の占有負荷だけでなく配信元サーバの負荷が大きなものとなるため、ユーザーに安定して配信するための大規模な設備投資の負担が大きくなっており、結果として高解像度で秒当りの画像枚数が多い動画は扱えない状況にある。

動画サーバへのアクセスの集中を回避するために考えられた[IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")のような新しい技術を使用するためには、現在のインターネットを構成している多くの通信機器を対応する新しいものと取り替えねばならず、主要なインターネット通信環境を保有する[プロバイダ各社が](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、それほどの投資に見合ったメリットをほとんど得られない現状では、すぐに解決できるとは考えられない。

### アナログ動画の衰退

上記の動画配信サービスの拡大に加えて、将来の[地上波アナログ放送](https://ja.wikipedia.org/wiki/地上波アナログ放送 "wikilink")の停波やインターネット光接続の増加、VHSビデオの衰退、TV放送の多チャンネル化、番組著作権のメディア・フリー化、[H.264](../Page/H.264.md "wikilink")デコーダの一般化、NHKやTokyo MXのようなTV放送局のネット進出、[iPod touchのような携帯動画端末の普及](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")、NTT各社の[NGN](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")（次世代ネットワーク）計画など、デジタル・データによる高解像度・大画面の動画コンテンツの普及が加速度をつけて増加しており、一部には今ある地上波TV番組のかなりの視聴時間は、将来インターネット配信などのメディアが奪うのではないかという意見もある\[1\]。

### 将来のP2Pによるコンテンツ配信

BitTorrent DNAのようなP2Pによるコンテンツ配信が今後普及すれば、以下のような効果が得られる。

  - ユーザー側では、多くの人が使用するほど安定し、人気があるコンテンツほどダウンロードがより高速になる。
  - コンテンツの配信事業者側では、配信設備を増やすのではなくむしろ既にある設備が過剰になるくらいに配信サーバの負担が軽くなる。
  - プロバイダ側でも特段の対応は求められない。ただし、大容量データ配信による通信路への負担は増すので対応が必要になる可能性がある。

現状ではサーバ機の増設やネットワーク機器の更新による販売機会が減ることや、TV放送などの業界などへの影響以外でのデメリットは考えられない。ただ、スポーツ中継のような即時性が求められる動画番組の配信の対応には不明な点がある。すでにBitTorrent DNAに似たP2Pソフトに[Joost](../Page/Joost.md "wikilink")がある。

## 脚注

## 出典

  - 「BitTorrent DNA」日経NETWORK 2008年1月号 p.28-p.29

## 関連項目

  - [Joost](../Page/Joost.md "wikilink")
  - [BitTorrent](../Page/BitTorrent.md "wikilink")

## 外部リンク

  - [日本法人のウェブサイト](https://web.archive.org/web/20101120032303/http://bittorrent.co.jp/dna/)(2010年11月20日時点のアーカイブ)

[en:BitTorrent (software)\#BitTorrent DNA](https://ja.wikipedia.org/wiki/en:BitTorrent_\(software\)#BitTorrent_DNA "wikilink")

[Category:BitTorrent](https://ja.wikipedia.org/wiki/Category:BitTorrent "wikilink") [Category:インターネットテレビ局](https://ja.wikipedia.org/wiki/Category:インターネットテレビ局 "wikilink") [Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink")

1.  大野敏行、野沢哲生著　「アナログ停波に死角あり」　日経エレクトロニクス　2007年12月3日号　p.47-p.65