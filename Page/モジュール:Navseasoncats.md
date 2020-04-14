> この記事は[モジュール:Navseasoncats](https://ja.wikipedia.org/wiki/モジュール:Navseasoncats)から翻訳されています。


local p = {}

local errors = '' local nexistingcats = 0 local currtitle = mw.title.getCurrentTitle() local testcasecolon = '' local testcases = (currtitle.subpageText == 'testcases') if testcases then testcasecolon = ':' end local navborder = true local followRs = true local listall = false local listofalllinks = {} local skipgaps = false local misctrackingcats = {

`   '', -- [1] placeholder for '`
`   '', -- [2] placeholder for '`
`   '', -- [3] placeholder for `
`   '', -- [4] placeholder for `
`   '', -- [5] placeholder for `
`   '', -- [6] placeholder for `
`   '', -- [7] placeholder for `
`   '', -- [8] placeholder for `
`   '', -- [9] placeholder for `
`   '', --[10] placeholder for `
`   '', --[11] placeholder for `
`   '', --[12] placeholder for `
`   '', --[13] placeholder for `
`   '', --[14] placeholder for `
`   '', --[15] placeholder for `

} local avoidself = (currtitle.text \~= 'Navseasoncats' and --avoid self

`                   currtitle.text ~= 'Navseasoncats/doc' and      --avoid self`
`                   currtitle.text ~= 'Navseasoncats/sandbox' and  --avoid self`
`                   (currtitle.nsText ~= 'Template' or testcases)) --avoid nested transclusion errors (i.e. ``)`

\--[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink") --[Utility & category functions](https://ja.wikipedia.org/wiki/Utility_&_category_functions "wikilink") --[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink")

\--Error message handling --Also used by . function p.errorclass( msg )

`   return mw.text.tag( 'span', {class='error mw-ext-cite-error'}, '`<b>`Error!`</b>` '..string.gsub(msg, '&#', '&#') )`

end

\--Failure handling --Also used by . function p.failedcat( errors, sortkey )

`   if avoidself then`
`       return (errors or '')..'***Navseasoncats failed to generate navbox***'..`
`              '`[`'..(sortkey``   ``or``   ``'O')..'`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_failed_to_generate_navbox "wikilink")`'`
`   end`
`   return ''`

end

\--Check for nav_\*() navigational isolation (not necessarily an error). --Used by all nav_\*(). function isolatedcat()

`   if nexistingcats == 0 and avoidself then`
`       misctrackingcats[7] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``isolated`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_isolated "wikilink")`'`
`   end`

end

\-- --Now unused, in favor of catlinkfollowr(). -- --Similar to : make a piped link to a category, if it exists; --if it doesn't exist, just display the greyed link title without linking. function catlink( catname, displaytext )

`   catname = mw.text.trim(catname or '')`
`   displaytext = mw.text.trim(displaytext or '')`
`   local grey = '#888'`
`   local disp = catname`
`   if displaytext ~= '' then --use 'displaytext' parameter if present`
`       disp = mw.ustring.gsub(displaytext, '%s+%(.+$', ''); --strip any trailing disambiguator`
`   end`
`   `
`   local exists = mw.title.new( catname, 'Category' ).exists`
`   if exists then`
`       nexistingcats = nexistingcats + 1`
`       return '`[`'..disp..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")`'`
`   else`
`       return '`<span style="color:'..grey..'">`'..disp..'`</span>`'`
`   end`

end

\--Similar to catlink() but follows s. --Returns { \<\#R target navelement\>, \<basetext of \#R target\> } if  followed; --returns { <original navelement>, nil } otherwise. --Used by all nav_\*(). function catlinkfollowr( catname, displaytext )

`   catname = mw.text.trim(catname or '')`
`   displaytext = mw.text.trim(displaytext or '')`
`   local grey = '#888'`
`   local disp = catname`
`   if displaytext ~= '' then --use 'displaytext' parameter if present`
`       disp = mw.ustring.gsub(displaytext, '%s+%(.+$', ''); --strip any trailing disambiguator`
`   end`
`   `
`   local link, nilorR`
`   local exists = mw.title.new( catname, 'Category' ).exists`
`   if exists then`
`       nexistingcats = nexistingcats + 1`
`       if followRs then`
`           local R = rtarget(catname)`
`           if R == catname then --no #R`
`               link = '`[`'..disp..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")`'`
`               nilorR = nil`
`           else --#R followed`
`               link = '`[`'..disp..'`](https://ja.wikipedia.org/wiki/Category:'..R..' "wikilink")`'`
`               nilorR = R`
`           end`
`       else`
`           link = '`[`'..disp..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")`'`
`           nilorR = nil`
`       end`
`   else`
`       link = '`<span style="color:'..grey..'">`'..disp..'`</span>`'`
`       nilorR = nil`
`       --return { '`[`'..disp..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")`', nil } --for debugging`
`   end`
`   `
`   if listall then`
`       if nilorR then --#R followed`
`           table.insert( listofalllinks, '`[`:Category:'..catname..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")` → '..'`[`:Category:'..nilorR..'`](https://ja.wikipedia.org/wiki/Category:'..nilorR..' "wikilink")` ('..link..')' )`
`       else --no #R`
`           table.insert( listofalllinks, '`[`:Category:'..catname..'`](https://ja.wikipedia.org/wiki/Category:'..catname..' "wikilink")` ('..link..')' )`
`       end`
`   end`
`   `
`   return { link, nilorR }`

end

\--Returns the target of , if it exists, else returns the original cat. --Used by catlinkfollowr(), and so indirectly by all nav_\*(). function rtarget( cat )

`   local catcontent = mw.title.new( cat or '', 'Category' ):getContent()`
`   if string.match( catcontent or '', '{{ *[Cc]at' ) then`
`       local regex = {`
`           --from `<https://dispenser.info.tm/~dispenser/cgi-bin/rdcheck.py?page=Template:Category_redirect>
`           --the following 11 pages (7 condensed) redirect to `[`Template:Category``   ``redirect`](https://ja.wikipedia.org/wiki/Template:Category_redirect "wikilink")` (as of 6/2019):`
`           { '1', '{{ *[Cc]ategory *[Rr]edirect' }, --most likely match 1st`
`           { '2', '{{ *[Cc]at *redirect' },         --444+240 transclusions`
`           { '3', '{{ *[Cc]at *redir' },            --8+3`
`           { '4', '{{ *[Cc]ategory *move' },        --6`
`           { '5', '{{ *[Cc]at *red' },              --6`
`           { '6', '{{ *[Cc]atr' },                  --4`
`           { '7', '{{ *[Cc]at *move' },             --0`
`       }`
`       for k, v in pairs (regex) do`
`           local rtarget = mw.ustring.match( catcontent, v[2]..'%s*|%s*([^|}]+)' )`
`           if rtarget then`
`               rtarget = mw.ustring.gsub(rtarget, '^1%s*=%s*', '')`
`               rtarget = string.gsub(rtarget, '^[Cc]ategory:', '')`
`               return rtarget`
`           end`
`       end`
`   end`
`   return cat`

end

\--Returns a numbered list of all s followed by catlinkfollowr() -\> rtarget(). --Used by all nav_\*(). function listalllinks()

`   local nl = '\n# '`
`   local out = ''`
`   if currtitle.nsText == 'Category' then`
`       errors = p.errorclass('The `<b>`|list-followed-redirects=yes`</b>` parameter/utility '..`
`                           'should not be saved in category space, only previewed.')`
`       out = p.failedcat(errors, 'Z')`
`   end`
`   if listofalllinks[1] then`
`       return out..nl..table.concat(listofalllinks, nl)`
`   else`
`       return out..nl..'No links found!?'`
`   end`

end

\--Returns an unsigned string of the 1-4 digit decade ending in "0", else error. --Used by nav_decade() only. function sterilizedec( decade )

`   if decade == nil or decade == '' then`
`       return nil`
`   end`
`   `
`   local dec = string.match(decade, '^[-%+]?(%d?%d?%d?0)$') or `
`               string.match(decade, '^[-%+]?(%d?%d?%d?0)%D')`
`   if dec then`
`       return dec`
`   else`
`       --fix 2-4 digit decade`
`       local decade_fixed234 = string.match(decade, '^[-%+]?(%d%d?%d?)%d$') or`
`                               string.match(decade, '^[-%+]?(%d%d?%d?)%d%D')`
`       if decade_fixed234 then`
`           return decade_fixed234..'0'`
`       end`
`       `
`       --fix 1-digit decade`
`       local decade_fixed1   = string.match(decade, '^[-%+]?(%d)$') or`
`                               string.match(decade, '^[-%+]?(%d)%D')`
`       if decade_fixed1 then`
`           return '0'`
`       end`
`       `
`       --unfixable`
`       errors = 'sterilizedec() error'`
`       return nil`
`   end`

end

\--Check for nav_hyphen default gap size + isolatedcat() (not necessarily an error). --Used by nav_hyphen() only. function defaultgapcat( bool )

`   if bool and nexistingcats == 0 and avoidself then`
`       --using "nexistingcats > 0" isn't as useful, since the default gap size obviously worked`
`       misctrackingcats[8] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``default``   ``season``   ``gap``   ``size`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_default_season_gap_size "wikilink")`'`
`   end`

end

\--12 -\> 12th, etc. --Used by nav_nordinal(), nav_wordinal(), and . function p.addord( i )

`   if tonumber(i) then`
`       local s = tostring(i)`
`       `
`       local tens = string.match(s, '1%d$')`
`       if    tens then return s..'th' end`
`       `
`       local  ones = string.match(s, '%d$')`
`       if     ones == '1' then return s..'st'`
`       elseif ones == '2' then return s..'nd'`
`       elseif ones == '3' then return s..'rd' end`
`       `
`       return s..'th'`
`   end`
`   return i`

end

\--[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink") --[Formerly separated templates/modules](https://ja.wikipedia.org/wiki/Formerly_separated_templates/modules "wikilink") --[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink")

\--[==========================={{ nav_hyphen }}=============================](https://ja.wikipedia.org/wiki/==========================={{_nav_hyphen_}}============================= "wikilink")

function nav_hyphen( start, hyph, finish, firstpart, lastpart, minseas, maxseas, testgap )

`   --Expects a PAGENAME of the form "Some sequential 2015–16 example cat", where `
`   --  start     = 2015`
`   --  hyph      = –`
`   --  finish    = 16 (sequential years can be abbreviated, but others must be full year, i.e. "2001–2005")`
`   --  firstpart = Some sequential`
`   --  lastpart  = example cat`
`   --  minseas   = 1800 ('min' starting season shown; optional)`
`   --  maxseas   = 1999 ('max' starting season shown; optional; 1999 will show 1999-00)`
`   --  testgap   = 0 (testcasegap parameter for easier testing; optional)`
`   `
`   --sterilize start`
`   if string.match(start or '', '^%d%d?%d?%d?$') == nil then --1-4 digits, AD only`
`       local start_fixed = mw.ustring.match(start or '', '^%s*(%d%d?%d?%d?)%D')`
`       if start_fixed then`
`           start = start_fixed`
`       else`
`           errors = p.errorclass('Function nav_hyphen can\'t recognize the number "'..(start or '')..'" '..`
`                               'in the first part of the "season" that was passed to it. '..`
`                               'For e.g. "2015–16", "2015" is expected via "|2015|–|16|".')`
`           return p.failedcat(errors, 'H')`
`       end`
`   end`
`   local nstart = tonumber(start)`
`   `
`   --en dash check`
`   if hyph ~= '–' then`
`       misctrackingcats[3] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``range``   ``not``   ``using``   ``en``   ``dash`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_range_not_using_en_dash "wikilink")`' --nav still processable, but track`
`   end`
`   `
`   --sterilize finish`
`   if string.match(finish or '', '^%d+$') == nil then`
`       local finish_fixed = mw.ustring.match(finish or '', '^%s*(%d%d?%d?%d?)%D')`
`       if finish_fixed then`
`           finish = finish_fixed`
`       else`
`           errors = p.errorclass('Function nav_hyphen can\'t recognize "'..(finish or '')..'" '..`
`                               'in the second part of the "season" that was passed to it. '..`
`                               'For e.g. "2015–16", "16" is expected via "|2015|–|16|".')`
`           return p.failedcat(errors, 'I')`
`       end`
`   else`
`       if string.len(finish) >= 5 then`
`           errors = p.errorclass('The second part of the season passed to function nav_hyphen should only be four or fewer digits, not "'..(finish or '')..'". '..`
`                               'See `[`MOS:DATERANGE`](https://ja.wikipedia.org/wiki/MOS:DATERANGE "wikilink")` for details.')`
`           return p.failedcat(errors, 'J')`
`       end`
`   end`
`   local nfinish = tonumber(finish)`
`   `
`   --sterilize min/max`
`   local nminseas = tonumber(minseas) or -9999 --same behavior as nav_year`
`   local nmaxseas = tonumber(maxseas) or  9999 --same behavior as nav_year`
`   if nminseas > nstart then nminseas = nstart end`
`   if nmaxseas < nstart then nmaxseas = nstart end`
`   `
`   local lspace = ' ' --assume a leading space (most common)`
`   local tspace = ' ' --assume a trailing space (most common)`
`   if string.match(firstpart, '%($') then lspace = '' end --DNE for "Madrid city councillors (2007–2011)"-type cats`
`   if string.match(lastpart,  '^%)') then tspace = '' end --DNE for "Madrid city councillors (2007–2011)"-type cats`
`   `
`   --calculate term length/intRAseason size & finishing year`
`   local t = 1`
`   while t <= 10 do`
`       local nish = nstart + t --use switchADBC to flip this sign to work for years BC`
`       if nish == nfinish or string.match(nish, '%d?%d$') == finish then`
`           break`
`       end`
`       if t == 10 then`
`           errors = p.errorclass('Function nav_hyphen can\'t determine a reasonable term length for "'..start..hyph..finish..'".')`
`           return p.failedcat(errors, 'K')`
`       end`
`       t = t + 1`
`   end`
`   `
`   --apply MOS:DATERANGE to parent`
`   local lenstart = string.len(start)`
`   local lenfinish = string.len(finish)`
`   if lenstart == 4 then --"2001–"`
`       if t == 1 then --"2001–02" & "2001–2002" both allowed`
`           if lenfinish ~= 2 and lenfinish ~= 4 then`
`               errors = p.errorclass('The second part of the season passed to function nav_hyphen should be two or four digits, not "'..finish..'".')`
`               return p.failedcat(errors, 'L')`
`           end`
`       else --"2001–2005" is required for t > 1; track "2001–05"; anything else = error`
`           if lenfinish == 2 then`
`               if avoidself then`
`                   misctrackingcats[4] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``range``   ``abbreviated`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_range_abbreviated "wikilink")`'`
`               end`
`           elseif lenfinish ~= 4 then`
`               errors = p.errorclass('The second part of the season passed to function nav_hyphen should be four digits, not "'..finish..'".')`
`               return p.failedcat(errors, 'M')`
`           end`
`       end`
`       if finish == '00' and avoidself then --full year required regardless of term length`
`           misctrackingcats[4] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``range``   ``abbreviated`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_range_abbreviated "wikilink")`'`
`       end`
`   end`
`   `
`   --calculate intERseason gap size`
`   local hgapdefault = 0 --assume & start at the most common case: 2001–02, 2002–03, etc.`
`   local hgap = hgapdefault`
`   local hgap_success = false`
`   while hgap <= 5 do --verify`
`       local prevseason2 = firstpart..lspace..(nstart-t-hgap)..hyph..string.match(nstart-hgap, '%d?%d$')    ..tspace..lastpart`
`       local nextseason2 = firstpart..lspace..(nstart+t+hgap)..hyph..string.match(nstart+2*t+hgap, '%d?%d$')..tspace..lastpart`
`       local prevseason4 = firstpart..lspace..(nstart-t-hgap)..hyph..(nstart-hgap)    ..tspace..lastpart`
`       local nextseason4 = firstpart..lspace..(nstart+t+hgap)..hyph..(nstart+2*t+hgap)..tspace..lastpart`
`       if t == 1 then --test abbreviated range first, then full range`
`           if mw.title.new(prevseason2, 'Category').exists or --use 'or', in case we're at the edge of the cat structure,`
`              mw.title.new(nextseason2, 'Category').exists or --or we hit a "–00"/"–2000" situation on one side`
`              mw.title.new(prevseason4, 'Category').exists or`
`              mw.title.new(nextseason4, 'Category').exists`
`           then`
`               hgap_success = true`
`               break`
`           end`
`       elseif t > 1 then --test full range first, then abbreviated range`
`           if mw.title.new(prevseason4, 'Category').exists or --use 'or', in case we're at the edge of the cat structure,`
`              mw.title.new(nextseason4, 'Category').exists or --or we hit a "–00"/"–2000" situation on one side`
`              mw.title.new(prevseason2, 'Category').exists or `
`              mw.title.new(nextseason2, 'Category').exists`
`           then`
`               hgap_success = true`
`               break`
`           end`
`       end`
`       hgap = hgap + 1`
`   end`
`   if hgap_success == false then`
`       hgap = tonumber(testgap) or hgapdefault --tracked via defaultgapcat()`
`   end`
`   `
`   --begin navhyphen`
`   local navh = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = -3`
`   while i <= 3 do`
`       local from  = nstart + i*(t+hgap)`
`       local from2 = string.match(from, '%d?%d$')`
`       local to  = tostring(from+t)`
`       local to2 = string.match(to, '%d?%d$')`
`       local tofinal = to2 --assume t=1 and abbreviated 'to' (the most common case)`
`       if t > 1 or         --per MOS:DATERANGE (e.g. 1999-2004)`
`         (from2 - to2) > 0 --century transition exception (e.g. 1999–2000)`
`       then`
`           tofinal = to --default to the MOS-correct format, in case no fallbacks found`
`       end`
`       `
`       --check existance of 4-digit, MOS-correct range, with abbreviation fallback`
`       if t > 1 and string.len(from) == 4 then --e.g. 1999-2004`
`           --determine which link exists (full or abbr)`
`           local full = firstpart..lspace..from..hyph..tofinal..tspace..lastpart`
`           if not mw.title.new( full, 'Category' ).exists then`
`               local abbr = firstpart..lspace..from..hyph..to2..tspace..lastpart`
`               if mw.title.new( abbr, 'Category' ).exists then`
`                   tofinal = to2 --rv to MOS-incorrect format; if full AND abbr DNE, then tofinal is still in its MOS-correct format`
`               end`
`           end`
`       elseif t == 1 then --full-year consecutive ranges are also allowed`
`           local abbr = firstpart..lspace..from..hyph..tofinal..tspace..lastpart --assume tofinal is in abbr format`
`           if not mw.title.new( abbr, 'Category' ).exists and tofinal ~= to then`
`               local full = firstpart..lspace..from..hyph..to..tspace..lastpart`
`               if mw.title.new( full, 'Category' ).exists then`
`                   tofinal = to --if abbr AND full DNE, then tofinal is still in its abbr format (unless it's a century transition)`
`               end`
`           end`
`       end`
`       `
`       --populate navh`
`       if i ~= 0 then --left/right navh`
`           local orig = firstpart..lspace..from..hyph..tofinal..tspace..lastpart`
`           local disp = from..hyph..tofinal`
`           local catlink = catlinkfollowr(orig, disp)`
`           `
`           if catlink[2] and avoidself then --a `` was followed, figure out why`
`               local origbase = string.gsub(orig, '%d+[–-]%d+', '')`
`               local rtarbase = string.gsub(catlink[2], '%d+[–-]%d+', '')`
`               if origbase ~= rtarbase then`
`                   misctrackingcats[5] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``range``   ``redirected``   ``(base``   ``change)`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_range_redirected_\(base_change\) "wikilink")`'`
`               else`
`                   misctrackingcats[6] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``range``   ``redirected``   ``(MOS)`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_range_redirected_\(MOS\) "wikilink")`'`
`               end`
`           end`
`           `
`           if from >= 0 and nminseas <= from and from <= nmaxseas then`
`               navh = navh..'*'..catlink[1]..'\n'`
`           else`
`               local hidden = '`<span style="visibility:hidden">`'..disp..'`</span>`'`
`               navh = navh..'*'..hidden..'\n'`
`               if listall then`
`                   listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`               end`
`           end`
`       else --center navh`
`           navh = navh..'*`<b>`'..start..hyph..finish..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   defaultgapcat(not hgap_success)`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navh..'|}'`
`   end`

end

\--[=========================={{ nav_tvseason }}============================](https://ja.wikipedia.org/wiki/=========================={{_nav_tvseason_}}============================ "wikilink")

function nav_tvseason( firstpart, tv, lastpart, maximumtv )

`   --Expects a PAGENAME of the form "Futurama (season 1) episodes", where `
`   --  firstpart = Futurama (season `
`   --  tv        = 1`
`   --  lastpart  = ) episodes`
`   --  maximumtv = 7 ('max' tv season parameter; optional)`
`   tv = tonumber(tv)`
`   if tv == nil then`
`       errors = p.errorclass('Function nav_tvseason can\'t recognize the TV season number sent to its 2nd parameter.')`
`       return p.failedcat(errors, 'T')`
`   end`
`   `
`   local maxtv = tonumber(maximumtv) or 9999 --allow +/- qualifier`
`   if maxtv < tv then maxtv = tv end --input error; maxtv should be >= parent`
`   `
`   local loffset = 0 --left-offset`
`   --if tv <= 5 then loffset = 6 - tv end --commented to behave similarly to the other nav_* functions`
`   `
`   --begin navtvseason`
`   local navt = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = (-5 + loffset)`
`   while i <= (5 + loffset) do`
`       local t = tv + i`
`       if i ~= 0 then --left/right navt`
`           local catlink = catlinkfollowr( firstpart..' '..t..lastpart, t )`
`           if (t >= 1 and t <= maxtv) then --hardcode mintv`
`               if catlink[2] and avoidself then --a `` was followed`
`                   misctrackingcats[14] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``TV``   ``season``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_TV_season_redirected "wikilink")`'`
`               end`
`               navt = navt..'*'..catlink[1]..'\n'`
`           else`
`               local hidden = '`<span style="visibility:hidden">`'..'0'..'`</span>`' --'0' to maintain dot spacing`
`               navt = navt..'*'..hidden..'\n'`
`               if listall then`
`                   listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`               end`
`           end`
`       else --center navt`
`           navt = navt..'*`<b>`'..tv..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navt..'|}'`
`   end`

end

\--[==========================={{ nav_decade }}=============================](https://ja.wikipedia.org/wiki/==========================={{_nav_decade_}}============================= "wikilink")

function nav_decade( firstpart, decade, lastpart, mindecade, maxdecade )

`   --Expects a PAGENAME of the form "Some sequential 2000 example cat", where `
`   --  firstpart = Some sequential`
`   --  decade    = 2000`
`   --  lastpart  = example cat`
`   --  mindecade = 1800 ('min' decade parameter; optional)`
`   --  maxdecade = 2020 ('max' decade parameter; optional; defaults to next decade)`
`   `
`   --sterilize dec`
`   local dec = sterilizedec(decade)`
`   if errors ~= '' then`
`       errors = p.errorclass('Function nav_decade was sent "'..(decade or '')..'" as its 2nd parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0".')`
`       return p.failedcat(errors, 'D')`
`   end`
`   local ndec = tonumber(dec)`
`   `
`   --sterilize mindecade & determine AD/BC`
`   local mindefault = '-9999'`
`   local mindec = sterilizedec(mindecade) --returns a tostring(unsigned int), or nil + errors`
`   if mindec then`
`       if string.match(mindecade, '-%d') or `
`          string.match(mindecade, 'BC')`
`       then`
`           mindec = '-'..mindec --better +/-0 behavior with strings (0-initialized int == "-0" string...)`
`       end`
`   elseif errors ~= '' then`
`       errors = p.errorclass('Function nav_decade was sent "'..(mindecade or '')..'" as its 4th parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0", the earliest decade to be shown.')`
`       return p.failedcat(errors, 'E')`
`   else`
`       mindec = mindefault --tonumber() later, after error checks`
`   end`
`   `
`   --sterilize maxdecade & determine AD/BC`
`   local maxdefault = '9999'`
`   local maxdec = sterilizedec(maxdecade) --returns a tostring(unsigned int), or nil + error`
`   if maxdec then`
`       if string.match(maxdecade, '-%d') or `
`          string.match(maxdecade, 'BC')`
`       then                     --better +/-0 behavior with strings (0-initialized int == "-0" string...),`
`           maxdec = '-'..maxdec --but a "-0" string -> tonumber() -> tostring() = "-0",`
`       end                      --and a  "0" string -> tonumber() -> tostring() =  "0"`
`   elseif errors ~= '' then`
`       errors = p.errorclass('Function nav_decade was sent "'..(maxdecade or '')..'" as its 5th parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0", the highest decade to be shown.')`
`       return p.failedcat(errors, 'F')`
`   else`
`       maxdec = maxdefault`
`   end`
`   `
`   local tspace = ' ' --assume trailing space for "1950s in X"-type cats`
`   if string.match(lastpart, '^-') then tspace = '' end --DNE for "1970s-related"-type cats`
`   `
`   --AD/BC switches & vars`
`   `
`   local parentBC = string.match(lastpart, '^BC') --following the "0s BC" convention for all years BC`
`   lastpart = mw.ustring.gsub(lastpart, '^BC%s*', '') --handle BC separately; AD never used`
`   --TODO?: handle BCE, but only if it exists in the wild`
`   `
`   local dec0to40AD = (ndec >= 0 and ndec <= 40 and not parentBC) --special behavior in this range`
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local BCdisp = ''`
`   local D = -math.huge --secondary switch & iterator for AD/BC transition`
`   `
`   --check non-default min/max more carefully; determine right-offset`
`   local roffset = 0`
`   if mindec ~= mindefault then`
`       if tonumber(mindec) > ndec*switchADBC then`
`           mindec = tostring(ndec*switchADBC) --input error; mindec should be <= parent`
`       end`
`   end`
`   if maxdec ~= maxdefault then --a non-default max will override offsetting behavior`
`       if tonumber(maxdec) < ndec*switchADBC then`
`           maxdec = tostring(ndec*switchADBC) --input error; maxdec should be >= parent`
`       end`
`   else                            --offset only if 1) max == maxdefault,`

\--[\*\* BHG commented out default offsets unless and until there is an expicit consensus for this \*\* perverse behaviour, which disrupts navigation by making the poistion of the page's decade \*\* jump around erratically as we approcha and then pass the current decade local thisyear = mw.getContentLanguage():formatDate( 'Y' ) local nthisdecade = tonumber(string.match(thisyear, '^%d%d%d')..'0') if ndec \<= nthisdecade then --and 2) we're not on a future-decade cat (e.g. Works set in the 2100s) local diff = nthisdecade - ndec\*switchADBC --in 2019: diff=30 for 1980, 0 for 2010, -20 for 2030 if diff \< 0 then diff = 0 end --always show at least 1 decade ahead for present-decade+ cats if diff \>= 0 and diff \<= 30 then roffset = 40 - diff --in 2019: roffset=10 for 1980, 40 for 2010, 40 for 2030 end end \*\* End section commented by BHG --](https://ja.wikipedia.org/wiki/**_BHG_commented_out_default_offsets_unless_and_until_there_is_an_expicit_consensus_for_this_**_perverse_behaviour,_which_disrupts_navigation_by_making_the_poistion_of_the_page's_decade_**_jump_around_erratically_as_we_approcha_and_then_pass_the_current_decade_local_thisyear_=_mw.getContentLanguage\(\):formatDate\(_'Y'_\)_local_nthisdecade_=_tonumber\(string.match\(thisyear,_'^%d%d%d'\)..'0'\)_if_ndec_\<=_nthisdecade_then_--and_2\)_we're_not_on_a_future-decade_cat_\(e.g._Works_set_in_the_2100s\)_local_diff_=_nthisdecade_-_ndec*switchADBC_--in_2019:_diff=30_for_1980,_0_for_2010,_-20_for_2030_if_diff_\<_0_then_diff_=_0_end_--always_show_at_least_1_decade_ahead_for_present-decade+_cats_if_diff_\>=_0_and_diff_\<=_30_then_roffset_=_40_-_diff_--in_2019:_roffset=10_for_1980,_40_for_2010,_40_for_2030_end_end_**_End_section_commented_by_BHG_-- "wikilink")

`   end`
`   local nmindec = tonumber(mindec) --similar behavior to nav_year & nav_nordinal`
`   local nmaxdec = tonumber(maxdec) --similar behavior to nav_nordinal`
`   `
`   --begin navdecade`
`   local bnb = '' --border/no border`
`   if navborder == false then --for embedding in `
`       bnb = ' border-style: none; background-color: transparent;'`
`   end`
`   local navd = '{| class="toccolours hlist" style="text-align: center; margin: auto;'..bnb..'"\n'..'|\n'`
`   `
`   local i = (-50 - roffset)`
`   while i <= (50 - roffset) do`
`       local d = ndec + i*switchADBC`
`       `
`       if i ~= 0 then --left/right navd`
`           local BC = ''`
`           BCdisp = ''`
`           if dec0to40AD then`
`               if D < -10 then`
`                   d = math.abs(d + 10) --b/c 2 "0s" decades exist: "0s BC" & "0s" (AD)`
`                   BC = 'BC '`
`                   if d == 0 then`
`                       D = -10 --track 1st d = 0 use (BC)`
`                   end`
`               elseif D >= -10 then`
`                   D = D + 10 --now iterate from 0s AD`
`                   d = D      --2nd d = 0 use`
`               end`
`           elseif parentBC then`
`               if switchADBC == -1 then --parentBC looking at the BC side (the common case)`
`                   BC = 'BC '`
`                   if d == 0 then     --prepare to switch to the AD side on the next iteration`
`                       switchADBC = 1 --1st d = 0 use (BC)`
`                       D = -10        --prep`
`                   end`
`               elseif switchADBC == 1 then --switched to the AD side`
`                   D = D + 10 --now iterate from 0s AD`
`                   d = D      --2nd d = 0 use (on first use)`
`               end`
`           end`
`           if BC ~= '' and ndec <= 50 then`
`               BCdisp = ' BC' --show BC for all BC decades whenever a "0s" is displayed on the nav`
`           end`
`           `
`           --determine target cat`
`           local disp = d..'s'..BCdisp`
`           local catlink = catlinkfollowr( firstpart..' '..d..'s'..tspace..BC..lastpart, disp )`
`           if catlink[2] and avoidself then --a `` was followed`
`               misctrackingcats[9] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``decade``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_decade_redirected "wikilink")`'`
`           end`
`           `
`           --populate left/right navd`
`           local shown = '*'..catlink[1]..'\n'`
`           local hidden = '`<span style="visibility:hidden">`'..disp..'`</span>`'`
`           local dsign = d --use d for display & dsign for logic`
`           if BC ~= '' then dsign = -dsign end`
`           if (nmindec <= dsign) and (dsign <= nmaxdec) then`
`               if dsign == 0 and (nmindec == 0 or nmaxdec == 0) then --distinguish b/w -0 (BC) & 0 (AD)`
`                   --"zoom in" on +/- 0 and turn dsign/min/max temporarily into +/- 1 for easier processing`
`                   local zsign, zmin, zmax = 1, nmindec, nmaxdec`
`                   if BC ~= '' then zsign = -1 end`
`                   if     mindec == '-0' then zmin = -1`
`                   elseif mindec ==  '0' then zmin =  1 end`
`                   if     maxdec == '-0' then zmax = -1`
`                   elseif maxdec ==  '0' then zmax =  1 end`
`                   `
`                   if (zmin <= zsign) and (zsign <= zmax) then`
`                       navd = navd..shown`
`                       hidden = nil`
`                   else`
`                       navd = navd..'*'..hidden..'\n'`
`                   end`
`               else`
`                   navd = navd..shown --the common case`
`                   hidden = nil`
`               end`
`           else`
`               navd = navd..'*'..hidden..'\n'`
`           end`
`           if listall and hidden then`
`               listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`           end`
`           `
`       else --center navd`
`           if D >= -10 then`
`               D = D + 10 --housekeeping b/w left/right sides`
`           end`
`           if parentBC then`
`               BCdisp = ' BC'`
`               if ndec == 0 then`
`                   switchADBC = 1 --next element will be 0s AD`
`                   D = -10 --for this special case, D is still -inf`
`               end`
`           else`
`               BCdisp = ''`
`           end`
`           navd = navd..'*`<b>`'..dec..'s'..BCdisp..'`</b>`\n'`
`       end`
`       `
`       i = i + 10`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navd..'|}'`
`   end`

end

\--[============================{{ nav_year }}==============================](https://ja.wikipedia.org/wiki/============================{{_nav_year_}}============================== "wikilink")

function nav_year( firstpart, year, lastpart, minimumyear, maximumyear )

`   --Expects a PAGENAME of the form "Some sequential 1760 example cat", where `
`   --  firstpart   = Some sequential`
`   --  year        = 1760`
`   --  lastpart    = example cat`
`   --  minimumyear = 1758 ('min' year parameter; optional)`
`   --  maximumyear = 1800 ('max' year parameter; optional)`
`   year = tonumber(year) or tonumber(mw.ustring.match(year or '', '^%s*(%d*)'))`
`   local minyear = tonumber(string.match(minimumyear or '', '-?%d+')) or -9999    --allow +/- qualifier`
`   local maxyear = tonumber(string.match(maximumyear or '', '-?%d+')) or  9999    --allow +/- qualifier`
`   if string.match(minimumyear or '', 'BC') then minyear = -math.abs(minyear) end --allow BC qualifier (AD otherwise assumed)`
`   if string.match(maximumyear or '', 'BC') then maxyear = -math.abs(maxyear) end --allow BC qualifier (AD otherwise assumed)`
`   `
`   if year == nil then`
`       errors = p.errorclass('Function nav_year can\'t recognize the year sent to its 2nd parameter.')`
`       return p.failedcat(errors, 'Y')`
`   end`
`   `
`   --AD/BC switches & vars`
`   `
`   local yearBCElastparts = { --needed for parent = AD 1-5, when the BC/E format is unknown`
`       --"BCE" removed to match both AD & BCE cats; easier & faster than multiple string.match()s`
`       ['example_Hebrew people_example'] = 'BCE', --example entry format; add to & adjust as needed`
`   }`
`   local parentAD = string.match(firstpart, 'AD$')  --following the "AD 1" convention from AD 1 to AD 10`
`   local parentBC = string.match(lastpart, '^BCE?') --following the "1 BC" convention for all years BC`
`   firstpart = mw.ustring.gsub(firstpart, '%s*AD$', '') --handle AD/BC separately for easier & faster accounting`
`   lastpart  = mw.ustring.gsub(lastpart,  '^BCE?%s*', '')`
`   local BCe = parentBC or yearBCElastparts[lastpart] or 'BC' --"BC" default`
`   `
`   local year1to15AD = (year >= 1 and year <= 15 and not parentBC) --special behavior in this range`
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local Y = 0 --secondary iterator for AD-on-a-BC-parent`
`   `
`   if minyear > year*switchADBC then minyear = year*switchADBC end --input error; minyear should be <= parent`
`   if maxyear < year*switchADBC then maxyear = year*switchADBC end --input error; maxyear should be >= parent`
`   `
`   --determine interyear gap size to condense special category types, if possible`
`   local ygapdefault = 1 --assume/start at the most common case: 2001, 2002, etc.`
`   local ygap = ygapdefault`
`   if string.match(lastpart, 'presidential') then`
`       local ygap1, ygap2 = ygapdefault, ygapdefault --need to determine previous & next year gaps indepedently`
`       local ygap1_success, ygap2_success = false, false`
`       `
`       local prevseason = nil`
`       while ygap1 <= 5 do --Czech Republic, Poland, Sri Lanka, etc. have 5-year terms`
`           prevseason = firstpart..' '..(year-ygap1)..' '..lastpart`
`           if mw.title.new(prevseason, 'Category').exists then`
`               ygap1_success = true`
`               break`
`           end`
`           ygap1 = ygap1 + 1`
`       end`
`       `
`       local nextseason = nil`
`       while ygap2 <= 5 do --Czech Republic, Poland, Sri Lanka, etc. have 5-year terms`
`           nextseason = firstpart..' '..(year+ygap2)..' '..lastpart`
`           if mw.title.new(nextseason, 'Category').exists then`
`               ygap2_success = true`
`               break`
`           end`
`           ygap2 = ygap2 + 1`
`       end`
`       `
`       if ygap1_success and ygap2_success then`
`           if ygap1 == ygap2 then ygap = ygap1 end`
`       elseif ygap1_success then  ygap = ygap1`
`       elseif ygap2_success then  ygap = ygap2`
`       end`
`   end`
`   `
`   --skip non-existing years, if requested`
`   local ynogaps = {} --populate with existing years in the range, at most, [year-60, year+60]`
`   if skipgaps then`
`       if year > 70 then --add support for AD/BC (<= AD 10) if/when needed`
`           local yskipped = {} --track skipped y's to avoid double-checking`
`           local cat, found, Yeary`
`           `
`            --populate nav element queue outwards positively from the parent`
`           local Year = year --to save/ratchet progression`
`           local i = 1`
`           while i <= 5 do`
`               local y = 1`
`               while y <= (15 - i) do --'15' in case we get to i=5 and find nothing 10 y out`
`                   found = false`
`                   Yeary = Year + y`
`                   if yskipped[Yeary] == nil then`
`                       yskipped[Yeary] = Yeary`
`                       cat = firstpart..' '..Yeary..' '..lastpart`
`                       found = mw.title.new( cat, 'Category' ).exists`
`                       if found then break end`
`                   end`
`                   y = y + 1`
`               end`
`               if found then Year = Yeary`
`               else          Year = Year + 1 end`
`               ynogaps[i] =  Year`
`               i = i + 1`
`           end`
`           `
`           ynogaps[0] = year --the parent`
`           `
`           --populate nav element queue outwards negatively from the parent`
`           Year = year --reset ratchet`
`           i = -1`
`           while i >= -5 do`
`               local y = -1`
`               while y >= (-15 - i) do --'-15' in case we get to i=-5 and find nothing -10 y out`
`                   found = false`
`                   Yeary = Year + y`
`                   if yskipped[Yeary] == nil then`
`                       yskipped[Yeary] = Yeary`
`                       cat = firstpart..' '..Yeary..' '..lastpart`
`                       found = mw.title.new( cat, 'Category' ).exists`
`                       if found then break end`
`                   end`
`                   y = y - 1`
`               end`
`               if found then Year = Yeary`
`               else          Year = Year - 1 end`
`               ynogaps[i] =  Year`
`               i = i - 1`
`           end`
`       else`
`           skipgaps = false --AD/BC not supported`
`       end`
`   end`
`   `
`   --begin navyears`
`   local navy = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local y`
`   local i = -5`
`   while i <= 5 do`
`       if skipgaps then`
`           y = ynogaps[i]`
`       else`
`           y = year + i*ygap*switchADBC`
`       end`
`       local BCdisp = ''`
`       if i ~= 0 then --left/right navy`
`           `
`           local AD = ''`
`           local BC = ''`
`           if year1to15AD then`
`               if year >= 11 then --parent = AD 11-15`
`                   if y <= 10 then --prepend AD on y = 1-10 cats only, per existing cats`
`                       AD = 'AD '`
`                   end`
`                   `
`               elseif year >= 1 then --parent = AD 1-10`
`                   if y <= 0 then`
`                       BC = BCe..' '`
`                       y = math.abs(y - 1) --skip y = 0 (DNE)`
`                   elseif y >= 1 and y <= 10 then --prepend AD on y = 1-10 cats only, per existing cats`
`                       AD = 'AD '`
`                   end`
`               end`
`               `
`           elseif parentBC then`
`               if switchADBC == -1 then --displayed y is in the BC regime`
`                   if y >= 1 then     --the common case`
`                       BC = BCe..' '   `
`                   elseif y == 0 then --switch from BC to AD regime`
`                       switchADBC = 1`
`                   end`
`               end`
`               if switchADBC == 1 then --displayed y is now in the AD regime`
`                   Y = Y + 1 --skip y = 0 (DNE)`
`                   y = Y     --easiest solution: start another iterator for these AD y's displayed on a BC year parent`
`                   AD = 'AD '`
`               end`
`           end`
`           if BC ~= '' and year <= 5 then --only show 'BC' for parent years <= 5: saves room, easier to read,`
`               BCdisp = ' '..BCe          --and 6 is the first/last nav year that doesn't need a disambiguator;`
`           end                            --the center/parent year will always show BC, so no need to show it another 10x`
`           `
`           --populate left/right navy`
`           local ysign = y --use y for display & ysign for logic`
`           local disp = y..BCdisp`
`           if BC ~= '' then ysign = -ysign end`
`           local catlink = catlinkfollowr( firstpart..' '..AD..y..' '..BC..lastpart, disp )`
`           if (minyear <= ysign) and (ysign <= maxyear) then --ex: 1758, 1759, 1761, 1762, 1763, 1764, 1765`
`               if catlink[2] and avoidself then --a `` was followed`
`                   misctrackingcats[10] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``year``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_year_redirected "wikilink")`'`
`               end`
`               navy = navy..'*'..catlink[1]..'\n'`
`           else --ex: 1755, 1756, 1757`
`               local hidden = '`<span style="visibility:hidden">`'..disp..'`</span>`'`
`               navy = navy..'*'..hidden..'\n'`
`               if listall then`
`                   listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`               end`
`           end`
`       else --center navy; ex: 1760`
`           if parentBC then BCdisp = ' '..BCe end`
`           navy = navy..'*`<b>`'..year..BCdisp..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navy..'|}'`
`   end`

end

\--[==========================={{ nav_roman }}==============================](https://ja.wikipedia.org/wiki/==========================={{_nav_roman_}}============================== "wikilink")

function nav_roman( firstpart, roman, lastpart, minimumrom, maximumrom )

`   local toarabic = require('Module:ConvertNumeric').roman_to_numeral`
`   local toroman  = require('Module:Roman').main`
`   `
`   --sterilize/convert rom/num`
`   local num = tonumber(toarabic(roman))`
`   local rom = toroman({ [1] = num })`
`   if num == nil or rom == nil then --out of range or some other error`
`       errors = p.errorclass('Function nav_roman can\'t recognize one or more of "'..(num or 'nil')..'" & "'..`
`                           (rom or 'nil')..'" in category "'..firstpart..' '..roman..' '..lastpart..'".')`
`       return p.failedcat(errors, 'R')`
`   end`
`   `
`   --sterilize min/max`
`   local minrom = tonumber(minimumrom or '') or tonumber(toarabic(minimumrom or ''))`
`   local maxrom = tonumber(maximumrom or '') or tonumber(toarabic(maximumrom or ''))`
`   if minrom < 1 then minrom = 1 end    --toarabic() returns -1 on error`
`   if maxrom < 1 then maxrom = 9999 end --toarabic() returns -1 on error`
`   if minrom > num then minrom = num end`
`   if maxrom < num then maxrom = num end`
`   `
`   --begin navroman`
`   local navr = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = -5`
`   while i <= 5 do`
`       local n = num + i`
`       `
`       if n >= 1 then`
`           local r = toroman({ [1] = n })`
`           if i ~= 0 then --left/right navr`
`               local catlink = catlinkfollowr( firstpart..' '..r..' '..lastpart, r )`
`               if minrom <= n and n <= maxrom then`
`                   if catlink[2] and avoidself then --a `` was followed`
`                       misctrackingcats[11] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``roman``   ``numeral``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_roman_numeral_redirected "wikilink")`'`
`                   end`
`                   navr = navr..'*'..catlink[1]..'\n'`
`               else`
`                   local hidden = '`<span style="visibility:hidden">`'..r..'`</span>`'`
`                   navr = navr..'*'..hidden..'\n'`
`                   if listall then`
`                       listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`                   end`
`               end`
`           else --center navr`
`               navr = navr..'*`<b>`'..r..'`</b>`\n'`
`           end`
`       else`
`           navr = navr..'*`<span style="visibility:hidden">`'..'I'..'`</span>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navr..'|}'`
`   end`

end

\--[=========================={{ nav_nordinal }}============================](https://ja.wikipedia.org/wiki/=========================={{_nav_nordinal_}}============================ "wikilink")

function nav_nordinal( firstpart, ord, lastpart, minimumord, maximumord )

`   local nord = tonumber(ord)`
`   local minord = tonumber(string.match(minimumord or '', '(-?%d+)[snrt]?[tdh]?')) or -9999 --allow full ord & +/- qualifier`
`   local maxord = tonumber(string.match(maximumord or '', '(-?%d+)[snrt]?[tdh]?')) or  9999 --allow full ord & +/- qualifier`
`   if string.match(minimumord or '', 'BC') then minord = -math.abs(minord) end --allow BC qualifier (AD otherwise assumed)`
`   if string.match(maximumord or '', 'BC') then maxord = -math.abs(maxord) end --allow BC qualifier (AD otherwise assumed)`
`   `
`   local temporal = string.match(lastpart, 'century') or`
`                    string.match(lastpart, 'millennium')`
`   `
`   local tspace = ' ' --assume a trailing space after ordinal`
`   if string.match(lastpart, '^-') then tspace = '' end --DNE for "19th-century"-type cats`
`   `
`   --AD/BC switches & vars`
`   `
`   local ordBCElastparts = { --needed for parent = AD 1-5, when the BC/E format is unknown`
`       --lists the lastpart of valid BCE cats`
`       --"BCE" removed to match both AD & BCE cats; easier & faster than multiple string.match()s`
`       ['-century Hebrew people'] = 'BCE', --WP:CFD/Log/2016 June 21#Category:11th-century BC Hebrew people`
`       ['-century Jews']          = 'BCE', --co-nominated`
`       ['-century Judaism']       = 'BCE', --co-nominated`
`       ['-century rabbis']        = 'BCE', --co-nominated`
`   }`
`   local parentBC = mw.ustring.match(lastpart, '%s(BCE?)')       --"1st-century BC" format`
`   local lastpartNoBC = mw.ustring.gsub(lastpart, '%sBCE?', '')  --easier than splitting lastpart up in 2; AD never used`
`   local BCe = parentBC or ordBCElastparts[lastpartNoBC] or 'BC' --"BC" default`
`   `
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local O = 0 --secondary iterator for AD-on-a-BC-parent`
`   `
`   if not temporal and minord < 1 then minord = 1 end --nothing before "1st parliament", etc.`
`   if minord > nord*switchADBC then minord = nord*switchADBC end --input error; minord should be <= parent`
`   if maxord < nord*switchADBC then maxord = nord*switchADBC end --input error; maxord should be >= parent`
`   `
`   --determine right-offset, to not show unnecessary future millenia`
`   local roffset = 0`
`   if temporal and nord <= 3 then`
`       if string.match(lastpartNoBC, 'millennium ') and --only offset "1st millennium BC in Egypt" to "3rd-millennium people"-type cats`
`          string.match(lastpartNoBC, 'millennium in fiction') == nil and --except these, which extend > 4th millennium`
`          maxord == 9999 --only apply if max unspecified`
`       then`
`           if not parentBC and nord <= 3 then --1st, 2nd, & 3rd millennium parents`
`               roffset = nord + 1`
`           elseif parentBC and nord == 1 then --1st millennium BC only`
`               roffset = 1`
`           end`
`       end`
`   end`
`   `
`   --begin navnordinal`
`   local bnb = '' --border/no border`
`   if navborder == false then --for embedding in `
`       bnb = ' border-style: none; background-color: transparent;'`
`   end`
`   local navo = '{| class="toccolours hlist" style="text-align: center; margin: auto;'..bnb..'"\n'..'|\n'`
`   `
`   local i = (-5 - roffset)`
`   while i <= (5 - roffset) do`
`       local o = nord + i*switchADBC`
`       local BC = ''`
`       local BCdisp = ''`
`       if i ~= 0 then --left/right navo`
`           `
`           if parentBC then`
`               if switchADBC == -1 then --parentBC looking at the BC side`
`                   if o >= 1 then     --the common case`
`                       BC = ' '..BCe`
`                   elseif o == 0 then --switch to the AD side`
`                       BC = ''`
`                       switchADBC = 1`
`                   end`
`               end`
`               if switchADBC == 1 then --displayed o is now in the AD regime`
`                   O = O + 1 --skip o = 0 (DNE)`
`                   o = O     --easiest solution: start another iterator for these AD o's displayed on a BC year parent`
`               end`
`           elseif o <= 0 then --parentAD looking at BC side`
`               BC = ' '..BCe`
`               o = math.abs(o - 1) --skip o = 0 (DNE)`
`           end`
`           if BC ~= '' and nord <= 5 then --only show 'BC' for parent ords <= 5: saves room, easier to read,`
`               BCdisp = ' '..BCe          --and 6 is the first/last nav ord that doesn't need a disambiguator;`
`           end                            --the center/parent ord will always show BC, so no need to show it another 10x`
`           `
`           --populate left/right navo`
`           local oth = p.addord(o)`
`           local osign = o --use o for display & osign for logic`
`           if BC ~= '' then osign = -osign end`
`           local hidden = '`<span style="visibility:hidden">`'..oth..'`</span>`'`
`           if temporal then --e.g. "3rd-century BC"`
`               local lastpart = lastpartNoBC --lest we recursively add multiple "BC"s`
`               if BC ~= '' then`
`                   lastpart = string.gsub(lastpart, temporal, temporal..BC) --replace BC if needed`
`               end`
`               local catlink = catlinkfollowr( firstpart..' '..oth..tspace..lastpart, oth..BCdisp )`
`               if (minord <= osign) and (osign <= maxord) then`
`                   if catlink[2] and avoidself then --a `` was followed`
`                       misctrackingcats[12] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``nordinal``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_nordinal_redirected "wikilink")`'`
`                   end`
`                   navo = navo..'*'..catlink[1]..'\n'`
`               else`
`                   navo = navo..'*'..hidden..'\n'`
`                   if listall then`
`                       listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`                   end`
`               end`
`           elseif BC == '' and minord <= osign and osign <= maxord then --e.g. >= "1st parliament"`
`               local catlink = catlinkfollowr( firstpart..' '..oth..tspace..lastpart, oth )`
`               if catlink[2] and avoidself then --a `` was followed`
`                   misctrackingcats[12] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``nordinal``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_nordinal_redirected "wikilink")`'`
`               end`
`               navo = navo..'*'..catlink[1]..'\n'`
`           else --either out-of-range (hide), or non-temporal + BC = something might be wrong (2nd X parliament BC?); handle exceptions if/as they arise`
`               navo = navo..'*'..hidden..'\n'`
`           end`
`       else --center navo`
`           if parentBC then BC = ' '..BCe end`
`           navo = navo..'*`<b>`'..p.addord(o)..BC..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navo..'|}'`
`   end`

end

\--[========================={{ nav_wordinal }}=============================](https://ja.wikipedia.org/wiki/========================={{_nav_wordinal_}}============================= "wikilink")

function nav_wordinal( firstpart, word, lastpart, minimumword, maximumword, frame )

`   local eng2ord = require('Module:ConvertNumeric').english_to_ordinal`
`   local ord2eng = require('Module:ConvertNumeric').numeral_to_english`
`   local sc = string.match(word, '^%u') --sentence-case check`
`   local lc = string.lower(word) --operate on/with lc, and restore any sc later`
`   local nword = eng2ord(lc)`
`   local case = nil`
`   if sc then case = 'U' end`
`   `
`   --sterilize min/max`
`   local minword = 1`
`   local maxword = 99`
`   if minimumword then`
`       local num = tonumber(minimumword)`
`       if num and 0 < num and num < maxword then`
`           minword = num`
`       else`
`           local ord = eng2ord(minimumword)`
`           if 0 < ord and ord < maxword then`
`               minword = ord`
`           end`
`       end`
`   end`
`   if maximumword then`
`       local num = tonumber(maximumword)`
`       if num and 0 < num and num < maxword then`
`           maxword = num`
`       else`
`           local ord = eng2ord(maximumword)`
`           if 0 < ord and ord < maxword then`
`               maxword = ord`
`           end`
`       end`
`   end`
`   if minword > nword then minword = nword end`
`   if maxword < nword then maxword = nword end`
`   `
`   --begin navwordinal`
`   local navw = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = -5`
`   while i <= 5 do`
`       local n = nword + i`
`       `
`       if n >= 1 then`
`           local nth = p.addord(n)`
`           if i ~= 0 then --left/right navw`
`               local frame_args = frame:newChild{ args = { n, ord = 'on', case = case } } --easier to do this than modify Module:ConvertNumeric`
`               local w = ord2eng( frame_args )`
`               local catlink = catlinkfollowr( firstpart..' '..w..' '..lastpart, nth )`
`               if minword <= n and n <= maxword then`
`                   if catlink[2] and avoidself then --a `` was followed`
`                       misctrackingcats[13] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``wordinal``   ``redirected`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_wordinal_redirected "wikilink")`'`
`                   end`
`                   navw = navw..'*'..catlink[1]..'\n'`
`               else`
`                   local hidden = '`<span style="visibility:hidden">`'..nth..'`</span>`'`
`                   navw = navw..'*'..hidden..'\n'`
`                   if listall then`
`                       listofalllinks[#listofalllinks] = listofalllinks[#listofalllinks]..' ('..hidden..')'`
`                   end`
`               end`
`           else --center navw`
`               navw = navw..'*`<b>`'..nth..'`</b>`\n'`
`           end`
`       else`
`           navw = navw..'*`<span style="visibility:hidden">`'..'0th'..'`</span>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   isolatedcat()`
`   if listall then`
`       return listalllinks()`
`   else`
`       return navw..'|}'`
`   end`

end

\--[==========================={{ find_var }}===============================](https://ja.wikipedia.org/wiki/==========================={{_find_var_}}=============================== "wikilink")

\--Also used by . function p.find_var( pn )

`   --Extracts the variable text (e.g. 2015–16, 3rd, 2000s, III, etc.) from a string`
`   local pagename = currtitle.baseText`
`   if pn and pn ~= '' then`
`       pagename = pn`
`   end`
`   `
`   local cpagename = 'Category:'..pagename --limited-Lua-regex workaround`
`   `
`   local d_season = mw.ustring.match(cpagename, ':(%d+s).+%(%d+[–-]%d+%)') --i.e. `
`   `
`   local y_season = mw.ustring.match(cpagename, ':(%d+) .+%(%d+[–-]%d+%)') --i.e. `
`   `
`   local season   = mw.ustring.match(cpagename, '[:%s%(](%d+[–-]%d+)[%)%s]') or --split in 2 b/c you can't frontier '$'/eos?`
`                    mw.ustring.match(cpagename, '[:%s](%d+[–-]%d+)$')`
`                   `
`   local tvseason = mw.ustring.match(cpagename, 'season (%d+)') or`
`                    mw.ustring.match(cpagename, 'series (%d+)')`
`                   `
`   local nordinal = mw.ustring.match(cpagename, '[:%s](%d+[snrt][tdh])[-%s]') or`
`                    mw.ustring.match(cpagename, '[:%s](%d+[snrt][tdh])$')`
`                   `
`   local decade   = mw.ustring.match(cpagename, '[:%s](%d+s)[%s-]') or`
`                    mw.ustring.match(cpagename, '[:%s](%d+s)$')`
`                   `
`   local year     = mw.ustring.match(cpagename, '[:%s](%d+)%s') or`
`                    mw.ustring.match(cpagename, '[:%s](%d+)$')`
`                   `
`   local roman    = mw.ustring.match(cpagename, '%s([IVXLCDM]+)%s')`
`   `
`   local found    = d_season or y_season or season or tvseason or `
`                    nordinal or decade or year or roman`
`   `
`   if found then`
`       if string.match(found, '%d%d%d%d%d') == nil then`
`           --return in order of decreasing complexity/least chance for duplication`
`           if d_season then return { 'decade',   d_season } end`
`           if y_season then return { 'year',     y_season } end`
`           if season   then return { 'season',   season   } end`
`           if tvseason then return { 'tvseason', tvseason } end`
`           if nordinal then return { 'nordinal', nordinal } end`
`           if decade   then return { 'decade',   decade   } end`
`           if year     then return { 'year',     year     } end`
`           if roman    then return { 'roman',    roman    } end`
`       end`
`   else --try word ('zeroth' to 'ninety-ninth' only)`
`       local eng2ord = require('Module:ConvertNumeric').english_to_ordinal`
`       local split = mw.text.split(pagename, ' ')`
`       for i=1, #split do`
`           if eng2ord(split[i]) > -1 then`
`               return { 'wordinal', split[i] }`
`           end`
`       end`
`   end`
`   `
`   errors = p.errorclass('Function find_var can\'t find the variable text in category "'..pagename..'".')`
`   return { 'error', p.failedcat(errors, 'V') }`

end

\--[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink") --[Main](https://ja.wikipedia.org/wiki/Main "wikilink") --[==========================================================================](https://ja.wikipedia.org/wiki/========================================================================== "wikilink")

function p.navseasoncats( frame )

`   local args = frame:getParent().args`
`   local dby  = args['decade-below-year']    --used by `
`   local cbd  = args['century-below-decade'] --used by `
`   local cat  = args['cat']                  --'testcase' alias for mainspace`
`   local list = args['list-all-links']       --utility to output all links & followed #Rs instead of a navbar`
`   local follow = args['follow-redirects']   --default 'yes'`
`   local testcase    = args['testcase']`
`   local testcasegap = args['testcasegap']`
`   local minimum = args['min']`
`   local maximum = args['max']`
`   local skip_gaps = args['skip-gaps']`
`   `
`   if dby then`
`       navborder = false`
`       dby = string.gsub(dby, ' ', ' ') --unicodify forced whitespace`
`   end`
`   if cbd then`
`       navborder = false`
`       cbd = string.gsub(cbd, ' ', ' ') --unicodify forced whitespace`
`   end`
`   if follow and follow == 'no' then`
`       followRs = false`
`   end`
`   if list and list == 'yes' then`
`       listall = true`
`   end`
`   if skip_gaps and skip_gaps == 'yes' then`
`       skipgaps = true`
`       if avoidself then`
`           misctrackingcats[15] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``using``   ``skip-gaps``   ``parameter`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_using_skip-gaps_parameter "wikilink")`'`
`       end`
`   end`
`   `
`   if currtitle.nsText == 'Category' then`
`       if cat      then misctrackingcats[1] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``using``   ``cat``   ``parameter`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_using_cat_parameter "wikilink")`' end`
`       if testcase then misctrackingcats[2] = '`[`'..testcasecolon..'Category:Navseasoncats``   ``using``   ``testcase``   ``parameter`](https://ja.wikipedia.org/wiki/'..testcasecolon..'Category:Navseasoncats_using_testcase_parameter "wikilink")`' end`
`   end`
`   `
`   local pagename = testcase or cat or dby or cbd or currtitle.baseText`
`   `
`   local findvar = p.find_var(pagename)`
`   if findvar[1] == 'error' then return findvar[2]..table.concat(misctrackingcats) end --basic format error checking in find_var()`
`   `
`   local findvar_escaped = string.gsub( findvar[2], '%-', '%%%-')`
`   local firstpart, lastpart = string.match(pagename, '^(.-)'..findvar_escaped..'(.*)$')`
`   firstpart = mw.text.trim(firstpart or '')`
`   lastpart  = mw.text.trim(lastpart or '')`
`   `
`   local start = string.match(findvar[2], '^%d+')`
`   `
`   --determine the appropriate nav function`
`   `
`   if findvar[1] == 'season' then       --e.g. "1–4", "1999–2000", "2001–02", "2001–2002", "2005–2010", etc.`
`       local hyphen, finish = mw.ustring.match(findvar[2], '%d([–-])(%d+)') --ascii 150 & 45 (ndash & keyboard hyphen); mw req'd`
`       return nav_hyphen( start, hyphen, finish, firstpart, lastpart, minimum, maximum, testcasegap )..table.concat(misctrackingcats)`
`       `
`   elseif findvar[1] == 'tvseason' then --e.g. "1", "15" but preceded with "season" or "series"`
`       return nav_tvseason( firstpart, start, lastpart, maximum )..table.concat(misctrackingcats) --"minimum" defaults to 1`
`       `
`   elseif findvar[1] == 'decade' then   --e.g. "0s", "2010s"`
`       return nav_decade( firstpart, start, lastpart, minimum, maximum )..table.concat(misctrackingcats)`
`       `
`   elseif findvar[1] == 'year' then     --e.g. "500", "2001"`
`       return nav_year( firstpart, start, lastpart, minimum, maximum )..table.concat(misctrackingcats)`
`       `
`   elseif findvar[1] == 'roman' then    --e.g. "I", "XXVIII"`
`       return nav_roman( firstpart, findvar[2], lastpart, minimum, maximum )..table.concat(misctrackingcats)`
`       `
`   elseif findvar[1] == 'nordinal' then --e.g. "4th"`
`       return nav_nordinal( firstpart, start, lastpart, minimum, maximum )..table.concat(misctrackingcats)`
`       `
`   elseif findvar[1] == 'wordinal' then --e.g. "first", "ninety-ninth"`
`       return nav_wordinal( firstpart, findvar[2], lastpart, minimum, maximum, frame )..table.concat(misctrackingcats)`
`       `
`   else                                 --malformed`
`       errors = p.errorclass('Failed to determine the appropriate nav function from malformed season "'..findvar[2]..'". ')`
`       return p.failedcat(errors, 'N')..table.concat(misctrackingcats)`
`   end`

end

return p

[Category:Navseasoncats_using_cat_parameter](https://ja.wikipedia.org/wiki/Category:Navseasoncats_using_cat_parameter "wikilink") [Category:Navseasoncats_using_testcase_parameter](https://ja.wikipedia.org/wiki/Category:Navseasoncats_using_testcase_parameter "wikilink") [Category:Navseasoncats_range_not_using_en_dash](https://ja.wikipedia.org/wiki/Category:Navseasoncats_range_not_using_en_dash "wikilink") [Category:Navseasoncats_range_abbreviated](https://ja.wikipedia.org/wiki/Category:Navseasoncats_range_abbreviated "wikilink") [Category:Navseasoncats_range_redirected_(base_change)](https://ja.wikipedia.org/wiki/Category:Navseasoncats_range_redirected_\(base_change\) "wikilink") [Category:Navseasoncats_range_redirected_(MOS)](https://ja.wikipedia.org/wiki/Category:Navseasoncats_range_redirected_\(MOS\) "wikilink") [Category:Navseasoncats_isolated](https://ja.wikipedia.org/wiki/Category:Navseasoncats_isolated "wikilink") [Category:Navseasoncats_default_season_gap_size](https://ja.wikipedia.org/wiki/Category:Navseasoncats_default_season_gap_size "wikilink") [Category:Navseasoncats_decade_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_decade_redirected "wikilink") [Category:Navseasoncats_year_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_year_redirected "wikilink") [Category:Navseasoncats_roman_numeral_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_roman_numeral_redirected "wikilink") [Category:Navseasoncats_nordinal_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_nordinal_redirected "wikilink") [Category:Navseasoncats_wordinal_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_wordinal_redirected "wikilink") [Category:Navseasoncats_TV_season_redirected](https://ja.wikipedia.org/wiki/Category:Navseasoncats_TV_season_redirected "wikilink") [Category:Navseasoncats_using_skip-gaps_parameter](https://ja.wikipedia.org/wiki/Category:Navseasoncats_using_skip-gaps_parameter "wikilink") [Category:1760s_in_the_Province_of_Quebec_(1763–1791)](https://ja.wikipedia.org/wiki/Category:1760s_in_the_Province_of_Quebec_\(1763–1791\) "wikilink") [Category:1763_establishments_in_the_Province_of_Quebec_(1763–1791)](https://ja.wikipedia.org/wiki/Category:1763_establishments_in_the_Province_of_Quebec_\(1763–1791\) "wikilink")