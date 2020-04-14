> この記事は[Tera Term](https://ja.wikipedia.org/wiki/Tera_Term)から翻訳されています。


**Tera Term**（テラターム）は、寺西 高（てらにし たかし）により開発されたリモートログオン[クライアントである](../Page/クライアント_\(コンピュータ\).md "wikilink")。現在では**TeraTerm Project**により[オープンソース](../Page/オープンソース.md "wikilink")（[修正BSDライセンス](../Page/BSDライセンス.md "wikilink")）として開発されている。

[SSH](../Page/Secure_Shell.md "wikilink")・[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")・[シリアルの各](../Page/シリアルポート.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")に対応し、[Microsoft Windowsで使用できる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 沿革

### オリジナルの開発・公開

物理学者の寺西高によるオリジナルは、1994年から1998年にかけて開発された。 [16ビット](../Page/16ビット.md "wikilink")版の**Tera Term**と[32ビット](../Page/32ビット.md "wikilink")版の**Tera Term Pro**が有り（以降では明記しない限りは16ビット版と32ビット版を明確に区別せずに**Tera Term**と記述する）、telnetによる[リモートホスト](../Page/リモートホスト.md "wikilink")への接続と、シリアルポートでの接続を可能とし、[マクロを備えているのが特徴であった](../Page/マクロ言語.md "wikilink")。

[XMODEM](../Page/XMODEM.md "wikilink")や[ZMODEM](https://ja.wikipedia.org/wiki/ZMODEM "wikilink")などの[バイナリ転送プロトコル](../Page/バイナリ転送プロトコル.md "wikilink")もサポートしており、[パソコン通信](../Page/パソコン通信.md "wikilink")や[UNIX](../Page/UNIX.md "wikilink")への[ログイン](https://ja.wikipedia.org/wiki/ログイン "wikilink")に好く使われていた。 [組み込み分野では](../Page/組み込みシステム.md "wikilink")[ハードウェア](../Page/ハードウェア.md "wikilink")に[シリアルポート](../Page/シリアルポート.md "wikilink")で接続し、機器の試験のためにマクロ機能が利用されることも多かった。

また、Robert O’Callahanによる**TTSSH**(An SSH Extension to Teraterm)を[プラグイン](../Page/プラグイン.md "wikilink")として組み込むことで、**Tera Term**に拠るSSH1接続が可能となっていた。

この**Tera Term**の最終バージョンは2.3で、対応[OSは](../Page/オペレーティングシステム.md "wikilink") [Microsoft Windows NTおよび](../Page/Microsoft_Windows_NT.md "wikilink")[Microsoft Windows 95である](../Page/Microsoft_Windows_95.md "wikilink")。

「オリジナルの」**Tera Term**は、1990年代のWindows向け[フリーウェア](../Page/フリーウェア.md "wikilink")としては、珍しく[ソースコード](../Page/ソースコード.md "wikilink")が公開されている。しかし、ソースコードを変更した[バイナリ](../Page/バイナリ.md "wikilink")を再配布するには原作者の許可が必要とされていて、[Open Source Initiativeに拠る](../Page/Open_Source_Initiative.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の定義には厳密には合致しない。 なお、**TTSSH**は当初からオープンソース[ライセンス](../Page/ソフトウェアライセンス.md "wikilink")（BSDライセンス）で公開されている。

### 派生版の登場

ソースコードが公開されているため、その後に[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応版・[ローカライズ版](../Page/国際化と地域化.md "wikilink")・[プロキシ](../Page/プロキシ.md "wikilink")対応版・半透明化に対応した版などの派生版が登場した。 しかし、主開発者が不在であることや派生版を再配布するためには原作者の許可が必要だったことなどを理由として、**Tera Term**の開発を第三者が引き継ぐことが難しい状況が続いた。

当時において、[セキュリティに関する需要が高まっていく中で](../Page/コンピュータセキュリティ.md "wikilink")、セキュリティ上の脆弱性があるとされているtelnetやSSH1は利用されなくなっていった。 当時は**TTSSH**がSSH2に対応しておらず、また、SSH2に対応していた派生版としてはAyera Technologiesによる**TeraTerm Pro Web**が有るがソースコードが(現在においても)開示されていないため、[PuTTY](../Page/PuTTY.md "wikilink")等に[ユーザー](https://ja.wikipedia.org/wiki/ユーザー "wikilink")を奪われていった。

### SSH2対応とオープンソース化

[平田豊](https://ja.wikipedia.org/wiki/平田豊_\(ソフトウェア開発者、ライター\) "wikilink")\[1\]を中心とするTeraTerm Projectによって、2004年3月に**Tera Term**への[パッチ](../Page/パッチ.md "wikilink")という形態で[UTF-8](../Page/UTF-8.md "wikilink")サポート版が作成され、同年8月にはSSH2に対応した**TTSSH**が[ベータ版](../Page/ベータ版.md "wikilink")として公開された。

同年9月に、寺西高に連絡が取れて、TeraTerm Projectが正式な開発とバイナリ再配布の許可を取得した。 更に、修正BSDライセンスの下で、**TTSSH2**を取り込んで**UTF-8 TeraTerm Pro with TTSSH2**としてオープンソース化された。

後に、インストーラーの採用で関連ツールを同時にインストールされるように改良され、2008年6月にはオリジナルと同じく**Tera Term**に改称された\[2\]。

バージョン4.xx以降では、UTF-8とSSH2対応を主軸とし、派生版の機能を取り込んだ開発を目的とする\[3\]。

現在では、**Tera Term**は(そのユーザーを奪った)PuTTYを[リンク](../Page/リンケージエディタ.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")として用いている\[4\]。また、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")にではなく[アメリカに拠点を置く](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[コミュニティも在る](../Page/インターネットコミュニティ.md "wikilink")\[5\]。

## 注釈

<references />

## 関連項目

  - [Secure Shell](../Page/Secure_Shell.md "wikilink")

      - [OpenSSH](../Page/OpenSSH.md "wikilink")
      - [WinSCP](../Page/WinSCP.md "wikilink")
      - [RLogin](https://ja.wikipedia.org/wiki/RLogin "wikilink")
      - [PuTTY](../Page/PuTTY.md "wikilink")
      - [Poderosa](../Page/Poderosa.md "wikilink")

  -
  - [Telnet](../Page/Telnet.md "wikilink")

  - [端末エミュレータ](../Page/端末エミュレータ.md "wikilink")

  - [XMODEM](../Page/XMODEM.md "wikilink")

  - [ZMODEM](https://ja.wikipedia.org/wiki/ZMODEM "wikilink")

  - [Kermit](../Page/カーミット_\(プロトコル\).md "wikilink")

## 外部リンク

  - [Tera Term Open Source Project](https://ttssh2.osdn.jp/index.html.ja)

[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1994年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1994年のソフトウェア "wikilink") [Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink") [Category:telnet](https://ja.wikipedia.org/wiki/Category:telnet "wikilink")

1.
2.  この**Tera Term**は、オリジナルの16ビット版**Tera Term**と同名だが、同32ビット版**Tera Term Pro**の後継である。
3.
4.
5.