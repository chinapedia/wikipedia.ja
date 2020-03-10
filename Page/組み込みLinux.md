> この記事は[Linux](https://ja.wikipedia.org/wiki/Linux)から翻訳されています。


**組み込みLinux**（くみこみ-、）とは、[組み込みシステム](../Page/組み込みシステム.md "wikilink")に特化した[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")や[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")、またはそれら搭載する組み込み機器を指す用語である。[携帯電話](../Page/携帯電話.md "wikilink")や[携帯情報端末](../Page/携帯情報端末.md "wikilink")、メディアプレイヤーなどの家電機器、[ネットワーク機器](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[ファクトリーオートメーション](../Page/ファクトリーオートメーション.md "wikilink")装置、[カーナビ](../Page/カーナビゲーション.md "wikilink")、医療機器など様々な組み込みシステムにて利用されている。米VDC (Venture Development Corporation) の[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")における調査によると、Linux は18%の組み込みエンジニアが使用しているとされる\[1\]。

## 通常のLinuxとの違い

デスクトップおよび[サーバ](../Page/サーバ.md "wikilink")などの汎用的なシステムと異なり、組み込みシステムでは[リソースが制限されており](../Page/計算資源.md "wikilink")、例えば[RAMや](../Page/Random_Access_Memory.md "wikilink")[二次記憶装置の容量が小さい](../Page/補助記憶装置.md "wikilink")。組み込みLinuxを使った機器は、二次記憶装置として[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")の代わりにより小さい[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")を使うことが多い。組み込みLinuxはアプリケーションや対象ハードウェアに必要な機能に特化されていることが多く、Linuxカーネルもそのアプリケーションに対し最適化し構成されている。最適化の具体的な例は、OSの[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")化などである。

## 開発

一般的にLinuxは[移植性にすぐれるシステムであると言われており](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")、デスクトップコンピュータやサーバにあまり採用されていない[コンピュータ・アーキテクチャ](../Page/コンピュータ・アーキテクチャ.md "wikilink")にも移植されている。その中には組み込みシステムも含まれている。

組み込みシステムへのオペレーティングシステムの移植には[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[アセンブラや](../Page/アセンブリ言語.md "wikilink")[C](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")、[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")を利用するケースもあるが、それらと比較して、OS自体の[ソースコード](../Page/ソースコード.md "wikilink")を修正して再配布でき、[ロイヤルティー](https://ja.wikipedia.org/wiki/ロイヤルティー "wikilink")やライセンス料が発生しないといった[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")/[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアとしての特徴だけではなく技術的な優位点もあり、使用メモリ量が比較的少なく（2MB以下のメモリで起動可能）、安定した動作、比較的サポートベースが大きい、などの利点がある。組み込みLinuxは、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")に少数の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")を組み合わせたものである。[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")には[glibcの代わりに](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")、もっとリソース消費量の少ない [dietlibc](https://ja.wikipedia.org/wiki/dietlibc "wikilink")、[uClibc](https://ja.wikipedia.org/wiki/uClibc "wikilink")、[Newlib](https://ja.wikipedia.org/wiki/Newlib "wikilink")が採用される場合もある。

2006年05月、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")開発者の[グレッグ・クロー＝ハートマン](https://ja.wikipedia.org/wiki/グレッグ・クロー＝ハートマン "wikilink")によりLinuxのドライバ開発キットがリリースされた\[2\]。また、[Linux Foundation](../Page/Linux_Foundation.md "wikilink")（以前は[OSDL](https://ja.wikipedia.org/wiki/Open_Source_Development_Labs "wikilink")）によって開発のトレーニング講座や無料の[ウェビナー](https://ja.wikipedia.org/wiki/ウェビナー "wikilink")が開かれている。

組み込みLinuxに使われるオープンソースの[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")としては、[BusyBox](https://ja.wikipedia.org/wiki/BusyBox "wikilink")などのオールインワンなものや、[Samba](https://ja.wikipedia.org/wiki/Samba "wikilink")や[WebKit](https://ja.wikipedia.org/wiki/WebKit "wikilink")、[FreeType](../Page/FreeType.md "wikilink")などのプロプライエタリな代替が少なくかつ重要なものも多い。また、[Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink")や[Moblin](https://ja.wikipedia.org/wiki/Moblin "wikilink")、[Android](../Page/Android.md "wikilink")のようにミドルウェアの大部分をオープンソースで改めて開発するものや、[Palm WebOSのようにミドルウェアの多数の部分にオープンソースソフトウェアを組み合わせて使うものもある](https://ja.wikipedia.org/wiki/Palm_WebOS "wikilink")。マルチメディアに関してはオープンソースで扱う場合、[GStreamer](https://ja.wikipedia.org/wiki/GStreamer "wikilink")経由でハードウェアデコーダと[FFmpeg](../Page/FFmpeg.md "wikilink")をバックエンドにして使われることが多いが、[Android](../Page/Android.md "wikilink")においては[OpenCore](https://ja.wikipedia.org/wiki/OpenCore "wikilink")が使われている。

開発環境としては[Eclipseか](../Page/Eclipse_\(統合開発環境\).md "wikilink")、商用製品が使われることが多い。Eclipseでは組み込みにおいて以下のプラグインが使われる。

  - Eclipse C/C++ Development Tooling (CDT) - EclipseでのCやC++の開発に必須
  - Target Management (RSE)
  - Linux Tools Project - プロファイラや動的解析などの機能を統合
  - Tools for mobile Linux (TmL)
  - EGit - バージョン管理システムの一つ、[Git](https://ja.wikipedia.org/wiki/Git "wikilink")の統合
  - Mylyn - バグトラッカの統合

また、Eclipseには[Moblin Eclipse Plug-inや](https://ja.wikipedia.org/wiki/Moblin_Eclipse_Plug-in "wikilink")[Android Development Tools](https://ja.wikipedia.org/wiki/Android_Development_Tools "wikilink") (ADT) など特定のOSに特化したプラグインも存在する。 また、開発にはエミュレータの[Qemu](https://ja.wikipedia.org/wiki/Qemu "wikilink")や分散コンパイルの為の[distcc](https://ja.wikipedia.org/wiki/distcc "wikilink")や[icecc](https://ja.wikipedia.org/wiki/icecc "wikilink")なども使われる。

## シェア

### スマートフォン

[Gartnerのプレスリリースによると](../Page/ガートナー.md "wikilink")、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")のLinuxのシェアは8.1%としている\[3\]。AdMobのレポートによると、全世界のモバイルデバイスにおいてLinuxカーネルを採用しているOSである[Android](../Page/Android.md "wikilink")と[Palm WebOSを合わせたシェアは](https://ja.wikipedia.org/wiki/Palm_WebOS "wikilink")2009年8月時点で11%であり、2009年2月の2%と比べ9%伸びている\[4\]。また、AdMobの2010年2月のレポートによると、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")におけるAndroidのシェアは24%に達し、2位になったとしている\[5\]。

日本では、NTTドコモの制定したMOAP(L)及びALPベースの[FOMA](../Page/FOMA.md "wikilink")端末用[オペレータパック](https://ja.wikipedia.org/wiki/オペレータパック "wikilink")に使われている。

### テレビ

日本では、ネットワーク接続可能なハイエンド機種のテレビにはほぼLinuxが搭載されている\[6\]。

### ゲームコンソール

ゲームコンソール（[コンシューマーゲーム](../Page/コンシューマーゲーム.md "wikilink")）において、Linuxが使われる例は少ない。

PS2においては、[PS2 Linuxがハード込みで発売された](../Page/PS2_Linux.md "wikilink")。また、[PlayStation BB UnitにはLinuxが使われている](../Page/PlayStation_BB_Unit.md "wikilink")。PS3においてはLinuxがインストールできることを売りにしていたが、新型を出した際にオミットされた。また、旧型PS3においてもファームウェア更新によって無効化された。

近年ではスマートフォンのゲーム市場が活性化されており\[7\]、[Android](../Page/Android.md "wikilink")でのゲーム市場も急速に成長している\[8\]。そのため[Xperia Playや](https://ja.wikipedia.org/wiki/Xperia_Play "wikilink")[ODROID](https://ja.wikipedia.org/wiki/ODROID "wikilink")のような[Android](../Page/Android.md "wikilink")を使った携帯ゲーム端末が出始めている。

その他、直接組み込みLinuxが使われているコンソールとしては、[GP2X](https://ja.wikipedia.org/wiki/GP2X "wikilink")/[GP2X Wizや](https://ja.wikipedia.org/wiki/GP2X_Wiz "wikilink")[LeapFrog Didj](https://ja.wikipedia.org/wiki/LeapFrog_Didj "wikilink")、[Pandora](https://ja.wikipedia.org/wiki/Pandora "wikilink")、[EVO Smart Consoleなどがある](https://ja.wikipedia.org/wiki/EVO_Smart_Console "wikilink")。

## Linuxカーネルの組み込み向け機能

以下は、組み込み機器に特化したLinuxカーネルの機能である。"CONFIG_\*"という表記はカーネルコンフィグレーションであり、コンパイルする際に機能を有効化するための識別子となる。Linuxカーネルは[モノリシックであるため](../Page/モノリシックカーネル.md "wikilink")、カーネルコンパイル時に必要とする機能を有効化する。

  - 多くのCPUアーキテクチャやハードウェアプラットフォームで動作
      - [MMU](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink") (メモリ管理ユニット)の無いCPUでも動作可能 (CONFIG_MMU=n)
  - 少ない資源でも動作
      - [XIP](https://ja.wikipedia.org/wiki/XIP "wikilink") (Execute in place)
      - 読み出し専用ファイルシステム ([romfs](https://ja.wikipedia.org/wiki/romfs "wikilink")、[cramfs](https://ja.wikipedia.org/wiki/cramfs "wikilink")や[SquashFS](https://ja.wikipedia.org/wiki/SquashFS "wikilink")など)
      - サイズを削ることができる ([Linux Tinyなど](https://ja.wikipedia.org/wiki/Linux_Tiny "wikilink"))
      - シングルプロセッサに最適化可能 (CONFIG_SMP=n)
      - メモリ内圧縮スワップによるメモリの有効活用 (ramzswap(compcache))
      - [NAND型フラッシュメモリ](https://ja.wikipedia.org/wiki/NAND型フラッシュメモリ "wikilink")を直接使用可能 ([JFFS2](https://ja.wikipedia.org/wiki/JFFS2 "wikilink")や[UBIFS](https://ja.wikipedia.org/wiki/UBIFS "wikilink"))
  - タイトな用途にも使用可能
      - マウントの早いファイルシステム ([YAFFS2](https://ja.wikipedia.org/wiki/YAFFS2 "wikilink")など)
      - [ソフトリアルタイム](https://ja.wikipedia.org/wiki/ソフトリアルタイム "wikilink") (CONFIG_PREEMPT)
      - [ハードリアルタイム](https://ja.wikipedia.org/wiki/ハードリアルタイム "wikilink") (CONFIG_PREEMPT_RT patch set)
      - ユーザーアプリケーションのリソース制限 (rlimit, [cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink")など)
      - [サンドボックス](https://ja.wikipedia.org/wiki/サンドボックス_\(セキュリティ\) "wikilink") (seccomp)
      - コンテナ ([LXC](https://ja.wikipedia.org/wiki/LXC "wikilink"))
      - リブート不要なセキュリティパッチ ([Ksplice](https://ja.wikipedia.org/wiki/Ksplice "wikilink"))

なお、AMP (非対称型[マルチプロセッシング](https://ja.wikipedia.org/wiki/マルチプロセッシング "wikilink")) にはまだ対応していない。[Renesasと](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink")[TIはそれぞれ異なったVirtioベースの仕組みを提案している](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")\[9\]\[10\]。

## 他の組み込みOSとの比較

  - ミドルウェアが豊富
      - POSIX互換であるためUNIX系のミドルウェアが使える
      - TCPスタック、LANスタック、Wifiスタック、Bluetoothスタック、USBスタックなどの各種プロトコルスタックが揃っている
  - 開発しやすい
      - PC上である程度の開発が可能
          - Linuxカーネルはアーキテクチャー毎に開発されているのではなく、デスクトップ、サーバー、組み込み、[メインフレーム](../Page/メインフレーム.md "wikilink")に関わりなく、共通のソースベースで開発されており、アーキテクチャー相互のソースレベルでの互換性は高い
          - [GCC](../Page/GNUコンパイラコレクション.md "wikilink")、[GNU Binutilsを利用してクロスビルドツール](https://ja.wikipedia.org/wiki/GNU_Binutils "wikilink")（[クロスコンパイラ](../Page/クロスコンパイラ.md "wikilink")、クロスリンカなど）を用意することもでき、ビルドまではPC上ですべての開発が可能
      - カーネルがモジュール化されているため、再起動なくモジュールの開発が可能（[ローダブル・カーネル・モジュール](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink")）
      - [NFSが使えるため](https://ja.wikipedia.org/wiki/Network_File_System "wikilink")、ファイル転送が容易
      - tftpbootが使えるため、カーネル切り替えが容易
      - gdbserverが使えるため、リモートデバッグが容易に可能
      - distccを使った分散コンパイルが容易に可能
  - 機能が豊富、設定も柔軟（反面、複雑ともいえる）
      - カーネルのコンパイルオプション(.config)には汎用OS向けのものも含まれる（共通のソースベースを利用しているため）
      - カーネルのコンパイルオプション(.config)には組み込み向けの設定も多いが、その多くが何らかの資源や機能とのトレードオフであるため、知識が必要になる。
      - カーネル全体の状態の取得・動的な調整が可能 ([/sys](https://ja.wikipedia.org/wiki/sysfs "wikilink")/以下, [/proc](https://ja.wikipedia.org/wiki/procfs "wikilink")/sys/ 以下, sysctlなどでチューニング可能)
          - ネットワークバッファ
      - プロセス毎の状態の取得・動的な調整が可能 (/proc/プロセス番号/ 以下, rlimitなど)
          - メモリ逼迫時のOOMキラーにより[kill](https://ja.wikipedia.org/wiki/kill "wikilink")されるプロセスの優先順位の設定
      - 動作中のカーネルから別カーネルへ再起動をかけず瞬時に切り替え可能 (コールドブート機能。[kexec](https://ja.wikipedia.org/wiki/kexec "wikilink"))
  - オープンソースである
      - 自由に改良することができる（それぞれ[ソフトウェアライセンス](../Page/ソフトウェアライセンス.md "wikilink")により条件や義務が異なるが、少なくとも改変や再頒布に関しては[ロイヤルティー・フリーで自由に可能である](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")）
      - 世界中の企業・団体・個人・政府機関による持続的な開発が行われている
          - 脆弱性も調べられているため、セキュリティが高い
      - サポート企業・団体が複数ある
      - 機能の開発を依頼できる所が多い
      - 開発講座が多い
      - 採用前に工数を見積もれる
      - Linuxカーネルなどは[GPLでライセンスされているため](../Page/GNU_General_Public_License.md "wikilink")、機器の販売など*配布を伴う*場合はソースコードの開示が必要となる（しかし配布を伴わないケース、例えば「自組織内で私的に流用するのみ」ならばソースコードを一切開示する必要はない）。
          - ソースコードの提供によりOSSコミュニティにコードが還元され、ソフトウェアの機能向上につながり、結果として自社製品の機能強化につながる可能性もある。
          - 採用事例が多く公開されている
  - デバッグ/プロファイリングの仕組みが豊富
      - カーネルのロック依存性動的チェック ([lockdep](https://ja.wikipedia.org/wiki/lockdep "wikilink") (CONFIG_LOCKDEP_SUPPORT。標準で有効))
      - カーネルのデバッグログの個別動的有効無効切り替え ([ddebug](https://ja.wikipedia.org/wiki/ddebug "wikilink") (dynamic debug。CONFIG_DYNAMIC_DEBUG))
      - カーネル用のデバッガ ([KDB](https://ja.wikipedia.org/wiki/KDB "wikilink"), [KGDB](https://ja.wikipedia.org/wiki/KGDB "wikilink"), [KGTP](https://ja.wikipedia.org/wiki/KGTP "wikilink")(パッチ))
      - カーネルプローブ([kprobe](https://ja.wikipedia.org/wiki/kprobe "wikilink"), [jprobes](https://ja.wikipedia.org/wiki/jprobes "wikilink"), [SystemTap](https://ja.wikipedia.org/wiki/SystemTap "wikilink"))
      - ユーザー空間プローブ ([uprobes](https://ja.wikipedia.org/wiki/uprobes "wikilink") (パッチ))
      - カーネル内イベントトレーサ ([ftrace event tracer](https://ja.wikipedia.org/wiki/ftrace_event_tracer "wikilink"), [kprobe-based event tracer](https://ja.wikipedia.org/wiki/kprobe-based_event_tracer "wikilink"), GDB tracepoint support(パッチ), trace-cmd, KernelShark)
      - システムコールトレーサ ([strace](https://ja.wikipedia.org/wiki/strace "wikilink"))
      - プロセストレーサ ([ptrace](https://ja.wikipedia.org/wiki/ptrace "wikilink"), [utrace](https://ja.wikipedia.org/wiki/utrace "wikilink"))
      - 共有ライブラリトレーサ ([ltrace](https://ja.wikipedia.org/wiki/ltrace "wikilink"))
      - ユーザランド用デバッガ ([GDB](../Page/GNUデバッガ.md "wikilink"))
      - プロファイリング ([gcov](https://ja.wikipedia.org/wiki/gcov "wikilink") (カーネルではGCOV_KERNEL), [OProfile](https://ja.wikipedia.org/wiki/OProfile "wikilink"), [perf tools](https://ja.wikipedia.org/wiki/perf_tools "wikilink"))
      - ロック競合のチェック (lock_stat, perf lock)
      - 各種ベンチマーク (perf bench, ffsbなど)
      - ハードウェアによって生まれるレイテンシの検出 ([Hardware Latency Detector](https://ja.wikipedia.org/wiki/Hardware_Latency_Detector "wikilink") (rtパッチ))
      - モニタリング (top, htop, iotop, slabtop, xrestop, latencytop, powertop, apachetopなど)
      - 動的カーネル内メモリ管理バグチェッカ ([Kmemcheck](https://ja.wikipedia.org/wiki/Kmemcheck "wikilink"), [Kmemleak](https://ja.wikipedia.org/wiki/Kmemleak "wikilink"))
      - 動的メモリ管理・スレッドバグチェッカ ([Valgrind](https://ja.wikipedia.org/wiki/Valgrind "wikilink") (UserModeLinux+パッチを使うことでカーネルのチェックも可能))
      - 静的解析 ([Clang Static Analyzer](https://ja.wikipedia.org/wiki/Clang_Static_Analyzer "wikilink"), [Smatch](https://ja.wikipedia.org/wiki/Smatch "wikilink"), [Coccinelle](https://ja.wikipedia.org/wiki/Coccinelle_\(ソフトウェア\) "wikilink"))
      - ロギング ([MRTG](https://ja.wikipedia.org/wiki/MRTG "wikilink"), [Nagios](../Page/Nagios.md "wikilink"), [Xymon](https://ja.wikipedia.org/wiki/Xymon "wikilink"), [Zabbix](https://ja.wikipedia.org/wiki/Zabbix "wikilink"), [Hinemos](https://ja.wikipedia.org/wiki/Hinemos "wikilink"), [Cacti](https://ja.wikipedia.org/wiki/Cacti "wikilink"), [Munin](https://ja.wikipedia.org/wiki/Munin "wikilink")など)
      - リモート管理 ([OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH "wikilink"), [adb](https://ja.wikipedia.org/wiki/adb "wikilink"), [screen](https://ja.wikipedia.org/wiki/GNU_Screen "wikilink"))
      - クラッシュダンプ取得

## リアルタイム性能

リアルタイムな用途では、スループットよりもレイテンシが重要となることが多い。レイテンシを改善するためには、カーネルの設定変更・チューニングの他に、アプリケーション自身も最適化する必要がある。カーネルのレイテンシを測定するために[Cyclictest](https://ja.wikipedia.org/wiki/Cyclictest "wikilink")などのベンチマークや各種トレーサが使われる。Linuxにおけるリアルタイム全般の情報は Real-Time Linux Wiki にまとめられている。ELCヨーロッパ2008において[ソニー](../Page/ソニー.md "wikilink")のFrank Rowandによりターゲットへのレイテンシ最適化の実例がプレゼンテーションされている\[11\]\[12\]。また、同氏によってハードウェア/カーネルに付随するリアルタイムの不足点と改善案が提示されている\[13\]。

かつてのLinuxカーネルはリアルタイム性能が悪かったため、高機能なLinuxカーネルをリアルタイム用途とともに使うために、Linuxカーネルよりも下にリアルタイム性能が高くリアルタイムタスクを実行可能な別のシンプルなカーネルが使われることが多かった。現在は[MontaVista](https://ja.wikipedia.org/wiki/MontaVista "wikilink")、[レッドハット](../Page/レッドハット.md "wikilink")などにより[プリエンプション](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")用のパッチセットRT PREEMPTが開発されLinuxカーネルのリアルタイム性能は大きく改善しているものの、他のカーネルとの組み合わせは現在も使われている。

また、Linuxカーネルにはバージョン2.0時点で導入された、アトミックな単一カーネルロックのBKL (Big Kernel Lock)が以前存在していたが、レイテンシ・スループットや[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")を大きく下げる原因となるため\[14\]、現在はロックの細分化やロックレス・アルゴリズムへの置き換えなどによって、全てのBKLが削除されている\[15\]。

現在、RT PREEMPTは"mainline"と呼ばれる[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")管理の主要カーネルツリーへのマージを目指している。標準やPREEMPTで有効になった機能の他にCONFIG_PREEMPT_RCUやthreadirqsなど多くの部分が既にマージされているが、まだマージされていないフィーチャーは残っている\[16\]。

### 他のマイクロカーネルとの組み合わせ

  - [RTAI](https://ja.wikipedia.org/wiki/RTAI "wikilink") (Adeos+Linux)
  - [RTLinux](https://ja.wikipedia.org/wiki/RTLinux "wikilink") (Realtime executive+Linux)
  - [Linux on ITRON](https://ja.wikipedia.org/wiki/Linux_on_ITRON "wikilink") (ITRON+Linux)
  - [T-Linux](https://ja.wikipedia.org/wiki/T-Linux "wikilink") (T-Engine+Linux)
  - [L4-Linux](https://ja.wikipedia.org/wiki/L4-Linux "wikilink") (L4+Linux)
  - [Litron](https://ja.wikipedia.org/wiki/Litron "wikilink") ([TOPPERS/JSPカーネル](https://ja.wikipedia.org/wiki/TOPPERS/JSPカーネル "wikilink")+Linux)
  - [Wind River Real-Time Core for Linux](https://ja.wikipedia.org/wiki/Wind_River_Real-Time_Core_for_Linux "wikilink") (Real-Time Core+Linux)

### その他

  - [KURT-Linux](https://ja.wikipedia.org/wiki/KURT-Linux "wikilink")
  - [ART-Linux](https://ja.wikipedia.org/wiki/ART-Linux "wikilink")
      -
        [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")より[通商産業省工業技術院](https://ja.wikipedia.org/wiki/通商産業省工業技術院 "wikilink")電子技術総合研究所（現:[産業技術総合研究所](https://ja.wikipedia.org/wiki/産業技術総合研究所 "wikilink")）にて開発されている\[17\]。2009年にLinux バージョン2.6用に更新したものがソースコード、バイナリ含め一般公開された\[18\]。

## 関連団体

[thumb](https://ja.wikipedia.org/wiki/ファイル:V9.jpg "wikilink") Linuxの組み込み用途での使用を推進する業界団体がいくつか結成されている。

2000年7月に結成された [Emblix](https://ja.wikipedia.org/wiki/Emblix "wikilink") は日本における組み込みLinuxの普及とその周辺技術の標準化を目的としている。プロセスをグループ化しCPUのリソースを制限するCABIが開発されたが、現在はプロセス集約機能[cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink")に取って代わられている。

2003年に結成された [CE Linux Forum](https://ja.wikipedia.org/wiki/CE_Linux_Forum "wikilink") はLinuxカーネル本体に組み込み用機能を含めることを目的としている。2010年10月、メンバーの重複が多いことや活動目的の一致、組み込みLinuxに関わる企業や開発者の増加から[Linux Foundationと合併し](../Page/Linux_Foundation.md "wikilink")、従来の活動の継続の他、組み込みLinuxの開発プロセスを容易にするために[Yocto Projectという技術ワークグループを開始した](https://ja.wikipedia.org/wiki/Yocto_Project "wikilink")\[19\]\[20\]。

Linuxに関する統括的団体である[Linux Foundationも組み込みLinuxを推進している](../Page/Linux_Foundation.md "wikilink")。2005年にLinux Foundationに合流した Embedded Linux Consortium (2000年3月結成) には、[IBM](../Page/IBM.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[LynuxWorks](https://ja.wikipedia.org/wiki/LynuxWorks "wikilink") などが参加し、[APIの標準化を行っていた](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。そこで作成された ELCPS (Embedded Linux Consortium Platform Specification) は、組み込みLinuxを使った機器の開発において、アプリケーションの移植性を有する標準プラットフォームとしてどのような機能を含めるべきかのガイドとなっている。

2004年に結成された [Linux Phone Standard Forum](https://ja.wikipedia.org/wiki/Linux_Phone_Standard_Forum "wikilink") はLinuxを使った携帯電話でのアプリケーション環境の標準化を目的としている。

2006年に結成された [LiMo Foundation](https://ja.wikipedia.org/wiki/LiMo_Foundation "wikilink") は、サードパーティのLinuxベース携帯電話向けアプリケーション開発のための標準インタフェースの確立を目的としている（設立時メンバーは、[モトローラ](../Page/モトローラ.md "wikilink")、[NEC](../Page/日本電気.md "wikilink")、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")、[サムスン電子](../Page/サムスン電子.md "wikilink")、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")、[ボーダフォン](https://ja.wikipedia.org/wiki/ボーダフォン "wikilink")）。

2007年に結成された [Open Handset Alliance](../Page/オープン・ハンドセット・アライアンス.md "wikilink") は、[Android](../Page/Android.md "wikilink")の開発推進を目的としている。

2009年に日本で結成された [Open Embedded Software Foundation](https://ja.wikipedia.org/wiki/Open_Embedded_Software_Foundation "wikilink") は、[Android](../Page/Android.md "wikilink")に関わる企業間の協力を目的としている。また、できる限りAndroidと同じApatche 2.0ライセンスで、最小構成のAndroid (Light Weight Android)やデジタルテレビ拡張 (Digital TV Extension)、各種スタックなどの開発を予定している。2010年3月にEmbedded Masterをリリースした。これはAndroid 1.6をベースにSIP/RTPスタックやBluetoothのHID/SPP/OBEXプロファイルへの対応、リモコン対応、ポインティング対応、GUI用APIなどを追加したものである\[21\]。

2010年に結成された [Linaro](https://ja.wikipedia.org/wiki/Linaro "wikilink") は、六ヶ月毎に参加企業の各SoCに最適化されたツール・カーネル・ミドルウェアを提供することなどを目的とした非営利のイギリス企業である(設立時のメンバーは[ARM](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")、[サムスン電子](../Page/サムスン電子.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[Freescale](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")、[ST-Ericsson](https://ja.wikipedia.org/wiki/ST-Ericsson "wikilink")、[Texas Instruments](https://ja.wikipedia.org/wiki/Texas_Instruments "wikilink"))\[22\]。

### 組み込みLinuxを利用している商用製品

#### 携帯電話・スマートフォン

  - [モトローラ](../Page/モトローラ.md "wikilink"):
      - RAZR² V8, RAZR² V9, ROKR E2, ROKR E6, A780, E680, A910, A1200, U9, E8 (MontaVistaなどがベース)
      - DROID, Motorola Milestone (Androidベース)
      - など
  - [:en:First International Computer](https://ja.wikipedia.org/wiki/:en:First_International_Computer "wikilink"): Neo 1973 ([OpenMoko](../Page/OpenMoko.md "wikilink"))
  - [Google](../Page/Google.md "wikilink"): [Android Dev Phone](https://ja.wikipedia.org/wiki/Android_Dev_Phone "wikilink"), [Nexus One](https://ja.wikipedia.org/wiki/Nexus_One "wikilink") (Androidベース)
  - [パナソニックモバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/パナソニックモバイルコミュニケーションズ "wikilink"):
      - FOMA [P702iD](../Page/P702iD.md "wikilink")，[P901iTV](https://ja.wikipedia.org/wiki/P901iTV "wikilink")，[P902iS](https://ja.wikipedia.org/wiki/P902iS "wikilink")，[P903i](https://ja.wikipedia.org/wiki/P903i "wikilink"), [P901i](https://ja.wikipedia.org/wiki/P901i "wikilink") (MOAP(L)ベース)
      - [P-02B](https://ja.wikipedia.org/wiki/P-02B "wikilink") (FOMA端末用[オペレータパック](https://ja.wikipedia.org/wiki/オペレータパック "wikilink")ベース)
      - など
  - [NEC](../Page/日本電気.md "wikilink"):
      - FOMA [N900iL](https://ja.wikipedia.org/wiki/N900iL "wikilink")\[23\], [N901iC](https://ja.wikipedia.org/wiki/N901iC "wikilink"), [N902iL](https://ja.wikipedia.org/wiki/N902iL "wikilink"), [N902iL onefone](https://ja.wikipedia.org/wiki/N902iL_onefone "wikilink"), [N902iX](https://ja.wikipedia.org/wiki/N902iX "wikilink"), [N903i](https://ja.wikipedia.org/wiki/N903i "wikilink"), [N904i](../Page/N904i.md "wikilink"), [N905i](../Page/N905i.md "wikilink"), [N905iμ](../Page/N905iμ.md "wikilink"), [N906i](https://ja.wikipedia.org/wiki/N906i "wikilink"), [N906iμ](https://ja.wikipedia.org/wiki/N906iμ "wikilink") (MOAP(L)ベース)
      - FOMA [N601i](https://ja.wikipedia.org/wiki/N601i "wikilink"), [N702iS](../Page/N702iS.md "wikilink"), [N703iD](../Page/N703iD.md "wikilink"), [N703iμ](../Page/N703iμ.md "wikilink"), [N704iμ](../Page/N704iμ.md "wikilink"), [N705i](../Page/N705i.md "wikilink"), [N705i](../Page/N705i.md "wikilink"), [N706i](../Page/N706i.md "wikilink"), [N706ie](https://ja.wikipedia.org/wiki/N706ie "wikilink") (MOAP(L)ベース)
      - [N-01A](https://ja.wikipedia.org/wiki/N-01A "wikilink"), [N-02A](https://ja.wikipedia.org/wiki/N-02A "wikilink"), [N-03A](https://ja.wikipedia.org/wiki/N-03A "wikilink"), [N-04A](https://ja.wikipedia.org/wiki/N-04A "wikilink"), [N-06A](https://ja.wikipedia.org/wiki/N-06A "wikilink"), [N-07A](https://ja.wikipedia.org/wiki/N-07A "wikilink"), [N-08A](https://ja.wikipedia.org/wiki/N-08A "wikilink"), [N-09A](https://ja.wikipedia.org/wiki/N-09A "wikilink") (MOAP(L)ベース)
      - [N-01B](https://ja.wikipedia.org/wiki/N-01B "wikilink"), [N-02B](https://ja.wikipedia.org/wiki/N-02B "wikilink") (FOMA端末用オペレータパックベース)
      - [SoftBank 820N](https://ja.wikipedia.org/wiki/SoftBank_820N "wikilink"), [SoftBank 821N](https://ja.wikipedia.org/wiki/SoftBank_821N "wikilink"), [SoftBank 830N](https://ja.wikipedia.org/wiki/SoftBank_830N "wikilink"), [SoftBank 831N](https://ja.wikipedia.org/wiki/SoftBank_831N "wikilink"), [SoftBank 840N](https://ja.wikipedia.org/wiki/SoftBank_840N "wikilink"), [SoftBank 841N](https://ja.wikipedia.org/wiki/SoftBank_841N "wikilink")
      - [SoftBank 930N](https://ja.wikipedia.org/wiki/SoftBank_930N "wikilink"), [SoftBank 931N](https://ja.wikipedia.org/wiki/SoftBank_931N "wikilink"), [SoftBank 940N](https://ja.wikipedia.org/wiki/SoftBank_940N "wikilink"), [SoftBank 001N](https://ja.wikipedia.org/wiki/SoftBank_001N "wikilink")
      - など
  - [カシオ計算機](../Page/カシオ計算機.md "wikilink"): [SoftBank 830CA](https://ja.wikipedia.org/wiki/SoftBank_830CA "wikilink"), [SoftBank 930CA](https://ja.wikipedia.org/wiki/SoftBank_930CA "wikilink")
  - [HTC Nippon](https://ja.wikipedia.org/wiki/HTC_Nippon "wikilink"): [HT-03A](https://ja.wikipedia.org/wiki/HT-03A "wikilink"), [X06HT](https://ja.wikipedia.org/wiki/X06HT "wikilink")(HTC Desire) (Androidベース)
  - [T-Mobile](../Page/T-モバイル.md "wikilink"): [T-Mobile G1](https://ja.wikipedia.org/wiki/T-Mobile_G1 "wikilink") (Androidベース)
  - [Palm](../Page/パーム_\(企業\).md "wikilink"): [Palm Pre](https://ja.wikipedia.org/wiki/Palm_Pre "wikilink"), [Palm Pixi](https://ja.wikipedia.org/wiki/Palm_Pixi "wikilink") (Palm WebOS)
  - [ノキア](https://ja.wikipedia.org/wiki/ノキア "wikilink"): [N900](https://ja.wikipedia.org/wiki/N900 "wikilink") (Maemo)
  - [ソニー・エリクソン](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink"):
      - [SO705i](../Page/SO705i.md "wikilink")\[24\], [SO706i](../Page/SO706i.md "wikilink") (MOAP(L)ベース)
      - [Xperia SO-01B](https://ja.wikipedia.org/wiki/Xperia_SO-01B "wikilink") (Androidベース)
  - [シャープ](../Page/シャープ.md "wikilink"): [IS01](https://ja.wikipedia.org/wiki/IS01 "wikilink") (Androidベース)
  - [Emblaze Mobile](https://ja.wikipedia.org/wiki/Emblaze_Mobile "wikilink"): ELSE (ELSE INTUITIONベース)
  - [東京工科大学](../Page/東京工科大学.md "wikilink")&[ネットツーコム](https://ja.wikipedia.org/wiki/ネットツーコム "wikilink"): [工科大ケータイ](https://ja.wikipedia.org/wiki/工科大ケータイ "wikilink")
  - [京セラ](../Page/京セラ.md "wikilink"): [Kyocera Zio M6000 Android](https://ja.wikipedia.org/wiki/Kyocera_Zio_M6000_Android "wikilink") (Androidベース)

#### Wi-Fi 電話

  - [SMC Networks](https://ja.wikipedia.org/wiki/SMC_Networks "wikilink"): SMC WSKP100

#### モバイルインターネット端末・PDA

  - [ノキア](https://ja.wikipedia.org/wiki/ノキア "wikilink"): Nokia 770 Internet Tablet, N810, N800 (Maemo)
  - [シャープ](../Page/シャープ.md "wikilink"):
      - [Zaurus](../Page/ザウルス.md "wikilink")
          - SL-B500, SL-C700 (Embedixベース)
          - SL-C750, SL-C760, SL-C860 (OpenPDAベース)
          - SL-C3000, SL-C1000, SL-C3100, SL-C3200 (Lineo uLinuxベース)
      - [NetWalker](https://ja.wikipedia.org/wiki/NetWalker "wikilink")
          - PC-Z1, PC-T1 ([Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")ベース)
  - [ソニー](../Page/ソニー.md "wikilink"): [mylo](https://ja.wikipedia.org/wiki/mylo "wikilink")\[25\]

#### テレビ・レコーダ

  - [パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink"):
      - TH-36D30T, TH-32D30T, TY-S36D50, TY-S32D50, TY-S28D50, TH-36D60, TH-32D60, TH-32D55, TH-28D55
      - DMR-E700BD
      - [VIERA](https://ja.wikipedia.org/wiki/VIERA "wikilink")\[26\]
      - [D-dock](https://ja.wikipedia.org/wiki/D-dock "wikilink")\[27\]
      - [ブルーレイDIGA](https://ja.wikipedia.org/wiki/DIGA "wikilink")\[28\], [ハイビジョンDIGA](https://ja.wikipedia.org/wiki/DIGA "wikilink")\[29\]
      - など
  - [日立](https://ja.wikipedia.org/wiki/日立 "wikilink"): Wooo 9000シリーズ\[30\]\[31\], W50P-HR10000\[32\], W37L-HR9000\[33\]など
  - [ソニー](../Page/ソニー.md "wikilink"):\[34\]
      - CoCoon Channel Server\[35\] (MontaVistaベース)
  - [シャープ](../Page/シャープ.md "wikilink"): \[36\]
  - [東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink"): \[37\]
  - [NEC](https://ja.wikipedia.org/wiki/NEC "wikilink"): AX10\[38\]
  - [People of Lava](https://ja.wikipedia.org/wiki/People_of_Lava "wikilink"): [Scandinavia](https://ja.wikipedia.org/wiki/Scandinavia "wikilink")\[39\] (Androidベース)

#### ホームサーバー・マイクロサーバー・LAN接続型ハードディスク

  - [シャープ](../Page/シャープ.md "wikilink"): [ガリレオ](https://ja.wikipedia.org/wiki/ガリレオ_\(曖昧さ回避\) "wikilink") (HG-01S, HG-02S)\[40\] (axLinuxベース)
  - [玄人志向](https://ja.wikipedia.org/wiki/玄人志向 "wikilink"):
      - [玄箱](https://ja.wikipedia.org/wiki/玄箱 "wikilink") (EMモードはMontaVistaベース・他のOSをインストール可能)
      - [玄柴](https://ja.wikipedia.org/wiki/玄柴 "wikilink") ([Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")ベース・他のOSもインストール可能)
  - [ぷらっとホーム](../Page/ぷらっとホーム.md "wikilink"): [OpenBlockS](https://ja.wikipedia.org/wiki/OpenBlockS "wikilink"), OpenBlockS S, OpenBlockS R, OpenBlockS 266, OpenBlockS 600
  - [マーベル](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink"): [SheevaPlug](https://ja.wikipedia.org/wiki/SheevaPlug "wikilink"), [Plug Computer 3.0](https://ja.wikipedia.org/wiki/Plug_Computer_3.0 "wikilink"), [GuruPlug](https://ja.wikipedia.org/wiki/GuruPlug "wikilink") ([Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")ベース・他のOSもインストール可能)
  - [アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink"):
      - [LANDISK](https://ja.wikipedia.org/wiki/LANDISK "wikilink")シリーズ ([Debian](../Page/Debian.md "wikilink")(など?)ベース)
      - [USL-5P](https://ja.wikipedia.org/wiki/USL-5P "wikilink")シリーズ
  - [BUFFALO](https://ja.wikipedia.org/wiki/バッファロー_\(パソコン周辺機器\) "wikilink"):
      - [LinkStation](https://ja.wikipedia.org/wiki/LinkStation "wikilink")シリーズ ([MontaVista](https://ja.wikipedia.org/wiki/MontaVista "wikilink")(など?)ベース)
      - [TeraStation](https://ja.wikipedia.org/wiki/TeraStation "wikilink")シリーズ
  - [NETGEAR](https://ja.wikipedia.org/wiki/NETGEAR "wikilink"): [ReadyNAS DUO](https://ja.wikipedia.org/wiki/ReadyNAS_DUO "wikilink"), [ReadyNAS NV+など](https://ja.wikipedia.org/wiki/ReadyNAS_NV+ "wikilink") ([Debian](../Page/Debian.md "wikilink")ベース)
  - [NTTコムウェア](https://ja.wikipedia.org/wiki/NTTコムウェア "wikilink"): [L-BOX](https://ja.wikipedia.org/wiki/L-BOX "wikilink")

#### [ハンディカム](https://ja.wikipedia.org/wiki/ハンディカム "wikilink")

  - [ソニー](../Page/ソニー.md "wikilink"): [HDR-SR7](https://ja.wikipedia.org/wiki/HDR-SR7 "wikilink"), [HDR-CX12](https://ja.wikipedia.org/wiki/HDR-CX12 "wikilink"), [HDR-CX500V](https://ja.wikipedia.org/wiki/HDR-CX500V "wikilink")

#### [デジタルカメラ](../Page/デジタルカメラ.md "wikilink")

  - [ソニー](../Page/ソニー.md "wikilink"): [サイバーショット](https://ja.wikipedia.org/wiki/サイバーショット "wikilink") [DSC-T100](https://ja.wikipedia.org/wiki/DSC-T100 "wikilink"), [DSC-T20](https://ja.wikipedia.org/wiki/DSC-T20 "wikilink"), [DSC-G1](https://ja.wikipedia.org/wiki/DSC-G1 "wikilink"), [DSC-G3](https://ja.wikipedia.org/wiki/DSC-G3 "wikilink"), [DSC-H7](https://ja.wikipedia.org/wiki/DSC-H7 "wikilink"), [DSC-W80](https://ja.wikipedia.org/wiki/DSC-W80 "wikilink"), [DSC-W80HDPR](https://ja.wikipedia.org/wiki/DSC-W80HDPR "wikilink"), [DSC-W200](https://ja.wikipedia.org/wiki/DSC-W200 "wikilink"), [DSC-H3](https://ja.wikipedia.org/wiki/DSC-H3 "wikilink"), [DSC-H10](https://ja.wikipedia.org/wiki/DSC-H10 "wikilink"), [DSC-H50](https://ja.wikipedia.org/wiki/DSC-H50 "wikilink"), [DSC-T200](https://ja.wikipedia.org/wiki/DSC-T200 "wikilink"), [DSC-T70](https://ja.wikipedia.org/wiki/DSC-T70 "wikilink"), [DSC-T2](https://ja.wikipedia.org/wiki/DSC-T2 "wikilink"), [DSC-TX1](https://ja.wikipedia.org/wiki/DSC-TX1 "wikilink"), [DSC-WX1](https://ja.wikipedia.org/wiki/DSC-WX1 "wikilink"), [DSC-W110](https://ja.wikipedia.org/wiki/DSC-W110 "wikilink"), [DSC-W120](https://ja.wikipedia.org/wiki/DSC-W120 "wikilink"), [DSC-W170](https://ja.wikipedia.org/wiki/DSC-W170 "wikilink"), [DSC-W220](https://ja.wikipedia.org/wiki/DSC-W220 "wikilink"), [DSC-T900](https://ja.wikipedia.org/wiki/DSC-T900 "wikilink"), [DSC-T90](https://ja.wikipedia.org/wiki/DSC-T90 "wikilink"), [DSC-W270](https://ja.wikipedia.org/wiki/DSC-W270 "wikilink"), [DSC-HX1](https://ja.wikipedia.org/wiki/DSC-HX1 "wikilink"), [DSC-W300](https://ja.wikipedia.org/wiki/DSC-W300 "wikilink"), [DSC-T300](https://ja.wikipedia.org/wiki/DSC-T300 "wikilink"), [DSC-T700](https://ja.wikipedia.org/wiki/DSC-T700 "wikilink"), [DSC-T77](https://ja.wikipedia.org/wiki/DSC-T77 "wikilink")など

#### [プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")

  - [オリンパス](https://ja.wikipedia.org/wiki/オリンパス "wikilink"): ORPHIS HC5500シリーズ\[41\]

#### フォトフレーム

  - [アルゴシステム](https://ja.wikipedia.org/wiki/アルゴシステム "wikilink"): [Algo Smart Panelシリーズ](https://ja.wikipedia.org/wiki/Algo_Smart_Panel "wikilink")
  - [ソニー](../Page/ソニー.md "wikilink"): [VGF-CP1](https://ja.wikipedia.org/wiki/VGF-CP1 "wikilink")\[42\]
  - [NTT東日本](../Page/東日本電信電話.md "wikilink"): 光iフレーム (Androidベース)
  - [Camangi](https://ja.wikipedia.org/wiki/Camangi "wikilink"): [Camangi WebStation](https://ja.wikipedia.org/wiki/Camangi_WebStation "wikilink") (Androidベース)
  - [NEC](https://ja.wikipedia.org/wiki/NEC "wikilink"): コミュニケーター (Androidベース)

#### 電子ブックリーダー

  - [Amazon.com](../Page/Amazon.com.md "wikilink"): [Kindle](../Page/Amazon_Kindle.md "wikilink")\[43\]
  - [バーンズ・アンド・ノーブル](../Page/バーンズ・アンド・ノーブル.md "wikilink"): [Nook](https://ja.wikipedia.org/wiki/Nook "wikilink")
  - [Skiff LLC](https://ja.wikipedia.org/wiki/Skiff_LLC "wikilink"): [Skiff Reader](https://ja.wikipedia.org/wiki/Skiff_Reader "wikilink")
  - [Foxit](https://ja.wikipedia.org/wiki/Foxit "wikilink"): [Foxit eSlick](https://ja.wikipedia.org/wiki/Foxit_eSlick "wikilink")
  - [Neofonie GmbH](https://ja.wikipedia.org/wiki/Neofonie_GmbH "wikilink"): [WePad](https://ja.wikipedia.org/wiki/WePad "wikilink")

#### ルーター

  - [バッファロー](https://ja.wikipedia.org/wiki/バッファロー "wikilink"):
      - AS-A100 (DD-WRTベース)
      - WBR-B11, WBR-G54, WLA-G54, WLA-G54C, BLR-TX4S
      - WLAH-G54, WLAH-A54G54
      - BHR-4RV, FS-G54, WBR2-B11, WBR2-G54, WHR2-A54G54, WHR2-G54, WHR2-G54V, WHR3-AG54, WLA2-G54, WLA2-G54C, WLI-TX4-G54HP, WLI2-TX1-AG54, WLI2-TX1-AMG54, WLI2-TX1-G54, WLI3-TX1-G54, WLI3-TX1-AMG54, WZR-G108, WZR-G54, WZR-HP-G54, WZR-RS-G54, WZR-RS-G54HP
      - WER-A54G54, WER-AG54, WER-AM54G54, WER-AMG54, WHR-HP-AMPG
      - WHR-G54S, WHR-HP-G54, WHR-AMG54, WHR-AM54G54, WLI3-TX1-G54 WLI3-TX1-AMG54, WLI-TX4-G54HP, WLI-TX4-AMG54, WRP-AMG54
      - WHR-G, WHR-G125
      - WHR-HP-G
      - WZR-AMPG144NH, WZR-AMPG300NH, WZR-AG300NH
      - WLI-TX4-AG300N
      - WZR-AGL300NH
      - WZR2-G300N
      - WZR-HP-G300NH
  - [リンクシス](https://ja.wikipedia.org/wiki/リンクシス "wikilink"): WRT54G
  - [プラネックス](https://ja.wikipedia.org/wiki/プラネックス "wikilink"): BRC-W14V, BRC-14V, BRC-W14VG, BRC-14VG, BRC-W14VG-BT, BRC-14VG-BT\[44\]
  - [パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink"): broadband terminal\[45\]
  - [AVM GmbH](https://ja.wikipedia.org/wiki/:en:AVM_GmbH "wikilink"): [FRITZ\!Box](https://ja.wikipedia.org/wiki/:en:FRITZ!Box "wikilink")
  - [LASER5](https://ja.wikipedia.org/wiki/LASER5 "wikilink"): L-Router

#### プレーヤ

##### オーディオプレーヤ

  - [ケンウッド](https://ja.wikipedia.org/wiki/ケンウッド "wikilink"): HD20GA7, HD30GA9, HD30GB9\[46\]

##### マルチメディアプレーヤ

  - [ターボリナックス](https://ja.wikipedia.org/wiki/ターボリナックス "wikilink"): wizpy (wizpy OS)

#### シンセサイザー

  - [ヤマハ](../Page/ヤマハ.md "wikilink"): [MOTIF XS](https://ja.wikipedia.org/wiki/ヤマハ・MOTIFシリーズ#MOTIF_XS6_/_MOTIF_XS_7_/_MOTIF_XS8 "wikilink"), [MOTIF-RACK XS](https://ja.wikipedia.org/wiki/ヤマハ・MOTIFシリーズ#MOTIF-RACK_XS "wikilink") (MontaVistaベース)
  - [KORG](https://ja.wikipedia.org/wiki/コルグ "wikilink"): [OASYS](https://ja.wikipedia.org/wiki/コルグ・OASYS "wikilink")

#### カーナビ

  - [ソニー](../Page/ソニー.md "wikilink"): [NV-XYZ](https://ja.wikipedia.org/wiki/NV-XYZ "wikilink") 33, 55, 77など

#### ラジコン

  - [Jokerworks](https://ja.wikipedia.org/wiki/Jokerworks "wikilink"): ジョーカーレーサー R/C サーバー
  - [Parrot](https://ja.wikipedia.org/wiki/Parrot "wikilink"): [AR.Drone](https://ja.wikipedia.org/wiki/AR.Drone "wikilink") - ラジコンヘリコプター

#### ロボット

  - [産業技術総合研究所](https://ja.wikipedia.org/wiki/産業技術総合研究所 "wikilink")ほか: [HRP-2m Choromet](https://ja.wikipedia.org/wiki/HRP-2m_Choromet "wikilink"), [HRP-4C](https://ja.wikipedia.org/wiki/HRP-4C "wikilink") (ART Linux)
  - [富士通](../Page/富士通.md "wikilink"): [HOAP-1](https://ja.wikipedia.org/wiki/HOAP-1 "wikilink"), [HOAP-2](https://ja.wikipedia.org/wiki/HOAP-2 "wikilink"), [HOAP-3](https://ja.wikipedia.org/wiki/HOAP-3 "wikilink") (RT-Linux)
  - [富士ソフト](https://ja.wikipedia.org/wiki/富士ソフト "wikilink"): [PALRO](https://ja.wikipedia.org/wiki/PALRO "wikilink") (Ubuntu)

#### カラオケ

  - [第一興商](../Page/第一興商.md "wikilink"):
      - [デンモクの一部](https://ja.wikipedia.org/wiki/DAM_\(カラオケ\)#デンモク "wikilink")
      - [DAM-DSII](https://ja.wikipedia.org/wiki/DAM_\(カラオケ\)#DAMステーション "wikilink") (MontaVistaベース)
      - など

#### その他

  - [フィリップス](../Page/フィリップス.md "wikilink"): LPC3180
  - [LASER5](https://ja.wikipedia.org/wiki/LASER5 "wikilink"): L-CardA, L-Card+, NPA1000, L-Board

### ベンダー

  - [ACCESS](https://ja.wikipedia.org/wiki/ACCESS_\(企業\) "wikilink") (ACCESS Linux Platform)
  - [LynuxWorks](https://ja.wikipedia.org/wiki/LynuxWorks "wikilink") (LynuxWorks Linux)
  - [MontaVistaソフトウェア](https://ja.wikipedia.org/wiki/MontaVistaソフトウェア "wikilink") (MontaVista Linux)
  - [TimeSys](https://ja.wikipedia.org/wiki/TimeSys "wikilink") (TimeSys Linux)
  - [ウインドリバー・システムズ](https://ja.wikipedia.org/wiki/ウインドリバー・システムズ "wikilink") (Wind River Linux)
  - [コンカレント・コンピュータ](https://ja.wikipedia.org/wiki/コンカレント・コンピュータ "wikilink") ([RedHawk Linux](https://ja.wikipedia.org/wiki/RedHawk_Linux "wikilink"))
  - [アックス](https://ja.wikipedia.org/wiki/アックス "wikilink") (axLinuxなど)
  - [シリコンリナックス](https://ja.wikipedia.org/wiki/シリコンリナックス "wikilink") (シリコンリナックスOS)
  - [リネオソリューションズ](https://ja.wikipedia.org/wiki/リネオソリューションズ "wikilink") (Lineo uLinux)
  - [アドソル日進](../Page/アドソル日進.md "wikilink") (BlueCat Linux)
  - [エニア](https://ja.wikipedia.org/wiki/エニア "wikilink") (Enea Linux)

### 支援団体・企業

#### ドライバ・ソフトウェア開発

  - [Linux Driver Project](https://ja.wikipedia.org/wiki/Linux_Driver_Project "wikilink") - NDAありなしに関わらず無料でドライバ開発を行っている\[47\]
  - [シャープビジネスコンピュータソフトウェア](https://ja.wikipedia.org/wiki/シャープビジネスコンピュータソフトウェア "wikilink") - シャープのガリレオシリーズのソフトウェアを作成\[48\]
  - [デバイスドライバーズ](https://ja.wikipedia.org/wiki/デバイスドライバーズ "wikilink")
  - [日新システムズ](https://ja.wikipedia.org/wiki/日新システムズ "wikilink")

#### ドライバ開発の研修

  - [NECラーニング](https://ja.wikipedia.org/wiki/NECラーニング "wikilink")
  - [イーエルティ](https://ja.wikipedia.org/wiki/イーエルティ "wikilink")
  - [ウェルビーン](https://ja.wikipedia.org/wiki/ウェルビーン "wikilink")

## プラットフォーム

### 実装

  - [Qt Extended](https://ja.wikipedia.org/wiki/Qt_Extended "wikilink") - モバイル機器向けアプリケーションプラットフォーム
  - [Openmoko](https://ja.wikipedia.org/wiki/Openmoko "wikilink") - 携帯電話向けプラットフォーム
  - [MeeGo](https://ja.wikipedia.org/wiki/MeeGo "wikilink") - [Linux Foundationが統括する種々デバイス向けのプラットフォーム](../Page/Linux_Foundation.md "wikilink")。現在は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")とノキアが主導している。MaemoとMoblinを統合して作られた。
      - [Maemo](https://ja.wikipedia.org/wiki/Maemo "wikilink") - ノキア主導の[ハンドヘルドコンピュータ](https://ja.wikipedia.org/wiki/ハンドヘルドコンピュータ "wikilink")向けプラットフォーム
          - [Hildon](https://ja.wikipedia.org/wiki/Hildon "wikilink") - Maemoのアプリケーションプラットフォーム
      - [Moblin](https://ja.wikipedia.org/wiki/Moblin "wikilink") - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")主導のネットブックやモバイルインターネット端末向けプラットフォーム
  - [Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink") - [LiMo Foundationの仕様を](https://ja.wikipedia.org/wiki/LiMo_Foundation "wikilink")[MeeGo](https://ja.wikipedia.org/wiki/MeeGo "wikilink")に取り込み作られた、インテルとサムスン主導の携帯電話向けプラットフォーム<ref>

</ref>。

  - [MOAP](../Page/MOAP.md "wikilink")(L) - [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")主導の携帯電話向けプラットフォーム
  - [Access Linux Platform](../Page/Access_Linux_Platform.md "wikilink") - ACCESS主導の携帯電話向けプラットフォーム\[49\]
      - [Hiker](https://ja.wikipedia.org/wiki/Hiker "wikilink") - Access Linux Platformのアプリケーションフレームワーク
  - [Palm WebOS](https://ja.wikipedia.org/wiki/Palm_WebOS "wikilink") - Palmの携帯電話プラットフォーム
      - [Mojo](https://ja.wikipedia.org/wiki/Mojo "wikilink") - Palm WebOSのアプリケーションプラットフォーム
  - [Android](../Page/Android.md "wikilink") - Google主導の携帯電話・タブレット向けプラットフォーム
  - [Bada](https://ja.wikipedia.org/wiki/Bada "wikilink") - Sumsung主導の携帯電話プラットフォーム
  - [Meltemi](https://ja.wikipedia.org/wiki/Meltemi "wikilink") - Nokiaの低価格端末向けプラットフォーム
  - [Ubuntu MID Edition](https://ja.wikipedia.org/wiki/Ubuntu "wikilink") - Canonical主導のモバイルインターネット端末向けプラットフォーム
  - [OpenWrt](https://ja.wikipedia.org/wiki/OpenWrt "wikilink") - ルータ向けプラットフォーム
  - [DD-WRT](https://ja.wikipedia.org/wiki/DD-WRT "wikilink") - ルータ向けプラットフォーム
  - [OPIE](../Page/OPIE.md "wikilink") - Qtopia (現[Qt Extended](https://ja.wikipedia.org/wiki/Qt_Extended "wikilink"))の派生
  - [Familiar Linux](https://ja.wikipedia.org/wiki/Familiar_Linux "wikilink") - PDA向けディストリビューション
  - [JLime](https://ja.wikipedia.org/wiki/JLime "wikilink") - [ハンドヘルドコンピュータ](https://ja.wikipedia.org/wiki/ハンドヘルドコンピュータ "wikilink")向けディストリビューション
  - [GPE Palmtop Environment](https://ja.wikipedia.org/wiki/GPE_Palmtop_Environment "wikilink") - PDA向けアプリケーションプラットフォーム
  - [OpenZaurus](https://ja.wikipedia.org/wiki/OpenZaurus "wikilink") - [ザウルス](../Page/ザウルス.md "wikilink")用の代替OS

### 仕様

  - [LiMo Platform](https://ja.wikipedia.org/wiki/LiMo_Foundation "wikilink") - 携帯電話端末メーカーが主導の携帯電話向けプラットフォーム。[Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink")プロジェクトに採用される。

## 特許問題

組み込みLinuxに関わらず、元となるLinuxカーネルにまつわる[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")、とりわけ[ソフトウェア特許](https://ja.wikipedia.org/wiki/ソフトウェア特許 "wikilink")の問題がいくつか存在する。

### Linuxカーネルに含まれる特許

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")では[リード・コピー・アップデート](https://ja.wikipedia.org/wiki/リード・コピー・アップデート "wikilink")を始めとしていくつかの特許で保護された技術が利用されている。これらの保護されている技術はパッチ寄稿者が特許権者である場合、Linuxや他のオープンソースプロジェクトで使うことを権利者が許可している場合が多い（このような特許で保護されたテクノロジーは多くは企業の従業員によるLinuxカーネルへの貢献によるものが多数を占めるため）。

### Open Invention Network

2005年には[Open Invention Network](https://ja.wikipedia.org/wiki/Open_Invention_Network "wikilink")(OIN) が誕生し、Linuxや関連アプリケーションに対し自社保有の特許を行使しないことに同意しかつOINとライセンス契約を締結すれば、OINのライセンシーはOINが保有するLinux関連特許を[ロイヤリティフリー](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")で使えることが保証されるようになった。これら特許には[Samba](https://ja.wikipedia.org/wiki/Samba "wikilink")、[Mono](../Page/Mono_\(ソフトウェア\).md "wikilink")、[Apacheなどが利用する特許も含まれる](../Page/Apache_HTTP_Server.md "wikilink")\[50\]\[51\]。現在OINにはライセンサーまたはライセンシーとして[IBM](../Page/IBM.md "wikilink")（[メインフレーム](../Page/メインフレーム.md "wikilink")や[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")の[著作権](../Page/著作権.md "wikilink")ならびに特許を持つ）、[ノベル](../Page/ノベル_\(企業\).md "wikilink")（[UNIX](../Page/UNIX.md "wikilink")の著作権ならびに[UNIX System Vの特許を持つ](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")）、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（[SunOS](https://ja.wikipedia.org/wiki/SunOS "wikilink")/[Solaris](../Page/Solaris.md "wikilink")の特許を持つ）\[52\]、[HP](../Page/ヒューレット・パッカード.md "wikilink")（[HP-UX](../Page/HP-UX.md "wikilink")や[Palm](../Page/Palm.md "wikilink")の特許を持つ\[53\]）、[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink")\[54\]（[IOSの特許を持つ](../Page/Cisco_IOS.md "wikilink")）、[レッドハット](../Page/レッドハット.md "wikilink")、[Google](../Page/Google.md "wikilink")、[カノニカル](https://ja.wikipedia.org/wiki/カノニカル "wikilink")（特にこの3社は[FLOSS](https://ja.wikipedia.org/wiki/FLOSS "wikilink")への多数の貢献を行う企業として有名）\[55\]、[フィリップス](../Page/フィリップス.md "wikilink")、[NEC](../Page/日本電気.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")、[富士通ゼネラル](https://ja.wikipedia.org/wiki/富士通ゼネラル "wikilink")、[富士通](../Page/富士通.md "wikilink")などを含め数百の企業、団体、個人\[56\]が参加している。

### マイクロソフトによる特許の主張

2007年5月、[マイクロソフト](../Page/マイクロソフト.md "wikilink")は「訴訟を起こすつもりはない」とするものの、Linuxカーネルに42件の特許侵害があると主張した\[57\]。一方[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はOSの基本理論が1960年代に成立したことを挙げ、「マイクロソフトの方が特許を侵害している可能性が高い」と主張し、侵害内容の提示を求めた\[58\]。

2007年10月、マイクロソフトは[欧州連合でのマイクロソフト製品の競争法違反に関する裁判で敗訴した](https://ja.wikipedia.org/wiki/マイクロソフトの欧州連合における競争法違反事件 "wikilink")。

2009年2月にはマイクロソフトは[TomTom](https://ja.wikipedia.org/wiki/TomTom "wikilink")のLinux製品が自社の[FAT](../Page/File_Allocation_Table.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")に関する特許を侵害したとして提訴した（詳しくは記事"[マイクロソフト対TomTom事件](https://ja.wikipedia.org/wiki/マイクロソフト対TomTom事件 "wikilink")"を参照）。同年3月この裁判は和解に終わり、問題とされたLinuxのFATファイルシステムに関するコードはその後特許に抵触しない形に修正された\[59\]。また同年9月、OINはマイクロソフトが持っていたLinux関連特許22件を[Allied Security Trust](https://ja.wikipedia.org/wiki/Allied_Security_Trust "wikilink") (AST) から買い取ったと発表した\[60\]。これらの特許はASTがマイクロソフトの非公開オークションにより手に入れたものである\[61\]。ASTはOIN同様特許訴訟を防衛することを目的とした[パテントプール](https://ja.wikipedia.org/wiki/パテントプール "wikilink")を形成する企業[コンソーシアム](../Page/コンソーシアム.md "wikilink")であり、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")・[モトローラ](../Page/モトローラ.md "wikilink")・[HP](../Page/ヒューレット・パッカード.md "wikilink")・[ベライゾン・コミュニケーションズ](https://ja.wikipedia.org/wiki/ベライゾン・コミュニケーションズ "wikilink")・[シスコ](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")・[Google](../Page/Google.md "wikilink")・[エリクソン](https://ja.wikipedia.org/wiki/エリクソン "wikilink")などのメンバーで構成されている\[62\]。

2010年1月、マイクロソフトは[ティーボ](https://ja.wikipedia.org/wiki/ティーボ "wikilink")を特許侵害で提訴した。ティーボはLinuxを製品に利用しているが（記事"[TiVo化](https://ja.wikipedia.org/wiki/TiVo化 "wikilink")"などを参照）このときマイクロソフトはLinuxに関しては法廷で取り上げなかった\[63\]。

[富士ゼロックス](../Page/富士ゼロックス.md "wikilink")はLinux製品の特許についてマイクロソフトと[クロスライセンス](https://ja.wikipedia.org/wiki/クロスライセンス "wikilink")契約を結び\[64\]、[メルコや](https://ja.wikipedia.org/wiki/バッファロー_\(パソコン周辺機器\) "wikilink")[アイ・オー・データ機器](https://ja.wikipedia.org/wiki/アイ・オー・データ機器 "wikilink")もマイクロソフトとLinux製品の特許に関する契約を結んでいる\[65\]\[66\]。同種の特許防衛を事業とする企業コンソーシアム、[RPX Corporationにはマイクロソフトと共にLinuxに関わる企業が多数参加している](https://ja.wikipedia.org/wiki/RPX_Corporation "wikilink")。

### iPhoneとAndroidの特許係争

2010年、[アップルが](../Page/アップル_\(企業\).md "wikilink")[HTCを特許侵害で提訴した](https://ja.wikipedia.org/wiki/HTC_\(企業\) "wikilink")。侵害したとする特許の中にはOSレベルのものも含まれている\[67\]。この件でHTCは[Google](../Page/Google.md "wikilink")等のパートナー企業と協力を取りアップルへ[反訴](../Page/反訴.md "wikilink")することを計画している\[68\]。また、同年4月、マイクロソフトは[Android](../Page/Android.md "wikilink")が特許侵害しているとして非難した\[69\]。マイクロソフトと協業関係であったHTCはこの件でマイクロソフトと特許契約を結んでいる\[70\]。同年4月、HPは[パームを買収し](../Page/パーム_\(企業\).md "wikilink")、パームの持つ1500件の特許を引き継ぐこととなった\[71\]。アップルがパームを提訴しなかった理由はこれらの特許の存在があるとも噂されている\[72\]。なお、パームは[Beの](https://ja.wikipedia.org/wiki/Be_\(企業\) "wikilink")[BeOS](../Page/BeOS.md "wikilink")に関する知的財産を買収しているが、これらの特許は会社を分割した際にPalmSource（現[ACCESS Systems](https://ja.wikipedia.org/wiki/ACCESS_Systems "wikilink")）が引き継いでいるとみられる。

### フリーソフトウェアコミュニティからの提言

2010年4月、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink") (FSF) は「[ビルスキー対カッポス事件](https://ja.wikipedia.org/wiki/ビルスキー対カッポス事件 "wikilink")」 (*[Bilski v. Kappos](https://ja.wikipedia.org/wiki/:en:Bilski_v._Kappos "wikilink")*) をテーマに[ソフトウェア特許](https://ja.wikipedia.org/wiki/ソフトウェア特許 "wikilink")の問題を描いたドキュメンタリー映画、[Patent Absurdityを公開した](https://ja.wikipedia.org/wiki/Patent_Absurdity "wikilink")\[73\]。この映画はソフトウェア特許支持者、反対者双方の意見を収録したドキュメンタリーである。

## 関連項目

  - [OpenZaurus](https://ja.wikipedia.org/wiki/OpenZaurus "wikilink")
  - [LiMo Foundation](https://ja.wikipedia.org/wiki/LiMo_Foundation "wikilink")

## 脚注

## 外部リンク

  - [G2Linx](http://www.g2linx.com)

  -
  - [Embedded Linux wiki](http://elinux.org/)

  - 組み込みLinuxに関するニュースサイト

  - [Embedded Linux mailist list archive](http://www.spinics.net/lists/linux-embedded/)

[Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.
2.  [新参Linuxプログラマ向けのドライバ開発キットがリリース](http://sourceforge.jp/magazine/06/05/30/1441250)
3.  [Gartner Says Worldwide Smartphone Sales Reached Its Lowest Growth Rate With 3.7 Per Cent Increase in Fourth Quarter of 2008](http://www.gartner.com/it/page.jsp?id=910112)
4.  [AdMob Mobile Metrics Report](http://metrics.admob.com/wp-content/uploads/2009/09/AdMob-Mobile-Metrics-Aug-092.pdf) (3頁)
5.  [AdMob Mobile Metrics Report February 2010](http://metrics.admob.com/wp-content/uploads/2010/03/AdMob-Mobile-Metrics-Feb-10.pdf)
6.
7.  [iPhone、携帯ゲーム機としても勢力伸ばす](http://www.itmedia.co.jp/news/articles/1003/24/news013.html)
8.  [Android Mobile Sales Chart - October 2009](http://news.vgchartz.com/news.php?id=5777)
9.  [PATCH 00/02 virtio: Virtio platform driver](http://lkml.indiana.edu/hypermail/linux/kernel/1103.1/00996.html)
10. [RFC 0/8 Introducing a generic AMP/IPC framework](http://lkml.indiana.edu/hypermail/linux/kernel/1106.2/02253.html)
11. [Adventures In Real-Time Performance Tuning, Part 1](http://tree.celinuxforum.org/CelfPubWiki/ELCEurope2008Presentations?action=AttachFile&do=get&target=adventures_in_real_time_performance_tuning_part_1-no_hidden.pdf)
12. [Adventures In Real-Time Performance Tuning, Part 2](http://tree.celinuxforum.org/CelfPubWiki/ELCEurope2008Presentations?action=AttachFile&do=get&target=adventures_in_real_time_performance_tuning_part_2-no_hidden.pdf)
13. [Real-Time Linux Failure](http://elinux.org/images/b/be/Real_time_linux_failure.pdf)
14.
15.
16. [Status of Preempt-RT and why there is no roadmap](http://elinux.org/images/c/ca/Elc2011_gleixner.pdf)
17. [ムービングアイ，「ART-Linuxカーネル」の無償ダウンロード・サービスを開始（発表資料要約） - 組み込みソフト - Tech-On！](http://techon.nikkeibp.co.jp/members/01db/200307/1011043/?ST=print)
18. <http://sourceforge.net/projects/art-linux/>
19. [Linux FoundationとCE Linux Forumが合併、新WG Yocto Projectもスタート](http://itpro.nikkeibp.co.jp/article/NEWS/20101028/353523/)
20. [Linux Foundation と Consumer Electronics Linux Forum が合併](http://www.linuxfoundation.jp/lf-celf)
21. [組み込み機器向けに最適化したAndroid「Embedded Master」が公開](http://www.eetimes.jp/news/3756)
22. [ARM・サムスン・IBM・TIら、組み込みLinux支援団体 Linaro を発足](http://japanese.engadget.com/2010/06/03/linaro/)
23. [「N900iL」は日本初のLinux携帯](http://plusd.itmedia.co.jp/mobile/articles/0407/13/news065.html)
24. [写真で解説する「SO705i」（ソフトウェア編）](http://plusd.itmedia.co.jp/mobile/articles/0801/11/news067.html)
25. [■塩田紳二のPDAレポート■ ソニー「mylo」ハードウェアレポート](http://pc.watch.impress.co.jp/docs/2006/1106/pda53.htm)
26. [組み込み機器技術展ET2006に「Linuxタウン」出現，ケータイもデジカメもプロジェクタも(page 2)](http://itpro.nikkeibp.co.jp/article/NEWS/20061117/254028/?ST=oss&P=2)
27.
28.
29.
30. [増田和夫が見た“Wooo”「W42P-HR9000」（1）高画質を支える数々の新技術](http://www.phileweb.com/news/d-av/200606/05/15708.html)
31. [薄型テレビを制したLinux，開発現場の“守護霊”と“中央線”](http://itpro.nikkeibp.co.jp/article/OPINION/20070115/258629/)
32.
33.
34.
35. [CES:米MontaVista、同社Linux搭載のソニー「CoCoon」など展示](http://www.nikkeibp.co.jp/archives/226/226014.html)
36.
37.
38.
39. [初の“Google TV”、スウェーデンのメーカーが発表](http://www.itmedia.co.jp/news/articles/1004/06/news033.html)
40. [アックスの組み込みLinuxはほかと根本的に違う（1/2） − ＠IT MONOist](http://monoist.atmarkit.co.jp/fembedded/01axe/axe01.html)
41. [「ORPHIS　HC5500シリーズ」新登場](http://www.olympus.co.jp/jp/news/2005b/nr051108hc5500j.cfm)
42. [フォトフレーム : ソニー、ネットワーク対応デジタルフォトフレーム“キャンバス オンライン CP1 ”を発表](http://www.digi-came.com/jp/modules/news/article.php?storyid=1835)
43. [Amazon、Kindleのソースコードを公開](https://news.mynavi.jp/news/2009/06/19/033/index.html)
44. [BRCシリーズプログラムソースコード](http://www.planex.co.jp/support/download/router/linux_src.shtml)
45.
46. [HD20GA7/HD30GA9/HD30GB9 ■GNU GPL/LGPL適用ソフトウェアに関するお知らせ](http://web.archive.org/web/20080115192833/http://www.kenwood.com/j/download/hd20ga7/gpl.html)
47. [Free Linux Driver Development Questions and Answers\!](http://www.kroah.com/log/linux/free_drivers_faq.html)
48. [DEVELOPMENT：シャープビジネスコンピュータソフトウェア株式会社](http://www.sbc.co.jp/promo/dev/farm/02.html)
49. [Linux基盤「ALP」でケータイOSのエコシステムを構築](http://monoist.atmarkit.co.jp/fembedded/25access/access01.html)
50. [Linux System](http://www.openinventionnetwork.com/pat_linuxdef.php)
51. [complete list of Linux System components](http://www.openinventionnetwork.com/pat_linuxdefpop.html)
52. [Oracle Signs License Agreement with Open Invention Network](http://www.openinventionnetwork.com/press_release03_27_07.php)
53.
54. [米TwitterとCiscoがLinux特許保護のOpen Invention Network (OIN) に加入](http://sourceforge.jp/magazine/11/08/12/0359211)
55. [Canonical Signs License Agreement With Open Invention Network](http://www.openinventionnetwork.com/press_release04_17_07.php)
56. [OIN Community of Licensees](http://www.openinventionnetwork.com/licensees.php)
57. [「オープンソースの特許侵害235件」－Microsoftの公表に騒然](http://enterprise.watch.impress.co.jp/cda/infostand/2007/05/21/10303.html)
58.
59. [Microsoft の特許侵害主張に『Linux』開発者がパッチで対応](http://japan.internet.com/webtech/20090706/12.html)
60. [Linux関連特許管理のOIN，Microsoftから特許22件を取得](http://itpro.nikkeibp.co.jp/article/NEWS/20090909/336865/)
61. [Linux知的財産を管理するOIN、元マイクロソフト所有の特許を買い取りへ](http://www.computerworld.jp/topics/osst/161469.html)
62. [Sun, EBay, Rock & Republic, Troyer: Intellectual Property](http://www.bloomberg.com/apps/news?pid=conewsstory&refer=conews&tkr=1149L:US&sid=aI70xRS4IR9w)
63. [Microsoft sues TiVo...but not over Linux. Surprise\!](http://news.cnet.com/8301-13505_3-10438791-16.html)
64. [富士ゼロックスとマイクロソフトは特許のクロスライセンス契約を締結](http://www.microsoft.com/japan/presspass/detail.aspx?newsid=2996)
65. [メルコグループとマイクロソフト、バッファロー製品に搭載のLinuxソフトウェアについて特許に関する契約を締結](http://www.microsoft.com/japan/presspass/detail.aspx?newsid=3730)
66. [アイ・オー・データとマイクロソフトが製品に搭載のLinuxソフトウェアについての特許に関する契約を締結](http://www.microsoft.com/japan/presspass/detail.aspx?newsid=3823)
67. [Apple vs HTC: a patent breakdown](http://www.engadget.com/2010/03/02/apple-vs-htc-a-patent-breakdown/)
68. [Apple訴訟を受け、HTCがGoogleと共同で反訴を計画か - NYT](https://news.mynavi.jp/news/2010/03/20/015/index.html)
69. [マイクロソフト、「Android」を特許侵害と非難](http://japan.cnet.com/news/biz/story/0,2000056020,20412885,00.htm?ref=rss)
70.
71. [HP、Palmを12億ドルで買収、「全力でWebOSを盛り立ていく」](http://jp.techcrunch.com/archives/20100428hp-palm-deal-webos/)
72.
73. [FSFがソフトウェア特許に反対するドキュメンタリー映画「Patent Absurdity」を公開](http://sourceforge.jp/magazine/10/04/20/0810208)