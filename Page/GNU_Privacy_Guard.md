> この記事は[GNU Privacy Guard](https://ja.wikipedia.org/wiki/GNU_Privacy_Guard)から翻訳されています。


**GNU Privacy Guard** (**GnuPG**, **GPG**) とは、[Pretty Good Privacy](../Page/Pretty_Good_Privacy.md "wikilink") (PGP) の別実装として、[GPL](../Page/GNU_General_Public_License.md "wikilink") に基づいた[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")ソフトである。 [OpenPGP](https://ja.wikipedia.org/wiki/OpenPGP "wikilink") 規格 (RFC 4880) に完全準拠しているが、古い PGP との互換性は完全ではない。

## 開発

GnuPG の開発は [ヴェルナー・コッホ](https://ja.wikipedia.org/wiki/ヴェルナー・コッホ "wikilink")(Werner Koch) によって始められた。現在では David Shaw と Timo Schulz も加わっている。また、[g10 Code](http://www.g10code.de/) が Werner Koch と Timo Schulz を資金面で援助している。

バージョン 1.0.0 は 1999 年にリリースされ、それ以降 2002 年の 1.2.0 や 2004 年の 1.4.0 のように、安定版は最初の小数部分が偶数になるバージョンでリリースされている。

一方、 [S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink") 機能の導入を目的とした別系列の開発版が 1.9 系列として開発が進められていた。この系列は[2006年](../Page/2006年.md "wikilink")[11月23日](../Page/11月23日.md "wikilink")に 2.0 としてリリースされた。

2014年11月、[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")のサポートなど新しいOpenPGP規格に準拠した 2.1 系列がリリースされた。

2.0 系列、2.2/2.1 系列と並行して 1.4 系列のサポートは継続しており、1.4 系列は 2.2/2.1 系列あるいは 2.0 系列と同時にインストール、独立して運用することが可能である。2.2/2.1 系列と 2.0 系列を同時にインストールすることはできない\[1\]。

### 系列

2018年1月現在、GnuPG には 2 つの系列が存在する。

  - "modern" (2.2): 最新の開発系列であり、[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")など新機能を実装している。2017年8月28日に、2.2.0として新たな安定版となった\[2\]。初版リリースは2014年11月6日\[3\]。
  - "classic" (1.4): 旧来のスタンドアロン版。古いシステムや組み込み用途に適している。初版リリースは2004年12月16日\[4\]。

既にサポートが終了した系列は 3 つ存在する。

  - 2.0 系列: 初版リリースは2006年11月13日\[5\]。最終版は2016年3月31日リリースの2.0.30\[6\]。
  - 1.2 系列: 初版リリースは2002年9月22日\[7\]、最終版は2004年10月26日リリースの1.2.6\[8\]。
  - 1.0 系列: 初版リリースは1999年9月7日\[9\]、最終版は2002年4月30日リリースの1.0.7\[10\]。

## 利用形態

GnuPG は数多くの OS に含められてきた。

また、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink") の[フロントエンド](../Page/フロントエンド.md "wikilink")も開発されており、[KMail](https://ja.wikipedia.org/wiki/KMail "wikilink") や [Evolution](../Page/Evolution_\(ソフトウェア\).md "wikilink") といった[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")に統合されたものや、 [KDE](../Page/KDE.md "wikilink") の [KGpg](https://ja.wikipedia.org/wiki/KGpg "wikilink") や [GNOME](../Page/GNOME.md "wikilink") の [Seahorse](https://ja.wikipedia.org/wiki/Seahorse "wikilink") のように単独のアプリケーションもある。これらフロントエンドの多くは GnuPG 開発者が用意した GPGME (GnuPG Made Easy) ライブラリを利用している。

  - GUIフロントエンドの例
      - [WinPT](https://ja.wikipedia.org/wiki/WinPT "wikilink")（Windows用）
      - [GnuPG Shell](https://ja.wikipedia.org/wiki/GnuPG_Shell "wikilink")（Linux/Windows用）
      - [KGpg](https://ja.wikipedia.org/wiki/KGpg "wikilink")、[Seahorse](https://ja.wikipedia.org/wiki/Seahorse "wikilink")（Linux用）
  - 電子メールクライアントの例
      - [Enigmail](https://ja.wikipedia.org/wiki/Enigmail "wikilink")（Linux/macOS/Windows用、[Mozilla Thunderbirdおよび](../Page/Mozilla_Thunderbird.md "wikilink")[Seamonkey](https://ja.wikipedia.org/wiki/Seamonkey "wikilink")用[アドオン](../Page/拡張機能_\(Mozilla\).md "wikilink")）
      - [KMail](https://ja.wikipedia.org/wiki/KMail "wikilink")、[Evolution](../Page/Evolution_\(ソフトウェア\).md "wikilink")（Linux用）
  - 統合パッケージ（GnuPGとGUIフロントエンド・電子メールクライアントの一括インストール）
      - [Gpg4win](https://ja.wikipedia.org/wiki/Gpg4win "wikilink")（Windows用）
      - [GPGTools](https://ja.wikipedia.org/wiki/GPGTools "wikilink")（macOS用）

## アルゴリズム

GnuPG は、特許で制限されているアルゴリズムを含めていない。

このため従来の GnuPG では、[PGP](../Page/Pretty_Good_Privacy.md "wikilink") の過去のバージョンで標準で用いられていた [International Data Encryption Algorithm](https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm "wikilink") (IDEA) を使うことができず、使用にはプラグインが必要であったが、各国における IDEA の特許切れ\[11\]に伴い、1.4.13/2.0.20 から IDEA が含まれるようになった<ref name="IDEA_1.4">

` `</ref><ref name="IDEA_2.0">`GnuPG 2.0 系列 で用いられる Libgcrypt がバージョン 1.5.2 で IDEA をサポートし、これが GnuPG 2.0.20 に組み込まれたため。  `
` `</ref>`。これは、過去のコンテンツの署名検証、復号および古いPGPからGnuPGへの移行といった互換性維持のための最低限のサポートであり、既定では新しい鍵の作成における選択肢には現れない`<ref name="IDEA_1.4_2">`  `
` `</ref>`。`

[RSA](../Page/RSA暗号.md "wikilink") は 2000 年に特許が切れたため、1.0.3 から含まれるようになった<ref name="RSA">

` `</ref>`。`

また、1.4.10/2.0.12 より [Camellia](../Page/Camellia.md "wikilink") も含まれるようになった<ref name="Camellia">

` `</ref>`。`

GnuPG 2.0.26および1.4.18において対応しているアルゴリズムは以下の通りである。

  - [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")
      - [RSA](../Page/RSA暗号.md "wikilink")（1.0.3 より）
      - [ElGamal](https://ja.wikipedia.org/wiki/ElGamal暗号 "wikilink")
      - [DSA](https://ja.wikipedia.org/wiki/Digital_Signature_Algorithm "wikilink")
  - [共通鍵暗号](../Page/共通鍵暗号.md "wikilink")
      - [IDEA](https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm "wikilink")（1.4.13/2.0.20 より）
      - [3DES](../Page/トリプルDES.md "wikilink")
      - [CAST5](../Page/CAST-128.md "wikilink")
      - [Blowfish](../Page/Blowfish.md "wikilink")
      - [AES-128, AES-192, AES-256](../Page/Advanced_Encryption_Standard.md "wikilink")
      - [Twofish](../Page/Twofish.md "wikilink")
      - [Camellia Camellia-192, Camellia-256](../Page/Camellia.md "wikilink")-128,（1.4.10/2.0.12 より）
  - [暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")
      - [MD5](../Page/MD5.md "wikilink")
      - [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")
      - [RIPEMD](https://ja.wikipedia.org/wiki/RIPEMD "wikilink")-160
      - [SHA-2 SHA-384, SHA-512, SHA-224](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")56,
  - [圧縮形式](../Page/データ圧縮.md "wikilink")
      - 無圧縮
      - [ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")
      - [ZLIB](https://ja.wikipedia.org/wiki/zlib "wikilink")
      - [BZIP2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")

2.2/2.1系列では[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink") ([楕円曲線DSA](https://ja.wikipedia.org/wiki/楕円曲線DSA "wikilink") (ECDSA)、[楕円曲線ディフィー・ヘルマン鍵共有](https://ja.wikipedia.org/wiki/楕円曲線ディフィー・ヘルマン鍵共有 "wikilink") (ECDH)、[エドワーズ曲線デジタル署名アルゴリズム](https://ja.wikipedia.org/wiki/エドワーズ曲線デジタル署名アルゴリズム "wikilink") (EdDSA)) に対応する\[12\]。

## 脚注

## 外部リンク

  - [The GNU Privacy Guard - GnuPG.org](https://www.gnupg.org/)
  - [GNU Privacy Guard講座](http://gnupg.hclippr.com/)
  - [GnuPG-Mini-Howto](http://www.isbsd.com/gnupg/GPGMiniHowto.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:1999年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1999年のソフトウェア "wikilink")

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
11. 欧州および日本：2011年5月16日、アメリカ合衆国：2012年1月7日
12.