> この記事は[NT File System](https://ja.wikipedia.org/wiki/NT_File_System)から翻訳されています。


**NT File System** (**NTFS**) とは、[Windows NT系の標準](../Page/Windows_NT系.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。

## 歴史

### バージョン

  - NTFS 1.0 - [Windows NT 3.1で使用されたバージョン](../Page/Microsoft_Windows_NT.md "wikilink")。
  - NTFS 1.1 - [Windows NT 3.51で使用されたバージョン](../Page/Microsoft_Windows_NT.md "wikilink")。
  - NTFS 1.2 (4.0) - [Windows NT 4.0で使用されたバージョン](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink")。
  - NTFS 3.0 (5.0) - [Windows 2000で使用されたバージョン](../Page/Microsoft_Windows_2000.md "wikilink")。
  - NTFS 3.1 (5.1) - [Windows XP以降で使用されているバージョン](../Page/Microsoft_Windows_XP.md "wikilink")。

括弧内はそれぞれが実装されたWindows NT系のバージョン。NTFSのバージョンとして呼ばれることがある。

### 互換性

NTFS 1.2とNTFS 3.xとの間には互換性が無く、Windows NT 4.0上からNTFS 3.xにアクセスするには、Service Pack 4以上を適用する必要がある。また、Windows 2000以降で、自身が使用しているバージョンよりも前のバージョンのNTFSにアクセスすると、その時点で自身が使用しているバージョンに変換する。

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の[パーティション](../Page/パーティション.md "wikilink")テーブルIDが、[HPFS](../Page/HPFS.md "wikilink")と同じであるため、登場当初はディスク ユーティリティが誤動作することがあった。

### 後継

サーバ向けにマイクロソフトはWindows Server 2012においてNTFSの欠点を解消した[ReFS](https://ja.wikipedia.org/wiki/ReFS "wikilink")を導入している。HomeやProバージョンでは今後もNTFSが使われていく予定である。

## 特徴

  - 大容量
    1ボリューム当たりの推奨最大サイズは、2 [TiBであるが](https://ja.wikipedia.org/wiki/テビバイト "wikilink")、それ以上のファイルシステムも作成可能である（理論上は、2<sup>64</sup>-1[クラスタ](https://ja.wikipedia.org/wiki/クラスタ_\(記憶媒体\) "wikilink")\[1\]まで可能だが、コンピュータの性能上制限してある）。
  - 検索の高速化
    ファイルの管理は[B+木](../Page/B+木.md "wikilink")で行われ、大量のファイルが存在していても、検索やアクセス速度の低下が少ない。
  - 長いファイル名
    [MS-DOS](../Page/MS-DOS.md "wikilink")の「ファイル名 8[バイト](../Page/バイト_\(情報\).md "wikilink") + 拡張子 3バイト」から、ファイル名・拡張子にとらわれず、[Unicode](../Page/Unicode.md "wikilink")で最大255文字のファイル名を付けることができるようになった（ドットもファイル名の一部となった）。
  - POSIXサポート
    [アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")政府のコンピュータ納入の条件として[POSIX](../Page/POSIX.md "wikilink")サポートが必須条項であったため、NTFSはPOSIX.1仕様の環境を提供する。これには、ファイル名やディレクトリ名の大文字と小文字の区別やアクセス権、[ハードリンク](../Page/ハードリンク.md "wikilink")、互換性を持つ[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")のサポートが含まれる。
  - [代替データ ストリーム](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\)#マイクロソフト "wikilink")（マルチ データ ストリーム）
    NTFSは、一つのディレクトリ エントリに対して、複数のデータ ストリームを持つことができる。これは[Macintosh](../Page/Macintosh.md "wikilink")で使われる[HFS+におけるマルチ](../Page/HFS_Plus.md "wikilink") フォークに相当する機能で、ファイルの概要情報やアクセス制御リストなどはこの機能を利用してディレクトリ エントリに結び付けられている。

### 頑健性とセキュリティ

  - 堅牢性の向上
    突然の電力供給停止などの障害が発生した場合、[トランザクションログ](https://ja.wikipedia.org/wiki/トランザクションログ "wikilink")から、実行した処理をロールバックし、ファイルシステムの不整合を発生させない[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")をサポートしている。
  - 耐障害性
    [ハードディスク内の](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[不良セクタ](https://ja.wikipedia.org/wiki/不良セクタ "wikilink")を動的に認識する。以降その[セクタを含むクラスタに対するアクセスは別のクラスタに代替されるようになる](https://ja.wikipedia.org/wiki/ディスクセクタ "wikilink")。冗長性のあるダイナミック ボリュームまたは記憶域スペースを使用していなかった場合、不良セクタにあったデータは回復されない。
  - セキュリティの向上
    ファイルやディレクトリごとに[ACLによるアクセス権の設定が可能である](../Page/アクセス制御リスト.md "wikilink")。また、ファイルアクセスの監視を行う設定も可能である。
  - [ディスククォータ](https://ja.wikipedia.org/wiki/ディスククォータ "wikilink")
    Windows 2000以降のNTFSは、ユーザーごとのディスクの使用量の上限を設定できる。[Windows Server 2003 R2からは](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2003#Windows_Server_2003_R2 "wikilink")、ディレクトリごとのディスクの使用量の上限を設定することができるようになった。
  - 暗号化
    Windows 2000以降のNTFSは、[Encrypting File Systemをサポートし](https://ja.wikipedia.org/wiki/Encrypting_File_System "wikilink")、NTFSボリューム上のファイルとフォルダの透過的な暗号化をサポートしている。これは圧縮機能の一実装であり、暗号化されたファイルやフォルダは常に圧縮されている。暗号化を利用した場合、自分自身の証明書を失うとシステム管理者を含めて誰も永久にアクセスできなくなる。
  - スナップショット
    Windows XPおよびWindows Server 2003以降では「」(VSS) と称する[スナップショット機能が導入された](../Page/スナップショット_\(ファイルシステム\).md "wikilink")\[2\]。Windows付属のバックアップ ユーティリティ ([NTBackup](https://ja.wikipedia.org/wiki/:en:NTBackup "wikilink"), [Backup and Restore](https://ja.wikipedia.org/wiki/:en:Backup_and_Restore "wikilink")) はボリュームシャドウコピーサービスを利用しており、ある時点のボリュームの状態を正確にバックアップできる。[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") Service Pack 1以降のWindowsではChkdskにVSSを利用し正確なチェックが行えるようになり、本来なら修復が不要なボリュームをオフラインにせずに済むようになった\[3\]。また、[Windows Server 2003や](../Page/Microsoft_Windows_Server_2003.md "wikilink")[Windows Vistaにおいては](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、ボリュームシャドウコピーサービスによってファイルの世代別保存を実現する\[4\]\[5\]。
  - 変更ジャーナル
    ファイルに対する変更を記録する。

### 容量効率の向上

Windows NT 3.51からサポートされたファイル圧縮をNTFSもサポートしている。LZNT1アルゴリズム（[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")の変種）を使用したファイル単位での透過的な圧縮をサポートし、ディスクの空き領域を増加させることができる。ただし、4 KiBを超えるアロケーション ユニット サイズでは圧縮機能を利用できない。

加えて、[スパース ファイルもサポートする](https://ja.wikipedia.org/wiki/スパース_ファイル "wikilink")。ファイルの一部が0で埋められている場合、クラスタ単位で0で埋められている領域をスキップし、ディスク容量を節約する。これはデータベースのハッシュテーブル ファイルや[仮想マシンの仮想ハードディスク](../Page/仮想機械.md "wikilink") ファイルなど大部分が0で埋められているファイルで効率よく働く。

NTFSには小さなファイルをファイルのメタデータと一緒にMFT内に収める機能がある。これはアロケーション ユニットを割り当てない事による若干の容量面のメリットとユーザーデータの読み取りにメタデータとは別のI/Oを必要としない速度面のメリットがある。

ファイル数は少ないが巨大なファイルを格納したいと思うなら、最大2048 [KiB](https://ja.wikipedia.org/wiki/キビバイト "wikilink") のアロケーション ユニット サイズを選択できる。これにより、断片化の問題、管理領域とデータ領域の比率など、ファイルシステム性能を左右する問題を解決する。

NTFS圧縮やスパースファイルの使用、極度の断片化によるエクステント リストを使い切ってしまう状況に対応するためのオプションが有り、これの使用によって規定では1 KiBのファイルレコードを4 KiBまで増加させることができる\[6\]。副次的な効果としてMFT内に収められるユーザーデータも増加する。

なお、2010年時点でのNTFSの実装では、クラスタ数は2<sup>32</sup>-1までとなっている。このため、16 TiBを超えるボリュームは、4 KiBを超えるアロケーション ユニット サイズを指定しなければならない。サポートされているアロケーション ユニット サイズは2048 KiB (Windows 10 バージョン1703、Windows Server 2016までは最大64 KiB)までである。したがって、NTFSボリュームは8 PiBまでの制限がある。また、OSのバージョンと容量によっては機能に制限がある。

### 後方互換性

[仮想DOSマシン](../Page/仮想DOSマシン.md "wikilink")上で動作するソフトウェアに対して、ファイル システム上で一意なパス名であることを保証した8.3形式ファイル名を保存することができる。この機能は任意に有効・無効を設定することができるので、NTFSのファイルシステム最適化の代表的なものとされるが、非推奨とされていた。Windows 7では有効・無効をボリューム単位で設定できるようになりシステムボリュームでは有効、データボリュームでは無効といった運用が可能となった（フォーマット時の規定値は有効）。Windows 8ではパフォーマンス上の理由により8.3形式のファイル名は非推奨となり\[7\]フォーマット時の規定値がシステムボリュームを除き無効となった。

原則としてファイル名の大文字小文字は区別されるが、サブシステムがこの機能の有効無効を選択している。[Win32サブシステムではファイル名の大文字小文字は区別されず](../Page/Windows_API.md "wikilink")、ファイル名の大文字小文字が異なるファイルを上書きした場合は、最後に使われたファイル名のファイルが保存される。POSIX・[Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")サブシステム・[Windows Subsystem for Linuxではファイル名の大文字小文字は区別され](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink")、ファイル名の大文字小文字が異なるファイルは上書きされず別のファイルとして保存される。

さらに高度な応用として[ファイル システム フィルターを備え](https://ja.wikipedia.org/wiki/ファイル_システム_フィルター "wikilink")、ファイルシステム機能やファイルシステム上の名前空間を任意のソフトウェアでオーバーライド（継承）できる。この機能をもとに圧縮機能・暗号化機能・ファイル変更ジャーナル・スナップショット機能・クォータ機能をサブシステムを含むユーザー プロセスからは何ら変更の無いアクセスで利用できる透過的な実装が行われたほか、サードパーティによるファイル システムに対する[フォレンジック](https://ja.wikipedia.org/wiki/フォレンジック "wikilink")監査の実装などに活用されている。

### チェックと修復

Windows NT系には、ファイルシステムの論理エラーまたは物理エラーの確認およびファイルシステムの修復コマンドとして、「[chkdsk](../Page/スキャンディスク.md "wikilink")」コマンドが用意されている\[8\]。実際にファイルシステムの修復を行うには、「<kbd>chkdsk 〈対象ボリューム〉 /f</kbd>」を、[不良クラスタ](https://ja.wikipedia.org/wiki/不良クラスタ "wikilink")の修復を試みるには、「<kbd>chkdsk 〈対象ボリューム〉 /r</kbd>」を実行する。

ファイル数の増加に伴う chkdsk の実行時間の増加に対しWindows 8では従来のメタデータの走査とエラーの修復の両方をボリュームをオフラインにして行う方式からメタデータの走査とエラーの記録をオンラインで行いエラーの修復のみをオフラインで行う方式に変えた為、ボリュームのダウンタイムはデータ量には依存しなくなった\[9\]。

また、NTFSは[MFTの](https://ja.wikipedia.org/wiki/マスター_ファイル_テーブル "wikilink")「$BadClus」ファイルに不良クラスタの情報を記録しているため、不良クラスタを含むパーティションをパーティションコピーツールなどで丸ごと他のハードディスクにコピーすると、「$BadClus」ファイルもそのままコピーされてしまい、新しいハードディスクには不良クラスタが存在しないにもかかわらず、chkdskでは不良クラスタが存在しているように見えることがある。これを修復してリセットするには、「<kbd>chkdsk 〈対象ボリューム〉 /b</kbd>」を実行する（ただし、Windows Vistaまたは[Windows Server 2008以降のみ](../Page/Microsoft_Windows_Server_2008.md "wikilink")）。

ファイルシステム上の[不良クラスタ](https://ja.wikipedia.org/wiki/不良クラスタ "wikilink")と[S.M.A.R.T.におけるバッドセクタは別物である](../Page/Self-Monitoring,_Analysis_and_Reporting_Technology.md "wikilink")。

なお、chkdskによるNTFSの修復により、ディスク エラーの状況が悪化する場合があるため、修復の前に重要なファイルはバックアップしておくことが推奨される。また、chkntfsコマンドを使用することで、Windows起動時に自動的にchkdskを実行したり、自動実行をキャンセルしたりすることができる\[10\]。

### 欠点

#### フラグメンテーション（断片化）

これはNTFSの欠点ではなく、ファイルシステムという仕組みの性質であるが、データの削除やデータサイズの増減を許容するファイルシステムでは、それら操作時の必要に応じてコンパクションを行わない限り、いずれかの段階で[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")が発生する。NTFSはFAT32と比較しフラグメンテーションしにくい。その根拠としてMFT機能が挙げられている\[11\]。フラグメンテーションの量はアロケーション ユニット サイズに反比例し、最も小さなアロケーション ユニット サイズの512バイトで最も顕著になる\[12\]。

FATよりは軽度とされたそのフラグメンテーションの実体は、[Diskeeper](../Page/Diskeeper.md "wikilink")のレポート機能などによって一般に知られるようになった。Windows 2000からNTFS対応の[デフラグ](../Page/デフラグ_\(Windows\).md "wikilink") ツールがWindowsに標準搭載された。

#### 機能制限

  - Windows XPおよびそれ以前のWindowsでは、NTFSボリュームをマウント状態にしたままでメンテナンスすることができない。Windows Vista以降ではデフォルトでバックグラウンドメインテナンスが行われている。
  - POSIX.1仕様では[シンボリックリンクが明記されていないことから](../Page/ソフトリンク.md "wikilink")、当初はシンボリックリンクをサポートしていなかった。その代わり、「ジャンクション」という類似の機能があるが、これはボリュームおよびフォルダに対してのみ提供される。Windows NT系では[ハードリンク](../Page/ハードリンク.md "wikilink")はサポートされており、Windows XPではコマンドラインから操作できる。Windows Vistaからシンボリックリンクにも対応するようになった。ジャンクションやシンボリックリンクは、[リパース ポイントと呼ばれる機能によって実現されている](https://ja.wikipedia.org/wiki/リパース_ポイント "wikilink")。

#### コードページ

基本的にはファイル名はUCS-2で格納される。ここでファイル名を非UNICODE文字種とUNICODEで参照した場合、名前の不一致が発生する。名前の不一致はコードページに依存し、名前空間の一貫性を損なってしまう。原則として厳密に名前空間を取り扱うのであれば、UNICODEでアクセスすべきで、ロケール依存コードページによってアクセスすべきではない。慣例的にコードページ依存文字を使う[ftp](https://ja.wikipedia.org/wiki/ftp "wikilink")などのプロトコルの取り扱いは注意を必要とする。

#### アクセスタイム

NTFSは従来のMS-DOSファイルシステムにはない、ファイル最終アクセス時刻を記録する。その為ファイルを読みだしただけでもディスクへの書き込みが生じる。このリード・モディファイ・ライトの特性が悪い方向に働くケースはいくつかある。一つは小さなたくさんのファイルへのアクセスでファイルシステムの性能を、。もう一つは[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")を使ったデバイスにアクセスした時に頻繁にページのフラッシュを発生させ、やはりファイルシステムの性能を低下させてしまう。Vista以降最終アクセス時刻は既定で更新されない。\[13\]

## Windows NT系以外からのアクセス

NTFSは元々、Windows NT系における[サーバ](../Page/サーバ.md "wikilink")用途を目的として開発されたファイルシステムであり、MS-DOSから使われてきたFATと互換性を持たない。そのため、クライアント向けのOSであるWindows 9x系からアクセスすることはできない。

Windows上では規模を拡大するNTFSだが、マイクロソフトの戦略やセキュリティにより、その仕様が一般には公開されていない。このため、他のOSからNTFSを「安全確実に」読み書きすることは事実上不可能である。しかし、現在では有志によって不完全ながらもNTFSにアクセスするための手段が用意されている。

  - mount
    [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")カーネル 2.4以降と [FreeBSD](../Page/FreeBSD.md "wikilink")などは、「<kbd>mount -t ntfs</kbd>」コマンドによって読み取りのみサポートしている。
  - NTFS-3G\[14\]
    [NTFS-3G](https://ja.wikipedia.org/wiki/NTFS-3G "wikilink")は、Tuxera社が開発しているNTFSドライバであり、NTFSパーティションへの読み書きに対応している。マイクロソフトと知的所有権の合意のもとで開発されていることから、他の実装と比較し、安定した読み書きが行えるとされる。各種Linux、FreeBSD、macOS、[BeOS](../Page/BeOS.md "wikilink") 上で動作する。オープンソースかつフリーである。実際にはユーザー アクセス手段の実装である[Filesystem in Userspace](../Page/Filesystem_in_Userspace.md "wikilink") (FUSE) も併せてインストールする必要がある。
  - Captive NTFS\[15\]
    Captive NTFSは、NTFSパーティションの読み書きに対応。使用するにはWindows内のドライバが必須。
  - NTFS for Windows98\[16\]
    NTFS for Windows98は、Windows 98からNTFSにアクセスするソフトであったが、Windows 9x系のサポート終了に伴い提供を終えた。
  - 市販のアクセス ドライバ
    「[Microsoft NTFS for Mac by Paragon Software](https://www.paragon-software.com/jp/home/ntfs-mac/)」（パラゴン ソフトウェア社） macOSに対応している。

## 脚注

## 関連項目

  - [マスター ファイル テーブル](https://ja.wikipedia.org/wiki/マスター_ファイル_テーブル "wikilink") (MFT)
  - [HPFS](../Page/HPFS.md "wikilink")

## 外部リンク

  - [Windows Sysinternals](http://technet.microsoft.com/en-us/sysinternals/default.aspx) - NTカーネルおよびNTFSに関するメンテナンス ツールを提供している。

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.  512バイト/セクタかつ1セクタ/クラスタ、つまり512バイト/クラスタのとき、8 [ZiB](https://ja.wikipedia.org/wiki/ゼビバイト "wikilink") - 512 Bytes。
2.
3.
4.
5.
6.  [A heavily fragmented file in an NTFS volume may not grow beyond a certain size](http://support.microsoft.com/kb/967351/en-us)
7.  Windows Server 2012のサーバーマネージャーの新しいボリュームウィザード上に「非推奨」と表記されている
8.
9.  [chkdsk の刷新と新しい NTFS 正常性モデルの追加](http://blogs.msdn.com/b/b8_ja/archive/2012/05/16/chkdsk-ntfs.aspx)
10.
11. [1](http://www.atmarkit.co.jp/fwin2k/experiments/defragment/defragment_column.html)
12. [2](http://support.microsoft.com/kb/902201/ja)
13.
14.
15. [Captive NTFS](http://www.jankratochvil.net/project/captive/)
16. [NTFS for Windows98](http://www.sysinternals.com/Utilities/NtfsWindows98.html)