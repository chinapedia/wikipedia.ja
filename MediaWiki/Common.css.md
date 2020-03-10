> この記事は[MediaWiki:Common.css](https://ja.wikipedia.org/wiki/MediaWiki:Common.css)から翻訳されています。


/\* ここに書いた CSS はすべての外装に反映されます \*/

/\*

`* フォント・ファミリの設定`
`*/`

.Unicode {

`   font-family: 'TITUS Cyberbit Basic', 'Code2000', 'Chrysanthi Unicode', 'Doulos SIL', 'Bitstream Cyberbit', 'Bitstream CyberBase', 'Bitstream Vera', 'Thryomanes', 'Gentium', 'GentiumAlt', 'Visual Geez Unicode', 'Lucida Grande', 'Arial Unicode MS', 'Microsoft Sans Serif', 'Lucida Sans Unicode', sans-serif;`

}

.IPA {

`   font-family: 'Charis SIL', 'Doulos SIL', 'DejaVu Sans', 'Code2000', 'Hiragino Kaku Gothic Pro', 'Matrix Unicode', 'Tahoma', 'Microsoft Sans Serif', sans-serif;`

}

.SAMPA {

`   font-family: 'Courier', monospace;`

}

/\* [Template:Polytonic](https://ja.wikipedia.org/wiki/Template:Polytonic "wikilink")で使用されていないため、.polytonicは不要と思われる \*/

  -
    lang(grc) /\*, .polytonic \*/ {

`   font-family: 'Athena', 'Gentium', 'Palatino Linotype', 'Arial Unicode MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Code2000', sans-serif;`

}

  -
    lang(my), .interwiki-my { font-family: 'Padauk' }
    lang(si), .interwiki-si { font-family: 'KaputaUnicode' }

/\* make the list of references look smaller \*/ ol.references, div.reflist {

`   font-size: 90%;            /* Default font-size */`

}

div.reflist ol.references {

`   font-size: 100%;           /* Reset font-size when nested in div.reflist */`
`   list-style-type: inherit;  /* Enable custom list style types */`

}

/\* default skin for navigation boxes \*/ /\* navbox container style \*/ .navbox {

`   box-sizing: border-box;`
`   border: 1px solid #a2a9b1;`
`   width: 100%; `
`   margin: auto;`
`   clear: both;`
`   font-size: 88%;`
`   text-align: center;`
`   padding: 1px;`

}

/\* single pixel border between adjacent navboxes (doesn't work for IE6, but that's okay) \*/ .navbox + .navbox {

`   margin-top: -1px;`

}

/\* title and above/below styles \*/ .navbox-title, .navbox-abovebelow, .navbox th {

`   text-align: center;`
`   padding-left: 1em;`
`   padding-right: 1em;`

}

/\* group style \*/ .navbox-group {

`   white-space: nowrap;`
`   text-align: right;`
`   font-weight: bold;`
`   padding-left: 1em;`
`   padding-right: 1em;`

}

/\* Background color \*/ .navbox, .navbox-subgroup {

`   background: #fdfdfd;`

}

/\* Must match background color \*/ .navbox-list {

`   border-color: #fdfdfd;`

}

/\* Level 1 color \*/ .navbox-title, .navbox th {

`   background: #ccccff;`

}

/\* Level 2 color \*/ .navbox-abovebelow, .navbox-group, .navbox-subgroup .navbox-title {

`   background: #ddddff;`

}

/\* Level 3 color \*/ .navbox-subgroup .navbox-group, .navbox-subgroup .navbox-abovebelow {

`   background: #e6e6ff;`

}

/\* Even row striping \*/ .navbox-even {

`   background: #f7f7f7;`

}

/\* Odd row striping \*/ .navbox-odd {

`   background: transparent;`

}

/\* [MediaWiki:Common.js](https://ja.wikipedia.org/wiki/MediaWiki:Common.js "wikilink") にある createCollapseButtons 関数を参照。 \*/ .collapseButton {

`   float: right;`
`   font-weight: normal;`
`   text-align: right;`
`   width: auto;`

}

/\* [Template:Navbox](https://ja.wikipedia.org/wiki/Template:Navbox "wikilink") に配置する場合、左に配置されている [Template:Tnavbar](https://ja.wikipedia.org/wiki/Template:Tnavbar "wikilink") とのバランスを取る。 \*/ .navbox .collapseButton {

`   width: 6em;`

}

/\* [en:MediaWiki:Common.css](https://ja.wikipedia.org/wiki/en:MediaWiki:Common.css "wikilink") から複製。 \*/ /\* Style for horizontal lists (separator following item).

`  Note: hlist formatting will break if the resulting HTML lacks a breakable character`
`  between list items. This happens when the following conditions are true:`
`  1) The list is made using wiki markup (where HTML is built by parser.php)`
`  2) HTMLTidy is disabled or unavailable (such as on Special: pages)`
`  In such cases, building lists with .hlist using HTML instead of wiki markup`
`  will work around this problem. See also `[`Bugzilla:39617`](https://ja.wikipedia.org/wiki/Bugzilla:39617 "wikilink")`.`
`  IE8-specific classes are assigned in `[`MediaWiki:Common.js/IEFixes.js`](https://ja.wikipedia.org/wiki/MediaWiki:Common.js/IEFixes.js "wikilink")`.`
`  Last updated: January 24, 2013`
`  @source mediawiki.org/wiki/Snippets/Horizontal_lists`
`  @maintainer: `[`User:Edokter`](https://ja.wikipedia.org/wiki/User:Edokter "wikilink")
`  @revision: 3.1`

  - /

.skin-monobook .hlist dl, .skin-modern .hlist dl, .skin-vector .hlist dl {

`   line-height: 1.5em;`

} .hlist dl, .hlist ol, .hlist ul {

`   margin: 0;`
`   padding: 0;`

} /\* Display list items inline and make them nowrap \*/ .hlist dd, .hlist dt, .hlist li {

`   margin: 0;`
`   display: inline;`
`   white-space: nowrap;`

} /\* Allow wrapping for list items (in tight spaces) \*/ .hlist.hwrap dd, .hlist.hwrap dt, .hlist.hwrap li {

`   white-space: normal;`

} /\* Display nested lists inline and allow them to wrap \*/ .hlist dl dl, .hlist dl ol, .hlist dl ul, .hlist ol dl, .hlist ol ol, .hlist ol ul, .hlist ul dl, .hlist ul ol, .hlist ul ul {

`   display: inline;`
`   white-space: normal;`

} /\* Generate interpuncts \*/ .hlist dt:after {

`   content: ": ";`
`   white-space: normal;`

} .hlist dd:after, .hlist li:after {

`   content: " · ";`
`   font-weight: bold;`
`   white-space: normal;`

} /\* 日本語版の独自仕様。-pipe と -hyphen \*/ .hlist-pipe dd:after, .hlist-pipe li:after {

`   content: " | ";`
`   font-weight: normal;`

} .hlist-hyphen dd:after, .hlist-hyphen li:after {

`   content: " - ";`
`   font-weight: normal;`

} .hlist-comma dd:after, .hlist-comma li:after {

`   content: "、 ";`
`   font-weight: normal;`

} .hlist dd:last-child:after, .hlist dt:last-child:after, .hlist li:last-child:after {

`   content: none;`

} /\* For IE8 \*/ .hlist dd.hlist-last-child:after, .hlist dt.hlist-last-child:after, .hlist li.hlist-last-child:after {

`   content: none;`

} /\* Add parentheses around nested lists \*/ .hlist dd dd:first-child:before, .hlist dd dt:first-child:before, .hlist dd li:first-child:before, .hlist dt dd:first-child:before, .hlist dt dt:first-child:before, .hlist dt li:first-child:before, .hlist li dd:first-child:before, .hlist li dt:first-child:before, .hlist li li:first-child:before {

`   content: "(";`
`   font-weight: normal;`

} .hlist dd dd:last-child:after, .hlist dd dt:last-child:after, .hlist dd li:last-child:after, .hlist dt dd:last-child:after, .hlist dt dt:last-child:after, .hlist dt li:last-child:after, .hlist li dd:last-child:after, .hlist li dt:last-child:after, .hlist li li:last-child:after {

`   content: ")";`
`   font-weight: normal;`

} /\* For IE8 \*/ .hlist dd dd.hlist-last-child:after, .hlist dd dt.hlist-last-child:after, .hlist dd li.hlist-last-child:after, .hlist dt dd.hlist-last-child:after, .hlist dt dt.hlist-last-child:after, .hlist dt li.hlist-last-child:after, .hlist li dd.hlist-last-child:after, .hlist li dt.hlist-last-child:after, .hlist li li.hlist-last-child:after {

`   content: ")";`
`   font-weight: normal;`

} /\* Put numbers in front of ordered list items \*/ .hlist.hnum ol {

`   counter-reset: list-item;`

} .hlist.hnum ol \> li {

`   counter-increment: list-item;`

} .hlist.hnum ol \> li:before {

`   content: counter(list-item) ".\a0";`

} .hlist.hnum dd ol \> li:first-child:before, .hlist.hnum dt ol \> li:first-child:before, .hlist.hnum li ol \> li:first-child:before {

`   content: "(" counter(list-item) " ";`

}

/\* Avoid elements from breaking between columns \*/ .nocolbreak, li, dd {

`   -webkit-column-break-inside: avoid;`
`   page-break-inside: avoid;`
`   break-inside: avoid-column;`

} dt {

`   -webkit-column-break-after: avoid;`
`   page-break-after: avoid;`
`   break-after: avoid-column;`

} dd {

`   -webkit-column-break-before: avoid;`
`   page-break-before: avoid;`
`   break-before: avoid-column;`

}

/\* Style for "notices" \*/ .notice {

`   text-align: justify;`
`   margin: 1em;`
`   padding: 0.2em;`

}

h1 {

`   line-height: 1.2em;`

}

/\* Metadata \*/ table.metadata {

`   border: 1px solid #a2a9b1;`
`   display: none;`

}

/\*

`Add formatting to make sure that "external references" from `[`Template:Ref`](https://ja.wikipedia.org/wiki/Template:Ref "wikilink")` do`
`not get URL expansion, not even when printed. The mechanism up to MediaWiki 1.4 was`
`that the HTML code contained a SPAN following the anchor A; this SPAN had the class`
`"urlexpansion", which was not displayed on screen, but was shown when the medium was`
`"print". The rules below ensure (a) that there is no extra padding to the right of`
`the anchor (displayed as "[`<number>`]"), (b) that there is no "external link arrow" for`
`the link, and (c) that this SPAN of class "urlexpansion" is never shown.`

  - /

.plainlinksneverexpand {

`   background: none !important;`
`   padding: 0 !important;`

}

.plainlinksneverexpand .urlexpansion {

`   display: none !important;`

}

/\*

`Make sure that ext links displayed within "plainlinksneverexpand" don't get`
`the arrow...`

  - /

.plainlinksneverexpand a {

`   background: none !important;`
`   padding: 0 !important`

}

/\*

`With MediaWiki 1.5, the mechanism has changed: instead of a SPAN of class "urlexpansion"`
`following the anchor A, the anchor itself now has class "external autonumber" and the`
`expansion is inserted when printing (see the common printing style sheet at`
`//en.wikipedia.org/w/skins/common/commonPrint.css) using the ":after" pseudo-`
`element of CSS. We have to switch this off for links due to Template:Ref!`

  - /

.plainlinksneverexpand a.external.text:after {

`   display: none !important;`

}

.plainlinksneverexpand a.external.autonumber:after {

`   display: none !important;`

}

/\* Change the external link icon to an Adobe icon for all PDF files \*/ .mw-parser-output a\[href$=".pdf"\].external, .mw-parser-output a\[href\*=".pdf?"\].external, .mw-parser-output a\[href\*=".pdf\#"\].external, .mw-parser-output a\[href$=".PDF"\].external, .mw-parser-output a\[href\*=".PDF?"\].external, .mw-parser-output a\[href\*=".PDF\#"\].external {

`   background: url("//upload.wikimedia.org/wikipedia/commons/2/23/Icons-mini-file_acrobat.gif") no-repeat right;`
`   /* @noflip */`
`   padding-right: 18px;`

}

/\* Merge template style \*/ .messagebox {

`   border: 1px solid #a2a9b1;`
`   background: #f8f9fa;`
`   width: 80%;`
`   margin: 0 auto 1em auto;`
`   padding: 0.2em;`
`   text-align: justify;`

}

.messagebox.merge {

`   border: 2px solid #033;`
`   width: 55%;`
`   background: #eff;`
`   padding: 1em;`
`   margin: 1em auto 1em auto;`

}

.messagebox.cleanup {

`   border: 1px solid #9f9fff;`
`   background: #efefff;`
`   text-align: center;`

}

.messagebox.standard-talk {

`   border: 1px solid #c0c090;`
`   background: #f8eaba;`

}

.infobox {

`   border: 1px solid #a2a9b1;`
`   background-color: #f8f9fa;`
`   color: black;`
`   margin: 0.5em 0 0.5em 1em;`
`   padding: 0.2em;`
`   float: right;`
`   clear: right;`
`   text-align: left;`
`   font-size: 88%;`
`   line-height: 1.5em;`

} .infobox caption {

`   margin-top: 0.5em;`
`   font-size: 125%;`
`   font-weight: bold;`

} .infobox td, .infobox th {

`   vertical-align: top;`

} .infobox.bordered {

`   border-collapse: collapse;`

} .infobox.bordered td, .infobox.bordered th {

`   border: 1px solid #a2a9b1;`

} .infobox.bordered .borderless td, .infobox.bordered .borderless th {

`   border: 0;`

}

.infobox.sisterproject {

`   width: 20em;`
`   font-size: 90%;`

}

/\* styles for bordered infobox with merged rows \*/ .infobox.bordered .mergedtoprow td, .infobox.bordered .mergedtoprow th {

`   border: 0;`
`   border-top: 1px solid #a2a9b1;`
`   /* @noflip */`
`   border-right: 1px solid #a2a9b1;`

}

.infobox.bordered .mergedrow td, .infobox.bordered .mergedrow th {

`   border: 0;`
`   /* @noflip */`
`   border-right: 1px solid #a2a9b1;`

}

/\* Styles for geography infoboxes, eg countries,

`  country subdivisions, cities, etc.            */`

.infobox.geography {

`   border-collapse: collapse;`
`   line-height: 1.6em;`
`   font-size: 88%;`

}

.infobox.geography td, .infobox.geography th {

`   border-top: 1px solid #a2a9b1;`
`   padding: 0.4em 0.6em 0.4em 0.6em;`

} .infobox.geography .mergedtoprow td, .infobox.geography .mergedtoprow th {

`   border-top: 1px solid #a2a9b1;`
`   padding: 0.4em 0.6em 0.2em 0.6em;`

}

.infobox.geography .mergedrow td, .infobox.geography .mergedrow th {

`   border: 0;`
`   padding: 0 0.6em 0.2em 0.6em;`

}

.infobox.geography .mergedbottomrow td, .infobox.geography .mergedbottomrow th {

`   border-top: 0;`
`   border-bottom: 1px solid #a2a9b1;`
`   padding: 0 0.6em 0.4em 0.6em;`

}

.infobox.geography .maptable td, .infobox.geography .maptable th {

`   border: 0;`
`   padding: 0;`

}

1.  wpSave {

`   font-weight: bold;`

}

/\* Icons for medialist templates [Template:Listen](https://ja.wikipedia.org/wiki/Template:Listen "wikilink"),

`  `[`Template:Multi-listen_start`](https://ja.wikipedia.org/wiki/Template:Multi-listen_start "wikilink")`, `[`Template:Video`](https://ja.wikipedia.org/wiki/Template:Video "wikilink")`,`
`  `[`Template:Multi-video_start`](https://ja.wikipedia.org/wiki/Template:Multi-video_start "wikilink")` */`

/\* TemplateStyles \*/ div.listenlist {

`   background: url("//upload.wikimedia.org/wikipedia/commons/4/47/Sound-icon.svg") no-repeat scroll 0 0 transparent;`
`   background-size: 30px;`
`   padding-left: 40px;`

}

/\* Change the external link icon to an Adobe icon anywhere the PDFlink class \*/ /\* is used (notably Template: PDFlink). This works in IE, unlike the above. \*/ span.PDFlink a {

`   background: url(//upload.wikimedia.org/wikipedia/commons/2/23/Icons-mini-file_acrobat.gif) center right no-repeat !important;`
`   padding-right: 17px !important;`

}

/\* infoboxCountry [Template:基礎情報 国等に](https://ja.wikipedia.org/wiki/Template:基礎情報_国 "wikilink") \*/ dl\#infoboxCountry {

`   clear: right;`
`   float: right;`
`   width: 300px;`
`   margin-left: 0.5em;`
`   background: #fff;`

}

dl\#infoboxCountry dt.infoboxCountryNameJa {

`   font-size: 1.36em;`
`   margin: 0 0 0.13em;`
`   text-align: center;`

}

dl\#infoboxCountry dt.infoboxCountryName {

`   font-size: 1.13em;`
`   font-weight: normal;`
`   margin: 0 0 0.13em;`
`   text-align: center;`

}

dl\#infoboxCountry dd.infoboxCountryDataA {

`   margin: 0;`
`   padding: 0;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   border-style: solid solid none solid;`
`   background: #f8f9fa;`

}

dl\#infoboxCountry table.infoboxCountryPrevSucc {

`   width: 298px;`
`   border-collapse: collapse;`
`   font-size: 0.95em;`
`   background: #f8f9fa;`

}

dl\#infoboxCountry table.infoboxCountryPrevSucc td {

`   margin: 0;`
`   padding: 4px;`
`   text-align: center;`

}

dl\#infoboxCountry td.infoboxCountryPrev {

`   text-align: left;`
`   width: 60px`

}

dl\#infoboxCountry td.infoboxCountrySucc {

`   text-align: right;`
`   width: 60px;`

}

dl\#infoboxCountry table.infoboxCountryInsignia {

`   width: 298px;`
`   border-collapse: collapse;`
`   font-size: 0.95em;`
`   background: #eee;`
`   text-align: center;`
`   border-top: 1px solid #a2a9b1;`

} dl\#infoboxCountry table.infoboxCountryInsignia th {

`   padding: 4px;`
`   width: 50%;`
`   border: none;`

}

dl\#infoboxCountry table.infoboxCountryInsignia td {

`   padding: 4px;`
`   font-size: 0.85em;`

}

dl\#infoboxCountry dd.infoboxCountryAdd, dl\#infoboxCountry dd.infoboxCountryMotto, dl\#infoboxCountry dd.infoboxCountryAnthem, dl\#infoboxCountry dd.infoboxCountryMap {

`   text-align: center;`
`   width: 290px;`
`   margin: 0;`
`   padding: 4px;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   border-style: solid solid none solid;`

}

dl\#infoboxCountry dd.infoboxCountryAdd, dl\#infoboxCountry dd.infoboxCountryMotto, dl\#infoboxCountry dd.infoboxCountryAnthem {

`   font-size: 0.8em;`
`   background: #f8f9fa;`

}

dl\#infoboxCountry dd.infoboxCountryMap { }

dl\#infoboxCountry dd.infoboxCountryDataB {

`   margin: 0;`
`   padding: 0;`
`   border: 1px solid #a2a9b1;`

}

dl\#infoboxCountry dd.infoboxCountryDataB table {

`   width: 298px;`
`   border-collapse: collapse;`
`   border-color: #a2a9b1;`
`   font-size: 0.9em;`
`   background: #f8f9fa;`
`   line-height: 1.3;`

}

dl\#infoboxCountry dd.infoboxCountryDataB tr {

`   border-color: #a2a9b1;`
`   vertical-align: top;`

}

dl\#infoboxCountry dd.infoboxCountryDataB th {

`   padding: 4px;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   text-align: left;`
`   font-weight: normal;`
`   width: 50%;`

}

dl\#infoboxCountry dd.infoboxCountryDataB td {

`   padding: 4px;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   width: 50%;`

}

dl\#infoboxCountry td.infoboxCountrySome {

`   padding: 0;`

}

dl\#infoboxCountry td.infoboxCountrySome dl, dl\#infoboxCountry td.infoboxCountrySome dl dd {

`   margin: 0;`
`   padding: 0;`

}

dl\#infoboxCountry td.infoboxCountrySome dl dt {

`   margin: 0;`
`   padding: 4px;`
`   font-weight: normal;`
`   border-top: 1px solid #a2a9b1;`

}

dl\#infoboxCountry td.infoboxCountrySome dl dt.infoboxCountryLeader {

`   border-top: none;`

}

dl\#infoboxCountry td.infoboxCountrySome dl table {

`   width: 100%;`
`   font-size: 100%;`
`   border-collapse: collapse;`
`   background: #f8f9fa;`

}

dl\#infoboxCountry td.infoboxCountrySome dl th {

`   width: 50%;`
`   padding: 4px;`
`   text-indent: 0.75em;`

}

dl\#infoboxCountry td.infoboxCountrySome dl td {

`   width: 50%;`
`   padding: 4px;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   border-style: solid none none solid;`

}

dd\#Infobox_before-after {

`   width: 298px;`
`   margin: 0;`
`   padding: 0;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   border-style: none solid solid solid;`
`   background: #f8f9fa;`

}

dd\#Infobox_before-after table {

`   border-collapse: collapse;`
`   width: 100%;`
`   background: transparent;`

}

dd\#Infobox_before-after th {

`   width: 50%;`
`   padding: 0 4px;`

}

dd\#Infobox_before-after th.infoboxCountryPrev {

`   border-right: 1px solid #ccc;`

}

dd\#Infobox_before-after th.infoboxCountrySucc {

`   border-left: #ccc 1px solid;`

}

dd\#Infobox_before-after td.infoboxCountryPrev {

`   width: 50%;`
`   padding: 2px 4px;`
`   font-size: 80%;`
`   text-align: left;`
`   vertical-align: top;`
`   border-color: #ccc;`
`   border-width: 1px;`
`   border-style: solid solid none none;`

}

dd\#Infobox_before-after td.infoboxCountrySucc {

`   width: 50%;`
`   padding: 2px 4px;`
`   font-size: 80%;`
`   text-align: right;`
`   vertical-align: top;`
`   border-color: #ccc;`
`   border-width: 1px;`
`   border-style: solid none none solid;`

}

dl\#infoboxCountry dd.infoboxCountryNote {

`   font-size: 0.75em;`
`   width: 290px;`
`   margin: 0;`
`   padding: 2px 4px;`
`   border-color: #a2a9b1;`
`   border-width: 1px;`
`   border-style: none solid solid;`
`   background: #f8f9fa;`

}

/\* リダイレクトの表示 \*/

/\* [特別:Allpages](https://ja.wikipedia.org/wiki/特別:Allpages "wikilink")・[特別:Prefixindex](https://ja.wikipedia.org/wiki/特別:Prefixindex "wikilink") \*/ .allpagesredirect a:link, .allpagesredirect a:visited, /\* カテゴリ内 \*/ .redirect-in-category a:link, .redirect-in-category a:visited, /\* ウォッチリスト \*/ .watchlistredir a:link, .watchlistredir a:visited {

`   color: #666;`

}

/\* NavFrame関係。[MediaWiki:Monobook.cssも参照](../MediaWiki/Monobook.css.md "wikilink") \*/ div.Boxmerge, div.NavFrame {

`   margin: 0px;`
`   padding: 2px;`
`   border: 1px solid #a2a9b1;`
`   text-align: center;`
`   border-collapse: collapse;`
`   font-size: 95%;`

}

div.Boxmerge div.NavFrame {

`   border-style: none;`
`   border-style: hidden;`

}

div.NavPic {

`   background-color: #ffffff;`
`   margin: 0px;`
`   padding: 2px;`
`   float: left;`

}

div.NavFrame div.NavHead {

`   height: 1.6em;`
`   font-weight: bold;`
`   font-size: 100%;`
`   background-color: #efefef;`
`   position: relative;`
`   text-align: center;`

}

div.NavFrame p {

`   font-size: 100%;`

}

div.NavFrame div.NavContent {

`   font-size: 100%;`

}

div.NavFrame div.NavContent p {

`   font-size: 100%;`

}

div.NavEnd {

`   margin: 0px;`
`   padding: 0px;`
`   line-height: 1px;`
`   clear: both;`

}

a.NavToggle {

`   position: absolute;`
`   top: 0px;`
`   right: 3px;`
`   font-weight: normal;`

/\* font-size: 83.3%;\*/ }

/\* Article message box styles \*/ table.ambox {

`   margin: 0px 10%;   /* 10% = 他の要素にはみ出るのを防ぐ */`
`   border: 1px solid #a2a9b1;`
`   border-left: 10px solid #1e90ff;    /* 初期値: "notice" の青 */`
`   background: #fbfbfb;`

} table.ambox + table.ambox { /\* 重なったボックスの間を単一の罫線に \*/

`   margin-top: -1px;`

} .ambox th.mbox-text, .ambox td.mbox-text { /\* メッセージ本体のセル \*/

`   padding: 0.25em 0.5em;       /* 左右に 0.5em ずつの余白 */`

} .ambox td.mbox-image { /\* 左の画像セル \*/

`   padding: 2px 0 2px 0.5em;    /* 左に 0.5em、右に 0px の余白 */`

} .ambox td.mbox-imageright { /\* 右の画像セル \*/

`   padding: 2px 0.5em 2px 0;    /* 左に 0px、右に 0.5em の余白  */`

}

table.ambox-notice {

`   border-left: 10px solid #1e90ff;    /* 青 */`

} table.ambox-speedy {

`   border-left: 10px solid #b22222;    /* 赤 */`
`   background: #fee;                   /* 桃 */`

} table.ambox-delete {

`   border-left: 10px solid #b22222;    /* 赤 */`

} table.ambox-content {

`   border-left: 10px solid #f28500;    /* 橙 */`

} table.ambox-style {

`   border-left: 10px solid #f4c430;    /* 黄 */`

} table.ambox-move {

`   border-left: 10px solid #9932cc;    /* 紫 */`

} table.ambox-protection {

`   border-left: 10px solid #bba;       /* 灰色・金色 */`

}

/\* Cell sizes for ambox/tmbox/imbox/cmbox/ombox/fmbox/dmbox message boxes \*/ th.mbox-text, td.mbox-text { /\* The message body cell(s) \*/

`   border: none; `
`   padding: 0.25em 0.9em;       /* 0.9em left/right */`
`   width: 100%;    /* Make all mboxes the same width regardless of text length */`
`   font-size: 90%;`

} td.mbox-image { /\* The left image cell \*/

`   border: none; `
`   padding: 2px 0 2px 0.9em;    /* 0.9em left, 0px right */`
`   text-align: center; `

} td.mbox-imageright { /\* The right image cell \*/

`   border: none;`
`   padding: 2px 0.9em 2px 0;    /* 0px left, 0.9em right */`
`   text-align: center; `

} td.mbox-empty-cell { /\* An empty narrow cell \*/

`   border: none;`
`   padding: 0px;`
`   width: 1px;`

}

/\*

`* `[`MediaWiki:Revision-info`](https://ja.wikipedia.org/wiki/MediaWiki:Revision-info "wikilink")`、`[`MediaWiki:Revision-info-currentのフォントサイズ調整`](https://ja.wikipedia.org/wiki/MediaWiki:Revision-info-current "wikilink")`。`
`* 2010-07-15 by `[`User:Penn``   ``Station`](https://ja.wikipedia.org/wiki/User:Penn_Station "wikilink")
`*/`

1.  revision-info, \#revision-info-current {

`  font-size: small;`
`  margin-top: 4px;`

}

/\* ambox - 以下、日本語版の独自拡張 \*/ table.ambox div.ambox-imagecontainer { /\* 画像セル内の画像表示領域 \*/

`   width: 52px;`

} table.ambox.ambox-section { /\* 節用メッセージボックス \*/

`   margin: 0 10%;`

} table.ambox.ambox-section div.ambox-imagecontainer {

`   width: 52px;`

}

table.ambox.ambox-section th.mbox-text, table.ambox.ambox-section td.mbox-text {

`   padding: 0.25em 0.5em;  `

}

/\* Image message box styles \*/ table.imbox {

`   margin: 4px 10%; `
`   border-collapse: collapse; `
`   border: 3px solid #1e90ff;    /* Default "notice" blue */`
`   background: #fbfbfb;`

} .imbox .mbox-text .imbox { /\* For imboxes inside imbox-text cells. \*/

`   margin: 0 -0.5em;    /* 0.9 - 0.5 = 0.4em left/right. */`

} .mbox-inside .imbox { /\* For imboxes inside other templates. \*/

`   margin: 4px;`

}

table.imbox-notice {

`   border: 3px solid #1e90ff;    /* Blue */`

} table.imbox-speedy {

`   border: 3px solid #b22222;    /* Red */`
`   background: #fee;             /* Pink */`

} table.imbox-delete {

`   border: 3px solid #b22222;    /* Red */`

} table.imbox-content {

`   border: 3px solid #f28500;    /* Orange */`

} table.imbox-style {

`   border: 3px solid #f4c430;    /* Yellow */`

} table.imbox-move {

`   border: 3px solid #9932cc;    /* Purple */`

} table.imbox-protection {

`   border: 3px solid #bba;       /* Gray-gold */`

} table.imbox-license {

`   border: 3px solid #88a;       /* Dark gray */`
`   background: #f7f8ff;          /* Light gray */`

} table.imbox-featured {

`   border: 3px solid #cba135;    /* Brown-gold */`

}

/\* Category message box styles \*/ table.cmbox {

`   margin: 3px 10%;`
`   border-collapse: collapse;`
`   border: 1px solid #a2a9b1; `
`   background: #DFE8FF;    /* Default "notice" blue */`

}

table.cmbox-notice {

`   background: #DFE8FF;    /* Blue */`

} table.cmbox-speedy {

`   margin-top: 4px;`
`   margin-bottom: 4px;`
`   border: 4px solid #b22222;    /* Red */`
`   background: #FFDBDB;          /* Pink */`

} table.cmbox-delete {

`   background: #FFDBDB;    /* Red */`

} table.cmbox-content {

`   background: #FFE7CE;    /* Orange */`

} table.cmbox-style {

`   background: #FFF9DB;    /* Yellow */`

} table.cmbox-move {

`   background: #E4D8FF;    /* Purple */`

} table.cmbox-protection {

`   background: #EFEFE1;    /* Gray-gold */`

}

/\* Other pages message box styles \*/ table.ombox {

`   margin: 4px 10%; `
`   border-collapse: collapse; `
`   border: 1px solid #a2a9b1;       /* Default "notice" gray */`
`   background: #f8f9fa;`

}

table.ombox-notice {

`   border: 1px solid #a2a9b1;       /* Gray */`

} table.ombox-speedy {

`   border: 2px solid #b22222;    /* Red */`
`   background: #fee;             /* Pink */`

} table.ombox-delete {

`   border: 2px solid #b22222;    /* Red */`

} table.ombox-content {

`   border: 1px solid #f28500;    /* Orange */`

} table.ombox-style {

`   border: 1px solid #f4c430;    /* Yellow */`

} table.ombox-move {

`   border: 1px solid #9932cc;    /* Purple */`

} table.ombox-protection {

`   border: 2px solid #bba;       /* Gray-gold */`

}

/\* Talk page message box styles \*/ table.tmbox {

`   margin: 4px 10%;`
`   border-collapse: collapse;`
`   border: 1px solid #c0c090;    /* Default "notice" gray-brown */`
`   background: #f8eaba;`

} .mediawiki .mbox-inside .tmbox { /\* For tmboxes inside other templates. The "mediawiki" \*/

`   margin: 2px 0;               /* class ensures that this declaration overrides other */`
`   width: 100%;  /* For Safari and Opera */     /* styles (including mbox-small above) */`

} .mbox-inside .tmbox.mbox-small { /\* "small" tmboxes should not be small when \*/

`   line-height: 1.5em;          /* also "nested", so reset styles that are   */   `
`   font-size: 100%;             /* set in "mbox-small" above.                */`

}

table.tmbox-speedy {

`   border: 2px solid #b22222;    /* Red */`
`   background: #fee;             /* Pink */`

} table.tmbox-delete {

`   border: 2px solid #b22222;    /* Red */`

} table.tmbox-content {

`   border: 2px solid #f28500;    /* Orange */`

} table.tmbox-style {

`   border: 2px solid #f4c430;    /* Yellow */`

} table.tmbox-move {

`   border: 2px solid #9932cc;    /* Purple */`

} table.tmbox-protection, table.tmbox-notice {

`   border: 1px solid #c0c090;    /* Gray-brown */`

}

/\* Disambig and set index box styles \*/ table.dmbox {

`   clear: both; `
`   margin: 0.9em 1em; `
`   border-top: 1px solid #ccc; `
`   border-bottom: 1px solid #ccc; `
`   background: transparent;`

}

/\* Footer and header message box styles \*/ table.fmbox {

`   clear: both;`
`   margin: 0.2em 0;`
`   width: 100%;`
`   border: 1px solid #a2a9b1;`
`   background: #f8f9fa;     /* Default "system" gray */`

} table.fmbox-system {

`   background: #f8f9fa;`

} table.fmbox-warning {

`   border: 1px solid #bb7070;  /* Dark pink */`
`   background: #ffdbdb;        /* Pink */`

} table.fmbox-editnotice {

`   background: transparent;`

}

/\* Div based "warning" style fmbox messages. \*/ div.mw-warning-with-logexcerpt, div.mw-lag-warn-high, div.mw-cascadeprotectedwarning, div\#mw-protect-cascadeon {

`   clear: both;`
`   margin: 0.2em 0;`
`   border: 1px solid #bb7070;`
`   background: #ffdbdb;`
`   padding: 0.25em 0.9em;`

} /\* Div based "system" style fmbox messages. Used in

`  `[`MediaWiki:Noarticletext`](../MediaWiki/Noarticletext.md "wikilink")` and `[`MediaWiki:Readonly``   ``lag`](https://ja.wikipedia.org/wiki/MediaWiki:Readonly_lag "wikilink")`. */`

div.mw-lag-warn-normal, div.noarticletext, div.fmbox-system {

`   clear: both;`
`   margin: 0.2em 0;`
`   border: 1px solid #a2a9b1;`
`   background: #f8f9fa;`
`   padding: 0.25em 0.9em;`

}

/\* These mbox-small classes must be placed after all other

`  ambox/tmbox/ombox etc classes. "body.mediawiki" is so `
`  they override "table.ambox + table.ambox" above. */`

body.mediawiki table.mbox-small { /\* For the "small=yes" option. \*/

`   clear: right;`
`   float: right;`
`   margin: 4px 0 4px 1em;`
`   width: 238px;`
`   font-size: 88%;`
`   line-height: 1.25em;`

} body.mediawiki table.mbox-small-left { /\* For the "small=left" option. \*/

`   margin: 4px 1em 4px 0;`
`   width: 238px;`
`   border-collapse: collapse;`
`   font-size: 88%;`
`   line-height: 1.25em;`

}

/\* [Template: Pathnav](https://ja.wikipedia.org/wiki/Template:_Pathnav "wikilink") \*/ .pathnavbox {

`   clear: both;`
`   border: 1px outset #eef;`
`   padding: 0.3em 0.6em;`
`   margin: 0 0 0.5em 0;`
`   background-color: #eef;`
`   font-size: 90%;`

}

.pathnavbox ul {

`   list-style: none none;`
`   margin-top: 0;`
`   margin-bottom: 0;`

}

.pathnavbox \> ul {

`   margin: 0;`

}

.pathnavbox ul li {

`   margin: 0;`

}

/\* 脚注ジャンプ先強調 \*/ ol.references \> li:target {

`   background-color: #DEF;`

}

sup.reference:target {

`   background-color: #DEF;`

}

cite:target {

`   background-color: #DEF;`

}

/\* Otheruses等の冒頭曖昧さ回避テンプレート \*/ .dablink {

`   margin: 0.5em 0;`
`   padding: 3px 2em;`
`   background-color: transparent;`
`   border-bottom: 1px solid #a2a9b1;`
`   font-size: 90%;`

}

/\* どの見出しレベルまで目次に表示するかを制限します。例えば、

<div class="toclimit-3">

とすると

`    ==headings== と ===headings=== が目次に反映され、これより下の見出しレベルは無視されます。*/`

.toclimit-2 .toclevel-2 {display: none;} .toclimit-3 .toclevel-3 {display: none;} .toclimit-4 .toclevel-4 {display: none;} .toclimit-5 .toclevel-5 {display: none;} .toclimit-6 .toclevel-6 {display: none;} .toclimit-7 .toclevel-7 {display: none;}

/\* 特定場所での改行を防ぐ:

`  1) 個別に指定した場所`
`  2) リンク途中`
`  3) そのページ自身へのリンク（太字部分）`
`  4) グループ名付きの ref タグ `<ref group="注">` --> "[注 1]" */`

.nowrap, .nowraplinks a, .nowraplinks .selflink, sup.reference a {

`   white-space: nowrap;`

} /\* 以下のクラスを指定した場所では解除する: \*/ .wrap, .wraplinks a {

`   white-space: normal;`

}

/\* For template documentation \*/ /\* TemplateStyles \*/ .template-documentation {

`   clear: both;`
`   margin: 1em 0 0 0;`
`   border: 1px solid #a2a9b1;`
`   background-color: #ecfcf4;`
`   padding: 1em;`

}

/\* Geographical coordinates defaults.

`  See `[`Template:Coord/link`](https://ja.wikipedia.org/wiki/Template:Coord/link "wikilink")` for how these are used. `
`  The classes "geo", "longitude", and "latitude" are used by `
`  the `[`Geo``   ``microformat`](https://ja.wikipedia.org/wiki/Geo_microformat "wikilink")`, so the names should not be changed. */`

.geo-default, .geo-dms, .geo-dec {

`   display: inline;`

}

.geo-nondefault, .geo-multi-punct {

`   display: none;`

}

.longitude, .latitude {

`   white-space: nowrap;`

}

/\*

`* ``の下線部を標準的なディスプレイで表示したときのみ表示されるようにするクラス。`
`* 2009-01-03 by `[`User:mizusumashi`](https://ja.wikipedia.org/wiki/User:mizusumashi "wikilink")
`*/`

@media screen {

`   .fix-domain {`
`       border-bottom:dashed 1px;`
`   }`

}

/\*

`* カテゴリページのリスト部にフロート指定のブロックを入れない。`
`* 2009-01-24 by `[`User:mizusumashi`](https://ja.wikipedia.org/wiki/User:mizusumashi "wikilink")
`*/`

1.  mw-subcategories, \#mw-pages, \#mw-category-media {

`   clear: both;`

}

/\*

`* Content in columns with CSS instead of tables `[`Template:Columns`](https://ja.wikipedia.org/wiki/Template:Columns "wikilink")
`* 2009-02-10 by `[`User:mizusumashi`](https://ja.wikipedia.org/wiki/User:mizusumashi "wikilink")
`*/`

div.columns-2 div.column {

`   float: left;`
`   width: 50%;`
`   min-width: 300px;`

} div.columns-3 div.column {

`   float: left;`
`   width: 33.3%;`
`   min-width: 200px;`

} div.columns-4 div.column {

`   float: left;`
`   width: 25%;`
`   min-width: 150px;`

} div.columns-5 div.column {

`   float: left;`
`   width: 20%;`
`   min-width: 120px;`

}

/\* Don't display page title on the main page \*/ body.page-メインページ \#siteSub, body.page-メインページ .subtitle, body.page-メインページ h1.firstHeading, body.page-メインページ h1.pagetitle {

`   display: none;`

}

/\* Common.js の LinkFA() を参照 \*/

1.  p-lang li.FA {

`   list-style-image: url("//upload.wikimedia.org/wikipedia/commons/d/d0/Monobook-bullet-star-transparent.png");`

}

/\* Common.js の LinkGA() を参照 \*/

1.  p-lang li.GA {

`   list-style-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Blue_star_boxed.svg/9px-Blue_star_boxed.svg.png");`

}

/\* [<File:Wikipedia-logo-v2-200px-transparent.png>](https://ja.wikipedia.org/wiki/File:Wikipedia-logo-v2-200px-transparent.png "fig:File:Wikipedia-logo-v2-200px-transparent.png")を背景画像として適用する（2013年版メインページなどで使用） \*/ .globegris {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/1/10/Wikipedia-logo-v2-200px-transparent.png");`

}

/\* 上付き脚注番号への太字適用を取り消し \*/ sup.reference {

`   font-weight: normal;`

}

/\* Unbulleted lists \*/ .plainlist ol, .plainlist ul {

`   line-height: inherit;`
`   list-style: none none;`
`   margin: 0;`

} .plainlist ol li, .plainlist ul li {

`   margin-bottom: 0;`

}

/\* [Template:Asbox](https://ja.wikipedia.org/wiki/Template:Asbox "wikilink")用のスタイル \*/ .asbox {

`   border: solid #999 1px;`
`   background: #F8F8F8;`
`   margin: 0.5em 10%;`
`   clear: both;`

}

/\* [Template:Math](https://ja.wikipedia.org/wiki/Template:Math "wikilink") 用の texhtml クラス。(2016-06-07) \*/

/\* Generic class for Times-based serif, texhtml class for inline math \*/ .times-serif, span.texhtml {

`   font-family: "Nimbus Roman No9 L", "Times New Roman", Times, serif;`
`   font-size: 108%;`
`   line-height: 1;`

} span.texhtml {

`   white-space: nowrap;`

} span.texhtml span.texhtml {

`   font-size: 100%;`

} span.mwe-math-mathml-inline {

`   font-size: 108%;`

}

/\* Force tabular and lining display for digits and texhtml \*/ .digits, .texhtml {

`   -moz-font-feature-settings: "lnum", "tnum", "kern" 0;`
`   -webkit-font-feature-settings: "lnum", "tnum", "kern" 0;`
`   font-feature-settings: "lnum", "tnum", "kern" 0;`
`   font-variant-numeric: lining-nums tabular-nums;`
`   font-kerning: none;`

}

/\* 日本語版追加分 \*/ span.texhtml sup {

` vertical-align: 1.0ex;`
` font-size: 75%;`

} span.texhtml sub {

` vertical-align: -0.5ex;`
` font-size: 75%;`

}

/\* MediaWiki:Common.js - modifyEditsection

`  拡張節編集リンク内の分割線をビジュアルエディター無効でも表示する */`

.ve-not-available .editsection-extensions .mw-editsection-divider {

`   display: inline;`

}

/\* ウォッチリストや最近の更新において「略語のリスト」が本文と重なる問題の解消 \*/ .mw-changeslist \> .mw-changeslist-legend.mw-enhanced {

`   position: relative;`

}