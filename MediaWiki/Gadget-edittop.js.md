> この記事は[MediaWiki:Gadget-edittop.js](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-edittop.js)から翻訳されています。


// \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* // \*\* \*\*\*WARNING GLOBAL GADGET FILE\*\*\* \*\* // \*\* changes to this file affect many users. \*\* // \*\* please discuss on the talk page before editing \*\* // \*\* \*\* // \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* // Imported from [User:Alex Smotrov/edittop.js](https://ja.wikipedia.org/wiki/User:Alex_Smotrov/edittop.js "wikilink"), version as of: 2007-06-19T04:28:52 // Updated from [User:TheDJ/Gadget-edittop.js](https://ja.wikipedia.org/wiki/User:TheDJ/Gadget-edittop.js "wikilink"), version as of: 2009-04-28T11:54:22

if ($.inArray( mw.config.get('wgAction'), \[ 'view', 'purge' \]) \!== -1 && mw.config.get( 'wgNamespaceNumber' ) \>=0) {

` $(function edittop_hook () {`
`   var localtitles = {`
`     cs: 'Editovat úvodní sekci',`
`     en: 'Edit lead section',`
`     fa: 'ویرایش بخش آغازین',`
`     fr: 'Modifier le résumé introductif',`
`     id: 'Sunting bagian atas',`
`     it: 'Modifica della sezione iniziale',`
`     ja: '導入部を編集',`
`     min: 'Suntiang bagian ateh',`
`     ko: '도입부를 편집',`
`     pa: 'ਸੋਧ',`
`     pt: 'Editar a seção superior',`
`     'pt-br': 'Editar a seção superior',`
`     sr: 'Уреди уводни део',`
`     vi: 'Sửa phần mở đầu'`
`   };`

`   var our_content = $("#content, #mw_content").first();`
`   var span1 = our_content.find("span.mw-editsection:not(.plainlinks)").first();`
`   if (!span1.length) {`
`     return;`
`   }`
`   var span0 = span1.clone();`
`   // （暫定措置）MediaWiki:Common.js modifyEditsectionで追加された拡張リンクを除去`
`   span0.find('.editsection-extensions').remove();`

`   if ( mw.user.options.get( 'gadget-righteditlinks' ) == 1 ) {`
`     var editwidth = span1.outerWidth() + (mw.config.get("skin") == "monobook" ? 10 : 0);`
`     $("div.topicon, #mw-fr-revisiontag").css("margin-right", editwidth + "px");`
`   }`
`   $("#mw_header h1, #content h1").first().append(span0);`
`   span0.find("a").each(function (idx) {`
`     var a = $(this);`
`     a.attr("title", localtitles[mw.config.get( 'wgUserLanguage' )] || localtitles.en);`
`     if (a.attr("href").indexOf("&section=T") == -1) {`
`       a.attr("href", a.attr("href").replace(/&section=\d+/, "&section=0&summary=/*%20top%20*/%20"));`
`     }`
`     else { //transcluded`
`       a.attr("href", mw.util.getUrl( mw.config.get( 'wgPageName' ) ) + "?action=edit&section=0&summary=/*%20top%20*/%20");`
`     }`
`   });`
` });`

}