> この記事は[ReactOS](https://ja.wikipedia.org/wiki/ReactOS)から翻訳されています。


**ReactOS**（リアクト オーエス）は、[Microsoft Windows NT系](../Page/Windows_NT系.md "wikilink")（[2000以降](../Page/Microsoft_Windows_2000.md "wikilink")）と[アプリケーション及び](../Page/アプリケーションソフトウェア.md "wikilink")[ドライバに於ける](../Page/デバイスドライバ.md "wikilink")[バイナリ互換性を目指す](../Page/Application_Binary_Interface.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である\[1\]。

## 特徴

ReactOSは、主に[C言語](../Page/C言語.md "wikilink")で実装されているが、「ReactOS Explorer」のように幾つかの要素は[C++](../Page/C++.md "wikilink")によって記述されている。[ARMと](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")に移植が進んでおり、一部の[Windows APIは実装済みである](https://ja.wikipedia.org/wiki/Windows_API "wikilink")。 [Wine](../Page/Wine.md "wikilink")プロジェクトと提携し、互換レイヤーに関してはWineに依存\[2\]しているが、そのほかの機能は開発チームが独自に実装している。 しかしながら、[開発者の不足により](https://ja.wikipedia.org/wiki/ソフトウェア開発者 "wikilink")[開発は遅れぎみである](../Page/ソフトウェア開発.md "wikilink")。

開発では、法的脅威と[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")に関する不安に対処するために大規模なソースコード監査が実施\[3\]されている。

## 語源

「React」という単語は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の独占状態に対する開発チームの不満を意味している\[4\]。

## 歴史

[thumb](https://ja.wikipedia.org/wiki/ファイル:ReactOS_0.3.1_-_Device_Manager.png "wikilink")

### 開発初期

[1996年](../Page/1996年.md "wikilink")頃、オープンソース開発者のグループが**FreeWin95**というプロジェクトを開始した。このプロジェクトの目標は[Windows 95の](../Page/Microsoft_Windows_95.md "wikilink")[クローン](https://ja.wikipedia.org/wiki/クローン "wikilink")となるOSを実装することであった。しかしプロジェクトはシステムの設計に関する議論で行き詰まり、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")の終わりになっても、何の成果も出せずにいた。

プロジェクトのメンバーはプロジェクトの復活を呼びかけ、クローンの対象をWindows NTへと変更し、名称を**ReactOS**に改名した。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")、[カーネル](../Page/カーネル.md "wikilink")と基本的なドライバの開発を開始しReactOSプロジェクトが発足した。\[5\]

### コードの流用疑惑

[2006年](../Page/2006年.md "wikilink")[1月17日](https://ja.wikipedia.org/wiki/1月17日 "wikilink")、ReactOSの開発者向け[メーリングリスト](../Page/メーリングリスト.md "wikilink")に一人の開発者から「ReactOSにはWindowsを逆アセンブルしたコードが含まれている」との投稿があった\[6\]。

また、全開発者に「クリーンルーム方式のリバースエンジニアリングのみを行う。」よう契約書にサインをさせた\[7\]。

[2006年](../Page/2006年.md "wikilink")[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink")、まだ完全に監査は完了していなかったものの、活動再開の発表がなされた。コードの調査を完了させ、ソースコードの影響する部分を書き直すには何年もかかるため、この件によってプロジェクトの進行が遅れるものと考えられていたが、2008年8月末までにコードの監査は完了した\[8\]。なお、開発と監査は同時に進行していた。このコード監査は、新たにリポジトリを作成し、監査が終了したら、コードを元の場所から新リポジトリへと移動する、という手順で行われた。

## 機能

[thumb](https://ja.wikipedia.org/wiki/ファイル:ReactOS_0.3_-_1.jpg "wikilink")

2011年現在、[GUIが用意され](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、基本的な操作が可能になっている。主な[APIや](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[ABIが用意され](../Page/Application_Binary_Interface.md "wikilink")、幾つかのアプリケーションの動作が報告\[9\]されている。また、[カーネル](../Page/カーネル.md "wikilink")は概ね安定している。

## 開発の現状と今後

現在、ReactOSの開発者はUSBをサポートする作業も行っている。また、GUIシステムの改良や[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")、[マルチメディア](../Page/マルチメディア.md "wikilink")、[プラグアンドプレイ](../Page/プラグアンドプレイ.md "wikilink")ハードウェアに対応する作業も行われている。いくつかのアプリケーションは動作が保証されないものの、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や、[Monoを利用した](../Page/Mono_\(ソフトウェア\).md "wikilink")[.NETはサポートされている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")\[10\]\[11\]。マルチユーザー環境が開発されれば、ターミナル・サービスやリモート・デスクトップの開発も行われることとなる。この開発には[XRDP](https://ja.wikipedia.org/wiki/XRDP "wikilink")、 [VNC](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink")、 [rdesktop](https://ja.wikipedia.org/wiki/rdesktop "wikilink")が用いられることとなるだろう。Windows NTサブシステムと同様に、[DOS](../Page/MS-DOS.md "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[POSIX](../Page/POSIX.md "wikilink")サブシステムも提供されている\[12\]。

開発者はWindows NT バージョン5、6とより互換性を持つカーネルを開発し、より多くのアプリケーションをサポートすることを目標としている。また、改良されたUSB、ネットワーク、その他のハードウェアのサポートも利用可能となる可能性がある。

また、3Dゲームのサポートの強化および、完全な[OpenGL](../Page/OpenGL.md "wikilink")サポートのための作業も行われている。ReactOSプロジェクトのオープンソース版[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")ともいえる、ReactXの開発にも進歩の動きがみられる\[13\]。

ReactOS プロジェクトは、2ヶ月から6ヶ月の間隔で新しいバージョンをリリースすることを目標としており、バージョン0.5.0からはベータ版となり、実用的なシステムとなる計画である。\[14\]

0.4.8以降[NTFS](https://ja.wikipedia.org/wiki/NTFS "wikilink")の実装が始まっている。

### アーキテクチャのサポート

現在、ReactOSの開発者はReactOSの多数の[移植に取り組んでいる](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink"):

  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")
  - [Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink") \[15\]
  - [ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink") \[16\]
  - [AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink") \[17\]

ReactOSは[Hyper-V](../Page/Hyper-V.md "wikilink")\[18\]、[VMware](../Page/VMware.md "wikilink")、[VirtualBox](../Page/VirtualBox.md "wikilink")、[QEMU](../Page/QEMU.md "wikilink")のような上記のハードウェアを[エミュレートもしくは](../Page/エミュレータ.md "wikilink")[仮想化するソフトウェア上でも動作することが知られている](../Page/仮想機械.md "wikilink")\[19\]。

ReactOSでも、移植性を見据えた処置が取られている。例えば、0.2.5においてはさまざまなIA-32アーキテクチャや[Xboxプラットフォームへの対応が追加された](../Page/Xbox_\(ゲーム機\).md "wikilink")。また、2005年の段階で、ReactOSをPowerPCやXenアーキテクチャへと移植する作業も進行中である。

## 関連するプロジェクト

[Wine_on_ReactOS.svg](https://ja.wikipedia.org/wiki/File:Wine_on_ReactOS.svg "fig:Wine_on_ReactOS.svg") ReactOSは[Wine](../Page/Wine.md "wikilink")プロジェクトと協力して活動しており\[20\]、よってWineが行っているWin32 APIの実装を活用することができる。依存しているレイヤーは、主にWineの[DLLに関連しており](../Page/ダイナミックリンクライブラリ.md "wikilink")、それらの多くはReactOSとWineで共通している\[21\]。双方のプロジェクトは互いの互換性の問題に取り組んでいる。

もう一つの関連するプロジェクトは[Samba TNGである](https://ja.wikipedia.org/wiki/Samba_TNG "wikilink")。Samba TNGはLSASS, SAM, NETLOGON, SPOOLSSといった多数のサービスを実装している。Samba TNGはモジュール化されているため、各サービスは容易にReactOSへと取り込むことができる\[22\]。

## 国際化と地域化

ReactOSはバージョン0.2.2より、[UTF-16](../Page/UTF-16.md "wikilink")を適切に扱うことができるように改良された。 これにより、[文字コード](../Page/文字コード.md "wikilink")として[UTF-16](../Page/UTF-16.md "wikilink")を用いたアプリケーションを動作させることが可能となった。 また、[ハードコード](https://ja.wikipedia.org/wiki/ハードコード "wikilink")されたメッセージを[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")ファイルへと移す作業も行われ、OSに組み込まれているアプリケーションの多くは国際化されたメッセージを表示することができるようになっている。 0.2.7リリース以後に大半のリソースファイルにおいて翻訳の活動が行われた。\[23\]

### 日本語対応

[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")に[日本語](../Page/日本語.md "wikilink")が指定されている場合には、メッセージは日本語で表示される。しかし、新機能の追加などにより、英語で表示される部分もまた増えてきている。

バージョン0.3.10からは、「Systema Font」という日本語フォントが追加されたため、インストール時に日本語を選択すれば、日本語が表示できるようになった。 また、バージョン0.3.11からは、「Systema Font」から「[Droid Sans Fallback](https://ja.wikipedia.org/wiki/Droid_\(書体\) "wikilink")」にフォントが変更され、中国語・韓国語の表示も可能になった。

## 脚注

## 関連項目

  - [Freedows OS](https://ja.wikipedia.org/wiki/Freedows_OS "wikilink"), [Alliance OS](https://ja.wikipedia.org/wiki/Alliance_OS "wikilink") - かつて存在したWindowsクローンの試み
  - [WinFrame](https://ja.wikipedia.org/wiki/WinFrame "wikilink") - Citrix社が開発していたWindowsクローン
  - [Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")
  - [Linspire](../Page/Linspire.md "wikilink")
  - [Wine](../Page/Wine.md "wikilink")
  - [エミュレーション](../Page/エミュレータ.md "wikilink")

## 外部リンク

  -
  - [ReactOS Wiki](http://www.reactos.org/wiki/) - 公式Wiki

  - [SourceForge.net](../Page/SourceForge.net.md "wikilink") の [ReactOS プロジェクトのページ](http://sourceforge.net/projects/reactos/)

[Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink")

1.  [“Vistaっぽい見た目”を実現したWindows互換OS「ReactOS 0.4.6」 - PC Watch](https://pc.watch.impress.co.jp/docs/news/1079887.html)、2018年9月25日閲覧。
2.
3.
4.
5.
6.
7.
8.  [1](http://www.reactos.org/generated/locked_files.log)
9.
10.
11.
12.
13.
14. [ReactOSロードマップ](http://www.reactos.org/wiki/index.php/Roadmap)
15.
16.
17.
18.
19.
20.
21.
22.
23.