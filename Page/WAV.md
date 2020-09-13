> この記事は[WAV](https://ja.wikipedia.org/wiki/WAV)から翻訳されています。


**WAV**または**WAVE**（ウェイヴ、ウェヴ、ワヴ） (RIFF waveform Audio Format) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[IBM](../Page/IBM.md "wikilink")により開発された音声データ記述のための[フォーマットである](../Page/音声ファイルフォーマット.md "wikilink")。[RIFFの一種](../Page/Resource_Interchange_File_Format.md "wikilink")。主として[Windowsで使われるファイル形式である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[ファイルに格納した場合の](../Page/ファイル_\(コンピュータ\).md "wikilink")[拡張子](../Page/拡張子.md "wikilink")は、.wav。

RIFF上の識別子は「WAVE」であるが、拡張子から、WAVフォーマットという呼び名が一般化した。音楽業界ではweb（ウェブ）と響きを区別する為に、ワブとも呼ばれる。

通常は非圧縮、リニア[PCMの](../Page/パルス符号変調.md "wikilink")[サンプリング](../Page/サンプリング.md "wikilink")データ用のフォーマットとして扱われるが、WAVはいわゆる[コンテナ形式で](../Page/コンテナフォーマット.md "wikilink")、データ形式は自由であり、[μ-lawや](../Page/G.711.md "wikilink")、[ADPCM](../Page/適応的差分パルス符号変調.md "wikilink")、[MP3](../Page/MP3.md "wikilink")、[WMAなどの圧縮データを格納することもできる](../Page/Windows_Media_Audio.md "wikilink")。Windows以外のOSで作成したリニアPCMデータを直接Windowsで閲覧するとwavとして認識される。

WAVフォーマットでは、データ長が32ビット符号なし[整数型](../Page/整数型.md "wikilink")で記述されているため、4GBを超えるファイルを作成できない。この制限を越えるため、データ長を[64ビット](../Page/64ビット.md "wikilink")符号なし整数型で記述するWave64 (.w64) というフォーマットも存在する。

RIFFのチャンクとして、WAVファイル内にタグ情報を付加する事が出来るが、使用する文字コードは特に規定されておらず、互換性に問題が生じ易い仕様になっている。

## 仕様

### RIFF

RIFFファイルはタグ付きのファイル形式で、チャンクと呼ばれるコンテナの集合である\[1\]。 チャンクには4文字のタグ)FourCC)とチャンクのサイズ(バイト数)があり、タグによってチャンクのフォーマットが区別される。 いくつか標準的なタグがあり、4文字すべてが大文字のタグは予約されたタグである。
RIFFファイルの一番外側のチャンクはRIFFタグを持つ。 チャンクデータの最初の4バイトはフォームの種類を指定するFourCCでその後ろにサブチャンクが続く。 WAVファイルの場合、FourCCは`WAVE`である。
RIFF形式ではチャンクの出現順には一般的な規定がないが、`fmt`チャンクは`data`チャンクの直前に置くという例外がある。
タグファイル形式の利点として、RIFFファイルの利用者が知らないタグは読み飛ばし、処理可能なチャンクのみを扱うことができる点があげられる。

RIFFフォーマットにおいて複数バイトで表現されるデータの並びは[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")である。

RIFFファイルの一例を挙げる。 この例ではオフセット0x0に`RIFF`チャンクがあり、チャンクの長さは0x00630b20である。 `FourCC`は`WAVE`であり、ファイルがWAVファイルであることを示している。 オフセット0x12からはサブチャンクが続く。 オフセット0x30から`fmt`チャンクが始まり、オフセット0x48から`data`チャンクが始まっている。 <code>

    00000000   52 49 46 46 20 0b 63 00 57 41 56 45 4a 55 4e 4b  RIFF .c.WAVEJUNK
    00000010   1c 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    00000020   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    00000030   66 6d 74 20 10 00 00 00 01 00 02 00 44 ac 00 00  fmt ........D...
    00000040   10 b1 02 00 04 00 10 00 64 61 74 61 d8 0a 63 00  ........data..c.
    00000050   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    00000060   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    00000070   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    00000080   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
    ...

</code>

### fmt チャンク

`fmt`チャンクの構造は、拡張可能なWAVEFORMATEX構造体によって定義される\[2\]。

チャンネル数、サンプルレート、サンプルのビット数などが定義される。

    typedef struct {
        WORD  wFormatTag;
        WORD  nChannels;
        DWORD nSamplesPerSec;
        DWORD nAvgBytesPerSec;
        WORD  nBlockAlign;
        WORD  wBitsPerSample;
        WORD  cbSize;
    } WAVEFORMATEX;

`fmt`チャンクのサイズが16バイトのときは、拡張を持たないフォーマットでありcbSizeは存在しない。

フォーマットはwFormatTagであらわされ、リニアPCMの場合は1(`WAVE_FORMAT_PCM`)、32ビット浮動小数点の場合は3(`WAVE_FORMAT_IEEE_FLOAT`)となっている。 これらの定数はWindows SDKに含まれるmmreg.h\[3\]によって定義されており、さらにそれぞれのフォーマットによって`fmt`チャンクの構造の詳細が決まる。

### dataチャンク

`data`チャンクの中身は`fmt`チャンクによって定義されるフォーマットに基づく。

2チャンネルのリニアPCMの場合には、左チャンネル・右チャンネルの順に[符号付整数](https://ja.wikipedia.org/wiki/符号付整数 "wikilink")([2の補数](../Page/2の補数.md "wikilink"))で格納される。

[浮動小数点数](../Page/浮動小数点数.md "wikilink")で格納される場合、慣習からデータ値の範囲は-1.0から+1.0に限られる。

## Windows上での圧縮

Windows上では、[ACMを利用すれば](https://ja.wikipedia.org/wiki/Audio_Compression_Manager "wikilink")、圧縮などが行える。この機能が利用できる[ソフトウェア](../Page/ソフトウェア.md "wikilink")として、[サウンド レコーダーがある](../Page/サウンド_レコーダー.md "wikilink")。

## 脚注

## 関連項目

  - [AIFF](../Page/AIFF.md "wikilink") - wavと同じ用途で使用されるコンテナフォーマット
  - [Broadcast Wave Format](../Page/Broadcast_Wave_Format.md "wikilink") (BWF) - wavの内包するデータを厳密化、チャンクを拡張した形式
  - [Cwav](../Page/Cwav.md "wikilink") - wavを利用した圧縮形式

## 外部リンク

  - [Extensible Wave-Format Descriptors](https://docs.microsoft.com/en-us/windows-hardware/drivers/audio/extensible-wave-format-descriptors) from Microsoft (Updated October 26, 2017)
  - [WAVE File Format - technical details](https://web.archive.org/web/20080113195252/http://www.borg.com/~jglatt/tech/wave.htm) (1999)

### 解説サイト

  - [Broadband Watch--BBっとWORDS 「WAVの構造と現状」](http://bb.watch.impress.co.jp/cda/bbword/16386.html)

[Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:デジタルオーディオ](https://ja.wikipedia.org/wiki/Category:デジタルオーディオ "wikilink") [Category:スタジオ関連機材](https://ja.wikipedia.org/wiki/Category:スタジオ関連機材 "wikilink")

1.  [Sustainability of Digital Formats: Planning for Library of Congress Collections - RIFF (Resource Interchange File Format)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000025.shtml)
2.  [Microsoft Docs WAVEFORMATEX](https://docs.microsoft.com/en-us/previous-versions//ms713497%28v%3dvs.85%29)
3.  [Microsoft Docs mmreg.h header](https://docs.microsoft.com/en-us/windows/win32/api/mmreg/)