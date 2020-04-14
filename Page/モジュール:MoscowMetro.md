> この記事は[モジュール:MoscowMetro](https://ja.wikipedia.org/wiki/モジュール:MoscowMetro)から翻訳されています。


local i18n = {

`   NAMES = {`
`       ['1']   = 'ソコーリニチェスカヤ線',-- 'Сокольническая'`
`       ['2']   = 'ザモスクヴォレーツカヤ線', -- 'Замоскворецкая'`
`       ['3']   = 'アルバーツコ＝ポクローフスカヤ線', -- 'Арбатско-Покровская'`
`       ['4']   = 'フィリョーフスカヤ線', -- 'Филёвская'`
`       ['5']   = '環状線', -- 'Кольцевая'`
`       ['6']   = 'カルーシュスコ＝リーシュスカヤ線', -- 'Калужско-Рижская'`
`       ['7']   = 'タガーンスコ＝クラスノプレースネンスカヤ線', -- 'Таганско-Краснопресненская'`
`       ['8']   = 'カリーニンスコ＝ソンツェフスカヤ線', -- 'Калининская'`
`       ['8А']  = 'カリーニンスコ＝ソンツェフスカヤ線', -- 'Солнцевская'`
`       ['9']   = 'セルプホーフスコ＝チミリャーゼフスカヤ線', -- 'Серпуховско-Тимирязевская'`
`       ['10']  = 'リュビリーンスコ＝ドミトロフスカヤ線', -- 'Люблинско-Дмитровская' リュブリーンスコだが他記事に合わせる`
`       ['11']  = '大環状線', -- 'Большая кольцевая'`
`       ['11А'] = 'カホーフスカヤ線', -- 'Каховская'`
`       ['12']  = 'ブートフスカヤ線', -- 'Бутовская'`
`       ['13']  = 'モスクワモノレール', -- 'Монорельс'`
`       ['14']  = 'モスクワ中央環状線', -- 'Московское центральное кольцо'`
`       ['15']  = 'ネクラソフスカヤ線', -- 'Некрасовская'`
`       ['16']  = 'コムナルスカヤ線', -- 'Коммунарская'`
`       ['D1']  = 'MCD-1', -- 'МЦД-1'`
`       ['D2']  = 'MCD-2', -- 'МЦД-2'`
`       ['D3']  = 'MCD-3', -- 'МЦД-3'`
`       ['D4']  = 'MCD-4', -- 'МЦД-4'`
`       ['D5']  = 'MCD-5', -- 'МЦД-5'`
`   },`
`   html = {`
`       icon_fmt = '`<span title="%s">[`%spx`](https://ja.wikipedia.org/wiki/File:Moskwa_Metro_Line_%s.svg "fig:%spx")</span>`', -- parameters: alt, linenum, icon size, alt, link`
`       text_fmt = '`[<span style="display:inline-block;line-height:%spx;height:%spx;font-size:%spx;font-style:normal;font-weight:bold;background:#%s;color:white;white-space:nowrap;text-align:center" title="%s">` %s `</span>](https://ja.wikipedia.org/wiki/%s "wikilink")`', --`[`parameters:``   ``link,``   ``icon``   ``size,``   ``icon``   ``size,``   ``icon``   ``size``   ``-``   ``3,``   ``color,``   ``alt,``   ``linenum`](https://ja.wikipedia.org/wiki/parameters:_link,_icon_size,_icon_size,_icon_size_-_3,_color,_alt,_linenum "wikilink")
`       small = '`<span style="font-size:85%%">`%s`</span>`',`
`       style = '`<span style="%s">`%s`</span>`',`
`       sortkey = '`<span style="display:none" class="sortkey">`%s`</span>`',`
`   },`
`   text = {`
`       transfer = 'Переход на станцию %s %s',`
`       CPIC = 'Кросс-платформенная пересадка на станцию %s %s',`
`       dab = ' (станция метро)',`
`   },`
`   default = {`
`       icon_size = '15'`
`   }`

} i18n.NAMES\['КалЛ'\] = i18n.NAMES\['8'\]; i18n.NAMES\['КСЛ'\] = i18n.NAMES\['8'\]; i18n.NAMES\['СолЛ'\] = i18n.NAMES\['8А'\]; i18n.NAMES\['ТПК'\] = i18n.NAMES\['11'\]; i18n.NAMES\['БКЛ'\] = i18n.NAMES\['11'\]; i18n.NAMES\['L1'\] = i18n.NAMES\['12'\]; i18n.NAMES\['Л1'\] = i18n.NAMES\['12'\]; --для совместимости с предыдущими версиями шаблонов i18n.NAMES\['МОЖД'\] = i18n.NAMES\['14'\]; i18n.NAMES\['МЦК'\] = i18n.NAMES\['14'\]; i18n.NAMES\['КожЛ'\] = i18n.NAMES\['15'\]; i18n.NAMES\['НЛ'\] = i18n.NAMES\['15'\]; i18n.NAMES\['КомЛ'\] = i18n.NAMES\['16'\];

i18n.line = function(num) -- название линии в именительном падеже

`   if num == '13' then return 'Московский монорельс'`
`   elseif num == '14' then return 'Московское центральное кольцо'`
`   elseif num == 'D1' then return 'МЦД-1'`
`   elseif num == 'D2' then return 'МЦД-2'`
`   elseif num == 'D3' then return 'МЦД-3'`
`   elseif num == 'D4' then return 'МЦД-4'`
`   elseif num == 'D5' then return 'МЦД-5'`
`   else return i18n.NAMES[num] .. ' линия'`
`   end`

end

i18n.link = function(num) -- ссылка на страницу линии

`   if num == '5' then return i18n.NAMES[num] .. ' линия (Москва)'`
`   else return i18n.line(num)`
`   end`

end

i18n.ofLine = function(num) -- название линии в родительном падеже ("пересадка на станцию ... ... линии")

`   if num == 'ТПК' or num == '11' then return 'Большой кольцевой линии'`
`   elseif num == '13' then return 'Московского монорельса'`
`   elseif num == '14' then return 'Московского центрального кольца'`
`   elseif num == 'D1' then return 'МЦД-1'`
`   elseif num == 'D2' then return 'МЦД-2'`
`   elseif num == 'D3' then return 'МЦД-3'`
`   elseif num == 'D4' then return 'МЦД-4'`
`   elseif num == 'D5' then return 'МЦД-5'`
`   else return mw.ustring.sub(i18n.NAMES[num], 1, -3) .. 'ой линии'`
`   end`

end

local COLORS = { -- МЕНЯЙТЕ ЗНАЧЕНИЯ ЦВЕТОВ ТОЛЬКО ПОСЛЕ ОБСУЖДЕНИЯ в [ПРО:МОСМЕТРО](https://ja.wikipedia.org/wiki/ПРО:МОСМЕТРО "wikilink")

`   ['1']   = 'EF161E', -- Сокольническая`
`   ['2']   = '2DBE2C', -- Замоскворецкая`
`   ['3']   = '0078BE', -- Арбатско-Покровская`
`   ['4']   = '00BFFF', -- Филёвская`
`   ['5']   = '8D5B2D', -- Кольцевая`
`   ['6']   = 'ED9121', -- Калужско-Рижская`
`   ['7']   = '800080', -- Таганско-Краснопресненская`
`   ['8']   = 'FFD702', -- Калининская`
`   ['8А']  = 'FFD702', -- Солнцевская`
`   ['9']   = '999999', -- Серпуховско-Тимирязевская`
`   ['10']  = '99CC00', -- Люблинско-Дмитровская`
`   ['11']  = '82C0C0', -- Большая кольцевая`
`   ['11А'] = '82C0C0', -- Каховская`
`   ['12']  = 'A1B3D4', -- Бутовская`
`   ['13']  = '9999FF', -- Московский монорельс`
`   ['14']  = 'FFFFFF', -- Московское центральное кольцо`
`   ['15']  = 'DE64A1', -- Некрасовская`
`   ['16']  = 'D8D8D8', -- Коммунарская (временно)`
`   ['D1']  = 'f6a600', -- МЦД-1`
`   ['D2']  = 'e74280', -- МЦД-2`
`   ['D3']  = 'e95b0c', -- МЦД-3`
`   ['D4']  = '40b280', -- МЦД-4`
`   ['D5']  = '77b729', -- МЦД-5`
`   ['0']   = '231F20', -- для всех остальных планирующихся линий`

} COLORS\['КСЛ'\] = COLORS\['8'\]; COLORS\['КалЛ'\] = COLORS\['8'\]; COLORS\['СолЛ'\] = COLORS\['8А'\]; COLORS\['Солнцевская'\] = COLORS\['8А'\]; COLORS\['ТПК'\] = COLORS\['11'\]; COLORS\['БКЛ'\] = COLORS\['11'\]; COLORS\['L1'\] = COLORS\['12'\]; COLORS\['Л1'\] = COLORS\['12'\]; COLORS\['М1'\] = COLORS\['13'\]; COLORS\['МОЖД'\] = COLORS\['14'\]; COLORS\['МЦК'\] = COLORS\['14'\]; COLORS\['КожЛ'\] = COLORS\['15'\]; COLORS\['Кожуховская'\] = COLORS\['КожЛ'\]; COLORS\['НЛ'\] = COLORS\['15'\]; COLORS\['КомЛ'\] = COLORS\['16'\];

function IconByNum(num)

`   if num == 'КожЛ' then return nil`
`   elseif num == 'КСЛ' or num == 'КалЛ' then return '8'`
`   elseif num == 'СолЛ' then return '8А'`
`   elseif num == 'ТПК'  then return '11'`
`   elseif num == 'М1'   then return '13'`
`   elseif num == 'МОЖД' then return '14'`
`   else return num`
`   end`

end

local p = {}

function p.ColorByNum(frame)

`   return COLORS[mw.text.trim(frame.args[1] or '')] or '`[`Категория:Википедия:Статьи``   ``с``   ``неверно``   ``заданными``   ``параметрами``   ``модуля``   ``MoscowMetro`](https://ja.wikipedia.org/wiki/Категория:Википедия:Статьи_с_неверно_заданными_параметрами_модуля_MoscowMetro "wikilink")`'`

end

function p.NameByNum(frame)

`   return i18n.NAMES[mw.text.trim(frame.args[1] or '')] or '`[`Категория:Википедия:Статьи``   ``с``   ``неверно``   ``заданными``   ``параметрами``   ``модуля``   ``MoscowMetro`](https://ja.wikipedia.org/wiki/Категория:Википедия:Статьи_с_неверно_заданными_параметрами_модуля_MoscowMetro "wikilink")`'`

end

function p.interchange(frame)

`   local num, station, station_dabbed, CPIC = frame.args['line'] or '', frame.args['station'] or '', frame.args['station_dabbed'] or '', frame.args['CPIC'] or '' ~= ''`
`   local icon_size, alt, text, small, style = frame.args['size'] or '', frame.args['alt'] or '', frame.args['text'] or '', frame.args['small'] or '', frame.args['style'] or ''`
`   local icon, station_stripped`
`   if not i18n.NAMES[num] then return '`[`Категория:Википедия:Статьи``   ``с``   ``неверно``   ``заданными``   ``параметрами``   ``модуля``   ``MoscowMetro`](https://ja.wikipedia.org/wiki/Категория:Википедия:Статьи_с_неверно_заданными_параметрами_модуля_MoscowMetro "wikilink")`' end`
`   local iconN = IconByNum(num)`
`   if icon_size == '' then`
`       icon_size = i18n.default.icon_size`
`   elseif mw.ustring.sub(icon_size, -2 ) == 'px' then`
`       icon_size = mw.ustring.sub(icon_size, 1, -3 )`
`   end`
`   if alt == '' then`
`       if station ~= '' then`
`           alt = mw.ustring.format(i18n.text[CPIC ~= '' and 'CPIC' or 'transfer'], station, i18n.ofLine(num))`
`       elseif station_dabbed ~= '' then`
`           station_stripped = mw.ustring.match(station_dabbed, '(.-) %(') or station_dabbed`
`           alt = mw.ustring.format(i18n.text[CPIC ~= '' and 'CPIC' or 'transfer'], station_stripped, i18n.ofLine(num))`
`       else`
`           alt = i18n.line(num)`
`       end`
`   elseif station_dabbed ~= '' then`
`       station_stripped = mw.ustring.match(station_dabbed, '(.-) %(') or station_dabbed`
`   end`
`   local link = text == '' and (station_dabbed ~= '' and station_dabbed or (station ~= '' and station .. i18n.text.dab or i18n.link(num))) or i18n.link(num)`
`   if iconN then`
`       icon = mw.ustring.format(i18n.html.sortkey, mw.ustring.len(iconN) == 2 and iconN or '0' .. iconN) .. mw.ustring.format(i18n.html.icon_fmt, alt, iconN, icon_size, alt, link)`
`   else`
`       icon = mw.ustring.format(i18n.html.text_fmt, link, icon_size, icon_size, tonumber(icon_size) - 3, COLORS[num], alt, num)`
`   end`
`   if text == '' then return icon end`
`   `
`   function text2()`
`       return text == '2' and i18n.NAMES[num] or i18n.line(num)`
`   end`
`   `
`   local result = ''`
`   if station_dabbed ~= '' then`
`       result = '`[`'``   ``..``   ``(station``   ``~=``   ``''``   ``and``   ``station``   ``or``   ``station_stripped)``   ``..``   ``'`](https://ja.wikipedia.org/wiki/'_.._station_dabbed_.._' "wikilink")`'`
`   elseif station ~= '' then`
`       result = '`[`'``   ``..``   ``station``   ``..``   ``'`](https://ja.wikipedia.org/wiki/'_.._station_.._i18n.text.dab_.._' "wikilink")`'`
`   elseif link == mw.title.getCurrentTitle().prefixedText then`
`       result = style ~= '' and mw.ustring.format(i18n.html.style, style, text2()) or text2()`
`   elseif text == '2' and num ~= 'ТПК' or style ~= '' or num == '5' then`
`       result = '`[`'``   ``..``   ``(style``   ``~=``   ``''``   ``and``   ``mw.ustring.format(i18n.html.style,``   ``style,``   ``text2())``   ``or``   ``text2())``   ``..``   ``'`](https://ja.wikipedia.org/wiki/'_.._link_.._' "wikilink")`'`
`   else`
`       result = '`[`'``   ``..``   ``link``   ``..``   ``'`](https://ja.wikipedia.org/wiki/'_.._link_.._' "wikilink")`'`
`   end`
`   if small ~= '' then result = mw.ustring.format(i18n.html.small, result) end`
`   return (not iconN and station == '' and station_dabbed == '' and '' or icon .. ' ') .. result`

end

return p