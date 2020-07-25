> この記事は[QEMU](https://ja.wikipedia.org/wiki/QEMU)から翻訳されています。


**QEMU**（キューエミュ）は、[Fabrice Bellardが中心となって開発しているオープンソースのプロセッサ](https://ja.wikipedia.org/wiki/w:Fabrice_Bellard "wikilink")[エミュレータ](../Page/エミュレータ.md "wikilink")である。

## 概要

QEMUは機械全体をエミュレーションするシステムエミュレーションと呼ばれる環境と、[Linux](../Page/Linux.md "wikilink")の[ユーザーランドをエミュレーションするユーザーエミュレーションと呼ばれる環境がある](../Page/オペレーティングシステム.md "wikilink")。

ユーザーエミュレーション環境は、非特権モードのエミュレーションおよび、Linuxのシステムコール命令をネイティブのシステムコールに変換する。この環境は、組み込み機器の[クロスコンパイルや非](../Page/クロスコンパイラ.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")環境で[Wine](../Page/Wine.md "wikilink")を動かすために使用可能である。

システムエミュレーション環境は主に[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")などの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) を動かすことを目的に利用されており、OSの動作確認用としてQEMUを同梱する事がある。[携帯電話](../Page/携帯電話.md "wikilink")用プラットフォーム[Android](../Page/Android.md "wikilink")の[SDKにも利用されている](../Page/ソフトウェア開発キット.md "wikilink")。同様のプロジェクトには[Bochs](../Page/Bochs.md "wikilink")や[PearPC](../Page/PearPC.md "wikilink")などがあるがQEMUの特徴として、[中間コードを介して](../Page/中間言語.md "wikilink")[動的コンパイルを行うことにより](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")、x86、[PowerPC](../Page/PowerPC.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink")、[ARMなど多くのホスト](../Page/ARMアーキテクチャ.md "wikilink")[CPU](../Page/CPU.md "wikilink")に対して多くのターゲットCPUを高速にエミュレーション可能である事が挙げられる。x86システムエミュレーション環境に於いては[BIOSの動作環境はBochsと互換である](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。

かつては、アクセラレータとして、kqemuが用意されていた。バージョン 0.11 で廃止になり、これは [KVM](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink") になった。kqemu は、QEMUをより速く動作させる[モジュール](../Page/モジュール.md "wikilink")として提供されていた。kqemuは、x86又は[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")（[64ビット](../Page/64ビット.md "wikilink")CPU）をサポートしており、[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")の[仮想化](../Page/仮想化.md "wikilink")モニタとして動作する。これを使用するときには、同様のソフトウエアである[VMware](../Page/VMware.md "wikilink")同様、ホストCPUの実行できないコードをターゲットに於いて実行することは出来ない。Linux 2.4 及び 2.6上にて提供されている。[FreeBSD](../Page/FreeBSD.md "wikilink")並びにWindows NT/2000/2003/XPにおいては、実験的な提供がなされている。この部分は[HALを使って書かれたバイナリオブジェクトとサポートされているプラットフォーム用のHALのソースとして提供されており](https://ja.wikipedia.org/wiki/Hardware_Abstruction_Layer "wikilink")、商業的な配布には制限がある。

QEMUはCPUだけではなく、各種の周辺ハードウェアもエミュレートしている。以下にQEMUが実装している[PC](../Page/パーソナルコンピュータ.md "wikilink")（[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")）ハードウェアを示す。

  - [Intel 440FX](https://ja.wikipedia.org/wiki/Intel_440FX "wikilink") host PCI bridge and PIIX3 PCI to ISA bridge
  - [Intel Q35](https://ja.wikipedia.org/wiki/Intel_Q35 "wikilink") and [ICH9](https://ja.wikipedia.org/wiki/ICH9 "wikilink") Chipset
  - Cirrus CLGD 5446 PCI VGA card or dummy VGA card with Bochs VESA extensions (hardware level, including all non standard modes).
  - Red Hat QXL VGA or VirtIO GPU
  - Simulated VMware SVGA II(Include Bug)
  - [PS/2のマウスとキーボード](https://ja.wikipedia.org/wiki/PS/2コネクタ "wikilink")
  - 2 PCI IDE interfaces with hard disk and CD-ROM support
  - SATA Controller
  - SCSI Controller
  - SAS Controller
  - Floppy disk
  - ISA network adapters
  - Intel E1000 Network Adapter
  - Realtek 8139 Network Adapter
  - VirtIO Block Storage/SCSI/Network
  - [シリアルポート](../Page/シリアルポート.md "wikilink")
  - Creative [Sound Blaster 16](../Page/Sound_Blaster.md "wikilink") サウンドカード
  - ENSONIQ AudioPCI ES1370 sound card
  - Adlib(OPL2) - Yamaha YM3812 compatible chip
  - Intel 82801AA [AC97互換サウンドカード](../Page/Audio_Codec_97.md "wikilink")
  - [HD Audioサウンドカード](../Page/High_Definition_Audio.md "wikilink")
  - CS4231A compatible sound card
  - PCI UHCI USB controller and a virtual USB hub.

また、QEMUは-sオプションを指定すれば[tun](https://ja.wikipedia.org/wiki/tun "wikilink")デバイスを介してホスト上の[GDBと接続](../Page/GNUデバッガ.md "wikilink")、仮想マシンの動作状況を監視できるなど、[インサーキット・エミュレータ](../Page/インサーキット・エミュレータ.md "wikilink") (ICE) のような使い方も可能である。 そのほかに、QEMUは、[VNCや](../Page/Virtual_Network_Computing.md "wikilink")[SPICEサーバの機能が組み込まれており](https://ja.wikipedia.org/wiki/:en:SPICE_\(protocol\) "wikilink")、この機能により、リモートマシンの制御が可能である。

対応する仮想化支援機能が少なく、[VMware](../Page/VMware.md "wikilink")、[VirtualBox](../Page/VirtualBox.md "wikilink")よりも低速とされる。

## 関連項目

  - [バーチャルマシン](https://ja.wikipedia.org/wiki/バーチャルマシン "wikilink")
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")
  - [Microsoft Virtual PC](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink")
  - [Q](../Page/Q_\(エミュレータ\).md "wikilink")
  - [VirtualBox](../Page/VirtualBox.md "wikilink")
  - [VMware](../Page/VMware.md "wikilink")

## 外部リンク

  -
[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")