> この記事は[Telepathy](https://ja.wikipedia.org/wiki/Telepathy)から翻訳されています。


**Telepathy**（テレパシー）は、[インスタントメッセージングや](../Page/インスタントメッセンジャー.md "wikilink")[Voice over IP](../Page/VoIP.md "wikilink")、[ビデオ会議](../Page/ビデオ会議.md "wikilink")のような個人間のコミュニケーションを目的とするソフトウェアを作成する際に使われる[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")の総称である。テレパシーを使うことで、[D-Bus](../Page/D-Bus.md "wikilink")の[プロセス間通信](../Page/プロセス間通信.md "wikilink")メカニズムによるコンポーネントを利用したコミュニケーションソフトウェアを作ることが出来る。各アプリケーションとそれらが用いているネットワークプロトコルの境界を明確にすることにより、コミュニケーションソフトウェアの開発を単純にすること、また[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")や[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")の開発者たちによる[コード再利用](https://ja.wikipedia.org/wiki/コード再利用 "wikilink")を促進することが目標とされている。

以下に挙げる例は、テレパシーのインターフェイスを出力する様々なプロトコルがフリーソフトウェアとして実装されているケースである。

  - **Gabble**：オープンソースのインスタントメッセージングサーバである[XMPPに用いられている](../Page/Extensible_Messaging_and_Presence_Protocol.md "wikilink")。XMPPの拡張機能である[Jingle (プロトコル)のサポートも含む](https://ja.wikipedia.org/wiki/Jingle_\(プロトコル\) "wikilink")。

<!-- end list -->

  - **Butterfly**：[MSN Messengerに用いられている](https://ja.wikipedia.org/wiki/MSN_Messenger "wikilink")。

<!-- end list -->

  - **Idle**：[Internet Relay Chatに用いられている](../Page/Internet_Relay_Chat.md "wikilink")。

<!-- end list -->

  - **Salut**：リンク・ローカルな [XMPP](../Page/Extensible_Messaging_and_Presence_Protocol.md "wikilink") プロトコルに使用されている。

<!-- end list -->

  - **Haze**：[Pidgin](../Page/Pidgin.md "wikilink")に用いられている、libpurpleライブラリがサポートするプロトコルのアクセスに用いられる。[2007年](../Page/2007年.md "wikilink")の[Google Summer of Codeプロジェクトの一環として行われた](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink")\[1\]。

<!-- end list -->

  - **Telepathy-SofiaSIP**：[ノキア](../Page/ノキア.md "wikilink")のオープンソースなSofia-SIP libraryを用いた[セッション確立プロトコル](https://ja.wikipedia.org/wiki/セッション確立プロトコル "wikilink")に用いられる。

末端のアプリケーションに低位テレパシーコンポーネント（例えば接続マネージャ）の詳細を表示する方法を提示するコンポーネントの一つに、ミッション・コントロールがある\[2\]。

テレパシーを用いた基本的なインスタントメッセンジャーとテレビ電話ソフトウェアがノキア製携帯電話であるNokia [770](https://ja.wikipedia.org/wiki/Nokia_770 "wikilink")、[N800](https://ja.wikipedia.org/wiki/Nokia_N800 "wikilink")、[N810に搭載されている](https://ja.wikipedia.org/wiki/Nokia_N810 "wikilink")。[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")・[OpenMoko](../Page/OpenMoko.md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")プラットフォームの一部である。

## 仕様

プロトコルを実装することにより、「接続マネージャ」と呼ばれるD-Busサービスが与えられる。サービスに接続するためには、テレパシーのクライアントがその実装されたプロトコルを用いる必要がある。一度接続が成立すれば、以降のコミュニケーションは、接続により要求される“チャンネル”というオブジェクトを用いて行われる。例えば、あるチャンネルではテキストメッセージを送受信したり、コンタクトリストを表示したり、もしくはIP電話をしたりすることが出来る。

## 関連アプリケーション

  - [Landell](https://ja.wikipedia.org/wiki/Landell "wikilink")
  - [Tapioca](https://ja.wikipedia.org/wiki/Tapioca "wikilink")
  - [Empathy](https://ja.wikipedia.org/wiki/Empathy "wikilink")
  - [Decibel](../Page/Decibel.md "wikilink")

## 外部リンク

  - [プロジェクトのウェブサイト](http://telepathy.freedesktop.org)
  - Telepathyの開発代表者 Robert McQueenによるスピーチが視聴可能：["IM/VOIP Communications Framework"](http://mirror.linux.org.au/pub/linux.conf.au/2007/video/talks/301.ogg) (77MB oggビデオ)もしくは[ストリーミングフラッシュビデオ](http://lca2007.linux.org.au/talk/301)から。

## 脚注

<references/>

[Category:インスタントメッセンジャー](https://ja.wikipedia.org/wiki/Category:インスタントメッセンジャー "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")

1.
2.  [mission-control](http://mission-control.sourceforge.net/)