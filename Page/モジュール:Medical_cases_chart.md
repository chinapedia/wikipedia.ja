> この記事は[モジュール:Medical cases chart](https://ja.wikipedia.org/wiki/モジュール:Medical_cases_chart)から翻訳されています。


local p = {}

function p.buildBars( frame )

`   local barwidth = frame.args.barwidth`
`   local data = frame.args.data`
`   local divisor = frame.args.divisor`
`   local numwidth = frame.args.numwidth`
`   local collapsible = frame.args.collapsible`

`   local lines = mw.text.split( data, '\n' )`
`   local i = 1`

`   if divisor == '' then`
`       local total1, total2 = 0, 0`

`       for parameter in mw.text.gsplit( lines[#lines], ';' ) do`
`           if not string.find( parameter, '^ *%a' ) then`
`               if i == 7 then`
`                   total1 = tonumber( (string.gsub( parameter, '%D', '' )) )`
`                   if not total1 then`
`                       total1 = 0`
`                   end`
`               elseif i == 9 then`
`                   total2 = tonumber( (string.gsub( parameter, '%D', '' )) )`
`                   if not total2 then`
`                       total2 = 0`
`                   end`
`                   break`
`               end`
`               i = i + 1`
`           end`
`       end`
`       divisor = math.max( total1, total2 ) / ( 0.95 * barwidth )`
`   end`
`   local bars = ''`
`   local args`

`   for k, line in pairs( lines ) do`
`       args, i = {}, 1`

`       for parameter in mw.text.gsplit( line, ';' ) do`
`           if string.find( parameter, '^ *%a' ) then`
`               parameter = mw.text.split( parameter, '=' )`
`               args[parameter[1]] = parameter[2]`
`           else`
`               args[i] = parameter`
`               i = i + 1`
`           end`
`       end`
`       args['divisor'] = divisor`
`       args['numwidth'] = numwidth`
`       args['collapsible'] = collapsible`
`       bars = bars .. frame:expandTemplate{ title = 'Medical cases chart/Row', args = args }`
`   end`
`   return bars`

end return p