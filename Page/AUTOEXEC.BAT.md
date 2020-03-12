> この記事は[AUTOEXEC.BAT](https://ja.wikipedia.org/wiki/AUTOEXEC.BAT)から翻訳されています。


**`AUTOEXEC.BAT`**（オートエグゼック・バット）は、[DOS系オペレーティングシステムで利用されるシステムファイルの名前である](../Page/DOS_\(OS\).md "wikilink")。中身は[テキスト形式の](../Page/テキストファイル.md "wikilink")[バッチファイル](../Page/バッチファイル.md "wikilink")であり、[ブート](../Page/ブート.md "wikilink")デバイスの[ルートディレクトリ](../Page/ルートディレクトリ.md "wikilink")に置かれる。

AUTOEXECとは "automatic execution"（自動実行）の略であり、システム起動時に[コマンド群を自動実行させる機能を持つことに由来する](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。このような[かばん語](../Page/かばん語.md "wikilink")にしたのは、[FAT系ファイルシステムのファイル名の長さ制限に対応するためである](../Page/File_Allocation_Table.md "wikilink")。「オートエクゼ」などと略されることもある。

## 使用法

`AUTOEXEC.BAT` が使われるのは、[MS-DOS](../Page/MS-DOS.md "wikilink")とそれをベースとした[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（[Windows 3.xまでと](../Page/Microsoft_Windows_3.x.md "wikilink")[Windows 9x系](../Page/Windows_9x系.md "wikilink")）である。このファイルはオペレーティングシステムの立ち上げ時、[`CONFIG.SYS`](../Page/CONFIG.SYS.md "wikilink")が処理された後で実行される。Windowsでは、これはグラフィカル環境が開始する前になされる。`CONFIG.SYS`とは異なり、`AUTOEXEC.BAT`内のコマンドは[DOSプロンプトから入力可能である](../Page/コマンドラインインタプリタ.md "wikilink")。このファイルは単にユーザーがコンピュータを起動したとき自動的に実行したいコマンドを入れているだけである。

よく見られる AUTOEXEC.BAT の使い方としては、[環境変数](../Page/環境変数.md "wikilink")を設定し、[ウイルススキャナーや何らかのシステム拡張やユーティリティを動作させ](../Page/アンチウイルスソフトウェア.md "wikilink")、低レベルで動作するドライバハンドラ（例えば[リアルモード](../Page/リアルモード.md "wikilink")のマウスやCD-ROMドライバなど）を起動させたりする。

[Windows Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink") では環境変数の設定のみを行うが\[1\]、これを変更することも可能である\[2\]。

[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") とその系統の [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") や [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") は、ユーザーがログオンした際に `AUTOEXEC.BAT` を調べる。Windows Me と同様、環境変数の設定以外は無視される\[3\]。

Windows上で起動時に実行したいアプリケーションは[レジストリ](../Page/レジストリ.md "wikilink")に記述する。

## 例

初期のDOSでは、デフォルトの`AUTOEXEC.BAT`は極めて単純だった。`date`コマンドと`time`コマンドは、初期の[PCがバッテリバックアップされた](../Page/IBM_PC.md "wikilink")[リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")を備えていなかったため、必須だった。

``` dos
echo off
cls
date
time
ver
```

アメリカ仕様以外の環境では、キーボードドライバも必要である（例えばフランス語版ならKEYBFR）。その後、様々なサードパーティ製デバイスドライバを起動することが多くなった。次の例は、DOS 5.x での基本的なコマンドだけで構成した`AUTOEXEC.BAT`である。

``` dos
@echo off
prompt $P$G
PATH=C:\DOS;C:\WINDOWS
set TEMP=C:\TEMP
set BLASTER=A220 I7 D1 T2
lh smartdrv.exe
lh doskey
lh mouse.com /Y
win
```

この例では共通の環境変数を設定した後、6行目でディスクキャッシュ [SmartDrive](https://ja.wikipedia.org/wiki/:en:SmartDrive "wikilink") をロードし、DOSのキーボードとマウスのドライバを起動してから、最後にWindowsを起動している。`prompt`コマンドは、DOSプロンプトを単純な "C\>" から "C:\\\>" に変更している。

一般に .SYS ファイルは `CONFIG.SYS` から呼び出し、*SmartDrive* のような[.EXE](../Page/EXEフォーマット.md "wikilink") プログラムは`AUTOEXEC.BAT`でロードする。マウスなどのデバイスは、.SYS ファイルとして `CONFIG.SYS` でロードすることもできるし、[.COM](../Page/COMファイル.md "wikilink") として `AUTOEXEC.BAT` でロードすることもでき、製造業者によって採用する技法が異なる\[4\]。

行の先頭に**REM**があるのは注釈を意味し、`AUTOEXEC.BAT`の一部として実行されることはない。"REM"のついた行はコメント行として使われたり、[トラブルシューティング](../Page/トラブルシューティング.md "wikilink")などのためにドライバを起動しないようにするときなどに使われる。同様のことは[コロンを](../Page/コロン_\(記号\).md "wikilink")2つ、あるいはコロンと半角スペースを行の先頭につけることでも実現される(**::**、''': ''')。

MS-DOS 6 およびそれ以降では、DOSのブートメニューは設定変更可能である。そのため、各種プログラム（DOSゲームやWindowsなど）に対応してブート設定を最適化させることができる。

``` dos
@echo off
prompt $P$G
PATH=C:\DOS;C:\WINDOWS
set TEMP=C:\TEMP
set BLASTER=A220 I7 D1 T2
goto %CONFIG%
:WIN
 lh smartdrv.exe
 lh mouse.com /Y
 win
goto END
:XMS
 lh smartdrv.exe
 lh doskey
 goto END
:END
```

`goto %CONFIG%` という行は、DOSに [`CONFIG.SYS`](../Page/CONFIG.SYS.md "wikilink") で定義されたメニューエントリを参照することを指示するものである。そして得られたプロフィール名に従って必要なドライバやユーティリティを設定する。設定完了後 `goto` コマンドで `:END`セクションまで飛ばす。`:END`以降の記述は全プロフィールで共通である。

## DOSと Win 9x のデュアルブート

[Windows 95](../Page/Microsoft_Windows_95.md "wikilink") を既に DOS や Windows がインストールされた環境にインストールすると、`CONFIG.SYS` と `AUTOEXEC.BAT` を `CONFIG.DOS` と `AUTOEXEC.DOS` に移動させようと試みる。これは Windows 9x と DOS の間でデュアルブートを容易にさせようとしてのことである。DOSでブートする際には、それらを一時的に `CONFIG.SYS` と `AUTOEXEC.BAT` に戻し、Win95版のファイルは `.W40` ファイルとしてバックアップ保存する。

Windows 9x は偽の[`MSDOS.SYS`](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink")ファイルもインストールする。このファイルには自動的に Windows に移行するかどうかも含めたシステムのブート手順を示すスイッチがいくつか含まれている。DOSプロンプトで立ち上げるには、この "BootGUI" オプションを "0" にセットする必要がある。そうするとシステムの動作はそれ以前の DOS/Windows ペアのようになる。WindowsはDOSプロンプトから "WIN" と入力することで起動できる。

カルデラの [DR-DOS](../Page/DR-DOS.md "wikilink") 7.02 かそれ以降をインストールすると、Windows版のファイルは `AUTOEXEC.BAT` のままでよく、DR-DOS は `AUTODOS7.BAT` というファイル名を使用する。[CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink") も違う名前となっており、`DCONFIG.SYS` である\[5\]。

## Windows NT と OS/2

[Windows NT系では](../Page/Windows_NT系.md "wikilink")、同様の機能を持つファイルとして`AUTOEXEC.NT`があり、[`%SystemRoot%`](../Page/環境変数.md "wikilink")`\system32`ディレクトリに置かれている。このファイルはオペレーティングシステムの起動処理では使われず、MS-DOSアプリケーションをロードしたときなど MS-DOS環境が起動したときに実行される。

Windows NT 系システムでもルートディレクトリに`AUTOEXEC.BAT`が置かれている場合がある。Windowsはその中の"SET"文と"PATH"文だけを認識し、全ユーザー向けの[環境変数](../Page/環境変数.md "wikilink")設定に使用する。このファイルシステムがFATであれば、同じところにMS-DOSもインストールすると、2つのOSの間で AUTOEXEC.BAT が共有されることになる。ただし、そのような使い方をする人は滅多にいないので、このファイルはたいていの場合空である。

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") は`AUTOEXEC.BAT`の代わりに `startup.cmd` を使用する。

## 脚注

## 関連項目

  - [DOS (OS)](../Page/DOS_\(OS\).md "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")
  - [IO.SYS](../Page/IO.SYS.md "wikilink")
  - [MSDOS.SYS](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink")
  - [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")
  - [CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink")

## 外部リンク

  - [Windows 98 Config.txt File](http://support.microsoft.com/?kbid=232557)

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")

1.  ["Subst" Command Does Not Work in Autoexec.bat File in Windows Millennium Edition](http://support.microsoft.com/kb/288997/en-us)
2.
3.  [INFO: Configuring Parsing of the AUTOEXEC.BAT File](http://support.microsoft.com/kb/124551/)
4.  [Mouse Doesn't Work with MS-DOS Shell](http://support.microsoft.com/kb/96706)
5.  <http://www.drdos.com/dosdoc/usergeng/01ugch1.htm>