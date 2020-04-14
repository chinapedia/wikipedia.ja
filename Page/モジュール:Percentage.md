> この記事は[モジュール:Percentage](https://ja.wikipedia.org/wiki/モジュール:Percentage)から翻訳されています。


\-- -- This module implements [Template:Percentage](https://ja.wikipedia.org/wiki/Template:Percentage "wikilink") -- local p = {}

local math_module = require( "Module:Math" ) local precision = math_module._precision local sortkey = require( "Module:Sortkey" )

local function rnd(num, digits)

`   -- This function implements `
`   return math_module._precision_format(tostring(num), digits)`

end

local function oom(num)

`   -- This function implements `
`   return math_module._order(tostring(num))`

end

function _nonscinote(num)

`   -- This function undoes scientific notation`
`   if mw.ustring.match(num or '', '^%s*(%d)%.(%d+)<span[^<>]*>×`</span>`10`<sup>`([%-−]*)(%d)`</sup>`%s*$') then`
`       local a,b,c,d = mw.ustring.match(num or '', '^%s*(%d)%.(%d+)<span[^<>]*>×`</span>`10`<sup>`([%-−]*)(%d)`</sup>`%s*$')`
`       d = tonumber(d) or 1`
`       if c ~= '' then`
`           return '0.' .. mw.ustring.rep('0', d - 1) .. a .. b`
`       else`
`           return a .. mw.ustring.sub(b .. mw.ustring.rep('0', d ), 1, d)`
`       end`
`   end`
`   return num`

end

local function fmtout(num,snote)

`   if snote then`
`       return _nonscinote(num)`
`   else`
`       return num`
`   end`

end

function _percentage(n1, n2, prec, suffix, pad, sigfig, sn)

`   local pct = 100*n1/n2`
`   skey = '`<span data-sort-value="'
            .. sortkey._sortKeyForNumber(pct) .. '♠" style="display:none"></span>`'`

`   -- prec = math.floor(prec)`

`   if sigfig ~= '' then`
`       if pct ~= 0 then`
`           return skey .. fmtout(rnd(pct, tonumber(sigfig) - oom(pct) - 1), sn) .. suffix`
`       else`
`           return skey .. fmtout(rnd(pct, tonumber(sigfig) - 3), sn) .. suffix`
`       end`
`   end`
`   if pad ~= '' then`
`       return skey .. fmtout(rnd(pct, prec), sn) .. suffix`
`   end`
`   `
`   prec = (prec < 0) and 0 or prec`
`   if pct ~= 0 then`
`       pct = ((pct < 0) and -1 or 1)*math.floor(math.abs(pct * 10^prec) + 0.5) / 10^prec`
`   end`
`   `
`   return skey .. fmtout(pct, sn) .. suffix`

end

function p.main(frame)

`   local args = frame.args[1] and frame.args or frame:getParent().args`
`   local yesno = require('Module:Yesno')`
`   return _percentage(`
`       tonumber(args[1]) or 0,`
`       tonumber(args[2]) or 100,`
`       tonumber(args[3]) or tonumber(args['pad']) or 0,`
`       args['%'] or '%', args['pad'] or '',`
`       args['sigfig'] or '',`
`       yesno(args['nonscinote'] or 'no')`
`       )`

end

return p