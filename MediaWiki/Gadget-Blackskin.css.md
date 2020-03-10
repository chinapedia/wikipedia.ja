> この記事は[MediaWiki:Gadget-Blackskin.css](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-Blackskin.css)から翻訳されています。


/\* 背景色・文字色 \*/ body, \#mw-page-base, \#content, \#footer, \#mw-head, .vectorTabs, .vectorTabs span, .pBody, \#p-cactions, \#p-cactions :not(h3) a, .uls-menu::before, .uls-menu div, input:not(\#searchButton), textarea, button:not(.mw-ui-button), select, fieldset, .oo-ui-popupWidget-popup, .mw-ui-button:not(.mw-interlanguage-selector), .mw-echo-ui-toggleReadCircleButtonWidget-circle-unread {

`   background: #000 !important;`

}

1.  searchButton, .mw-ui-button {

`   background-color: #000 !important;`

}

1.  content div:not(.mw-echo-ui-toggleReadCircleButtonWidget-circle), \#toc, \#filetoc,

table, caption, tr, th, td, blockquote, dl, dt, dd, .navbar span, .collapseButton a, .oo-ui-widget:not(.oo-ui-iconElement-icon), .oo-ui-widget :not(.oo-ui-iconElement-icon):not(.oo-ui-popupWidget-popup):not(.mw-echo-ui-toggleReadCircleButtonWidget-circle):not(.oo-ui-indicator-down):not(:empty):not(:hover),

1.  coordinates,

.editOptions,

1.  wikiEditor-ui-toolbar, \#wikiEditor-ui-toolbar :not(a) {

`   background: inherit !important;`

}

1.  p-personal li \> a {

`   color: #ff0 !important;`

}

1.  p-personal li \> a:hover,

.oo-ui-buttonElement-button:hover, .oo-ui-buttonElement-button:hover :not(.oo-ui-iconElement-icon), .oo-ui-buttonElement-button .mw-echo-ui-toggleReadCircleButtonWidget-circle:not(.mw-echo-ui-toggleReadCircleButtonWidget-circle-unread) {

`   background: #660 !important;`

}

body, \#content, .tocnumber,

1.  footer, \#footer li,

.vectorTabs span a, .vectorMenu span, .vectorMenu a, label, .oo-ui-widget, .oo-ui-widget \*, h1, h2, h3, h4, h5, h6, p, dt, dd, cite, caption, th, td,

1.  wikiEditor-ui-toolbar \*,

.search-types .current a, .results-info {

`   color: #0d0 !important;`

}

input, textarea, button, .mw-ui-button, select {

`   color: #9f9 !important;`

}

pre {

`   background: #010;`
`   color: #fff;`

} code {

`   background: #040;`
`   color: #0f0;`

}

.not-patrolled {

`   background: #040;`

}

.uls-menu div ul li:hover {

`   background: #020;`
`   border-radius: .5em;`

}

.ui-widget, .ui-widget \* {

`   background: #000;`
`   color: #0d0;`

}

/\* Reference Tooltip \*/ .referencetooltip li {

`   background: #000;`

} .referencetooltip li::after {

`   border-top-color: #000 !important;`

}

/\* 数式 \*/ .mwe-math-element {

`   -moz-filter: invert(100%);`
`   -webkit-filter: invert(100%);`
`   filter: invert(100%);`

}

/\* リンク色 \*/ a {

`   color: #77f;`

} a:visited {

`   color: #99d;`

} a:active, a.new {

`   color: #f44;`

}

1.  content a.interwiki, \#content a.external, \#content .extiw {

`   color: #5386db;`

} a.stub {

`   color: #974253;`

}

1.  p-cactions li \> a {

`   color: #77f;`

}

1.  p-cactions li \> .new a {

`   color: #b00;`

}

1.  mw-panel a {

`   color: #39f !important;`

}

.collapseButton a {

`   color: #77f !important;`

} .collapseButton a:active {

`   color: #f44 !important;`

}

.portlet {

`   background: #040 !important;`
`   color: #0d0;`

}

/\* ボーダー色 \*/ div, pre, table, tbody th, tbody td, fieldset, button, input, h1, h2, input, textarea, button, select {

`   border-color: #080 !important;`

} hr {

`   border-color: #080 !important;`
`   background-color: #080 !important;`
`   color: #080 !important;`

} .vectorTabs span, .vectorMenu {

`   border-left: 1px solid #080 !important;`
`   border-right: 1px solid #080;`

} .vectorTabs li:not(.selected), .vectorMenu {

`   border-bottom: 1px solid;`

} .portal {

`   border-top: 1px solid;`
`   background: none !important;`

} .uls-menu::before {

`   border-top: 1px solid #040;`
`   border-left: 1px solid #040;`

}

/\* メインページ \*/ .globegris {

`   background: url(//upload.wikimedia.org/wikipedia/commons/1/10/Wikipedia-logo-v2-200px-transparent.png) -40px -15px no-repeat !important;`

} img\[src\*="Blue-bg_rounded_cropped.svg"\] {

`   display: none;`

} .page-メインページ td:empty {

`   border-color: transparent !important;`

}

/\* ウィキペディアロゴ \*/

1.  p-logo {

`   background: url("//upload.wikimedia.org/wikipedia/ja/6/6e/WikiGreen.png") 8px 0px no-repeat !important;`
`   overflow: hidden;`

}

1.  p-logo a {

`   background: url("//upload.wikimedia.org/wikipedia/commons/c/ce/Transparent.gif") no-repeat !important;`
`   display: block;`
`   width: 154px;`
`   height: 155px;`

}

1.  p-logo a:hover {

`   position: absolute;`
`   top: 0;`
`   left: 0;`
`   width: 154px;`
`   height: 155px;`

}

/\* 履歴表示 \*/

1.  pagehistory li {

`   border: none;`

}

1.  pagehistory li.selected {

`   background: inherit;`
`   border: 1px dashed #080;`

} .mw-plusminus-pos {

`   color: #4b8;`

} .mw-plusminus-neg {

`   color: #e79;`

}

/\* 差分表示 \*/ .diff-addedline, .diff-deletedline {

`   color: #0c0 !important;`
`   background: #010 !important;`
`   font-size: smaller;`

} .diff-context {

`   font-size: smaller;`

} .diffchange {

`   color: #040 !important;`
`   font-weight: bold;`

}

/\* navbox \*/ .navbox-title {

`   border-top: 1px solid;`
`   border-bottom: 1px solid;`

} .navbox-group {

`   border-right: 1px solid;`

}

/\* infobox \*/ .infobox tr:not(:first-child) th:only-child {

`   border-top: 1px solid;`

}

/\* tracklist \*/ .tracklist {

`   border: 1px solid;`

} .tracklist tr:last-child div {

`   outline: none !important;`

}

/\* template category \*/ .ns-14 .cmbox tr {

`   background: inherit !important;`

}

/\* ウィジェットアイコン \*/ .vectorMenu h3 a {

`   background: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22UTF-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2222%22%20height%3d%2216%22%3e%3cpath%20d%3d%22M15.502%206.001l-5%205.001-5-5.001z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e) 100% 70% no-repeat !important;`

}

1.  p-personal li .mw-echo-notifications-badge-all-read {

`   color: transparent !important;`

}

1.  pt-notifications-alert .mw-echo-notifications-badge:before {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M17.5%2014V9c0-3-2.3-5-5.5-5S6.5%206%206.5%209v5c0%202%200%203-2%203v1h15v-1c-2%200-2-1-2-3zM12%2020H9c0%201%201.6%202%203%202s3-1%203-2h-3z%22%20fill%3d%22%23ff0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-bell, .mw-ui-icon-bell:before {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M17.5%2014V9c0-3-2.3-5-5.5-5S6.5%206%206.5%209v5c0%202%200%203-2%203v1h15v-1c-2%200-2-1-2-3zM12%2020H9c0%201%201.6%202%203%202s3-1%203-2h-3z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

}

1.  pt-notifications-notice .mw-echo-notifications-badge:before {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M3%2013.35l1.8-7.2c.2-.996.81-1.8%201.8-1.8h10.8c.99%200%201.6.867%201.8%201.8l1.8%207.2v4.5c0%20.99-.81%201.8-1.8%201.8H4.8c-.99%200-1.8-.81-1.8-1.8v-4.5zm6.96%201.8h4.08c-.49.557-1.212.9-2.04.9a2.68%202.68%200%200%201-2.04-.9h4.08c.414-.472.66-1.098.66-1.8h4.14l-1.44-7.2H6.6l-1.44%207.2H9.3c0%20.702.246%201.328.66%201.8z%22%20fill%3d%22%23ff0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-tray {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M3%2013.35l1.8-7.2c.2-.996.81-1.8%201.8-1.8h10.8c.99%200%201.6.867%201.8%201.8l1.8%207.2v4.5c0%20.99-.81%201.8-1.8%201.8H4.8c-.99%200-1.8-.81-1.8-1.8v-4.5zm6.96%201.8h4.08c-.49.557-1.212.9-2.04.9a2.68%202.68%200%200%201-2.04-.9h4.08c.414-.472.66-1.098.66-1.8h4.14l-1.44-7.2H6.6l-1.44%207.2H9.3c0%20.702.246%201.328.66%201.8z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

}

.oo-ui-icon-previous {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cg%20id%3d%22move-rtl%22%3e%3cpath%20id%3d%22arrow%22%20d%3d%22M15.065%2017.786l-5.302-5.303%205.302-5.302-1.415-1.41-6.714%206.72%206.714%206.71z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fg%3e%3c%2fsvg%3e);`

} .oo-ui-icon-next {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cg%20id%3d%22move-ltr%22%3e%3cpath%20id%3d%22arrow%22%20d%3d%22M8.935%207.18l5.302%205.303-5.302%205.303L10.35%2019.2l6.715-6.717-6.716-6.716z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fg%3e%3c%2fsvg%3e);`

}

.oo-ui-icon-advanced {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M20%2013.44v-2.88l-1.8-.3c-.1-.397-.3-.794-.6-1.39l1.1-1.49-2.1-2.088-1.5%201.093c-.5-.298-1-.497-1.4-.596L13.5%204h-2.9l-.3%201.79c-.5.098-.9.297-1.4.595L7.4%205.292%205.3%207.38l1%201.49c-.3.496-.4.894-.6%201.39l-1.7.2v2.882l1.8.298c.1.497.3.894.6%201.39l-1%201.492%202.1%202.087%201.5-1c.4.2.9.395%201.4.594l.3%201.79h3l.3-1.79c.5-.1.9-.298%201.4-.596l1.5%201.092%202.1-2.08-1.1-1.49c.3-.496.5-.993.6-1.39l1.5-.3zm-8%201.492c-1.7%200-3-1.292-3-2.982%200-1.69%201.3-2.98%203-2.98s3%201.29%203%202.98-1.3%202.982-3%202.982z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-indicator-down {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2212%22%20height%3d%2212%22%20viewBox%3d%220%200%2012%2012%22%3e%3cg%20id%3d%22down%22%3e%3cpath%20id%3d%22arrow%22%20d%3d%22M1%204h10L6%209%201%204%22%20fill%3d%22%230d0%22%2f%3e%3c%2fg%3e%3c%2fsvg%3e);`

}

.oo-ui-icon-doubleCheck {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M17%209.5L9.5%2017%206%2013.5%204.5%2015l5%205L20%209.5c-.706-.706-2.294-.706-3%200z%22%20fill%3d%22%230d0%22%2f%3e%3cpath%20d%3d%22M17%204.5L9.5%2012%206%208.5%204.5%2010l5%205L20%204.5c-.706-.706-2.294-.706-3%200z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-help {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cg%20id%3d%22help%22%3e%3cpath%20id%3d%22circle%22%20d%3d%22M12%202.085c-5.477%200-9.915%204.438-9.915%209.916%200%205.48%204.438%209.92%209.916%209.92%205.48%200%209.92-4.44%209.92-9.913%200-5.477-4.44-9.915-9.913-9.915zm.002%2018a8.084%208.084%200%201%201%200-16.168%208.084%208.084%200%200%201%200%2016.168z%22%20fill%3d%22%230d0%22%2f%3e%3cg%20id%3d%22question-mark%22%3e%3cpath%20id%3d%22top%22%20d%3d%22M11.766%206.688c-2.5%200-3.22%202.188-3.22%202.188l1.412.854s.298-.79.9-1.23c.517-.374%201.626-.624%202.22.126.7.885-.17%201.587-1.078%202.72C11.047%2012.53%2011%2015%2011%2015h1.97s.134-2.318%201.04-3.38c.603-.708%201.443-1.34%201.443-2.495s-1.187-2.437-3.687-2.437z%22%20fill%3d%22%230d0%22%2f%3e%3cpath%20id%3d%22bottom%22%20d%3d%22M11%2016h2v2h-2z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fg%3e%3c%2fg%3e%3c%2fsvg%3e);`

}

.oo-ui-icon-userAvatar {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M18.75%2017.4c-1.08-.36-3.6-1.35-3.6-1.35-.81-.27-.81-.99-.9-1.8v-.09c1.26-1.08%202.25-2.88%202.25-4.86%200-4.23-1.8-5.85-4.5-5.85-1.89%200-4.5%201.08-4.5%205.85%200%201.89.99%203.69%202.25%204.86v.09c0%20.81-.09%201.53-.9%201.8%200%200-2.61.99-3.6%201.35-1.17.36-2.25.9-2.25%202.25v.9h18v-.9c0-1.08-.72-1.8-2.25-2.25z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-changes {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M1.6%204h18.72v2H3.68v12H1.6V4zm20.8%202.998V20H4.72V6.998H22.4z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-article {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M12%2010h4V5h-4v5zm-5%202h9v-1H7v1zm0%202h9v-1H7v1zm0%202h9v-1H7v1zm4-9H7v1h4V7zm0%202H7v1h4V9zm0-4H7v1h4V5zM5%203h13v16H8c-1.7%200-3-1.3-3-3V3z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-speechBubbles {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22utf-8%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M20%209v9l2%202H8V9h12zM3%204h12v4H7v7H1l2-2V4z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

} .oo-ui-icon-userSpeechBubble {

`   background-image: url(data:image/svg+xml,%3c%3fxml%20version%3d%221.0%22%20encoding%3d%22UTF-8%22%20standalone%3d%22no%22%3f%3e%3csvg%20xmlns%3d%22http%3a%2f%2fwww.w3.org%2f2000%2fsvg%22%20width%3d%2224%22%20height%3d%2224%22%20viewBox%3d%220%200%2024%2024%22%3e%3cpath%20d%3d%22M14%2016.8c-.96-.32-3.2-1.2-3.2-1.2-.72-.24-.72-.88-.8-1.6v-.08c1.12-.96%202-2.56%202-4.32%200-3.76-1.6-5.2-4-5.2-1.68%200-4%20.96-4%205.2%200%201.68.88%203.28%202%204.32V14c0%20.72-.08%201.36-.8%201.6%200%200-2.32.88-3.2%201.2-1.04.32-2%20.8-2%202v.8h16v-.8c0-.96-.64-1.6-2-2zm.367-5.46l-1.796%202.938H24V4.4h-9.633v6.94z%22%20fill%3d%22%230d0%22%2f%3e%3c%2fsvg%3e);`

}