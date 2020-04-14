> この記事は[モジュール:JSONutil](https://ja.wikipedia.org/wiki/モジュール:JSONutil)から翻訳されています。


local JSONutil = { suite = "JSONutil",

`                  serial = "2019-07-18",`
`                  item   = 63869449 }`

\--\[=\[ preprocess JSON data \]=\] local Failsafe = JSONutil

JSONutil.more = 50 -- length of trailing context

local Fallback = function ()

`   -- Retrieve current default language code`
`   --     Returns  string`
`   return mw.language.getContentLanguage():getCode()`
`                                          :lower()`

end -- Fallback()

JSONutil.fair = function ( apply )

`   -- Reduce enhanced JSON data to strict JSON`
`   -- Parameter:`
`   --     apply  -- string, with enhanced JSON`
`   -- Returns:`
`   --     1    -- string|nil|false, with error keyword`
`   --     2    -- string, with JSON or context`
`   local m   = 0`
`   local n   = 0`
`   local s   = mw.text.trim( apply )`
`   local sep = string.char( 10 )`
`   local i, j, last, r, scan, sep0, sep1, stab, start, stub, suffix`
`   local framework = function ( a )`
`                             -- syntax analysis outside strings`
`                             local k = 1`
`                             local c`
`                             while k do`
`                                 k = a:find( "[{%[%]}]", k )`
`                                 if k then`
`                                     c = a:byte( k, k )`
`                                     if c == 0x7B then    -- {`
`                                         m = m + 1`
`                                     elseif c == 0x7D then    -- }`
`                                         m = m - 1`
`                                     elseif c == 0x5B then    -- [`
`                                         n = n + 1`
`                                     else    -- ]`
`                                         n = n - 1`
`                                     end`
`                                     k = k + 1`
`                                 end`
`                             end   -- while k`
`                     end    -- framework()`
`   local free = function ( a, at, f )`
`                    -- Throws: error if /* is not matched by */`
`                    local s = a`
`                    local i = s:find( "//", at, true )`
`                    local k = s:find( "/*", at, true )`
`                    if i or k then`
`                        local m = s:find( sep0, at )`
`                        if i   and   ( not m  or  i < m ) then`
`                            k = s:find( "\n",  i + 2,  true )`
`                            if k then`
`                                if i == 1 then`
`                                    s = s:sub( k + 1 )`
`                                else`
`                                    s = s:sub( 1,  i - 1 )   ..`
`                                        s:sub( k + 1 )`
`                                end`
`                            elseif i > 1 then`
`                                s = s:sub( 1,  i - 1 )`
`                            else`
`                                s = ""`
`                            end`
`                        elseif k   and   ( not m  or  k < m ) then`
`                            i = s:find( "*/",  k + 2,  true )`
`                            if i then`
`                                if k == 1 then`
`                                    s = s:sub( i + 2 )`
`                                else`
`                                    s = s:sub( 1,  k - 1 )   ..`
`                                        s:sub( i + 2 )`
`                                end`
`                            else`
`                                error( s:sub( k + 2 ), 0 )`
`                            end`
`                            i = k`
`                        else`
`                            i = false`
`                        end`
`                        if i then`
`                            s = mw.text.trim( s )`
`                            if s:find( "/", 1, true ) then`
`                                s = f( s, i, f )`
`                            end`
`                        end`
`                    end`
`                    return s`
`                end    -- free()`
`   if s:sub( 1, 1 ) == '{' then`
`       stab = string.char( 9 )`
`       s    = s:gsub( string.char( 13, 10 ),  sep )`
`               :gsub( string.char( 13 ),  sep )`
`       stub = s:gsub( sep, "" ):gsub( stab, "" )`
`       scan = string.char( 0x5B, 0x01, 0x2D, 0x1F, 0x5D )    -- [ \-\ ]`
`       j    = stub:find( scan )`
`       if j then`
`           r = "ControlChar"`
`           s = mw.text.trim( s:sub( j + 1 ) )`
`           s = mw.ustring.sub( s, 1, JSONutil.more )`
`       else`
`           i    = true`
`           j    = 1`
`           last = ( stub:sub( -1 ) == "}" )`
`           sep0 = string.char( 0x5B, 0x22, 0x27, 0x5D )    -- [ " ' ]`
`           sep1 = string.char( 0x5B, 0x5C, 0x22, 0x5D )    -- [ \ " ]`
`       end`
`   else`
`       r = "Bracket0"`
`       s = mw.ustring.sub( s, 1, JSONutil.more )`
`   end`
`   while i do`
`       i, s = pcall( free, s, j, free )`
`       if i then`
`           i = s:find( sep0, j )`
`       else`
`           r = "CommentEnd"`
`           s = mw.text.trim( s )`
`           s = mw.ustring.sub( s, 1, JSONutil.more )`
`       end`
`       if i then`
`           if j == 1 then`
`               framework( s:sub( 1, i - 1 ) )`
`           end`
`           if s:sub( i, i ) == '"' then`
`               stub = s:sub( j,  i - 1 )`
`               if stub:find( '[^"]*,%s*[%]}]' ) then`
`                   r = "CommaEnd"`
`                   s = mw.text.trim( stub )`
`                   s = mw.ustring.sub( s, 1, JSONutil.more )`
`                   i = false`
`                   j = false`
`               else`
`                   if j > 1 then`
`                       framework( stub )`
`                   end`
`                   i = i + 1`
`                   j = i`
`               end`
`               while j do`
`                   j = s:find( sep1, j )`
`                   if j then`
`                       if s:sub( j, j ) == '"' then`
`                           start  = s:sub( 1,  i - 1 )`
`                           suffix = s:sub( j )`
`                           if j > i then`
`                               stub = s:sub( i,  j - 1 )`
`                                       :gsub( sep,  "\\n" )`
`                                       :gsub( stab, "\\t" )`
`                               j = i + stub:len()`
`                               s = string.format( "%s%s%s",`
`                                                  start, stub, suffix )`
`                           else`
`                               s = start .. suffix`
`                           end`
`                           j = j + 1`
`                           break   -- while j`
`                       else`
`                           j = j + 2`
`                       end`
`                   else`
`                       r = "QouteEnd"`
`                       s = mw.text.trim( s:sub( i ) )`
`                       s = mw.ustring.sub( s, 1, JSONutil.more )`
`                       i = false`
`                   end`
`               end   -- while j`
`           else`
`               r = "Qoute"`
`               s = mw.text.trim( s:sub( i ) )`
`               s = mw.ustring.sub( s, 1, JSONutil.more )`
`               i = false`
`           end`
`       elseif not r then`
`           stub = s:sub( j )`
`           if stub:find( '[^"]*,%s*[%]}]' ) then`
`               r = "CommaEnd"`
`               s = mw.text.trim( stub )`
`               s = mw.ustring.sub( s, 1, JSONutil.more )`
`           else`
`               framework( stub )`
`           end`
`       end`
`   end   -- while i`
`   if not r   and   ( m ~= 0  or  n ~= 0 ) then`
`       if m ~= 0 then`
`           s = "}"`
`           if m > 0 then`
`               r = "BracketCloseLack"`
`               j = m`
`           elseif m < 0 then`
`               r = "BracketClosePlus"`
`               j = -m`
`           end`
`       else`
`           s = "]"`
`           if n > 0 then`
`               r = "BracketCloseLack"`
`               j = n`
`           else`
`               r = "BracketClosePlus"`
`               j = -n`
`           end`
`       end`
`       if j > 1 then`
`           s =  string.format( "%d %s", j, s )`
`       end`
`   elseif not ( r or last ) then`
`       stub = suffix or apply or ""`
`       j    = stub:find( "/", 1, true )`
`       if j then`
`           i, stub = pcall( free, stub, j, free )`
`       else`
`           i = true`
`       end`
`       stub = mw.text.trim( stub )`
`       if i then`
`           if stub:sub( - 1 ) ~= "}" then`
`               r = "Trailing"`
`               s = stub:match( "%}%s*(%S[^%}]*)$" )`
`               if s then`
`                   s = mw.ustring.sub( s, 1, JSONutil.more )`
`               else`
`                   s = mw.ustring.sub( stub,  - JSONutil.more )`
`               end`
`           end`
`       else`
`           r = "CommentEnd"`
`           s = mw.ustring.sub( stub, 1, JSONutil.more )`
`       end`
`   end`
`   if r and s then`
`       s = mw.text.encode( s:gsub( sep,  " " ) ):gsub( "|", "|" )`
`   end`
`   return r, s`

end -- JSONutil.fair()

JSONutil.fault = function ( alert, add, adapt )

`   -- Retrieve formatted message`
`   -- Parameter:`
`   --     alert  -- string, with error keyword, or other text`
`   --     add    -- string|nil|false, with context`
`   --     adapt  -- function|string|table|nil|false, for I18N`
`   -- Returns string, with HTML span`
`   local e = mw.html.create( "span" )`
`                    :addClass( "error" )`
`   local s = alert`
`   if type( s ) == "string" then`
`       s = mw.text.trim( s )`
`       if s == "" then`
`           s = "EMPTY JSONutil.fault key"`
`       end`
`       if not s:find( " ", 1, true ) then`
`           local storage = string.format( "I18n/Module:%s.tab",`
`                                          JSONutil.suite )`
`           local lucky, t = pcall( mw.ext.data.get, storage, "_" )`
`           if type( t ) == "table" then`
`               t = t.data`
`               if type( t ) == "table" then`
`                   local e`
`                   s = "err_" .. s`
`                   for i = 1, #t do`
`                       e = t[ i ]`
`                       if type( e ) == "table" then`
`                           if e[ 1 ] == s then`
`                               e = e[ 2 ]`
`                               if type( e ) == "table" then`
`                                   local q = type( adapt )`
`                                   if q == "function" then`
`                                       s = adapt( e, s )`
`                                       t = false`
`                                   elseif q == "string" then`
`                                       t = mw.text.split( adapt, "%s+" )`
`                                   elseif q == "table" then`
`                                       t = adapt`
`                                   else`
`                                       t = { }`
`                                   end`
`                                   if t then`
`                                       table.insert( t, Fallback() )`
`                                       table.insert( t, "en" )`
`                                       for k = 1, #t do`
`                                           q = e[ t[ k ] ]`
`                                           if type( q ) == "string" then`
`                                               s = q`
`                                               break   -- for k`
`                                           end`
`                                       end   -- for k`
`                                   end`
`                               else`
`                                   s = "JSONutil.fault I18N bad #" ..`
`                                       tostring( i )`
`                               end`
`                               break   -- for i`
`                           end`
`                       else`
`                           break   -- for i`
`                       end`
`                   end   -- for i`
`               else`
`                   s = "INVALID JSONutil.fault I18N corrupted"`
`               end`
`           else`
`               s = "INVALID JSONutil.fault commons:Data: " .. type( t )`
`           end`
`       end`
`   else`
`       s = "INVALID JSONutil.fault key: " .. tostring( s )`
`   end`
`   if type( add ) == "string" then`
`       s = string.format( "%s – %s", s, add )`
`   end`
`   e:wikitext( s )`
`   return tostring( e )`

end -- JSONutil.fault()

JSONutil.fetch = function ( apply, always, adapt )

`   -- Retrieve JSON data, or error message`
`   -- Parameter:`
`   --     apply   -- string, with presumable JSON text`
`   --     always  -- true, if apply is expected to need preprocessing`
`   --     adapt   -- function|string|table|nil|false, for I18N`
`   -- Returns table, with data, or string, with error as HTML span`
`   local lucky, r`
`   if not always then`
`       lucky, r = pcall( mw.text.jsonDecode, apply )`
`   end`
`   if not lucky then`
`       lucky, r = JSONutil.fair( apply )`
`       if lucky then`
`           r = JSONutil.fault( lucky, r, adapt )`
`       else`
`           lucky, r = pcall( mw.text.jsonDecode, r )`
`           if not lucky then`
`               r = JSONutil.fault( r, false, adapt )`
`           end`
`       end`
`   end`
`   return r`

end -- JSONutil.fetch()

Failsafe.failsafe = function ( atleast )

`   -- Retrieve versioning and check for compliance`
`   -- Precondition:`
`   --     atleast  -- string, with required version or "wikidata" or "~"`
`   --                 or false`
`   -- Postcondition:`
`   --     Returns  string  -- with queried version, also if problem`
`   --              false   -- if appropriate`
`   local last  = ( atleast == "~" )`
`   local since = atleast`
`   local r`
`   if last  or  since == "wikidata" then`
`       local item = Failsafe.item`
`       since = false`
`       if type( item ) == "number"  and  item > 0 then`
`           local entity = mw.wikibase.getEntity( string.format( "Q%d",`
`                                                                item ) )`
`           if type( entity ) == "table" then`
`               local vsn = entity:formatPropertyValues( "P348" )`
`               if type( vsn ) == "table"  and`
`                  type( vsn.value ) == "string"  and`
`                  vsn.value ~= "" then`
`                   if last  and  vsn.value == Failsafe.serial then`
`                       r = false`
`                   else`
`                       r = vsn.value`
`                   end`
`               end`
`           end`
`       end`
`   end`
`   if type( r ) == "nil" then`
`       if not since  or  since <= Failsafe.serial then`
`           r = Failsafe.serial`
`       else`
`           r = false`
`       end`
`   end`
`   return r`

end -- Failsafe.failsafe()

\-- Export local p = { }

p.failsafe = function ( frame )

`   -- Versioning interface`
`   local s = type( frame )`
`   local since`
`   if s == "table" then`
`       since = frame.args[ 1 ]`
`   elseif s == "string" then`
`       since = frame`
`   end`
`   if since then`
`       since = mw.text.trim( since )`
`       if since == "" then`
`           since = false`
`       end`
`   end`
`   return Failsafe.failsafe( since )  or  ""`

end -- p.failsafe()

p.JSONutil = function ()

`   -- Module interface`
`   return JSONutil`

end

return p