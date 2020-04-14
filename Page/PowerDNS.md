> この記事は[PowerDNS](https://ja.wikipedia.org/wiki/PowerDNS)から翻訳されています。


**PowerDNS** は[DNSサーバ](../Page/DNSサーバ.md "wikilink")で、 [C++](../Page/C++.md "wikilink")で記述され、 [GPLの下でライセンスされている](../Page/GNU_General_Public_License.md "wikilink")。 ほとんどの[Unix系OSで実行される](../Page/UNIX.md "wikilink")。 PowerDNSは、単純な[BIND](../Page/BIND.md "wikilink")スタイルのゾーンファイルから[リレーショナルデータベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink") \[1\]や[負荷分散](../Page/サーバロードバランス.md "wikilink") / [フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink") [アルゴリズム](../Page/アルゴリズム.md "wikilink")に至るまで、さまざまな*バックエンドを*備えている。DNS [リゾルバは別のプログラムとして提供される](../Page/Domain_Name_System.md "wikilink")。

## 歴史

PowerDNS の開発は1999年に始まり、当初は商用のプロプライエタリ製品だった。 2002年11月、ソースコードはオープンソースGPL v2ライセンスの下で公開された。 \[2\] \[3\]

## 特徴

PowerDNS [Authoritative Server](../Page/DNSサーバ.md "wikilink")(**pdns_server**)は、単一のコアと、 [マルチスレッドを実行する複数の](../Page/スレッド_\(コンピュータ\).md "wikilink")[動的にロード可能な](../Page/ライブラリ.md "wikilink") [バックエンドで構成される](../Page/フロントエンド.md "wikilink")。コアはすべてのパケット処理とDNSインテリジェンスを処理し、1つ以上のバックエンドは任意の[ストレージ方法を使用して](../Page/記憶装置.md "wikilink")[DNSレコードを配信する](../Page/Domain_Name_System.md "wikilink")。

[ゾーン転送と更新通知がサポートされており](https://ja.wikipedia.org/wiki/DNSゾーン転送 "wikilink")、プロセスは*非特権*および*[chrootedで](../Page/Chroot.md "wikilink")*実行できる。 クエリ処理を高速化するために、さまざまな*[キャッシュ](../Page/DNSサーバ.md "wikilink")*が維持される。 *実行時制御*は**pdns_control**コマンドを介して利用する。これにより、個別のゾーンのリロード、キャッシュパージ、ゾーン通知、および[マルチルータートラフィックグラファー](https://ja.wikipedia.org/wiki/MRTG "wikilink") / rrdtool 形式の[統計のダンプが可能になる](../Page/統計学.md "wikilink")。 オプションのビルトイン[Webサーバ](../Page/Webサーバ.md "wikilink")からリアルタイム情報を取得することもできる 。

PowerDNS の管理インターフェイスを作成する独立したプロジェクトが多数ある。

### DNSSEC

PowerDNS [Authoritative Serverは](../Page/DNSサーバ.md "wikilink")、バージョン3.0の時点で[DNSSECをサポートしている](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")。 事前に署名されたゾーンを提供できるが、オンライン署名とキー管理を実行することもできる。これには比較的簡単であるという利点があるが、サーバー自体に暗号化キー情報が存在するという欠点がある(例えば、 HSM で使用されない場合のHTTPSサーバにも当てはまります)。

## リゾルバ

PowerDNS Recursor (**pdns_recursor** \[4\])は、個別のプロセスとして実行される*解決[DNSサーバ](../Page/DNSサーバ.md "wikilink")*である。

PowerDNS のこの部分はシングルスレッドだが、 [BoostとMTaskerライブラリ](../Page/Boost_C++ライブラリ.md "wikilink")\[5\]を使用して、マルチスレッドであるかのように記述される\[6\]これは単純な[AOL](https://ja.wikipedia.org/wiki/協調マルチタスクライブラリです。_スタンドアロンパッケージとしても利用できる。_pdns_recursor_を単独で実行することは権限のあるコンポーネントよりも効率的であるため、単にキャッシング/再帰/ネームサービスを提供することが目的であれば、pdns_recursorのゲートキーパーとしてpdns_serverプロセスを実行する必要ない。_2007年現在、Recursor_は、[[AOL "wikilink")、[Shaw Cable](https://ja.wikipedia.org/wiki/ショー・コミュニケーションズ "wikilink")、Neuf Cegetel 等、世界最大の[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")のいくつかで使用されている。

[DNSSEC](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink") 検証のサポートは、バージョン4.0の**pdns_recursor** に追加された。

## 参照

  - DNSサーバーソフトウェアの比較

## 参照資料

## 外部リンク

  - [公式ホームページ](https://www.powerdns.com/)

  -
[Category:DNSソフトウェア](https://ja.wikipedia.org/wiki/Category:DNSソフトウェア "wikilink")

1.
2.
3.
4.
5.  [MTasker](http://ds9a.nl/mtasker/)
6.  [MTasker](http://ds9a.nl/mtasker/)