> この記事は[MediaWiki:Gadget-exlinks.js](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-exlinks.js)から翻訳されています。


// \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* // \*\* \*\*\*WARNING GLOBAL GADGET FILE\*\*\* \*\* // \*\* changes to this file affect many users. \*\* // \*\* please discuss on the talk page before editing \*\* // \*\* \*\* // \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* /\*\*

`* @source mediawiki.org/wiki/Snippets/Open_external_links_in_new_window`
`* @version 5`
`*/`

mw.hook('wikipage.content').add(function($content) {

`   // Second selector is for external links in Parsoid HTML+RDFa output (bug 65243).`
`   $content.find('a.external, a[rel="mw:ExtLink"]').each(function () {`
`       // Can't use wgServer because it can be protocol relative`
`       // Use this.href property instead of this.getAttribute('href')  because the property`
`       // is converted to a full URL (including protocol)`
`       if (this.href.indexOf(location.protocol + '//' + location.hostname) !== 0) {`
`           this.target = '_blank';`
`       }`
`   });`

});