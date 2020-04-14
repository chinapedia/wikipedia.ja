> この記事は[モジュール:Interlinear](https://ja.wikipedia.org/wiki/モジュール:Interlinear)から翻訳されています。


local p = {} local data = mw.loadData( 'Module:Interlinear/data' ) local gloss_override = {} -- for custom gloss abbreviations local getArgs = require('Module:Arguments').getArgs local yesno = require('Module:Yesno') local lang_data = mw.loadData( 'Module:Lang/data' )

-----

\-- Almost-global variables

-----

local glossing_type, displaying_messages, free_translation, msg, buffer

-----

\-- General settings

-----

local conf = { --settings

`   WordSeparator = " \n\r\t", -- Don't replace with %s as this would include non-breaking spaces`
`   GlossAbbrPattern = "^([Ø0-9A-Z]+)$", -- this isn't a full regex, but a Lua pattern`
`   -- NOTE: The following characters must be formatted for use in a pattern set.`
`   GlossAbbrBoundary = "-.,;:<>‹›/\\~+=%?%s%[%]()%_\127'",`
`   GlossExcludeTable = {I = true,}, --strings not be treated as glossing abbreviations`
`   GlossExcludePattern = '[0-9][0-9]+',`
`   GlossSmallCapsExclude = "^[AOPS]$", -- glossing abbreviations matching this pattern will not be rendered in small caps`
`   GlossingType = "label", -- if set to "label" gloss abbreviations are formatted as an `<abbr>` with the "label" appearing in a tooltip`
`                       -- if set to "wikilink" the abbreviation is formatted as a wikilink to the relevant wikipedia article`
`                       -- if set to "none" abbreviations aren't formatted at all`
`   ErrorCategory = "",`
`   AmbiguousGlossCategory = "",`
`   MessageGlossingError = "Error(s) in interlinear glossing",`
`   combining_gender_numbers = "[0-9][0-9]?$", --e.g. G4 '4th gender' or CL7 'class 7'`
`   combining_gender_prefixes = {G = "gender", CL = "class"},`
`   combining_person = {["1"] = "first person", ["2"] = "second person", ["3"] = "third person"},`
`   combining_number = {S = "singular", SG = "singular", P = "plural", PL = "plural", D = "dual", DU = "dual", TRI = "trial"},`
`   combining_gender = {F = "feminine", M = "masculine", N = "neuter"},`
`   LowerCaseGlosses = {["1sg"] = true, ["2sg"] = true, ["3sg"] = true, ["1du"] = true, ["2du"] = true, ["3du"] = true, ["1pl"] = true, ["2pl"] = true,`
`       ["3pl"] = true, ["Fsg"] = true, ["Fpl"] = true, ["Msg"] = true, ["Mpl"] = true,}, -- these are the non-all-upper-case strings that will be recognised as glossing abbreviations`
`   ErrorHelpLocation = "Template:Interlinear",`

}

-----

\-- CSS styles and classes

-----

conf.style = { --CSS styles

`   WordDiv = "float: left; margin-bottom: 0.3em;",`
`   WordMargin = "margin-right: 1em;",`
`   WordP = "margin: 0px;", -- the style for the word `

elements

`   GlossAbbr = "font-variant: small-caps; font-variant-numeric: oldstyle-nums; text-transform: lowercase; ", -- won't be applied to gloss abbreviations containing lower-case characters`
`   HiddenText = "display: none;",`
`   EndDiv = "clear: left; display: block;", -- style of the `

<div>

element at the end of the interlinear display

`   ErrorMessage = "font-size: inherit",`

} conf.class = { --CSS classes

`   Interlinear = "interlinear",`
`   GlossAbbr  = "gloss-abbr",`
`   GlossAbbrAmb = "gloss-abbr-ambiguous",`
`   GlossAbbrError = "gloss-abbr-error",`
`   ErrorMessage = "error",`

}

-----

\-- Sundry small functions

-----

local function normalise(str)

`   return mw.ustring.gsub(str,"[" .. conf.WordSeparator .. "]+"," ")`

end

local function tidyCss(str)

`   str = mw.ustring.gsub(str, '^[\"\']*(.-)[\"\']*$', "%1") -- trims quotation marks`
`   if mw.ustring.sub(str, -1) ~= ";" then str = str .. ";" end -- appends ";" if missing`
`   return str`

end

local function highlight(text)

`   if text then`
`       return '`<span style="color:#C00;font-weight:bold;">`' .. text .. '`</span>`'`
`   else return "" end`

end

local function tone_sup(str)

`   return mw.ustring.gsub(str, "([^%p%s0-9])([0-9])", "%1`<sup>`%2`</sup>`")`

end

local function is_empty(str) -- returns "false" if its argument is a string containing chars other than spaces \&c.

`   if not str then return true end`
`   if mw.ustring.find(str, "[^" .. conf.WordSeparator .. "]")`
`       then return false`
`   else return true end`

end

local function help_link (anchor)

`   if anchor then`
`       return " (`[`help`](https://ja.wikipedia.org/wiki/"_.._conf.ErrorHelpLocation_.._"#"_.._anchor_.._" "wikilink")`)"`
`   else return "" end`

end

\-- the following is part of a trial implementation of automatic transliteration: local function transliterate (str, lang_from, lang_to, scheme)

`   local lookup = {grc = {module = 'Module:Ancient Greek', funct = "transliterate", } }`
`   if not lang_from then`
`       msg:add("error", "Source language for transliteration is not set")`
`   else`
`       local t = lookup[lang_from]`
`       if t then`
`           local module = require(t.module)`
`           return module[t.funct](str)`
`       else msg:add("error", "Can't find transliterator for language '" .. lang_from .. "'")`
`       end`
`   end`
`   return ""`

end -- end of trial block

-----

\-- The following two functions update the glossing settings based on the received -- template arguments. set_global_glossing_settings() updates the global settings -- that are valid for all gloss abbreviations. set_glossing_type() -- returns the glossing type, which can vary between the different lines.

-----

local function set_global_glossing_settings(a)

`   local style = ""`
`   if a.style then style = tidyCss(a.style) end`
`   if a.underline == "no" then`
`       style = style .. "text-decoration: none;" end`
`   if a.small_caps == "no" then`
`       style = style .. "font-variant:normal; text-transform: none;" end`
`   if style ~= "" then conf.style.GlossAbbr = conf.style.GlossAbbr .. style end`

end

local function set_glossing_type(glossing)

`   if glossing then`
`       local GlossingType`
`       glossing = mw.ustring.lower(mw.text.trim(glossing))`
`       if mw.ustring.find(glossing, 'link') then`
`           GlossingType = "wikilink"`
`       elseif mw.ustring.find(glossing, 'label')`
`           or  mw.ustring.find(glossing, 'no link') then`
`           GlossingType = 'label'`
`       elseif mw.ustring.find(glossing, 'no abbr') then`
`           GlossingType = "no abbr"`
`       elseif yesno(glossing) == false then`
`           GlossingType = nil`
`       elseif yesno(glossing) then`
`           GlossingType = conf.GlossingType`
`       else`
`           msg:add('error', 'Glossing type "' .. glossing .. '" not recognised') end`
`       return GlossingType`
`   else error("set_glossing_type: 'glossing' is nil or false", 2)`
`   end`

end

local function set_custom_glosses(list)

`   local abbs = mw.text.split(list, '[;\n\t]')`
`   for _,v in pairs(abbs) do`
`       local gloss = mw.text.split(v, ':')`
`       local a = mw.text.trim(gloss[1])`
`       if a and a ~= "" then`
`           gloss_override[a] = {}`
`           gloss_override[a].expansion = gloss[2]`
`           gloss_override[a].wikipage = gloss[3]`
`       end`
`   end`

end

-----

\-- The UserMessages object contains and processes error messages and warnings

-----

local UserMessages = {errors = {}, warnings = {}, gloss_messages = {}} function UserMessages:add(msgtype, text, gloss)

`   if msgtype == "gloss_message" then`
`       self.gloss_messages[gloss] = text`
`   elseif msgtype == "warning" then`
`       table.insert(self.warnings, text)`
`   elseif msgtype == "non-repeating error" then`
`       self.errors.nre = text`
`   elseif msgtype == "ambiguous gloss" then`
`       self.if_ambiguous_glosses = true`
`   elseif msgtype == "error" then`
`       table.insert(self.errors, text)`
`   else return error("UserMessages:add(): unknown message type", 2)`
`   end`

end function UserMessages:print_errors()

`   local out = ""`
`   local namespace = mw.title.getCurrentTitle().namespace`
`   if next(self.errors) or self.warnings[1] then`
`       local err_span = mw.html.create("span")`
`       err_span:attr("style", conf.style.ErrorMessage)`
`       err_span:addClass(conf.class.ErrorMessage)`
`       for _,v in pairs(self.errors) do`
`           err_span:wikitext(" " .. v .. ";") end`
`       if namespace % 2 == 0 and namespace ~= 2 -- non-talk namespaces, excluding user pages; if modifying please update the description on the category page`
`           then err_span:wikitext(conf.ErrorCategory)`
`       end`
`       out = tostring(err_span)`
`       mw.addWarning(conf.MessageGlossingError)`
`   end`
`   if self.if_ambiguous_glosses then`
`       if namespace == 0 -- article namespace`
`           then out = out .. conf.AmbiguousGlossCategory -- this category will only track articles`
`       end`
`   end`
`   return out`

end function UserMessages:print_warnings()

`   local out = ""`
`   -- Messages and warnings get displayed only if the page is being viewed in "preview" mode:`
`   if displaying_messages and (next(self.gloss_messages) or next(self.warnings)) then`
`       local div = mw.html.create("div")`
`       div:addClass("messagebox")`
`           :css("margin", "inherit")`
`           :wikitext("`<i>`This message box is shown only in preview:`</i>`")`
`           :newline()`
`       for _,v in ipairs(self.warnings) do`
`           local p = div:tag("p")`
`           p:addClass(conf.class.ErrorMessage)`
`           p:attr("style", conf.style.ErrorMessage)`
`           p:wikitext(v)`
`       end`
`       if self.gloss_messages then`
`           div:wikitext("`

To change any of the following default expansions, see [the template's documentation](https://ja.wikipedia.org/wiki/Template:Interlinear/doc#Custom_abbreviations "wikilink"):

")

`           end`
`       for _,v in pairs(self.gloss_messages) do`
`           div:wikitext("`

" .. v .. "

")

`       end`
`       out = out .. "\n\n" .. tostring(div)`
`   end`
`   return out`

end

-----

\-- gloss_lookup() receives a gloss abbreviation and tries to uncover its meaning.

-----

local function gloss_lookup(a, label, wikilink)

`   local _label, _wikilink, _lookup = nil, nil, nil`
`   if gloss_override[a] then _lookup = gloss_override[a]`
`   elseif data.abbreviations[a] then _lookup = data.abbreviations[a] end`
`   if _lookup and _lookup.expansion ~= "" then`
`       _label, _wikilink = _lookup.expansion, _lookup.wikipage`
`   else`
`       local prefix = mw.ustring.sub(a,1,1)`
`       local suffix = mw.ustring.sub(a,2)`
`       if conf.combining_person[prefix] then -- is it of the form 1PL or 3FS?`
`           _label = conf.combining_person[prefix]`
`       local _suffix = conf.combining_number[suffix] or conf.combining_gender[suffix]`
`           if _suffix then`
`               _label = _label .. ", " .. _suffix`
`           else`
`               local suffix1 = mw.ustring.sub(suffix,1,1)`
`               local suffix2 = mw.ustring.sub(suffix,2)`
`                   if conf.combining_gender[suffix1]`
`                   and  conf.combining_number[suffix2] then`
`                       _label = _label .. ", " .. conf.combining_gender[suffix1] .. ", " .. conf.combining_number[suffix2]`
`                   else _label = nil end`
`           end`
`   elseif mw.ustring.match(suffix,conf.combining_gender_numbers) then -- cases like G4 = gender 4`
`       local _i,_j = mw.ustring.find(a, conf.combining_gender_numbers)`
`       local _pre = mw.ustring.sub(a, 1, _i - 1)`
`       local _suff = mw.ustring.sub(a, _i)`
`       if conf.combining_gender_prefixes[_pre] then`
`           _label = conf.combining_gender_prefixes[_pre] .. " " .. _suff`
`       end`
`   elseif prefix == "N" then -- dealing with cases like NPST = non-past`
`       local s = gloss_override[suffix] or data.abbreviations[suffix]`
`           if s ~= nil and not s.ExcludeNegation then`
`               _label = "non-" .. s.expansion`
`               _wikilink = s.wikipage`
`           end`
`           s = nil`
`       end`
`   end`
`   if _label == "" then _label = nil end`
`   if _wikilink == "" then _wikilink = nil end`
`   if not label then label = _label end`
`   if not wikilink then wikilink = _wikilink end`
`   return label, wikilink`

end

-----

\-- format_gloss() calls gloss_lookup() to find the meaning of a gloss -- abbreviation, which it then proceeds to format

-----

local function format_gloss(gloss, label, wikilink)

`   local gloss2 = mw.ustring.gsub(gloss,"<.->","") -- remove any html fluff`
`   gloss2 = mw.ustring.gsub(gloss2, "%'%'+", "") -- remove wiki bold/italic formatting`
`   gloss2 = mw.text.trim(mw.ustring.upper(gloss2))`
`   if not (label or wikilink)`
`       or (not label and glossing_type == "label")`
`       or (not wikilink  and glossing_type == "wikilink")`
`       then`
`           if glossing_type ~= "no abbr"`
`               then label, wikilink = gloss_lookup(gloss2, label, wikilink)`
`           end`
`   end`
`   local gloss_node`
`   if glossing_type == "no abbr"`
`       then gloss_node = mw.html.create("span")`
`   else gloss_node = mw.html.create("abbr") end`
`   gloss_node:addClass(conf.class.GlossAbbr)`
`   if label or wikilink then`
`       if not mw.ustring.match(gloss, "%l") -- excluding glosses that contain lower-case characters`
`           and not mw.ustring.match(gloss,conf.GlossSmallCapsExclude) -- and also excluding A, O etc. from rendering in small caps`
`           then gloss_node:attr("style", conf.style.GlossAbbr)`
`       end`
`       local abbr_label`
`       if label then abbr_label = label`
`           else abbr_label = wikilink end`
`       gloss_node:attr("title", abbr_label)`
`       if data.abbreviations[gloss2] then`
`           if data.abbreviations[gloss2].ambiguous then`
`               gloss_node:addClass(conf.class.GlossAbbrAmb)`
`                   msg:add("ambiguous gloss")`
`               end`
`       end`
`       if glossing_type == "wikilink" and wikilink`
`           then gloss_node:wikitext("`[`"``   ``,``   ``gloss,``   ``"`](https://ja.wikipedia.org/wiki/",_wikilink,_" "wikilink")`")`
`           else gloss_node:wikitext(gloss) end`
`       if displaying_messages then -- logging gloss lookups:`
`           local message = ""`
`           if label then`
`               message = "assuming " .. gloss2 .. " means \"" .. abbr_label .. "\";" end`
`           if glossing_type == "wikilink" and wikilink then`
`               message = message .. " linking to `[`"``   ``..``   ``wikilink``   ``..``   ``"`](https://ja.wikipedia.org/wiki/"_.._wikilink_.._" "wikilink")`;"`
`           end`
`           msg:add("gloss_message", message, gloss)`
`       end`
`   elseif glossing_type == "no abbr"`
`       then gloss_node`
`               :attr("style", conf.style.GlossAbbr)`
`               :wikitext(gloss)`
`   else`
`       if displaying_messages then`
`           msg:add("warning", "Gloss abbreviation " .. highlight(gloss2) .. "  not recognised" .. help_link("gloss abbr"))`
`       end`
`       msg:add("non-repeating error", "Unknown glossing abbreviation(s)" .. help_link("gloss abbr"))`
`       gloss_node`
`           :addClass(conf.class.GlossAbbrError)`
`           :addClass("error")`
`           :css("font-size", "100%")`
`           :attr("title", gloss2 .. ": glossing abbreviation not found")`
`           :attr("style", conf.style.ErrorMessage)`
`           :wikitext(gloss)`
`   end`
`   return tostring(gloss_node)`

end

-----

\-- find_gloss() parses a word into morphemes, and it calls format_gloss() -- for anything that looks like a glossing abbreviation.

-----

local function find_gloss(word)

`   local function scan_gloss(boundary, gloss_abbr) -- checks a morpheme if it is a gloss abbreviation`
`       if (mw.ustring.match(gloss_abbr, conf.GlossAbbrPattern)`
`           or conf.LowerCaseGlosses[gloss_abbr])`
`           and not (conf.GlossExcludeTable[gloss_abbr]`
`               or mw.ustring.match(gloss_abbr, conf.GlossExcludePattern))`
`           then gloss_abbr = format_gloss(gloss_abbr)`
`       end`
`       return boundary .. gloss_abbr`
`   end`
`   local word = mw.text.decode(word, true)`
`   if word == "I" -- for the case of the English word "I", the 1SG pronoun`
`       then return word end`
`   local pattern = "([" .. conf.GlossAbbrBoundary .. "]?)([^" .. conf.GlossAbbrBoundary .. "]+)"`
`   word = mw.ustring.gsub(word, pattern, scan_gloss) -- splits into morphemes`
`   return word`

end

-----

\-- The main purpose of the bletcherous parse() is to split a line into words and and then for each eligible word -- to call find_gloss(). The parser outputs the individual words (with any gloss abbreviation formatting applied). -- The simple job of splitting at whitespaces has been made complicated by a) the fact that the input can contain -- whitespaces inside the various html elements that are the result of the application of various formatting templates; -- and b) the need to be able to recognise the output of the template that formats custom gloss abbreviations -- (and hence skip passing it on to find_gloss). See talk for a suggestion about its future.

-----

local function parse(cline, i, tags_found,ifglossing)

`   local function issue_error(message, culprit)`
`       UserMessages:add("error",  message .. ": `*`"``   ``..``   ``mw.ustring.sub(cline.whole,``   ``1,``   ``i-1)``   ``..``   ``"`**`"``   ``..``   ``culprit``   ``..``   ``"`***`")`
`   end`
`   if i > cline.length then return i end --this will only be triggered if the current line has less words than line 1`
`   local next_step, j, _, chunk`
`   local probe = mw.ustring.sub(cline.whole,i,i)`
`   if mw.ustring.match(probe,"[" .. conf.WordSeparator .. "]") and tags_found == 0`
`       then next_step =  i-1`
`   elseif probe == "[" then --Wikilink?`
`       if mw.ustring.sub(cline.whole,i+1,i+1) == "[" then`
`           _,j,chunk = mw.ustring.find(cline.whole,"(%[%[.-%]%])", i)`
`       else chunk = "["; j = i end --not a wikilink then`
`       buffer = buffer .. chunk`
`       next_step =  parse(cline, j+1,tags_found,ifglossing)`
`   elseif probe == "{"  and tags_found == 0 then --curly brackets enclose a sequence of words to be treated as a single unit`
`       _,j,chunk = mw.ustring.find(cline.whole,"(.-)(})", i+1)`
`       if not chunk then`
`           issue_error("Unclosed curly bracket", "{")`
`           chunk = highlight("{"); j = i`
`       elseif ifglossing==true then`
`           chunk = find_gloss(chunk)`
`       else`
`           if cline.tone_sup then chunk = tone_sup(chunk) end`
`       end`
`       buffer = buffer .. chunk`
`       next_step =  parse(cline, j+1,tags_found,ifglossing)`
`   elseif probe == "<" then -- We've encountered an HTML tag. What do we do now?`
`       local _,j,chunk = mw.ustring.find(cline.whole,"(<.->)",i)`
`       if not chunk then`
`           issue_error("Unclosed angle bracket", "<")`
`           chunk = highlight("<"); j = i`
`       elseif mw.ustring.sub(cline.whole,i,i+1) == "</" then -- It's a CLOSING tag`
`           if cline.glossing`
`               and ifglossing==false`
`               and mw.ustring.match(chunk,"`</abbr>`")`
`               then ifglossing=true end`
`           tags_found = tags_found - 1`
`       elseif not mw.ustring.match(chunk, "/>$") -- It's an OPENING tag, unless it opens a self-closing element (in which case the element is ignored)`
`           then if ifglossing == true -- the following checks for the output of ``:`
`                   and mw.ustring.find(chunk, conf.class.GlossAbbr, 1, true) -- it's important that the "find" function uses literal strings and not patterns`
`                       then ifglossing = false end`
`           tags_found = tags_found + 1`
`       end`
`       buffer = buffer .. chunk`
`       next_step = parse(cline, j+1,tags_found,ifglossing)`
`   else -- No HTML tags, so we only need to find where the word ends`
`       local _,k,chunk = mw.ustring.find(cline.whole,"(..-)([ <[])",i)`
`       if k then --ordinary text`
`           if ifglossing==true then`
`               buffer = buffer .. find_gloss(chunk)`
`           else`
`               if cline.tone_sup then chunk = tone_sup(chunk) end`
`               buffer = buffer .. chunk`
`           end`
`           next_step = parse(cline, k, tags_found, ifglossing)`
`       else -- reached end of string`
`           if ifglossing == true then`
`               chunk = find_gloss(mw.ustring.sub(cline.whole,i))`
`           else`
`               chunk = mw.ustring.sub(cline.whole,i)`
`               if cline.tone_sup then chunk = tone_sup(chunk) end`
`           end`
`           buffer = buffer .. chunk`
`           next_step = cline.length`
`       end`
`   end`
`   return next_step`

end

-----

\-- The following function is called by Template:gcl and is used for formatting an individual glossing abbreviation

-----

function p.gcl(frame)

`   local args = getArgs(frame,{`
`       trim = true,`
`       removeBlanks = false,`
`       parentOnly = true,`
`       wrappers = {'Template:Gcl'},`
`   })`
`   msg = UserMessages`
`   set_global_glossing_settings{style = args.style, underline = args.underline, small_caps = args['small-caps']}`
`   if not args.glossing then`
`       glossing_type = conf.GlossingType -- a global variable`
`   else glossing_type = set_glossing_type(args.glossing)`
`   end`
`   local gloss, label, wikilink = args[1], args[2], args[3]`
`   if not gloss then UserMessages:add("error", "No gloss supplied")`
`       return UserMessages:print() end`
`   if wikilink and not args.glossing then -- if a wikilink is supplied and glossing isn't set to 'label'...`
`       glossing_type = 'wikilink' end --     .. then the wikilink will be formatted as such`
`   if label == "" then label = nil end`
`   if wikilink == "" then wikilink = nil end`
`   local result = format_gloss(gloss, label, wikilink)`
`   return result`

end

-----

\-- The following is the function called by Template:Interlinear. -- It processes the template arguments, then calls parse() to split the input lines into words -- and it then builds the output html.

-----

function p.interlinearise(frame)

-----

\-- Prepare arguments

-----

`   local if_auto_translit = false`
`   local args = getArgs(frame, { -- configuration for Module:Arguments`
`       trim = true,`
`       removeBlanks = false,`
`       parentFirst = true,`
`       wrappers = {'Template:Interlinear', 'Template:Fs interlinear'},`
`   })`
`   local template_name = frame:getParent():getTitle()`
`   if template_name == 'Template:Fs interlinear' then`
`       args.italics1 = args.italics1 or "no"`
`       args.italics2 = args.italics2 or "yes"`
`       args.glossing3 = args.glossing3 or "yes"`
`       if args.transl and not args.transl2 then args.transl2 = args.transl end`
`       if_auto_translit = true`

`   end`
`   local revid = frame:preprocess( "``" )`
`   if  revid == "" then`
`       if not args['display-messages'] or yesno(args['display-messages']) then`
`       displaying_messages = true end-- messages will be displayed only in preview mode`
`   end`
`   msg = UserMessages`
`   local line = {}`

`   local function set_italics(n)`
`       line[n].attr.style = line[n].attr.style .. "font-style: italic;"`
`       line[n].tone_sup = true -- single digits are assumed to be tone markers and will hence be superscripted`
`       if args['tone-superscripting'] and not yesno(args['tone-superscripting'])`
`           then line[n].tone_sup = false end`
`   end`

`   if args.glossing then -- the glossing= parameter sets the default glossing type`
`       local _gl = set_glossing_type(args.glossing)`
`       if _gl then conf.GlossingType = _gl end`
`   end`
`   --this looks for a list of glossing abbreviations on the page that transcludes the template:`
`   local _ablist_section = frame:preprocess('{{#section:``|list-of-glossing-abbreviations}}')`
`   if _ablist_section and _ablist_section ~= "" then`
`       local _a = mw.ustring.gsub(_ablist_section, '`

</?div [^\n]*>

', '') -- strips off the div tags

`       set_custom_glosses(_a)`
`   end`
`   --and this looks looks for a list of abbreviations set within the template:`
`   local _ablist = args.abbreviations or args.ablist`
`   if _ablist and _ablist ~= ""`
`       then set_custom_glosses(_ablist) end`

`   local _spacing = tonumber(args.spacing)`
`   if _spacing and _spacing <= 20`
`       then conf.style.WordDiv = conf.style.WordDiv .. 'margin-right: ' .. _spacing .. 'em;'`
`   else conf.style.WordDiv = conf.style.WordDiv .. conf.style.WordMargin`
`   end`

`   local offset, last_line = 0, 0`
`   for j,v in ipairs(args) do -- iterates over the unnamed parameters from the template`
`       last_line = last_line +1`
`       if is_empty(v)`
`           then offset = offset + 1`
`       else`
`       local i = j - offset`
`       line[i] = {}`
`       v = normalise(v)`

`       -- the following is part of a trial implementation of automatic transliteration:`
`       if if_auto_translit and v == "auto" and i > 1 then`
`           local source_line = line[i-1]`
`           local src_lang = source_line.lang`
`           if not src_lang then src_lang = args.lang end`
`           if src_lang then`
`                   v = transliterate(source_line.whole, src_lang)`
`           else v = ""; msg:add("error", "No language specified for automatic transliteration")`
`           end`
`       end  -- end of trial block`

`       line[i].whole = v`
`       line[i].length = mw.ustring.len(v)`

`       local _c = args["c" .. i]`
`       if _c and _c ~= "" then`
`           line.hasComments = true`
`           line[i].c = _c`
`       end`

`       ---prepare style arguments----`
`       line[i].class = ""`
`       local _style = args["style" .. i]`
`       if not _style then _style = ""`
`       else _style = tidyCss(_style) end`
`       --line[i].attr holds the attributes for the `

elements that enclose the words in line i

`       line[i].attr = {style = conf.style.WordP .. _style}`

`       local _lang = args["lang" .. i]`
`       if _lang and #_lang > 1 then`
`           line[i].lang = _lang`
`       else _lang = args.lang`
`           if _lang and #_lang > 1 and i == 1 then -- if a lang= parameter is supplied, it's assumed to apply to line 1`
`               line[i].lang = _lang`
`           end`
`       end`
`       line[i].attr.lang = line[i].lang`

`       if yesno(args["italics" .. i]) then`
`           set_italics(i)`
`       end`

`       local _transl = args["transl" .. i]`
`       if _transl and #_transl > 1 then`
`           _transl = mw.ustring.lower(_transl)`
`           local _lookup = lang_data.translit_title_table[_transl]`
`           if _lookup then`
`               if _lang and  _lookup[_lang] then`
`                   _transl = _lookup[_lang]`
`               else _transl = _lookup.default`
`               end`
`               if _transl then`
`                   line[i].attr.title = _transl`
`               end`
`           else  msg:add("error", "Transliteration scheme '" .. _transl .. "' not recognised")`
`           end`
`       end`

`       local _glossing = args["glossing" .. i]`
`       if _glossing then`
`           line[i].glossing = set_glossing_type(_glossing)`
`           -- Do not treat default glossing settings as custom.`
`           if not ((i == 1 and not yesno(_glossing)) or (i == 2 and yesno(_glossing))) then`
`               line.HasCustomGlossing = true`
`           end`
`       end`

`       local _ipa = args['ipa' .. i]`
`       if yesno(_ipa) then`
`           line[i].class = "IPA"`
`       end`

`       local _class = args['class' .. i]`
`       if _class then`
`           line[i].class = line[i].class .. " " .. _class`
`       end`

`       if line[i].class == ""`
`           then line[i].class = nil end`
`       end -- ends the first if-statement in the loop`
`   end -- ends the FOR cycle`

`   local line_count = #line`
`   if line_count == 0 then`
`       msg:add("error", template_name .. ": no lines supplied.")`
`       return msg:print_errors()`
`   end`

`   if line_count > 1 then`
`       local _italics = args.italics`
`       local n = tonumber(_italics)`
`       if n and n > 0 then`
`           set_italics(n)`
`       elseif not (_italics and not yesno(_italics)) and not (args["italics1"] and not yesno(args["italics1"])) then`
`           set_italics(1) -- by default, the first line will get italicised, unless italics=no or italics1=no`
`       end`
`       -- the last unnamed parameter is assumed to be the free translation:`
`       free_translation = args[last_line]`
`       if not is_empty(free_translation) then`
`           line [line_count] = nil   end  --... and is thus excluded from interlinearising`
`   end`

\-- If glossing isn't specified for any line, then it's chosen by default to occur -- in the second line, unless only a single line has been supplied, in which case -- the assumption is that it is the one containing grammatical glosses

`   if yesno(args.glossing) == false then`
`       line.HasCustomGlossing = true`
`   end`
`   if not line.HasCustomGlossing then`
`       if line_count == 1 then`
`           line[1].glossing = conf.GlossingType`
`       elseif line[2] then`
`           line[2].glossing = conf.GlossingType`
`       end`
`   end`
`   set_global_glossing_settings{style = args['glossing-style'], underline = args.underline, small_caps = args['small-caps']}`

-----

\-- Segment lines into words

-----

`   for i,v in ipairs(line) do`
`       local ifglossing = false`
`       if line[i].glossing then`
`           ifglossing = true -- if true the parser will attempt to format gloss abbreviations in the current line`
`           glossing_type = line[i].glossing -- neccessarily a global variable`
`       end`
`       local wc, n = 1, 1`
`       line[i].words = {}`
`       while n <= line[i].length do`
`           buffer = ""`
`           n = parse(line[i], n, 0, ifglossing)+2`
`           line[i].words[wc] = buffer`
`           wc = wc + 1`
`       end`
`   end`

`   ----Check for mismatches in number of words across lines----`
`   local number_of_words, mismatch_found = 0, false`
`   for i,v in ipairs(line) do -- find the maximum number of words in any line`
`       local wc = #line[i].words`
`       if wc ~= number_of_words then`
`           if i ~= 1 and wc ~= 0 then`
`               mismatch_found = true`
`           end`
`           if wc > number_of_words then`
`               number_of_words = wc`
`           end`
`       end`
`   end`
`   ----Deal with mismatches---`
`   if mismatch_found then`
`       local error_text = "Mismatch in the number of words between lines: "`
`       for i,v in ipairs(line) do`
`           local wc = #line[i].words`
`           error_text = error_text .. wc .. " word(s) in line " .. i .. ", "`
`           if wc ~= number_of_words then`
`               for current_word = wc+1, number_of_words do`
`                   line[i].words[current_word] = " "`
`               end`
`           end`
`       end`
`       if string.sub(error_text, -2) == ", "`
`           then error_text = string.sub(error_text, 1, #error_text - 2) .. " "`
`       end`
`       error_text = error_text .. help_link("mismatch")`
`       UserMessages:add("error", error_text)`
`   end`

-----

\-- Build the HTML

-----

`   ---- If just a single line was supplied, format it as inline text`
`   if line_count == 1 then`
`       local span = mw.html.create('span')`
`       span:attr(line[1].attr)`
`       for wi = 1, number_of_words do`
`           local space`
`           if wi < number_of_words then space = " " else space = "" end`
`           span:wikitext(line[1].words[wi] .. space)`
`       end`
`       return tostring(span)`
`   end`

`   ---- More than one line supplied, so we'll produce interlinear display`
`   local div = mw.html.create("div")`
`   div:addClass(conf.class.Interlinear)`

`   -- For stuff to be displayed in the left margin, like example numbering`
`   local number, indent = nil, nil`
`   if args.number and args.number ~= ""`
`       then number = args.number end`
`   if args.indent and args.indent ~=""`
`       then indent = args.indent end`
`   if indent or number then`
`       if not indent then indent = "4" end --default value`
`       div:css("margin-left", indent .. 'em')`
`       if number then`
`           div:tag("div")`
`               :css("position", "absolute")`
`               :css("left", "1em")`
`               :wikitext(args.number)`
`       end`
`   end`

`   if args.box and args.box ~= "" then`
`       div:css("background-color", "#f8f9fa")`
`           :css("border", "1px solid #eaecf0")`
`           :css("padding", "1em") end`
`   if args.top and args.top ~= "" then --lines to display above the interlinear block`
`       div:tag("div")`
`           :wikitext(args.top)`
`   end`

`   -- Producing the interlinear block`
`   for wi = 1, number_of_words do`
`       local div2 = div:tag("div")`
`                   :attr("style", conf.style.WordDiv)`
`       for i,_ in ipairs (line) do`
`           if line[i].whole ~= "" then -- skipping empty lines`
`               local p = div2:tag("p")`
`               p:attr(line[i].attr)`
`               if line[i].class then`
`                   p:addClass(line[i].class)`
`               end`
`               local _text = line[i].words[wi]`
`               if _text == "" or _text == " "`
`                   then _text = " " end -- `

elements without content mess up the interlinear display

`               p:wikitext(_text)`
`           end`
`       end`
`   end`

`   --- If any "comments" have been specified, add them at the end of each line`
`   if line.hasComments then`
`       local divc = div:tag("div")`
`                   :attr("style", conf.style.WordDiv)`
`       for i,_ in ipairs (line) do`
`           local p = divc:tag("p")`
`           p:attr("style", conf.style.WordP)`
`           if line[i].c then`
`               p:wikitext(line[i].c)`
`           else p:wikitext(" ")`
`           end`
`       end`
`   end`

`   --Add hidden lines containing the content of each line of interlinear text: this is for accessibility`
`   for i,v in ipairs(line) do`
`       local hidden_line = div:tag("p")`
`       hidden_line:attr("style", conf.style.HiddenText)`
`                   :wikitext(v.whole)`
`   end`

`   -- Format the free translation`
`   local ft_line = div:tag("p")`
`   if free_translation and free_translation ~= "" then`
`       ft_line:attr("style", "clear: left;")`
`       ft_line:wikitext(free_translation)`
`   end`
`   if args.bottom and args.bottom ~= ""`
`       then local bottom = div:tag('p')`
`       bottom:css('margin-top', '0')`
`       bottom:wikitext(args.bottom)`
`   end`
`   ft_line:node(msg:print_errors()) -- for error messages`

`   local end_div = div:tag("div")`
`       end_div:attr("style", conf.style.EndDiv)`
`   div:newline()`
`   local temp_track = ""`
`   if last_line == 2`
`       then temp_track = ""`
`   end`
`   if last_line > 3 and template_name ~= 'Template:Fs interlinear'`
`       then  temp_track = ""`
`   end`
`   return tostring(div) .. temp_track .. msg:print_warnings()`

end

return p

[Category:Pages_with_errors_in_interlinear_text](https://ja.wikipedia.org/wiki/Category:Pages_with_errors_in_interlinear_text "wikilink") [Category:Articles_with_ambiguous_glossing_abbreviations](https://ja.wikipedia.org/wiki/Category:Articles_with_ambiguous_glossing_abbreviations "wikilink") [Category:Pages_with_interlinear_glosses_using_two_unnamed_parameters](https://ja.wikipedia.org/wiki/Category:Pages_with_interlinear_glosses_using_two_unnamed_parameters "wikilink") [Category:Pages_with_interlinear_glosses_using_more_than_three_unnamed_parameters](https://ja.wikipedia.org/wiki/Category:Pages_with_interlinear_glosses_using_more_than_three_unnamed_parameters "wikilink")