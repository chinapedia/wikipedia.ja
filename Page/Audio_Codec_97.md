> この記事は[Audio Codec 97](https://ja.wikipedia.org/wiki/Audio_Codec_97)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Yakumo_Notebook_536S_-_Realtek_ALC655-7154.jpg "wikilink") **Audio Codec 97**（オーディオコーデック キュウジュウナナ）は[1996年](../Page/1996年.md "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が提唱したサウンド[インターフェースの標準規格である](../Page/インタフェース_\(情報技術\).md "wikilink")。96年に最初のRev. 1.0が発表され以降改定を重ねており、Rev. 2.3が最新版となっている。[2004年](../Page/2004年.md "wikilink")に発表された**[High Definition Audio](../Page/High_Definition_Audio.md "wikilink")**が後継規格となっている。なお一般には**AC'97**と略称されることが多い。本項でも以下ではAC'97と呼称する。

## 概要

従来はワンチップ構成されることも多かったサウンドデバイスを論理コントローラとアナログコーデックに分離し、高音質化と柔軟性を確保している。また論理コントローラ部をソフトウェア処理させることでサウンドシステムの価格低下も実現する。論理コントローラとアナログコーデックはそれぞれに役割が定められており、5線の双方向シリアルインターフェイスである**AC-LINK**で接続される。ハードウェアの電気的仕様に加え、扱うべきサンプリング周波数・入出力チャンネル数なども規格として定められており、互換性の確保が図られている。

### AC'97規格の特徴

  - AC-LINKにより論理コントローラとアナログコーデックをリンク
  - 20bit/96kHzまでの2chステレオ入出力に対応
  - 20bit/48KHzまで8(7.1)chサラウンド出力に対応
  - モノラルマイク入力に対応
  - データおよび音声一系統ずつのモデム機能
  - [S/PDIF](https://ja.wikipedia.org/wiki/S/PDIF "wikilink")準拠デジタル入出力に対応

なお、機能のサポートはAC'97規格のリビジョンおよび製品の実装に依存する。

### 論理コントローラの主な機能

  - サンプリング周波数変換
  - デジタルソース[ミキシング](../Page/ミキシング.md "wikilink")
  - ウェーブテーブルシンセサイザー
  - [3Dオーディオ機能](../Page/立体音響.md "wikilink")
  - レガシ互換機能

### アナログコーデックの主な機能

  - [アナログ→デジタル変換](../Page/デジタル-アナログ変換回路.md "wikilink")
  - [デジタル→アナログ変換](../Page/アナログ-デジタル変換回路.md "wikilink")
  - アナログソースミキシング

## 「AC'97」と「オンボードサウンド」

[thumb](https://ja.wikipedia.org/wiki/ファイル:Onkyo_se-80pci.jpg "wikilink") SE-80PCI)\]\] AC'97の普及と同時期に[オンボード](../Page/オンボード.md "wikilink")サウンドと呼ばれるマザーボードに実装するサウンド機能の普及も進んだため、「AC'97」がオンボードサウンド機能の代名詞のように扱われることも多い。しかし前述のように本来、AC'97 = Audio Codec '97はインターフェースに関する規格であり、[スタンドアローン](../Page/スタンドアローン.md "wikilink")の[サウンドカード](../Page/サウンドカード.md "wikilink")でも[PCI世代以降はAC](../Page/Peripheral_Component_Interconnect.md "wikilink")'97準拠のものが多く、それらは「サウンドチップ」と呼ばれる論理コントローラと汎用のAC'97アナログコーデックを組み合わせた構成となっている。

## 問題点と後継規格

1999年に登場したIntel810チップセットで採用された**[ICH](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink")**以降、一般的なPC用[チップセット](../Page/チップセット.md "wikilink")のサウスブリッジにはAC'97準拠の論理コントローラが統合されていた。そのため、当時のPCのサウンド機能は、サウスブリッジの論理コントローラと[マザーボード](../Page/マザーボード.md "wikilink")上のアナログコーデックチップで実現している場合が多かった。安価かつ実装面積が少ないというメリットがある反面、AC'97で定められているサンプリングレートでは[DVD-Audio](../Page/DVD-Audio.md "wikilink")などの高音質フォーマットに十分対応できないという問題があった。

2004年、AC'97の問題点に対応するための後継規格としてインテルは[High Definition Audio](../Page/High_Definition_Audio.md "wikilink")(HD Audio)規格を発表した。2006年頃までには新規に出荷されるシステムの大半はHD Audio準拠サウンド機能に置き換えられたが、旧式チップを使用した廉価システムなどではAC'97も依然使用されていた。

## AC'97規格準拠アナログコーデックチップの主なメーカー

  - [Analog Devices](https://ja.wikipedia.org/wiki/Analog_Devices "wikilink")
  - Avance Logic（AC'97コーデック事業はRealtekが買収）
  - [C-Media Electronics](https://ja.wikipedia.org/wiki/C-Media_Electronics "wikilink")
  - [National Semiconductor](https://ja.wikipedia.org/wiki/ナショナルセミコンダクター "wikilink")
  - [Realtek Semiconductor](../Page/Realtek.md "wikilink")
  - [Sigmatel](https://ja.wikipedia.org/wiki/Sigmatel "wikilink")→[IDT](../Page/IDT.md "wikilink")
  - [VIA Technologies](../Page/VIA_Technologies.md "wikilink")
  - [YAMAHA LSI](../Page/ヤマハ.md "wikilink")
  - [旭化成](../Page/旭化成.md "wikilink")エレクトロニクス（旧旭化成マイクロシステム）

## 関連項目

  - [マザーボード](../Page/マザーボード.md "wikilink")
  - [サウンドカード](../Page/サウンドカード.md "wikilink")
  - [オンボード](../Page/オンボード.md "wikilink")
  - [High Definition Audio](../Page/High_Definition_Audio.md "wikilink")

[Category:インテル](https://ja.wikipedia.org/wiki/Category:インテル "wikilink") [Category:サウンドカード](https://ja.wikipedia.org/wiki/Category:サウンドカード "wikilink")