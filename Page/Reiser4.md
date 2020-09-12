> この記事は[Reiser4](https://ja.wikipedia.org/wiki/Reiser4)から翻訳されています。


**Reiser4**（ライザーフォー）は[ReiserFS](../Page/ReiserFS.md "wikilink")ファイルシステムの後継として、[DARPAと](../Page/国防高等研究計画局.md "wikilink")[Linspire](../Page/Linspire.md "wikilink")から支援を受けた[Namesys](https://ja.wikipedia.org/wiki/Namesys "wikilink")社により[フルスクラッチで開発されたファイルシステムである](https://ja.wikipedia.org/wiki/スクラッチビルド#他分野での用語の流用 "wikilink")。

2006年当時、[ReiserFS](../Page/ReiserFS.md "wikilink")は多くのLinux[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")のデフォルトのファイルシステムとして広く採用されてたが、その後継であるReiser4は[Linux](../Page/Linux.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")のメインにマージされないまま、2006年に主要な開発者のハンス・ライザーが妻を殺害した容疑で逮捕されたことによって実質的に終了した。しかしながら、Reiser4は[アンドリュー・モートンによる](https://ja.wikipedia.org/wiki/アンドリュー・モートン_\(プログラマ\) "wikilink")「-mm」カーネルソースで動作可能であった（[2011年](../Page/2011年.md "wikilink")現在のmmツリー、mmotmツリーには含まれていない）。2006年当時のReiser4はLinuxの次世代ファイルシステムの有力な候補の一つとみなされていたにもかかわらず、Reiser4がカーネルにマージされなかった理由として、Linuxカーネル開発陣はReiser4がLinux標準[コーディングスタイル](https://ja.wikipedia.org/wiki/コーディングスタイル "wikilink")を守っていないからだと説明していたが\[1\]、[ハンス・ライザー](../Page/ハンス・ライザー.md "wikilink")は政治的な理由（カーネルの開発陣がハンス・ライザーのことを嫌っているから）であるとしていた\[2\]。

ハンス・ライザー（2008年に懲役15年が確定し、2021年に出所予定）の逮捕後、Reiser4は新機能の導入こそされなくなったものの、熱狂的支持者によって継続してメンテナンスされており、2019年にはLinux5.0に対応。

## 特徴

Reiser4の目標：

  - 柔軟なログ形式によってより効率の良い [ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")を実現する。
  - ディスクスペースや速度についてより効率よく小さなファイル群をサポートする。（[tail packingによる](https://ja.wikipedia.org/wiki/tail_packing "wikilink")）
  - たくさんのファイルがある[ディレクトリ](../Page/ディレクトリ.md "wikilink")をより高速に認識する。
  - 追加機能をプラグインとして実装できるようにするためのサポート。（特別な[メタデータ](../Page/メタデータ.md "wikilink")や[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")と[データ圧縮](../Page/データ圧縮.md "wikilink")など）
  - [allocate-on-flush](https://ja.wikipedia.org/wiki/allocate-on-flush "wikilink")により動的に最適化されたディスクレイアウトを実現する。（[XFS](../Page/XFS.md "wikilink")では遅延確保と呼ばれている）
  - データベース・トランザクションのサポート

いくつかのより進んだ特徴は[VFSのAPIがないため利用できない](../Page/仮想ファイルシステム.md "wikilink")（ユーザ定義のトランザクションなど）。

現在のところReiser4はいくつかの標準的なファイルシステムの仕様を満たせていない。オンラインリパッカーなどである（他のファイルシステムで提供されるデフラグメンテーションユーリティーに似ている）。Reiser4の開発者によるとこれから実装の予定だが、開発費用を払う人がいれば早期に実現するだろうと発言している\[3\]。

## パフォーマンス

Reiser4は[dancing treeバランス化アプローチと共にB](https://ja.wikipedia.org/wiki/dancing_tree "wikilink")\*木を採用する。メモリを圧迫するかトランザクションの完了時を除き、過疎なノードはディスクへのフラッシュまたはマージされない。システムは時間やスペースを浪費せずにファイルやディレクトリを作成することができるようになる。

2004年、Namesysにより公開された総合的なベンチマークテストでは、1キロバイトのファイル群の操作においてReiser4は本格的に競合する[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")に比べ10～15倍高速であることが示された。

Namesysのベンチマークは通常ext3に比べ通常の目的において2倍のパフォーマンスを持つと示唆している\[4\]。その他のベンチマークの結果によればReiser4は多くの他の処理では遅いことが分かる\[5\]。

## 参照

## 関連

  - [ReiserFS](../Page/ReiserFS.md "wikilink")
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")

## 外部リンク

  - [Reiser4 ホームページ](https://reiser4.wiki.kernel.org/index.php/Main_Page)
  - [Reiser4の紹介](http://www.kuro5hin.org/story/2003/8/9/172159/7912) on [kuro5hin](https://ja.wikipedia.org/wiki/kuro5hin "wikilink")
  - [Reiser4プログラマーズガイド](http://pvh.ca/trac/wiki/reiser4)
  - [Hans Reiser: Reiser4 ファイルシステム](http://www.youtube.com/watch?v=mIrMVPnxa04) [ハンス・ライザー](../Page/ハンス・ライザー.md "wikilink")自身による解説（[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")ビデオ）
  - [Reiser4はLinux Kernelに無いのか](http://wiki.kernelnewbies.org/WhyReiser4IsNotIn) at kernelnewbies.org and [Hans Reiser's response to Kernelnewbies' criticism](http://www.gossamer-threads.com/lists/engine?do=post_view_flat;post=668645;page=1;sb=post_latest_reply;so=ASC;mh=25;list=linux)
  - [Reiser4 とKernelの方針について](http://programming.linux.com/programming/06/07/31/1548201.shtml?tid=91&tid=96) （Linux.com）

[de:Reiser File System\#Reiser4](https://ja.wikipedia.org/wiki/de:Reiser_File_System#Reiser4 "wikilink")

[Category:Linuxのファイルシステム](https://ja.wikipedia.org/wiki/Category:Linuxのファイルシステム "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink")

1.
2.
3.
4.
5.