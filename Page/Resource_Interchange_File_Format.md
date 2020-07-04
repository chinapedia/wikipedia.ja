> この記事は[Resource Interchange File Format](https://ja.wikipedia.org/wiki/Resource_Interchange_File_Format)から翻訳されています。


（**RIFF**、「資源交換用ファイル形式」の意味）は、タグ付きのデータを格納するための汎用メタファイル形式である。[1991年](../Page/1991年.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[IBM](../Page/IBM.md "wikilink")が提案し、マイクロソフトの[Windows 3.1のマルチメディアファイルのデフォルトフォーマットとして採用された](../Page/Microsoft_Windows_3.x.md "wikilink")。[エレクトロニック・アーツ](../Page/エレクトロニック・アーツ.md "wikilink")が[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に策定した[Interchange File Format](../Page/Interchange_File_Format.md "wikilink") (IFF、「交換用ファイル形式」の意味) に基づいている。RIFFは[IBM PCが使っている](../Page/IBM_PC.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサに合わせて多[バイト整数を](../Page/バイト_\(情報\).md "wikilink")[リトルエンディアン形式で格納するのに対して](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、IFFは[Amiga](../Page/Amiga.md "wikilink")や[Macintosh](../Page/Macintosh.md "wikilink")で使われていたため、[68kプロセッサのビッグエンディアンを採用していた点が異なる](../Page/MC68000.md "wikilink")。なお、[アップルは](../Page/アップル_\(企業\).md "wikilink")[1988年](../Page/1988年.md "wikilink")にIFFに基づいた[ビッグエンディアンの](https://ja.wikipedia.org/wiki/エンディアン "wikilink")[AIFF](../Page/AIFF.md "wikilink")を策定している。

マイクロソフトの実装は、RIFFメタ形式を基盤とした各種[ファイル形式](../Page/ファイルフォーマット.md "wikilink") ([AVI](../Page/Audio_Video_Interleave.md "wikilink"), [ANI](https://ja.wikipedia.org/wiki/ANI_\(ファイルフォーマット\) "wikilink"), [WAV](../Page/WAV.md "wikilink")) で知られている。

## 概要

RIFFファイルは「チャンク」と呼ばれるものの並びである。形式は[IFFと全く同一であり](../Page/Interchange_File_Format.md "wikilink")、上述の通りエンディアンだけが異なる。また、チャンク名の意味も一部異なる。

全てのチャンクは次のような形式である。

  - 4バイト: チャンクの[ASCII](../Page/ASCII.md "wikilink")識別子。例えば「fmt」、「data」など。
  - 4バイト: 符号なしでリトルエンディアンの32[ビット](../Page/ビット.md "wikilink")整数。チャンクの長さを示す（このフィールドと上の識別子を除いた長さ）。
  - 可変長フィールド: チャンクデータ本体。長さは上記フィールドで示されたもの。
  - パディング: チャンク長が偶数バイトでない場合に1バイト追加される。

チャンク識別子「RIFF」と「LIST」は、チャンク内にサブチャンクを含むことができる。これらのチャンクは、識別子と長さの後が次のような形式である。

  - 4バイト: このチャンクのASCII識別子（フォームタイプと呼ぶ。RIFFチャンクの場合、「AVI」や「WAVE」がある）
  - サブチャンクの並び

ファイル全体が1つのRIFFチャンクで構成され、サブチャンクの並びが格納されている。したがって、正しいRIFFファイルの先頭には「R」、「I」、「F」、「F」の4文字が必ず存在する。

[欧州放送連合](../Page/欧州放送連合.md "wikilink")が開発したRIFF仕様に基づいた多チャンネルファイル形式として[RF64](https://ja.wikipedia.org/wiki/RF64 "wikilink")がある。これは[BWF互換であり](../Page/Broadcast_Wave_Format.md "wikilink")、4[ギガバイト](../Page/ギガバイト.md "wikilink")を超えるファイルが構成可能である。

## INFOチャンク

マイクロソフトのWindows 3.1の公式文書によると、ファイルの先頭にINFOチャンクを置くべきとしている。これにより、ファイル内容に関する[メタデータ](../Page/メタデータ.md "wikilink")に素早くアクセスでき、ファイルシステムやマルチメディアアプリケーションがファイルの先頭を参照して、作者情報、サムネイル、プレビュー、ファイル形式情報などを取り出せる。

[Windows XPのファイル管理では](../Page/Microsoft_Windows_XP.md "wikilink")、RIFF形式のファイルがあると自動的にINFOチャンクを読もうとする。また、ユーザーがファイルサイズや作成日などの属性情報に加えて、RIFFフィールド（作者、コピーライト日付）を指定することもできる。

## 問題

マイクロソフトは、あらゆるマルチメディアファイルにRIFFを使用するという方針の下、[MIDI](../Page/MIDI.md "wikilink")ファイルにもRIFFを使った新たなファイル形式を策定した。これは、既存のをRIFFラッパーで囲んだような形式で、`.rmi`（ に由来）という拡張子であった。このため、Windows上でMIDIファイルを新たな形式に変換してやる必要が生じた。

大きな動画ファイルでは、先頭にあるべきINFOチャンクを拡張・追加するということはファイル全体のずれを生じるため、ディスクI/Oが多数発生する。これを防ぐため、大きなファイルを作成するときにINFOチャンクにダミーデータを使ってパディングしておく必要がある。そうすることでINFOチャンクに新たな情報を追加してもファイル全体にずれが生じない。そのため、プログラマには正しいファイル形式の知識が必要だった。しかし、マイクロソフトのRIFFに関する文書は分散していて把握しきれないことも多く、一部のプログラマはファイルの最後尾にINFOチャンクを追加してもよいと思い込んでしまった。この対処法が広まった結果、非互換が生じ、正しいファイル形式しか認識しないソフトウェアによって最後尾のINFOチャンクが上書きされてしまうなどの問題が出てきた。

このような擬似RIFFファイルは特に[Macintosh](../Page/Macintosh.md "wikilink")でよく見られた（Macintoshのプログラマがマイクロソフトの仕様を把握していないことが多かったためと言われている）。一般にMacintosh上のソフトウェアやクロスプラットフォームのソフトウェアの開発者はこの問題に気づいており、間違ったINFOチャンクも扱えるようにしていることが多かった。例えば、2004年ごろのアップルのWindows上での[QuickTime](../Page/QuickTime.md "wikilink")プレイヤーソフトは間違ったINFOチャンクも扱えていたが、[ソニー](../Page/ソニー.md "wikilink")のWindows専用のソフトはそうではなかった。これは、多数のメディアファイルを一括処理する場合に問題を生じ、例えば一括でファイル形式の変換をする際に（ユーザーが気づく前に）メタデータが失われてしまうといった事態が発生する。

[CorelDRAW](../Page/CorelDRAW.md "wikilink")10 は通常、RIFFファイル構造を使うが、INFOチャンクは最後尾に置かれる。そのため、デフォルトのWindowsのファイルマネージャではビットマップのプレビューが表示できない。これに対処するにはアドオンユーティリティが必要である。

## RIFF に基づく主なファイル形式

  - [WAV](../Page/WAV.md "wikilink") （Windowsオーディオ）
  - [AVI](../Page/Audio_Video_Interleave.md "wikilink") （Windows動画）
  - RMI （Windows RIFF [MIDI](../Page/MIDI.md "wikilink")ファイル）
  - CDR （[CorelDRAW](../Page/CorelDRAW.md "wikilink")ベクターグラフィックスファイル）
  - [ANI](https://ja.wikipedia.org/wiki/ANI_\(ファイルフォーマット\) "wikilink") （Windowsのアニメーション付きカーソル）
  - [WebP](https://ja.wikipedia.org/wiki/WebP "wikilink") （[Google](../Page/Google.md "wikilink")が開発した静止画ファイル形式）

## 関連項目

  - [IFF](../Page/Interchange_File_Format.md "wikilink")
  - [AIFF](../Page/AIFF.md "wikilink")
  - [FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink")
  - [BWF](../Page/Broadcast_Wave_Format.md "wikilink")

## 外部リンク

  - [](http://msdn2.microsoft.com/en-us/library/ms713231.aspx)
  - \[<http://msdn2.microsoft.com/en-us/library/ms779636(VS.85>).aspx \]
  - [](http://msdn.microsoft.com/ja-jp/archive/default.asp?url=/archive/en-us/dx81_vb/directx_vb/htm/_dx_reading_wave_files_dxaudio.asp)
  - [](http://msdn2.microsoft.com/en-us/library/ms807157.aspx)
  - [](http://support.microsoft.com/default.aspx?scid=KB;EN-US;Q120253)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")