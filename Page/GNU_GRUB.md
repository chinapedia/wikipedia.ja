> この記事は[GNU GRUB](https://ja.wikipedia.org/wiki/GNU_GRUB)から翻訳されています。


[GNU_GRUB_on_MBR_partitioned_hard_disk_drives.svg](https://ja.wikipedia.org/wiki/File:GNU_GRUB_on_MBR_partitioned_hard_disk_drives.svg "fig:GNU_GRUB_on_MBR_partitioned_hard_disk_drives.svg")-partitioned hard disk drives\]\] [GNU_GRUB_on_GPT_partitioned_hard_disk_drives.svg](https://ja.wikipedia.org/wiki/File:GNU_GRUB_on_GPT_partitioned_hard_disk_drives.svg "fig:GNU_GRUB_on_GPT_partitioned_hard_disk_drives.svg")-partitioned hard disk drives\]\] **GNU GRUB** (GRand Unified Bootloader) は[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")にて開発されている高機能な[ブート](../Page/ブート.md "wikilink")ローダである。 グラブと読まれることが多い\[1\]。 大きく分けてバージョン0.9x系の**GRUB Legacy**と、1.9x系の**GRUB 2**の2種類がある。

GRUBはの[リファレンス実装](../Page/リファレンス実装.md "wikilink")でもある。Multiboot Specification([マルチブート](../Page/マルチブート.md "wikilink")[仕様](../Page/仕様.md "wikilink"))とは、コンピュータにインストールされた複数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を個別に起動する際にOSの選択肢をユーザーに提示したり、または、あるOSの[パーティション](../Page/パーティション.md "wikilink")上に存在する特定の[カーネル](../Page/カーネル.md "wikilink")に関する利用可能な設定を有効化する方法を提供するなどといった、マルチブートに関する[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")なシステムを規定する仕様である。同仕様は現在[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink") (FSF) がメンテナンスしている。

もともとGRUBは**Grand Unified Bootloader**という名前でGNUプロジェクトとは無関係のプロジェクトにて開発されていたが、[GNU](../Page/GNU.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は開発中の[カーネル](../Page/カーネル.md "wikilink")である[GNU HurdをブートするためGRUBを利用していた](../Page/GNU_Hurd.md "wikilink")。のちに主要貢献者の助言もあり、公式なGNUプロジェクトとなった。現在ではGNUのカーネルであるGNU Hurdだけではなく、主に[Linux](../Page/Linux.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")などの[Unix系](../Page/Unix系.md "wikilink")OSや、[Solaris](../Page/Solaris.md "wikilink") x86（10 1/06 release以降\[2\]）でも利用されている。

## 歴史

GRUBは当初、エーリヒ・シュテファン・ブーリン(Erich Stefan Boleyn)により開発されており\[3\]、これはFSFが開発していたGNU Hurdオペレーティングシステムを起動させるための作業の一環であった\[4\]。[1999年](../Page/1999年.md "wikilink")、主要貢献者であったゴルドン・マッツィヒカイト（Gordon Matzigkeit）と[奥地秀則](https://ja.wikipedia.org/wiki/奥地秀則 "wikilink")(Yoshinori K. Okuji)の働きかけによって、GRUBは公式GNUプロジェクトの公開プロジェクトとなり最新の[ソースコード](../Page/ソースコード.md "wikilink")をホストするanonymous [CVSが提供されることとなった](../Page/Concurrent_Versions_System.md "wikilink")\[5\]。 [GNU_GRUB_components.svg](https://ja.wikipedia.org/wiki/File:GNU_GRUB_components.svg "fig:GNU_GRUB_components.svg") (sector 0). `core.img` is written to the empty sectors between the MBR and the first partition, if available (for legacy reasons the first partition starts at sector 63 instead of sector 1, but this is not mandatory). The `/boot/grub`-directory can be located on an distinct partition, or on the /-partition.\]\]

## 特徴

GRUBは動的に設定でき、コンピュータのブートタイム中に異なるカーネルや[初期RAMディスク](https://ja.wikipedia.org/wiki/initrd "wikilink")(initrd)を選択するといった柔軟な設定変更が可能である。そのような目的を実現するために 、GRUBはシンプルかつ[Bash](../Page/Bash.md "wikilink")ライクな[コマンドラインインタフェースを提供しており](../Page/キャラクタユーザインタフェース.md "wikilink")、ユーザーは通常のブートメニューリストにその場で 新たなブートシーケンスを追加することもできる。

GRUBは（起動処理の初期のコードが[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")を利用している\[6\]のを除き、）[移植性](../Page/移植性.md "wikilink")が極めて高く、複数の実行可能フォーマットをサポートしており、ディスクのジオメトリ変換に依存していない。GRUBは[Logical Block Address](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink")(LBA)モードのサポートに加え、ほぼ全ての主要なUNIXファイルシステム、並びに[VFAT及び](../Page/File_Allocation_Table.md "wikilink")[NTFSなど](../Page/NT_File_System.md "wikilink")[Microsoft Windowsで使用するファイルシステムもサポートしている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。GRUBを利用することで、サポートしている任意のファイルシステム上に存在するファイルの中身をユーザーは見ることができる。

GRUBは様々なユーザーインタフェースを用いて設定することができる。多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")ではGRUBのブートメニューに表示される背景画像のカスタマイズなどを行う[グラフィカルな設定ツールを用意している](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。またGRUBのテキストインタフェースを利用すると、リモート・ターミナルから[シリアルポート](../Page/シリアルポート.md "wikilink")経由で接続できる\[7\]。

GRUBはネットワーク経由でのOSイメージのダウンロードも可能で、従って[ディスクレスシステムもサポートしている](../Page/シンクライアント.md "wikilink")。GRUBはローカルから起動するだけではなく、起動前の自動的なOSイメージの伸長 もできる。

GRUBはスクロール可能なOSブート選択画面を表示する。GRUBは設定ファイル"menu.lst"（または"grub.cfg"など）にエントリーを追加することで150またはそれを超えるブート選択を容易に行うことが可能であり、矢印キーでブートするOSを選択する。

GRUBはマルチブートに対応しているが、を利用しマルチブート非対応のOSをもサポートしている。ブートOSの追加と同じく、2、3行のコマンドシーケンスを設定ファイルに書き込む、またはGRUBシェルでその場で適切なコマンドを実行することで、[MS-DOS](../Page/MS-DOS.md "wikilink")、Windows、Linux、[BSD](../Page/BSD.md "wikilink")、または、Solarisオペレーティングシステムをいとも簡単に起動させることができる。これらUnix系OSやDOS、Windowsなどを起動するためのチェーンローダがGRUBに組み込まれている。

前述の通り、通常のブートメニューに加え、Bashライクなターミナルコマンドプロンプトが利用でき、ブートプロセスの一部または全部をチェックしたり変更することが可能な豊富なコマンドセットを持っている。これらの手法を活用することで、コンピュータにインストールされているOSの特別な知識が事前になくとも、インストールされているOSを起動する目的で[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、または[CD-ROM](../Page/CD-ROM.md "wikilink")デバイスからGRUBを利用し起動することもできる。

GRUBは一般的なUnix系OS上においてインストール可能であり、また特定の実装を用いてDOSやWindowsからのインストールも可能である。

## ブートプロセス

*以下の説明はx86([80x86](https://ja.wikipedia.org/wiki/x86 "wikilink"), [x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink"))システムを対象としている。その他のシステムには当てはまらないかもしれない。*

コンピュータの電源を入れると、[BIOSは設定されたプライマリブートデバイス](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")（大抵はコンピュータの[ハードディスクである](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")）を探し出し、ディスクの先頭512バイトに位置する[マスターブートレコード](../Page/マスターブートレコード.md "wikilink")(MBR)から初期ブートストラッププログラムをロードする。この後制御はこのコードに移る。

### GRUB バージョン1 (GRUB Legacy)

GRUBをインストールしたコンピュータならば、通常GRUBの初期ブートプログラムであるStage 1ローダがMBRにインストールされている。しかし、チェーンロード可能な別のブートローダ（例: [MBM](https://ja.wikipedia.org/wiki/マルチ・ブート・マネージャ "wikilink")）がMBRにインストールされていても構わない。後者の場合は、パーティションの（Volume boot record, VBR、または[パーティションブートレコード](https://ja.wikipedia.org/wiki/パーティションブートレコード "wikilink")、 Partition boot record, PBRとも呼ばれる）のような別の[ブートセクタ](../Page/ブートセクタ.md "wikilink")にGRUBのStage 1ローダをインストールし、このStage 1ローダをMBR上のブートローダからチェーンブートすればよい。ブートセクタのサイズは限られており、更にStage 1ローダが使用する[BIOS割り込みルーチン](https://ja.wikipedia.org/wiki/BIOS割り込みルーチン "wikilink")の制限から、このタイミングでは、ディスクの先頭以内の固定領域から2、3のディスクセクタを読み込み、GRUBの次のStageローダをロードする程度のことしかできない 。

Stage 1ローダは直接Stage 2ローダを読み込めるが、通常はその間に入るStage 1.5ローダを読み込むためセットアップを行う。GRUBのStage 1.5はハードディスクのMBRの直後から最初のパーティション手前までにある先頭30KB以内に位置するローダであり、何らかの理由でこの領域が利用できない場合（例えば、異常な[パーティションテーブル](https://ja.wikipedia.org/wiki/パーティションテーブル "wikilink")が原因でセクタアドレスが読み取れなかったり、特殊なディスクドライバを必要とするケース、または[GPTもしくは](../Page/GUIDパーティションテーブル.md "wikilink")[LVMなどを利用するシステムの場合など](../Page/論理ボリュームマネージャ.md "wikilink")）は、Stage 1.5ローダのインストールに失敗する。Stage 1.5ローダのイメージはファイルシステム固有のドライバを含んでおり、これを用いてStage 1.5ローダはStage 2ローダをファイルシステム上の任意の場所（例えばファイルパスが`/boot/grub`の[ディレクトリ](../Page/ディレクトリ.md "wikilink")）から発見できるようになり、これを直接ロードできる。この後、Stage 2はデフォルトの設定ファイル、及び必要とされるその他任意のモジュールを読み込む。

### GRUB バージョン2

構造及び処理のフローはGRUB バージョン1に酷似している。GRUB バージョン1のStage 1ローダに似た*boot.img*と呼ばれるコードがMBRまたはPBR(VBR)に保存される。しかしながら、このboot.imgはデフォルトで[LBA48アドレッシングを利用しセクタを読み込むことができる](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#48bit_LBA\(BigDrive\) "wikilink")。このコードは*diskboot.img*から生成される*core.img*の最初のセクタをロードし、更に生成されたcore.imgファイルの残りをロードするのに使用される。core.imgファイルは通常GRUB バージョン1のStage 1.5ローダと同じ領域に保存されるためそれと同様の問題をはらんでいる。しかし、Stage 1.5ローダを移動したり、そのインストールに失敗した 場合に比べ、GRUB バージョン2のcore.imgを別のファイルシステムに移動したり、まだファイルシステムを作成していない「空のパーティション」（*bare partition*）へ移動させた場合に生じる問題は少なくなっている。このcore.imgというのは簡単に言うと、GRUB LegacyのStage 2ローダからローディングに必要な主要コードのみを取り出したものであり、GRUBの動作のためMBRやVBRに必須ではあるが、Stage 2ローダよりはるかに小さい。格納サイズが制約されているMBRやVBRへインストールできないというサイズの問題はこれにて解決され、GRUB Legacyで発生する可能性のあった、Stage 2がGRUBから利用不可能になり動作しなくなるという問題の部分的な解決策になっている。<ref>

  -
  - </ref>

core.imgファイルを一旦ロードすると、デフォルトの設定ファイル及び必要とされるその他任意のモジュールもロードされる。

### GRUBのロード以降

GRUBのロードがひとたび完了すると、どのOSを起動するか選択するためのインタフェースが提供される。これは通常、グラフィカルなメニューのかたちをとっていることが多い。そのようなメニューが利用できない場合、またはユーザーが直接制御した場合、GRUBは自身が持つコマンドプロンプトを提供する。これを用いてユーザーはブートパラメータを手動で指定することが可能である。GRUBはユーザーが定義した時間何も操作せず経過すると自動的に特定のカーネルをロードするよう設定できる（デフォルトではメニューの最上位にあるOSが起動する）。

GRUBがOSもしくはカーネルの選択メニューにおいて受け付けるコマンドの内、最も重要なものはおそらく次の2つである。

  - OSの起動前に、メニュー上であるOSにカーソルを当てて選択した状態でキーボードの'e'を押下した場合、そのOSの起動パラメータを編集できる<ref name="if">

</ref>（これら起動パラメータはGRUB自身が持つ機能ではないが、現代的なOSやカーネルはパラメータ機能を持っている）。典型的なケースとして、Linuxシステムのカーネル・パラメータの変更の際にこのことを利用する。このように、既に起動済みシステム上でGRUBの設定を変更しない、及びカーネル・パラメータを編集しないケースというのは、突発的な事態、例えばOSがブートに失敗したケースなどを想定しており、そのような事態が起きてもGRUBは対応できる。また、カーネル・パラメータのコマンドラインを利用すると、とりわけ 、OS起動前に、ある[LKMを無効化する](https://ja.wikipedia.org/wiki/ローダブル・カーネル・モジュール "wikilink")、またはブラックリスト化（LKMをロードしないようカーネルに知らせる機能）することが可能となる。特定のLKMが壊れており、このため正常なブート・シーケンスが阻害される場合、おそらくこの機能が必要となる。例としてLinuxカーネルのLKMである"nvidia-current"というものをブラックリスト化する場合、カーネル・パラメータの末尾に"modprobe.blacklist=nvidia-current"のような文字列を追記する必要があるが、予めGRUBの設定ファイルにこの文字列が無かったとしても、キーボードの'e'を押下してパラメータをオン・ザ・フライで変更できるのである\[8\]。

  - 任意の状態でキーボードの'c'を押下した場合、BashライクなGRUBのコマンドラインを表示する\[9\]。とはいえこれは通常のLinux上の[シェル](../Page/シェル.md "wikilink")とは異なる。これはGRUB固有の特定コマンドしか受け付けない<ref>

</ref>。

いずれの場合もパラメータの編集が完了したあと、Ctrl+xキーを同時に押下すればOSがこのパラメータを使って起動する\[10\]。

ブートオプションが選択されると、GRUBは選択したカーネルを[メモリにロードし](../Page/記憶装置.md "wikilink")、以後の制御を全てカーネルに委ねる。あるいは、GRUBはを利用し、別のブートローダにブートプロセスの制御を渡すこともできる。これはWindowsのようなマルチブート標準をサポートしない、またはGRUBが直接サポートしていないOSをロードするのに使用される手段である。この場合、他のシステムのブートプログラムはGRUBが保全したまま維持される。 そして、カーネルの代わりとして、他システムはあたかもMBRから起動したかのようにロードされる。 このことからGRUBは、Microsoftブートメニューと同じく、マルチブート非対応のOSも追加で選択できるブートマネージャであるといえる。 既にシステムにWindows OSが存在する場合、「その上に追加で」Linuxディストリビューションをインストールする際には、現代的なLinuxディストリビューションのインストーラは、GRUBがこのような挙動をするよう自動的に設定する場合がある。そして、既にインストール済みのオリジナルOSは一切の変更が加わらず維持され、それは例えば、複数のバージョンのWindowsがインストールされているシステムでも同様である。

## GRUBのインストール

GRUBの鍵となる特徴は、それがOSと結びつくことなくインストールされることにあるが、初めてのインストールにおいては、Linuxのイメージのコピーが少なくとも1つ必要となる。ただ当該Linuxシステムが1つ存在すれば、ローダをインストールする後述のコマンドを実行し別のパーティションのVBRにインストールできる。または[光学ディスクにもGRUBをインストールできる](../Page/光ディスク.md "wikilink")\[11\]ので、以後この光学ディスクを用いれば、Linuxのインストールに関係なくシステムに存在するOSをGRUBから起動できる。もっとも、移植版のGRUBも存在するため、ローダをインストールするコマンドを実行できる環境ならば、別にLinuxでなくともよい。

GRUBはスタンドアローンシステムとして動作することにより、前述の通りチェーンロードを利用し、インストールされた主要なOSすべてを正しくかつ有効にブートできる実質的なミニシステムとなる。

LILOのようなブートローダとは異なり、設定ファイルの変更の度にGRUBをMBRまたはパーティションに再インストールする必要などない。

Linuxにおいては、"grub-install"というシェルコマンドが、Stage 1ローダをMBRまたはパーティションのいずれか一方にインストールするため利用される。GRUBの設定ファイル、（通常は）Stage 2ローダそしてその他のファイルは有効なパーティション上に存在しなければならない。もしこれらのファイルやパーティションが利用できなくなった場合、Stage 1は即座にGRUBシェル[コマンドラインインタフェースに落ちてしまう](../Page/キャラクタユーザインタフェース.md "wikilink")。

GRUBの設定ファイルの名前やディスク上の位置は各システム様々である。例えば、[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")とGRUB Legacyを使用する[Debian GNU/Linuxでは設定ファイルは](../Page/Debian.md "wikilink")`/boot/grub/menu.lst`に存在する。また[Fedora](../Page/Fedora.md "wikilink")、[Gentoo Linuxでは](../Page/Gentoo_Linux.md "wikilink")、`/boot/grub/grub.conf`に存在する。 GRUB 2をインストールしたDebian、[Ubuntu](../Page/Ubuntu.md "wikilink")では`/boot/grub/grub.cfg`である。Fedoraではまた、[FHS準拠の為](https://ja.wikipedia.org/wiki/Filesystem_Hierarchy_Standard "wikilink")`/etc/grub.conf`から`/boot/grub/grub.conf`への[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")が張られている。また同様の理由で、Debian、Ubuntuではデフォルトの設定ファイルが`/etc/default/grub`に存在し、ユーザーは通常巨大なgrub.cfgファイルよりも種々の設定値を設定しやすいユーザーフレンドリーなこのファイルを書き換える。書き換えが完了し、`update-grub`という`grub-install`の[ラッパースクリプトを実行する](https://ja.wikipedia.org/wiki/ラッパー_\(ソフトウェア\) "wikilink")（または適切なカーネルのインストールに使用される[パッケージから同コマンドが呼び出される](../Page/パッケージ管理システム.md "wikilink")）ことで、適切なカーネルとinitrdを指定した`/boot/grub/grub.cfg`が生成される\[12\]。

GRUBは何らかの理由でハードディスクがない、またはハードディスクからのブートができなくなったシステムを起動するため、BIOSアクセス可能かつ[El Torito](https://ja.wikipedia.org/wiki/ISO_9660#El_Torito "wikilink")([en](https://ja.wikipedia.org/wiki/:en:El_Torito_\(CD-ROM_standard\) "wikilink"))対応の[光学ドライブ](../Page/光学ドライブ.md "wikilink")\[13\]、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")または[USB フラッシュドライブのような](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")へのインストールも可能である。

## 開発

もっとも広く使用されているGRUBのバージョンは*GRUB Legacy*と呼ばれる。このバージョンは現在、バグ修正のみを受け付け、新しい機能は追加されないことになっている。GRUB開発者は新しいバージョンのGRUB 2に開発を集中している\[14\]。このバージョンは、GNU GRUBの既存のコードを整頓し、より強固なものに変え、かつ移植性、機能性を向上させること を含む目標を掲げて全面的な書き変えを行ったものである。GRUB 2の開発は当初**PUPA**\[15\]と言う名前のもと始まった。PUPAプロジェクトは日本の[独立行政法人](../Page/独立行政法人.md "wikilink")[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")の援助を受けており、「平成14年度 [未踏ソフトウェア創造事業](https://ja.wikipedia.org/wiki/情報処理推進機構#未踏ソフトウェア創造事業 "wikilink")」\[16\]に「次世代GRUBブートローダの基本設計と実装」という案件として採択された\[17\]\[18\]。PUPAはGRUB バージョン0.9xがGRUB Legacyとリネームされた[2002年](../Page/2002年.md "wikilink")頃、GRUB 2の開発に統合された。

プロジェクトの目標はいくつかあったが一例を挙げると、[PowerPC](../Page/PowerPC.md "wikilink")など非x86[プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、ソフトウェアの[国際化と地域化](../Page/国際化と地域化.md "wikilink")\[19\]、非ASCII文字\[20\] 、動的なモジュールローディング、[メモリ管理](../Page/メモリ管理.md "wikilink")、簡易な[スクリプト言語](../Page/スクリプト言語.md "wikilink")、x86プラットフォーム依存コードの特定のモジュールへの移動及び隔離、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[フレームワーク等の各種サポートが含まれている](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")。[Ubuntu](../Page/Ubuntu.md "wikilink")はそのバージョン9.10からデフォルトのブートローダとして採用しており\[21\]、Fedora 14、Debian 6.0 (コードネーム: squeeze)など他のディストリビューションでのサポートも開始されている。

### 派生

公式には開発は完了しているが、GRUB Legacyが[エンドユーザー](../Page/エンドユーザー.md "wikilink")の間にて未だ広く使用されているが故に、いくつかの非公式なプロジェクトがGRUB Legacyのコードを彼ら自身で改善するため、[フォークしている](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。例えば、"setgrubdevice"や"usbshift"などの新しいコマンドを含む**[Super Grub Disk](https://ja.wikipedia.org/wiki/Super_Grub_Disk "wikilink")**\[22\]や**[GRUB4DOS](https://ja.wikipedia.org/wiki/GRUB4DOS "wikilink")**などがある。特にGRUB4DOSはDOS/LINUXからの起動 、Windowsブートマネージャ、[SYSLINUX](https://ja.wikipedia.org/wiki/SYSLINUX "wikilink")、または[LILO](../Page/LILO.md "wikilink")経由での起動、並びにMBR/CDからの起動をサポートするユニバーサルブートローダである。またBIOSディスクエミュレーションや[ATAPI](https://ja.wikipedia.org/wiki/ATAPI "wikilink") CDROMドライバも組み込まれている\[23\]。いくつか改良されているコマンドもあり、"find --set-root", "map --hook", そして"cdrom"がそれに当たる\[24\]。

[OpenSolaris](../Page/OpenSolaris.md "wikilink")ではGRUB Legacyにや自動的な[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")カーネル選択、そして（[データ圧縮](../Page/データ圧縮.md "wikilink")やマルチブート環境での動作も含む）[ZFS](../Page/ZFS.md "wikilink")からのブートをサポートするための各種改良が加えられている\[25\]\[26\]。[Syllable OSプロジェクトでは](https://ja.wikipedia.org/wiki/Syllable "wikilink")からのシステム起動をサポートするため改変版のGRUBを作成している\[27\]。

## GRUBを設定するためのツール

[thumb](https://ja.wikipedia.org/wiki/ファイル:StartUp-Manager.png "wikilink") GRUB自身のセットアップのためのモジュールに加え、しばしばいくつかのディストリビューションでは追加のセットアップツールが使用される。例えば、[SUSE](../Page/SUSE.md "wikilink")/[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")ディストリビューションにおける[YaST2](https://ja.wikipedia.org/wiki/YaST2 "wikilink")、[Fedora](../Page/Fedora.md "wikilink")/[RHELディストリビューションの](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[Anacondaインストーラがそれに該当する](../Page/Anaconda_\(インストーラー\).md "wikilink")。[Ubuntu](../Page/Ubuntu.md "wikilink")など[Debian](../Page/Debian.md "wikilink")ベースのディストリビューションで使われるはGRUBのグラフィカルな設定エディタである。その他、GRUB 2用の[KDE](../Page/KDE.md "wikilink") Control Moduleがいくつか存在する\[28\]\[29\]。GRLDR ICEというGRUB4DOS向けにgrldrファイルのデフォルト設定を変更するための小さいツールもある。

### ユーティリティ

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:GRUB_customizer.png "wikilink") GRUB UtilitiesはGRUB Legacy、GRUB 2及びGRUB4DOS用のマルチプラットフォームユーティリティのコレクションである\[30\]。

## 対応しているファイルシステム (GRUB 2)

GRUB 2では、以下のファイルシステムがサポートされ、GRUBからファイルシステム上のファイルにアクセスできる。

  - [FFS](../Page/Unix_File_System.md "wikilink")
  - [UFS](../Page/Unix_File_System.md "wikilink")2
  - [FAT](../Page/File_Allocation_Table.md "wikilink")16/32
  - [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")/[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")/[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")
  - [NTFS](../Page/NT_File_System.md "wikilink")
  - [ReiserFS](../Page/ReiserFS.md "wikilink")
  - [JFS](../Page/Journaled_File_System.md "wikilink")
  - [XFS](../Page/XFS.md "wikilink")
  - [MINIX FS](https://ja.wikipedia.org/wiki/MINIXファイルシステム "wikilink")
  - [ZFS](../Page/ZFS.md "wikilink")\[31\]
  - [Btrfs](https://ja.wikipedia.org/wiki/Btrfs "wikilink")\[32\]

## 起動トラブルについて

GRUBは、MBRに収録されるGRUB本体と、パーティション内に収録される設定ファイルなどから構成される。 一般的にこれらの設定ファイル等は、GRUB Legacyのstage1.5/2ローダをインストールしたLinux用パーティション内に保存される。このため、Linuxを削除する目的でLinux用パーティションごと破壊してしまうと、起動できなくなるトラブルに見舞われる。

このほかにもGRUBの起動システムは多種多様な要因によって起動不能となることがある。 BIOSからのHDD認識、ストレージデバイスコントローラーの認識状態、USBストレージ機器の接続状況などから、こういった問題がおきる可能性がある。

こういった問題に、GRUBは処理の段階ごとに停止(待機)時の表示から状況を判断できるように設計されている。 またGRUBコンソールやGRUB rescueコンソールが表示される場合は、他の起動ディスクなどを用いること無く、起動可能な状態に復旧できる場合もある。

<table>
<caption>GRUB停止(待機)時表示</caption>
<thead>
<tr class="header">
<th><p>表示例</p></th>
<th><p>呼称</p></th>
<th><p>発生状況</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>grub&gt;</p></td>
<td><p>GRUBコンソール</p></td>
<td><p>起動やkernel設定等に関わる一時的変更を行なうために、手動でGRUBコンソールを呼び出した場合<br />
GRUB2の設定ファイル等のパーティションが読み込んだのち、grub.cfgが読み込めなかった場合</p></td>
</tr>
<tr class="even">
<td><p>error:invalid extent<br />
grub rescue &gt;</p></td>
<td><p>GRUB rescueコンソール</p></td>
<td><p>GRUB2のgrub.cfgを読み込んだ上で何らかのトラブルが生じた場合</p></td>
</tr>
<tr class="odd">
<td><p>error: no such partition.<br />
grub rescue&gt;</p></td>
<td><p>GRUB rescueコンソール</p></td>
<td><p>GRUB2の設定ファイルが保存されているパーティションが見つからない場合</p></td>
</tr>
</tbody>
</table>

## 脚注

### 注釈

### 出典

## 関連項目

  -
  - [Windows Boot Manager](https://ja.wikipedia.org/wiki/Windows_Boot_Manager "wikilink")

  - [LILO](../Page/LILO.md "wikilink")

  -
  - [coreboot](https://ja.wikipedia.org/wiki/coreboot "wikilink")

  - [UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")

## 関連リンク

  -
  -
## 外部リンク

  - [GNU GRUBプロジェクト公式サイト](https://www.gnu.org/software/grub/)
      - [GNU GRUB公式マニュアル](https://www.gnu.org/software/grub/manual)
      - [公式のhelp-grubメーリングリスト](https://lists.gnu.org/mailman/listinfo/help-grub)
      - [PUPA](http://www.nongnu.org/pupa/) (歴史的な意味のみ)
  - [LILO and GRUB: Boot Loaders Made Simple by Judith Myerson](https://archive.li/9vhK)
  - [Booting Linux on x86 using Grub2](http://people.apache.org/~skitching/MineOfInformation/linux/Booting_Linux_on_x86_with_Grub2.html)
  - [Boot with GRUB](https://www.linuxjournal.com/article/4622)、[Linux Journal](https://ja.wikipedia.org/wiki/Linux_Journal "wikilink") - すばらしいチュートリアル。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[11月10日](../Page/11月10日.md "wikilink")開催された、[横浜Linuxユーザグループ](https://ja.wikipedia.org/wiki/横浜Linuxユーザグループ "wikilink") (YLUG) 第92回カーネル読書会でのプレゼンテーション及びビデオ。GRUB主要開発者、[奥地秀則](https://ja.wikipedia.org/wiki/奥地秀則 "wikilink")(Yoshinori K. Okuji)による。GRUBの開発がいわゆる[システムプログラミングであることがよくわかる](../Page/システムソフトウェア.md "wikilink")。
      - [YLUG 第92回カーネル読書会 ブートローダとOSの親密な関係(1/2) 基礎知識編](https://www.nicovideo.jp/watch/sm5287206)
      - [YLUG 第92回カーネル読書会 ブートローダとOSの親密な関係(2/2) GRUB構造編](https://www.nicovideo.jp/watch/sm5287732)
      - [ブートローダと OS の親密な関係](http://enbug.org/KernelStudyMeeting.pdf) - 当講演で使用した資料

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:研究プロジェクト](https://ja.wikipedia.org/wiki/Category:研究プロジェクト "wikilink")

1.  [GRUB - 日立ITソリューションズIT用語辞典](https://it-words.jp/w/GRUB.html)
2.
3.
4.
5.
6.  次はその一例であり、x86アーキテクチャ用コードである。
7.  奥地自身もGRUBの開発に利用していた。
8.  [Arch Linuxの例](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")。"7 Blacklisting"を参照。
9.
10.
11.
12.
13.
14.
15.
16.
17. 担当[PMは](../Page/プロジェクトマネージャ.md "wikilink")[新部裕](https://ja.wikipedia.org/wiki/新部裕 "wikilink")。
18.
19. 従来のLILOやGRUB Legacyでは実現できていない。
20.
21. [GRUB 2 by default](http://www.ubuntu.com/getubuntu/releasenotes/910overview#GRUB%202%20by%20default), Ubuntu 9.10 Technical Overview, Ubuntu
22.
23.
24.
25. Modifying Solaris Boot Behavior on x86 Based Systems (Task Map) - System Administration Guide: Basic Administration
26. (System Administration Guide: Basic Administration) - Sun Microsystems
27.
28.
29.
30.
31.
32.