> この記事は[Wizpy](https://ja.wikipedia.org/wiki/Wizpy)から翻訳されています。


**wizpy**（ウイズピー）とは[ターボリナックス](https://ja.wikipedia.org/wiki/ターボリナックス "wikilink")株式会社から発売された携帯型OS＋マルチメディアプレーヤーである。

## 概要

1.7インチの有機ELディスプレイに、2Gバイトもしくは4Gバイトの[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")（うち1.2GBはOS、アプリケーションデータ）を搭載した携帯型デジタルオーディオプレーヤー。また、オーディオプレーヤーでありながら、パソコンに接続し起動時にブートデバイスとして指定することで、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")（Turbolinux FUJIベース）を起動することができる。これにより接続するPCに問わず同じ自分のPC環境を持ち運ぶことを可能としている。パソコンとの接続には[USBを用いる](../Page/ユニバーサル・シリアル・バス.md "wikilink")。すべてのデータは本体の中に保存できるため、接続したパソコンには記録は残らない。発売当初、本体の色は白と黒の2色だったが、2007年11月より、スマートブルー、チタンシルバー、シュガーピンク（いずれも4GBモデルのみ）の3色が加わった。また、wizpyOSとKNOPPIXEdu6のデュアルブートが可能な『wizpy KNOPPIX Edu6 Edition』モデル（4GB、1色のみ）がある。

## パソコンとして

[Turbolinux FUJIをベースとして](../Page/Turbolinux.md "wikilink")、[Live CDのように](../Page/Live_CD.md "wikilink")[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")にインストールすることなしにオペレーティングシステムを起動する。同等のコンセプトでは[USB-knoppixなどがあるが](../Page/KNOPPIX.md "wikilink")、USB-knoppixがユーザーの環境に合わせて比較的自由に[アプリケーションの](../Page/アプリケーションソフトウェア.md "wikilink")[インストール](../Page/インストール.md "wikilink")・[カスタマイズ](https://ja.wikipedia.org/wiki/カスタマイズ "wikilink")が行えるのに対し、wizpyOSはシステム領域の多くの部分が書き込み不可とされており、カスタマイズはターボリナックス社で提供しているアプリケーションをインストールすることで行うというスタンスである。

  - 特徴

<!-- end list -->

  - 起動には、PCのBIOS設定を変更してUSBデバイスを優先させることによりwizpyOSをブートさせる。基本的にはUSB-HDD扱いでPCに認識されるが、wizpy本体の設定を変更することでUSB-CDROMとして認識させることも可能。また、USBデバイスからのブートをサポートしていない機器の為に、専用の起動CDからUSB機器を認識させた後にwizpyOSを起動させる手段、PCに『grub for DOS』を事前にインストールすることにより、ブート時にwizpyを認識させる方法が用意されている。
  - 起動したマシンのハードディスクの中身は原則見えない。
  - wizpyOS起動中のサウンド出力は、PCのサウンドデバイスは一切利用せず、wizpy本体をUSBオーディオとして動作させることでwizpy上のヘッドフォン端子から出力する。
  - アプリケーションのインストールは、ターボリナックス社で提供されているamaパッケージのもののみ可能。RPMパッケージなどからのインストールは不可。
  - amaパッケージは[squashFS](https://ja.wikipedia.org/wiki/squashFS "wikilink")形式をベースにした圧縮ファイルであり、amaはwizpyOS起動時に自動でマウントされる。amaにアプリケーションで必要なライブラリなどを内包させることで、共有ライブラリの依存問題に囚われることなく、任意でアプリケーションの追加・削除ができる仕組みになっている。
  - ターボリナックス社より公開されている『wizpyOSアプリケーション開発キット』で独自のamaパッケージの作成が可能。開発キットはTurbolinux FUJI環境で動作する。
  - wizpyOS上における、wizpy本体のファームウェア及びプリインストールされているアプリケーション等の一括アップデート
  - wizpy製品登録ユーザー向けのネットワークストレージサービス（500[MBまで](https://ja.wikipedia.org/wiki/メガバイト "wikilink")）の利用が可能だったがこのサービスは既に終了している。http://www.wizpy.jp/index.php?action_info_detail=true\&category=1\&number=178

<!-- end list -->

  - プリインストールされている主なアプリケーション :

<!-- end list -->

  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")（[Firefox](../Page/Mozilla_Firefox.md "wikilink")）
  - [電子メールクライアント](../Page/電子メールクライアント.md "wikilink")（[Thunderbird](../Page/Mozilla_Thunderbird.md "wikilink")）
  - [オフィスソフト](../Page/オフィススイート.md "wikilink")（[OpenOffice.org](../Page/OpenOffice.org.md "wikilink") ※4GBモデルのみ。2GBは別途インストール）
  - [日本語入力システム](../Page/日本語入力システム.md "wikilink")（[ATOK](../Page/ATOK.md "wikilink")）
  - [Skype](https://ja.wikipedia.org/wiki/Skype "wikilink")
  - 音楽再生（[Amarok](../Page/Amarok.md "wikilink")）
  - [画像ビューア](https://ja.wikipedia.org/wiki/画像ビューア "wikilink")（[showimg](https://ja.wikipedia.org/wiki/showimg "wikilink")）
  - [メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")（Turboメディアプレーヤー ※wmvの再生が可能）
  - [RealPlayer](../Page/RealPlayer.md "wikilink")
  - DVDリッピングツール（TurboRip）

<!-- end list -->

  - [PDFビューワー](../Page/Portable_Document_Format.md "wikilink")（Adobe Reader）
  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - Java Runtime Environment
  - ricoh fonts

## 音楽プレーヤーとして

PCと接続時はマスストレージ、USBオーディオ機器として認識される。

  - 音楽再生（[OGG](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink"),[MP3](../Page/MP3.md "wikilink"),[WMA](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")）
  - 音声録音（[MP3](../Page/MP3.md "wikilink")）
  - FMラジオ
  - 静止画表示（[JPEG](../Page/JPEG.md "wikilink")）
  - 動画再生（[XviD](https://ja.wikipedia.org/wiki/XviD "wikilink")）
  - テキスト表示（.utfのみ。.txtは不可）

が利用可能。

## その他

  - ターボリナックス社は本製品のキャッチフレーズとして『手のひらサイズのパソコン』を謳っている。このことにより発表当初はwizpy自体がLinuxで動作するメディアプレーヤー、[PDAのような製品として](../Page/携帯情報端末.md "wikilink")、間違った認識で捉えて紹介したメディアもあった。
  - Youtubeやニコニコ動画のコンテンツをダウンロードできる『コンテンツダウンローダー』の機能がある。
  - 2009年1月、いくつかのネットショップにて数種類のモデルが通常より安価に販売された。Amazon.co.jpでは¥3,100、ビックカメラドットコムでは¥3,080。これがショップの在庫処分のために行われた特価販売なのか、[ターボリナックス](https://ja.wikipedia.org/wiki/ターボリナックス "wikilink")社の在庫処分を理由とするものなのかは明らかになっていない。
  - 「Wizpy」の名称は[小倉優子](https://ja.wikipedia.org/wiki/小倉優子 "wikilink")によるもの。

## 外部リンク

  - [wizpy Club](http://www.wizpy.jp/)
  - [製品紹介サイト](http://www.turbolinux.co.jp/products/wizpy/)
  - [プレスリリース](http://www.turbolinux.co.jp/cgi-bin/newsrelease/index.cgi?date2=20070031153734&mode=syosai)
  - [wizpy@wiki](http://www20.atwiki.jp/wizpy/)

[Category:携帯型プレーヤー](https://ja.wikipedia.org/wiki/Category:携帯型プレーヤー "wikilink")