> この記事は[モジュール:Medical cases chart](https://ja.wikipedia.org/wiki/モジュール:Medical_cases_chart)から翻訳されています。


local getArgs = require('Module:Arguments').getArgs local yesno = require('Module:Yesno') local barBox = require('Module:Bar box')

local language = 'ja-JP' -- local default language

local i18n = require("Module:Medical cases chart/i18n")\[language\]

local function is(v)

`   return (v or '') ~= ''`

end

local p = {}

function p._barColors(n)

`   local colors = {`
`       'DimGrey', --deaths`
`       'SkyBlue', --recoveries`
`       'Tomato', --cases or altlbl1`
`       'Gold', --altlbl2`
`       'OrangeRed' --altlbl3`
`   }`

`   return colors[n]`

end

function p._legend0(args)

`   return '`<span style="font-size:90%; margin:0px">`' .. '`<span style="' .. 'background-color:' .. (args[1] or 'none') .. '; border:' .. (args.border or 'none') .. '; color:' .. (args[1] or 'none') .. '">`' .. '    ' .. '`</span>`' .. ' ' .. (args[2] or '') .. '`</span>`'`

end

function p._customBarStacked(args)

`   barargs = {}`
`   barargs[1] = args[1]`

`   local function _numwidth(nw)`
`       if nw == 'n' then`
`           return 0`
`       elseif nw == 't' then`
`           return 2.45`
`       elseif nw == 'm' then`
`           return 3.5`
`       elseif nw == 'w' then`
`           return 4.55`
`       elseif nw == 'x' then`
`           return 5.6`
`       elseif nw == 'd' then`
`           return 3.5`
`       end`

`       return 3.5`
`   end`

`   width1 = 3.5`
`   width2 = 3.5`
`   if is(args.numwidth) then`
`       width1 = _numwidth(mw.ustring.sub(args.numwidth,1,1))`
`       width2 = _numwidth(mw.ustring.sub(args.numwidth,2,2))`
`       width3 = _numwidth(mw.ustring.sub(args.numwidth,3,3))`
`       width4 = _numwidth(mw.ustring.sub(args.numwidth,4,4))`
`   end`

`   barargs[2] =`
`       '`<span class="cbs-ibr" style="padding:0 0.3em 0 0; width:' .. width1 .. 'em">`' .. (args[7] or '') .. '`</span>`' ..`
`       '`<span class="cbs-ibl" style="width:' .. width2 .. 'em">`' .. (args[8] or '') .. '`</span>`'`

`   if mw.ustring.len(args.numwidth) == 4 then`
`       local padding = '0.3em'`
`       if mw.ustring.sub(args.numwidth,3,3) == 'n' then`
`           padding = '0'`
`       end`

`       barargs.note2 =`
`           '`<span class="cbs-ibr" style="padding:0 ' .. padding .. ' 0 0; width:' .. width3 .. 'em">`' .. (args[9] or '') .. '`</span>`' ..`
`           '`<span class="cbs-ibl" style="width:' .. width4 .. 'em">`' .. (args[10] or '') .. '`</span>`'`
`   end`

`   for i=1,5 do`
`       barargs[2*i + 1] = p._barColors(i)`
`       barargs[2*i + 2] = (tonumber(args[i+1]) or 0)/(tonumber(args.divisor) or 1)`
`       barargs['title' .. i] = args[i+1]`
`   end`

`   barargs.align = 'cdcc'`
`   barargs.collapsed = args.collapsed`
`   barargs.id = args.id`
`   barargs.rowstyle = is(tonumber(args.rowheight)) and ('line-height:'..args.rowheight..';') or nil`

`   return barBox._stacked(barargs)`

end

function p._row(args)

`   local barargs = {}`
`   local rowDate = args.prevDate or ''`

`   if is(args[1]) then`
`       if pcall(function () mw.getContentLanguage():formatDate('', args[1]) end) then`
`           barargs[1] = args[1]`
`           rowDate = args[1]`
`       else`
`           barargs[1] = '`<strong class="error">`' .. i18n.invalidTime .. '`</strong>`'`
`       end`
`   else`
`       barargs[1] = '⋮'`
`   end`

`   barargs[2] = args[2] or 0`
`   barargs[3] = args[3] or 0`

`   if is(args['alttot1']) then`
`       barargs[4] = args['alttot1']`
`   elseif args[4] then`
`       barargs[4] = (tonumber(args[4]) or 0) - (tonumber(barargs[2]) or 0) - (tonumber(barargs[3]) or 0)`
`   else`
`       barargs[4] = 0`
`   end`

`   barargs[5] = args[5] or 0`

`   if is(args['alttot2']) then`
`       barargs[6] = args['alttot2']`
`   elseif args[6] then`
`       barargs[6] = (tonumber(args[6]) or 0) - (tonumber(barargs[2]) or 0) - (tonumber(barargs[3]) or 0)`
`   else`
`       barargs[6] = 0`
`   end`

`   barargs[7] = args[7] or ''`

`   local function changeArg(firstright, valuecol, changecol)`
`       local change = ''`
`       if yesno(args['firstright' .. firstright]) == true then`
`           change = '(' .. i18n.na .. ')'`
`       elseif yesno(args['firstright' .. firstright]) == false or not is(args['firstright' .. firstright]) then`
`           if not is(args[1]) and is(args[valuecol]) then`
`               change = '(' .. i18n['='] .. ')'`
`           else`
`               change = is(args[changecol]) and '(' .. args[changecol] .. ')' or ''`
`           end`
`       end`

`       return change`
`   end`

`   barargs[8] = changeArg(1,7,8)`
`   barargs[9] = args[9] or ''`
`   barargs[10] = changeArg(2,9,10)`

`   barargs.divisor = args.divisor or 1`
`   barargs.numwidth = args.numwidth`
`   barargs.rowheight = args.rowheight`

`   if yesno(args.collapsible) == true then`
`       local duration = tonumber(args.duration) or 15`
`       if args.collapsed then`
`           barargs.collapsed = args.collapsed`
`       elseif args.rowsToEnd >= duration then`
`           barargs.collapsed = 'y'`
`       else`
`           barargs.collapsed = ''`
`       end`

`       if args.id then`
`           barargs.id = args.id`
`       elseif args.nooverlap and args.rowsToEnd < duration then`
`           barargs.id = 'l' .. duration`
`       else`
`           barargs.id = mw.ustring.lower(mw.getLanguage('ja'):formatDate('M', rowDate))`
`           if args.rowsToEnd < duration then`
`               barargs.id = barargs.id .. '-l' .. duration`
`           end`
`       end`
`   else`
`       barargs.collapsed = ''`
`       barargs.id = ''`
`   end`

`   return p._customBarStacked(barargs)`

end

function p._buildBars(args)

`   local lines = mw.text.split(args.data, '\n')`
`   local frame = mw.getCurrentFrame()`
`   local lang = mw.getContentLanguage()`

`   local bars, rows, months, prevRow, maxparam = {}, {}, {}, '', 1`
`   for k, line in pairs(lines) do`
`       local barargs, i = {}, 1`
`       for parameter in mw.text.gsplit(line, ';') do`
`           parameter = mw.text.trim(parameter)`
`           if string.find(parameter, '^%a') then`
`               parameter = mw.text.split(parameter, '=')`
`               if parameter[1] == 'alttot1' or parameter[1] == 'alttot2' then`
`                   parameter[2] = tonumber(frame:callParserFunction('#expr', parameter[2]))`
`                   if is(parameter[2]) then`
`                       maxparam = math.max(maxparam, parameter[2])`
`                   end`
`               end`
`               barargs[parameter[1]] = parameter[2]`
`           else`
`               if is(parameter) then`
`                   if i >= 2 and i <= 6 then`
`                       parameter = tonumber(frame:callParserFunction('#expr', frame:callParserFunction('formatnum',parameter,'R')))`
`                       maxparam = math.max(maxparam, parameter or 1)`
`                   end`
`                   barargs[i] = parameter`
`                   if i == 7 or i == 9 then`
`                       parameter = tonumber(mw.ustring.match(frame:callParserFunction('formatnum',parameter,'R'), '^%d*'))`
`                       maxparam = math.max(maxparam, parameter or 1)`
`                   end`
`               end`
`               i = i + 1`
`           end`
`       end`

`       local function fillCols(col, change)`
`           local data = args['right' .. col .. 'data']`
`           local changetype = args['changetype' .. col]`
`           local value, num, prevnum`

`           if data == 'alttot1' then`
`               num = tonumber(barargs.alttot1 or barargs[4])`
`               prevnum = tonumber(prevRow.alttot1 or prevRow[4])`
`           elseif data == 'alttot2' then`
`               num = tonumber(barargs.alttot2 or barargs[6])`
`               prevnum = tonumber(prevRow.alttot2 or prevRow[6])`
`           elseif is(data) then`
`               num = tonumber(barargs[tonumber(data) + 1])`
`               prevnum = tonumber(prevRow[tonumber(data) + 1])`
`           end`

`           if is(data) and num then -- nothing in column, source found, and data exists`
`               value = changetype == 'o' and '' or lang:formatNum(num) -- set value to num if changetype isn't 'o'`
`               `
`               if not change and yesno(barargs['firstright' .. col] ~= true) then`
`                   if prevnum and prevnum ~= 0 then -- data on previous row`
`                       if num - prevnum ~= 0 then --data has changed since previous row`
`                           change = num-prevnum`
`                           if changetype == 'a' then -- change type is "absolute"`
`                               if change > 0 then`
`                                   change = '+' .. lang:formatNum(change)`
`                               end`
`                           else -- change type is "percent", "only percent" or undefined`
`                               local percent = 100 * change / prevnum -- calculate percent`
`                               local rounding = math.abs(percent) >= 10 and "%.0f" or math.abs(percent) >= 1 and "%.1f" or "%.2f"`
`                               percent = tonumber(mw.ustring.format(rounding, percent)) -- round to two sigfigs`
`                               `
`                               if percent > 0 then`
`                                   change = '+' .. lang:formatNum(percent) .. '%'`
`                               elseif percent < 0 then`
`                                   change = lang:formatNum(percent) .. '%'`
`                               else`
`                                   change = i18n['=']`
`                               end`
`                           end`
`                       else -- data has not changed since previous row`
`                           change = i18n['=']`
`                       end`
`                   else -- no data on previous row`
`                       barargs['firstright' .. col] = true -- set to (n.a.)`
`                   end`
`               end`
`           end`

`           return value, change`
`       end`

`       if not is(barargs[7]) then`
`           barargs[7], barargs[8] = fillCols(1, barargs[8])`
`       end`
`       if not is(barargs[9]) then`
`           barargs[9], barargs[10] = fillCols(2, barargs[10])`
`       end`
`       `
`       if is(barargs[1]) then`
`           local e,f,g = pcall(`
`               function ()`
`                   return mw.getLanguage('ja'):formatDate('M',barargs[1]),`
`                       mw.getLanguage('ja'):formatDate('j',barargs[1])`
`               end`
`           )`
`           if e then`
`               months[#months+1] = {f,g}`
`           end`
`       end`
`       `
`       barargs.prevDate = prevRow[1]`
`       rows[#rows + 1] = barargs`
`       prevRow = barargs`
`   end`

`   for i=1,#rows do -- build rows`
`       rows[i].divisor = tonumber(args.divisor) and tonumber(args.divisor) or maxparam / (0.95 * args.barwidth)`
`       rows[i].numwidth = args.numwidth`
`       rows[i].collapsible = args.collapsible`
`       rows[i].rowsToEnd = #rows - i`
`       rows[i].rowheight = args.rowheight`
`       rows[i].duration = args.duration`
`       if #months>(args.duration or 0) then`
`           rows[i].nooverlap = args.nooverlap`
`       end`
`       `
`       bars[i] = p._row(rows[i])`
`   end`
`   `
`   return table.concat(bars), months`

end

function p._monthToggleButton(args)

`   local month = mw.ustring.lower(mw.ustring.sub(args.month[1] or '',1,3))`
`   local outString = ''`
`   local newline = (args.nonewline or false) and '' or '\n'`
`   if is(month) then`
`       local collapsed = (args.active == '') and '' or ' mw-collapsed'`
`       local uncollapsed = (args.active == '') and ' mw-collapsed' or ''`
`       if args.nooverlap then`
`           outString = '`<span class="mw-collapsible mw-customtoggle-' .. month .. ' %s" id="mw-customcollapsible-' .. month .. '" style="padding:0 8px">`%s`</span>`\n' ..`
`               '`<span class="mw-collapsible mw-customtoggle-' .. month .. ' %s" id="mw-customcollapsible-' .. month .. '" style="border:2px solid lightblue; padding:0 8px">`%s`</span>`' .. newline`
`           `
`           if mw.ustring.sub(month,1,1) == 'l' and tonumber(mw.ustring.sub(month,2)) == args.duration then`
`               --"Last ## days"`
`               local lastDays = mw.ustring.format(i18n.lastDays, args.duration)`
`           `
`               outString = mw.ustring.format( outString,`
`                   collapsed, lastDays,`
`                   uncollapsed, lastDays )`
`           else`
`               if i18n.m[month] then`
`                   if is(args.month[2]) and is(args.month[3]) then`
`                       -- "Mmm ##–##"`
`                       month = mw.ustring.gsub(i18n.toggleRange,'$.', {`
`                           ['$m'] = i18n.m[month],`
`                           ['$s'] = args.month[2],`
`                           ['$e'] = args.month[3]})`
`                   else`
`                       --"Mmm"`
`                       month = i18n.m[month]`
`                   end`
`               end`
`                       `
`               outString = mw.ustring.format( outString,`
`                   uncollapsed, month,`
`                   collapsed, month )`
`           end`
`       elseif mw.ustring.sub(month,1,1) == 'l' and tonumber(mw.ustring.sub(month,2)) == args.duration then`
`           local customtoggles = {(' mw-customtoggle-l' .. args.duration)}`
`           for k in pairs(i18n.m) do --list of months`
`               customtoggles[#customtoggles + 1] = ' mw-customtoggle-' .. k .. '-l' .. args.duration`
`           end`
`           `
`           local lastDays = mw.ustring.format(i18n.lastDays, args.duration)`
`           `
`           outString = '`<span class="mw-collapsible' .. table.concat(customtoggles) .. collapsed .. '" id="mw-customcollapsible-' .. month .. '" style="padding:0 8px">`' .. lastDays .. '`</span>`\n' ..`
`               '`<span class="mw-collapsible' .. table.concat(customtoggles) .. uncollapsed .. '" id="mw-customcollapsible-' .. month .. '" style="border:2px solid lightblue; padding:0 8px">`' .. lastDays .. '`</span>`' .. newline`
`           `
`       else`
`           local customtoggles = ' mw-customtoggle-' .. month .. ' mw-customtoggle-' .. month .. '-l' .. args.duration`
`           `
`           outString = '`<span class="mw-collapsible' .. customtoggles .. uncollapsed .. '" id="mw-customcollapsible-' .. month .. '" style="padding:0 8px">`' .. (i18n.m[month] or month)  .. '`</span>`\n' ..`
`               '`<span class="mw-collapsible mw-customtoggle-' .. customtoggles .. collapsed .. '" id="mw-customcollapsible-' .. month .. '" style="border:2px solid lightblue; padding:0 8px">`' .. (i18n.m[month] or month)  .. '`</span>`'  .. newline`
`       end`
`   end`
`   `
`   return outString`

end

function p._chart(args)

`   local navbar = require('Module:Navbar')._navbar`

`   local barargs = {}`

`   local function _numwidth(p)`
`       local nw = mw.ustring.sub(args.numwidth or '',p,p)`
`       if nw == 'n' then`
`           return 0`
`       elseif nw == 't' then`
`           return 40`
`       elseif nw == 'm' then`
`           return 55`
`       elseif nw == 'w' then`
`           return 70`
`       elseif nw == 'x' then`
`           return 85`
`       elseif nw == 'd' then`
`           return 55`
`       end`

`       return 0`
`   end`

`   local numwidth = 120`
`   local right1 = numwidth - 8 -- -8 because of padding`
`   if args.numwidth then`
`       numwidth = _numwidth(1) + 10 + _numwidth(2)`
`       if mw.ustring.len(args.numwidth) == 4 then`
`           numwidth = numwidth + _numwidth(3) + _numwidth(4)`
`           if mw.ustring.sub(args.numwidth,3,3) == 'n' then`
`               numwidth = numwidth + 6`
`           else`
`               numwidth = numwidth + 10`
`           end`
`       end`

`       right1 = _numwidth(1) + 2 + _numwidth(2)`
`       if not args.right2 and mw.ustring.len(args.numwidth) == 4 then`
`           right1 = right1 + _numwidth(3) + _numwidth(4)`
`           if mw.ustring.sub(args.numwidth,3,3) == 'n' then`
`               numwidth = numwidth + 6`
`           else`
`               numwidth = numwidth + 10`
`           end`
`       end`
`   end`

`   local barwidth = 280`

`   if args.barwidth == 'thin' then`
`       barwidth = 120`
`   elseif args.barwidth == 'medium' then`
`       barwidth = 280`
`   elseif args.barwidth == 'wide' then`
`       barwidth = 400`
`   elseif args.barwidth == 'auto' then`
`       barwidth = 'auto'`
`   end`

`   if tonumber(barwidth) then`
`       barargs.width = 100 + barwidth + numwidth .. 'px'`
`       barargs.barwidth = barwidth .. 'px'`
`   else`
`       barargs.width = 'auto'`
`       barargs.barwidth = 'auto'`
`   end`

`   barargs.float = args.float and args.float or 'right'`
`   local location = mw.ustring.gsub(args.location, 'the ', '')`
`   location = mw.ustring.upper(mw.ustring.sub(location,1,1)) .. mw.ustring.sub(location,2)`

`   -- get duration for toggles`
`   local duration = 15 -- default if manual togglesbar is last 15 days`
`   if yesno(args.collapsible) == true and ( not is(args.togglesbar) ) then`
`       duration = tonumber(args.duration) or 15 -- default if auto togglesbar is last 15 days`
`   end`
`   `
`   local months, togglesbar, lastdate = {{}}, '', nil`
`   if args.rows then`
`       barargs.bars = args.rows`
`       if yesno(args.collapsible) == true then`
`           togglesbar = is(args.togglesbar) and args.togglesbar or ''`
`       end`
`   elseif is(args.data) or is(args.datapage) then`
`       local buildargs = {}`
`       `
`       local nooverlap = yesno(args.nooverlap)`
`       `
`       buildargs.barwidth = tonumber(barwidth) or 280`
`       buildargs.data = is(args.datapage) and require('Module:Medical cases chart/data')._externalData(args) or args.data`
`       buildargs.divisor = args.divisor`
`       buildargs.numwidth = args.numwidth`
`       buildargs.collapsible = args.collapsible`
`       buildargs.right1data = args.right1data or -- if no right1data and right1 title is default, use 3rd classification`
`               not args.right1 and 3`
`       buildargs.right2data = args.right2data or -- if no right2data and right2 title is deaths, use 1st classification`
`               (args.right2 == i18n.noOfDeaths or args.right2 == i18n.noOfDeaths2) and 1`
`       buildargs.changetype1 = mw.ustring.sub(args.changetype1 or (args.changetype or ''),1,1) -- 1st letter`
`       buildargs.changetype2 = mw.ustring.sub(args.changetype2 or (args.changetype or ''),1,1) -- 1st letter`
`       buildargs.rowheight = args.rowheight`
`       buildargs.duration = duration`
`       if is(args.togglesbar) then`
`           buildargs.nooverlap = false`
`       else`
`           buildargs.nooverlap = nooverlap`
`       end`
`       `
`       barargs.bars, monthList = p._buildBars(buildargs)`
`       `
`       local lastRow = #monthList`
`       if nooverlap == true then`
`           if #monthList <= duration then`
`               nooverlap = false`
`           else`
`               lastRow = #monthList - duration`
`           end`
`       end`

`       for i=1,(lastRow) do -- deduplicate months`
`           if monthList[i][1] ~= months[#months][1] then --new month`
`               if #months > 1 and i > 1 then`
`                   months[#months][3] = monthList[i-1][2] --store end of previous month`
`               end`
`               months[#months+1] = monthList[i] --store start of this month`
`           end`
`       end`
`       months[#months][3] = monthList[lastRow][2] --store end of final month`
`       `
`       -- automatically generate toggles`
`       if yesno(args.collapsible) == true then`
`           if is(args.togglesbar) then`
`               togglesbar = args.togglesbar`
`           else`
`               local toggles = {}`
`               for i=1,#months do`
`                   toggles[#toggles+1] = p._monthToggleButton({month=months[i], duration=duration, nooverlap=nooverlap})`
`               end`
`               toggles[#toggles+1] = p._monthToggleButton({month={('l' .. duration)}, duration=duration, nooverlap=nooverlap})`
`               togglesbar = '`

<div class="nomobile" style="text-align:center">

\\n' .. table.concat(toggles) .. '

</div>

'

`           end`
`       end`
`   end`
`   `
`   local title = {}`
`   title[1] = '`

<div style="display:flex; justify-content:center;">

' .. (args.pretitle and args.pretitle .. '' or '') ..

`       (args.location3 and '' .. args.location3 or '') ..`
`       (args.location2 and '' .. args.location2 or '') ..`
`       args.location .. '' .. i18n.casesIn .. '' .. args.disease ..`
`       (args.posttitle and 'の症例数' .. args.posttitle or 'の症例数') .. '`<span class="nowrap">`  `</span>`(`

<div style="font-size:75%;">

' ..

`       navbar({[1] = args.navbartitle, titleArg = ':' .. mw.getCurrentFrame():getParent():getTitle(), mini = 1, nodiv = 1}) ..`
`       '`

</div>

)

</div>

'

`   title[2] = p._legend0({[1] = p._barColors(1), [2] = '死亡'})`
`   if yesno(args.recoveries) == false then`
`       title[3] = ''`
`   else`
`       title[3] = '`<span class="nowrap">`   `</span>`' .. p._legend0({[1] = p._barColors(2), [2] = args.reclbl or i18n.recoveries})`
`   end`
`   title[4] = '`<span class="nowrap">`   `</span>`' .. p._legend0({[1] = p._barColors(3), [2] = args.altlbl1 or i18n.activeCases})`
`   if args.altlbl2 then`
`       title[5] = '`<span class="nowrap">`   `</span>`' .. p._legend0({[1] = p._barColors(4), [2] = args.altlbl2})`
`   else`
`       title[5] = ''`
`   end`
`   if args.altlbl3 then`
`       title[6] = '`<span class="nowrap">`   `</span>`' .. p._legend0({[1] = p._barColors(5), [2] = args.altlbl3}) ..'\n'`
`   else`
`       title[6] = '\n'`
`   end`
`   title[7] = togglesbar`
`   `

`   barargs.title = table.concat(title)`
`   barargs.left1 =`
`       '`

<div class="center" style="width:95px">

' ..

`           "`**`"``   ``..``   ``i18n.date``   ``..``   ``"`**`" ..`
`       '`

</div>

'

`   barargs.right1 =`
`       '`

<div class="center" style="width:' .. right1 .. 'px">

' ..

`           "`**`"``   ``..``   ``(args.right1``   ``or``   ``i18n.noOfCases)``   ``..``   ``"`**`" ..`
`       '`

</div>

'

`   if args.right2 then`
`       local right2 = _numwidth(3) + _numwidth(4)`
`       if mw.ustring.sub(args.numwidth,3,3) == 'n' then`
`           right2 = right2 - 2`
`       else`
`           right2 = right2 + 2`
`       end`

`       barargs.right2 =`
`       '`

<div class="center" style="width:' ..right2 ..'px">

' ..

`           "`**`"``   ``..``   ``args.right2``   ``..``   ``"`**`" ..`
`       '`

</div>

'

`   end`

`   barargs.caption = args.caption`
`   barargs.css = 'Template:Medical_cases_chart/styles.css'`
`   return barBox._box(barargs)`

end

function p.chart(frame)

`   local args = getArgs(frame, {`
`       valueFunc = function (key, value)`
`           if value then`
`               value = mw.text.trim(value)`
`               if ({['numwidth']=1,['barwidth']=1,['recoveries']=1,['changetype']=1})[mw.ustring.gsub(key,"%A","")] then`
`                   value = mw.ustring.lower(value) --make numwidth, barwidth, recoveries, and changetype lower case`
`               end`
`               if is(value) then`
`                   return value`
`               end`
`           end`
`           return nil`
`       end`
`   })`
`   return p._chart(args)`

end

function p.barColors(frame)

`   return p._barColors(tonumber(frame:getParent().args[1]))`

end

function p.buildBars(frame)

`   local bars = p._buildBars(frame.args)`
`   return bars`

end

function p.monthToggleButton(frame)

`   local args = {}`
`   args.month = {frame:getParent().args.month or frame:getParent().args[1] or 'l15'}`
`   args.active = frame:getParent().args.active or 'true'`
`   args.duration = frame:getParent().args.duration or 15`
`   args.nonewline = true`
`   return p._monthToggleButton(args)`

end

return p