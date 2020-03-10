> この記事は[LSI](https://ja.wikipedia.org/wiki/LSI)から翻訳されています。


**音声合成LSI**（おんせいごうせいエルエスアイ）とは、[自然言語](../Page/自然言語.md "wikilink")による[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")出力の処理を行う[LSIである](../Page/集積回路.md "wikilink")。

汎用[DSPに近いものから](https://ja.wikipedia.org/wiki/デジタルシグナルプロセッサ "wikilink")、専用アナログICに近いものまでいろいろあるが、この記事では、主に[家電製品などに組み込まれ](../Page/家庭用電気機械器具.md "wikilink")、使用者に製品の動作状況を知らせるための[ヒューマンマシンインターフェース](https://ja.wikipedia.org/wiki/ヒューマンマシンインターフェース "wikilink")として用いられたものについて扱う。かつては、単純なコマンドベースの、アナログ的な音声合成手法にもとづくものが多かったが、近年では[ROMの大容量化](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")（コストパフォーマンス向上）などにより、あらかじめ[録音](../Page/録音.md "wikilink")された音声データを基に[ディジタル信号処理](https://ja.wikipedia.org/wiki/ディジタル信号処理 "wikilink")を行い出力するようなものも多い。

## 歴史

[コンピュータ](../Page/コンピュータ.md "wikilink")用に市販された初めての音声合成システムは、[1976年](../Page/1976年.md "wikilink")のCompu-Talker CT-1([$](https://ja.wikipedia.org/wiki/USドル "wikilink")398.00)である。コンピュータ用の増設ボードとして登場したが、当時は各社のコンピュータの[ハードウェア](../Page/ハードウェア.md "wikilink")に[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")がなく、汎用品として使用することができなかったため、あくまで電子部品の一つという扱いであった。

一般に音声合成が広まったのは、[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")に発売された[テキサスインスツルメンツ](https://ja.wikipedia.org/wiki/テキサスインスツルメンツ "wikilink")社のSpeak & Spellsという知育玩具の商業的成功によるところが大きい。この製品の当時の販売価格は日本で1万円程度と安価であったため、人気を博した。数十年前の製品であるが、現在でもミュージックシーンで人気があり、実機は高値で売買されている。

また、当時[米国で普及していた](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[パソコンである](../Page/パーソナルコンピュータ.md "wikilink")[Apple IIに](../Page/Apple_II.md "wikilink")、音声合成LSIを搭載した製品が販売されていた。これらの製品はいずれも[英語](../Page/英語.md "wikilink")圏で開発されており、出力言語は英語であった。

かつて、[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")の[メロディIC](https://ja.wikipedia.org/wiki/メロディIC "wikilink")として音声合成LSIが製造されていたが既に生産終了となっている。現在はアクエストがAVR[マイコン](../Page/マイコン.md "wikilink")に音声合成エンジンを書き込んだマイコンベースの音声合成LSIを発売しており、[秋月電子通商](../Page/秋月電子通商.md "wikilink")などで購入が可能。

## 電子音による音声合成方式

古くは、様々な[周波数](../Page/周波数.md "wikilink")や長さから成る電子音の複雑な合成を行って、限られた記憶容量しか持たない電子機器の音声出力などに使われた。鼻にかかったような[アクセント](../Page/アクセント.md "wikilink")が特徴的な音声を出力するこの方式のLSIは、[PC-6001mkII](https://ja.wikipedia.org/wiki/PC-6001mkII "wikilink")などの[8ビットパソコン](../Page/8ビットパソコン.md "wikilink")にも搭載された。今日でも旧式の[自動販売機](../Page/自動販売機.md "wikilink")に、このLSIを持つ製品が残されている。

この合成電子音を用いる方式の場合、母音と子音・アクセントをコマンド類で制御できるため、動作させるための[データ](../Page/データ.md "wikilink")を少なくでき、また制御も簡単であったため、処理能力や記憶容量に制約のある[マイコン](../Page/マイコン.md "wikilink")機器に組み込むのに適していた。[1970年代](../Page/1970年代.md "wikilink")後半から[1980年代](../Page/1980年代.md "wikilink")にかけて、[ハイテク](https://ja.wikipedia.org/wiki/ハイテク "wikilink")さをアピールし、他社製品との[差別化](https://ja.wikipedia.org/wiki/差別化 "wikilink")を図りたい日本の各家電メーカーは[多機能化](https://ja.wikipedia.org/wiki/多機能化 "wikilink")の一環として、競って「しゃべる家電」を市場投入した。

しかしアクセントを強弱で表現する英語の音声出力には十分実用的であったものの、アクセントを音程で表現する[日本語](../Page/日本語.md "wikilink")等では言語を正確に表現することができなかったため、若干聞き取りづらい音声出力しか行えず、日本では次第に「コンピュータ声」として敬遠され、廃れていった。

## デジタル録音方式

合成電子音方式に代わって登場したのがデジタル録音の音声を用いる方式で、内蔵されたROMに搭載された音声データを再生するものである。デジタル録音方式は、あらかじめ録音されたフレーズを組み合せて発声させる出力方式であることから、合成電子音方式と比較して汎用性に乏しかった。その欠点もLSI生産コストの低減により、機器に合わせた仕様のLSIチップが大量生産されるようになるにつれて解消された。またLSIに[フラッシュメモリー](https://ja.wikipedia.org/wiki/フラッシュメモリー "wikilink")を組み込むことで、パッケージ化された後に任意のメッセージを録音可能なものも存在する。

録音音声により発声する方式は、当初こそ記憶容量の問題から音声データの[ビットレート](https://ja.wikipedia.org/wiki/ビットレート "wikilink")が低く、「感度の悪い[ラジオ](../Page/ラジオ.md "wikilink")」程度に聞き取りづらいものであったが、次第に記憶容量が増えたり[データ圧縮](../Page/データ圧縮.md "wikilink")方式が改良されるにつれて、明瞭な音声を搭載することができるようになった。今日では[コストダウン](https://ja.wikipedia.org/wiki/コストダウン "wikilink")も進み、[玩具](../Page/玩具.md "wikilink")類、自動販売機、[キャッシュディスペンサー等の音声アナウンスのみならず](../Page/現金自動預け払い機.md "wikilink")、構内放送等の[チャイム](https://ja.wikipedia.org/wiki/チャイム "wikilink")音（俗にいう[ウェストミンスターの鐘](https://ja.wikipedia.org/wiki/ビッグ・ベン#鐘の音 "wikilink")）においても同方式を用いて電子的に録音された音が用いられ、また、信頼性の高さから人命に関わる[火災報知器](https://ja.wikipedia.org/wiki/火災報知器 "wikilink")の避難を促す音声ガイドにもこれらのLSIが利用されている。

## 音声合成

現在では[パソコンを用いて録音された音声や文章を読み上げるさせることができるが](../Page/パーソナルコンピュータ.md "wikilink")、これらは音声合成LSIを内蔵せず、汎用性の高い[CPU](../Page/CPU.md "wikilink")を使ってデジタル録音データの[ファイルから音声を再構成したり](../Page/ファイル_\(コンピュータ\).md "wikilink")、文章を解析してイントネーションなどの傾向を分析し、[ソフトウェア](../Page/ソフトウェア.md "wikilink")内で音声を合成して発声させている。この方式は高度な処理能力を必要とするため、性能に限りのあるLSIで実現することは困難だが、現在のパソコンであれば十分な処理能力を持つため、音声合成LSIを凌ぐ機能を実現することが可能となっている。

ことこれらでは、より自然な発声が行えるよう様々な[アルゴリズム](../Page/アルゴリズム.md "wikilink")が開発・利用されており、2000年代においては処理能力の向上したパソコンで、音程を付けて歌う製品も流通している。

## 関連項目

  - [音声合成](https://ja.wikipedia.org/wiki/音声合成 "wikilink")
  - [ヒューマンマシンインターフェース](https://ja.wikipedia.org/wiki/ヒューマンマシンインターフェース "wikilink")
  - [知育玩具](../Page/知育玩具.md "wikilink")
  - [自動販売機](../Page/自動販売機.md "wikilink")

## 外部リンク

  - [セイコーエプソン・音声合成IC](http://www.epson.jp/device/semicon/product/speech_audio/index.htm)
  - [沖電気・音声合成LSI](http://www.okisemi.com/jp/semicon/speech_audio/246/index.html)
  - [アクト・ブレイン　音声合成LSI](http://www.actbrain.jp/development/inhouse/index.html) - 規則音声合成機能を1チップに集約
  - ヤマハ音源LSI [YMU765『MA-5』](http://smaf-yamaha.com/jp/what/soundchip_ma5.html) - 携帯電話 [SMAF](../Page/SMAF.md "wikilink") 用
  - アクエスト音声合成LSI [AquesTalk pico LSI『ATP3011F4』](http://www.a-quest.com/products/atp3011f4-pu.html) - 1チップ音声合成

[Category:音声合成](https://ja.wikipedia.org/wiki/Category:音声合成 "wikilink") [Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink")