> この記事は[Windows-1252](https://ja.wikipedia.org/wiki/Windows-1252)から翻訳されています。


**Windows-1252**または**コードページ1252** (Code Page 1252, CP1252) は、[Microsoft Windowsの英語版および他の数種の西欧言語版で従来のコンポーネントが既定で使用する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ラテン文字](../Page/ラテン文字.md "wikilink")の[文字コード](../Page/文字コード.md "wikilink")である。

## 概要

[Windowsコードページ](https://ja.wikipedia.org/wiki/Windowsコードページ "wikilink")のグループの一種である。[LaTeX](../Page/LaTeX.md "wikilink")パッケージでは*ansinew*と呼ばれる。この文字コードは[ISO 8859-1の](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")[上位集合](https://ja.wikipedia.org/wiki/上位集合 "wikilink")だが、0x80から0x9Fの範囲に[制御文字](../Page/制御文字.md "wikilink")ではなく[図形文字](https://ja.wikipedia.org/wiki/図形文字 "wikilink")を収録していることにより、[IANAの](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")[ISO-8859-1](https://ja.wikipedia.org/wiki/ISO-8859-1 "wikilink")とは異なる。Windowsでは[コードページ](../Page/コードページ.md "wikilink")番号1252およびIANA登録名 "windows-1252" という名前で知られる。このコードページは[ISO 8859-15に含まれる印字可能文字もすべて収録している](https://ja.wikipedia.org/wiki/ISO/IEC_8859-15 "wikilink") (ただしいくつかは異なる[コードポイント](https://ja.wikipedia.org/wiki/コードポイント "wikilink")にマップされている)。

ISO 8859-1と比較して追加された文字としては、各種の欧文記号の他、[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")の[Œ](../Page/Œ.md "wikilink")、[フィンランド語](../Page/フィンランド語.md "wikilink")などで用いる[Š](../Page/Š.md "wikilink")と[Ž](https://ja.wikipedia.org/wiki/Ž "wikilink")、[ユーロ記号](../Page/ユーロ記号.md "wikilink")、ISO 8859-1では小文字しか収録されていなかった[Ÿ](https://ja.wikipedia.org/wiki/Ÿ "wikilink")がある。これらの文字は [ISO/IEC 8859-15](https://ja.wikipedia.org/wiki/ISO/IEC_8859-15 "wikilink") でも定義されている。

多くの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")がMIME charset ISO-8859-1をWindows-1252として扱い (ISO-8859-1の余分な制御コードはどのみちHTMLでは禁止されている)、そのため文字コードはISO-8859-1と宣言しているWebページにしばしばWindows-1252の符号が見られる。これは[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")でも同様である。しかしこのような文字の使用には、とりわけ受信側がLinuxやMac OSなど、Windows以外のシステムであるときに、困難が伴う可能性がある。他のシステムは0x80から0x9Fの範囲に意味のある文字を割り当てていないかもしれないし、異なる独自拡張の文字を割り当てているかもしれない。

Windows-1252のような、Windowsで使われるコードページを参照するために「[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")コードページ」という用語が使われることもある。Windows-1252はMicrosoft Windows用語ではANSIコードページとみなされているが、このコードページがANSIで標準化されたことはない。この名前は (後に変更されて[ISO-8859-1](https://ja.wikipedia.org/wiki/ISO-8859-1 "wikilink")となった) 初期のANSI草案から取られた。このように、Windows-1252は非標準のコードページであり歴史的理由からANSIコードページと呼ばれている \[1\]。

[Unicode](../Page/Unicode.md "wikilink") ([UTF-8](../Page/UTF-8.md "wikilink")形式であることが多い) がWindows-1252などの8ビット「コードページ」に代わって徐々に使われるようになりつつある。

## コード表

以下の表にWindows-1252を示す。<span style="text-decoration:underline">下線</span>は制御文字、および制御文字と図形文字の中間的性質をもつ文字を表す。ISO-8859-1からの変更点は背景色を変え、十進表記を「***太字・イタリック***」にすることで強調している。

| Windows-1252 (CP1252) |
| --------------------- |
|                       |
| 0x                    |
| 1x                    |
| 2x                    |
| 3x                    |
| 4x                    |
| 5x                    |
| 6x                    |
| 7x                    |
| 8x                    |
| 9x                    |
| Ax                    |
| Bx                    |
| Cx                    |
| Dx                    |
| Ex                    |
| Fx                    |

[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[ユニコードコンソーシアム](../Page/ユニコードコンソーシアム.md "wikilink")のWebサイト上の情報によれば、符号位置 81, 8D, 8F, 90, および 9D は未使用である。しかし、コードページからUnicodeへ変換するための[Windows API呼び出しはこれらを対応する](../Page/Windows_API.md "wikilink")[C1制御記号](https://ja.wikipedia.org/wiki/C1制御記号 "wikilink")にマップしている。符号位置 80 のユーロ文字はキャロン ([ハーチェク](../Page/ハーチェク.md "wikilink")) 付きの S や Z と同様、このコードページの以前のバージョンでは存在していなかった。

英語版 のWindowsでは、Windows-1252の文字は[Altキー](https://ja.wikipedia.org/wiki/Altキー "wikilink")を押下したままゼロに続けて文字の3桁10進符号を[テンキー](../Page/テンキー.md "wikilink")で入力することにより挿入できる (ゼロを省略する点以外同様の方法で、古い[コードページ437](https://ja.wikipedia.org/wiki/コードページ437 "wikilink")の文字も入力できる)。

## 脚注

## 関連項目

  - [Windowsコードページ](https://ja.wikipedia.org/wiki/Windowsコードページ "wikilink")
  - [西欧のラテン文字集合 (コンピュータ)](https://ja.wikipedia.org/wiki/西欧のラテン文字集合_\(コンピュータ\) "wikilink")

## 外部リンク

  - [Windows 1252の参照表](http://www.microsoft.com/globaldev/reference/sbcs/1252.mspx) (英語)
  - [IANAの文字コード名登録簿](http://www.iana.org/assignments/charset-reg/windows-1252) (英語)
  - [Windows 1252のUnicode対応表](http://www.unicode.org/Public/MAPPINGS/VENDORS/MICSFT/WINDOWS/CP1252.TXT) (英語)
  - ["best fit"によるWindows 1252のUnicode対応表](http://www.unicode.org/Public/MAPPINGS/VENDORS/MICSFT/WindowsBestFit/bestfit1252.txt) (英語)

[de:ISO 8859-1\#Windows-1252](https://ja.wikipedia.org/wiki/de:ISO_8859-1#Windows-1252 "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:ISO_8859](https://ja.wikipedia.org/wiki/Category:ISO_8859 "wikilink") [Category:Windowsコードページ](https://ja.wikipedia.org/wiki/Category:Windowsコードページ "wikilink")

1.  [The Old New Thing: Why is the default 8-bit codepage called "ANSI"?](http://blogs.msdn.com/oldnewthing/archive/2004/05/31/144893.aspx)