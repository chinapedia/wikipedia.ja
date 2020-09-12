> この記事は[モジュール:Broodkruimel](https://ja.wikipedia.org/wiki/モジュール:Broodkruimel)から翻訳されています。


local p = {}

\-- Openingstag voor alle tabellen in de broodkruimel p.table = '

<table cellspacing="1" cellpadding="0">

' -- Curly dinges voor achter vertakkingen p.curly = '<big>}</big>' -- Wolkje voor weggelaten categorieen p.wolkje = '(...)' -- Maximaal aantal categorieen voor we het voor gezien houden p.MAX = 50 -- Categorie waar we pagina's met broodkruimelproblemen in zetten p.probleemcat = 'テンプレート呼び出しエラーのあるページ/Template:パンくず小路'

\-- We houden bij of we problemen tegenkomen. Het soort probleem -- geven we aan met een letter die als sorteersleutel in de -- probleemcategorie gebruiken. Als er meer problemen zijn, nemen -- we gewoon de laatste. -- "C": er is iets mis met de wikitekst. Mogelijk een ontbrekende -- sluittag oid. -- "P": parameterprobleem: er is een ongeldige waarde voor -- een parameter opgegeven -- "M": we hebben p.MAX bereikt, dus de boom is niet af -- "O": de pagina (of categorie) is ongecategoriseerd p.problemen = ""

\--\[\[

`   broodkruimel( frame )`

`   Maakt een broodkruimelnavigatie voor de categorieen van een pagina.`
`   Als frame.args[pagina] opgegeven is, wordt die pagina gebruikt.`
`   Zoniet, en frame.args[1] is opgegeven, dan wordt die pagina gebruikt.`
`   Als geen van beiden opgegeven is, wordt de huidige pagina gebruikt.`
`   `

\]\] function p.broodkruimel( frame )

`   -- Voor welke pagina?`
`   local title = frame.args.page or frame.args[1]`
`   if ( not title or title == "" ) then`
`       title = mw.title.getCurrentTitle().prefixedText`
`   end`
`   `
`   -- Hoogte?`
`   local level = 8`
`   p.force = false`
`   if ( frame.args.length and frame.args.length ~= "" ) then`
`       n = tonumber( frame.args.length )`
`       if ( n ~= nil and n > 0 ) then`
`           level = n`
`           if ( frame.args.force and frame.args.force ~= "" ) then`
`               p.force = true`
`           end`
`       else`
`           p.probleem( "P" )`
`       end`
`   end`
`   `
`   -- Maximale aantal parallelle vertakkingen?`
`   p.max_branch = 4`
`   if ( frame.args.maxbranch and frame.args.maxbranch ~= "" ) then`
`       local n = tonumber( frame.args.maxbranch )`
`       if ( n ~= nil and n > 0 ) then`
`           p.max_branch = n`
`       else`
`           p.probleem( "P" )`
`       end`
`   end`
`   `
`   -- Text verkleinen?`
`   local txtsize = 20`
`   p.verklein = false`
`   if ( frame.args.startsize and frame.args.startsize ~= "" ) then`
`       p.verklein = true`
`       local n = tonumber( frame.args.startsize ) `
`       if ( n ~= nil and n > 0 ) then`
`           txtsize = 2 * n`
`       else`
`           p.probleem( "P" )`
`       end`
`   end`
`   `
`   -- Negeerlijst?`
`   p.negeerlijst = {}`
`   if ( frame.args.ignore and frame.args.ignore ~= "" ) then`
`       p.negeerlijst = p.parseNegeerLijst( frame.args.ignore )`
`   end`
`       `
`   -- Maak boom`
`   local trees = p.createCategoryTree( title, level )`
`   `
`   -- Maak kruimel`
`   local ntitle, ntree = next( trees )`
`   local kruimel = ""`
`   if ( type( ntree ) == "table" and next( ntree ) ) then`
`       kruimel = p.createBreadCrumb( ntitle, ntree, txtsize )`
`   else`
`       -- Als we geen broodkruimel kunnen maken omdat de pagina`
`       -- in meer dan max_branch cats zit, printen we simpelweg de`
`       -- bovenliggende cats: i.v.m. de layout moeten we in ieder`
`       -- geval iets tonen.`
`       kruimel = p.printcats( p.hoofdcats )`
`       if ( p.hoofdcats == nil or next( p.hoofdcats ) == nil ) then`
`           -- ongecategoriseerde pagina`
`           p.probleem( "O" )`
`       end`
`   end`
`   `
`   return kruimel .. p.printprobleem()`
`   `

end

\--[parseCategories( wikitext ) Zoekt geldige categorieen in wikitext.](https://ja.wikipedia.org/wiki/parseCategories\(_wikitext_\)_Zoekt_geldige_categorieen_in_wikitext. "wikilink") function p.parseCategories( txt )

`   if ( txt == nil ) then return {} end`
`   `
`   local cats = {}`
`   `
`   local pattern = "%[%[%s*[Cc][Aa][Tt][Ee][Gg][Oo][Rr][Yy]?%s*:%s*([^|%]]+)[|%]]"`
`       `
`   for category in mw.ustring.gmatch( txt, pattern ) do`
`       category = p.cleanupCatTitle( category )`
`       -- Sla categorieen met gekke dingen over: sjablonen e.d. `
`       if ( mw.ustring.find( category, "[{}%[%]]" ) == nill) then`
`           -- Als de naam langer is dan 50 tekens is er waarschijnlijk`
`           -- iets mis `
`           if ( mw.ustring.len( category ) < 100 ) then`
`               if ( p.negeerlijst[category] == nil ) then`
`                   cats[category] = ""`
`                   p.branchcount = p.branchcount + 1`
`               end`
`           else`
`               if ( p.hoofdcats == nil ) then`
`                   p.probleem( "C" )`
`               end`
`           end`
`       end`
`   end`
`   `
`   if ( p.hoofdcats == nil ) then`
`       -- De cats direct boven de pagina slaan we op voor: die `
`       -- gebruiken we als we geen boom kunnen maken`
`       p.hoofdcats = cats`
`   end`
`   `
`   return cats`
`   `

end

\--[createCategoryTree( title, maxlevel ) Maakt een boom van de categorieen boven title, tot een afstand van maxlevel. Stopt als de boom meer dan p.max_branch takken bevat.](https://ja.wikipedia.org/wiki/createCategoryTree\(_title,_maxlevel_\)_Maakt_een_boom_van_de_categorieen_boven_title,_tot_een_afstand_van_maxlevel._Stopt_als_de_boom_meer_dan_p.max_branch_takken_bevat. "wikilink") function p.createCategoryTree( title, maxlevel )

`   local level = 0`
`   local tree = { [title] = "" } `
`   `
`   p.seen = {}`
`   p.count = 0`
`   `
`   while level < maxlevel do`
`       level = level + 1`
`       p.branchcount = 0`
`       local new_tree = p.addLevel( mw.clone (tree) )`
`       if ( not p.force and p.branchcount > p.max_branch ) then`
`           return tree`
`       elseif ( new_tree == nil ) then`
`           return tree`
`       end`
`       tree = new_tree`
`   end`
`   `
`   return tree`
`   `

end

function p.addLevel ( tree )

`   local result = {}`
`   `
`   for cat,rest in pairs( tree ) do`
`       `
`       if ( rest == "" ) then`
`           if ( p.seen[cat] ) then`
`               if ( cat == "Category:主要カテゴリ" ) then`
`                   result[cat] = {}`
`               else`
`                   result[cat] = { ["..."] = {} }`
`                   p.branchcount = p.branchcount + 1`
`               end`
`           else`
`               p.count = p.count + 1`
`               if ( p.count > p.MAX ) then`
`                   p.probleem( "M" )`
`                   return nil`
`               end`
`               page = mw.title.new( cat )`
`               local cats = p.parseCategories( page:getContent() )`
`               result[cat] = cats`
`               p.seen[cat] = true`
`           end`
`       else`
`           local temp = p.addLevel( rest )`
`           if ( temp == nil ) then`
`               return nil`
`           else`
`               result[cat] = temp`
`           end`
`       end`
`   end`
`   `
`   return result`
`   `

end

\--[createBreadCrumb( title, trees, txtsize ) Maakt een breadcrumb navigatie voor trees. title: de titel van de pagina waarvoor de breadcrumb is trees: de categoriebomen zoals gemaakt door createCategoryTrees(title) txtsize: lettergrootte](https://ja.wikipedia.org/wiki/createBreadCrumb\(_title,_trees,_txtsize_\)_Maakt_een_breadcrumb_navigatie_voor_trees._title:_de_titel_van_de_pagina_waarvoor_de_breadcrumb_is_trees:_de_categoriebomen_zoals_gemaakt_door_createCategoryTrees\(title\)_txtsize:_lettergrootte "wikilink") function p.createBreadCrumb( title, tree, txtsize )

`       tree = tree or {}`
`   local str = ""`
`   `
`   if ( p.verklein ) then`
`       str = str .. '`

<div style="font-size: ' .. math.floor( txtsize/2 ) .. 'pt">

'

`   end`
`   `
`   str = str .. p.table .. '`

<tr>

<td align="right">

'

`   local count = 0`
`   `
`   for ntitle, ntree in pairs( tree ) do`
`       count = count + 1`
`       if ( ntitle == "..." ) then`
`           str = str .. p.wolkje`
`       else`
`           if ( type( ntree ) == "table" ) then`
`               str = str .. p.createBreadCrumb( ntitle, ntree, txtsize-1 ) `
`           else`
`               str = str .. p.createBreadCrumb( ntitle, {}, txtsize-1 ) `
`           end`
`       end`
`   end`
`   `
`   str = str .. "`

</td>

<td>

"

`   if ( count > 1 ) then`
`       str = str .. p.curly .. '`

</td>

<td align="right">

'

`   end`
`   if ( count > 0 ) then`
`       str = str .. '`

</td>

<td>

 → 

</td>

<td>

'

`   end`
`   `
`   str = str .. "`[`"``   ``..``   ``p.removeCatNS(``   ``title``   ``)``   ``..``   ``"`](https://ja.wikipedia.org/wiki/:"_.._title_.._" "wikilink")`"`
`   str = str .. "`

</td>

</tr>

</table>

"

`   if ( p.verklein ) then str = str .. "`

</div>

" end

`   return str`
`   `

end

\--[cleanupCatTitle( title ) Standaardiseert een categorienaam: overbodige spaties aan begin en eind weg, underscores vervangen door spaties, de eerste letter een hoofdletter, naamruimte ervoor.](https://ja.wikipedia.org/wiki/cleanupCatTitle\(_title_\)_Standaardiseert_een_categorienaam:_overbodige_spaties_aan_begin_en_eind_weg,_underscores_vervangen_door_spaties,_de_eerste_letter_een_hoofdletter,_naamruimte_ervoor. "wikilink") function p.cleanupCatTitle( title )

`   title = mw.text.trim( title )`
`   title = p.removeCatNS( title )`
`   title = mw.ustring.gsub( title, "_", " " )`
`   title = mw.language.getContentLanguage():ucfirst( title )`
`   title = "Category:" .. title`
`   `
`   return title`
`   `

end

\--[removeCatNS( title ) Verwijdert "Categorie:" of "Category:"](https://ja.wikipedia.org/wiki/removeCatNS\(_title_\)_Verwijdert_"Categorie:"_of_"Category:" "wikilink") function p.removeCatNS( title )

`   title = mw.ustring.gsub( title, "^[Cc][Aa][Tt][Ee][Gg][Oo][Rr][Yy]%s*:%s*", "" )`
`   return title`

end

\--[parseNegeerLijst( str ) Parsed een door komma's gescheiden lijst van categorienamen](https://ja.wikipedia.org/wiki/parseNegeerLijst\(_str_\)_Parsed_een_door_komma's_gescheiden_lijst_van_categorienamen "wikilink") function p.parseNegeerLijst( str )

`   local lijst = {}`
`   `
`   cats = mw.text.split( str, ',', true )`
`   `
`   for _, cat in pairs( cats ) do`
`       cat = p.cleanupCatTitle( cat )`
`       lijst[cat] = ""`
`   end`
`   `
`   return lijst`

end

\--[printCats( cats ) Print de categorieen in cats. Als we geen broodkruimel kunnen we maken gebruiken we deze functie om simpelweg de direct bovenliggende cats te tonen.](https://ja.wikipedia.org/wiki/printCats\(_cats_\)_Print_de_categorieen_in_cats._Als_we_geen_broodkruimel_kunnen_we_maken_gebruiken_we_deze_functie_om_simpelweg_de_direct_bovenliggende_cats_te_tonen. "wikilink") function p.printcats( cats )

`   local str = ""`
`   `
`   str = str .. "`

<div style='text-align: left;'>

 カテゴリ: "

`   if ( ( type( cats ) ~= "table" ) or next( cats ) == nil ) then`
`       str= str .. "`*`No`*`"`
`   else`
`       for cat in pairs( cats ) do`
`           str = str .. '`[`'``   ``..``   ``p.removeCatNS(``   ``cat``   ``)``   ``..``   ``'`](https://ja.wikipedia.org/wiki/:'_.._cat_.._' "wikilink")`'`
`           if ( next( cats, cat ) ~= nil ) then`
`               str = str .. " • "`
`           end`
`       end`
`   end`
`   `
`   str = str .. '`

</div>

'

`   return str`
`   `

end

function p.printprobleem( )

`   if ( p.problemen ~= nil and p.problemen ~= "" ) then`
`       return ""`
`   else`
`       return ""`
`   end`

end

function p.probleem( letter )

`   p.problemen = letter`

end

\--[pptable( table ) Maakt een string van een table gemaakt door createCategoryTrees(). Alleen voor testen en debuggen.](https://ja.wikipedia.org/wiki/pptable\(_table_\)_Maakt_een_string_van_een_table_gemaakt_door_createCategoryTrees\(\)._Alleen_voor_testen_en_debuggen. "wikilink") function p.pptable( table )

`   local str = ""`
`       table = table or {}`

`   for k,v in pairs( table ) do`
`       str = str .. k .. ": "`
`       if ( type( v ) == "string" ) then`
`       else`
`           str = str .. "{" .. p.pptable(v) .. "}, "`
`       end`
`       `
`   end`
`   `
`   return str`

end

return p

[Category:"_.._p.probleemcat_.._"](https://ja.wikipedia.org/wiki/Category:"_.._p.probleemcat_.._" "wikilink")