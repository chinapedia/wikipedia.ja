> この記事は[モジュール:Colored list](https://ja.wikipedia.org/wiki/モジュール:Colored_list)から翻訳されています。


local sequences = {

`   excel = {`
`       [0]='#274',`
`       [1]='#36C',`
`       [2]='#C33',`
`       [3]='#85B',`
`       [4]='#072',`
`       [5]='#B38',`
`       [6]='#B40',`
`       [7]='#279'`
`   }, calc = {`
`       [0] = '#0000FF',`
`       [1] = '#FF0000',`
`       [2] = '#FF00FF',`
`       [3] = '#008000',`
`       [4] = '#000080',`
`       [5] = '#800000',`
`       [6] = '#800080',`
`       [7] = '#808000'`
`   }, accent = {`
`       [0]='#7fc97f',`
`       [1]='#beaed4',`
`       [2]='#fdc086',`
`       [3]='#ffff99',`
`       [4]='#386cb0',`
`       [5]='#f0027f',`
`       [6]='#bf5b17',`
`       [7]='#666666'`
`   }, dark2 = {`
`       [0]='#1b9e77',`
`       [1]='#d95f02',`
`       [2]='#7570b3',`
`       [3]='#e7298a',`
`       [4]='#66a61e',`
`       [5]='#e6ab02',`
`       [6]='#a6761d',`
`       [7]='#666666'`
`   }, category10 = {`
`       [0]='#1f77b4',`
`       [1]='#ff7f0e',`
`       [2]='#2ca02c',`
`       [3]='#d62728',`
`       [4]='#9467bd',`
`       [5]='#8c564b',`
`       [6]='#e377c2',`
`       [7]='#7f7f7f',`
`       [8]='#bcbd22',`
`       [9]='#17becf'`
`   }, set1 = {`
`       [0]='#e41a1c',`
`       [1]='#377eb8',`
`       [2]='#4daf4a',`
`       [3]='#984ea3',`
`       [4]='#ff7f00',`
`       [5]='#ffff33',`
`       [6]='#a65628',`
`       [7]='#f781bf',`
`       [8]='#999999'`
`   }, tableau10 = {`
`       [0]='#4e79a7',`
`       [1]='#f28e2c',`
`       [2]='#e15759',`
`       [3]='#76b7b2',`
`       [4]='#59a14f',`
`       [5]='#edc949',`
`       [6]='#af7aa1',`
`       [7]='#ff9da7',`
`       [8]='#9c755f',`
`       [9]='#bab0ab',`
`   }, google = {`
`       [0]='#F92',`
`       [1]='#739',`
`       [2]='#2AC',`
`       [3]='#A14',`
`       [4]='#48F',`
`       [5]='#FB2',`
`       [6]='#6B4',`
`       [7]='#754',`
`       [8]='#999',`
`       [9]='#EC4',`
`       [10]='#45A',`
`       [11]='#CD4',`
`   }, category20 = {`
`       [0]='#1f77b4',`
`       [1]='#aec7e8',`
`       [2]='#ff7f0e',`
`       [3]='#ffbb78',`
`       [4]='#2ca02c',`
`       [5]='#98df8a',`
`       [6]='#d62728',`
`       [7]='#ff9896',`
`       [8]='#9467bd',`
`       [9]='#c5b0d5',`
`       [10]='#8c564b',`
`       [11]='#c49c94',`
`       [12]='#e377c2',`
`       [13]='#f7b6d2',`
`       [14]='#7f7f7f',`
`       [15]='#c7c7c7',`
`       [16]='#bcbd22',`
`       [17]='#dbdb8d',`
`       [18]='#17becf',`
`       [19]='#9edae5'`
`   }, category20b = {`
`       [0]='#393b79',`
`       [1]='#5254a3',`
`       [2]='#6b6ecf',`
`       [3]='#9c9ede',`
`       [4]='#637939',`
`       [5]='#8ca252',`
`       [6]='#b5cf6b',`
`       [7]='#cedb9c',`
`       [8]='#8c6d31',`
`       [9]='#bd9e39',`
`       [10]='#e7ba52',`
`       [11]='#e7cb94',`
`       [12]='#843c39',`
`       [13]='#ad494a',`
`       [14]='#d6616b',`
`       [15]='#e7969c',`
`       [16]='#7b4173',`
`       [17]='#a55194',`
`       [18]='#ce6dbd',`
`       [19]='#de9ed6',`
`   }, category20c = {`
`       [0]='#3182bd',`
`       [1]='#6baed6',`
`       [2]='#9ecae1',`
`       [3]='#c6dbef',`
`       [4]='#e6550d',`
`       [5]='#fd8d3c',`
`       [6]='#fdae6b',`
`       [7]='#fdd0a2',`
`       [8]='#31a354',`
`       [9]='#74c476',`
`       [10]='#a1d99b',`
`       [11]='#c7e9c0',`
`       [12]='#756bb1',`
`       [13]='#9e9ac8',`
`       [14]='#bcbddc',`
`       [15]='#dadaeb',`
`       [16]='#636363',`
`       [17]='#969696',`
`       [18]='#bdbdbd',`
`       [19]='#d9d9d9'`
`   }`

}

sequences.dark = sequences.dark2 sequences.category = sequences.category10 sequences.set = sequences.set1 sequences.tableau = sequences.tableau10

local p = {}

function p._list(args)

`   local sequence = sequences[args.sequence] or sequences[args.s] or sequences.category10`
`   `
`   local class1, class2 = `*`,`*
`   if (args.class or '') ~= ''  then`
`       class1 = '`

<div class="' .. args.class .. '">

\\n'

`       class2 = '`

</div>

'

`   end`

`   output, i = {}, 1   `
`   for k, v in pairs(args) do`
`       if tonumber(k) then`
`           output[i] = (args.pre or '* ') .. '<' .. (args.tag or 'span') .. ' style="color:' .. sequence[math.mod( (i-1),(#sequence + 1))] .. ';' .. (args.style or '') .. '">' .. (v or '') .. '</' .. (args.tag or 'span') .. '>'`
`           i = i + 1`
`       end`
`   end`
`   `
`   return class1 .. table.concat( output,(args.sep or '\n') ) .. class2`

end

function p.list(frame)

`   return p._list(frame:getParent().args[1] and frame:getParent().args or frame.args)`

end

return p