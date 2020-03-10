> この記事は[Intel 820](https://ja.wikipedia.org/wiki/Intel_820)から翻訳されています。


[Asus_P3C2000_-_Intel_FW82820-8653.jpg](https://ja.wikipedia.org/wiki/File:Asus_P3C2000_-_Intel_FW82820-8653.jpg "fig:Asus_P3C2000_-_Intel_FW82820-8653.jpg") **Intel 820**（i820）は、パフォーマンスPC向けとして1999年に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社が発表・発売した[インテル チップセットの一つ](../Page/インテル_チップセット.md "wikilink")。正式名称はIntel 820 AGP Set。開発コードはCamino（カミーノ）。

## 概要

**Intel 820**は、[Intel 440BXの後継となるパフォーマンスPC向けチップセットとして](../Page/Intel_440BX.md "wikilink")、Intel 800チップセットの2番目の製品として企画された。[1999年](../Page/1999年.md "wikilink")[9月](../Page/9月.md "wikilink")の発表予定であったが、直前に問題が見付かり発表と発売は[11月](../Page/11月.md "wikilink")に延期された。

チップセットの構成は、先行発表した同じIntel 800チップセットである[Intel 810と同様に](../Page/Intel_810.md "wikilink")、ノースブリッジとサウスブリッジを転送速度266MB/sのハブ・リンクで接続しているハブ・アーキテクチャ (Hub Architecture) による2チップ構成となっている。Intel 800チップセット以前のIntel 400チップセットは[PCIで接続されている点が大きく違う](../Page/Peripheral_Component_Interconnect.md "wikilink")。

ノースブリッジに相当するIntel 82820は[グラフィックス機能を搭載していないため](../Page/オンボードグラフィック.md "wikilink")、Intel 810のノースブリッジのGMCHとは違って、**[Memory Controller Hub](https://ja.wikipedia.org/wiki/Memory_Controller_Hub "wikilink")** (MCH) と呼称され、サウスブリッジに相当する**[I/O Controller Hub](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink")** (ICH) と呼ばれている。2000年にはICHをICH2に置き換えた**Intel 820E**が発表されている。Intel 820Eの開発コードネームはCamino 2（カミーノ2）。

最大の特徴は、インテルがPC用の次世代メモリと位置づけていた[RDRAM](../Page/RDRAM.md "wikilink")を初めて採用した点である。他にもインテルチップセットとして初めて133 MHz [FSBと](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")[AGP 2.0準拠の外部AGPサポートするなど](https://ja.wikipedia.org/wiki/AGP "wikilink")、パフォーマンスPC向けとしては意欲的な仕様となっている。

セキュリティ機能として[Pentium IIIで採用された](../Page/Pentium_III.md "wikilink")[プロセッサ シリアル ナンバーを利用した](https://ja.wikipedia.org/wiki/プロセッサ_シリアル_ナンバー "wikilink")**ランダム・ナンバ・ジェネレータ**や、管理用機能としてS0ステートでもステータスを返す**アラート オン LAN**などの新機能も搭載している。

Intel 820には、オプションとして**[Memory Translator Hub](https://ja.wikipedia.org/wiki/Memory_Translator_Hub "wikilink")** (MTH) が用意されている。これは、まだ普及していないRDRAMに量産効果がまだ効かないことでコスト高となってしまうことを緩和する措置で、これによりIntel 820でも既に普及しているPC100 [SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink")を利用することが可能となっている。 [SMP機能は](../Page/対称型マルチプロセッシング.md "wikilink")2CPUまでの対応となっている。

同時期のIntelチップセットであるIntel 810ファミリおよび[Intel 815では](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")[CPUバス](https://ja.wikipedia.org/wiki/CPUバス "wikilink")にAGTLを採用した**Tualatin**コアのPentium III・Celeronの登場に伴い、AGTL対応のB0ステッピングを出荷したが、Intel 820ファミリの普及は断念しAGTLを採用するIntel 830に移行させる措置を取ったことから、B0ステッピングは投入されずTualatinコアのサポートは行われなかった。

### 発表前のトラブル

当初、Intel 820はRIMMソケットを3本までサポートするとされており、各[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")の製造者は3本のスロットでマザーボードを設計し、製造を準備していた。しかし当初1999年春に発表と予告していたIntel 820は延期を繰り返し、9月に予告されていた正式発表直前に3本のRIMMソケットがあるIntel 820システム上で全ソケットにRDRAMモジュールを搭載した場合、Direct Rambus上の電流レベルが下がりエラー訂正不可能なレベルの[ノイズ](../Page/ノイズ.md "wikilink")が発生するという問題が発覚し、[ドタキャン](https://ja.wikipedia.org/wiki/ドタキャン "wikilink")と言われるほど急な延期となった。

この問題に対しインテルはIntel 820の問題ではなくマザーボードの設計の問題とし、RIMMソケットを2ソケットまでに制限することで回避可能であるとし、設計ガイドラインの変更などの対応で済ませた。しかし、製造済みのマザーボードを廃棄せざるを得なくなったマザーボードメーカーは不満を漏らし、一部のマザーボード製造者はマザーボードの設計ではなくRDRAMのメモリスロットを2本に制限しても同様の問題が発生するとしてIntel 820自体の問題だと指摘するなどしたが、不透明なまま原因は不問にふされ、出荷の再開と11月の正式発表が行われた。

これらの経緯により、Intel 820には正式発表の前からネガティブなイメージが付いてしまうことになった。

## MCH

MCHであるIntel 82820はメインメモリとして1GBまでのシングルチャンネルPC600/700/800のRDRAMに対応している。これによりPC100 SDRAMの800 MB/秒を大幅に上回る最大1.6 GB/秒の転送速度を実現した。サポートするRIMMソケットは2ソケットまでに制限されている。

オプションのMTHを用いることでPC100 SDRAMにも対応可能とされたが、後述のMTHの不具合により出荷後に非対応に仕様変更された。

インテルチップセットとして初めて133MHz [FSBは](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")133MHzをサポートし、また100MHz FSBにも対応している。しかし66 MHzのFSBは正式には対応していない為、発表当時は[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")の動作対象外とされていた。

Intel 810と異なりグラフィックスコアは内蔵せず、[AGP 2.0準拠のAGP](https://ja.wikipedia.org/wiki/AGP "wikilink") 4Xに対応した外部AGPをサポートする。これにより、AGPの転送速度はi440BXの533 MB/秒から倍の1.06 GB/秒に高められている。

## MTH

Intel 820をPC100 SDRAMに対応させる為のオプションとして準備されたのが、Memory Translator Hub(MTH)である。MTHをRDRAMのメモリバスに接続し信号をSDRAMのものに変換することで、Intel 820でもSDRAMを使用することが可能となっている。RDRAMとSDRAMの同時使用は不可ながら、RIMMソケットとDIMMソケットの共存も可能である。 MTHはIntel 820チップセットにオンボード搭載されるか、もしくはRIMMソケットに装着するSDRAMメモリを装着するサブボード上に搭載される形式で利用される。

しかし、MTHは発売後に高負荷時に正常に動作しない欠陥が見付かり、全製品が回収対象となった。IntelはMTHの改修を行わないことを決定し、Intel 820のオプションから削除、Intel 820の性能向上版であるIntel 820EでもMTHはオプションリストには含まれない。

### MTHのトラブル

MTHは、次世代メモリが量産効果で値下がりするまでSDRAMを代用できるようにすることでIntel 820の普及を狙ったものだったが、実際には非常に信号仕様がシビアであり、PC100 SDRAMを利用すると稼動しない・安定しないといった現象が多発していた。

さらに2000年5月10日にはMTHに高負荷がかかった場合、MTHがリセットしてしまう致命的なバグが発覚した。 これによりMTH搭載製品は全品[リコール対象となり](https://ja.wikipedia.org/wiki/リコール_\(一般製品\) "wikilink")、高価なRDRAMと組合わせるしかなくなったIntel 820の普及がさらに困難になっただけでなく、Intel 820とRDRAMの双方に多大な悪いイメージをもたらせてしまった。

## ICH

MCHに接続されるIntel 82801AAはICHと呼称され、従来のサウスブリッジ同様に[ATA](../Page/Advanced_Technology_Attachment.md "wikilink")・[USBや各種レガシコントローラを搭載する他](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[AC'97対応のサウンドコントローラやネットワークの論理層も統合している](../Page/Audio_Codec_97.md "wikilink")。この為、コーデックチップ又は物理層チップを追加するだけで、安価にサウンド/ソフトウェア[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")機能・[ネットワーク機能を](../Page/Local_Area_Network.md "wikilink")[オンボード](../Page/オンボード.md "wikilink")で実現できるようになった。これに伴いOEMメーカーがオプションのバリエーションを採用しやすくするための[AMRスロットがサポートされている](https://ja.wikipedia.org/wiki/Audio_and_Modem_Riser "wikilink")。

またIntel 820EではATA100に対応したIntel 82801BAのICH2が採用されており、AMRの後継となる[CNRスロットもサポートされている](https://ja.wikipedia.org/wiki/Communication_and_Networking_Riser "wikilink")。

## 評価と影響

Intel 820は、成功を収めたIntel 440BXチップセットの後継として、またインテルの描いた次世代PCテクノロジを具体化する製品として投入された製品であるが、結果としてインテルチップセット史上でもまれに見る大失敗に終わった。

Intel 820が失敗に終わった要因はいくつもあるが、主な理由としては以下のものが挙げられる。

  - RDRAMの高価さ
    i820の登場した99年12月時点において、PC100 SDRAMの128MBモジュールが2万円弱だったのに対し、PC800 RDRAMの128MBモジュールは5倍近い10万円弱もの高価な製品であった。ギャップを埋める存在として期待されたMTHは欠陥により全品リコールとなった為、Intel 820にはRDRAMを組合わせる選択肢しかなかった。さらにIntel 820はRIMMソケットを2ソケットまでしかサポートしない為、十分なメモリ容量と後の拡張性の両立を考えた場合、最初から高価な大容量モジュール1枚で構成する必要もあり、割高な印象をさらに強めた。
    当初インテルはIntel 820の本格普及に伴いRDRAMが量産されるようになれば、RDRAMの価格も急速に下がりし普及に弾みがつくと予測を立てていた。しかし、Intel 820の普及が進まずにRDRAMの値下がりも期待したほど進まず、この為、一方が普及しないからもう一方も普及しない、というネガティブスパイラルに陥ることになった。
  - 性能優位の乏しさ
    Intel 820が採用したRDRAMは転送速度が最大で1.6 GB/秒に達したものの、当時最新鋭のPentium IIIで採用された133 MHz FSBでさえ転送速度は1.06 GB/秒でしかなかった。そもそもRDRAMは次世代CPUのPentium 4などで利用する目的で導入されたもので、Pentium IIIではRDRAMの性能を十分に引き出すことができず、価格に見合った性能の優位性を示すことができなかった。
    RDRAMを採用したIntel 820システムはメモリ転送速度は確かに優秀であったものの、当時はPCでの[動画](../Page/動画.md "wikilink")編集などメモリ転送速度が重視される処理はまだ一般的ではなく、RDRAMの優位性は[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")上でしか評価されなかった。このため、Intel 820は圧倒的に高価なRDRAMを必要とするが性能はそれに見合わないという評価が定着することになった。
  - Intel 820自体のネガティブなイメージ
    上述の正式発表直前の[ドタキャン](https://ja.wikipedia.org/wiki/ドタキャン "wikilink")、およびMTHのリコールにより「Intel 820は安定していない・信用できない」というイメージが広がることになった。特に前世代の440BXチップセットは極めて高い評価を得ていた為、Intel 820のネガティブなイメージとのギャップが際立ち、買換えを期待されていた440BXユーザー層の買い控えや、競合他社である[VIA](https://ja.wikipedia.org/wiki/VIA "wikilink")や[SiS](https://ja.wikipedia.org/wiki/SiS "wikilink")のチップセットへの乗り換えを引き起こすことになった。

これらの要因が積み重なった結果、市場ではIntel 820に置き換わらずに旧型となった440BXを採用した新製品が発売され続け、パフォーマンス向けのPentium IIIを本来はローエンド向けのIntel 810と組合わせた機種を販売する事態となった。インテルはRDRAMの普及計画を一時的に先送りにし、成功を収めていたIntel 810を改良してPC133 SDRAMと外部AGPをサポートした[Intel 815シリーズを発表した](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")。IntelはIntel 820の代替としてPentium III用チップセットの決定版としてIntel 830の開発を決定したが、別の要因でIntel 830の発売は見送られ、市場では440BXの後継はIntel 820ではなく440BXより性能は劣る部分があるもののIntel 815ファミリであると広く認められるようになった。Intel 820はマイナーチェンジ版のIntel 820Eが発表されたもののほとんど採用されることはなく、Intel 820ファミリは終息に至った。

[2000年](../Page/2000年.md "wikilink")にインテルは[NetBurst](https://ja.wikipedia.org/wiki/NetBurst "wikilink")マイクロアーキテクチャに基づいた新CPU [Pentium 4と](../Page/Pentium_4.md "wikilink")[Xeon](../Page/Xeon.md "wikilink")を発表し、同時に発表した[Intel 850および](https://ja.wikipedia.org/wiki/Intel_850 "wikilink")[Intel 860チップセットを発表した](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_860_チップセット_ファミリ "wikilink")。RDRAMはNetBurstマイクロアーキテクチャの為に開発し導入したメモリサブシステムであるが、Pentium 4に無料でRDRAMのモジュール[RIMM](https://ja.wikipedia.org/wiki/RIMM "wikilink")を無料添付して販売するなど普及と販売を促進したが、RDRAMへの根強いネガティブイメージも一因となって失敗に終わり、インテルは莫大なコストを費やしたRDRAMの普及を断念し[DDR SDRAMがPC用次世代メモリのデファクトスタンダードとなっていくことになる](https://ja.wikipedia.org/wiki/DDR_SDRAM "wikilink")。

Intel 820の失敗はPC市場におけるRDRAMという新技術の導入の失敗と大きく重なっており、その後の新技術の導入には慎重さを重視するようになった。

## ラインナップ

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>対応FSB</p></th>
<th><p>対応メモリ</p></th>
<th><p>メモリ容量</p></th>
<th><p>MTH</p></th>
<th><p>ICH</p></th>
<th><p>ATA</p></th>
<th><p>USB</p></th>
<th><p>PCI</p></th>
<th><p>SMP</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>820</p></td>
<td><p>133/100MHz</p></td>
<td><p>PC800・PC700・PC600</p></td>
<td><p>1GB</p></td>
<td><p>オプション<br />
(後、非対応)</p></td>
<td><p>ICH</p></td>
<td><p>ATA66</p></td>
<td><p>2ポート</p></td>
<td><p>6</p></td>
<td><p>2CPUまで</p></td>
</tr>
<tr class="even">
<td><p>820E</p></td>
<td><p>133/100MHz</p></td>
<td><p>PC800・PC700・PC600</p></td>
<td><p>1GB</p></td>
<td><p>非対応</p></td>
<td><p>ICH2</p></td>
<td><p>ATA100</p></td>
<td><p>4ポート</p></td>
<td><p>6</p></td>
<td><p>2CPUまで</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
  - [チップセット](../Page/チップセット.md "wikilink")
  - [インテル チップセット](../Page/インテル_チップセット.md "wikilink")
  - [Intel 840](https://ja.wikipedia.org/wiki/Intel_840 "wikilink")
  - [Intel 815](https://ja.wikipedia.org/wiki/Intel_815 "wikilink")
  - [Intel 810](../Page/Intel_810.md "wikilink")
  - [RDRAM](../Page/RDRAM.md "wikilink")

## 外部リンク

  - [インテルプレスリリースによるi820発表](http://web.archive.org/web/20000301204902/http://www.intel.co.jp/jp/intel/pr/press99/991116.htm)（2000年3月1日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
  - [欠陥のあるメモリ・トランスレータ･ハブ搭載のマザーボードを交換](http://web.archive.org/web/20000622020141/http://www.intel.co.jp/jp/intel/pr/press2000/000511b.htm) （2000年6月22日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
  - [次期チップセットIntel 820がドタキャン。Intelは緊急事態に突入](https://pc.watch.impress.co.jp/docs/article/990927/kaigai01.htm)
  - [【820延期続報】820を変更せずマザーボード再設計で対処](http://www.nikkeibp.co.jp/archives/083/83290.html)
  - [不具合発表でMTH搭載のi820マザーボードが姿消す](https://akiba-pc.watch.impress.co.jp/hotline/20000513/etc_i820mth.html)

[Category:インテルのチップセット](https://ja.wikipedia.org/wiki/Category:インテルのチップセット "wikilink")