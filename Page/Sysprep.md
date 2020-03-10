> この記事は[Sysprep](https://ja.wikipedia.org/wiki/Sysprep)から翻訳されています。


**Sysprep**(**Sys**tem **Prep**aration Utility)とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[Windowsオペレーティングシステムを展開するためのシステム準備ツールの名前である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。現在このツールの実行ファイル名はSysprep.exeである。

## 歴史

Sysprepは、[Windows NT 4.0で初めて導入された](https://ja.wikipedia.org/wiki/Windows_NT_4.0 "wikilink")。[Windows 2000や](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")[Windows XP用のSysprepが現在マイクロソフトから入手可能である](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")。[Windows Vistaは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、製品パッケージからのインストールにSysprepが使用される初めてのバージョンである。

## 使用用途

デスクトップの展開は一般的に、[ディスク複製](https://ja.wikipedia.org/wiki/ディスク複製 "wikilink")ソフトウェアによって行われる。Sysprepは、[ディスクイメージ](https://ja.wikipedia.org/wiki/ディスクイメージ "wikilink")によるディスクの複製と復元のためのオペレーティングシステムを準備するために使うことが出来る。

Windowsオペレーティングシステムのインストールでは、インストールごとに一意に生成される多くの要素があり、多数のコンピュータにディスクイメージを複製して展開する前に一般化しておく必要がある。いくつかの要素の例:

  - コンピュータ名
  - [セキュリティ識別子](https://ja.wikipedia.org/wiki/セキュリティ識別子 "wikilink")([SID](https://ja.wikipedia.org/wiki/SID "wikilink"))
  - ドライバキャッシュ

SysprepはSysprepのプロセスの間に新しいコンピュータ名、一意なSID、カスタムドライバキャッシュデータベースの生成を行うことでこれらの問題を解決しようとする。

管理者はSetupMgr.exe（Windows XPの場合）またはSystem Image Manager（Windows Vistaの場合）をSysprepによる新しいコンピュータへの展開処理の応答ファイルを作成するために使用することが出来る。

## 外部リンク

  - [Sysprep ツールを使用して Windows XP の展開を自動化する方法](http://support.microsoft.com/kb/302577/ja)
  - [Hardware devices not installed in Sysprep image](http://support.microsoft.com/default.aspx?scid=kb;en-us;837691)
  - [Windows XP の Sysprep の新機能](http://support.microsoft.com/kb/282190/ja)
  - [Informational guide on how to use Sysprep for deploying Windows 2000/XP](http://vernalex.com/guides/sysprep/)
  - [Sysprep for Windows 2008 R2](http://www.happysysadm.com/2010/11/vmware-windows-2008-r2-template.html)

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink")