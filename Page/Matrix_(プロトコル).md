> この記事は[Matrix \(プロトコル\)](https://ja.wikipedia.org/wiki/Matrix_\(プロトコル\))から翻訳されています。


**Matrix**は、のための[オープン標準](../Page/オープン標準.md "wikilink")で軽量な[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。あるのアカウントを持つユーザが、[チャット](../Page/チャット.md "wikilink")、[VoIP](../Page/VoIP.md "wikilink")及び[テレビ電話](../Page/テレビ電話.md "wikilink")を介して、別のサービスプロバイダのユーザとコミュニケーションを行うことができるように設計されている。つまり、標準的な[SMTP](https://ja.wikipedia.org/wiki/SMTP "wikilink")による電子メールが[ストアアンドフォワード](../Page/ストアアンドフォワード.md "wikilink")型の電子メールサービスで提供されているように、異なるサービスプロバイダ間でリアルタイム通信をシームレスに機能させることを目的としている。

技術的な観点から見ると、Matrixはリアルタイム通信のための[アプリケーション層](../Page/アプリケーション層.md "wikilink")の通信プロトコルである。Matrixはサーバのオープンな連合を介しての[JSON](https://ja.wikipedia.org/wiki/JSON "wikilink")形式のメッセージの安全な配布及び永続化のための[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink") API及び[オープンソース](../Page/オープンソース.md "wikilink")の[リファレンス実装](../Page/リファレンス実装.md "wikilink")を提供している\[1\]\[2\]。[WebRTC](https://ja.wikipedia.org/wiki/WebRTC "wikilink")を介して標準的な[Webサービス](../Page/Webサービス.md "wikilink")と統合することができ、ブラウザ間での応用が容易である。

## 歴史

初期のプロジェクトは、Matthew HodgsonとAmandine Le Papeによって "Amdocs Unified Communications"\[3\] と呼ばれるチャットツールを構築しながら内で作成された。その後、Amdocsはからまでの開発作業の殆どに資金提供をした\[4\]。MatrixはWebRTC 2014 Conference & Expoでイノベーション賞を受賞し\[5\]、のWebRTC Worldで "Best in Show" 賞を受賞した\[6\]。このプロトコルはに登場した後、幾つかの指摘を交えて賞賛を受けた。レビュアーはこの種のオープンな[インスタントメッセージ](../Page/インスタントメッセージ.md "wikilink")やマルチメディアを定義する試みは、広く採用されることが困難であり、これは技術的及び政治的に関連する課題を強調していると述べた\[7\]。プロバイダ間で相互運用するサービスに対するユーザの十分な需要があるかは不明だった\[8\]\[9\]。、Amdocsの[子会社](../Page/子会社.md "wikilink")の "Vector Creations Limited" が設立され、Matrixのスタッフが移動した\[10\]。

、Amdocsからの資金提供が削減されることが発表され、翌週にコアチームは[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")を拠点とするMatrixと[Elementのサポートのための独自の会社である](../Page/Element_\(ソフトウェア\).md "wikilink") "New Vector" を設立した\[11\]。この期間中、コアチームの賃金の一部の支援のために、Matrixを基盤とするコミュニティ及び企業へのサポートに対する複数の連絡があった\[12\]。開発速度を維持するために[Patreon](https://ja.wikipedia.org/wiki/Patreon "wikilink")及びのクラウドファンディングアカウントが作成され\[13\]、コアチームはMatrix "Live" と呼ばれる[ビデオポッドキャストを開始した](../Page/ポッドキャスト.md "wikilink")\[14\]。これは "This Week in Matrix" と呼ばれる週間[ブログ](../Page/ブログ.md "wikilink")形式に拡張され、関心のあるコミュニティメンバーは、Matrix関連のニュースを読んだり、関連するニュースを投稿することができる\[15\]。New VectorはMatrixにサービスを提供し、Matrixサーバの有料ホスティングを提供し、収入を得ることを目的に設立された\[16\]。

New Vectorの設立から数週間後、Matrixチームとは [スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")の作成で協力する計画を発表した\[17\]。Librem 5はMatrixネイティブのスマートフォンを意図しており、デフォルトの[プリインストール](../Page/プリインストール.md "wikilink")メッセージングアプリと電話アプリは、VoIP、テレビ電話及びインスタントメッセージにMatrixを使用する必要がある\[18\]。

、[KDE](../Page/KDE.md "wikilink")はIRCクライアントの[Konversation](../Page/Konversation.md "wikilink")をMatrixに対応させることを取り組んでいることを発表した\[19\]。下旬、New Vectorは[Ethereum](https://ja.wikipedia.org/wiki/Ethereum "wikilink")を基盤とする[ベンチャー](../Page/ベンチャー.md "wikilink")であるStatusから500万米ドルの投資を受けた\[20\]\[21\]。

、[フランス共和国政府は独自のインスタントメッセージングツールを作成する計画を発表した](https://ja.wikipedia.org/wiki/政府_\(フランス第五共和政\) "wikilink")\[22\]。"Tchap" と呼ばれるElementとMatrixをベースとするアプリの開発を初頭に開始し\[23\]、に[iOS及び](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")[Android](../Page/Android.md "wikilink")向けにオープンソースとしてリリースされた\[24\]。

、標準の更なる発展のための法的に中立的な法人として\[25\]、"The Matrix.org Foundation C.I.C." と呼ばれるが設立された\[26\]。

、KDEコミュニティは[Telegram](https://ja.wikipedia.org/wiki/Telegram "wikilink")、[Slack及び](https://ja.wikipedia.org/wiki/Slack_\(ソフトウェア\) "wikilink")[Discordなどの他の最新ツールの分散型の代替として](https://ja.wikipedia.org/wiki/Discord_\(ソフトウェア\) "wikilink")、コミュニティ内部でのコミュニケーションにMatrixを採用し、独自のサーバインスタンスを運用することを発表した\[27\]。

、Matrix.orgの稼働中のサーバが攻撃されセキュリティ被害を受けた\[28\]。この攻撃は、Matrixプロトコルの問題ではなく、Matrix.org以外のホームサーバには直接影響は無かった。

、Matrixプロトコルは[ベータ版](../Page/ベータ版.md "wikilink")では無くなり、全てのAPI及びリファレンス実装のホームサーバであるSynapseのバージョンが1.0になり、The Matrix.org Foundationが正式に発足した\[29\]\[30\]。

、New VectorはMatrixの開発のために追加で850万米ドルを調達した\[31\]。

、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[連邦国防省](https://ja.wikipedia.org/wiki/連邦国防省 "wikilink")はMatrixプロトコル、Synapseサーバ及びElementアプリケーションに基づいた安全なインスタントメッセージングツールの "BwMessenger" と呼ばれるパイロットプロジェクトを発表した。これはフランスのTchapプロジェクトをモデルとしている。[連邦政府の長期的な目標は](../Page/連邦政府_\(ドイツ\).md "wikilink")、全ての省庁及び下位当局をカバーするメッセンジャーサービスを使用できるようにすることである\[32\]。

、[Mozilla](../Page/Mozilla.md "wikilink")はIRCの代替としてMatrixの使用を開始することを発表した。この発表で、下旬に移行を完了することを述べた。MozillaのIRCサーバであるirc.mozilla.orgは又はまでに削除されると言われている\[33\]。

## プロトコル

Matrixはウェブ向けの一般的なメッセージング及びデータ同期システムになるという長期的な目標と共に、VoIP、[IoT](https://ja.wikipedia.org/wiki/IoT "wikilink")及びグループコミュニケーションを含むインスタントメッセージなどの使用例を対象としている。このプロトコルはセキュリティと[レプリケーション](../Page/レプリケーション.md "wikilink")に対応しており、単一の制御点や障害無しに完全な会話記録を維持する。既存の通信サービスはMatrixエコシステムと統合することができる\[34\]。

Matrixのクライアントはオープンな連合インスタントメッセージング、VoIP及びIoTの通信に使用することができる。

Matrixの標準仕様はMatrixに対応したクライアント、サーバ及びサービス間でのJSONデータを安全に送信及び複製するための[RESTful](../Page/Representational_State_Transfer.md "wikilink") HTTP APIを明記している。クライアントはサーバ上の "room" にデータをPUTすることでデータを送信し、"room" に参加している全てのMatrixサーバにデータを複製する。このデータは改竄を軽減するために[Git](../Page/Git.md "wikilink")形式の署名で署名され、成り済ましを防ぐために連合トラフィックは[HTTPS](../Page/HTTPS.md "wikilink")で暗号化及び各サーバの秘密鍵で署名される。複製は[結果整合性](https://ja.wikipedia.org/wiki/結果整合性 "wikilink")の意味論に従う。これによって、他の参加しているサーバから欠落している履歴を再同期することにより、オフライン又はデータ損失後でも機能する。

Olmライブラリはの実装を介してルーム毎に任意の[エンドツーエンド暗号化](https://ja.wikipedia.org/wiki/エンドツーエンド暗号化 "wikilink")を提供する\[35\]。は、ルームの参加者だけが読めることを保証できる。これを組み合わせると、Matrixを介して送信されるデータは、Matrixサーバからは[暗号文](../Page/暗号文.md "wikilink")に見え、そのルームの承認された参加者だけが復号できるようになる。Olmライブラリ及びMegolmライブラリは、による暗号レビューの対象となっており、その結果は公開されており\[36\]、Matrixチームによって対処されている\[37\]。このレビューはが後援した。

## ブリッジ

Matrixは他のチャットアプリケーションからMatrixのルームへのメッセージのブリッジングに対応している。これらのブリッジはサーバ上で実行され、Matrix以外のサーバと通信するプログラムである。ブリッジはパペット又はリレーとして機能することができる。前者では個々のユーザが目に見える形でメッセージを投稿し、後者ではボットが操り人形でないユーザアカウントのメッセージを投稿する。

現在公式に対応しているブリッジ:

コミュニティによって管理されているその他の注目すべきブリッジ:

## クライアント

[Elementはクライアントのリファレンス実装である](../Page/Element_\(ソフトウェア\).md "wikilink")。は[GNOME](../Page/GNOME.md "wikilink")の公式クライアントである。この他にも多くのクライアント、ボット、ブリッジ、サーバ及びリファレンス実装以外のMatrixプロトコルの実装が存在する\[38\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - [XMPP](https://ja.wikipedia.org/wiki/XMPP "wikilink")
  - [SIP](../Page/Session_Initiation_Protocol.md "wikilink")
  - [RCS](https://ja.wikipedia.org/wiki/Rich_Communication_Services "wikilink")

## 外部リンク

  -
  -
[Category:通信](https://ja.wikipedia.org/wiki/Category:通信 "wikilink") [Category:インスタントメッセンジャー](https://ja.wikipedia.org/wiki/Category:インスタントメッセンジャー "wikilink") [Category:IP電話](https://ja.wikipedia.org/wiki/Category:IP電話 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.