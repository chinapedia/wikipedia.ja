> この記事は[モジュール:Template parameter value](https://ja.wikipedia.org/wiki/モジュール:Template_parameter_value)から翻訳されています。


local p = {} local escape = require("Module:String")._escapePattern function trimspaces(s)

`   return string.gsub(s, "^%s*(.-)%s*$", "%1")`

end

local function getTitle(title)

`   local success, titleObj = pcall(mw.title.new, title)`
`   if success then return titleObj`
`   else return nil end`

end

function p.main(frame)

`   local args = require('Module:Arguments').getArgs(frame, {`
`       wrappers = 'Template:Template parameter value'`
`   })`
`   local template = escape(args[2])`
`   local parameter = escape(args[4])`
`   local numberedParameter = (tonumber(parameter) ~= nil)`
`   `
`   local templateCount = 0`
`   local parameterCount = 0`
`   local templateMatch = tonumber(args[3] or 1)`
`   local parameterMatch = tonumber(args[5] or 1)*(numberedParameter and parameter or 1)`
`   `
`   local targettitle = getTitle(args[1])`
`   if targettitle == nil then return "" end`
`   local content = string.gsub(targettitle:getContent() or "", "[\r\n]", "")`
`   `
`   while templateCount ~= templateMatch do`
`       if content == nil then return "" end`
`       content = string.match(content, '{{' .. template .. "(.+)")`
`       templateCount = templateCount + 1`
`   end`
`   `
`   while parameterCount ~= parameterMatch do`
`       if content == nil then return "" end`
`       content = string.match(content, '|%s*' .. (numberedParameter and "" or parameter .. '%s*=%s*') .. '([^|].*)')`
`       parameterCount = parameterCount + 1`
`   end`
`   `
`   if content == nil then return "" end`
`   `
`   content = string.gsub(content, "`

</?%a*include%a*>

", "")

`   content = string.match(content, '^([^|}]*{{[^}]+}}[^|}]*)|') or string.match(content, '([^|}]+)')`
`   content = frame:preprocess{text = content}`
`   content = trimspaces(content)`
`   `
`   return content`

end

return p