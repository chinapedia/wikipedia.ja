> この記事は[Cooperative Linux](https://ja.wikipedia.org/wiki/Cooperative_Linux)から翻訳されています。


**Cooperative Linux**は、[Microsoft Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")である。Dan Aloniが開発した。略称は**coLinux**。[Windows 2000](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")・[Windows XP](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")・[Windows Vista](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")・[Windows 7で利用できる](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")。[エミュレータ](../Page/エミュレータ.md "wikilink")や[仮想マシンではなく](../Page/仮想機械.md "wikilink")、本物のLinuxカーネルがWindows上で動作することが大きな特徴である。[TAP-Win32](https://ja.wikipedia.org/wiki/TAP-Win32 "wikilink")や[WinPcap](https://ja.wikipedia.org/wiki/WinPcap "wikilink")といったネットワークツールを経由して外部のネットワークへ接続が可能。

Dan Aloniは**coLinux**以前に[Umlwin32](http://umlwin32.sourceforge.net/)と言うものを開発していた。これは[Linux](../Page/Linux.md "wikilink")の[UML技術を](https://ja.wikipedia.org/wiki/ユーザーモードLinux "wikilink")[Microsoft Windowsに実装しようとしたもので](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、Dan AloniはUmlwin32をより実用的に発展させたものとして、UMLとは違う切り口から**coLinux**の開発を始めた。

## 動作原理

  - Windows[アプリケーションとしてLinuxカーネルが動作する](../Page/アプリケーションソフトウェア.md "wikilink")
  - Windows用[ドライバとしてlinux](../Page/デバイスドライバ.md "wikilink").sysがLinuxカーネルからの/への入出力を行う
  - [補助記憶装置は実パーティション又はディスクイメージを利用する](https://ja.wikipedia.org/wiki/ストレージ "wikilink")
  - [メインメモリは一般的なアプリケーションと同様](../Page/主記憶装置.md "wikilink")、Windowsの[ユーザー空間](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")の一部を利用する(起動時に設定ファイルの記述により割当量を決定する)
  - 現時点では[ディスプレイアダプタおよびサウンドアダプタは実装されていない](../Page/ビデオカード.md "wikilink")。そのため、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")を利用するには[X Window Systemや](../Page/X_Window_System.md "wikilink")[VNCを使ってリモートコンピュータのように接続する](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink")。音声はサウンド[サーバ](../Page/サーバ.md "wikilink")を利用することで再生できる。

## 特徴

### 仮想マシンとの比較

  - 入出力のオーバーヘッドが少なく高速である。
  - 通常の[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")やブートローダを用いないため、起動が高速である。
  - NTサービスとしてLinuxを稼動させることができる。
  - coLinuxはカーネルバージョンを変更できない。

### Cygwinとの比較

  - coLinux は「本物の」Linuxであるため、Linux用の通常のバイナリが利用できる。すなわち豊富な既存のLinux用ソフトウェアが利用できる。
  - [Debian GNU/Linuxや](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")といった、一般のLinuxディストリビューションを、ほぼそのままcoLinux上で利用できる。
  - 入出力のオーバーヘッドで課題の大きい[Cygwin](../Page/Cygwin.md "wikilink")と比較して高速である。

### Windows/Linuxデュアルブート環境との比較

  - Windows上で動作するソフトウェアとLinux上で動作するソフトウェアを同時に並行して利用できる。
  - 同時に複数のcoLinuxを起動できる。

## 外部リンク

  - [colinux.org(英語)](http://www.colinux.org/)
      - [Snapshots(英語)](http://www.colinux.org/snapshots/)
  - [The User-mode Linux Kernel HomePage(英語)](http://user-mode-linux.sourceforge.net/)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")