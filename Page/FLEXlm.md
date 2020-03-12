> この記事は[FLEXlm](https://ja.wikipedia.org/wiki/FLEXlm)から翻訳されています。


**FLEXlm**（フレックスエルエム）は、[ソフトウェア](../Page/ソフトウェア.md "wikilink")のライセンスを管理するソフトウェアである。

[ネットワーク経由で複数のユーザ](../Page/コンピュータネットワーク.md "wikilink")、複数種のソフトウェアを管理する機能がある。米国Globetrotter社によって[1988年](../Page/1988年.md "wikilink")に開発され現在は[Macrovision](https://ja.wikipedia.org/wiki/Macrovision "wikilink")社の製品となっている。なおMacrovisionは、FLEXnet Publisher と改称している。米Macrovision Solutions Corporation（マクロヴィジョン）は2009年7月17日、社名を「Rovi Corporation（ロヴィ コーポレーション）」に正式に変更したことを発表した。

ここでいう[ライセンス](../Page/ライセンス.md "wikilink")とはユーザがソフトウェアベンダーから購入や借用したソフトウェアの使用権のことであり、FLEXlmはそのソフトを実際に実行する際の可否を自動管理するものである。ユーザに対してはそのソフトウェアベンダーの製品に付随して出荷される場合が多く、通常、前記Macrovisionから直接入手の必要はない。

FLEXlmにはソフトウェア利用を特定の[マシンに固定するノードロック形式と利用マシンを限定しないフローティング形式がある](../Page/コンピュータ.md "wikilink")。両者の混在も可能である。 フローティング形式はネットワークライセンスとも呼ばれネットワークを通じてライセンスの配布が行われる。この場合、その管理を行うライセンスサーバとなるマシンが必要となる。

動作としてはユーザ側があるソフトを起動しようとすると自動的にライセンスサーバに問い合わせを行い、妥当であればサーバはライセンスを貸出す(check-out)操作を行い、ユーザのソフトの起動を許可する。ユーザが使用を終われば返却(check-in)操作が行われる。ユーザの要求に対しソフトの種類が異なる場合や規定のライセンス数を超えている場合などの場合はcheck-outを行なわず、ユーザはソフトを起動できない。 ネットワークは特に[LANに限定されるものではなく](../Page/Local_Area_Network.md "wikilink")[インターネット](../Page/インターネット.md "wikilink")経由や設定によっては[ファイアウォール](../Page/ファイアウォール.md "wikilink")経由でのライセンス配布も可能である。

FLEXlm自体はサーバで実行されるlmgrdという[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")、特定のベンダー固有のベンダーデーモン、それに付随するユーティリティ群からなっている。lmgrdはひとつで複数の異なるベンダーの管理も行える。ライセンスサーバは通常1台であるが、3台での冗長構成をとることもでき、その場合3台のうち1台が故障しても継続的にライセンス配布が可能である。

管理されるソフトウェアはライセンスファイルあるいはkeyと呼ばれるテキストファイルに条件が記述される。内容は対象ソフトウェアの名前、ライセンスの有効期間、ライセンス数、そして暗号文字列などからなる。それらのどこかをユーザが勝手に書き換えるとライセンスは無効となる。またファイルの冒頭ではサーバを特定する番号(hostid)や[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")のポート番号も記載される。このポート番号についてはユーザが変更可能である。FLEXlmでは（特にサーバ）は[UNIX](../Page/UNIX.md "wikilink")系のマシンで使われることが多いがPCでも可能である。PCの場合hostidは[ネットワークカード](../Page/ネットワークカード.md "wikilink")の[MACアドレス](../Page/MACアドレス.md "wikilink")が用いられる。ノードロックの場合はサーバは必要なくこのライセンスファイルのみでよい。

適用例としては[EDA](https://ja.wikipedia.org/wiki/EDA "wikilink")分野の各社のソフトウェアでFLEXlmが標準的に採用されている。

## 関連項目

  - [コピーガード](../Page/コピーガード.md "wikilink")

## 外部リンク

  - [Software Licensing](https://www.flexerasoftware.com/monetize/products/flexnet-licensing.html) - [Flexera Software](http://www.flexerasoftware.jp/)

[Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink")