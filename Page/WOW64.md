> この記事は[WOW64](https://ja.wikipedia.org/wiki/WOW64)から翻訳されています。


**WOW64**（ワウ64、**W**indows 32-bit **O**n **W**indows **64**-bit）とは、[64ビット](../Page/64ビット.md "wikilink") ([x64](https://ja.wikipedia.org/wiki/x64 "wikilink")および[IA-64](../Page/IA-64.md "wikilink")) 版の[Microsoft Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Win32アプリケーションを実行する](../Page/Windows_API.md "wikilink")、[エミュレーション](https://ja.wikipedia.org/wiki/エミュレーション "wikilink")レイヤー・サブシステムである。

## 概要

64ビット版のWindowsは基本的に、完全に64ビット化された[NTカーネルで動作する](../Page/Windows_NT系.md "wikilink")。[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")や[IA-64](../Page/IA-64.md "wikilink")対応のオペレーティングシステムでは、x86の32ビット[ABIに対応するかどうかの選択を迫られることとなった](../Page/Application_Binary_Interface.md "wikilink")。64ビットのWindowsでは、64ビットABIと32ビットABIの両方に対応し、Win32APIをWin64APIに呼び変えるエミュレーション層が実装されている。これがWOW64である。これにより、32ビットアプリケーションはそのまま64ビットのWindowsでも動作する。

## 構造

WOW64は、WOW64ホストプロセスによって予約された4GBの仮想空間に32ビットABIのコードを読み込み、そこで発生したWin64 APIに変換可能なAPI呼び出しを変換して、Win64サブシステムに伝達する。構造体の変換は自動的に行われ、Win32側では現在動作しているOSが32ビットシステムか、64ビットシステムかを意識する必要は全くない。またユーザーモードで動作するコンポーネント群は32ビット版と64ビット版が用意され、例えばOLEなどは32ビットで閉じた範囲で動作できる。64ビット版で提供されるコードは単一のソースから、32ビット版と64ビット版両方をそれぞれコンパイルして作られているため、機能的には32ビットシステムと64ビットシステムの間に差異は無い。

## 問題点

Windowsの64ビットABIは、Win32の32ビットABIをそのまま64ビットに拡張したものである。従って、64ビットABIのアプリケーションは8[TBのアドレス空間を独占的に使えるようになっているが](../Page/テラバイト.md "wikilink")、ここに一つの問題点がある。32ビットABIのコードを格納可能な仮想空間下位4GBをも64ビットABIに独占されてしまったことである。このため、32ビットABIを格納する場所が無く、32ビットアプリケーションはもとより、[DLLや](../Page/ダイナミックリンクライブラリ.md "wikilink")[OCXをロードして呼び出すことも不可能となってしまった](../Page/Component_Object_Model.md "wikilink")。そのため、マイクロソフトは、32ビットABIのコードと64ビットABIのコードとの相互な呼び出しを禁止している（COMインターフェースを経由すれば相互乗り入れは可能であるが、x64アーキテクチャで本来可能であった32ビットコードと64ビットコードのシームレスな相互呼び出し機能は全く生かされていない）。この顕著な例として、[Internet Explorerの振舞があげられる](../Page/Internet_Explorer.md "wikilink")。32ビットのActiveXコンポーネントを検出すると、64ビット版Internet Explorerは処理を中断して32ビット版Internet Explorerに処理を引き継ぐ。32ビットアプリケーションと64ビットアプリケーションの間には、実行ファイル以外のコンポーネント群を互いに利用することができない深い溝がある。

## プログラミング

16ビット時代から32ビットへの過渡期に用意された[サンク](https://ja.wikipedia.org/wiki/サンク "wikilink")(**thunk**)メカニズムはWOW64では提供されず、32ビットコードと64ビットコードは1つのプロセスに共存できない。32ビットのプロセスと64ビットのプロセスとの通信は、アウトプロセスCOMをはじめとして、各種のプロセス間通信が使用可能である\[1\]。

2010年現在、Windowsアプリケーションやミドルウエアの殆どはx64には移行していない。よってこれらのソフトウエア資源を継承しつつ、x64に対応したアプリケーションを開発するには、WOW64の機能を使って32ビットソフトウエア資源へのアクセスを確保し、64ビットアプリケーションに対してCOMインターフェースの形で提供することで、異なるABIが混在する過渡期を乗り越えることができる。またCOMインターフェースの形をとることにより、[.NET Frameworkへのアクセスも用意できる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

## システムフォルダとレジストリ

2010年現在の64Bit Windowsでは、Windows システムフォルダ([%systemroot%](../Page/環境変数.md "wikilink")\\System32)には64ビットのバイナリが置かれ、32ビットプログラムはその中にあるファイルには直接アクセスすることができない。32ビットプログラムによるSystem32フォルダへのアクセスは、自動的に%systemroot%\\SysWOW64へとリダイレクトされる動作となり、プログラムからはSystem32フォルダにアクセスしているように見える。SysWOW64フォルダには32ビットのバイナリが用意されている。

[Windows レジストリへ](../Page/レジストリ.md "wikilink")32ビットアプリケーションがアクセスする場合は、一部リダイレクトされる。HKLM\\SOFTWAREとHKCR\\下のレジストリキーへのアクセスは、それぞれWow6432Nodeと呼ばれるキーの配下にアクセスしている。

## 脚注

## 外部リンク

  - [32bitアプリを64bitWindows7で動かす「WOW64」](http://ascii.jp/elem/000/000/480/480200/) - [ASCII.jp](https://ja.wikipedia.org/wiki/ASCII.jp "wikilink")
  - [Running 32-bit Applications - Platform SDK: 64-bit Windows Programming](http://msdn.microsoft.com/en-us/library/aa384249.aspx) - MSDN Library
  - [Best Practices for WOW64](https://download.microsoft.com/download/a/f/7/af7777e5-7dcd-4800-8a0a-b18336565f5b/wow64_bestprac.docx)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink")

1.