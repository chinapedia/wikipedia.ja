> この記事は[ PV4](https://ja.wikipedia.org/wiki/_PV4)から翻訳されています。


**PV4**とは、アースソフトが開発し販売していた、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")[アナログコンポーネント](https://ja.wikipedia.org/wiki/コンポーネント映像信号 "wikilink")[ビデオキャプチャボードである](https://ja.wikipedia.org/wiki/キャプチャ_\(録画ソフト\) "wikilink")。

## 概要

PV4は、その出自であるPVシリーズをベースに[ザイリンクス](https://ja.wikipedia.org/wiki/ザイリンクス "wikilink") [FPGA](../Page/プログラマブルロジックデバイス.md "wikilink") XC3S200A-4FTG256Cを採用し、コストダウンを計りながらも[ハイビジョン](../Page/ハイビジョン.md "wikilink")最大解像度1920x1080iに対応したビデオキャプチャカードである。XC3S200AのPCIマクロブロックは3.3V PCIバスのみ対応の為、PV4は5Vスロットで使用出来ない。[カードエッジ](https://ja.wikipedia.org/wiki/カードエッジ "wikilink")は3.3V/5V兼用に切り込みが入れてある為、5Vスロットにも差し込めるがその場合intel ICH9のような3.3V駆動5Vトレラントのサウスブリッジ以外ではボードが壊れてしまう（実質的には[ICH9登場前まではAMD](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ#ICH9 "wikilink") CPU向けチップセットでしか使用できなかった）。ビデオ信号入力はD端子接続となっており、あわせて[S/PDIF](https://ja.wikipedia.org/wiki/S/PDIF "wikilink")音声入力コネクタを併せ持つ。2系統コネクタがあり、ソフトウエアからコネクタを切り替える事ができる。[CGMS-Aに対しては一切の制限がなく](https://ja.wikipedia.org/wiki/コピーガード "wikilink")、[ARIBが言う所の](https://ja.wikipedia.org/wiki/電波産業会 "wikilink")[無反応機](https://ja.wikipedia.org/wiki/無反応機 "wikilink")の一種にあげられる。ハイビジョン放送、[Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")、[HD-DVD](https://ja.wikipedia.org/wiki/HD-DVD "wikilink")、[NTSC](../Page/NTSC.md "wikilink")準拠の映像をキャプチャーできる。FPGAを利用する事により少数ロットで低価格なハードウエアが実際に作れる事を実証している民生品の一つである。なお、2008年11月7日で生産終了した。

## ビデオキャプチャ

ビデオキャプチャはFPGA上でY・Pb・PrのAD変換処理と解像度変換処理、音声入力の同期までを行った非圧縮状態で[ビデオカード](../Page/ビデオカード.md "wikilink")もしくは[メモリに](../Page/主記憶装置.md "wikilink")[DMA転送する](../Page/Direct_Memory_Access.md "wikilink")。Y信号2バイト、Pb・Pr信号各1バイトをハイビジョンベースバンド最大30MHzで転送する為、PCIバスの帯域を最大120MB/sec占有する。この為ハードディスクインターフェースとPV4が挿入されているPCIバスが分離されていない場合キャプチャ可能最大解像度が低下する。また画像を上下2分割×偶数/奇数ライン別の4分割で処理する為、最低限でもデュアルコアCPUが望ましく、ICH9R対応ドライバが開発されるまでは実質的に[Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")・[Athlon64 X2のみが最大解像度を処理できた](https://ja.wikipedia.org/wiki/Athlon64_X2 "wikilink")（初期モデルはAthlon64 X2環境でしか動作できなかったが修正ファームによって解消され現在は[Intel Core2Duo](https://ja.wikipedia.org/wiki/Intel_Core2 "wikilink")、Core2Quad、[AMD Phenomシリーズで最大解像度を扱える](../Page/AMD_Phenom.md "wikilink")。最大解像度1920x1080iにこだわらなければ地上波デジタルの1440x1080i解像度でより、広い範囲のCPUが使用できる）。圧縮はデータフォーマットの基本規格を[SMPTE](https://ja.wikipedia.org/wiki/SMPTE "wikilink")・[MPEGに準拠しつつも](../Page/Moving_Picture_Experts_Group.md "wikilink")、マルチコアで分割処理した情報を統合しないで格納する独自コンテナにリアルタイムで格納し、ハードディスクに記録する。プレビューのみの場合はFPGA上でビデオカード上で表示可能な信号を直接生成する為、視聴するのみであればCPU能力は殆ど必要としない。

## トランスコード

トランスコード処理用として[Aviutl](https://ja.wikipedia.org/wiki/Aviutl "wikilink")用の[プラグイン](../Page/プラグイン.md "wikilink")を提供している。これにより独自コンテナに格納された映像記録を、[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")や[MPEG2](https://ja.wikipedia.org/wiki/MPEG2 "wikilink")など汎用フォーマットに変換する事ができる。トランスコード処理はビデオキャプチャ処理よりもCPU負荷が高い。またPVシリーズのユーザーが開発したリアルタイムトランスコード用DLLがあり、キャプチャと同時にトランスコード処理が行う事もできる。ただしこの場合PCIバスの帯域を消費し、メモリにDMA転送が行われている上で、さらに非圧縮信号を汎用フォーマットに変換する為、プラグインによるトランスコード処理よりもさらなるCPU負荷がかかる為、最大解像度の制限はより厳しい。

## デジタル放送との関係

[ダビング10](../Page/ダビング10.md "wikilink")が提唱される迄は、PVシリーズの様な無反応機に対して、アナログコンポーネント信号をコピー制御ビットによって、2001年時点では720pに、後に525iまでダウンコンバートして出力するという対策を実施するか否か、2011年アナログ放送停波までに結論を出す計画であった。しかし、これは同時に既にユーザーの手に行き渡っているアナログハイビジョンテレビも全て解像度を低下させる事になり、メーカはもとより消費者の反発を受ける事は免れない計画であった。コピーワンスの計画にあったコピー制御ビットの操作による解像度低下に関する事項はダビング10の計画からは削除され、2008年現在白紙の状態にある（PC用チューナカードのメーカーは自ら自主規制を行い、権利者はそのような事は全く要請していないとImpress社の取材に答えている）。[著作権侵害](https://ja.wikipedia.org/wiki/著作権侵害 "wikilink")コンテンツの著しい流通、また[フリーオ](../Page/フリーオ.md "wikilink")や[PT2](https://ja.wikipedia.org/wiki/PT2 "wikilink")のようなデジタル無反応機の登場、[B-CAS](https://ja.wikipedia.org/wiki/B-CAS "wikilink")カードの存在意義そのものに所轄省庁である[総務省](../Page/総務省.md "wikilink")が疑問を呈して問題の整理にかかるなど、消費者の権利とコンテンツホルダーの権利のバランスは既に崩れており、今後の動向は全く不明である。

## 関連項目

  - [録画](https://ja.wikipedia.org/wiki/録画 "wikilink")
  - [TVチューナー](https://ja.wikipedia.org/wiki/TVチューナー "wikilink")

## 外部リンク

  - 有限会社アースソフト 公式HP
      - [PV4 目次（バージョン3.5以降の情報）](http://earthsoft.jp/PV/)
      - [PV4/PV3 共通目次（バージョン3.1.2(2007年9月9日) ～ バージョン3.4.3(2008年6月15日)の情報）](http://earthsoft.jp/PV4_PV3/index.html)

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:画像処理](https://ja.wikipedia.org/wiki/Category:画像処理 "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink")