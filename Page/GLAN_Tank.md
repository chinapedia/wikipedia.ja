> この記事は[GLAN Tank](https://ja.wikipedia.org/wiki/GLAN_Tank)から翻訳されています。


**GLAN Tank** (SOTO-HDLGW) は、[挑戦者](https://ja.wikipedia.org/wiki/挑戦者 "wikilink")が2006年1月に出荷開始した、『スパニング・ミラーリング対応 ストリーミングサーバ組み立てキット』である。 [Glantank.jpg](https://ja.wikipedia.org/wiki/File:Glantank.jpg "fig:Glantank.jpg")

筐体内に電源と制御基板が組み込まれた状態で販売されており、製品に[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")ドライブは含まれていないため、購入者が別途入手して組み込む必要がある。 ハードディスクドライブは、二台まで内蔵でき、基板には、セカンダリポートの空きランドが存在するが、ドライブはプライマリポートの[マスター/スレーブ](https://ja.wikipedia.org/wiki/マスター/スレーブ "wikilink")として接続される事になる。

位置づけとしては、[LAN TankのGbE対応版であるが](../Page/LAN_Tank.md "wikilink")、実際には筐体の外観と、初期ファームウェアに実装されている機能が類似している程度しか共通点は無い。 ハードウェアとしては、別物の基板であるため別機種とも言える。 LAN Tankとの比較した場合の相違点としては、CPUの変更、[USBポートが](../Page/ユニバーサル・シリアル・バス.md "wikilink")2ポート追加、電圧ブザーの追加の他、電源スイッチの挙動が、スイッチがOnの状態で給電された場合、Onになるように変更されている。 添付品については、エンブレムの変更、整流用の樹脂板が追加され、CD-ROMについては二枚組になった。 また、カタログ上は、HDDのスピンオフと同期でファンコントロールが行えるような表記になっていたが、それは事実ではなく、CPLDに対してコマンドを送ることでのみON、OFFのみであるが、制御が可能になっている。ドライバのソースこそ公開されなかったものの、開発者の働きかけにより、そのレジスタ仕様は別途公開された。 ファームウェアの変更点としては、ARM用のDebian GNU/Linuxベースに変更され、パッケージがそのまま利用可能になった他、カーネルが2.6系へ変更され、akaDAVから、Apache2/mod_davへソフトウェアが変更になっている。それに伴い、ftpサーバー、ポート切り替え、Web公開機能は廃止された。

搭載CPUのマイナーさから、簡単にコンパイルが通らない、素直に動作しないなど、[玄箱](https://ja.wikipedia.org/wiki/玄箱 "wikilink")よりもユーザーを選び、[ツンデレ](https://ja.wikipedia.org/wiki/ツンデレ "wikilink")仕様と評された[LAN Tankに対し](../Page/LAN_Tank.md "wikilink")、素直にARMの資産が使えるこの製品は従順仕様とも言われる。 動作クロックの向上とGbE対応により概ねパフォーマンスは向上しているが、FPUが存在しないため、実数演算を伴うソフトウェアの実行は苦手である。

インストールはPC/AT互換機でインストーラを用いてHDDへ起動イメージを書き込むのは前作も同じであるが、今回は、PC側で構築する構成を指定の上、ブートシステムとインストーラを転送し、GLAN Tank側で自動的にそれに基づき攻勢するようになった。 PC側でのインストーラは「MAKAI(MAKe Again Iso-image)」というディストリビューションがベースになっており、HDD上の実行環境をROM化し、CD-ROMからLiveCDとして利用できるように作られた物である。GLAN Tankのインストーラでは、各種ライセンスなどの表示と、HDDに対して、初期パーティションと、動作モードを示すパーティションIDの設定、並びに起動に必要なファイルの転送を行う処理を行うように作られている。 正式に対応しているインストール用の環境にはPATAのインターフェイスを持つPC/AT互換機が必要であるが、後述の通りブートストラップの変更により、パーティションの作成、ファイルの展開を行うことで起動可能な状態にすることが可能であるため、USB変換ドングル等の併用により、ノートPC等を用いたインストール方法も確立され、開発者の開いたイベントやユーザが個人で解説するなどした。

製品としては、あくまで、**ストリーミングサーバ組み立てキット**であり、前作同様、開発者の意向から、標準では、[samba](https://ja.wikipedia.org/wiki/samba "wikilink")はインストールされず、Windowsからネットワークドライブとして使う[NASとして利用する場合は](../Page/ネットワークアタッチトストレージ.md "wikilink")、ユーザが自らインストール/設定を行う必要がある。 意図的に「能動的に利用すること」を要求するように構成されているが、CPUの変更により、様々な事が容易に実現できるようになった。 利用のノウハウや、HDDの稼動実績などが[ユーザの作成したWiki](http://iohack.sealandair.info/wiki/)に集約されており、自由に編集できる事もあってか、公式ページよりも充実した情報や、各種リンクが用意されている。

[ハードウェア](../Page/ハードウェア.md "wikilink")としては、親ブランドである株式会社[アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink")のGigaLANDISKの二台HDDを内蔵できるタイプの製品がベースになっているが、樹脂パーツが着色されていない事や、エンブレムの違い程度で、他は同一である。 ソフトウェア的には、親ブランドの製品では出来なかったミラーリングで二台運用する事が可能になっているが、ベースとなる筐体が分解を考慮していないため、きっちり組み上げてしまった際のメンテナンス性は高いとは言えないことも前作と同じであり、エアフロー改善のためと思われる樹脂板の存在により、HDDの着脱は更に手間を要するようになった。 RAIDからの復旧には復旧モードが用意されたことから、自分でコマンドを知らずとも、崩壊や故障などでデグレードしたシステムからの復旧は容易になっている。

また、今回追加されたDebianモードの初期仕様では、利用にシリアルコンソールが必須であり、表示デバイスを持たないため、その他のモードでもいざというときにはシリアルコンソールが頼みの綱となる。 接続位置は異なるものの、[LAN Tankシリアルコンソール用のSERIAL](../Page/LAN_Tank.md "wikilink")-KITが利用可能となっており、GLAN Tankの発売に伴い、再発売される事となった。 元々そのような利用を考慮していない筐体のため、これらのオプションをきちんと内蔵して利用できないのも前作と同じである。

尚、内蔵FlashROMに書き込まれているのは、RedBootであり、シリアルコンソールの速度は115.2Kb.p.s.に設定されている。 ブートストラップの変更に伴い、HDDのMBRにブートマネージャは不要となった。

## スペック

|                                                                   |                                                                                                                              |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| [HDD搭載可能台数](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") | 3.5インチ×2（Big Drive対応、8GB以上必須）                                                                                                |
| CPU                                                               | [Intel XScale](https://ja.wikipedia.org/wiki/Intel_XScale "wikilink") 400[MHz](https://ja.wikipedia.org/wiki/MHz "wikilink") |
| [RAM](../Page/Random_Access_Memory.md "wikilink")（メモリ）            | 128M[Byte](../Page/バイト_\(情報\).md "wikilink")                                                                                 |
| [LAN](../Page/Local_Area_Network.md "wikilink")                   | 1000Base-T/100Base-T/10Base-T×1                                                                                              |
| [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 2.0                   | ×4                                                                                                                           |

## 外部リンク

  - [SOME TANKS](http://iohack.sourceforge.jp/tanks/)
  - [I-O HACK Wiki](http://iohack.sealandair.info/wiki/)(現在つながりません。)
  - [I-O Hack Wiki](http://wiki.nothing.sh/835.html)
  - [iohack Project](http://sourceforge.jp/projects/iohack/)
  - [MAKAI(MAKe Again Iso-image)](http://makai.sourceforge.jp/wiki/index.php?FrontPage)

## その他関連

  - [挑戦者](https://ja.wikipedia.org/wiki/挑戦者 "wikilink")
  - [アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink")
  - [玄人志向](https://ja.wikipedia.org/wiki/玄人志向 "wikilink")

[Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink")