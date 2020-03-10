> この記事は[Parallels Workstation](https://ja.wikipedia.org/wiki/Parallels_Workstation)から翻訳されています。


**Parallels Workstation** は、[パラレルス](../Page/パラレルス.md "wikilink")の最初の商用ソフトウェア製品。同社は[仮想化](../Page/仮想化.md "wikilink")ソフトウェアの開発を専門とするソフトウェア企業。Parallels Workstation は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースのコンピュータ（OSは [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") または [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")）向けの[仮想機械](../Page/仮想機械.md "wikilink")であり、x86仮想コンピュータを複数同時に生成・実行することができる。基本的に店頭販売せず、ダウンロードパッケージとして配布されている。（[Macintosh](../Page/Macintosh.md "wikilink")向けの製品は [Parallels Desktop](https://ja.wikipedia.org/wiki/Parallels_Desktop "wikilink")）

## 実装

他の仮想化ソフトウェアと同様、Parallels Workstation は[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")技術を使っている。ハイパーバイザとは、プライマリOSとホストコンピュータの間に置かれる薄いソフトウェア層である。ハイパーバイザはホストマシンのハードウェアリソースの一部を直接制御し、仮想機械モニタとプライマリOSの両方にそれらリソースへのインタフェースを提供する。これにより、仮想化ソフトウェアのオーバーヘッドを低減する。Parallels Workstation のハイパーバイザは、インテルの [Virtualization Technology](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") (VT) やAMDの Secure Virtual Machine (SVM) といったハードウェア仮想化技術もサポートしている。

## 機能

Parallels Workstation はハードウェアエミュレーション仮想化ソフトウェアであり、仮想機械エンジンによって各仮想機械は自前の[CPU](../Page/CPU.md "wikilink")、[RAM](../Page/Random_Access_Memory.md "wikilink")、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、[CD-ROM](../Page/CD-ROM.md "wikilink")ドライブ、[入出力](../Page/入出力.md "wikilink")機器、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")など、実際のコンピュータを構成する全ての要素を持つことができる。Parallels Workstation は仮想環境内のあらゆるデバイスを仮想化し、それには[GPUや](../Page/Graphics_Processing_Unit.md "wikilink")[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")、ハードディスクアダプタなども含まれる。また、[パラレルポート](https://ja.wikipedia.org/wiki/パラレルポート "wikilink")や[USBデバイスのためのパススルードライバも提供している](../Page/ユニバーサル・シリアル・バス.md "wikilink")。

ゲスト仮想機械はホストコンピュータの実際のハードウェアとは無関係に全て同じハードウェアドライバを使っているため、仮想機械インスタンスはコンピュータ間での可搬性が高い。例えば、動作中の仮想機械を一時停止し、別の物理コンピュータにコピーし、再スタートさせることが可能である。

Parallels Workstation は標準的なPCのハードウェアを完全に仮想化でき、以下のようなものも仮想化対象となる\[1\]。

  - [Pentiumまたは](../Page/Intel_Pentium_\(1993年\).md "wikilink")[Duron](../Page/Duron.md "wikilink")プロセッサ
  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") i815チップセット互換の[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")
  - 最大1.5GBの[RAM](../Page/Random_Access_Memory.md "wikilink")（ただし、i815は実際には512MBまでしかメモリをサポートしていない）
  - [VGAおよび](../Page/Video_Graphics_Array.md "wikilink")[SVGAビデオカード](../Page/Super_Video_Graphics_Array.md "wikilink")（VESA 3.0 サポート）
  - 1.44MB[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")。実際の物理装置にマッピングすることもできるし、イメージファイルにマッピングすることもできる。
  - 最大4個の[IDEデバイス](../Page/Advanced_Technology_Attachment.md "wikilink")。仮想ハードドライブは20MBから128GBまで可能で、仮想 CD/DVD-ROM ドライブもある。IDEデバイスは物理装置にマッピングすることもできるし、イメージファイルにマッピングすることもできる。
  - 最大4個の[シリアルポート](../Page/シリアルポート.md "wikilink")。実際のポートにマッピングすることもできるし、パイプや出力ファイルにマッピングすることもできる。
  - 最大3個の双方向[パラレルポート](https://ja.wikipedia.org/wiki/パラレルポート "wikilink")。実際のポートにマッピングすることもできるし、プリンターや出力ファイルにマッピングすることもできる。
  - Realtek RTL8029 (AS) 互換の仮想[イーサネット](../Page/イーサネット.md "wikilink")カード
  - 2ポートUSB 1.1 コントローラ
  - [AC97互換サウンドカード](../Page/Audio_Codec_97.md "wikilink")
  - 104キーWindows対応キーボードとPS/2ホイール付きマウス

## 既知の問題点

Parallels Workstation には[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")3月現在、以下のような問題（制限）がある。

  - 32ビットのOSしか実行できない。
  - 1つの仮想機械インスタンスに複数個のCPUを割り当てることができない。
  - DVD / CD-ROMのパススルーアクセスが実装されていないため、ゲスト仮想機械が排他的に装置を使ってDVDやCDを焼くことができない。
  - 全仮想機械のメモリ容量の合計は最大4GBで、個々の仮想機械では最大1.5GBまで。
  - ネットワークエミュレーションでは[NATをサポートしていない](../Page/ネットワークアドレス変換.md "wikilink")\[2\]。

## 関連項目

  - [VMware Workstation](https://ja.wikipedia.org/wiki/VMware "wikilink")
  - [ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")
  - [仮想アプライアンス](../Page/仮想アプライアンス.md "wikilink")
  - [仮想機械](../Page/仮想機械.md "wikilink")
  - [仮想化](../Page/仮想化.md "wikilink")
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")

## 脚注

[Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.
2.