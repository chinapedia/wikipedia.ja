> この記事は[WireGuard](https://ja.wikipedia.org/wiki/WireGuard)から翻訳されています。


**WireGuard**は、[フリーかつオープンソースの](https://ja.wikipedia.org/wiki/FLOSS "wikilink")[ルーティング](../Page/ルーティング.md "wikilink")又は[ブリッジで安全な](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")接続を作成するための技術である[Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink") (VPN) の実装であり、[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")及び[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")内の[モジュールとして実行され](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink")、[IPsec](../Page/IPsec.md "wikilink")や[OpenVPN](../Page/OpenVPN.md "wikilink")よりも優れた性能を目指している\[1\]。WireGuardはJason A. Donenfeldによって書かれ、[GNU GPL v2の下で配布されている](../Page/GNU_General_Public_License.md "wikilink")\[2\]。

## 特徴

WireGuardは単純で非常に効果的なVPNを提供することを目指している。[Ars Technicaのレビューによると](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink")、OpenVPNやIPsecなどの一般的なVPN技術は、多くの場合セットアップが困難であり、簡単に切断され、再接続のネゴシエーションにかなりの時間を要し、古い暗号方式を使用しており、[ソースコード](../Page/ソースコード.md "wikilink")が比較的大規模であることから[バグ](../Page/バグ.md "wikilink")の発見が困難になっていると述べている\[3\]。

WireGuardの設計ではこれらの問題を軽減し、[トンネルのセキュリティを強化し](../Page/トンネリング.md "wikilink")、デフォルトで管理しやすくしている。暗号パッケージのバージョン管理を使用することによって、その時点で最も安全と考えられる暗号方式に焦点を当てており、更に、コードベースは約4,000行となり、が容易である。Ars Technicaはテストにおいて、代替と比較してWireGuardは安定したトンネルの作成が容易であると報告し、WireGuardの「実用的な」な即時再接続と比較して、代替の長い再接続の遅延に「戻ることは難しい」とコメントした\[4\]。

## プロトコル

WireGuardはには[Curve25519](https://ja.wikipedia.org/wiki/Curve25519 "wikilink")、暗号化には[ChaCha20](https://ja.wikipedia.org/wiki/ChaCha20 "wikilink")、には[Poly1305](https://ja.wikipedia.org/wiki/Poly1305 "wikilink")、ハッシュテーブル鍵には、[ハッシュには](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")[BLAKE2s](https://ja.wikipedia.org/wiki/BLAKE2s "wikilink")を利用する\[5\]。[ネットワーク層](../Page/ネットワーク層.md "wikilink")の[IPv4](../Page/IPv4.md "wikilink")及び[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の両方に対応し、及び ([カプセル化](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")) にも対応している\[6\]。

、[フランス国立情報学自動制御研究所](../Page/フランス国立情報学自動制御研究所.md "wikilink") (INRIA) の研究者は、 を使用して作成されたプロトコルのマシンチェック済み証明を公開した\[7\]。

## 歴史

コードベースの最初期のスナップショットはから存在する\[8\]。WireGuardの初期の採用者はVPNサービスプロバイダの\[9\]、AzireVPN\[10\]、IVPN\[11\]及びcryptostorm\[12\]であった。WireGuardはMullvad、、IVPN及びから寄付を受け取った\[13\]。

の時点で、WireGuardの開発者はソースコードとプロトコルを実験的なものとして扱うことを推奨しており、発見される可能性のある脆弱性のと互換性の有る安定版が未だリリースされていないことを注意した\[14\]\[15\]。

、Linuxのネットワーキングスタックの主要メンテナであるDavid Millerは、今後のカーネルのリリースにWireGuardを含めるために、"net-next" メンテナツリーにWireGuardのパッチを受け入れた\[16\]\[17\]\[18\]。に[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はDavid Millerの"net-next" ツリーを[マージし](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理システム\) "wikilink")、WireGuardがメインラインLinuxカーネルツリーに統合された\[19\]。

## 反応

[オレゴン州](../Page/オレゴン州.md "wikilink")選出の[上院議員の](../Page/アメリカ合衆国上院.md "wikilink")は、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink") (NIST) にIPsecやOpenVPNなどの既存の技術の代替としてWireGuardを評価することを推奨している\[20\]。

## 実装

WireGuardプロトコルの実装:

  - Donenfeldによる[Cと](../Page/C言語.md "wikilink")[Goで書かれた初期実装](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")\[21\]。
  - [Cloudflare](https://ja.wikipedia.org/wiki/Cloudflare "wikilink")の[Rustで書かれた](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")実装である*BoringTun*\[22\]\[23\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - [SSH](../Page/Secure_Shell.md "wikilink")

## 外部リンク

  -
  -
[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink") [Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink") [Category:Linuxのソフトウェア](https://ja.wikipedia.org/wiki/Category:Linuxのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

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