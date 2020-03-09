> この記事は[MediaWiki:Monobook.css](https://ja.wikipedia.org/wiki/MediaWiki:Monobook.css)から翻訳されています。


/\*

``` css
 */

/*
a { text-decoration: none }
*/

/* enlarge font-size for ja fonts*/
#bodyContent { font-size:118% }

/* Donations link to be uncommented during fundraising drives */
#siteNotice {
    padding-left: 0.3em;
    font-style: normal;
    text-align: center;
    margin-top: 0.5em;
}

/*
#siteNotice {
    display:none;
    padding: 0.3em;
    margin-top:0.5em;
}
*/

/* Make all non-namespace pages have a light blue content area. This is done by
   setting the background color for all #content areas to light blue and then
   overriding it for any #content enclosed in a .ns-0 (main namespace). I then
   do the same for the "tab" background colors. --Lupo */

#content {
    background: #FBFCFF; /* a light blue ja*/
}

.ns-0 * #content {
    background: white;
}

#mytabs li {
    background: #FBFCFF;
}

.ns-0 * #mytabs li {
    background: white;
}

#mytabs li a {
    background-color: #FBFCFF;
}

.ns-0 * #mytabs li a {
    background-color: white;
}

#p-cactions li {
    background: #FBFCFF;
}

.ns-0 * #p-cactions li {
    background: white;
}

#p-cactions li a {
    background-color: #FBFCFF;
}

.ns-0 * #p-cactions li a {
    background-color: white;
}

/* "出典: フリー百科事典『ウィキペディア（Wikipedia）』" */
#siteSub {
    display: inline;
    font-size: 98%;
    font-weight: normal;
}

#bodyContent #siteSub a {
    color: #000;
    text-decoration: none;
    background-color: transparent;
    background-image: none;
    padding-right: 0;
}

/* link color stub sleshold (ja only from MediaWiki1.2) */
#stub{
    color:#6699FF
}

/* Bold 'edit this page' link to encourage newcomers */
#ca-edit a { font-weight: bold !important; }

/* Display "User $1, you are already logged in!"
   ([[MediaWiki:Alreadyloggedin|MediaWiki:Alreadyloggedin]]) in red and bold */
div.alreadyloggedin { color: red; font-weight: bold; }

/* Standard Navigationsleisten, aka box hiding thingy from .de.*/
/* NavFrame関係。[[MediaWiki:Common.css|MediaWiki:Common.css]]も参照 */
a.NavToggle {
 font-size:83.3%;
}

/*p { font-family: "ＭＳ ゴシック" ,"Osaka-等幅" ,"Times New Roman" ,serif; }*/

/* 脚注挿入による行間のずれを軽減する。[[MediaWiki‐ノート:Common.css#脚注による行間のずれ|MediaWiki‐ノート:Common.css#脚注による行間のずれ]] */
sup {
  font-size:.85em;
  vertical-align:.4em;
  line-height: 0;
}

#coordinates {
    position: absolute;
    z-index: 10;
    background-color: #fff;
    right: 0;
    top: 0;
    font-size: 85%;
}
#bodyContent {
    position: relative;
    width: 100%; /* IE6でスクロールがもたつく問題への暫定対処 */
}
.topicon {
    position: absolute;
    z-index: 10;
    right: 0;
    top: -30px;
    display: block !important;
}
/*
coord系テンプレートに、id="coordinates" を付け、テンプレートからは全てのCSSを除去。
[[Template:Featured_article|Template:Featured article]]に class="metadata topicon" style="display:none" を付け、残りのCSSは全て除去する。
*/

/*
```

\*/