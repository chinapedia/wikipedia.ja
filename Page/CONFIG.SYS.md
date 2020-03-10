> この記事は[CONFIG.SYS](https://ja.wikipedia.org/wiki/CONFIG.SYS)から翻訳されています。


**CONFIG.SYS**（コンフィグ シス）は[MS-DOS](../Page/MS-DOS.md "wikilink")や[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")などの[OSにおいて初期設定を行う](../Page/オペレーティングシステム.md "wikilink")[ファイルである](../Page/ファイル_\(コンピュータ\).md "wikilink")。また、[Windows NT系ではCONFIG](../Page/Windows_NT系.md "wikilink").NTという同様のファイルが存在する。

CONFIGとはConfiguration（コンフィギュレーション。「構造」、コンピュータ用語では「設定」などと訳される）の略といわれる。

## 概要

このファイルはOSが使用する[メモリ領域を指定したり](../Page/半導体メモリ.md "wikilink")、拡張メモリ（[8086系](../Page/Intel_8086.md "wikilink")[CPU](../Page/CPU.md "wikilink")の[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")において読み書きできない範囲にあるメモリ領域の呼称）や[CD-ROM](../Page/CD-ROM.md "wikilink")などの[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を組み込んだりするために、OSの起動時に最初に読み込まれる設定ファイルである。なお [Windowsでも下位層にMS](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")-DOS部分を持つ[9x系では起動初期の設定に用いられることがある](https://ja.wikipedia.org/wiki/Windows_9x系 "wikilink")。

CONFIG.SYSは起動ドライブの[ルートディレクトリ](https://ja.wikipedia.org/wiki/ルートディレクトリ "wikilink")に配置される。なお一部の互換DOS（MS-DOSとの互換性を保つように造られているものの[マイクロソフト](../Page/マイクロソフト.md "wikilink")非公認のOSの呼称）においてはファイル名が異なる場合がある（[DR-DOS](https://ja.wikipedia.org/wiki/DR-DOS "wikilink")の場合はDCONFIG.SYS、[FreeDOS](../Page/FreeDOS.md "wikilink")ではFDCONFIG.SYS）。

## 構文

基本的に CONFIG.SYS は先頭から順に解釈されるが、一部のコマンド（命令文）は任意の行に置くことができる。

  - DEVICE=(デバイスドライバの[パス](../Page/ディレクトリ.md "wikilink")、[パラメータ](../Page/引数.md "wikilink")) - [コンベンショナルメモリにデバイスドライバを組み込む](https://ja.wikipedia.org/wiki/MS-DOS#メモリ管理 "wikilink")。
  - BUFFERS=(数値) - ディスクアクセス（読み書き）のための[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")領域数。
  - FILES=(数値) - ファイルハンドル（OSを通して開くファイルに付与される識別番号）の最大数。つまり同時に開くことのできるファイルの最大数。
  - FCBS=(数値) - FCB（ファイルコントロールブロック、MS-DOSバージョン2.0以前で使われていたファイル管理方法）で同時に開くことのできるファイルの最大数。
  - SHELL=(シェルのパス、パラメータ) - [シェル](../Page/シェル.md "wikilink")プログラムの指定。省略すると "\\[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")" が仮定される。
  - LASTDRIVE=(A-Z) - 最後に使用するドライブ識別文字。省略すると "P" が仮定される。

<!-- end list -->

  - [DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")のみ

<!-- end list -->

  - COUNTRY=(国番号),([コードページ](../Page/コードページ.md "wikilink")),(country.sysのパス) - [コードページ](../Page/コードページ.md "wikilink")の指定

<!-- end list -->

  - MS-DOSバージョン5.0以降

<!-- end list -->

  - DEVICEHIGH=(デバイスドライバのパス、パラメータ) - [UMBにデバイスドライバを組み込む](https://ja.wikipedia.org/wiki/Upper_Memory_Area "wikilink")（UMBが使用不可、または入りきらない場合はコンベンショナルメモリに組み込む）。
  - DOS=(HIGH/LOW),(UMB|NOUMB) - MS-DOSのシステム本体を[HMAに組み込むか否かの選択](https://ja.wikipedia.org/wiki/XMS "wikilink")（HIGHでHMAに組み込む）と、UMBを使用可にするか使用不可にするかの選択（"UMB"で有効、"NOUMB"で無効）。省略するとLOW, NOUMBが仮定される。

<!-- end list -->

  - MS-DOSバージョン 6.2 以降

<!-- end list -->

  - INSTALL=(常駐コマンドのパス、パラメータ) - デバイスドライバ以外の常駐プログラムを実行する。
  - SET (変数名)=(文字列) - [環境変数](../Page/環境変数.md "wikilink")を設定する。
  - BREAK (ON/OFF) - CTRL+C（STOP または BREAK）割り込みの有効／無効指定。
  - 行頭の REM または ";" - 注釈文の行とみなされ、OSでは読み飛ばされる。
  - 行頭の "?" - コマンド実行前に都度確認する。

## CONFIG.SYSの例

### イギリスで稼働しているPC/AT互換機における例

```
 device = c:\dos\himem.sys
 device = c:\dos\emm386.exe umb
 dos = high,umb
 devicehigh = c:\windows\mouse.sys
 devicehigh = c:\dos\setver.exe
 devicehigh = c:\dos\smartdrv.exe
 country = 044,437,c:\dos\country.sys
 shell = c:\dos\command.com c:\dos /e:512 /p
```

この例の各行の記述は以下の通り。

1.  コンベンショナルメモリ上でhimem.sysを実行する。これにより[XMS](https://ja.wikipedia.org/wiki/XMS "wikilink")方式による拡張メモリへのアクセスが可能になる。
2.  コンベンショナルメモリ上で[emm386.exeを実行する](../Page/EMM386.md "wikilink")。[EMS方式によるメモリアクセスの他](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")、UMBも使用可能になる。
      -
        なお、この行におけるemm386.exeの引数には、このほかに "ram"（EMS使用）や "noems"（UMBのみ）などが存在する。
3.  MS-DOS 本体をHMAに組み込み、UMBを使用可能にする。
4.  UMB 上でmouse.sysを実行する。
5.  UMB 上でsetver.exeを実行する。
6.  UMB 上でsmartdrv.exeを実行する。
7.  地域をイギリス、コードページを437(英語)にする。
8.  [シェル](../Page/シェル.md "wikilink")として[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")を使用する。この際に常駐部分を完全に常駐させる(EXITコマンドで終了しない)とともに、[環境変数](../Page/環境変数.md "wikilink")領域を512バイト確保する。

### 日本で稼働しているNEC PC-9800シリーズにおける例（バージョン5.0以上の場合）

PC-9800シリーズでは、[コンソール](https://ja.wikipedia.org/wiki/コンソール "wikilink")画面において日本語表示に標準対応しているため、[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")で日本語キーボードや日本語表示を利用する際に必要となる各種ドライバ類は不要である。また同機種は日本での利用を前提としているため（日本国外では動作保証されない）、国番号などの指定も省略する。

    DEVICE=A:\DOS\HIMEM.SYS
    DEVICE=A:\DOS\EMM386.EXE /UMB
    DEVICEHIGH=A:\DOS\NECCD.SYS /D:CD_101
    SHELL=A:\COMMAND.COM /P /E:2000
    LASTDRIVE=Q
    DOS=HIGH,UMB

1.  コンベンショナルメモリ上でHIMEM.SYSを実行し、XMS方式による拡張メモリの利用を可能にする。
2.  コンベンショナルメモリ上でEMM386.EXEを実行し、EMS方式によるメモリアクセスおよびUMBを使用可能にする。
3.  UMBにNECCD.SYS（CD-ROM ドライブを使用可能にするデバイスドライバ）を読み込み、そのドライブの内部名を"CD_101"にする。
4.  シェルコマンドにA:\\[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")を使用し、環境変数領域を2000バイト確保する。
5.  ドライブQ:までを使用可能にする。
6.  MS-DOS本体でHMAおよびUMBを利用する。

## 外部リンク

  - Microsoftサポート技術情報
      - [W98:README：MS-DOS CONFIG.SYS コマンド](http://support.microsoft.com/kb/412281/ja)
      - [Maximum Line Length and Count for Batch Files & CONFIG.SYS](http://support.microsoft.com/kb/69563/en-us)
      - [\[DOS](http://support.microsoft.com/kb/411572/ja)基本的な CONFIG.SYS と AUTOEXEC.BAT ファイルの例\]

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [MSDOS.SYS](https://ja.wikipedia.org/wiki/MSDOS.SYS "wikilink")
  - [AUTOEXEC.BAT](../Page/AUTOEXEC.BAT.md "wikilink")

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:OS/2](https://ja.wikipedia.org/wiki/Category:OS/2 "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")