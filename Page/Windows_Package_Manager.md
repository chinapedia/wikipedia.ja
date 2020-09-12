> この記事は[Windows Package Manager](https://ja.wikipedia.org/wiki/Windows_Package_Manager)から翻訳されています。


**Windows Package Manager** (**winget**) は、[Windows 10向けの](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")[フリーかつオープンソースの](../Page/FLOSS.md "wikilink")[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")である。 [コマンドラインユーティリティと](../Page/キャラクタユーザインタフェース.md "wikilink")、アプリケーションをインストールするための一連のサービスから構成されている\[1\]\[2\]。 [ISV](https://ja.wikipedia.org/wiki/ISV "wikilink")はソフトウェアパッケージの配布チャネルとしてこれを利用することができる。

## 歴史

Windows Package Managerはので初めて発表された\[3\]\[4\]。

Windows Package Managerの開発が決定する前、開発チームは様々な代替オプションを検討し、[Chocolatey](https://ja.wikipedia.org/wiki/Chocolatey "wikilink")、Scoop及びなどの有名なパッケージ管理システムの開発チームや、AppGet、Npackd及び[PowerShell](../Page/PowerShell.md "wikilink")ベースのOneGetなどと協議を行った\[5\]。

wingetのリリース後、AppGetの開発者であるKeivan Beigiは、マイクロソフトがAppGetを買収し、から彼を雇用するという名目で話し合ったと主張した\[6\]。 この話し合いの後に、wingetのリリースの前日に彼を雇用しないことを確認するまで、マイクロソフトは彼との連絡を中断した。 彼はマイクロソフトがAppGetを帰属させないことに失望した。 wingetのリリース後、彼はAppGetのメンテナンスをに終了することを発表した\[7\]\[8\]\[9\]。 マイクロソフトはAppGetがwingetの多くの機能に貢献したことをブログに投稿することでこれに対応した\[10\]\[11\]。

## 概要

wingetは[EXE](../Page/EXEフォーマット.md "wikilink")、[MSIX及び](https://ja.wikipedia.org/wiki/Windows_Installer "wikilink")[MSIに基づくインストーラをサポートしている](https://ja.wikipedia.org/wiki/Windows_Installer "wikilink")\[12\]。 パブリックリポジトリはサポートされているアプリケーションのを[YAML](../Page/YAML.md "wikilink")形式でホストしている\[13\]。

[マルウェア](../Page/マルウェア.md "wikilink")がリポジトリとコンピュータに侵入する可能性を減らすために、Windows Package Managerは、及び[SHA-256](https://ja.wikipedia.org/wiki/SHA-256 "wikilink")[ハッシュ検証を利用している](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")\[14\]\[15\]。

wingetの[ソースコード](../Page/ソースコード.md "wikilink")及びコミュニティベースのマニフェストリポジトリは[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")の下でライセンスされており、[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")でホストされている\[16\]\[17\]。

## 歴史

以下は、マイクロソフトのフリーかつオープンソースの[ソースコードエディタ](https://ja.wikipedia.org/wiki/ソースコードエディタ "wikilink")である[Visual Studio Codeをインストールする場合の例である](https://ja.wikipedia.org/wiki/Visual_Studio_Code "wikilink")\[18\]:

``` PowerShell
PS C:\Users\Wikipedia> winget install vscode
```

## 脚注

### 注釈

### 出典

## 関連項目

  - [Web Platform Installer](https://ja.wikipedia.org/wiki/Web_Platform_Installer "wikilink")
  - [NuGet](https://ja.wikipedia.org/wiki/NuGet "wikilink")

## 外部リンク

  - \-

  -
  -
[Category:2020年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2020年のソフトウェア "wikilink") [Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink") [Category:マイクロソフトのソフトウェア](https://ja.wikipedia.org/wiki/Category:マイクロソフトのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  [Windows Package Manager Preview | Windows Command Line](https://devblogs.microsoft.com/commandline/windows-package-manager-preview/)
3.  [Microsoft debuts Windows Package Manager for your dev environment | VentureBeat](https://venturebeat.com/2020/05/19/microsoft-windows-package-manager-powertoys/)
4.
5.
6.
7.
8.
9.
10.
11. [Microsoft gives AppGet creator credit for Windows Package Manager - Neowin](https://www.neowin.net/news/microsoft-gives-appget-creator-credit-for-windows-package-manager)
12. [Use the winget tool to install and manage applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/package-manager/winget/)
13. [GitHub - microsoft/winget-pkgs: The Microsoft community Windows Package Manager manifest repository](https://github.com/microsoft/winget-pkgs)
14.
15. [How to Use Windows Package Manager - Petri](https://petri.com/how-to-use-windows-package-manager)
16.
17.
18.