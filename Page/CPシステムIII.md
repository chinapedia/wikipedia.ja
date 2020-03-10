> この記事は[CPIII](https://ja.wikipedia.org/wiki/CPIII)から翻訳されています。


**CPシステムIII**（シーピーシステム スリー）とは、[1996年](../Page/1996年.md "wikilink")に『[ウォーザード](https://ja.wikipedia.org/wiki/ウォーザード "wikilink")』と共に出荷された[カプコン](https://ja.wikipedia.org/wiki/カプコン "wikilink")開発の[アーケードゲーム基板](https://ja.wikipedia.org/wiki/アーケードゲーム基板 "wikilink")である。[2018年](../Page/2018年.md "wikilink")現在、この基板がカプコンの開発した最後の[アーケードゲーム](../Page/アーケードゲーム.md "wikilink")用[システム基板](https://ja.wikipedia.org/wiki/システム基板 "wikilink")となっている。日本国外を中心に**CPS-3**と略称されることがある（以降、記事中ではこの略称を用いる）。

## 概要

本機は前機種にあたる[CPシステムII](../Page/CPシステムII.md "wikilink")と比べてスペック的に高い性能を備えており、拡大縮小やフェードイン・フェードアウトなどの各種エフェクト機能もハード側で実装された。この時代の2D[格闘ゲームにおいては](../Page/対戦型格闘ゲーム.md "wikilink")、本機の『[ストリートファイターIII](https://ja.wikipedia.org/wiki/ストリートファイターIII "wikilink")』などで見られる滑らかで流れるような[アニメーション](../Page/アニメーション.md "wikilink")は、当時の他社のタイトルではほとんど見られない表現であった。こういった映像表現に驚愕した当時の格闘ゲームファンたちは「この基板は『ストIII』製作のために設計したのではないか？」と考察したほどだったとも言われている。

## ソフト供給形態

本機CPS-3が他機種とは大きく異なる特徴には、ソフトの供給形態と[セキュリティに関する仕様にある](../Page/コンピュータセキュリティ.md "wikilink")。CPS-3の構成とゲームの導入手順は以下通り。

  - ゲーム[CD-ROM](../Page/コンパクトディスク.md "wikilink")・CD-ROMドライブ
    CD-ROMにはゲーム本体の内容が[暗号](../Page/暗号.md "wikilink")化されて格納されている。特殊[フォーマットではないので普通に](../Page/ファイルフォーマット.md "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) でも読み込むことが可能で、中にはゲームデータや書き替え用画面の[ビットマップ画像](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")が入っている。CD-ROMドライブは[松下寿電子工業製の当時流通していた普通の](https://ja.wikipedia.org/wiki/PHCホールディングス "wikilink")[SCSI対応型でありPCへの流用も可能](../Page/Small_Computer_System_Interface.md "wikilink")。

<!-- end list -->

  - セキュリティ・[カートリッジ](../Page/ロムカセット.md "wikilink")
    ゲーム内容を[復号](https://ja.wikipedia.org/wiki/復号 "wikilink")するための[チップと](../Page/集積回路.md "wikilink")、ゲーム[BIOSが納められている](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。復号チップは[SRAMに](../Page/Static_Random_Access_Memory.md "wikilink")[バッテリーバックアップ](../Page/バッテリーバックアップ.md "wikilink")で復号鍵を保持する仕様。このCPS-3のセキュリティ・カートリッジは各ゲームごとに用意されており、いかなる種類の改竄にも非常に敏感に反応し、もし試みれば復号鍵は消去されカートリッジは用をなさなくなる。

<!-- end list -->

  - フラッシュメモリへのゲームデータの書き込み
    初期状態のCPS-3へ電源が入れられると、画面中央にCAPCOMのロゴが表示され接続のCD-ROMドライブにCD-ROMをセットするように促される。ドライブ側にCD-ROMをセット後、1Pのショット1を押すと書き込むゲームのタイトルが表示され、CD-ROM側よりゲームデータが[SIMM](../Page/SIMM.md "wikilink")フラッシュメモリへの書き込み作業が始まる。
    この間、画面にはデータの書き込みの進行状況のバーが表示され、データの書き込み作業が終わるまでは何もできないが、データの進行状況に応じてだんだん画面がモノクロからカラーへと色が付いてくるといった演出がある。なお、データの書き込み時間はゲームにより異なり、『ストリートファイターIII』のデータ書き込み場合は約20数分を要する。

<!-- end list -->

  - ゲームの起動
    データの書き込み終了後は、書き込まれたデータがセキュリティ・カートリッジ内のチップで復号されゲームが起動する。前述のデータの書き込みは導入時のみ必要な作業であり、SIMM側に書き込まれたデータはそのまま記録され次回の起動時はすぐにゲームが立ち上がり稼働状態となる。なお、SIMM側に書き込まれたデータとセットされたセキュリティ・カートリッジのゲームが違う場合は自動的に書き替えモードへ移行する。

<!-- end list -->

  - リリース後の評価
    CPS-3は人気タイトルはあったものの商業的には成功した部類のシステム基板とは言えず、このシステム用のゲームは全部で6タイトルが制作されただけである。CPS-3には、機械的・電気的な衝撃に弱く故障しやすいという欠点があり、オペレータたちは特にこれを敬遠した。また、セキュリティ・カートリッジ内の[電池](../Page/電池.md "wikilink")が切れるとゲームが動作しなくなるうえ、その交換費用を所有者側で負担しなければならなかった。さらに高性能とはいえ2Dグラフィックのみにしか対応しておらず、当時は多くのゲームが3D[ポリゴン](../Page/ポリゴン.md "wikilink")対応のハードウェアを念頭に開発されていたという背景もあったことからこのような評価になった。また、他のシステム基板と比べても高価であり、CPS-3用の[プログラミングはかなり難しかったとも噂されている](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。

<!-- end list -->

  - サポートの終了
    部品調達難に伴い、[2015年](../Page/2015年.md "wikilink")3月31日（カプコンサービスセンター2015年3月14日到着分）をもって基板自体の修理サポートが終了した\[1\]。継続されていたセキュリティ・カートリッジの電池交換も、カプコンサービスセンターから[セガ・ロジスティクスサービス](https://ja.wikipedia.org/wiki/セガ・ロジスティクスサービス "wikilink")へのアーケードゲームの修理サポート業務移管に伴い、[2019年](../Page/2019年.md "wikilink")2月28日（カプコンサービスセンター2019年2月27日到着分）をもって終了した\[2\]\[3\]。これに伴い、基板自体が故障したり、セキュリティ・カートリッジの電池が切れた場合は完全に稼働不可となった（セガ・ロジスティクスサービスによるメーカーサポートも受けられない）。

## 仕様

  - メイン[CPU](../Page/CPU.md "wikilink")：[日立](../Page/日立製作所.md "wikilink") [SH-2](https://ja.wikipedia.org/wiki/SH-2_\(プロセッサ\) "wikilink")（HD6417099）@ 20MHz（MAX 25MHz）
  - 記憶装置
      - [SCSI](../Page/Small_Computer_System_Interface.md "wikilink") [CD-ROM](../Page/CD-ROM.md "wikilink")ドライブ（松下寿電子工業製）
      - [RAM](../Page/Random_Access_Memory.md "wikilink") (variable amount)
      - SIMM[フラッシュROM](../Page/フラッシュメモリ.md "wikilink")：8×16MB

<!-- end list -->

  - サウンドチップ：16-チャンネル 8-bit サンプル プレイヤー、ステレオ
  - 最大同時発色数：32,768色（15-bitカラー、555RGB）

<!-- end list -->

  - 解像度：384×224
  - BG拡大縮小
  - スプライト拡大縮小
  - ラインスクロール
  - ラインズーム
  - フェードイン・フェードアウト
  - 半透明
  - シャドウ

## 作品リスト

| リリース日    | 国内版タイトル                                                                         | 海外版タイトル                                              |
| -------- | ------------------------------------------------------------------------------- | ---------------------------------------------------- |
| 1996年12月 | [ウォーザード](https://ja.wikipedia.org/wiki/ウォーザード "wikilink")                       | Red Earth                                            |
| 1997年2月  | [ストリートファイターIII](https://ja.wikipedia.org/wiki/ストリートファイターIII "wikilink")         | Street Fighter III - New Generation                  |
| 1997年10月 | ストリートファイターIII 2nd Impact                                                        | Street Fighter III, 2nd Impact: Giant Attack         |
| 1998年12月 | [ジョジョの奇妙な冒険](../Page/ジョジョの奇妙な冒険_\(対戦型格闘ゲーム\).md "wikilink")                     | JoJo's Venture                                       |
| 1999年5月  | ストリートファイターIII 3rd Strike                                                        | Street Fighter III, 3rd Strike: Fight for the Future |
| 1999年9月  | [ジョジョの奇妙な冒険 未来への遺産](https://ja.wikipedia.org/wiki/ジョジョの奇妙な冒険_未来への遺産 "wikilink") | JoJo's Bizarre Adventure                             |

※全て開発・販売ともカプコン

## 脚注

<references />

## 関連項目

  - [CPシステム](../Page/CPシステム.md "wikilink")
  - [CPシステムII](../Page/CPシステムII.md "wikilink")

## 外部リンク

  - [CPS-3 at System16: The Arcade Museum](http://www.system16.com/capcom/hrdw_cps3.html)

[Category:カプコンのアーケードゲーム基板](https://ja.wikipedia.org/wiki/Category:カプコンのアーケードゲーム基板 "wikilink")

1.  [弊社基板製品保守サービス業務終了のご案内](http://www.capcom.co.jp/arcade/news/operator/20140930.html) カプコン 2014年9月30日
2.  [弊社製品のサービス対応終了に関するご案内](http://www.capcom.co.jp/arcade/news/operator/201811.html)カプコン 2018年11月12日
3.  [業務用アミューズメント機器のサービス業務移管スケジュールに関するお知らせ](http://www.capcom.co.jp/arcade/news/operator/20190306.html)カプコン 2019年3月4日