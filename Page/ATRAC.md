> この記事は[ATRAC](https://ja.wikipedia.org/wiki/ATRAC)から翻訳されています。


**ATRAC**（**アトラック**、**Adaptive TRansform Acoustic Coding**）は、[ソニー](../Page/ソニー.md "wikilink")が開発したオーディオ[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")および可逆圧縮の技術・規格名、および後年開発された関連技術群の総称。いずれも、[ソニーグループ](../Page/ソニーグループ.md "wikilink")や、その他家電系メーカーの開発した規格・製品で主に利用される。[ミニディスク](../Page/ミニディスク.md "wikilink")のコンセプトである、「[CD](https://ja.wikipedia.org/wiki/CD "wikilink")と同等の記録時間を確保」「[コンパクトカセット](../Page/コンパクトカセット.md "wikilink")よりも高音質」「コスト面でリーズナブル」「編集・ランダムアクセスが容易な構造」の4点を満たすことを最優先として開発された\[1\]。

## 呼称について

ソニーはオリジナルATRAC（便宜上**ATRAC1**と通称される）の後に、関連技術の**ATRAC2**、**ATRAC3**、**ATRAC3plus**、および**ATRAC Advanced Lossless**を開発した。名称や用途が極めて似ているためこれら5種は「ATRAC系[コーデック](../Page/コーデック.md "wikilink")」としてまとめて扱われることが多いが、これらは相互互換性のない別々の規格である。

なお、ATRAC2・ATRAC3などの名称の末尾についている数字はATRACのバージョン番号であると誤解されることがあるが、正しくは名称の一部である。ソニー製ATRAC1コーデックの名称として「ATRAC Ver.○○」が使われるため、前者としばしば混同されるが、<span style="text-decoration:underline;">ATRAC3はATRACの最新版ではなく</span>、<span style="text-decoration:underline;">ATRAC Ver.3とATRAC3およびATRAC3plusは全くの別物</span>である。

ソニーは2005年秋より、これらすべての総称を**ATRAC**とすることで、規格混乱の収束を図っている\[2\]。

## ATRAC(1)

ATRACでは、QMF (Quadrature Mirror Filters) とMDCT（変形離散コサイン変換、Modified Discrete Cosine Transform）が利用されている。

エンコード過程においてはまずQMFに2回通され、帯域ごとに3分割される。このうち最初の通過で高音域 (11.025～22.05kHz) が分離され、2回目では残った音域が低音域 (0～5.5125kHz) と中音域 (5.5125～11.025kHz) に分離される。

分離後は、各々の帯域でMDCTが行われる。このMDCTの回数は場合によって変化し、高音域では1サウンドフレームあたり1回もしくは8回、低・中音域においては1回もしくは4回とされている。

このATRACはLSIの進歩に合わせて、Ver.1、Ver.2、Ver.3、Ver.3.5、Ver.4、Ver.4.5、TYPE-Rへとバージョンアップを重ねた\[3\]。

### ミニディスクにおける利用

ATRACは、音楽用の[ミニディスク](../Page/ミニディスク.md "wikilink")規格で採用された。ステレオ (通常292kbps) 、モノラル (通常146kbps)の2つのモードが用意されている。

最初期のMD機器で用いられていたソニー製ATRACコーデック"ATRAC Ver.1"では実記録ビットレートに現在の半分しか割り当てられていなかったため、[MP3](../Page/MP3.md "wikilink")より記録音質が極端に悪かった。このことがATRACの音質に対する悪印象を定着させてしまったことから、ATRAC Ver.1はその後の普及・展開にも大きな影響を及ぼしたコーデックとして悪名高い。ただしそれぞれのバージョン間で互換性はあるため、例えば最初期のMD機器で"ATRAC TYPE-R"でエンコードされたMDを再生することは可能である\[4\]。

なお、データ用MDであるMD-DATAやMD-DATA2でも音声を記録する場合のフォーマットとして使われることがある。

### SDDSにおける利用

ATRACはまた、SCPC社（現Sony Cinema Products Corporation）が開発した映画の音響システム[SDDS](../Page/ソニー・ダイナミック・デジタル・サウンド.md "wikilink") (Sony Dynamic Digital Sound) でも採用された。

収録は5.1chもしくは7.1chで、合計ビットレートは最大1280kbps。先行規格の[ドルビーデジタル](../Page/ドルビーデジタル.md "wikilink")や[dtsより音質の評価は高かったが](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")、設備コストなどが難点となり普及率は低い。現在のところ、劇場再生用しか対応されていない。

## ATRAC2

**ATRAC2**（アトラック・ツー）は、[1994年](../Page/1994年.md "wikilink")に発表された[ミニディスク](../Page/ミニディスク.md "wikilink")の汎用版「MD DATA」の標準音声フォーマットとして採用された技術・規格。詳細は不明だが、オリジナルのATRACよりも[TwinVQ](https://ja.wikipedia.org/wiki/TwinVQ "wikilink")や[AAC](../Page/AAC.md "wikilink")に近い技術とされる。

MD DATAでは最大4chの録音が可能で、ビットレートは1チャンネルあたり36.5kbpsまたは73kbps。主に演奏録音の用途において、2ch（ステレオ）録音しかできない通常のミニディスクのかわりに利用された。

## ATRAC3 / ATRAC3plus

**ATRAC3**（アトラック・スリー）は、ATRAC2をベースに開発された技術・規格で、[1999年](../Page/1999年.md "wikilink")に発表された。

音声は0～2.75625kHz、2.75625～5.5125kHz、5.5125～11.025kHz、11.025～22.05kHzと帯域ごとに4分割される。ビットレートは通常、132kbps、105kbps、66kbpsの3種類が使われる。このうち66kbpsはJoint Stereoを併用することでビットレートの不足を補っている。

ウォークマンに添付されている音楽管理・転送ソフトウェア[SonicStage](https://ja.wikipedia.org/wiki/SonicStage "wikilink")/[CONNECT Player](../Page/CONNECT_Player.md "wikilink")/[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")の楽曲配信サービスである[mora](https://ja.wikipedia.org/wiki/mora "wikilink")(モーラ)が、2012年9月までこの方式で楽曲を配信していた（同年10月以降は[AAC](../Page/AAC.md "wikilink")に変更）。

また、**ATRAC3plus**（アトラック・スリー プラス）はATRAC3をベースに開発された技術・規格で、[2002年](../Page/2002年.md "wikilink")に発表された。ATRAC3plusではATRAC3で帯域ごとに4分割されていたものを16分割にして特徴の分析精度を高め、多くの非可逆圧縮フォーマットで使用されている[整数の符号化](https://ja.wikipedia.org/wiki/整数の符号化 "wikilink")においてより多くの置き換えパターンを持つことで圧縮率を高めるといった方法が採用されている。ATRAC3との互換性はないが、発表以後はATRAC3とセットで採用されていることが多い。

ATRAC3plusは登場当初、64kbps、48kbpsの2モードのみが用意され、ATRAC3の基本3モードよりも高圧縮・低音質の用途に振られていた。しかし2004年ごろからは低圧縮・高音質用途向けのモードが追加されるなど、ATRAC3を徐々に置き換えていくかたちがとられている。

### PC上での利用

ATRAC3およびATRAC3plusは、AV機器・設備で内部的に使われることの多かったATRAC、ATRAC2とは違い、PC上でファイルとして利用されることが多い。

初めてATRAC3をサポートした一般向けソフトウェアは、ソニーの「[OpenMG Jukebox](https://ja.wikipedia.org/wiki/OpenMG_Jukebox "wikilink")」である。OpenMG Jukeboxは1999年末に発売されたウォークマンに添付されていた音楽管理・転送ソフトウェアで、ATRAC3での[CDリッピング](../Page/コンパクトディスク.md "wikilink")、PC上の[WAV](../Page/WAV.md "wikilink")・[MP3](../Page/MP3.md "wikilink")ファイルのATRAC3変換、およびウォークマンへの転送機能が用意されていた。

これらの機能は、ソニーが後年開発した[SonicStage](https://ja.wikipedia.org/wiki/SonicStage "wikilink")や[CONNECT Player](../Page/CONNECT_Player.md "wikilink")、その後継の[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")でもサポートされている。また他社からも[ジャストシステム](../Page/ジャストシステム.md "wikilink")の[BeatJam](../Page/BeatJam.md "wikilink")、[ケンウッド](../Page/ケンウッド.md "wikilink")のMuliaなど、主にNet MD機器向けに対応ソフトウェアがリリースされている。

ATRAC3plusへ初めて対応したソフトウェアは、[バイオの](../Page/VAIO.md "wikilink")2002年秋モデルにプリインストールされたSonicStage Ver.1.5である。当初は64kbps、48kbpsの2モードに対応し、ATRAC3の3モードよりも高圧縮・低音質の用途に振られていたが、Ver.2.0からは256kbps、Ver.3.2では320kbps、192kbps、160kbps、128kbps、96kbps、Ver.3.4では352kbpsが追加され、ATRAC3 132kbpsよりさらに高音質なモードを含む、幅広い用途をカバーするようになった。

SonicStage Vと[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")(Ver.1.0)ではMP3・WAVなど他のフォーマットからATRACに変換する機能は削除され、CDからの取り込みのみ対応している。[BeatJam](../Page/BeatJam.md "wikilink")などではファイルのATRAC変換も可能である。

ATRAC3ファイルの本来の拡張子は"aa3"だが、OpenMG Audioコンテナに格納した"oma"が利用されることがほとんどである。なお、[OpenMG](https://ja.wikipedia.org/wiki/OpenMG "wikilink")で暗号化した場合の拡張子は"omg"（OpenMGコンテナ）もしくは"oma"となる。"omg"はOpenMG Jukeboxや初期のSonicStageで使われていたが、"oma"登場以降は新たなファイル作成ができなくなり、[CONNECT PlayerやSonicStage](../Page/CONNECT_Player.md "wikilink") V、x-アプリでは非対応となった。"oma"はSonicStageバージョン2.1で登場し、初期は暗号化したファイルしか作れなかったが、CONNECT PlayerやSonicStageバージョン3.2以降は暗号化が任意となった。

ギャップレス再生に関しては、[LAME](../Page/LAME.md "wikilink")でエンコードしたMP3のように曲ファイルそのものにギャップレス情報を埋め込むわけではないので個別にエンコードしたファイルのギャップレス再生はできないが、所謂擬似ギャップレスには対応しており、CD全体、もしくは何曲かまとめてエンコードすることによってギャップレス再生に対応している。また本来ミニディスク向けフォーマットから発展したためか、ミニディスクと同様のカット編集（分割・結合）がx-アプリなどの対応ソフトウェアで行えるようになっている\[5\]。

### メモリースティック規格での利用

ATRAC3を採用した最初の[携帯音楽プレーヤー](../Page/携帯音楽プレーヤー.md "wikilink")は、[1999年](../Page/1999年.md "wikilink")末に発売されたソニーの[メモリースティック](../Page/メモリースティック.md "wikilink")[ウォークマン](../Page/ウォークマン.md "wikilink")「NW-MS7」である。この製品は付属ソフトウェアのOpenMG JukeboxによってCDの楽曲やPC上の[WAV](../Page/WAV.md "wikilink")・[MP3](../Page/MP3.md "wikilink")ファイルをATRAC3に変換し、本体に挿入したマジックゲート メモリースティック（MGMS）に転送するというかたちがとられていた。

[メモリースティック](../Page/メモリースティック.md "wikilink")上でのATRAC3/ATRAC3plusの扱いは[メモリースティックオーディオ](../Page/メモリースティックオーディオ.md "wikilink")として規格化されているため、別メーカーの別製品に挿入した場合でも原則として再生が可能である。ただしメモリースティック自体に複数のタイプが登場し、またATRAC3plusは遅れて2003年に採用されたことなどから、初期の製品との互換性には一部問題が生じている。

ウォークマン以外の機器でメモリースティック上のATRAC3ファイルを再生できるものには、ソニーの[CLIE](../Page/CLIE.md "wikilink")、[SCEの](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")[PSP](../Page/PlayStation_Portable.md "wikilink")、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")・[au向けの](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")（[ソニー・エリクソン・モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink")製、[三菱電機](../Page/三菱電機.md "wikilink")製の一部モデル）などがある。また、過去には[シャープ](../Page/シャープ.md "wikilink")からヘッドホン型メモリースティックプレーヤー「e-musee」、[ケンウッド](../Page/ケンウッド.md "wikilink")や[パイオニア](https://ja.wikipedia.org/wiki/パイオニア "wikilink")からメモリースティックスロット搭載ミニコンポ、[アルパインからメモリースティックスロット搭載カーオーディオ](../Page/アルパイン_\(企業\).md "wikilink")・カーナビゲーションなどが販売されていた。

### ミニディスク拡張規格での利用

[ミニディスク](../Page/ミニディスク.md "wikilink")では[2000年](../Page/2000年.md "wikilink")から導入された長時間録音規格「MDLP」において、ATRAC3 132kbpsがLP2モード、ATRAC3 66kbpsがLP4モードとして採用された。この後、翌[2001年](../Page/2001年.md "wikilink")登場の**Net MD**ではMD・PC間でデータ転送が可能になったため、ネットワークウォークマンなどとのATRAC3データの共有や、音楽配信サービスで購入したATRAC3データの転送・再生も可能になった。

また、[2004年](../Page/2004年.md "wikilink")に登場した拡張規格「Hi-MD」ではMDLPで規定された2モードのほか、採用が漏れていたATRAC3 105kbps、およびATRAC3plusの256kbps、64kbps、48kbpsが新モードとして追加された。このうち、ATRAC3plus 256kbpsと64kbpsについてはHi-SP、Hi-LPというモード名がつけられた。

### その他の機器における利用

[メモリースティック](../Page/メモリースティック.md "wikilink")[ウォークマン](../Page/ウォークマン.md "wikilink")発売の翌年である[2000年](../Page/2000年.md "wikilink")、ソニーは新ブランドとして「ネットワークウォークマン」（2005年からは単に「ウォークマン」となる）を創設し、以後メモリースティックタイプ、内蔵メモリタイプ、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")タイプを順次ラインナップした。これらネットワークウォークマンはすべてATRAC3に対応している（2007年以降の海外向け機種(型番の頭がNWZ-)を除く）ほか、[2003年](../Page/2003年.md "wikilink")に発売されたNW-MS70DからはATRAC3plusの再生にも対応した。また、CDウォークマンにはATRAC3/ATRAC3plusファイルが書き込まれたCD-R/RW（ATRAC CD）の再生をサポートする機種が存在する。

このほか、ソニー製機器では[VAIO](../Page/VAIO.md "wikilink") ミュージッククリップ、VAIO ポケット、[NETJUKE](../Page/NETJUKE.md "wikilink")、[PlayStation Portable](../Page/PlayStation_Portable.md "wikilink")、[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")、[PSX](../Page/PSX.md "wikilink")など非ウォークマンブランドのものにも対応例が多い。

また、ハードディスクドライブ搭載[カーナビゲーション](../Page/カーナビゲーション.md "wikilink")システムでは、ソニー、[クラリオン](../Page/クラリオン.md "wikilink")、[三洋電機](../Page/三洋電機.md "wikilink")、[パイオニア](https://ja.wikipedia.org/wiki/パイオニア "wikilink")、[富士通テン](https://ja.wikipedia.org/wiki/富士通テン "wikilink")が音楽再生機能用に利用している。

### RealAudio 8 with ATRAC3

[リアルネットワークス](../Page/リアルネットワークス.md "wikilink")の[RealAudio](../Page/RealAudio.md "wikilink")フォーマットでは、**RealAudio 8 with ATRAC3**としてATRAC3が採用された。暗号化技術の[OpenMG](https://ja.wikipedia.org/wiki/OpenMG "wikilink")も同時に導入され、同社のソフトウェアもネットワークウォークマン等と連携ができるようになった。

ビットレート設定は非常に柔軟で、352kbps、264kbps、176kbps、146kbps、132kbps、105kbps、94kbps、66kbpsなどが利用できる。ただしATRAC3は105kbpsを超える高ビットレート用途を想定して採用されていたため94kbps、66kbpsはオプション扱いで、通常の低ビットレート用途向けには別のコーデックが存在していた。

PC上のファイル作成においては当時のソニー製ソフトウェアと違い暗号化の有無を選択でき、拡張子は暗号化時"rmx"、非暗号化時"rmj"。いずれも、ソニー製ソフトウェアで生成したATRAC3ファイルとの直接的な互換性はないとされている。

なお、RealAudio 10フォーマットではATRAC3のかわりに[AAC](../Page/AAC.md "wikilink")が採用された。

### ユニバーサル・メディア・ディスクでの利用

[ユニバーサル・メディア・ディスク](../Page/ユニバーサル・メディア・ディスク.md "wikilink")では、ビデオ規格「UMD Video」およびオーディオ規格「UMD Audio」の音声フォーマットとして採用されている。

### かつて行われた音楽配信サービス

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の以下を始めとする[音楽配信](../Page/音楽配信.md "wikilink")サービスで、ATRACによる配信が行われており、全ての音楽配信サイトで[mora](https://ja.wikipedia.org/wiki/mora "wikilink")のプラットフォームを利用していた。主に使用されていたのはATRAC3の132kbps（moraで配信されている一部の楽曲に限りATRAC3plusの256kbpsも使用）であったが、ORICON STYLEはATRAC3plusを採用していた。なお、moraが2012年10月以降配信フォーマットを[DSD](../Page/Direct_Stream_Digital.md "wikilink")・[FLAC](../Page/FLAC.md "wikilink")による[ハイレゾリューションオーディオ](https://ja.wikipedia.org/wiki/ハイレゾリューションオーディオ "wikilink")と[MP3](../Page/MP3.md "wikilink")[AAC](../Page/AAC.md "wikilink") 320kbpsの[デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink")無しに切り替えたため、2013年1月のAnyMusicのサービス終了をもって、日本国内外から事実上ATRAC及び[OpenMG](https://ja.wikipedia.org/wiki/OpenMG "wikilink")形式を利用した音楽配信サービスが消滅した。

#### サービス一覧

  - AnyMusic（2013年1月17日をもって配信終了し2013年1月31日をもって再ダウンロード終了）
  - [mora](https://ja.wikipedia.org/wiki/mora "wikilink")（2012年9月30日をもってATRACでの配信終了）
  - Kmusic（moraへ統合）
  - bitmusic（2007年7月にmoraへ統合）
  - @MUSIC（2006年6月にmoraへ統合）
  - ORICON STYLE（2006年11月に配信終了）
  - Victor Music Download（ビクターエンタテインメントが運営。事実上moraに販売楽曲及び決済を共有化）
  - HMV DIGITAL（2010年2月に配信終了）
  - Yahoo\! ミュージックダウンロード（2012年8月に配信終了）

### レーベルゲートCD

2002年にレーベルゲートと[ソニー・ミュージックエンタテインメントが開発した](https://ja.wikipedia.org/wiki/ソニー・ミュージックエンタテインメント_\(日本\) "wikilink")「レーベルゲートCD」は、ATRAC3 132kbpsがPC用のデータ形式として採用された。レーベルゲートCDは[コピーコントロールCD](../Page/コピーコントロールCD.md "wikilink")の一種だが、インターネット経由で認証することでPC上でATRAC3ファイルを再生したり、ATRAC Audio Device・MGメモリースティックに回数制限付きで転送する機能が用意されている。後に認証なしでPC上でATRAC3ファイルを再生できる「レーベルゲートCD2」に置き換えられたが、2004年11月17日発売分以降の音楽タイトルには利用されていない。全タイトルがCD-DAでの再リリースに伴い[廃盤](../Page/廃盤.md "wikilink")となり、認証サービスも2008年3月までに終了した。

### その他

  - かつてはATRAC3/ATRAC3plus再生に対応した[携帯電話](../Page/携帯電話.md "wikilink")端末は[メモリースティック](../Page/メモリースティック.md "wikilink")を採用しており、[SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")採用端末での対応は稀であった。
      - 2005年に[京セラ](../Page/京セラ.md "wikilink")が開発した[ウィルコム](../Page/ウィルコム.md "wikilink")向け[PHS](../Page/PHS.md "wikilink")端末「[WX310K](../Page/WX310K.md "wikilink")」では、[miniSDカード上のATRAC](https://ja.wikipedia.org/wiki/SDメモリーカード#miniSDカード "wikilink")/MP3ファイルを再生できる「ミュージックプレイヤー(有償)」機能が用意されている。
      - [2007年](../Page/2007年.md "wikilink")[11月](../Page/11月.md "wikilink")にソニー・エリクソン・モバイルコミュニケーションズが開発した[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")向け「[SO905i](../Page/SO905i.md "wikilink")」では、USBデバイスをATRACモードとすることにより、ATRAC/MP3のmicroSD転送に対応している。
      - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")からは[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")[連合](https://ja.wikipedia.org/wiki/連合 "wikilink")）において「[SonicStage for LISMO](https://ja.wikipedia.org/wiki/SonicStage#SonicStage_for_LISMO "wikilink")」を展開。対応機器ではATRACのmicroSD転送に対応している。2009年からは「[x-アプリ for LISMO](https://ja.wikipedia.org/wiki/x-アプリ#x-アプリ_for_LISMO "wikilink")」となり、2013年11月まで展開が続けられた。
  - 2007年8月、ソニーは北米および欧州市場においてATRAC形式の音楽配信事業（CONNECT Music Store）からの撤退を発表した。これに伴い北米および欧州市場におけるATRACの展開は終了し、以降に発売される携帯音楽プレーヤーはATRAC形式及びSonicStageに非対応（MP3/WMA形式および[D\&D転送に対応](../Page/ドラッグ・アンド・ドロップ.md "wikilink")）となった。その後も日本市場では引き続きATRACの展開を続けているものの、2009年以降は国内向けのウォークマンもD\&D転送に対応しているうえ、前述のように音楽配信サービスの順次終了や[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")3.0以降の標準フォーマットがAACになるなど国内でも展開は縮小傾向である。

## ATRAC Advanced Lossless

**ATRAC Advanced Lossless**（アトラック アドバンスト ロスレス）は2005年9月のA\&Vフェスタ2005で発表された、ATRACで唯一の[可逆圧縮](../Page/可逆圧縮.md "wikilink")技術・規格。**AAL**と略されることが多い（この記事内でも以下AALとして表記する）。

ATRAC3もしくはATRAC3plusにより非可逆圧縮したデータ、およびそれと原音との差分を記録した誤差成分データを併せ持つことで無損失での記録を行う。携帯音楽プレーヤーにはAALデータ全体の転送のほか、ATRAC3/ATRAC3plus部分だけを取り出すことで小さなサイズのデータとしての高速転送もできる。一般的なロスレス圧縮では可逆圧縮データを小さなサイズのデータとして転送しようとする場合、再圧縮してから転送する為に転送に時間がかかるほか、可逆圧縮データとは別に非可逆圧縮データを保存する為に転送元機器のデバイス容量がより多く消費されるが、AALでは非可逆圧縮データをファイル内に内包しているので、転送時間やデバイスの消費容量が削減されるという利点がある。

AALの圧縮率は30～80%とされている。一般に可逆圧縮技術は原音の内容に圧縮率が大きく左右されるが、AALはそれに加えて非可逆圧縮データの形式や品質も圧縮率に影響する。

AALは、2005年11月1日に公開されたSonicStage Ver.3.3で初サポートされた。SonicStageでは、ベースとなる[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")部分の形式・品質をATRAC3plus（352kbps 256kbps、128kbps、64kbps）、ATRAC3（132kbps）から選択できる。AALデータ全体の転送にはAALに完全対応した機器が必要だが、ATRAC3/ATRAC3plus部分のみの転送は従来機器・AALに対応した機器何れに対しても行える。

ウォークマンAシリーズ（A800シリーズ以降）やSシリーズ（NW-S700F/600シリーズ以降）・X1000シリーズにてAALの再生に対応している。一方ウォークマンの海外モデルのほとんどやPSP・PS3ではロスレス部分の再生に対応していない。

発表された2005年当時、ソニーではAALを利用した[音楽配信](../Page/音楽配信.md "wikilink")サービスについても構想していたようであるが\[6\]、ATRAC形式の音楽配信サービス終了により事実上霧散解消状態となっている。また[サンプリング周波数](../Page/サンプリング周波数.md "wikilink")等がCDと同じ規格に固定されており、CDを超える音質での配信・録音の保存などが不可能なため、ソニーグループでも[FLAC](../Page/FLAC.md "wikilink")等ハイレゾフォーマットに対応した可逆圧縮規格にシフトしている。

## 他コーデック形式への変換

かつてはATRACファイルを他の形式に変換することは困難であり、ATRAC非対応のプレーヤーに買い替えた際にそれまでのATRAC資産が活用できない問題を抱えていた。

2006年5月にリリースされたSonicStage CP(Ver.4.x以降)および[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")(Ver.1.1以降）から、著作権保護されていないATRACファイルであればWAVに変換（再コーデック）できるほか(SonicStage V・[x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")Ver.1.0では不可)、ソニーUSAが配布する専用ツールでMP3に直接変換ができる\[7\]。

ATRAC形式への変換不対応としたソニーの[Media Go](https://ja.wikipedia.org/wiki/Media_Go "wikilink")([PlayStation Portable](../Page/PlayStation_Portable.md "wikilink")・[Xperia](https://ja.wikipedia.org/wiki/Xperia "wikilink")・[ウォークマン](../Page/ウォークマン.md "wikilink")等へのメディアファイル転送ソフト)では、ライブラリに取り込んだATRACファイルの再生と、機器転送時にMP3もしくはAACへ自動変換に対応している。バージョン2.5からは転送時でなくてもFLACやMP3、AACに変換できるようになった。

また、波形編集ソフト「[Sound it\!](../Page/Sound_it!.md "wikilink")」(Ver.5.0以降)でも、MP3・WAV・WMA等との相互変換・保存ができる。ATRACかATRAC3であれば、[FFmpeg](../Page/FFmpeg.md "wikilink")を使っているソフトウェアを使うことで再生や別形式への変換ができる (暗号化されたファイルは0.9以降)。

また、SONY製オーディオプレーヤー「[WALKMAN](../Page/ウォークマン.md "wikilink")」音楽管理・転送ソフト「[Music Center for PC](https://ja.wikipedia.org/wiki/Music_Center_for_PC "wikilink")」は、ATRACデータの [AAC](../Page/AAC.md "wikilink") / [FLAC](../Page/FLAC.md "wikilink") 変換に対応しており、ライブラリにインポートしてあるデータを変換できる。

## 脚注

## 関連項目

  - [ミニディスク](../Page/ミニディスク.md "wikilink")
  - [メモリースティック](../Page/メモリースティック.md "wikilink")
  - [メモリースティックオーディオ](../Page/メモリースティックオーディオ.md "wikilink")
  - [ウォークマン](../Page/ウォークマン.md "wikilink")
  - [非可逆圧縮](../Page/非可逆圧縮.md "wikilink")
  - [PASC](../Page/PASC.md "wikilink")
  - [SonicStage](https://ja.wikipedia.org/wiki/SonicStage "wikilink")
  - [x-アプリ](https://ja.wikipedia.org/wiki/x-アプリ "wikilink")
  - [Media Go](https://ja.wikipedia.org/wiki/Media_Go "wikilink")
  - [FFmpeg](../Page/FFmpeg.md "wikilink")
  - [foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")
  - [Rockbox](../Page/Rockbox.md "wikilink")

## 外部リンク

  - [ATRAC](http://www.sony.co.jp/Products/ATRAC3/index.html)
  - [Sony ATRAC3 Audio Codec](http://www.free-codecs.com/download/Sony_ATRAC3_Audio_Codec.htm)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:ソニーの製品](https://ja.wikipedia.org/wiki/Category:ソニーの製品 "wikilink") [Category:非可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:非可逆圧縮アルゴリズム "wikilink") [Category:可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:可逆圧縮アルゴリズム "wikilink")

1.
2.
3.
4.
5.  ATRAC以外の圧縮音声フォーマットは通常、再エンコードなしでのカット編集はできない。ただしMP3の場合はmp3DirectCutというフリーウェアで編集が可能である。また、ATRAC Advanced Losslessはギャップレスおよびカット編集に対応しない。
6.  [藤本健氏のATRAC開発者インタビュー](http://www.sony.co.jp/Products/ATRAC3/special/interview04.html)、ソニーATRAC公式サイト
7.