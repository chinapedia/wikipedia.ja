> この記事は[Microsoft Windows Services for UNIX](https://ja.wikipedia.org/wiki/Microsoft_Windows_Services_for_UNIX)から翻訳されています。


**Microsoft Windows Services for UNIX** (**SFU**) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する[Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[UNIX](../Page/UNIX.md "wikilink")の相互運用を支援するソフトウェアパッケージ集。[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") R2以降は**Subsystem for UNIX-based Applications** (**SUA**) へと引き継がれている。

## 主な機能

  - [GCC](../Page/GNUコンパイラコレクション.md "wikilink") 3.3 コンパイラ、ヘッダファイル、ライブラリ
  - [Microsoft Visual Studioコマンドラインコンパイラのccラッパー](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [GDB](https://ja.wikipedia.org/wiki/GDB "wikilink")
  - [NFSクライアントとサーバ](https://ja.wikipedia.org/wiki/Network_File_System "wikilink")
  - [X Window Systemクライアント](../Page/X_Window_System.md "wikilink")（サーバは提供されない）
  - [Telnet](../Page/Telnet.md "wikilink")サーバ
  - [NISサーバ](https://ja.wikipedia.org/wiki/Network_Information_Service "wikilink")
  - パスワード同期サービス
  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")サブシステム
  - UNIXツール群

## 歴史

  - [1999年](../Page/1999年.md "wikilink")[4月16日](https://ja.wikipedia.org/wiki/4月16日 "wikilink") :Windows NT Services for UNIX Add-on Pack日本語版 （29,800円）
    [2000年](../Page/2000年.md "wikilink")[8月11日](../Page/8月11日.md "wikilink") :Windows Services for UNIX Version 2.0 日本語版 （29,800円）
    [2002年](../Page/2002年.md "wikilink")[12月6日](../Page/12月6日.md "wikilink") :Windows Services for UNIX Version 3.0 日本語版 （29,800円）
    [2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")[1月20日](../Page/1月20日.md "wikilink") :Windows Services for UNIX Version 3.5 日本語版 （無償）
    [2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[12月6日](../Page/12月6日.md "wikilink") :Windows Server 2003 R2 Subsystem for UNIX-based Applications (5.2)
    [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[11月8日](../Page/11月8日.md "wikilink") :Windows Vista Subsystem for UNIX-based Applications (6.0)

元々はパッケージ製品として販売されていたが、2004年1月のSFU 3.5から無償提供された。

[Windows XPと](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Server 2003ではWindowsは](../Page/Microsoft_Windows_Server_2003.md "wikilink")[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")サブシステムが削除された為、POSIXを利用するには同パッケージが必須である。

## Subsystem for UNIX-based Applications

[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") R2 と [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Windows 7](https://ja.wikipedia.org/wiki/Microsoft_Windows_7 "wikilink") (Ultimate, Enterprise) と [Windows Server 2008](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008 "wikilink")、[Windows Server 2008 R2では](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink")、Subsystem for UNIX-based Applications (SUA) として、標準搭載されている。

## Windows Server 2012 以降の UNIX互換環境

[Windows Server 2012からマイクロソフト提供のUNIXベースアプリケーション用サブシステムが奨励されなくなった為](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink")、[Hyper-V](https://ja.wikipedia.org/wiki/Hyper-V "wikilink")でネイティブOS、または従来のOSを仮想化するか、公式に以下の環境を奨励している\[1\]。また、次期バージョンの[Windows 8.1および](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")[Windows Server 2012 R2からは完全に削除されているが](https://ja.wikipedia.org/wiki/Windows_Server_2012_R2 "wikilink")、組み込み向けの[Windows Embedded 8.1](https://ja.wikipedia.org/wiki/Windows_Embedded_8.1 "wikilink") Proには搭載された\[2\]。

  - [Cygwin](../Page/Cygwin.md "wikilink")
  - [mingw-w64または](https://ja.wikipedia.org/wiki/MinGW "wikilink")[MinGW](https://ja.wikipedia.org/wiki/MinGW "wikilink")

windows10では、正式版リリース一周年(2016年9月)の大型アップデートにより、64ビット版に限りSUAの後継ないし類似製品として 「 [Windows Subsystem for Linux](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink") 」 が利用可能となる。

## 脚注

## 関連項目

  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")
  - [Cygwin](../Page/Cygwin.md "wikilink")

## 外部リンク

  - [＠IT:Insider's Eye SFU 3.5はなぜ無償化されたのか](http://www.atmarkit.co.jp/fwin2k/insiderseye/20040319sfu35/sfu35.html)

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")

1.  [Windows Server 2012 で削除された機能または推奨されなくなった機能](http://technet.microsoft.com/ja-jp/library/hh831568) - Microsoft technet
2.  [Windows Embedded 8.1 Industry ; Das neue Windows Embedded OS](http://www.nik-nbg.de/uploads/tx_seminars/Windows_Embedded_8.1_Industry_Alexander_Wechsler.pdf)Alexander Wechsler , Wechsler Consulting GmbH & Co. KG