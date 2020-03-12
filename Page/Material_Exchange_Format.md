> この記事は[Material Exchange Format](https://ja.wikipedia.org/wiki/Material_Exchange_Format)から翻訳されています。


**Material eXchange Format** (**MXF**) は[SMPTE](../Page/SMPTE.md "wikilink")規格によって定義された[放送局](../Page/放送局.md "wikilink")などプロユースのデジタル映像や音声を扱うための[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")である。

## 概要

MXFはコード化された様々な映像データや音声データをメタデータとともに梱包するための「容器」あるいは「包装紙」のようなものである。現在発生しているプロ用途以外での様々な問題に対応するべく規格化されており、タイムコードとメタデータを完全に対応することで将来的にはプロ用途の標準規格となることを想定した規格となっている。

MXF自体は[Zero Divergence Directive](https://ja.wikipedia.org/wiki/Zero_Divergence_Directive "wikilink") (ZDD) として知られている方針の下で[Advanced Authoring Format](https://ja.wikipedia.org/wiki/Advanced_Authoring_Format "wikilink") (AAF) と同時に開発されており、[ノンリニア編集](../Page/ノンリニア編集.md "wikilink")が容易に行えるように企画設計がなされている。

## 使われ方

MXFファイルのためのWindowsの[拡張子](../Page/拡張子.md "wikilink")は""である。 [アップルのマッキントッシュではFile](../Page/アップル_\(企業\).md "wikilink") Type Codeとして""（末尾に空白文字が付いていることに注意）が用意されている。

全世界の放送局、プロダクションの標準フォーマットである。アメリカにおいては、HDに変更されたときにほとんど放送局は、ファイルベースのMXFファイルから放送電波に載せて放送している。日本においては、若干遅れて、現時点(2017年）においてもVTR/VCRから送出している放送局が多い。ただし、業界のデファクトスタンダードだったソニーのVTRのHDCAMのサポート期間が2022年までになったことにより（既に販売は終了）、日本の主要局もVTRからの送出からファイルベースの送出に変わりつつある。

## ソフトウェア

## MXF規格

  - **基本文書**
      - SMPTE 377M: The MXF File Format Specification (the overall master document)
      - SMPTE EG41: MXF Engineering Guide (A guide explaining how to use MXF)
      - SMPTE EG42: MXF Descriptive Metadata (A guide explaining how to use descriptive metadata in MXF)
  - **操作方法**
      - SMPTE 390M: OP-Atom (a very simple and highly constrained layout for simple MXF files)
      - SMPTE 378M: OP-1a (the layout options for a minimal simple MXF file)
      - SMPTE 391M: OP-1b
      - SMPTE 392M: OP-2a
      - SMPTE 393M: OP-2b
      - SMPTE 407M: OP-3a, OP-3b
      - SMPTE 408M: OP-1c, OP-2c, OP-3c
          - SMPTEには上記のように色々な操作方法が決められているが、OP-AtomとOp1a以外のフォーマットは見たことがない。
  - **コンテナの仕様**
      - SMPTE 379M: Generic Container (the way that essence is stored in MXF files)
      - SMPTE 381M: GC-MPEG (how to store [MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink") essence data in MXF using the Generic Container)
      - SMPTE 383M: GC-DV (how to store [DV](../Page/DV_\(ビデオ規格\).md "wikilink") essence data in MXF using the Generic Container)
      - SMPTE 385M: GC-CP (how to store [SDTI-CP](https://ja.wikipedia.org/wiki/SDTI-CP "wikilink") essence data in MXF using the Generic Container)
      - SMPTE 386M: GC-D10 (how to store [SMPTE D10](https://ja.wikipedia.org/wiki/SMPTE_D10 "wikilink") essence data in MXF using the Generic Container)
      - SMPTE 387M: GC-D11 (how to store [SMPTE D11](https://ja.wikipedia.org/wiki/SMPTE_D11 "wikilink") essence data in MXF using the Generic Container)
      - SMPTE 382M: GC-AESBWF (how to store [AES/EBU](https://ja.wikipedia.org/wiki/AES/EBU "wikilink") and Broadcast Wave audio essence data in MXF using the Generic Container)
      - SMPTE 384M: GC-UP (how to store Uncompressed Picture essence data in MXF using the Generic Container)
      - SMPTE 388M: GC-AA (how to store A-law coded audio essence data in MXF using the Generic Container)
      - SMPTE 389M: Generic Container Reverse Play System Element
      - SMPTE 394M: System Item Scheme-1 for Generic Container
      - SMPTE 405M: Elements and Individual Data Items for the GC SI Scheme 1
  - **Metadata, Dictionaries and Registries**
      - SMPTE 380M: DMS1 (a standard set of descriptive metadata to use with MXF files)
      - SMPTE 436M: MXF Mappings for VBI Lines and Ancillary Data Packets
      - SMPTE RP210: SMPTE Metadata Dictionary (the latest version is available here: <http://www.smpte-ra.org/mdd/index.html> )
      - SMPTE RP224: Registry of SMPTE Universal Labels

## 標準文章の入手方法

SMPTEのWebサイトからSMPTE規格をまとめた文章が収録されたCD-ROMを注文できる。

## 関連項目

  - [Advanced Authoring Format](https://ja.wikipedia.org/wiki/Advanced_Authoring_Format "wikilink")
  - [Broadcast Wave Format](../Page/Broadcast_Wave_Format.md "wikilink")

## 外部リンク

  - [mpeg.co.jp MXFラボ](http://www.mpeg.co.jp/libraries/mxf/index.html)：日本語による専門家の解説（*2017年時点においてはかなり古い情報です。メンテナンスされていないので*）
  - <http://www.amwa.tv/>
  - <http://mxf.info/>
  - <http://www.irt.de/mxf/>
  - <http://www.freemxf.org/>
  - [US Library of Congress Digital Preservation Program: MXF Format Description Properties](http://www.digitalpreservation.gov/formats/fdd/fdd000013.shtml)
  - [mxf](http://www.convertmxffiles.com/mxf.htm)

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink")