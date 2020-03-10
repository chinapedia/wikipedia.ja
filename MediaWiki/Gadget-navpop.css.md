> この記事は[MediaWiki:Gadget-navpop.css](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-navpop.css)から翻訳されています。


a.popupMoreLink { display: block; text-align: right; cursor: pointer; }

ins.popupDiff { background: \#AFE; } del.popupDiff { background: \#FFE6E6; }

1.  selectionPreview { /\* overflow: auto; max-height: 16ex; \*/

`                   border: 2px solid #DDD;`
`                   background-color: #EEF;`
`                   padding: 6px;`
`                   }`

.navpopup {

` border: solid #FFBE20 1px;`
` background-color: #FFFAEF;`
` padding: 5px;`
` font-size: 8pt;`
` /* opacity: 0.9; */`

}

/\* Configure Drag bar color \*/ .popupDrag {

` background-color: #FFBE20;`
` height: 5px;`
` margin-top: -5px;`
` margin-bottom: 5px;`

}

.popupDragHandle {

`cursor: move;`
`position: relative;`

}

/\* menu magic - many thanks to [User:Zocky](https://ja.wikipedia.org/wiki/User:Zocky "wikilink")\! \*/

/\* popups \*/ .popup_menu li {

`margin: 3px;`

}

.popup_menu {

` display:none;`
` position:absolute;`
` left:0;`
` margin: 0;`
` margin-top: 1em;`
` line-height: 1.25em;`
` list-style-type: none; `
` /*top:1.6ex; */`
` z-index:2;`
` width:10em; `
` background:white; `
` border:solid 1px grey;`
` padding: 0.5em !important;`
` margin-left: -6px;`
` margin-top: 1em;`
` border-width: 1px 1px 1px 6px;`

} .popup_menu a {display:block;} .popup_menu_row a {display:inline;} .popup_menu_row { list-style: none;

`                 padding: 0;`
`                 margin: 0;`
`                 /*)border: solid 1px red;*/`
`                 }`

.popup_drop {display:inline; position:relative} .popup_drop:hover .popup_menu, .popup_drop .popup_menu:hover {display:inline; background:White; padding:2px 2px 2px 2px}

.popup_drop:hover { background:\#CCF; color:\#44f; }

/\* other colours, styles and so on \*/ .popup_menu a:hover {background:\#CCf; color:\#44f} .popup_mainlink {font-size: 140%; font-weight: bold}

.popup_change_title_link { color: \#152; }

.popup_diff_dates {

`                   font-style: italic; `
`                   background: none;`
`                   }`

.popup_menu_item {

`                 list-style: none;`
`                 padding: 0;`
`                 margin: 0;`
`                  /*border: solid 1px green;*/`

} .popup_menu_item a{ display:block; }

.popup_history_row_even { background: \#eee; } .popup_history_date { font-weight: bold; font-size: 120%; }

/\* disable interwiki styling \*/ .popupPreview a.extiw, .popupPreview a.extiw:active {

`   color: #36b;`
`   background: none;`
`   padding: 0;`

} .popupPreview a.external {

`   color: #36b;`

} /\* this can be used in the content area to switch off special external link styling \*/ .popupPreview .plainlinks a {

`   background: none !important;`
`   padding: 0 !important;`

}