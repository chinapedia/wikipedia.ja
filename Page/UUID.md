> この記事は[UUID](https://ja.wikipedia.org/wiki/UUID)から翻訳されています。


**UUID**（**Universally Unique Identifier**）とは、[ソフトウェア](../Page/ソフトウェア.md "wikilink")上で[オブジェクトを一意に識別するための](../Page/オブジェクト_\(プログラミング\).md "wikilink")[識別子](../Page/識別子.md "wikilink")である。UUIDは128[ビット](../Page/ビット.md "wikilink")の数値だが、[16進法による](../Page/十六進法.md "wikilink")`550e8400-e29b-41d4-a716-446655440000`というような文字列による表現が使われることが多い。元来は[分散システム](https://ja.wikipedia.org/wiki/分散システム "wikilink")上で統制なしに作成できる識別子として設計されており、したがって将来にわたって重複や偶然の一致が起こらないという前提で用いることができる\[1\]。[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[GUID](https://ja.wikipedia.org/wiki/GUID "wikilink")は、UUIDの実装の1つと見なせる\[2\]。

## 規格

[Network Computing Systemで導入され](https://ja.wikipedia.org/wiki/:en:Network_Computing_System "wikilink")、それを[Distributed Computing Environment](../Page/Distributed_Computing_Environment.md "wikilink")（DCE）の一部として[Open Software Foundation](../Page/Open_Software_Foundation.md "wikilink")（OSF）が標準化し、「ISO/IEC 11578:1996 "Information technology -- Open Systems Interconnection -- Remote Procedure Call (RPC)"」の一部として文書化されている。また[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")はUUIDに関してを公開している。

## バリアント

UUIDには歴史的経緯から数種類のバリアント（変種）があり、現行の規格で定められているのはそのうちの1つである。16進表記をした場合に`xxxxxxxx-xxxx-xxxx-Nxxx-xxxxxxxxxxxx`のNの桁の上位ビットがバリアントを示す。現行の規格では上位2ビットが10<sub>2</sub>であることが定められているので、16進表記では8、9、A、Bのいずれかとなる。これ以外のバリアントは、規格制定以前に生成されたUUIDとの[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")、あるいは将来のために予約されている。全てが0のUUIDも、こうしたバリアントの一つである。

<table>
<thead>
<tr class="header">
<th><p>Msb0</p></th>
<th><p>Msb1</p></th>
<th><p>Msb2</p></th>
<th><p>バリアント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
<td><p>Network Computing Systemへの後方互換性のために予約</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>0</p></td>
<td><p><br />
</p></td>
<td><p>RFC4122で規格化されたバリアント</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>マイクロソフトが<a href="../Page/Component_Object_Model.md" title="wikilink">COMで用いている</a><a href="https://ja.wikipedia.org/wiki/GUID" title="wikilink">GUID</a>との後方互換性のために予約</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>将来のために予約</p></td>
</tr>
</tbody>
</table>

## バージョン

現行規格で定められているバリアントには、さらに生成方法が異なる複数の種類があり、これをバージョンと呼んでいる。16進表記をした場合に`xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx`のMの桁がバージョン（1から5）を示す。なお以降の16進表記でNの桁が小文字になっているのはバリアントの情報が含まれることを示す。

### バージョン1

もともとの生成法である、時刻と[MACアドレス](../Page/MACアドレス.md "wikilink")を利用したUUID。16進表記をすると`TTTTTTTT-TTTT-1TTT-sSSS-AAAAAAAAAAAA`のような構造になっており、それぞれタイムスタンプ（T:60ビット）、クロックシーケンス（S:14ビット＋上位2ビットが10<sub>2</sub>）、ノード（A:48ビット）からなる。

タイムスタンプはUUID生成時刻（[協定世界時](../Page/協定世界時.md "wikilink")）における1582年10月15日（[カトリック教会](https://ja.wikipedia.org/wiki/カトリック教会 "wikilink")における[グレゴリオ暦](../Page/グレゴリオ暦.md "wikilink")の実施日）0時0分からの経過時間を100ナノ秒単位で計測した数値。60ビットで3653年分の時刻を扱えるため、西暦5235年までこの方法を用いることができる。

ノードはUUIDを生成した装置を一意に示す値で、普通はネットワークカードに（通常一意に）与えられている[MACアドレス](../Page/MACアドレス.md "wikilink")を用いる。複数あるときは任意に一つを選択してよい。またMACアドレスが存在しない場合には、乱数を生成してマルチキャストビットを立てて用いることができる。

クロックシーケンスは、同一の機器で（同一のネットワークインタフェース（MACアドレス）を持ち）、かつ、時計の精度などのために同一のタイムスタンプにおいてUUIDを生成しなければならない場合に、同一のUUIDが重複しないように順次変更させて使う値である。この値はインクリメントなどで変更しなければならず、乱数列を使用してはならない。14ビットしかないので、乱数列では[誕生日パラドックスにより容易に同一のUUIDを生成し得るからである](../Page/誕生日のパラドックス.md "wikilink")。

また、機器の時刻管理や[うるう秒](https://ja.wikipedia.org/wiki/うるう秒 "wikilink")による時刻の巻き戻りのために、あるいは、時刻が進んでいる装置から遅れている装置にネットワークカードを移設したような場合にも重複が発生し得る。前者への対応として、クロックシーケンスは新しいタイムスタンプの度にリセットしたりせず、最後に生成した時の状態を保持し、継続して更新しなければならない。しかし、後者への対応は、前にそのカードを使っていた装置で生成されたクロックシーケンスを知ることは難しいため、乱数で再初期化せざるを得ない。

バージョン1のUUIDの特徴として、同じ装置で生成された事実やUUID生成の前後関係を知ることができる。しかし、MACアドレスは人為的に差し替え可能であり、必ずしもあてにはできない。

### バージョン2

[DCEシステムにおける権限](../Page/Distributed_Computing_Environment.md "wikilink")[認可を目的に設計されたもので](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink")、バージョン1のUUIDの一部を、[POSIX](../Page/POSIX.md "wikilink")のユーザーIDやグループIDで差し替えたもの。16進表記では`IIIIIIII-TTTT-2TTT-dDDD-AAAAAAAAAAAA`となり、タイムスタンプの一部とクロックシーケンスをそれぞれローカルID（I:32ビット）とローカルドメイン（D:14ビット＋上位2ビットが10<sub>2</sub>）で置き換えている。ローカルドメインはローカルIDの種類を示す値で、ユーザーIDを用いる場合には0（16進表記で8000）、グループIDを用いる場合には1（16進表記で8001）となる。\[3\]

### バージョン3/5

ドメイン名などなんらかの一意な名前（バイト列）を用いたUUIDで、ハッシュ関数として[MD5](../Page/MD5.md "wikilink")（バージョン3）または[SHA1](https://ja.wikipedia.org/wiki/SHA1 "wikilink")（バージョン5）を利用したもの。すでに一意であることがわかっている物があり、それと（事実上）1対1に対応するUUIDが必要な場合に用いられる。16進表記では`HHHHHHHH-HHHH-3HHH-hHHH-HHHHHHHHHHHH`、`HHHHHHHH-HHHH-5HHH-hHHH-HHHHHHHHHHHH`となり、そのほとんどがハッシュ値に由来する（H:122ビット）。用いる名前は[FQDN](../Page/Fully_Qualified_Domain_Name.md "wikilink")、[URL](../Page/Uniform_Resource_Locator.md "wikilink")、[X.500](../Page/X.500.md "wikilink") DNなど何でもよいが、それぞれの名前空間自体に固有のUUIDが割り当てられている必要がある。名前空間のUUID（バイト列）と名前を繋げてハッシュ値を計算し、それを名前のUUIDへと変換する。MD5の場合の変換は、128ビットのハッシュ値にバリアント (10<sub>2</sub>) とバージョン (0011<sub>2</sub>) を上書きする。SHA1は160ビットのハッシュだが、下位32ビットを切り捨て128ビットにした上で、同様にバリアント (10<sub>2</sub>) とバージョン (0101<sub>2</sub>) を上書きすることで変換する。

### バージョン4

バージョン4のUUIDは、乱数により生成される。他のUUIDと同様、バージョン4であることを示すために4ビットが使われ、バリアント（バリアント1と2に対して、それぞれ10<sub>2</sub>または110<sub>2</sub>）を示すために2または3ビットが使われる。したがって、バリアント1（つまりほとんどのUUID）では、ランダムなバージョン4のUUIDの場合、6ビットはバリアントとバージョンビットのためにあらかじめ決定されており、ランダムに生成される部分には122ビットが残されている。よって、バージョン4バリアント1のUUIDは、2<sup>122</sup>すなわち5.3（5.31[澗](../Page/澗.md "wikilink")、5.31）通り存在する。16進表記では、`RRRRRRRR-RRRR-4RRR-rRRR-RRRRRRRRRRRR`となる。バージョン4バリアント2のUUID（レガシーなGUID）の場合、バリアントに3ビットが確保されるため、UUIDの総数は半分になる。

## 使用例

有名な使用例としては、[ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")/[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")/[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")ファイルシステムのユーザースペースのツール\[4\]、[LUKS](https://ja.wikipedia.org/wiki/LUKS "wikilink")暗号パーティション、[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などがある\[5\]。これらのほとんどは、[セオドア・ツォー](https://ja.wikipedia.org/wiki/セオドア・ツォー "wikilink")によるオリジナルの実装に由来する\[6\]。

[Solaris](../Page/Solaris.md "wikilink")では、[カーネルパニック](https://ja.wikipedia.org/wiki/カーネルパニック "wikilink")が発生した場合において、[クラッシュダンプ](https://ja.wikipedia.org/wiki/クラッシュダンプ "wikilink")のデータをFault Management Eventと照合 (pairing) する目的で、実行中の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のインスタンスを特定するためにUUIDが使用されている\[7\]。

## 関連項目

  - [誕生日攻撃](https://ja.wikipedia.org/wiki/誕生日攻撃 "wikilink")
  - [Object identifier](https://ja.wikipedia.org/wiki/オブジェクト識別子 "wikilink") (OID)
  - [Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink") (URI)

## 脚注

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink")

1.  乱数に基づくUUID（UUID version 4）の場合、およそ5.3通り（\(2^{122}=5316911983139663491615228241121378304\)）存在し、正しく生成されていれば、[誕生日のパラドックス](../Page/誕生日のパラドックス.md "wikilink")によっても、2つのIDが偶然一致するまでには期待値で2<sup>61</sup>個のIDの生成が必要である。
2.  バイト列としては非互換だが16進表記は互換性がある。
3.
4.  たとえば、[e2fsprogs](https://ja.wikipedia.org/wiki/e2fsprogs "wikilink")はが提供する *libuuid* を使用している。
5.  [gen_uuid.c in Apple's Libc-391, corresponding to Mac OS X 10.4](https://opensource.apple.com/source/Libc/Libc-391/uuid/uuidsrc/gen_uuid.c)
6.
7.