> この記事は[モジュール:Xiangqi diagram plus](https://ja.wikipedia.org/wiki/モジュール:Xiangqi_diagram_plus)から翻訳されています。


\-- 模块:Xiangqi diagram的扩展版，支持更多功能 -- 目前还在测试中…… local p = {} function p.board(frame)

`   local args = require('Module:Arguments').getArgs(frame)`
`   ----设置对齐方式`
`   local align = string.gsub(args[1] or '', '\n', '')`
`   if align == '' then`
`       align = 'tright'`
`   end`
`   local header = string.gsub(args[2] or '', '\n', '')`
`   local footer = string.gsub(args[93] or '', '\n', '')`
`   ----设置整张图片的尺寸`
`   local size`
`   local width`
`   local height`

`   if args.size ~= nil then`
`       size = args.size`
`       width = size * 9`
`       height = size * 12`
`   elseif args.width ~= nil then`
`       width = args.width`
`       size = width / 9`
`       height = size * 12`
`   elseif args.height ~= nil then`
`       height = args.height`
`       size = height / 12`
`       width = size * 9`
`   else`
`       size = 25`
`       width = 225`
`       height = 300`
`   end`

`   local rows = args.rows`
`   local startrow = args.startrow`
`   local top = 0`
`   local bheight = height`

`   local cols = args.cols`
`   local startcol = args.startcol`
`   local left = 0`
`   local bwidth = width`
`   local bsize = size`

`   ----设置起始列和列数`
`   if cols == nil and startcol ~= nil then`
`       cols = 9 - startcol`
`   end`
`   if cols ~= nil then`
`       width = width * cols / 9`
`   end`
`   if cols ~= nil and startcol == nil then`
`       startcol = 1`
`   end`
`   if startcol ~= nil then`
`       left = bwidth / 9 * (startcol - 1)`
`   end`

`   ----设置起始行及行数`
`   if rows == nil and startrow ~= nil then`
`       rows = 12 - startrow`
`   end`
`   if rows ~= nil then`
`       bheight = bheight / 12 * rows`
`   end`
`   if rows ~= nil and startrow == nil then`
`       startrow = 1`
`   end`
`   if startrow ~= nil then`
`       top = height / 12 * startrow`
`   end`

`   ----元件大小設定`
`   local sizef1 = size / 15`
`   local sizef2 = size / 20`
`   local sizef3 = size / 5`
`   local margin = size / 2 - sizef3 / 2`
`   local sizeX = math.ceil(size / 2, 0)`
`   local marginX = size / 2 - sizeX / 2`

`   ----输出棋盘图片`
`   local qp = ''`
`   qp = qp .. '`

<div class="' .. align .. '" style="clear:right;">

'

`   qp = qp .. '`

<div style="text-align:center;width:' .. width .. 'px">

' .. header .. '

</div>

'

`   qp = qp .. '`

<div style="position:relative;width:' .. width .. 'px;height:' .. bheight .. 'px;overflow:hidden;">

'

`   qp = qp .. '`

<div style="position:absolute;top:-' .. top .. 'px;left:-' .. left .. 'px;width:' .. width .. 'px;">

'

`   qp = qp .. '`[`'``   ``..``   ``bwidth``   ``..``   ``'px`](https://ja.wikipedia.org/wiki/File:Xiangqi_board.svg "fig:' .. bwidth .. 'px")`'`
`   qp = qp .. '`

</div>

'

`   qp = qp .. '`

<div style="position:absolute;top:-' .. top .. 'px;left:-' .. left .. 'px;width:' .. width .. 'px;">

'

`   for i = 0, 9 do`
`       for j = 0, 8 do`
`           local qz = string.gsub(args[i * 9 + j + 3] or '', '\n', '')`
`           qz = string.gsub(qz, ' ', '')`
`           qz = string.gsub(qz, '　', '')`
`           qz = string.gsub(qz, '_', '')`

`           qz = string.gsub(qz, '车', 'rd')`
`           qz = string.gsub(qz, '車', 'rd')`
`           qz = string.gsub(qz, '伡', 'rl')`
`           qz = string.gsub(qz, '俥', 'rl')`
`           qz = string.gsub(qz, '马', 'hd')`
`           qz = string.gsub(qz, '馬', 'hd')`
`           qz = string.gsub(qz, '㐷', 'hl')`
`           qz = string.gsub(qz, '傌', 'hl')`
`           qz = string.gsub(qz, '相', 'el')`
`           qz = string.gsub(qz, '象', 'ed')`
`           qz = string.gsub(qz, '仕', 'al')`
`           qz = string.gsub(qz, '士', 'ad')`
`           qz = string.gsub(qz, '炮', 'cl')`
`           qz = string.gsub(qz, '砲', 'cd')`
`           qz = string.gsub(qz, '兵', 'sl')`
`           qz = string.gsub(qz, '卒', 'sd')`
`           qz = string.gsub(qz, '帅', 'gl')`
`           qz = string.gsub(qz, '帥', 'gl')`
`           qz = string.gsub(qz, '将', 'gd')`
`           qz = string.gsub(qz, '將', 'gd')`
`           qz = string.gsub(qz, '包', 'cd')`

`           qz = string.gsub(qz, '暗', 'rs')`

`           local sx = ((i + 1) * size)`
`           local sy = (j * size)`

`           local bj`

`           ----方框`
`           bj = string.find(qz, '%[')`
`           if bj ~= null then`
`               qp = qp .. '`

<div style="position:absolute;z-index:100;top:' .. sx .. 'px;left:' .. sy .. 'px;width:' .. size .. 'px;height:' .. size .. 'px;">

'

`               qp = qp .. '`

<div style="position:absolute;width:15%;height:15%;top:0px;left:0px;border-top:' .. sizef1 .. 'px solid #0f0;border-left:' .. sizef1 .. 'px solid #0f0;">

</div>

'

`               qp = qp .. '`

<div style="position:absolute;width:15%;height:15%;top:0px;right:0px;border-top:' .. sizef1 .. 'px solid #0f0;border-right:' .. sizef1 .. 'px solid #0f0;">

</div>

'

`               qp = qp .. '`

<div style="position:absolute;width:15%;height:15%;bottom:0px;left:0px;border-bottom:' .. sizef1 .. 'px solid #0f0;border-left:' .. sizef1 .. 'px solid #0f0;">

</div>

'

`               qp = qp .. '`

<div style="position:absolute;width:15%;height:15%;bottom:0px;right:0px;border-bottom:' .. sizef1 .. 'px solid #0f0;border-right:' .. sizef1 .. 'px solid #0f0;">

</div>

'

`               qp = qp .. '`

</div>

'

`           end`
`           qz = string.gsub(qz, '%[', '')`
`           qz = string.gsub(qz, '%]', '')`

`           ----標點`
`           bj = string.find(qz, '%.')`
`           if bj ~= null then`
`               qp = qp .. '`

<div style="position:absolute;z-index:99;top:' .. sx .. 'px;left:' .. sy .. 'px;width:' .. size .. 'px;">

'

`               qp = qp .. '`

<div style="margin:' .. margin .. 'px;width:' .. sizef3 .. 'px;height:' .. sizef3 .. 'px;background-color:#0f0;border-radius:100%;">

</div>

'

`               qp = qp .. '`

</div>

'

`           end`
`           qz = string.gsub(qz, '%.', '')`

`           ----標記叉號`
`           bj = string.find(qz, 'x')`
`           if bj ~= null then`
`               qp = qp .. '`

<div style="position:absolute;z-index:99;top:' .. sx .. 'px;left:' .. sy .. 'px;width:' .. size .. 'px;text-align:center;">

'

`               qp = qp .. '`[`'``   ``..``   ``sizeX``   ``..``   ``'px`](https://ja.wikipedia.org/wiki/File:red_x.svg "fig:' .. sizeX .. 'px")`'`
`               qp = qp .. '`

</div>

'

`           end`
`           qz = string.gsub(qz, 'x', '')`

`           if qz ~= '' then`
`               qp = qp .. '`

<div style="position:absolute;z-index:98;top:' .. sx .. 'px;left:' .. sy .. 'px;width:' .. size .. 'px;">

'

`               qp = qp .. '`[`'``   ``..``   ``size``   ``..``   ``'px`](https://ja.wikipedia.org/wiki/File:Xiangqi_'_.._qz_.._'1.svg "fig:' .. size .. 'px")`'`
`               qp = qp .. '`

</div>

'

`           end`
`       end`
`   end`

`   ----箭头`
`   local arrow = args.arrow`
`   if arrow ~= nil then`
`       qp = qp .. drawArrow(arrow, size)`
`   end`
`   local count = 2`
`   while args['arrow' .. count] ~= nil do`
`       qp = qp .. drawArrow(args['arrow' .. count], size)`
`       count = count + 1`
`   end`

`   qp = qp .. '`

</div>

</div>

<div style="width:' .. width .. 'px">

' .. footer .. '

</div>

</div>

'

`   return qp`

end

function drawArrow(arrow, size)

`   arrow = string.gsub(arrow, ' ', '')`
`   local start = 1`
`   local t = {}`
`   local str = ''`
`   while true do`
`       local pos = string.find(arrow, ',', start, true)`
`       if not pos then`
`           break`
`       end`
`       table.insert(t, string.sub(arrow, start, pos - 1))`
`       start = pos + string.len(',')`
`   end`
`   table.insert(t, string.sub(arrow, start))`
`   t[4] = t[4] * 1`
`   while t[4] < 0 do`
`       t[4] = t[4] + 360`
`   end`
`   while t[4] >= 360 do`
`       t[4] = t[4] - 360`
`   end`

`   ----箭頭的底盤 拿來旋轉方向使用`
`   str = str .. '`

<div style="z-index:108;position:absolute;'
    str = str .. 'left:' .. (t[1] - 1) * size .. 'px;'
    str = str .. 'top:' .. t[2] * size .. 'px;'
    str = str .. 'width:' .. t[3] * size .. 'px;'
    str = str .. 'height:' .. size .. 'px;'
    str = str .. 'transform-origin:' .. size / 2 .. 'px ' .. size / 2 .. 'px;'
    str = str .. 'transform:rotate(' .. t[4] .. 'deg);">

'

`   ----箭頭的直線部分`
`   str = str .. '`

<div style="z-index:108;position:absolute;'
    str = str .. 'left:' .. size / 2 .. 'px;'
    str = str .. 'top:' .. size / 2 - size / 16 .. 'px;'
    str = str .. 'width:' .. (t[3] - 0.4) * size .. 'px;'
    str = str .. 'height:' .. size / 8 .. 'px;'
    str = str .. 'background-color:#0f0;">

</div>

'

`   ----箭頭的頭部分`
`   str = str .. '`

<div style="z-index:108;position:absolute;'
    str = str .. 'left:' .. t[3] * size .. 'px;'
    str = str .. 'top:' .. size / 2 - size / 4 .. 'px;'
    str = str .. 'width:0px;height:0px;'
    str = str .. 'border:' .. size / 4 .. 'px solid transparent;'
    str = str .. 'border-left-color:#0f0;'
    str = str .. 'border-left-width:' .. size / 2 .. 'px;">

</div>

'

`   str = str .. '`

</div>

'

`   return str`

end

return p