> この記事は[MusicXML](https://ja.wikipedia.org/wiki/MusicXML)から翻訳されています。


**MusicXML**は、[XML形式の](../Page/Extensible_Markup_Language.md "wikilink")[楽譜](../Page/楽譜.md "wikilink")表記のための[オープン](../Page/オープン.md "wikilink")な[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。[Recordare](https://ja.wikipedia.org/wiki/Recordare "wikilink")（現[MakeMusic](https://ja.wikipedia.org/wiki/MakeMusic "wikilink")）によって開発された。[Finale](../Page/Finale.md "wikilink")や[Sibelius](https://ja.wikipedia.org/wiki/Sibelius "wikilink")、[Rosegarden](../Page/Rosegarden.md "wikilink")、[Notion](http://www.mi7.co.jp/products/presonus/notion/)などの[楽譜作成ソフトウェア](../Page/楽譜作成ソフトウェア.md "wikilink")によって作成することが可能である。

同じく楽譜記述のためのフォーマットである[MusiXML](https://ja.wikipedia.org/wiki/MusiXML "wikilink")とは関係ない。また、[ミュージカル・プラン](https://ja.wikipedia.org/wiki/ミュージカル・プラン "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である[MusicX](https://ja.wikipedia.org/wiki/MusicX "wikilink")の形式も、同様の名前だが、[互換性](../Page/互換性.md "wikilink")はない。

現在、楽譜作成ソフト独自[ファイルとMusicXMLの相互変換を目的としたDolet](../Page/ファイルフォーマット.md "wikilink")® Pluginsというプラグインを公開しており、2012年12月時点では[Finale](../Page/Finale.md "wikilink")版と[Sibelius](https://ja.wikipedia.org/wiki/Sibelius "wikilink")版が存在している。

## ファイルの例

[MusicXML_C_Whole_Note.svg](https://ja.wikipedia.org/wiki/File:MusicXML_C_Whole_Note.svg "fig:MusicXML_C_Whole_Note.svg") 右の楽譜を表現するための例を以下に示す。

``` xml
 <?xml version="1.1" encoding="UTF-8" standalone="no"?>
 <!DOCTYPE score-partwise PUBLIC
     "-//Recordare//DTD MusicXML 1.1 Partwise//EN"
     "http://www.musicxml.org/dtds/partwise.dtd">
 <score-partwise>
   <part-list>
     <score-part id="P1">
       <part-name>Music</part-name>
     </score-part>
   </part-list>
   <part id="P1">
     <measure number="1">
       <attributes>
         <divisions>1</divisions>
         <key>
           <fifths>0</fifths>
         </key>
         <time>
           <beats>4</beats>
           <beat-type>4</beat-type>
         </time>
         <clef>
           <sign>G</sign>
           <line>2</line>
         </clef>
       </attributes>
       <note>
         <pitch>
           <step>C</step>
           <octave>4</octave>
         </pitch>
         <duration>4</duration>
         <type>whole</type>
       </note>
     </measure>
   </part>
 </score-partwise>
```

## 外部リンク

  - [公式ホームページ](http://www.makemusic.com/musicxml) - 一部ページ、日本語対応
  - [開発者向けページ](http://www.musicxml.com/ja/for-developers/) - 定義ファイル一覧

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink")