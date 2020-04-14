> この記事は[ファイルマネージャー \(Windows\)](https://ja.wikipedia.org/wiki/ファイルマネージャー_\(Windows\))から翻訳されています。


**ファイルマネージャー**は1990年から1999年まで[Microsoft Windows内のアプリケーションとして存在していた](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ファイル管理プログラムである](https://ja.wikipedia.org/wiki/ファイルマネージャ "wikilink")。また2018年4月6日から、[Windows 10を含む現代のWindowsにおいても任意でダウンロードすることで](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")、動作させることができる。\[1\]\[2\]

[Windows 3.1などの以前のWindowsにおいて](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")、単一の画面で[ファイル](https://ja.wikipedia.org/wiki/ファイル "wikilink")の管理 (コピー、移動、開く(実行), 削除、検索等の操作)が行え、 [MS-DOS](../Page/MS-DOS.md "wikilink")コマンドによる[コマンドラインインターフェースおよびMS](../Page/キャラクタユーザインタフェース.md "wikilink")-DOSウィンドウ(MS-DOS Executive)でのファイルの管理を置き換えた。 [Windows 95や](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")[Windows NTおよびそれ以降のバージョンにおいては](https://ja.wikipedia.org/wiki/Windows_NT_4.0 "wikilink")、ファイル管理に[Windows エクスプローラーが導入され](../Page/Windows_Explorer.md "wikilink")、"マイ コンピュータ"アイコンをダブルクリックすることで表示されるシングルペイン構成の画面と比較して、ファイルマネージャーは(通常)2ペイン構成であり、画面構成が異なる。

## 概要

The program's interface showed a list of [directories](https://ja.wikipedia.org/wiki/directory_\(file_systems\) "wikilink") on the left hand panel, and a list of the current directory's contents on the right hand panel. File Manager allowed a user to create, rename, move, [print](https://ja.wikipedia.org/wiki/Printer_\(computing\) "wikilink"), copy, search for, and delete files and directories, as well as to set [permissions](https://ja.wikipedia.org/wiki/file_system_permissions "wikilink") ([attributes](https://ja.wikipedia.org/wiki/File_attribute "wikilink")) such as archive, read-only, hidden or system, and to associate file types with programs. Also available were tools to label and [format](https://ja.wikipedia.org/wiki/disk_formatting "wikilink") disks, manage folders for file sharing and to connect and disconnect from a [network drive](https://ja.wikipedia.org/wiki/network_drive "wikilink"). On [Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink") systems it was also possible to set [ACLs](https://ja.wikipedia.org/wiki/Access_control_list "wikilink") on files and folders on [NTFS](https://ja.wikipedia.org/wiki/NTFS "wikilink") partitions through the shell32 security configuration dialog (also used by Explorer and other Windows file managers). On NTFS drives, individual files or entire folders could be compressed or expanded.

The Windows NT version of File Manager allows users to change directory, file, local, network and user permissions.

Windows 95からWindows NT 4.0以降、ファイルマネージャーはWindows エクスプローラーによって置き換わった。しかし`WINFILE.EXE`はWindows 95, [Windows98](https://ja.wikipedia.org/wiki/Windows98 "wikilink"), [Windows Meの時点ではまだ](https://ja.wikipedia.org/wiki/Windows_Me "wikilink")16ビットアプリケーションとして、Windows NT 4.0では32ビットアプリケーションとして含まれていた 。 The last 32-bit `WINFILE.EXE` build (4.0.1381.318) was distributed as part of Windows NT 4.0 Service Pack 6a (SP6a). The last 16-bit `WINFILE.EXE` build (4.90.3000) was distributed as part of Windows Me operating system.

[クリス・ガザック](https://ja.wikipedia.org/wiki/クリス・ガザック "wikilink")はWindows 3.1開発チームのうちの1人であり、ファイルマネージャーのシェルの部分を担当していた。\[3\]

2018年にマイクロソフトはMITライセンスの下にソースコードを[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")に公開した。\[4\]

## バージョンの一覧

### 16ビット版

オリジナルの16ビット版ファイルマネージャは[8.3形式](https://ja.wikipedia.org/wiki/8.3形式 "wikilink")のファイル名を表示する。

Windows95に含まれているファイルマネージャにおいても、[ロングファイルネーム](https://ja.wikipedia.org/wiki/ロングファイルネーム "wikilink")または空白文字が含まれていた場合、前述の8.3形式のファイル名形式に従い、ファイル名のうち最初の6文字と、その後チルダ(\~)と数字の組み合わせ(1, 2, 3...)により表示する。

[Windows 3.1](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")、[Windows for Workgroups 3.1xに含まれていたファイルマネージャは](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")、[2000年問題](../Page/2000年問題.md "wikilink")に対応しておらず、ファイル名の日付部がセミコロンに置き換わるバグが存在した。マイクロソフトはこの問題に対し、すべてのWindows 3.1x OS環境下に修正したモジュールを配布した。\[5\]

### Windows NT版

Windows NT 32ビットプログラム版として書き直されたバージョンである。このバージョンはロングファイルネームおよび[NTFS](https://ja.wikipedia.org/wiki/NTFS "wikilink")ファイルシステムを新たにサポートした。Windows NT バージョン3.1, 3.5, 3.51, 4.0に含まれている。

### Windows 10版

2018年4月6日に、マイクロソフトはソースコードおよびバイナリを[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")をもとに公開した。この公開されたバージョンは、Windows10でも動作するよう改善されたバージョンである。 \[6\]\[7\] このバージョンは現代のVisual Studioでも64ビットアプリケーションとしてコンパイルできるように、いくつかの改良がなされている。\[8\] また、マイクロソフト社は2019年1月下旬に[Microsoftストア](https://ja.wikipedia.org/wiki/Microsoftストア "wikilink")にフリー版を公開している。

## 関連項目

  - [DOSシェル](https://ja.wikipedia.org/wiki/DOSシェル "wikilink")

## 参照記事

## 外部リンク

  - (英語)

  - [Windows File Manager を入手 - Microsoft Store ja-JP](https://www.microsoft.com/ja-jp/p/windows-file-manager/9p7vbbbc49rb)

<!-- end list -->

1.
2.
3.
4.
5.
6.
7.
8.