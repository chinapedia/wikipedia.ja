> この記事は[PeerCast](https://ja.wikipedia.org/wiki/PeerCast)から翻訳されています。


**PeerCast**（ピアキャスト）は、[オープンソース](../Page/オープンソース.md "wikilink")で開発されている[Peer to Peer方式の](../Page/Peer_to_Peer.md "wikilink")[ライブストリーミング](https://ja.wikipedia.org/wiki/ライブストリーミング "wikilink")配信[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。 広義にはそれを中心とした[ライブストリーミング](https://ja.wikipedia.org/wiki/ライブストリーミング "wikilink")ネットワークやコミュニティのことを指す。 略称に**ピアキャス・PeCa**などがある。主にゲーム配信や雑談配信などで利用されている。

## 概要

PeerCastは2002年にGiles Goddardによって、「誰でもラジオ放送ができるシステム」として開発された\[1\]。 ソースコードは[GPL](https://ja.wikipedia.org/wiki/GPL "wikilink")として公開され、2007年に公式サイトが閉鎖された以降も有志によってフォークされ開発が続けられた。 主なフォークには[PeerCast IM](https://osdn.jp/projects/peercast-im/)がある。 また、新たにC\#で書き直された互換クライアントである**[PeerCastStation](http://www.pecastation.org/)**がkumaryuによって公開され、開発が続けられている。

Peer to Peerの技術を利用し、配信者から閲覧者へ、その閲覧者から他の閲覧者へと[木構造のように配信する仕組み](../Page/木_\(数学\).md "wikilink")（[リレー](../Page/リレー.md "wikilink")方式）を用いている。

<table>
<tbody>
<tr class="odd">
<td><table>
<thead>
<tr class="header">
<th><p>PeerCastのストリーミング配信</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>　　　　　 配信者<br />
　　　　 ／　　　＼<br />
　閲覧者A　　閲覧者B（中継も担う）<br />
　　　　　　　　　／　　　 ＼<br />
　　　　　　 閲覧者C　　　閲覧者D</p></td>
</tr>
</tbody>
</table></td>
<td><table>
<thead>
<tr class="header">
<th><p>一般的なストリーミング配信</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>　閲覧者A　　閲覧者B<br />
　　　＼　　　／<br />
　　　　配信者<br />
　　　／　　　＼<br />
　閲覧者C　　閲覧者D</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

一般的なストリーミング配信では、閲覧者全てが配信用の[サーバ](../Page/サーバ.md "wikilink")にアクセスするため、閲覧者の需要量に応じて莫大な数のサーバや広域帯の[回線](https://ja.wikipedia.org/wiki/回線 "wikilink")が必要となるが、PeerCastでは上図のように配信者の負担は直接接続する閲覧者に対する帯域幅が確保されれば、特殊な機器を必要とせずに配信及び閲覧が可能である。一般的な[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")のファイルのコピーや移動操作やソフトウェアをインストールする知識、[ネットワークに関する各種設定の知識がある者なら手軽にストリーミング配信を行うことができる](../Page/コンピュータネットワーク.md "wikilink")。

PeerCast自体はデータの送受信機能しか備えておらず、視聴をするためには[Windows Media Playerや](../Page/Windows_Media_Player.md "wikilink")[MPlayer](../Page/MPlayer.md "wikilink")など､およびそれらに互換性のある[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")などが必要である。また、送り手として映像を配信するには[Windows Media Encoderや](https://ja.wikipedia.org/wiki/Windows_Media_Encoder "wikilink")[Open Broadcaster Softwareなどのソフトウェアで映像をストリーミング用にエンコードする必要がある](https://ja.wikipedia.org/wiki/Open_Broadcaster_Software "wikilink")。

配信されるファイル形式は[WMV・](../Page/Windows_Media_Video.md "wikilink")[flv](https://ja.wikipedia.org/wiki/FLV "wikilink") （映像向け）、[MP3](../Page/MP3.md "wikilink")・[OGG](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink") （音声向け）など配信者や配信場所により異なるため、それぞれのファイル形式を再生できるメディアプレイヤーを用意する必要がある。

最近では[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")、[ニコニコ動画](../Page/ニコニコ動画.md "wikilink")などにPeerCast配信動画が転載されるようになった。この他、[平沢進](../Page/平沢進.md "wikilink")のインタラクティブ・ライブの動画ストリーミング手段として用いられたことがある\[2\]。

## 様々な問題

### ポート開放

Peer to Peerで通信を行うため、[ルーター](../Page/ルーター.md "wikilink")を用いている環境では[ポートの開放作業が必要となる](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")。これらを行わずに配信ないし受信を行おうとすると、うまく通信ができない場合がある上、PeerCastの特性上、配信がうまく行き渡らないといった問題が発生する。

ポートを開放したにも関わらず配信及び受信できない場合は[プロバイダなどで通信規制が行われている場合がある](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。これはPeerCastが[ファイル共有](../Page/ファイル共有.md "wikilink")ソフトにも使われる[Gnutella](../Page/Gnutella.md "wikilink")を[通信プロトコル](../Page/通信プロトコル.md "wikilink")として使用しているため、規制の対象となっている可能性がある。

### フォールトトレラント性

最上流に位置する配信者から下流の閲覧者に向かうリレー形式を採用しており、PeerCast方式の番組を一つのシステムとして喩えると、配信者は元より中間の閲覧者が故障するとシステム全体に影響を与えやすい[フォールトトレラント性](https://ja.wikipedia.org/wiki/フォールトトレラント性 "wikilink")への課題がある。具体的には、リレーの上流にいる閲覧者のコンピュータの処理速度や通信速度が著しく遅い場合にはシステム全体のボトルネックになり、更に下流に位置する閲覧者への配信に影響を与える。

影響の状態としては頻繁に[バッファ](../Page/バッファ.md "wikilink")へのデータ受信待ちが発生し、その結果、映像や音声が途切れたり、下流に閲覧者を従えている閲覧者が接続を切るとリレーを受けている下流の閲覧者が巻き添えとなり、再度リレー先を見つけるまでの間は受信できない状態が起きる。

<table>
<tbody>
<tr class="odd">
<td><table>
<thead>
<tr class="header">
<th><p>閲覧者全員の配信が確立</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>　　　　配信者<br />
　　　／　　　＼<br />
　閲覧者A　　閲覧者B<br />
　　　　　　／　　 ＼<br />
　 　　閲覧者C　　 閲覧者D</p></td>
</tr>
</tbody>
</table></td>
<td><table>
<thead>
<tr class="header">
<th><p>閲覧者Bの切断により下流が途絶</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>　　　　配信者<br />
　　　／　　　＼<br />
　閲覧者A　　<del>閲覧者B</del><br />
　　　　　　／　　 ＼<br />
　 　　<del>閲覧者C</del>　　 <del>閲覧者D</del></p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

個々の閲覧者は上流から配信されたデータを一時的に蓄え、下流閲覧者に向けてデータ転送を行うため、配信元から末端に向かうにつれ時差が大きくなる性質がある。

これらの性質を理解しない閲覧者が多ければ多いほど、こうした問題へのリスクが更に高まるため、多数の閲覧者が受信している配信を長時間安定した状態で視聴するためには、PeerCastの特性を理解した上で配信者及び閲覧者が自分の直下のノードにポート未開放だったり映像をアップロードするのに十分な帯域のないクライアントが接続できないようにするなど対策が必要である。

### 著作権問題

個人配信では、テレビ放送の番組などの[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")や、手持ちの楽曲の配信などに使われていることも多いが、他者の[著作物](../Page/著作物.md "wikilink")を無断で不特定多数のリスナーに配信することを[著作権侵害](../Page/著作権侵害.md "wikilink")としている国、地域もある。

日本では、2009年9月8日、PeerCastで劇場公開前の映画を配信していた者が[著作権法](../Page/著作権法.md "wikilink")違反（[公衆送信権](../Page/公衆送信権.md "wikilink")侵害）容疑で逮捕された\[3\]。また2010年2月22日には、PeerCastで権利者に無断で映画を配信していた者が著作権法違反（公衆送信権侵害）容疑で逮捕された\[4\]。

## 註

## 外部リンク

  -
  - [PeerCastStation 公式サイト](http://www.pecastation.org/)

[Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:インターネットラジオ局](https://ja.wikipedia.org/wiki/Category:インターネットラジオ局 "wikilink")

1.
2.
3.  [日本国際映画著作権協会](https://ja.wikipedia.org/wiki/日本国際映画著作権協会 "wikilink")(JIMCA) “[公開前の洋画をネット配信、３５歳の男を逮捕。](http://www.jimca.co.jp/news/index.php?year=2009#200909080)”
4.  JIMCA “[ストリーミング配信ソフト「ピアキャスト」で、映画を無断配信し、逮捕。](http://www.jimca.co.jp/news/index.php?year=2010#201003230)”