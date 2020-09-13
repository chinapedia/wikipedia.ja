> この記事は[GUIDパーティションテーブル](https://ja.wikipedia.org/wiki/GUIDパーティションテーブル)から翻訳されています。


**GUIDパーティションテーブル** (*[GUID](../Page/GUID.md "wikilink") Partition Table*, **GPT**) は、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")上の[パーティションテーブル](https://ja.wikipedia.org/wiki/パーティションテーブル "wikilink")の配置に関する標準規格である。これは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の提案している[EFI標準の一部であり](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")、旧来の[BIOSで使用されている](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[マスターブートレコード](../Page/マスターブートレコード.md "wikilink") (MBR) の置き換えを意図している。従来のMBRパーティションが、テーブルのパラメータから、1セクタ512Byteで定義した場合、最大2[TiB迄の領域までしか管理できないのに対し](https://ja.wikipedia.org/wiki/テビバイト "wikilink")、GPTでは、最大8[ZiB迄の領域を定義](https://ja.wikipedia.org/wiki/ゼビバイト "wikilink")、管理できる。

2013年頃には、PC用として一般に市販のHDDの大容量化で、2T越えが始まっておりGPT導入は必至の課題であったが、マザーボード上のROM内などの[システムソフトウェア](../Page/システムソフトウェア.md "wikilink")のEFI対応もだいたい進んできていたことで、無事に導入が進んだという状況であった。

[300px](https://ja.wikipedia.org/wiki/ファイル:GUID_Partition_Table.png "wikilink")

## 機能

MBRがマスターブートコード（ブートローダ：起動できるアクティブ[パーティション](../Page/パーティション.md "wikilink")を探してプログラムをそこからロードして実行する機械語コードが入っている）で始まるのに対して、GPTはEFIが持つ拡張機能を使ってその処理を実現している。MBRのエントリがディスクの保護と互換性維持の目的で存在しているのに対して、GPTはパーティションテーブル・ヘッダーとしての役割を担っている。

GPTは[Logical Block Addressing](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink") (LBA) を使ってディスク内の位置を示す。MBRでは[CHSによって位置を指定していた](https://ja.wikipedia.org/wiki/Cylinder_head_sector "wikilink")。古いMBR情報は LBA 0 に含まれていて、GPTヘッダーは LBA 1 に置かれ、その後にパーティションテーブルが続く。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) では、16,384バイト（32セクター、16KiB）がGPT用に予約されていて、LBA 34 から通常の使い方ができるようになっている。

GPTは冗長性も提供している。GPTヘッダーとパーティションテーブルはディスクの先頭と最後部の両方に書き込まれている。

## 従来のMBR (LBA 0)

GPTを使用するディスクにもMBRが存在するのは、MBRを前提としたディスクユーティリティを利用した場合の事故の防止のため（誤って何も中身がないと判断されないため）である。MBRにはそのディスク全体がひとつのパーティションになっているという情報が記述されることになっている。GPT自体がBIOSによるMBRパーティションの代替であるため、そのパーティション識別子はシステムIDとして 0xEE が設定され、GPTを使用していることを示すことになっているが、双方のパーティションテーブルに有効な値を定義し、それをハイブリッドMBRと呼称する向きもある。但し、これはGPTの「MBRパーティションに対する置き換え」という目的から標準化、明示的な定義がされていない実装であり、OSによって扱いが異なる。ハイブリッドMBRの構成では多くの場合GUIDパーティションの方が優先されるが、Windowsをベースとするシステムでは、GPTをサポートするものであっても有効なMBRが存在する場合は、そちらを優先して解釈する。また、本来EFIとセットの実装であるが、MBRからGPTを理解するローダへ処理を移すという手段により、比較的最近の[Linux](../Page/Linux.md "wikilink")ではEFIが実装されていないシステムであっても、GPTからの起動や利用を可能としている\[1\]。

## パーティションテーブル・ヘッダー (LBA 1)

パーティションテーブル・ヘッダーでは、ユーザが使用可能なディスクの範囲を定義している。また、パーティションテーブル内のパーティションエントリ数とサイズを定義している。Windowsマシンでは、128エントリであり、それぞれ128バイトである。したがって、最大128個のパーティションを作成できる。

ヘッダーはディスクの[GUID](../Page/GUID.md "wikilink") (Globally Unique Identifier) を含んでいる。また、ヘッダー自身のサイズと位置（常に LBA 1）と、第二GPTヘッダーのサイズと位置（常にディスクの最後のセクター）を記録している。また重要な点として、自身のCRC32チェックサムを持っているので、専用のユーティリティ以外でGPTを変更するとチェックサムと不整合を起こす。チェックサムが不整合を起こすと、EFIは第二GPTを第一GPTにコピーする。第二GPTのチェックサムも不正だった場合はディスクにアクセスできなくなる。

## パーティションエントリ (LBA 2〜33)

パーティションエントリは単純である。最初の16バイトにパーティションの種類を表すGUIDが書き込まれている。たとえば、[EFIシステムパーティション](https://ja.wikipedia.org/wiki/EFIシステムパーティション "wikilink")のGUIDは {C12A7328-F81F-11D2-BA4B-00A0C93EC93B} である。ただし先頭3項目（8バイト）は項目内で[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")なので、実際には先頭から、28 73 2A C1 1F F8 D2 11 BA 4B 00 A0 C9 3E C9 3B のように書き込まれている。次の16バイトにはそのパーティション固有のGUIDが書き込まれている。続く8バイトにパーティションの最初のLBA、その次の8バイトにパーティションの最後のLBAが[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")で書き込まれている。さらにその後に、パーティション名と属性を書き込めるようになっている。

## OSのサポート

**表中の注釈**

  - "このバージョンではサポートされない"
    データ用としてもサポートされない。MBRにあるパーティションだけがOSからアクセス可能。
  - "リムーバブルディスクはMBRだけサポート"
    ユーザーからはGUIDパーティションにアクセス不可。[サードパーティー](../Page/サードパーティー.md "wikilink")製のツール経由でだけGUIDパーティションにアクセス可能。

### [UNIX](../Page/UNIX.md "wikilink") / [Unix系](../Page/Unix系.md "wikilink")

<table>
<thead>
<tr class="header">
<th><p>OS</p></th>
<th><p>バージョン</p></th>
<th><p>アーキテクチャ</p></th>
<th><p>BIOS経由でGPTからの起動</p></th>
<th><p>EFI経由でGPTからの起動</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
<td><p>7.0以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成ではGUID、MBRパーティションの両方が使われる。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
<td><p>ほとんどのx86 Linuxディストリビューション<br />
<a href="../Page/Fedora.md" title="wikilink">Fedora</a> 8以降、<a href="../Page/Ubuntu.md" title="wikilink">Ubuntu</a> 8.04以降[2]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x86-64</a>, <a href="../Page/IA-64.md" title="wikilink">IA-64</a>, <a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>fdisk等のツールはGPTを扱えない。gdisk[3]、<a href="../Page/GNU_GRUB.md" title="wikilink">GNU GRUB</a>、<a href="../Page/GNU_GRUB.md" title="wikilink">grub2などがGPTに対応</a>。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td><p>10.4.0以降<br />
（一部機能は10.4.6以降）[4]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Solaris.md" title="wikilink">Solaris</a></p></td>
<td><p>Solaris 10 1/06以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>Sparc版は非対応。x86/x64版は1/06 (update 2) よりGRUBが標準ブートローダーとなる。よってGPT対応もそれ以降。</p></td>
</tr>
</tbody>
</table>

### Windows（32ビット版）

古いバージョンの32ビット版（x86版）Windowsでは、2TiB以上の容量のディスク、およびGUIDパーティション自体を扱えないという問題がある。これは各ベンダーの32ビット版デバイスドライバーに起因する。

Vista以降では、32ビット版でもこれらの問題は修正されている。2TiB以上のパーティションを扱えないのはMBRパーティションの制限である。

下記の表にない、以前のOS（x86版）ではGPTはサポートされない。x86より以前のアーキテクチャでも同様。

<table>
<thead>
<tr class="header">
<th><p>OS</p></th>
<th><p>バージョン</p></th>
<th><p>アーキテクチャ</p></th>
<th><p>BIOS経由でGPTからの起動</p></th>
<th><p>EFI経由でGPTからの起動</p></th>
<th><p>GPTへのアクセス</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a></p></td>
<td><p>Service Pack 1以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista" title="wikilink">Windows Vista</a></p></td>
<td><p>RTM以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_Server_2008.md" title="wikilink">Windows Server 2008</a></p></td>
<td><p>RTM以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Microsoft_Windows_7.md" title="wikilink">Windows 7</a></p></td>
<td><p>RTM以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[5]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8" title="wikilink">Windows 8</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[6]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1" title="wikilink">Windows 8.1</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[7]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10#Windows_10" title="wikilink">Windows 10</a></p></td>
<td><p>TH1 RTM以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[8]。</p></td>
</tr>
</tbody>
</table>

### Windows（64ビット版）

IA-64版とx86-64版を列挙している。下記の表にないOS（64ビット版）ではGPTはサポートされない。

IA-64アーキテクチャのOSでは当初から、[EFI](https://ja.wikipedia.org/wiki/EFI "wikilink")とGPTからの起動をサポートしている。

<table>
<thead>
<tr class="header">
<th><p>OS</p></th>
<th><p>バージョン</p></th>
<th><p>アーキテクチャ</p></th>
<th><p>BIOS経由でGPTからの起動</p></th>
<th><p>EFI経由でGPTからの起動</p></th>
<th><p>GPTへのアクセス</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a></p></td>
<td><p>64-bit Edition, RTM</p></td>
<td><p><a href="../Page/IA-64.md" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。リムーバブルディスクはMBRだけサポート。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a></p></td>
<td><p>64-bit Edition, Version 2003</p></td>
<td><p><a href="../Page/IA-64.md" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。リムーバブルディスクはMBRだけサポート。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="../Page/IA-64.md" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。起動ディスクはGPTが必須[9]。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a></p></td>
<td><p>x64, Service Pack 1</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a></p></td>
<td><p>x64 Edition</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。リムーバブルディスクはMBRだけサポート。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista" title="wikilink">Windows Vista</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista" title="wikilink">Windows Vista</a></p></td>
<td><p>Service Pack 1</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Microsoft_Windows_Server_2008.md" title="wikilink">Windows Server 2008</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a>, <a href="../Page/IA-64.md" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Microsoft_Windows_7.md" title="wikilink">Windows 7</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[10]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2" title="wikilink">Windows Server 2008 R2</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a>, <a href="../Page/IA-64.md" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8" title="wikilink">Windows 8</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[11]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1" title="wikilink">Windows 8.1</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[12]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012" title="wikilink">Windows Server 2012</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[13]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012#Windows_Server_2012_R2" title="wikilink">Windows Server 2012 R2</a></p></td>
<td><p>RTM</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[14]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10#Windows_10" title="wikilink">Windows 10</a></p></td>
<td><p>TH1 RTM以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>ハイブリッドMBRの構成でMBRパーティションの方が優先される[15]。</p></td>
</tr>
</tbody>
</table>

## パーティションの型を表すGUID

<table>
<thead>
<tr class="header">
<th><p>対応OS</p></th>
<th><p>パーティション・タイプ</p></th>
<th><p>Globally-Unique Identifier (GUID)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>(None)</em></p></td>
<td><p>未使用エントリ</p></td>
<td><p><code>00000000-0000-0000-0000-000000000000</code></p></td>
</tr>
<tr class="even">
<td><p>MBRパーティション形式</p></td>
<td><p><code>024DEE41-33E7-11D3-9D69-0008C781F39F</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/EFIシステムパーティション" title="wikilink">EFIシステムパーティション</a></p></td>
<td><p><code>C12A7328-F81F-11D2-BA4B-00A0C93EC93B</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>bios_grub[16]</p></td>
<td><p><code>21686148-6449-6E6F-744E-656564454649</code> |-</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Windows</a></p></td>
</tr>
<tr class="odd">
<td><p>データパーティション（FATまたはNTFS）</p></td>
<td><p><code>EBD0A0A2-B9E5-4433-87C0-68B6B72699C7</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ダイナミックボリューム (LDM) メタデータ・パーティション</p></td>
<td><p><code>5808C8AA-7E8F-42E0-85D2-E1E90434CFB3</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ダイナミックボリューム (LDM) データ・パーティション</p></td>
<td><p><code>AF9B60A0-1431-4F62-BC68-3311714A69AD</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/HP-UX.md" title="wikilink">HP-UX</a></p></td>
<td><p>データパーティション</p></td>
<td><p><code>75894C1E-3AEB-11D3-B7C1-7B03A0000000</code></p></td>
</tr>
<tr class="odd">
<td><p>サービスパーティション</p></td>
<td><p><code>E2A1E728-32E3-11D6-A682-7B03A0000000</code> |-</p></td>
<td><p><a href="../Page/Linux.md" title="wikilink">Linux</a></p></td>
</tr>
<tr class="even">
<td><p>RAIDパーティション</p></td>
<td><p><code>A19D880F-05FC-4D3B-A006-743F0F84911E</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>スワップパーティション</p></td>
<td><p><code>0657FD6D-A4AB-43C4-84E5-0933C84B4F4F</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>LVMパーティション</p></td>
<td><p><code>E6D6D379-F507-44C2-A23C-238F2A3DF928</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>予約済み</p></td>
<td><p><code>8DA63339-0007-60C0-C436-083AC8230908</code> |-</p></td>
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
</tr>
<tr class="even">
<td><p>スワップパーティション</p></td>
<td><p><code>516E7CB5-6ECF-11D6-8FF8-00022D09712B</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Unix_File_System.md" title="wikilink">UFSパーティション</a></p></td>
<td><p><code>516E7CB6-6ECF-11D6-8FF8-00022D09712B</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Vinum Volume Managerパーティション</p></td>
<td><p><code>516E7CB8-6ECF-11D6-8FF8-00022D09712B</code> |-</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a><br />
<a href="../Page/Darwin_(オペレーティングシステム).md" title="wikilink">Darwin</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/アップル_(企業).md" title="wikilink">Apple</a> <a href="../Page/Unix_File_System.md" title="wikilink">UFS</a> 容器</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/APFS" title="wikilink">APFS</a> 容器、<br />
APFS 用 <a href="../Page/FileVault.md" title="wikilink">FileVault</a> パーティションの容器</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/ZFS.md" title="wikilink">ZFS</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Apple RAID パーティション</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple RAID 、オフライン</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Apple ブートパーティション (回復モード)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple ラベル</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Apple TV リカバリパーティション</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple Core Storage 容器、<br />
HFS+ 用 FileVault パーティションの容器</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SoftRAID_Status</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SoftRAID_Scratch</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SoftRAID_Volume</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SoftRAID_Cache</p></td>
<td><p>|-</p></td>
<td><p><a href="../Page/Solaris.md" title="wikilink">Solaris</a></p></td>
</tr>
<tr class="even">
<td><p>Rootパーティション</p></td>
<td><p><code>6A85CF4D-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>スワップパーティション</p></td>
<td><p><code>6A87C46F-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>バックアップパーティション</p></td>
<td><p><code>6A8B642B-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>/usrパーティション</p></td>
<td><p><code>6A898CC3-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>/varパーティション</p></td>
<td><p><code>6A8EF2E9-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>/homeパーティション</p></td>
<td><p><code>6A90BA39-1DD2-11B2-99A6-080020736631</code> |-</p></td>
<td><p>EFI_ALTSCTR</p></td>
</tr>
<tr class="even">
<td><p>予約済みパーティション</p></td>
<td><p><code>6A945A3B-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><code>6A9630D1-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><code>6A980767-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><code>6A96237F-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><code>6A8D2AC7-1DD2-11B2-99A6-080020736631</code></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<small>注意：LinuxとWindowsはデータパーティションを表すGUIDとして同じIDを使用している。</small>

<small>注意:この表にあるGUIDは[リトルエンディアンで表記されている](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。例えば、EFIシステムパーティションのGUIDは C12A7328-F81F-11D2-BA4B-00A0C93EC93B となっているが、これは次のような16バイトの並びである: 28 73 2A C1 1F F8 D2 11 BA 4B 00 A0 C9 3E C9 3B。先頭3ブロックだけバイト順序が入れ替わっている点に注意。</small>

## 脚注

### 注釈

### 出典

<references/>

## 関連項目

  - [マスターブートレコード](../Page/マスターブートレコード.md "wikilink") (MBR)
  - [GUID](../Page/GUID.md "wikilink")
  - [Unified Extensible Firmware Interface](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")

## 外部リンク

  - [GUID パーティション テーブル](http://technet.microsoft.com/ja-jp/library/cc773223.aspx) [マイクロソフト](../Page/マイクロソフト.md "wikilink")社のWebサイトにある説明

[Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:BIOS](https://ja.wikipedia.org/wiki/Category:BIOS "wikilink")

1.  <http://www.gnu.org/software/grub/manual/html_node/BIOS-installation.html>
2.  <https://help.ubuntu.com/community/MacBook>
3.  <http://www.rodsbooks.com/gdisk>
4.  <http://refit.sourceforge.net/myths/>
5.  <http://www.rodsbooks.com/gdisk/hybrid.html>
6.  <http://www.rodsbooks.com/gdisk/hybrid.html>
7.  <http://www.rodsbooks.com/gdisk/hybrid.html>
8.  <http://www.rodsbooks.com/gdisk/hybrid.html>
9.  <http://codeidol.com/windows/inside-windows-server-2003/Configuring-Data-Storage/Working-with-GPT-Disks/> Working with GPT Disks
10. <http://www.rodsbooks.com/gdisk/hybrid.html>
11. <http://www.rodsbooks.com/gdisk/hybrid.html>
12. <http://www.rodsbooks.com/gdisk/hybrid.html>
13. <http://www.rodsbooks.com/gdisk/hybrid.html>
14. <http://www.rodsbooks.com/gdisk/hybrid.html>
15. <http://www.rodsbooks.com/gdisk/hybrid.html>
16. <http://grub.enbug.org/BIOS_Boot_Partition>