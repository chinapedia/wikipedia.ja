> この記事は[モジュール:NUMBEROF](https://ja.wikipedia.org/wiki/モジュール:NUMBEROF)から翻訳されています。


local function trimArg(arg, i)

`   arg = mw.text.trim(arg or '')`
`   if arg == '' then`
`       if i then`
`           error('Parameter ' .. i .. ' is missing. See `[`Template:NUMBEROF`](https://ja.wikipedia.org/wiki/Template:NUMBEROF "wikilink")` documentation')`
`       end`
`       return nil`
`   end`
`   return mw.ustring.lower(arg)`

end

local function getValue(stats, action, map)

`   if action == 'depth' then`
`       -- `<https://meta.wikimedia.org/wiki/Wikipedia_article_depth>
`       -- This gives silly results if, for example, the number of articles is small.`
`       local n = { 'articles', 'edits', 'pages' }`
`       if map then`
`           for i, v in ipairs(n) do`
`               n[i] = map[v]`
`           end`
`       end`
`       for i, v in ipairs(n) do`
`           n[i] = stats[v] or 0`
`       end`
`       local articles, edits, pages = n[1], n[2], n[3]`
`       if pages == 0 or articles == 0 then`
`           return 0`
`       end`
`       return math.floor((edits/pages) * ((pages - articles)/articles)^2)`
`   end`
`   if map then`
`       action = map[action]`
`   end`
`   return stats[action]`

end

local function getIfLocal(site, action)

`   -- If wanted site is the local site where module is running,`
`   -- return numberof result for given action, or nil.`
`   -- This is faster than reading the cached table, and gives the current value.`
`   local localSite = string.match(mw.site.server, '.*//(.*)%.org$')  -- examples: 'af.wikipedia', 'commons.wikimedia'`
`   if site == localSite then`
`       if action == 'activeusers' then`
`           action = 'activeUsers'`
`       end`
`       return getValue(mw.site.stats, action)`
`   end`

end

local function main(frame)

`   local args = frame:getParent().args`
`   local action = trimArg(args[1], 1)  -- activeusers, admins, articles, edits, files, pages, users, depth`
`   if action:sub(1, 8) == 'numberof' then  -- numberofX is an alias for X`
`       action = trimArg(action:sub(9), 1)`
`   end`
`   local site = trimArg(args[2], 2)  -- "af" or "af.wikipedia" or "af.wikiquote" etc., including "total"`
`   if not site:find('.', 1, true) then`
`       site = site .. '.wikipedia'`
`   end`
`   local wantComma = trimArg(args[3])  -- nil for no commas in output; "N" or anything nonblank inserts commas`
`   local result = getIfLocal(site, action)`
`   if not result then`
`       local data = mw.loadData('Module:NUMBEROF/data')`
`       local map = data.map`
`       data = data.data`
`       result = data[site]`
`       if result then`
`           result = getValue(result, action, map)`
`       end`
`   end`
`   if result then`
`       if wantComma then`
`           result = mw.getContentLanguage():formatNum(result)`
`       end`
`       return result  -- number or formatted string`
`   end`
`   return -1`

end

return { main = main }