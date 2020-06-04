> この記事は[MediaWiki:Gadget-charinsert-core.js](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-charinsert-core.js)から翻訳されています。


/\*\*

`* Copied from `[`mw:User:Alex``   ``Smotrov/edittools.js`](https://ja.wikipedia.org/wiki/mw:User:Alex_Smotrov/edittools.js "wikilink")`, modified for use on the English Wikipedia.`
`*`
`* Configuration (to be set from `[`Special:MyPage/common.js`](https://ja.wikipedia.org/wiki/Special:MyPage/common.js "wikilink")`):`
`*   window.charinsertCustom – Object. Merged into the default charinsert list. For example, setting`
`*       this to { Symbols: '‽' } will add the interrobang to the end of the Symbols section.`
`*   window.editToolsRecall – Boolean. Set true to create a recall switch.`
`*   window.charinsertDontMove – Boolean. Set true to leave the box in its default position, rather`
`*       than moving it above the edit summary.`
`*   window.updateEditTools() – Function. Call after updating window.charinsertCustom to regenerate the`
`*       EditTools window.`
`*/`

/\* global jQuery, mw, charinsertCustom \*/

window.updateEditTools = function () { };

jQuery( document ).ready( function ( $ ) {

`   var $currentFocused,`
`       editTools;`

`   function getSelectedSection() {`
`       var selectedSection = mw.storage.get( editTools.storageKey )`
`           || mw.storage.session.get( editTools.storageKey );`
`       `
`       return selectedSection;`
`   }`
`   `
`   function saveSelectedSection( newIndex ) {`
`       mw.storage.set( editTools.storageKey, newIndex )`
`           || mw.storage.session.set( editTools.storageKey, newIndex );`
`   }`
`   `
`   editTools = {`
`       // Entries prefixed with ␥ (U+2425 SYMBOL FOR DELETE FORM TWO) will not appear in the article namespace (namespace 0).`
`       // Please make any changes to `[`MediaWiki:Edittools`](../MediaWiki/Edittools.md "wikilink")` as well, however, instead of using the ␥ symbol, use {{#ifeq:``|``| | }}.`
`       charinsert: {`
`           '挿入': ' – — ° ′ ″ ≈ ≠ ≤ ≥ ± − × ÷ ← → ・ §  ␥署名する: ␥--~~\~~  出典を明記する: `\[1\]`',`
`           'マークアップ': '記号:  – — ° ′ ″ ≈ ≠ ≤ ≥ ± − × ÷ ← → ・ § ␥--~~\~~ `\[2\]`  マークアップ:  {\{+}}  {\{\{+}}}  |  [+]  [\[+]]  [\[Category:+]]  #REDIRECT.[\[+]]     `<s>`+`</s>`  `<sup>`+`</sup>`  `<sub>`+`</sub>`  +  `

```
+
```

> \+

\<ref.name="+"_/\> {\\{\#tag:ref|+|group="注釈"|name=""}} {\\{Reflist}} \<references./\> <includeonly>+</includeonly> <noinclude>+</noinclude> {\\{DEFAULTSORT:+}} + \<span.class="plainlinks"\>+</span>',

`           '記号': '~ | ¡¿†‡↔↑↓•¶#∞  ‘+’ “+” ‹+› «+» {\{angle.bracket|+}}  ¤₳฿₵¢₡₢$₫₯€₠₣ƒ₴₭₤ℳ₥₦№₧₰£៛₨₪৳₮₩¥  ♠♣♥♦  ♭♯♮  ©®™ ◌',`
`           'ラテン文字': 'A a Á á À à Â â Ä ä Ǎ ǎ Ă ă Ā ā Ã ã Å å Ą ą Æ æ Ǣ ǣ  B b  C c Ć ć Ċ ċ Ĉ ĉ Č č Ç ç  D d Ď ď Đ đ Ḍ ḍ Ð ð  E e É é È è Ė ė Ê ê Ë ë Ě ě Ĕ ĕ Ē ē Ẽ ẽ Ę ę Ẹ ẹ Ɛ ɛ Ǝ ǝ Ə ə  F f  G g Ġ ġ Ĝ ĝ Ğ ğ Ģ ģ  H h Ĥ ĥ Ħ ħ Ḥ ḥ  I i İ ı Í í Ì ì Î î Ï ï Ǐ ǐ Ĭ ĭ Ī ī Ĩ ĩ Į į Ị ị  J j Ĵ ĵ  K k Ķ ķ  L l Ĺ ĺ Ŀ ŀ Ľ ľ Ļ ļ Ł ł Ḷ ḷ Ḹ ḹ  M m Ṃ ṃ  N n Ń ń Ň ň Ñ ñ Ņ ņ Ṇ ṇ Ŋ ŋ  O o Ó ó Ò ò Ô ô Ö ö Ǒ ǒ Ŏ ŏ Ō ō Õ õ Ǫ ǫ Ọ ọ Ő ő Ø ø Œ œ  Ɔ ɔ  P p  Q q  R r Ŕ ŕ Ř ř Ŗ ŗ Ṛ ṛ Ṝ ṝ  S s Ś ś Ŝ ŝ Š š Ş ş Ș ș Ṣ ṣ ß  T t Ť ť Ţ ţ Ț ț Ṭ ṭ Þ þ  U u Ú ú Ù ù Û û Ü ü Ǔ ǔ Ŭ ŭ Ū ū Ũ ũ Ů ů Ų ų Ụ ụ Ű ű Ǘ ǘ Ǜ ǜ Ǚ ǚ Ǖ ǖ  V v  W w Ŵ ŵ  X x  Y y Ý ý Ŷ ŷ Ÿ ÿ Ỹ ỹ Ȳ ȳ  Z z Ź ź Ż ż Ž ž  ß Ð ð Þ þ Ŋ ŋ Ə ə Ɂ ɂ  Ꞌ ꞌ  ʻ  ʼ  ʽ  ꞉ ꞏ',   `
`           'ギリシャ文字': 'ΆάΈέΉήΊίΌόΎύΏώ  ΑαΒβΓγΔδ  ΕεΖζΗηΘθ  ΙιΚκΛλΜμ  ΝνΞξΟοΠπ  ΡρΣσςΤτΥυ  ΦφΧχΨψΩω Ϝϝυ̯ι̯  ᾼᾳᾴᾺὰᾲᾶᾷἈἀᾈᾀἉἁᾉᾁἌἄᾌᾄἊἂᾊᾂἎἆᾎᾆἍἅᾍᾅἋἃᾋᾃἏἇᾏᾇ  ῈὲἘἐἙἑἜἔἚἒἝἕἛἓ  ῌῃῄῊὴῂῆῇἨἠᾘᾐἩἡᾙᾑἬἤᾜᾔἪἢᾚᾒἮἦᾞᾖἭἥᾝᾕἫἣᾛᾓἯἧᾟᾗ  ῚὶῖἸἰἹἱἼἴἺἲἾἶἽἵἻἳἿἷΪϊΐῒῗ  ῸὸὈὀὉὁὌὄὊὂὍὅὋὃ  ῤῬῥ  ῪὺῦὐὙὑὔὒὖὝὕὛὓὟὗΫϋΰῢῧ  ῼῳῴῺὼῲῶῷὨὠᾨᾠὩὡᾩᾡὬὤᾬᾤὪὢᾪᾢὮὦᾮᾦὭὥᾭᾥὫὣᾫᾣὯὧᾯᾧ ᾹᾱᾸᾰῙῑῘῐῩῡῨῠ `` ``',`
`           'キリル文字': 'АаБбВвГг  ҐґЃѓДдЂђ  ЕеЁёЄєЖж  ЗзЅѕИиІі  ЇїЙйЈјКк  ЌќЛлЉљМм  НнЊњОоПп  РрСсТтЋћ  УуЎўФфХх  ЦцЧчЏџШш  ЩщЪъЫыЬь  ЭэЮюЯя ӘәӨөҒғҖҗ ҚқҜҝҢңҮү ҰұҲҳҸҹҺһ  ҔҕӢӣӮӯҘҙ  ҠҡҤҥҪҫӐӑ  ӒӓӔӕӖӗӰӱ  ӲӳӸӹӀ  ҞҟҦҧҨҩҬҭ  ҴҵҶҷҼҽҾҿ  ӁӂӃӄӇӈӋӌ  ӚӛӜӝӞӟӠӡ  ӤӥӦӧӪӫӴӵ  ́',`
`           'ヘブライ文字': 'אבגדהוזחטיכךלמםנןסעפףצץקרשת  ׳ ״  װױײ',`
`           'アラビア文字': '  転写: ʾ  ā ī ū ṯ ḥ ḫ ẖ ḏ š ṣ ḍ ṭ ẓ ʿ ġ ẗ á ا ﺁ ب ت ث ج ح خ د ذ ر ز س ش ص ض ط ظ ع غ ف ق ك ل م ن ه ة و ي ى ء أ إ ؤ ئ',`
`           'IPA（英語）': 'ˈ ˌ  ŋ ɡ tʃ dʒ ʃ ʒ θ ð ʔ  ɑː ɒ æ aɪ aʊ ɛ ɛər+ eɪ ɪ ɪər+ iː ɔː ɔɪ oʊ ʊ ʊər+ uː ʌ ɜːr+  ə ər  ɒ̃ æ̃  {\{IPAc-en|+}} {\{IPA|+}} {\{angle.bracket|+}}',`
`           'IPA': '子音: ɱɳɲŋɴ : t̪ d̪ ʈɖɟɡɢʡʔ : ɸβθð  ʃʒʂʐɕʑ  çʝɣχʁ  ħʕʜʢɦɧ : ʋɹɻɥɰʍ : ʙⱱɾɽʀ  ɺ  ɫɬɮɭʎʟ : ɓɗᶑʄɠʛ  ʘǀǃǂǁ  母音: ɪʏɨʉɯʊ : øɘɵɤ  ə ɚ  ɛœɜɝɞʌɔ : æɶɐɑɒ  音声補助記号: ˈˌːˑʼˀˤᵝᵊᶢˠʰʱʲˡⁿᵑʷᶣ˞‿˕˔ ̚ ̪ ̺ ̻ ̼ ̬  ̊ ̥ ̞ ̝ ̘ ̙ ̽ ̟ ̠  ̈ ̤ ̹ ̜ ̍ ̩  ̆ ̯  ̃ ̰ ͡ ͜  アクセント:  ̋  ́  ̄  ̀  ̏  ̌  ̂ ᷄ ᷅ ᷇ ᷆ ᷈ ᷉  ˥˦˧˨˩ꜛꜜ : ↗↘‖  extIPA: ͈ ͉ ͎ ̣ ̫ ͊ ᷽ ͇ : ˭ᵻᵿ  {\{angle.bracket|+}} {\{IPA|+}} {\{IPA.link|+}}',`
`           '数学と論理記号': '− × ÷ ⋅ ° ∗ ∘ ± ∓ ≤ ≥ ≠ ≡ ≅ ≜ ≝ ≐ ≃ ≈ ⊕ ⊗ ⇐ ⇔ ⇒ ∞ ← ↔ → ≪ ≫ ∝ √ ∤ ≀ ◅ ▻ ⋉ ⋊ ⋈ ∴ ∵ ↦ ¬ ∧ ∨ ⊻ ∀ ∃ ∈ ∉ ∋ ⊆ ⊈ ⊊ ⊂ ⊄ ⊇ ⊉ ⊋ ⊃ ⊅ ∪ ∩ ∑ ∏ ∐ ′ ∫ ∬ ∭ ∮ ∇ ∂ ∆ ∅ ℂ ℍ ℕ ℙ ℚ ℝ ℤ ℵ ⌊ ⌋ ⌈ ⌉ ⊤ ⊥ ⊢ ⊣ ⊧ □ ∠ ⟨ ⟩ `\(+\)` {\{math|+}} {\{mvar|+}} {\{frac|+|}} {\{sfrac|+|}}'`
`       },`

`       charinsertDivider: "\240",`

`       storageKey: 'edittoolscharsubset',`

`       createEditTools: function ( placeholder ) {`
`           var sel, id;`
`           var box = document.createElement( 'div' );`
`           var prevSubset = 0, curSubset = 0;`
`           box.id = 'editpage-specialchars';`
`           box.className = "nopopups";`
`           box.title = '文字やマークアップをクリックすることで編集画面に追加できます';`

`           // append user-defined sets`
`           if ( window.charinsertCustom ) {`
`               for ( id in charinsertCustom ) {`
`                   if ( !editTools.charinsert[id] ) {`
`                       editTools.charinsert[id] = '';`
`                   }`
`               }`
`           }`

`           // create drop-down select`
`           sel = document.createElement( 'select' );`
`           for ( id in editTools.charinsert ) {`
`               sel.options[sel.options.length] = new Option( id, id );`
`           }`
`           sel.selectedIndex = 0;`
`           sel.style.marginRight = '.3em';`
`           sel.title = '記号の種類を選択';`
`           sel.onchange = sel.onkeyup = selectSubset;`
`           box.appendChild( sel );`

`           // create "recall" switch`
`           if ( window.editToolsRecall ) {`
`               var recall = document.createElement( 'span' );`
`               recall.appendChild( document.createTextNode( '↕' ) ); // ↔`
`               recall.onclick = function() {`
`                   sel.selectedIndex = prevSubset;`
`                   selectSubset();`
`               };`
`               recall.style.cssFloat = 'left';`
`               recall.style.marginRight = '5px';`
`               recall.style.cursor = 'pointer';`
`               box.appendChild( recall );`
`           }`

`           if ( getSelectedSection() ) {`
`               sel.selectedIndex = getSelectedSection();`
`           }`

`           placeholder.parentNode.replaceChild( box, placeholder );`
`           selectSubset();`
`           return;`

`           function selectSubset() {`
`               // remember previous (for "recall" button)`
`               prevSubset = curSubset;`
`               curSubset = sel.selectedIndex;`
`               //save into web storage for persistence`
`               saveSelectedSection( curSubset );`
`               `
`               //hide other subsets`
`               var pp = box.getElementsByTagName( 'p' ) ;`
`               for ( var i = 0; i < pp.length; i++ ) {`
`                   pp[i].style.display = 'none';`
`               }`
`               //show/create current subset`
`               var id = sel.options[curSubset].value;`
`               var p = document.getElementById( id );`
`               if ( !p ) {`
`                   p = document.createElement( 'p' );`
`                   p.className = 'nowraplinks';`
`                   p.id = id;`
`                   p.style.fontSize = '80%';`
`                   if ( id == 'アラビア文字' || id == 'ヘブライ文字' ) {`
`                       p.dir = 'rtl';`
`                   }`
`                   var tokens = editTools.charinsert[id];`
`                   if ( window.charinsertCustom && charinsertCustom[id] ) {`
`                       if ( tokens.length > 0 ) {`
`                           tokens += ' ';`
`                       }`
`                       tokens += charinsertCustom[id];`
`                   }`
`                   editTools.createTokens( p, tokens );`
`                   box.appendChild( p );`
`               }`
`               p.style.display = 'inline';`
`           }`
`       },`

`       createTokens: function ( paragraph, str ) {`
`           var tokens = str.split( ' ' ), token, i, n;`
`           for ( i = 0; i < tokens.length; i++ ) {`
`               token = tokens[i];`
`               n = token.indexOf( '+' );`
`               if ( token.charAt( 0 ) === '␥' ) {`
`                   if ( token.length > 1 && mw.config.get( 'wgNamespaceNumber' ) === 0 ) {`
`                       continue;`
`                   } else {`
`                       token = token.substring( 1 );`
`                   }`
`               }`
`               if ( token === '' || token === '_' ) {`
`                   addText( editTools.charinsertDivider + ' ' );`
`               } else if ( token === '\n' ) {`
`                   paragraph.appendChild( document.createElement( 'br' ) );`
`               } else if ( token === '___' ) {`
`                   paragraph.appendChild( document.createElement( 'hr' ) );`
`               } else if ( token.charAt( token.length-1 ) === ':' ) { // : at the end means just text`
`                   addBold( token );`
`               } else if ( n === 0 ) { // +`<tag>`  ->   `<tag>`+`</tag>
`                   addLink( token.substring( 1 ), '</' + token.substring( 2 ), token.substring( 1 ) );`
`               } else if ( n > 0 ) { // `<tag>`+`</tag>
`                   addLink( token.substring( 0, n ), token.substring( n+1 ) );`
`               } else if ( token.length > 2 && token.charCodeAt( 0 ) > 127 ) { // a string of insertable characters`
`                   for ( var j = 0; j < token.length; j++ ) {`
`                       addLink( token.charAt( j ), '' );`
`                   }`
`               } else {`
`                   addLink( token, '' );`
`               }`
`           }`
`           return;`

`           function addLink( tagOpen, tagClose, name ) {`
`               var handler;`
`               var dle = tagOpen.indexOf( '\x10' );`
`               var a = document.createElement( 'a' );`
`               `
`               if ( dle > 0 ) {`
`                   var path = tagOpen.substring( dle + 1 ).split( '.' );`
`                   tagOpen = tagOpen.substring( 0, dle );`
`                   handler = window;`
`                   for ( var i = 0; i < path.length; i++ ) {`
`                       handler = handler[path[i]];`
`                   }`
`                   $( a ).on( 'click', handler );`
`               } else {`
`                   tagOpen = tagOpen.replace( /\./g,' ' );`
`                   tagClose = tagClose ? tagClose.replace( /_/g,' ' ) : '';`
`                   $( a ).on( 'click', {`
`                       tagOpen: tagOpen,`
`                       sampleText: '',`
`                       tagClose: tagClose`
`                   }, insertTags );`
`               }`

`               name = name || tagOpen + tagClose;`
`               name = name.replace( /\\n/g,'' );`
`               a.appendChild( document.createTextNode( name ) );`
`               a.href = '';`
`               paragraph.appendChild( a );`
`               addText( ' ' );`
`           }`

`           function addBold( text ) {`
`               var b = document.createElement( 'b' );`
`               b.appendChild( document.createTextNode( text.replace( /_/g,' ' ) ) );`
`               paragraph.appendChild( b );`
`               addText( ' ' );`
`           }`
`           function addText( txt ) {`
`               paragraph.appendChild( document.createTextNode( txt ) );`
`           }`
`           function insertTags( e ) {`
`               e.preventDefault();`
`               if ( $currentFocused && $currentFocused.length && !$currentFocused.prop( 'readonly' ) ) {`
`                   $currentFocused.textSelection(`
`                       'encapsulateSelection', {`
`                           pre: e.data.tagOpen,`
`                           peri: e.data.sampleText,`
`                           post: e.data.tagClose`
`                       }`
`                   );`
`               }`
`           }`
`       },`

`       setup: function () {`
`           var placeholder;`
`           if ( $( '#editpage-specialchars' ).length ) {`
`               placeholder = $( '#editpage-specialchars' )[0];`
`           } else {`
`               placeholder = $( '`

<div id="editpage-specialchars">

</div>

' ).prependTo( '.mw-editTools' )\[0\];

`           }`
`           if ( !placeholder ) {`
`               return;`
`           }`
`           if ( !window.charinsertDontMove ) {`
`               $( '.editOptions' ).before( placeholder );`
`           }`
`           // Find the element that is focused`
`           $currentFocused = $( '#wpTextbox1' );`
`           // Apply to dynamically created textboxes as well as normal ones`
`           $( document ).on( 'focus', 'textarea, input:text', function () {`
`               $currentFocused = $( this );`
`           } );`

`           // Used to determine where to insert tags`
`           editTools.createEditTools( placeholder );`
`           window.updateEditTools = function () {`
`               editTools.createEditTools( $( '#editpage-specialchars' )[0] );`
`           };`
`       }`

`   }; // end editTools`

`   editTools.setup();`

} );

1.  `+`
2.  `+`