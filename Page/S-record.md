> この記事は[S-record](https://ja.wikipedia.org/wiki/S-record)から翻訳されています。


**Motorola S-record**は、[モトローラ](../Page/モトローラ.md "wikilink")によって作成されたファイル形式であり、バイナリ情報を[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") [16進テキスト形式で伝達する](../Page/十六進法.md "wikilink")。このファイル形式は**SRECORD**、**SREC**、**S19**、**S28**、**S37**とも呼ばれる。マイクロコントローラ、[EPROM](../Page/EPROM.md "wikilink")、[EEPROM](../Page/EEPROM.md "wikilink")、およびその他の種類のプログラマブルロジックデバイスの[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")のプログラミングによく使用される。典型的な適用では、コンパイラやアセンブラはプログラムのソースコード（[C言語](../Page/C言語.md "wikilink")や[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")など）を[機械語](../Page/機械語.md "wikilink")コードに変換し、16進ファイルに出力する。16進ファイルは、プログラマーによってインポートされ、機械語コードを[不揮発性メモリ](../Page/不揮発性メモリ.md "wikilink")に書き込むか、ロードおよび実行のために対象システムに転送される。

## 概要

The S-record format was created in the mid-1970s for the [Motorola 6800](../Page/MC6800.md "wikilink") processor. [Software development tools](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink") for that and other [embedded processors](../Page/組み込みシステム.md "wikilink") would make executable code and data in the S-record format. PROM programmers would then read the S-record format and "burn" the data into the PROMs or EPROMs used in the embedded system.

### その他の16進形式

There are other ASCII encoding with a similar purpose. BPNF, BHLF, and B10F were early binary formats, but they are neither compact nor flexible. Hexadecimal formats are more compact because they represent 4 bits rather than 1 bit per character. Many, such as S-record, are more flexible because they include address information so they can specify just a portion of a PROM. [Intel HEX](https://ja.wikipedia.org/wiki/Intel_HEX "wikilink") format was often used with Intel processors. Tek Hex is another hex format that can include a symbol table for debugging.

## フォーマット

### レコード構造

|   |      |            |         |      |          |
| - | ---- | ---------- | ------- | ---- | -------- |
| S | Type | Byte Count | Address | Data | Checksum |

An SREC format file consists of a series of ASCII text records. The records have the following structure from left to right:

1.  **Record type**, two characters, an uppercase "S" (0x53) then a numeric digit *0* to *9*, defining the type of record.
2.  **Byte count**, two hex digits, indicating the number of bytes (hex digit pairs) that follow in the rest of the record (address + data + checksum). This field has a minimum value of 3 for 16-bit address field plus 1 checksum byte, and a maximum value of 255 (0xFF).
3.  **Address**, four / six / eight hex digits as determined by the record type. The address bytes are arranged in [big endian](https://ja.wikipedia.org/wiki/エンディアン "wikilink") format.
4.  **Data**, a sequence of 2*n* hex digits, for *n* bytes of the data. For S1/S2/S3 records, a maximum of 32 bytes per record is typical since it will fit on an 80 character wide terminal screen, though 16 bytes would be easier to visually decode each byte at a specific address.
5.  **Checksum**, two hex digits, the [least significant byte](../Page/最下位ビット.md "wikilink") of  of the sum of the values represented by the two hex digit pairs for the byte count, address and data fields. See example section for a detailed checksum example.

### テキスト行終端記号

SREC records are separated by one or more ASCII line termination characters so that each record appears alone on a text line. This enhances legibility by visually [delimiting](https://ja.wikipedia.org/wiki/区切り文字 "wikilink") the records and it also provides padding between records that can be used to improve machine [parsing](../Page/構文解析.md "wikilink") efficiency.

Programs that create HEX records typically use line termination characters that conform to the conventions of their [operating systems](../Page/オペレーティングシステム.md "wikilink"). For example, Linux programs use a single LF ([line feed](../Page/改行コード.md "wikilink"), hex value `0A`) character to terminate lines, whereas Windows programs use a CR ([carriage return](https://ja.wikipedia.org/wiki/キャリッジ・リターン "wikilink"), hex value `0D`) followed by a LF.

### レコードタイプ

The following table describes 10 possible S-records. S4 is reserved and not currently defined. S6 was originally reserved but was later redefined.

<table>
<thead>
<tr class="header">
<th><p>Record<br />
Field</p></th>
<th><p>Record<br />
Purpose</p></th>
<th><p>Address<br />
Field</p></th>
<th><p>Data<br />
Field</p></th>
<th><p>Record<br />
Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>S0</strong></p></td>
<td><p>Header</p></td>
<td><p>16-bit<br />
"0000"</p></td>
<td></td>
<td><p>This record contains vendor specific ASCII text represented as a series of hex digit pairs. It is common to see the data for this record in the format of a <a href="https://ja.wikipedia.org/wiki/ヌル終端文字列" title="wikilink">null-terminated string</a>. The text data can be anything including a mixture of the following information: file/module name, version/revision number, date/time, product name, vendor name, memory designator on PCB, copyright notice. It is common to see: 48 44 52 which is the ASCII H, D, and R - "HDR".[1]</p></td>
</tr>
<tr class="even">
<td><p><strong>S1</strong></p></td>
<td><p>Data</p></td>
<td><p>16-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains data that starts at the 16-bit address field.[2] This record is typically used for 8-bit microcontrollers, such as AVR, PIC, 8051, 68xx, 6502, 80xx, Z80. The number of bytes of data contained in this record is "Byte Count Field" minus 3 (that is, 2 bytes for "16-bit Address Field" and 1 byte for "Checksum Field").</p></td>
</tr>
<tr class="odd">
<td><p><strong>S2</strong></p></td>
<td><p>Data</p></td>
<td><p>24-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains data that starts at a 24-bit address.[3] The number of bytes of data contained in this record is "Byte Count Field" minus 4 (that is, 3 bytes for "24-bit Address Field" and 1 byte for "Checksum Field").</p></td>
</tr>
<tr class="even">
<td><p><strong>S3</strong></p></td>
<td><p>Data</p></td>
<td><p>32-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains data that starts at a 32-bit address.[4] This record is typically used for 32-bit microcontrollers, such as ARM and 680x0. The number of bytes of data contained in this record is "Byte Count Field" minus 5 (that is, 4 bytes for "32-bit Address Field" and 1 byte for "Checksum Field").</p></td>
</tr>
<tr class="odd">
<td><p><strong>S4</strong></p></td>
<td><p>Reserved</p></td>
<td></td>
<td></td>
<td><p>This record is reserved.</p></td>
</tr>
<tr class="even">
<td><p><strong>S5</strong></p></td>
<td><p>Count</p></td>
<td><p>16-bit<br />
Count</p></td>
<td></td>
<td><p>This optional record contains a 16-bit count of <strong>S1</strong> / <strong>S2</strong> / <strong>S3</strong> records.[5] This record is used if the record count is less than or equal to 65,535 (0xFFFF), otherwise <strong>S6</strong> record would be used.</p></td>
</tr>
<tr class="odd">
<td><p><strong>S6</strong></p></td>
<td><p>Count</p></td>
<td><p>24-bit<br />
Count</p></td>
<td></td>
<td><p>This optional record contains a 24-bit count of <strong>S1</strong> / <strong>S2</strong> / <strong>S3</strong> records. This record is used if the record count is less than or equal to 16,777,215 (0xFFFFFF). If less than 65,536 (0x010000), then <strong>S5</strong> record would be used. <strong>NOTE:</strong> This newer record is the most recent change (it may not be official).[6]</p></td>
</tr>
<tr class="even">
<td><p><strong>S7</strong></p></td>
<td><p>Start Address<br />
(Termination)</p></td>
<td><p>32-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains the starting execution location at a 32-bit address.[7][8] This is used to terminate a series of <strong>S3</strong> records. If a SREC file is only used to program a memory device and the execution location is ignored, then an address of zero could be used.</p></td>
</tr>
<tr class="odd">
<td><p><strong>S8</strong></p></td>
<td><p>Start Address<br />
(Termination)</p></td>
<td><p>24-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains the starting execution location at a 24-bit address.[9][10] This is used to terminate a series of <strong>S2</strong> records. If a SREC file is only used to program a memory device and the execution location is ignored, then an address of zero could be used.</p></td>
</tr>
<tr class="even">
<td><p><strong>S9</strong></p></td>
<td><p>Start Address<br />
(Termination)</p></td>
<td><p>16-bit<br />
Address</p></td>
<td></td>
<td><p>This record contains the starting execution location at a 16-bit address.[11][12] This is used to terminate a series of <strong>S1</strong> records. If a SREC file is only used to program a memory device and the execution location is ignored, then an address of zero could be used.</p></td>
</tr>
</tbody>
</table>

### レコード順

Although some Unix documentation states "the order of S-records within a file is of no significance and no particular order may be assumed",\[13\] in practice most software has ordered the SREC records. The typical record order starts with a (sometimes optional) S0 header record, continues with a sequence of one or more S1/S2/S3 data records, may have one optional S5/S6 count record, and ends with one appropriate S7/S8/S9 termination record.

  - S19-style 16-bit address records

<!-- end list -->

1.  S0
2.  S1 (one or more records)
3.  S5 (optional record)
4.  S9

<!-- end list -->

  - S28-style 24-bit address records

<!-- end list -->

1.  S0
2.  S2 (one or more records)
3.  S5 (optional record)
4.  S8

<!-- end list -->

  - S37-style 32-bit address records

<!-- end list -->

1.  S0
2.  S3 (one or more records)
3.  S5 (optional record)
4.  S7

### 制限事項

**Record length** - Unix manual page documentation states, "An S-record file consists of a sequence of specially formatted ASCII character strings. An S-record will be less than or equal to 78 bytes in length." The manual page further limits the number of characters in the data field to 64 (or 32 data bytes).\[14\] A record with an 8-hex-character address and 64 data characters would be 78 (2+2+8+64+2) characters long (this count ignores possible end-of-line or string termination characters). The file could be printed on an 80-character wide teleprinter. A note at the bottom of the manual page states, "This \[manual page\] is the only place that a 78-byte limit on total record length or 64-byte limit on data length is documented. These values shouldn't be trusted for the general case."\[15\] If that limitation is ignored, the maximum length of an S-record is 514 characters: 2 for Record Type field + 2 for Byte Count field (whose value would be `0xFF=255`) + 2\*255 for Address, Data, and Checksum fields. Additional buffer space may be required for the line and string terminators. Using long line lengths has problems: "The Motorola S-record format definition permits up to 255 bytes of payload, or lines of 514 characters, plus the line termination. All EPROM programmers should have sufficiently large line buffers to cope with records this big. Few do."\[16\]

**Data field** - Some documentation recommends a maximum of 32 bytes of data (64 hex characters) in this field.\[17\] The minimum amount of data for S0/S1/S2/S3 records is zero. The maximum amount of data varies depending on the size of the address field. Since the Byte Count field can't be higher than 255 (0xFF), then the maximum number of bytes of data is calculated by 255 minus (1 byte for checksum field) minus (number of bytes in the address field). S0/S1 records support up to 252 bytes of data. S2 record supports up to 251 bytes of data. S3 record supports up to 250 bytes of data.

**Comments** - The SREC file format does not support comments. Some software ignores all text lines that do not start with "S" and ignores all text after the checksum field; that extra text is sometimes used (incompatibly) for comments. For example, the CCS PIC compiler supports placing a ";" comment line at the top or bottom of an [Intel HEX](https://ja.wikipedia.org/wiki/Intel_HEX "wikilink") file, and its manuals states "some programmers (MPLAB in particular) do not like comments at the top of the hex file", which is why the compiler has the option of placing the comment at the bottom of the hex file.\[18\]

## 例

  - Color legend

### チェックサム計算

The following example record:

is decoded to show how the checksum value is calculated as follows:

1.  Add: add each byte  +  +  = `19E` (hex) total.
2.  Mask: keep the least significant byte of the total = `9E` (hex).
3.  Complement: compute  of least significant byte =  (hex).

### 16-bit メモリアドレス







## 関連項目

  - , comparison of various encoding algorithms

  - [Intel HEX](https://ja.wikipedia.org/wiki/Intel_HEX "wikilink"), hex file format by Intel

  - , hex file format by Tektronix

## 参照資料

## 参考文献

  - Appendix A, "S Record Information", page A-1, states, "For compatibility with teletypewriters, some programs may limit the number of \[data\] bytes to as few as 28 (56 printable characters in the S-record)."

  -
  -
## 外部リンク

  - [RFC 4194 - The S Hexdump Format](https://tools.ietf.org/html/rfc4194) - IETF

<!-- end list -->

  - Software

<!-- end list -->

  - [SRecord](http://srecord.sourceforge.net/) is a collection of tools for manipulating SREC format files.
  - [BIN2MOT](http://www.keil.com/download/docs/4.asp), BINARY to Motorola S-Record file converter utility.
  - [SRecordizer](https://github.com/BigWinston/SRecordizer/wiki) is a tool for viewing, editing, and error checking S19 format files.
  - [bincopy](https://pypi.python.org/pypi/bincopy) is a python package for manipulating SREC format files.

[Category:組み込みシステム](https://ja.wikipedia.org/wiki/Category:組み込みシステム "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.