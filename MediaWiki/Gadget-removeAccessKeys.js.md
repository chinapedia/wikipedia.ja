> この記事は[MediaWiki:Gadget-removeAccessKeys.js](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-removeAccessKeys.js)から翻訳されています。


// \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* // \*\* \*\*\*WARNING GLOBAL GADGET FILE\*\*\* \*\* // \*\* changes to this file affect many users. \*\* // \*\* please discuss on the talk page before editing \*\* // \*\* \*\* // \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* // Imported from version as of: 2007-04-17T22:22:27 // Deactivating access keys, see [talk page](https://ja.wikipedia.org/wiki/Wikipedia_talk:WikiProject_User_scripts/Scripts/removeAccessKeys "wikilink")

$(function(){

`   var $nodeList;`
`   if (mw.config.get('skin') === 'vector') {`
`       $nodeList = $('#mw-head a, #mw-panel a');`
`   } else {`
`       $nodeList = $('#column-one a, #mw_portlets a, #p-cactions a, #p-personal a');`
`   }`
`   $nodeList = $nodeList.add('input, label').filter(function(){`
`       return this.accessKey && (!window.removeAccessKeys || window.removeAccessKeys.indexOf(this.accessKey) !== -1);`
`   });`
`   mw.loader.using('mediawiki.util').then(function(){`
`       $nodeList.removeAttr('accesskey').updateTooltipAccessKeys();`
`   });`

});