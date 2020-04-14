> この記事は[モジュール:Twitch](https://ja.wikipedia.org/wiki/モジュール:Twitch)から翻訳されています。


local p = {};

local function getWikidataProperty(property, from )

`   local entity = nil;`
`   if from == '' then`
`       entity = mw.wikibase.getEntityObject( );`
`   else`
`       entity = mw.wikibase.getEntityObject(from);`
`   end`
`   if not entity then`
`       return nil;`
`   end`
`   local claims = entity.claims or {};`
`   local hasProp = claims[property];`
`   if not hasProp then`
`       return nil;`
`   end`
`   return hasProp[1].mainsnak.datavalue.value;`

end

function p.main( frame )

`   local args = require( 'Module:Arguments' ).getArgs( frame, { wrappers = 'Template:Twitch', removeBlanks = false, parentFirst = true });`

`   local t_name = args[1] or args.id or '';`
`   local from = args.from or '';`

`   if t_name == '' then`
`       t_name = getWikidataProperty('P5797', from) or error('ウィキデータにIDが登録されていません。');`
`   end`
`   local lang = args.lang or '';`
`   local lang2 = '';`

`   if lang ~= '' then`
`       lang = '`<span xml:lang="' ..lang ..'" lang="' ..lang ..'">`';`
`       lang2 = '`</span>`';`
`   end`

`   local formatterURL = mw.text.decode(getWikidataProperty('P1630', 'P5797'));`
`   local url = mw.ustring.gsub(formatterURL, "\$1", t_name);`
`   local name = args[2] or args.name or '';`

`   if name == '' then`
`       name = mw.ustring.gsub(mw.title.getCurrentTitle().text, "%s+%b()$", "");`
`   end`

`   local t_name2 = '(@' .. t_name  ..')';`
`   if mw.ustring.match(name, '%(' .. t_name .. '%)$') then`
`       t_name2 = '';`
`   end`

`   return '[' ..url ..' ' ..lang ..name ..lang2 ..'] ' ..t_name2 ..' - `[`Twitch`](https://ja.wikipedia.org/wiki/Twitch "wikilink")`';`

end

return p;

[Category:ウィキデータにないTwitch](https://ja.wikipedia.org/wiki/Category:ウィキデータにないTwitch "wikilink")