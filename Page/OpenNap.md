> この記事は[OpenNap](https://ja.wikipedia.org/wiki/OpenNap)から翻訳されています。


**OpenNap**（オープン ナップ）はNapster社により運営されていた旧Napsterサービスの互換[プロトコル名および](../Page/通信プロトコル.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")ソフトウェアである。

## 概要

[Napster](../Page/Napster.md "wikilink")互換のプロトコルを利用した中央サーバ型のファイル交換機能と、独自プロトコルを利用したサーバに頼らない[ピュアP2P](https://ja.wikipedia.org/wiki/ピュアP2P "wikilink")型ネットワーク機能の両方を併せ持つ。

世界各地に[Napster](../Page/Napster.md "wikilink")互換サーバが立てられており、誰でも自由にログインできるサーバから、テーマが決まっている会員制のサーバまで様々なものがある。複数のネットワークに同時に接続することができる。

単にOpenNapと言うとプロトコル名を指す場合と、サーバソフトウェア名を指す場合があり、注意が必要である。

## NapsterとOpenNap

元々Napster互換として開発されたプロトコル、およびそれに準じたサーバソフトウェアであったが、Napster社の経営方針の変更により互換性はほぼ失われた。

その為、現在ではOpenNapは独自に発展したプロトコルとなっている。

## 機能

OpenNapは、Napster同様、[チャットシステム](https://ja.wikipedia.org/wiki/チャットシステム "wikilink")、[インスタントメッセージ](https://ja.wikipedia.org/wiki/インスタントメッセージ "wikilink")(IM)、[ファイル検索](https://ja.wikipedia.org/wiki/ファイル検索 "wikilink")、[ファイル参照](https://ja.wikipedia.org/wiki/ファイル参照 "wikilink")、[ファイル交換](https://ja.wikipedia.org/wiki/ファイル交換 "wikilink")の機能を有する。

ファイル交換部分以外は、IRCサーバを意識した作りとなっており。実際IRCとの共存タイプのサーバソフトウェアや、両対応のクライアントソフトが存在する。

## 日本語への対応

元々OpenNap自体は[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")を利用した検索システムを持っていたが、リンクサーバの実装が性能的な問題により困難だと判断した開発チームは、[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")を内部に持つことで非常に軽快な動作をするシステムを作り上げた。

しかし、問題点として、[分かち書き](https://ja.wikipedia.org/wiki/分かち書き "wikilink")がされていない日本語の検索に非常に大きな問題があった。

国内では、usjが中心となって立ち上げた[SlavaDev](https://ja.wikipedia.org/wiki/SlavaDev "wikilink")や、それを元にMataParaにより改良された[なぷぅやCappucinoによる](https://ja.wikipedia.org/wiki/Napu "wikilink")[FASS](https://ja.wikipedia.org/wiki/FASS "wikilink")などSlavaNap系陣営が、ハッシュテーブルではなくstrstr()関数を利用する事で全文検索を行う事で、日本語での検索システムの質を上げた。

また、それに対してOpenNap系陣営のShin1985による[OpenNapDev-JP](https://ja.wikipedia.org/wiki/OpenNapDev-JP "wikilink")やTrickの[OpenNap日本語検索強化パッチ](https://ja.wikipedia.org/wiki/OpenNap日本語検索強化パッチ "wikilink")はハッシュテーブルを利用する事に拘り、[SlavaNap](https://ja.wikipedia.org/wiki/SlavaNap "wikilink")系に比べてあまり検索精度が上がることは無かった。 OpenNap系は、主に国内最大手のONT2chやNeoShinNETなどの運営者やその協力者が自システムの為に開発していた為、その巨大なユーザーを支えるためにはメモリリソースなどの制約を無視出来なかった為と思われる。

また、斜陽期の2003年頃には、OpenNapをベースに[SQL](../Page/SQL.md "wikilink")や[KAKASI](https://ja.wikipedia.org/wiki/KAKASI "wikilink")を組み込み日本語検索やあいまい検索に対応した[SQLNap](https://ja.wikipedia.org/wiki/SQLNap "wikilink")などのシステムも登場したが、斜陽期であった事もあり、殆ど機能が実装されずにプロジェクトは解散した。

## OpenNapプロトコル準拠のソフトウェア

サーバソフトウェア

  - [OepnNap](https://ja.wikipedia.org/wiki/OepnNap "wikilink")
  - [OpenNap-NG](https://ja.wikipedia.org/wiki/OpenNap-NG "wikilink")
  - [OpenNapDev-JP](https://ja.wikipedia.org/wiki/OpenNapDev-JP "wikilink")
  - [SlavaNap](https://ja.wikipedia.org/wiki/SlavaNap "wikilink")
  - [SlavaNapDev](https://ja.wikipedia.org/wiki/SlavaNapDev "wikilink")
  - [Napu](https://ja.wikipedia.org/wiki/Napu "wikilink")
  - [FASS](https://ja.wikipedia.org/wiki/FASS "wikilink")
  - [FaceNap](https://ja.wikipedia.org/wiki/FaceNap "wikilink")
  - [DICE](https://ja.wikipedia.org/wiki/DICE "wikilink")

クライアントソフトウェア

  - [WinMX](../Page/WinMX.md "wikilink")
  - [Lopster](https://ja.wikipedia.org/wiki/Lopster "wikilink")
  - [XNap](https://ja.wikipedia.org/wiki/XNap "wikilink")
  - [TagNap](https://ja.wikipedia.org/wiki/TagNap "wikilink")
  - [Napchan](https://ja.wikipedia.org/wiki/Napchan "wikilink")
  - [2get](https://ja.wikipedia.org/wiki/2get "wikilink")
  - [Mameya](https://ja.wikipedia.org/wiki/Mameya "wikilink")
  - [Utatane](https://ja.wikipedia.org/wiki/Utatane "wikilink")

## 外部リンク

  - [SourceForge上の公式サイト](http://opennap.sourceforge.net/)

[Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink")