> この記事は[Broadcast Wave Format](https://ja.wikipedia.org/wiki/Broadcast_Wave_Format)から翻訳されています。


**Broadcast Wave Format** (**BWF**) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[WAV](../Page/WAV.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")の拡張であり、[映画](../Page/映画.md "wikilink")や[テレビ](../Page/テレビ.md "wikilink")で使われている[ノンリニア](../Page/ノンリニア編集.md "wikilink")[デジタルレコーダーの録音フォーマットとしてよく使われている](../Page/音響機器.md "wikilink")。

日本では、これを拡張した**BWF-J**という規格が使われている\[1\]。

## 概要

1997年、[欧州放送連合](../Page/欧州放送連合.md "wikilink")が仕様策定し、2001年と2003年に改定されている。

このフォーマットの目的は、各種コンピュータプラットフォームやアプリケーションでの音声データの円滑な交換を可能にする[メタデータ](../Page/メタデータ.md "wikilink")を追加することであった。従って、[メタデータ](../Page/メタデータ.md "wikilink")の形式が指定されていて、音響処理においてそれら情報を参照可能になっていて、他の記録との[同期が可能である](https://ja.wikipedia.org/wiki/タイムコード "wikilink")。このメタデータは標準のWAVファイルに追加された拡張チャンク（[RIFF参照](../Page/Resource_Interchange_File_Format.md "wikilink")）に格納される。

BWF形式のファイルの[拡張子](../Page/拡張子.md "wikilink")は .WAV である。

本来の WAV 形式でのチャンクに加えて、次のようなチャンクが追加されている。\[2\]

  - BWF本来の Bext チャンク ('bext')
  - iXMLチャンク ('iXML')
  - クオリティチャンク ('qlty')
  - MPEGオーディオ拡張チャンク ('mext')
  - ピークエンベロープチャンク ('levl')
  - リンクチャンク ('link')
  - axmlチャンク ('axml')
  - [コンティニューチャンク ('cont')](http://www.noa-audio.com/continue_chunk.html)

## WAVとの互換性

BWFと通常のWAVとの差異は、ファイルヘッダに拡張情報（Bextチャンク、符号化履歴など）があるという点だけあり、BWFを再生するのに特別なプレイヤーは必要としない。

だが、この互換性はWAVフォーマットのサイズ制限も引きずっている（サイズは32ビットで表されるが、多くの実装では符号付きで解釈されるため、2[GBが上限になっている](../Page/ギガバイト.md "wikilink")）。これを超えるような音声データを格納する場合、2種類のチャンク（上掲の "cont" と "link"）を使って複数のファイルに音声データを分割して格納できる。このような連続ファイルの命名規則は特に存在しないが、多くのプログラムは拡張子部分に番号を入れることで一目で連続したデータであることがわかるようになっている（.wav、.w01、.w02、…、.wNN といった形式）。これらのファイルはそれぞれBWFファイルとしての形式を保っているが、再生ソフトは最初のファイルを開いたときに全体をひとまとめに扱うことが多い。

BWF互換で多チャンネルの4GB以上の大きなファイルを作成できるフォーマットとして、2006年に[RF64](https://ja.wikipedia.org/wiki/RF64 "wikilink")が策定された。

## 関連項目

  - [WAV](../Page/WAV.md "wikilink")
  - [MXF](../Page/Material_Exchange_Format.md "wikilink") (Material eXchange Format)
  - [Advanced Authoring Format](https://ja.wikipedia.org/wiki/Advanced_Authoring_Format "wikilink")

## 脚注

## 外部リンク

  - [EBU Tech 3285 - Specification of the Broadcast Wave Format (BWF) - Version 1 - first edition (2001)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_tcm6-10544.pdf)
  - [EBU Tech 3285-s1 - Specification of the Broadcast Wave Format (BWF) - Supplement 1, MPEG Audio - first edition (1997)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_s1_tcm6-10545.pdf)
  - [EBU Tech 3285-s2 - Specification of the Broadcast Wave Format (BWF) - Supplement 2, Capturing Report - first edition (2001)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_s2_tcm6-10482.pdf)
  - [EBU Tech 3285-s3 - Specification of the Broadcast Wave Format (BWF) - Supplement 3, Peak Envelope Chunk - first edition (2001)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_s3_tcm6-10483.pdf)
  - [EBU Tech 3285-s4 - Specification of the Broadcast Wave Format (BWF) - Supplement 4, Link Chunk - first edition (2003)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_s4_tcm6-10484.pdf)
  - [EBU Tech 3285-s5 - Specification of the Broadcast Wave Format (BWF) - Supplement 5, <axml> Chunk - first edition (2003)](http://www.ebu.ch/CMSimages/en/tec_doc_t3285_s5_tcm6-10485.pdf)

[Category:音響工学](https://ja.wikipedia.org/wiki/Category:音響工学 "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink")

1.  [技術委員会オーディオ部会 BWF-J ワーキンググループ報告](http://www.jppanet.or.jp/bwf-j/bwf-j.htm) [一般社団法人](https://ja.wikipedia.org/wiki/一般社団法人 "wikilink")[日本ポストプロダクション協会](https://ja.wikipedia.org/wiki/日本ポストプロダクション協会 "wikilink")、2005年11月7日
2.  [BWF User Guide](http://www.ebu.ch/en/technical/publications/userguides/bwf_user_guide.php) 欧州放送連合