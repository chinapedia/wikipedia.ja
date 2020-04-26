> この記事は[モジュール:Month translator](https://ja.wikipedia.org/wiki/モジュール:Month_translator)から翻訳されています。


require ('Module:No globals')

local data = mw.loadData ('Module:month translator/data');

\--\[\[--------------------------\< M O N T H _ X L A T E \>--------------------------------------------------------

{{\#invoke:Sandbox/trappist the monk/month translator|month_xlate|<date>}}

\]\]

local function month_xlate (frame)

`   local t = {};`
`   local day, month, year;`
`   `
`   if 'dump' == frame.args[1] then                                             -- frame.args[1] = 'dump' to dump month_names table; `
`       return mw.dumpObject (data.month_names);`
`   end`
`   `
`   for i, pattern in ipairs (data.patterns) do                                     -- spin through the patterns table looking for a match`
`       local c1, c2, c3;                                                       -- captures in the 'pattern' from the pattern table go here`

`       c1, c2, c3 = mw.ustring.match (mw.text.trim(frame.args[1]), pattern[1]);    -- one or more captures set if source matches patterns[i][1])`
`       if c1 then                                                              -- c1 always set on match`

`           t = {`
`               [pattern[2] or 'x'] = c1,                                       -- fill the table of captures with the captures`
`               [pattern[3] or 'x'] = c2,                                       -- take index names from pattern table and assign sequential captures`
`               [pattern[4] or 'x'] = c3,                                       -- index name may be nil in pattern table so "or 'x'" spoofs a name for this index in this table`
`               };`
`           day = t.d or '';                                                    -- translate table contents to named variables;`
`           month = mw.ustring.lower (t.m or '');                               -- absent table entries are nil so set unused parts to empty string; lowercase for indexing`
`           month = data.override_names[month] or data.month_names[month];      -- replace non-English name with English name from translation tables`
`           year= t.y or '';`

`           if month then`
`               local df = table.concat ({pattern[2], pattern[3], pattern[4]}, ''); -- extract date format from pattern table (pattern[2], pattern[3], pattern[4])`

`               if 'dmy' == df then                                             -- for dmy dates`
`                   return table.concat ({day, month, year}, ' ');              -- assemble an English language dmy date`
`               elseif 'my' == df then                                          -- for month year dates`
`                   return table.concat ({month, year}, ' ');                   -- assemble an English language dmy date`
`               elseif 'mdy' == df then                                         -- for mdy dates`
`                   return string.format ('%s %s, %s', month, day, year);       -- assemble an English language mdy date`
`               elseif 'm' == df then                                           -- must be month (only valid option remaining)`
`                   return month;                                               -- none of the above, return the translated month;`
`               end`
`           end`
`           break;                                                              -- and done; if here found pattern match but did not find non-English month name in month_names{}`
`       end`
`   end `
`   return frame.args[1];                                                       -- if here, couldn't translate so return the original date`

end

\--[--------------------------\< E X P O R T E D F U N C T I O N S \>------------------------------------------](https://ja.wikipedia.org/wiki/--------------------------\<_E_X_P_O_R_T_E_D_F_U_N_C_T_I_O_N_S_\>------------------------------------------ "wikilink")

return {month_xlate = month_xlate};