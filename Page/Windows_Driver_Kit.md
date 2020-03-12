> この記事は[Windows Driver Kit](https://ja.wikipedia.org/wiki/Windows_Driver_Kit)から翻訳されています。


[Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink"){{-}}[Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink"){{-}}[Windows 7](../Page/Microsoft_Windows_7.md "wikilink"){{-}}[Windows Server 2016](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2016 "wikilink") TP{{-}}[Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink") | 種別 = [ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") | ライセンス = | 公式サイト = [Windows Hardware Dev Center - Windows 10 Hardware Dev Center](https://msdn.microsoft.com/en-us/windows/hardware/) }}

**Windows Driver Kit** (WDK) は[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") OS用[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")を作成するための[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")である。

バージョン7.1までのWDKはドキュメント、サンプル、ビルド環境、ツールなどを含んでいた。

WDKは[Windows Vistaよりも前までは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、Microsoft Driver Development Kit (DDK) と呼ばれていた。 WDKはDDKのほぼ全てのものを含み、加えて、Installable File System Kit と Display Compatibility Kit を含むようになった。

## ハードウェアのテストと測定

[Windows XP](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")/[Windows Server 2003までは](https://ja.wikipedia.org/wiki/Windows_Server_2003 "wikilink")、ハードウェアおよび開発したデバイスドライバーのテストと測定を行なうツールとして、「ハードウェア互換性テストキット」(Hardware Compatibility Test Kit, HCT) が提供されていた。

[Windows Vistaにおいて](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、HCTはDriver Test Manager (DTM) に置き換えられた。DTMはテスト自動化のフレームワーク（自動テストエンジン）を含む\[1\]。この時点では、DTMはWDKに含まれていた。

その後、DTMはWDKと分離され、Windows Logo Kit (WLK) に置き換えられた。

さらに、WLKは「Windowsハードウェア認定キット」(Windows Hardware Certification Kit, HCK) に置き換えられた\[2\]。

[Windows 10用には](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")、HCKの後継として「Windowsハードウェアラボキット」(Windows Hardware Lab Kit, HLK) が提供されている\[3\] \[4\]。

## 脚注

## 関連項目

  - [Windows Driver Model](../Page/Windows_Driver_Model.md "wikilink")
  - [Windows Display Driver Model](https://ja.wikipedia.org/wiki/Windows_Display_Driver_Model "wikilink")
  - [Windows Driver Foundation](../Page/Windows_Driver_Foundation.md "wikilink")
  - [Windows Kernel-Mode Driver Framework](https://ja.wikipedia.org/wiki/Windows_Kernel-Mode_Driver_Framework "wikilink")
  - [Windows User-Mode Driver Framework](https://ja.wikipedia.org/wiki/Windows_User-Mode_Driver_Framework "wikilink")

## 外部リンク

  - [Windows Hardware Dev Center - Windows 10 Hardware Dev Center](https://msdn.microsoft.com/en-us/windows/hardware/)
  - [WDK, HLK, ADK downloads - Windows 10 Hardware Dev Center](https://msdn.microsoft.com/en-us/windows/hardware/dn913721.aspx)
  - [Windows ハードウェア デベロッパー センター - Windows 10 ハードウェア デベロッパー センター](https://msdn.microsoft.com/ja-jp/windows/hardware)
  - [WDK、HLK、ADK のダウンロード - Windows 10 ハードウェア デベロッパー センター](https://msdn.microsoft.com/ja-jp/windows/hardware/dn913721.aspx)
  - [Windows Driver Kit](http://www.microsoft.com/japan/whdc/DevTools/WDK/default.mspx)
  - [Windows Driver Development Kit](http://www.microsoft.com/japan/whdc/DevTools/ddk/default.mspx)

[Category:マイクロソフトの開発ツール](https://ja.wikipedia.org/wiki/Category:マイクロソフトの開発ツール "wikilink") [Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink")

1.  [Introduction to Driver Test Manager | Windows Hardware Certification](http://windowshardwarecertification.blogspot.jp/2012/09/introduction-to-driver-test-manager.html)
2.  [Windows 7 Logo Program - Windows 8.1 HCK](https://msdn.microsoft.com/en-us/library/windows/hardware/dn641155.aspx)
3.  [Windows Hardware Certification Kit Downloads - Windows Hardware Dev Center](https://msdn.microsoft.com/en-us/library/windows/hardware/hh833788.aspx)
4.  [Windows ハードウェア認定キットのダウンロード - Windows ハードウェア デベロッパー センター](https://msdn.microsoft.com/ja-jp/library/windows/hardware/hh833788.aspx)