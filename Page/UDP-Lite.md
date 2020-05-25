> この記事は[UDP-Lite](https://ja.wikipedia.org/wiki/UDP-Lite)から翻訳されています。


**UDP-Lite**（ユーディーピー・ライト、Lightweight User Datagram Protocol）は、主に[インターネット](../Page/インターネット.md "wikilink")で使用される[プロトコル](../Page/プロトコル.md "wikilink")の1つで音声や動画の伝送を目的にしている。

## 概要

従来の[UDP](../Page/User_Datagram_Protocol.md "wikilink")[パケット](../Page/パケット.md "wikilink")では1[ビット](../Page/ビット.md "wikilink")でもデータが損傷すれば破棄されるのに対して、UDP-Liteはそのまま伝送される。

従来のUDPと同様、主に[IP上に実装されており](../Page/Internet_Protocol.md "wikilink")[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")のトランスポート層にあたる。UDPと同様に送達確認などを行わない無手順方式であり転送時のパケット紛失やデータ誤り等の対応手段が必要ならセッション層以上のプロトコルで対応する必要があるが、転送効率が高められるため、主に途中でデータが抜け落ちても問題が比較的少なく、むしろ再送処理による遅延が問題となる音声や動画の[ストリーム](https://ja.wikipedia.org/wiki/ストリーム "wikilink")配信での使用を想定して2004年7月にRFC 3828で定義された。

## UDPとの違い

  - UDPパケットでは1ビットでもデータが損傷すれば破棄されるのに対して、UDP-Liteはそのまま伝送される。
  - [プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")がUDPは17に対して、UDP-Liteは136である。
  - ヘッダー部の5-6バイト目がUDPでは「長さ」フィールドであったが、UDP-Liteでは「チェックサム・カバー範囲」（Checksum coverage）フィールド（後述）になっている。

## 規格と仕組み

### 規格

RFC 3828で定義されている。

### プロトコル番号：136

UDP-Liteには新たに136という[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")が割り当てられている。IPヘッダー中の該当位置にこの番号を示すことでIPパケットの中身がUDP-Liteとして認識される。

### チェックサム・カバー範囲

UDP-Liteヘッダー部の5-6バイト目が「[チェックサム](../Page/チェックサム.md "wikilink")・カバー範囲」と呼ばれ、「0」又は「8以上」の数字が入る。「0」の場合はUDP-Liteパケット全体が、「8以上」の場合はUDP-Liteヘッダー部を含む保護したいデータ部のサイズをバイト数で指定する。指定された範囲だけがチェックサム計算の対象となる。チェックサム計算の結果がヘッダー部の7-8バイト目に格納されるのはUDPと同じである。

例えば、チェックサム・カバー範囲の値が「8」である場合は、「8×8bit=64bit」となり、UDP-Liteヘッダー部の長さと同じになるため、ヘッダー分に続くデータ部分はチェックサムの計算対象からはずされる。データ部分がチェックサムの計算対象からはずされるということは、データ部分に損傷が生じても検知されずにそのまま運ばれることを意味する。

チェックサム・カバー範囲の値をUDP-Liteヘッダー部とUDP-Liteデータ部のサイズの合計値にすれば、従来のUDPの「長さ」フィールドと同じ値となり、互換性が保てるとしている。

### その他の仕様概要

  - TCPやUDP同様、ひとつのIPアドレスで16bit（65535個）の論理ポートを持つことができる。物理的・IPアドレス的に１つであっても、論理的に多重化された65535個までの通信を行うことができる。

### UDP-Liteパケットのフォーマット

ヘッダーの一部をUDPから変更することで、パケットの完全性の保証範囲をより柔軟に変更出来るようになった。 [UDP-Liteパケットのデータ・フォーマット.PNG](https://ja.wikipedia.org/wiki/File:UDP-Liteパケットのデータ・フォーマット.PNG "fig:UDP-Liteパケットのデータ・フォーマット.PNG")

## 参考図書

  - 日経NETWORK　2007年7月号 「UDP-Lite」 p.71

## 関連項目

  - [UDP](../Page/User_Datagram_Protocol.md "wikilink")
  - [RFC 3828](http://tools.ietf.org/html/rfc3828) - Lightweight User Datagram Protocol

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")