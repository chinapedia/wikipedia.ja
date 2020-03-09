> この記事は[PROM](https://ja.wikipedia.org/wiki/PROM)から翻訳されています。


**PROM** (Programmable ROM) は、[コンピュータ](../Page/コンピュータ.md "wikilink")システムで使用される[ROMの一種で](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、通常時はデータを読み出すだけで書き込む事ができないが、特定の手順で書き込みが可能なもののこと。およびその特徴を持ったROMの総称。

## 種類

書き込み可能なROMの総称として、以下の分類のものがある。

  - OTP ROM (One Time Programmable ROM) 1回のみ書込可能、消去不可
      - ヒューズROM
          - [ヒューズ](https://ja.wikipedia.org/wiki/ヒューズ "wikilink")型
              - 配線を焼き切るタイプ
              - [PN接合](https://ja.wikipedia.org/wiki/PN接合 "wikilink")を破壊するタイプ（バイポーラROM）
          - アンチヒューズ型
              - [MOS絶縁膜を破壊するタイプ](https://ja.wikipedia.org/wiki/MOSFET "wikilink")
      - 消去窓無し[UV-EPROM](https://ja.wikipedia.org/wiki/UV-EPROM "wikilink")
  - [EPROM](https://ja.wikipedia.org/wiki/EPROM "wikilink") 書込可能、消去可能
      - [UV-EPROM](https://ja.wikipedia.org/wiki/UV-EPROM "wikilink") 高電圧印加で書込可能、紫外線を照射することで消去可能
      - [EEPROM](https://ja.wikipedia.org/wiki/EEPROM "wikilink") 通常電圧印加で書込可能、通常電圧（もしくは高電圧）印加で消去可能
          - [フラッシュメモリ](https://ja.wikipedia.org/wiki/フラッシュメモリ "wikilink")（フラッシュ型EEPROM）

## OTPROM

[thumb社製のマイクロコントローラ](https://ja.wikipedia.org/wiki/ファイル:PIC16C57.JPG "wikilink")[PICのOTP](https://ja.wikipedia.org/wiki/PIC_\(コントローラ\) "wikilink") ROM版\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:PIC16C57JW.JPG "wikilink")

書き込み可能なROMのうち消去不可能なもの、つまり1回のみ書き込むことができるROMのことを指して、EPROMは含めずにPROMと言うことがある。

情報を書き込む際は、ROMライタと呼ばれる専用装置を使い、高電圧をかけて書き込みを行う。

ヒューズROMは、データに対応する[ビット](https://ja.wikipedia.org/wiki/ビット "wikilink")毎のヒューズの導通の有無で0/1を表す。

消去窓無しUV-EPROMは、消去窓が無い分紫外線照射によって消去することができないこと以外は、基本的にUV-EPROMの動作と同じである。データに対応するビット毎の[フローティングゲート](https://ja.wikipedia.org/wiki/フローティングゲート "wikilink")に電荷を貯め、電荷の有無で0/1を表す。

OTPROMは[マスクROM](https://ja.wikipedia.org/wiki/マスクROM "wikilink")に比べ、データの内容にあわせたフォトマスクを製造しなくて済む分、期間短縮、コストダウンにつながり、少量多品種の用途に向いている。

  - 代表的なOTPROM製品
      - 単体のROM
          - ヒューズROM 23xxx（23128など）
          - 消去窓無しUV-EPROM 27Cxxx（27C256など）
      - 他の回路と一緒にワンチップに集積したもの
          - [マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")
          - [プログラマブルロジックデバイス](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス "wikilink") PAL, GAL, アンチヒューズ型のCPLD,FPGA

2010年現在、多くの用途でフラッシュメモリーが用いられているため、あえてOTPROMを用いる場面は少ない。

フラッシュメモリーが登場する以前は、プログラム開発時は消去窓ありUV-EPROMを用いて消去/書込を繰り返し、量産時にはパッケージコストが安い消去窓無しUV-EPROM (OTPROM) を用いて単価を下げるという使い分けを行っていた。もっと大規模な大量生産を行う場合は、更に単価が安いマスクROMを用いる場合もある。

一部のマイクロコントローラでは、消去窓のがある[パッケージにチップが収められたものを開発用として](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\) "wikilink")、消去/書込を繰り返し可能にしている。一方量産用として、消去窓なしの安価なプラスチックパッケージに同じチップを収め、パッケージコストを下げたものを安く販売している。どちらもチップ自体は全く同じ (UV-EPROM) である。

## 関連項目

  - [EPROM](https://ja.wikipedia.org/wiki/EPROM "wikilink")
  - [Write Once Read Many](https://ja.wikipedia.org/wiki/Write_Once_Read_Many "wikilink")

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")