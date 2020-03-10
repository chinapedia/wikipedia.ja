> この記事は[EPSXe](https://ja.wikipedia.org/wiki/EPSXe)から翻訳されています。


**ePSXe**は、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")の[PlayStation用ソフトを](https://ja.wikipedia.org/wiki/PlayStation_\(ゲーム機\) "wikilink")、主に[Microsoft Windows上でプレイする為の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ゲームエミュレータ](https://ja.wikipedia.org/wiki/ゲームエミュレータ "wikilink")。後発のエミュレータより動作するソフトが圧倒的に多い。Ver1.9.25により、[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")のエミュレート機能が導入され、ユーザーは実機から吸い出した[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")を用意する必要がなくなった。しかし、以前と同様に実機の[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")を導入することも可能である。 PCの最新版は[2016年](../Page/2016年.md "wikilink")にリリースされたVer2.0.5である。

## 特徴

数々の市販のROMを動作させることが可能である。またプラグイン方式を採用しており、利用しているパソコンに合わせて環境設定を行うことが出来る。設定次第ではPS実機よりも優れた解像度でゲームを実行することも可能。

## 主な機能

多くの現行型エミュレータと同様に、ePSXeはGPU、SPU(サウンド)、およびCD-ROMドライブの機能をエミュレートするためにプラグイン方式を採用している。これはPSEmu Proにより確立された。ゲームを読み込む際には、コンピュータのCD-ROMドライブまたは、CDのイメージファイルを直接ハードディスクから読み込むことが可能である。

パッチ適用機能では、ユーザーがゲームにパッチを適用することができる。正常に動作しない、または全く動作しないゲームをパッチによって修復し、動作させることが可能である。パッチファイルは .ppf形式をサポートする。しかしバグを起こす全てのゲームのためにパッチがあるとは限らない。

[PlayStationのBIOSの機能をエミュレートする他のエミュレータと違い](https://ja.wikipedia.org/wiki/PlayStation_\(ゲーム機\) "wikilink")、ePSXeはプレイステーション本体からダンプした[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")を使用する。この[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")イメージファイルの著作権は[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")のものであるため、インターネット上に配布をする行為、またダウンロードする行為は違法である。これらの理由からePSXeにBIOSイメージファイルは同封されておらず、自分でダンプする必要がある。バージョン1.9.25において、HLE BIOSのサポートが追加され、BIOSイメージがなくともゲームを起動させることが可能となった。

### プラグイン

  - GPU
    グラフィック関連のプラグイン。多くのGPUプラグインは[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")、[OpenGL](../Page/OpenGL.md "wikilink")、[Glide APIのいずれかで動作し](https://ja.wikipedia.org/wiki/Glide_API "wikilink")、多くは[フリーウェア](../Page/フリーウェア.md "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")で利用できる。
  - SPU
    サウンド関連のプラグイン。SPUプラグインは、プラグインの設定に応じてBGMや効果音のエミュレートをすることが出来る。
  - CD-ROM
    ゲームを読み込むためのプラグイン。このプラグインはePSXeに初めから同封されている。サードパーティの多くは、CD-ROMの読み込みを7種類までエミュレートすることが可能である。
  - Input
    コントローラー関連のプラグイン。同封のプラグインでも十分であるが、他にもより多くの機能を持つプラグインも存在する。

### 互換性

ePSXeは多くのプレイステーションのゲームが動作する。 しかし多くの試行錯誤と設定の変更なしに完璧に動作するゲームはない。 ゲームが正常に動作しない場合は、利用可能なパッチを適用することで、正常動作をするものもある。

## 動作推奨環境

### PCバージョン

  - CPU: 800 MHz以上のCPU （推奨: [デュアルコア](https://ja.wikipedia.org/wiki/デュアルコア "wikilink")搭載CPU)
  - RAM: 256MB RAM　(推奨: 512MB RAM)
  - ビデオカード: [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 8.0、[OpenGL](../Page/OpenGL.md "wikilink") 1.0をサポートするビデオカード （推奨: OpenGL 2.0)
  - OS: Windows、MacOS、Linux
  - CD-ROM: 16x　もしくはそれ以上(任意)

### Androidバージョン

  - CPU: ARM もしくはx86(Intel Atom)
  - OS: Android2.2以降

## 脚注

## 外部リンク

  - [公式サイト（英語）](http://www.epsxe.com/)

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink")