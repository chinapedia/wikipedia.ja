> この記事は[モジュール:Bar box](https://ja.wikipedia.org/wiki/モジュール:Bar_box)から翻訳されています。


local getArgs = require('Module:Arguments').getArgs local yesno = require('Module:Yesno')

local function is(v)

`   return (v or '') ~= ''`

end

local function widths(w,d)

`   local width = is(w) and w or d`
`   if tonumber(width) then width = width .. 'px' end`
`   return width`

end

local p = {}

function p._box(args)

`   local width = widths(args.width,'auto')`
`   `
`   local class = 'barbox'`
`   if args.float == 'left' or args.float == 'right' or args.float == 'none' then`
`       class = 'barbox t' .. args.float`
`   elseif args.float == 'center' then`
`       class = 'barbox tnone'`
`   end`
`   `
`   local output = {}`
`   `
`   output[1] = mw.getCurrentFrame():extensionTag{ name = 'templatestyles', args = {src='Module:Bar box/styles.css'} }`
`   `
`   output[2] = is(args.css) and (mw.getCurrentFrame():extensionTag{ name = 'templatestyles', args = {src=args.css} }) or ''`
`   `
`   if (args.float == 'left') or (args.float == 'right') then`
`       output[3], output[15] = '', ''`
`   else`
`       output[3] =`
`           '`

<table style="margin:' .. ( (args.float == 'center') and '0 auto' or '0' ) .. '; border:none;">

' ..

`               '`

<tr>

' ..

`                   '`

<td style="border:none; padding:0;">

'

`       output[15] = '`

</td>

' ..

`               '`

</tr>

' ..

`           '`

</table>

' ..

`           ''`
`   end`
`   `
`   output[4] = `
`       '`

<div class="' .. class .. '" style="overflow-x: auto;' .. (args.style or '') .. '">

\\n' ..

`       '`

<div style="border:' .. (args.border_width or '1') .. 'px solid silver; font-size:88%; padding:0.4em; width:' .. width .. '; background: ' .. (args['background-color'] or 'white') .. ';">

\\n' ..

`       '`

<table style="text-align:left; border-collapse:collapse; width:100%;">

\\n'

`       output[5] = ( is(args.title) and (`
`           '`

<tr style="background:' .. (args.titlebar or 'none') .. '">

' ..

`               '`

<th style="text-align:center;" colspan="5">

' .. args.title .. '

</th>

' ..

`           '`

</tr>

\\n') or '')

`       output[6] =`
`           '`

<tr style="font-size:88%; height:4px;">

\\n'

`           output[7] =`
`               '<td ' .. (args.left2 and '' or 'colspan="2"') .. ' style="padding:0 4px; text-align:left;">' .. `
`                   (args.left1 or '') .. `
`               '`

</td>

\\n'

`           output[8] = ( is(args.left2) and (`
`               '`

<td style="padding:0 4px; text-align:right;">

' .. args.left2 .. '

</td>

\\n') or '')

`           output[9] =`
`               '`

<td style="width:' ..  widths(args.barwidth,'100px') .. '; text-align:left;">

</td>

\\n' ..

`               '<td ' .. (args.right2 and '' or 'colspan="2"') .. ' style="padding:0 4px; width:1em; text-align:right;">' .. `
`                   (args.right1 or '') .. `
`               '`

</td>

\\n'

`           output[10] = ( is(args.right2) and (`
`               '`

<td style="padding:0 4px; text-align:right;">

' .. args.right2 .. '

</td>

\\n') or '')

`       output[11] =`
`           '`

</tr>

\\n'

`       output[12] =`
`           args.bars or ''`
`       output[13] = ( is(args.caption) and (`
`           '`

<tr>

<td colspan="5" style="padding:5px; text-align:left;">

' ..

`               args.caption .. `
`           '`

</td>

</tr>

\\n') or '')

`   output[14] =`
`       '`

</table>

\\n

</div>

\\n

</div>

\\n'

`   -- output[15] defined above`
`   `
`   return table.concat(output)`

end

function p._percent(args)

`   local output = {}`
`   local background = is(args.bg) and ('background:' .. args.bg .. ';') or '' `
`   local percentage = ( is(args[3]) and args[3] or '0' ) .. '%'`
`   local rowStyle = is(args.rowstyle) and (' style="' .. args.rowstyle .. '"') or ''`
`   `
`   output[1] = '<tr' .. rowStyle .. '>\n'`
`       output[2] = '`

<td colspan="2" class="bb-4em" style="min-width:8em;' .. background .. '">

' .. (args\[1\] or '') .. '

</td>

\\n'

`       output[3] = '`

<td class="bb-lr" style="width:' .. widths(args.barwidth,'100px') .. ';' .. background .. '">

'

`           output[4] = '`

<div style="background:' .. ( is(args[2]) and args[2] or 'gray' ) .. ';width:' .. percentage .. ';overflow:hidden;">

 

</div>

'

`       output[5] = '`

</td>

\\n'

`       output[6] = '`

<td colspan="' .. ( is(args.note) and '1' or '2' ) .. '" class="bb-4emr" style="' .. background .. '">

' .. ( is(args\[4\]) and args\[4\] or percentage ) .. '

</td>

\\n'

`       output[7] = ( is(args.note) and ('`

<td class=bb-4emr" style="' .. background .. '">

' .. args.note .. '

</td>

\\n') or '' )

`   output[8] = '`

</tr>

'

`   return table.concat(output)`

end

function p._pixel(args)

`   local output = {}`
`   local background = ( is(args[2]) and args[2] or 'gray' )`
`   local width = ( is(args[3]) and args[3] or '0' )`
`   local note = ( is(args.note) and '1' or '2' )`
`   local rowStyle = is(args.rowstyle) and (' style="' .. args.rowstyle .. '"') or ''`
`   `
`   output[1] =`
`       '<tr' .. rowStyle .. '>\n'`
`       output[2] =`
`           '`

<td colspan="2" class="bb-4em">

' .. (args\[1\] or '') .. '

</td>

\\n'

`       output[3] =`
`           '<td class-"bb-lr">' ..`
`               '`

<div style="background:' .. background .. '; width:' .. width .. 'px; overflow:hidden">

' ..

`                   ' ' ..`
`               '`

</div>

' ..

`           '`

</td>

\\n'

`       output[4] =`
`           '`

<td colspan="' .. note .. '" class="bb-min3">

' ..

`               ( is(args[5]) and args[5] or (width .. (args[4] or '')) ) ..`
`           '`

</td>

\\n'

`       output[5] = ( is(args.note)  and (`
`           '`

<td class="bb-4emr">

' ..

`               args.note ..`
`           '`

</td>

\\n') or '' )

`   output[6] =`
`       '`

</tr>

'

`   return table.concat(output)`

end

function p._stacked(args)

`   local function _align(n, default)`
`       if (args.align or '') ~= '' then`
`           local a = mw.ustring.sub(args.align,n,n)`
`           if a == 'l' then`
`               return 'left'`
`           elseif a == 'c' then`
`               return 'center'`
`           elseif a == 'r' then`
`               return 'right'`
`           elseif a == 'd' then`
`               return default`
`           end`
`       end`
`       `
`       return default`
`   end`

`   local output = {}`
`   `
`   local rowStyle = is(args.rowstyle) and (' style="' .. args.rowstyle .. '"') or ''`
`   output[1] = ( is(args.id) and (`
`       '<tr class="mw-collapsible' .. ( yesno(args.collapsed) and ' mw-collapsed' or '') ..`
`       '" id="mw-customcollapsible-' .. args.id .. '"' .. rowStyle .. '>\n') or ('<tr' .. rowStyle .. '>\n') )`
`       output[2] =`
`           '<td ' .. (args.note1 and '' or 'colspan="2" ') .. `
`           'style="text-align:' .. _align(1,'left') .. '" class="bb-04em">' .. `
`               mw.text.trim(args[1] or '') .. `
`           '`

</td>

\\n'

`       output[3] = ( is(args.note1) and (`
`           '`

<td style="text-align:' .. _align(2,'right') .. '" class="bb-04em">

' ..

`               args.note1 .. `
`           '`

</td>

\\n') or '')

`       output[4] =`
`           '`

<td class="bb-lr">

\\n'

`           local maxn = 4`
`           for k in pairs(args) do`
`               local kn = tonumber(k) or 0`
`               if kn > maxn then maxn = kn end`
`           end`
`           `
`           for i=1,(( maxn - 2 )/2),1 do`
`               local width = ( mw.text.trim(args[(2*i) + 2] or 0) )`
`               width = (is(width) and width or 0)`
`               width = tonumber( mw.ustring.format("%.2f", width) )`
`               if width == 0 then`
`                   output[i+4] = ''`
`               else`
`                   local title = ( (args['title' .. i] or '') ~= '' ) and ( ' title=' .. args['title' .. i] ) or ''`
`                   local background = ( (args[(2*i) + 1] or '') ~= '' ) and args[(2*i) + 1] or 'gray'`
`                   `
`                   output[i+4] =`
`                       '<div' .. title .. ' style="background:' .. background .. ';width:' .. width .. 'px" class="bb-fl">' ..`
`                           '​' ..`
`                       '`

</div>

\\n'

`               end`
`           end`
`   `
`       output[#output+1] =`
`           '`

</td>

\\n'

`       output[#output+1] = `
`           '<td ' .. (args.note2 and '' or 'colspan="2" ') .. `
`           'style="text-align:' .. _align(3,'left') .. '" class="bb-04em">' .. `
`               mw.text.trim(args[2] or '') .. `
`           '`

</td>

\\n'

`       output[#output+1] = ( is(args.note2) and (`
`           '`

<td style="text-align:' .. _align(4,'right') .. '" class="bb-04em">

' ..

`               args.note2 ..`
`           '`

</td>

\\n') or '')

`   output[#output+1] =`
`       '`

</tr>

\\n'

`   return table.concat(output)`

end

function p._gap(args)

`   local output = {}`
`   local rowStyle = is(args.rowstyle) and (' style="' .. args.rowstyle .. '"') or ''`
`   local height = '10px'`
`   if (args.height or '') ~= '' then`
`       height = (tonumber(args.height) and (args.height .. 'px') or args.height)`
`   end`
`           `
`   output[1] =`
`       '<tr' .. rowStyle .. '>\n'`
`       output[2] = `
`           '`

<td colspan="5" style="height:'.. height .. '">

' .. (args\[1\] or '') .. '

</td>

\\n'

`   output[3] =`
`       '`

</tr>

\\n'

`   return table.concat(output)`

end

function p.box(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if (key == 'width') or (key == 'float') then`
`                   value = mw.ustring.lower(value)`
`               end`
`               if value ~= '' then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._box(args)`

end

function p.percent(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if value ~= '' then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._percent(args)`

end

function p.pixel(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if value ~= '' then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._pixel(args)`

end

function p.gap(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if value ~= '' then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._gap(args)`

end

function p.stacked(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if (key == 'collapsed') or (key == 'align') then`
`                   value = mw.ustring.lower(value)`
`               end`
`               if value ~= '' then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._stacked(args)`

end

return p

[Category:Pages_using_bar_box_without_float_left_or_float_right](https://ja.wikipedia.org/wiki/Category:Pages_using_bar_box_without_float_left_or_float_right "wikilink")