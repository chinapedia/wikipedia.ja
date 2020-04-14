> この記事は[モジュール:PageUtil](https://ja.wikipedia.org/wiki/モジュール:PageUtil)から翻訳されています。


local PageUtil = { suite = "PageUtil",

`                  serial = "2018-10-19",`
`                  item   = 0 }`

\--\[=\[ PageUtil \]=\]

PageUtil.maxPages = 200

local function fault( alert, frame )

`   -- Format message with class="error"`
`   --     alert  -- string, with message`
`   --     frame  -- object, if known`
`   -- Returns message with markup`
`   local scream = alert`
`   if frame then`
`       scream = string.format( "%s * %s", frame:getTitle(), scream )`
`   end`
`   return tostring( mw.html.create( "span" )`
`                           :addClass( "error" )`
`                           :wikitext( scream ) )`

end -- fault()

local function flat( adjust, assembly )

`   -- Replace links to pages by inner links`
`   --     adjust    -- string, with text`
`   --     assembly  -- table, with page infos`
`   -- Returns adjusted string`
`   local r = adjust`
`   local seek, shift, source, subst`
`   for k, v in pairs( assembly ) do`
`       source = v[ 1 ]`
`       shift  = v[ 2 ]`
`       source = ":?" .. source:gsub( " ", "[_ ]+" )`
`                              :gsub( "[%.%(%)%*%?%+%-]", "%1" )`
`                     .. "%s*"`
`       seek   = "%[%[%s*" .. source .. "(#[^%]]*%]%])"`
`       subst  = "`[`[^%`](https://ja.wikipedia.org/wiki/%1"_r_=_r:gsub\(_seek,_subst_\)_seek_=_"%[%[%s*"_.._source_.._"\(% "wikilink")`*%]%])"`
`       subst = "[[#" .. shift .. "%1"`
`       r = r:gsub( seek, subst )`
`       seek  = "%[%[%s*(" .. source .. "%]%])"`
`       subst = "[[#" .. shift .. "|%1"`
`       r = r:gsub( seek, subst )`
`   end -- for k, v`
`   return r`

end -- flat()

local function fraction( access, frame )

`   -- Retrieve text from section`
`   --     access  -- string, with request`
`   --     frame   -- object`
`   -- Returns content, or false`
`   -- Uses:`
`   --     mw.title.new() .exists`
`   local r`
`   local seek = "^(#lstx?):%s*%[%[([^%[|%]\n]+)%]%]%s*(%S.*)%s*$"`
`   local scope, source, section = access:match( seek )`
`   if source then`
`       local page = mw.title.new( source )`
`       source = page.prefixedText`
`       if page.exists then`
`           section = mw.text.trim( section )`
`           if section ~= "" then`
`               r = frame:callParserFunction{ name = scope,`
`                                             args = { source,`
`                                                      section } }`
`           end`
`       else`
`           r = tostring( mw.html.create( "div" )`
`                                :addClass( "error" )`
`                                :wikitext( source ) )`
`       end`
`   end`
`   return r`

end -- fraction()

local function full( access, frame, alias, assembly )

`   -- Retrieve text from page`
`   --     access    -- string, with page name`
`   --     frame     -- object`
`   --     alias     -- number, unique`
`   --     assembly  -- table, with page infos`
`   -- Returns string with content, or nil`
`   -- Uses:`
`   --     mw.title.new() .exists`
`   local page = mw.title.new( access )`
`   local r`
`   if page then`
`       if page.exists then`
`           local source  = page.prefixedText`
`           local segment = string.format( "PageUtilMerge-%d", alias )`
`           local seed`
`           if page.namespace == 0 then`
`               seed = ":" .. source`
`           else`
`               seed = source`
`           end`
`           r = string.format( "%s\n%s",`
`                              tostring( mw.html.create( "span" )`
`                                               :attr( "id", segment ) ),`
`                              frame:expandTemplate( { title = seed } ) )`
`           table.insert( assembly,  { source, segment } )`
`       else`
`           r = tostring( mw.html.create( "div" )`
`                                :addClass( "error" )`
`                                :wikitext( page.prefixedText ) )`
`       end`
`   else`
`       r = string.format( "%s '%s'", "Unknown page", access )`
`       r = tostring( mw.html.create( "div" )`
`                            :addClass( "error" )`
`                            :wikitext( r ) )`
`   end`
`   return r`

end -- full()

PageUtil.failsafe = function ( assert )

`   -- Retrieve versioning and check for compliance`
`   -- Precondition:`
`   --     assert  -- string, with required version or "wikidata",`
`   --                or false`
`   -- Postcondition:`
`   --     Returns  string with appropriate version, or false`
`   local since = assert`
`   local r`
`   if since == "wikidata" then`
`       local item = PageUtil.item`
`       since = false`
`       if type( item ) == "number"  and  item > 0 then`
`           local ent = mw.wikibase.getEntity( string.format( "Q%d",`
`                                                             item ) )`
`           if type( ent ) == "table" then`
`               local vsn = ent:formatPropertyValues( "P348" )`
`               if type( vsn ) == "table"  and`
`                  type( vsn.value ) == "string" and`
`                  vsn.value ~= "" then`
`                   r = vsn.value`
`               end`
`           end`
`       end`
`   end`
`   if not r then`
`       if not since  or  since <= PageUtil.serial then`
`           r = PageUtil.serial`
`       else`
`           r = false`
`       end`
`   end`
`   return r`

end -- PageUtil.failsafe()

PageUtil.getProtection = function ( access, action )

`   -- Retrieve protection`
`   --     access  -- string or title or nil, with page, default: current`
`   --     action  -- string or nil, with action, default: edit`
`   -- Returns number: One of: 0, 0.5, 0.75, 1`
`   local t = type( access )`
`   local r = 0`
`   local p`
`   if t == "string" then`
`       t = mw.title.new( access )`
`   elseif t == "table" then`
`       t = access`
`   else`
`       t = mw.title.getCurrentTitle()`
`   end`
`   p = t.protectionLevels`
`   if type( p ) == "table" then`
`       local s`
`       if type( action ) == "string" then`
`           s = mw.text.trim( action )`
`           if s == "" then`
`               s = false`
`           end`
`       end`
`       p = p[ s or "edit" ]`
`       if type( p ) == "table" then`
`           for k, v in pairs( p ) do`
`               if v == "autoconfirmed" then`
`                   r = 0.5`
`               elseif v == "editeditorprotected" then`
`                   r = 0.75`
`               elseif v == "sysop" then`
`                   r = 1`
`               end`
`           end -- for k, v`
`       end`
`   end`
`   return r`

end -- PageUtil.getProtection()

PageUtil.merge = function ( args, frame )

`   -- Retrieve text`
`   --     args   -- table, with request`
`   --     frame  -- object, if available`
`   -- Returns string, with content`
`   local max = 0`
`   local r   = ""`
`   for k, v in pairs( args ) do`
`       if type( k ) == "number"  and`
`          k > max then`
`           max = k`
`       end`
`   end -- for k, v`
`   if max > 0 then`
`       local n     = 0`
`       local pages = {  { mw.title.getCurrentTitle().prefixedText,`
`                          "" }  }`
`       local mode, s, section, swallow`
`       if not frame then`
`           frame = mw.getCurrentFrame()`
`       end`
`       for i = 1, max do`
`           s = args[ i ]`
`           if s then`
`               swallow = s:match( "^%s*(#lstx?:[^\n]*%S)%s*$" )`
`               if swallow then`
`                   s = fraction( swallow, frame )`
`                   n = n + 1`
`               else`
`                   swallow = s:match( "^%s*%[%[([^%[|%]\n]+)%]%]%s*$" )`
`                   if swallow then`
`                       s = full( swallow, frame, i, pages )`
`                       n = n + 1`
`                   end`
`               end`
`               if s then`
`                   r = r .. mw.text.trim( s )`
`               end`
`               if n > PageUtil.maxPages then`
`                   s = string.format( "`**`Too``   ``many``   ``pages``   ``(max.``   ``%d)`**`",`
`                                      PageUtil.maxPages )`
`                   r = string.format( "%s\n\n%s",`
`                                      r,`
`                                      fault( s, frame ) )`
`                   break -- for i`
`               end`
`           end`
`       end -- for i`
`       r = flat( r, pages )`
`   end`
`   return r`

end -- .merge()

\-- Export local p = { }

p.getProtection = function ( frame )

`   local n = PageUtil.getProtection( frame.args[ 1 ], frame.args[ 2 ] )`
`   local t = { [ 0 ]    = "",`
`               [ 0.5 ]  = mw.ustring.char( 189 ),`
`               [ 0.75 ] = mw.ustring.char( 190 ),`
`               [ 1 ]    = "1" }`
`   return t[ n ]`

end -- p.getProtection

function p.isRedirect()

`   return mw.title.getCurrentTitle().isRedirect and "1"  or  ""`

end -- p.isRedirect

p.merge = function ( frame )

`   local lucky, r = pcall( PageUtil.merge, frame.args, frame )`
`   if not lucky then`
`       r = fault( r, frame )`
`   end`
`   return r`

end -- p.merge

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
`   return PageUtil.failsafe( since )  or  ""`

end -- p.failsafe()

function p.PageUtil()

`   return PageUtil`

end

return p