> この記事は[Mumble](https://ja.wikipedia.org/wiki/Mumble)から翻訳されています。


**Mumble**(マンブル)は、[ゲーマー](../Page/ゲーマー.md "wikilink")向け音声通話用[VoIP](../Page/VoIP.md "wikilink")アプリケーション\[1\]。

[Skype](../Page/Skype.md "wikilink")、[Discord](https://ja.wikipedia.org/wiki/Discord_\(ソフトウェア\) "wikilink")、[TeamSpeak](https://ja.wikipedia.org/wiki/TeamSpeak "wikilink")などと同様、[フリーソフトウェアとして公開されている](../Page/フリーウェア.md "wikilink")。

## 概要

[クライアント・サーバー型](../Page/クライアントサーバモデル.md "wikilink")[アーキテクチャーを採用していて](../Page/コンピュータ・アーキテクチャ.md "wikilink")、ユーザーが同じサーバーを介して互いに会話できる\[2\]。 非常にシンプルな[ユーザーインターフェース](https://ja.wikipedia.org/wiki/ユーザーインターフェース "wikilink")を備えており、高音質と低遅延を特長としている。 すべての通信は[暗号](../Page/暗号.md "wikilink")化され、ユーザーの[プライバシー](../Page/プライバシー.md "wikilink")が確保される\[3\]。

Mumbleは[無料のオープンソースソフトウェアで](https://ja.wikipedia.org/wiki/FLOSS "wikilink")、異なる[OSでも使用可能な](../Page/オペレーティングシステム.md "wikilink")[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")となっており、[修正BSDライセンス](https://ja.wikipedia.org/wiki/修正BSDライセンス "wikilink")の条件の下、公開されている。

## チャンネル階層

Mumbleサーバー（「**Murmur**」と呼ばれる）には、ルートチャンネルとその下のチャンネルの階層ツリーがある。

ユーザーはこれらに一時的にチャンネルを接続することで、より大きな仮想チャンネルを作成することができる。

これは、チーム戦の[FPSなどのゲームの大規模イベントなどで](../Page/ファーストパーソン・シューティングゲーム.md "wikilink")、グループのユーザーが小さなチャンネルでチャットしている場合に、他のユーザーと共通のルートチャンネルのアナウンスを聞くことができ、役立つシステムである。

各チャンネルには、グループの関連セットと、ユーザー権限を制御するアクセス制御リストがある。 多くの使用シナリオをサポートしているが、チャンネルの構造が複雑になりやすい\[4\]。

## 音質

Mumbleは以前のデフォルトコーデックだった[Speex](../Page/Speex.md "wikilink")およびCELTに続き、さらに[低遅延な](../Page/レイテンシ.md "wikilink")[オーディオコーデック](https://ja.wikipedia.org/wiki/オーディオコーデック "wikilink")である[Opusバージョン](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink")1.2.4を使用している\[5\] 。

この音声圧縮技術とMumbleの設計によって、低遅延の通信を可能にしている。

つまり、一方で何か言われてからもう一方で聞かれるまでの間隔が短くなることで、よりリアルタイムに近い会話が可能になった。

また、Mumbleには[エコーキャンセル機能が組み込まれており](../Page/エコー除去.md "wikilink")、スピーカーまたは低品質のサウンドハードウェアを使用する場合のエコーを低減する。

## セキュリティとプライバシー

Mumbleは、 [TLS制御チャンネルを介してサーバーに接続し](../Page/Transport_Layer_Security.md "wikilink")、[UDPを介して送信される音声は](../Page/User_Datagram_Protocol.md "wikilink")、OCBモードの[AESで暗号化される](../Page/Advanced_Encryption_Standard.md "wikilink")\[6\]。バージョン1.2.9現在、Mumbleは、可能であればECDHE + [AES](../Page/Advanced_Encryption_Standard.md "wikilink")-[GCM暗号スイートを優先し](https://ja.wikipedia.org/wiki/Galois/Counter_Mode "wikilink")、完全な秘密音声転送を可能としている\[7\]。なお、バージョン1.2.0以降では、ユーザーの[パスワード](../Page/パスワード.md "wikilink")による認証はサポートされているが、一般的には[公開鍵証明書](../Page/公開鍵証明書.md "wikilink")の形式での認証を推奨していない\[8\]。

## オーバーレイ

ゲーム画面上で表示される統合オーバーレイがあり\[9\]、誰が話しているのか、どのリンクチャンネルにいるのか、わかるようになっている。

バージョン1.0以降、ユーザーはアバター(自分自身を示す画像)をアップロードしてオーバーレイで自分自身を表すことができ、ゲームをプレイしているときにもより他のプレイヤーを識別しやすくなった。

バージョン1.2の時点で、オーバーレイはWindows上のほとんどの[Direct3D](../Page/Direct3D.md "wikilink") 9/10および[OpenGL](../Page/OpenGL.md "wikilink")ゲームで動作し、[Linux](../Page/Linux.md "wikilink")および[Mac OS XでもOpenGLのものをサポートしている](https://ja.wikipedia.org/wiki/Mac_OS_X "wikilink")\[10\]。なお、Windows上での[Direct X 11ゲームのサポートは後のバージョンから行われるようになった](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。

## 定位置音声

特定のゲームでは、ゲーム内のプレイヤーの位置に応じて、立体的に他のプレイヤーの声をが聞こえるよう、音声に変更が加えられる\[11\]。これには、方向感覚だけでなく、距離感も含まれ、特にFPSでは、この要素は重要である。

これを実現するために、Mumbleは各プレイヤーのゲーム内でのポジションを、すべてのオーディオパケットで同じゲーム内のプレイヤーに送信する。 Mumbleは、これを行うために必要な情報をゲームプログラムを実行しているメモリ本体から直接読み取るか、いわゆるゲームとは[プラグイン](../Page/プラグイン.md "wikilink")を介して必要な情報を収集する\[12\]。

Mumbleとのゲームのリンクプラグインは、Mumbleプロジェクトが提供する小さなソースコードをゲームプログラムに含めることで、位置オーディオに必要な情報を公開する方法がゲームに提供されている\[13\][バルブ製の](../Page/Valve_Corporation.md "wikilink")[ゲームエンジン](../Page/ゲームエンジン.md "wikilink")である[Source Engineを採用するFPSゲーム](../Page/Source_Engine.md "wikilink")『[カウンターストライク](../Page/カウンターストライク.md "wikilink")』\[14\]、『[Team Fortress 2](https://ja.wikipedia.org/wiki/Team_Fortress_2 "wikilink")』、『[Day of Defeatt: Source](../Page/Day_of_Defeat.md "wikilink")』、『[ハーフライフ2](../Page/ハーフライフ2.md "wikilink")』\[15\]\[16\] や[MMORPG](../Page/MMORPG.md "wikilink")『』\[17\]\[18\]などの有名なゲームがMumbleプラグインを実装している。

## モバイルアプリ

もともと、デスクトップ版のみだったが、現在では[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")用の「 [Mumble for iOS](https://apps.apple.com/us/app/mumble/id443472808)」やAndorod用の「Plumble for Android」([Google Play](https://play.google.com/store/apps/details?id=com.morlunk.mumbleclient)、[F-Droid](https://f-droid.org/repository/browse/?fdid=com.morlunk.mumbleclient))が提供されている。

## サーバー統合

Mumbleは既存の技術的および社会的構造に適合している。そのため、サーバーは[Internet Communications Engine 上で完全に](https://ja.wikipedia.org/wiki/:en:Ice "wikilink")[リモート制御可能](../Page/遠隔手続き呼出し.md "wikilink")\[19\]、ユーザーチャンネルと仮想サーバー[インスタンス](../Page/インスタンス.md "wikilink")を操作できる。このプロジェクトでは、インターフェイスの機能を示す多数のサンプルスクリプト\[20\]既存の[phpBB](https://ja.wikipedia.org/wiki/phpBB "wikilink")やSimple Machines Forumの[データベース](../Page/データベース.md "wikilink")を使用したユーザー認証などの機能を提供するプレハブスクリプトを提供している\[21\]。murmurサーバーは、デフォルトでポート64738 [TCPおよび](../Page/Transmission_Control_Protocol.md "wikilink")[UDPを使用する](../Page/User_Datagram_Protocol.md "wikilink")。

Mumbleサーバー（Murmur）の代替ミニマリスト実装は「uMurmur」と呼ばれ\[22\]、たとえば[OpenWrt](https://ja.wikipedia.org/wiki/OpenWrt "wikilink")を実行する[レジデンシャルゲートウェイなど](https://ja.wikipedia.org/wiki/ホームゲートウェイ "wikilink")、[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")が限られている組み込みデバイスへのインストールを対象としている\[23\]。

## サーバーホスティング

他の多くのVoIPクライアントと同様、Mumbleサーバーはローカルでレンタルまたはホストできる。Mumbleサーバーをローカルでホストするには、Murmur（Mumbleインストーラーのオプションとして含まれている）をダウンロードして起動する必要がある。サーバーの構成は、構成ファイルを編集することで可能。 構成ファイルには、サーバー名、ユーザー認証、音質制限、およびポートに関する情報が含まれている。

また、サーバーを内部から管理するには、ユーザーに管理者権限を付与する必要がある。あるいは、スーパーユーザーアカウントにログインしてユーザーを管理することもでできる。サーバー内の管理者は、ルームを追加または編集し、ユーザーを管理し、サーバーの情報を表示できる。

## 脚注

## 関連項目

  - [VoIP](../Page/VoIP.md "wikilink")ソフトウェア
      - [Skype](../Page/Skype.md "wikilink")
      - [Discord](https://ja.wikipedia.org/wiki/Discord_\(ソフトウェア\) "wikilink")
      - [TeamSpeak](https://ja.wikipedia.org/wiki/TeamSpeak "wikilink")

## 外部リンク

  - [Mumble 公式サイト](https://www.mumble.info/)(英語)

[Category:インスタントメッセンジャー](https://ja.wikipedia.org/wiki/Category:インスタントメッセンジャー "wikilink") [Category:Androidのソフトウェア](https://ja.wikipedia.org/wiki/Category:Androidのソフトウェア "wikilink") [Category:IOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:IOSのソフトウェア "wikilink") [Category:Linuxのソフトウェア](https://ja.wikipedia.org/wiki/Category:Linuxのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:VoIPのソフトウェア](https://ja.wikipedia.org/wiki/Category:VoIPのソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.
2.
3.
4.
5.   Mumble|website=blog.mumble.info|language=en-US|access-date=2017-09-30}}
6.
7.
8.
9.
10.
11.
12. 例えば、FPSゲーム「[Alliance of Valiant Arms](https://ja.wikipedia.org/wiki/Alliance_of_Valiant_Arms "wikilink")」(AVA)では、ゲーム本体とは別にブラウザ上からプラグインをダウンロードする方式だった。現在AVAでは、同じくフリーの音声通話ソフト[Discordに置き換わっている](https://ja.wikipedia.org/wiki/Discord_\(ソフトウェア\) "wikilink")。
13.
14. 日本ではオンラインゲームとしてバルブと[ネクソン](../Page/ネクソン.md "wikilink")が共同開発し、ネクソンが提供していた「カウンターストライク オンライン」として知られる。日本版は2019年3月6日にサービス終了した。
15.
16.
17.
18.
19.
20.
21.
22.
23.