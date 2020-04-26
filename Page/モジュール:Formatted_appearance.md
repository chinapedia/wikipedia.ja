> この記事は[モジュール:Formatted appearance](https://ja.wikipedia.org/wiki/モジュール:Formatted_appearance)から翻訳されています。


\-- This module requires the use of Module:List. local list = require('Module:List')

local p = {}

\-- Local function which is used to get a correctly formatted entry. -- Function checks if the array had a value added by checking the counter, -- and returns the relevant result. local function getFormattedEntry(args, counter)

`   if (counter == 1) then                                                                              -- Check if the counter stayed the same.`
`       return ""                                                                                       -- Nothing was added to array; Return empty string.`
`   elseif (counter == 2) then                                                                          -- Check if only one value was added to the array.`
`       return args[1]                                                                                  -- Only one value was added to array; Return that value.`
`   else                                                                                                -- The array had more than one value added.`
`       return list.makeList("unbulleted", args)                                                        -- Call list.makeList() to retrieve the formatted plainlist.`
`   end`

end

\--[Local function which is used to format an appearance for a comic book, in the style of: Line 1: \<comic book title\> \#\<issue number\> (with comic book title in italics) Line 2: \<release date\> For other usages, see createGenericEntry(). The function works with the following combinations: -- Only comic book title (example: "The Incredible Hulk"). -- Title and issue number (example: "The Incredible Hulk" and "181"). -- Title and release date (example: "The Incredible Hulk and "November 1974"). -- Title, issue number and release date (example: "The Incredible Hulk", "181" and "November 1974"). -- Only release date (example: "November 1974"). --](https://ja.wikipedia.org/wiki/Local_function_which_is_used_to_format_an_appearance_for_a_comic_book,_in_the_style_of:_Line_1:_\<comic_book_title\>_#\<issue_number\>_\(with_comic_book_title_in_italics\)_Line_2:_\<release_date\>_For_other_usages,_see_createGenericEntry\(\)._The_function_works_with_the_following_combinations:_--_Only_comic_book_title_\(example:_"The_Incredible_Hulk"\)._--_Title_and_issue_number_\(example:_"The_Incredible_Hulk"_and_"181"\)._--_Title_and_release_date_\(example:_"The_Incredible_Hulk_and_"November_1974"\)._--_Title,_issue_number_and_release_date_\(example:_"The_Incredible_Hulk",_"181"_and_"November_1974"\)._--_Only_release_date_\(example:_"November_1974"\)._-- "wikilink") local function createComicEntry(appearanceMajor, appearanceMinor, appearanceDate)

`   local fullString = {}                                                                               -- Variable to save the array.`
`   local counter = 1                                                                                   -- Variable to save the array counter.`
`   `
`   if (appearanceMajor ~= nil) then                                                                    -- Check if a comic book title was entered.`

`       if (appearanceMinor == nil) then                                                                -- A comic book title was entered; Check if a issue number was entered.`
`           fullString[counter] = appearanceMajor                                                       -- A issue was not entered; Add only the comic book title to the array.`
`           counter = counter + 1                                                                       -- Increment counter by one.`
`       else `
`           fullString[counter] = appearanceMajor .. " " .. appearanceMinor                             -- A issue was entered; Add both to the array.`
`           counter = counter + 1                                                                       -- Increment counter by one.`
`       end`
`   end`
`   `
`   if (appearanceDate ~= nil) then                                                                     -- Check if a release date was entered.`
`       fullString[counter] = appearanceDate                                                            -- A release date was entered; Add it to the array.`
`       counter = counter + 1                                                                           -- Increment counter by one.`
`   end`

`   return getFormattedEntry(fullString, counter)                                                       -- Call getFormattedEntry() to get a correctly formatted entry.`

end

\--[Local function which is used to format an appearance for most usages, including television, film, books, songs and games, in the style of: Line 1: \<minor work title\> (in quotes) (Minor works include: TV episodes, chapters, songs and game missions) Line 2: \<major work title\> (in italics) (Major works include: TV series, films, books, albums and games) Line 3: \<release date\> For comic book usages, see createComicEntry(). The function works with the following combinations: -- Only minor work title (example: "Live Together, Die Alone"). -- Minor work title and major work title (example: "Live Together, Die Alone" and "Lost"). -- Minor work title and release date (example: "Live Together, Die Alone" and "May 24, 2006"). -- Minor work title, major work title and release date (example: "Live Together, Die Alone", "Lost" and "May 24, 2006"). -- Only major work title (example: "Lost"). -- major work title and release date (example: "Lost" and "May 24, 2006"). -- Only release date (example: "May 24, 2006"). --](https://ja.wikipedia.org/wiki/Local_function_which_is_used_to_format_an_appearance_for_most_usages,_including_television,_film,_books,_songs_and_games,_in_the_style_of:_Line_1:_\<minor_work_title\>_\(in_quotes\)_\(Minor_works_include:_TV_episodes,_chapters,_songs_and_game_missions\)_Line_2:_\<major_work_title\>_\(in_italics\)_\(Major_works_include:_TV_series,_films,_books,_albums_and_games\)_Line_3:_\<release_date\>_For_comic_book_usages,_see_createComicEntry\(\)._The_function_works_with_the_following_combinations:_--_Only_minor_work_title_\(example:_"Live_Together,_Die_Alone"\)._--_Minor_work_title_and_major_work_title_\(example:_"Live_Together,_Die_Alone"_and_"Lost"\)._--_Minor_work_title_and_release_date_\(example:_"Live_Together,_Die_Alone"_and_"May_24,_2006"\)._--_Minor_work_title,_major_work_title_and_release_date_\(example:_"Live_Together,_Die_Alone",_"Lost"_and_"May_24,_2006"\)._--_Only_major_work_title_\(example:_"Lost"\)._--_major_work_title_and_release_date_\(example:_"Lost"_and_"May_24,_2006"\)._--_Only_release_date_\(example:_"May_24,_2006"\)._-- "wikilink") local function createGenericEntry(appearanceMajor, appearanceMinor, appearanceDate)

`   local fullString = {}                                                                               -- Variable to save the array.`
`   local counter = 1                                                                                   -- Variable to save the array counter.`
`   `
`   if (appearanceMinor ~= nil) then                                                                    -- Check if a minor appearance was entered.`
`       fullString[counter] = appearanceMinor                                                           -- A minor appearance was entered; Add it to the array.`
`       counter = counter + 1                                                                           -- Increment counter by one.`
`   end`
`   `
`   if (appearanceMajor ~= nil) then                                                                    -- Check if a major appearance was entered.`
`       fullString[counter] = appearanceMajor                                                           -- A major appearance was entered; Add it to the array.`
`       counter = counter + 1                                                                           -- Increment counter by one.`
`   end`
`   `
`   if (appearanceDate ~= nil) then                                                                     -- Check if a release date was entered.`
`       fullString[counter] = appearanceDate                                                            -- A release date was entered; Add it to the array.`
`       counter = counter + 1                                                                           -- Increment counter by one.`
`   end`

`   return getFormattedEntry(fullString, counter)                                                       -- Call getFormattedEntry() to get a correctly formatted entry.`

end

\-- Local function which is used to format with a hash symbol comic book issues. -- For other minor works, see getFormattedGenericMinorWork(). local function getFormattedComicMinorWorkTitle(issue)

`   if (issue ~= nil) then                                                                              -- Check if the issue is not nil.`
`       if (string.find(issue, "#")) then                                                               -- Check if the issue already has a hash symbol.`
`           return issue                                                                                -- Hash symbol already present; Return issue.`
`       else`
`           local formattedString = string.gsub(issue, "%d+", "#%1")                                    -- Hash symbol not found; Add the symbol before the issue number.`
`           return formattedString                                                                      -- Return issue.`
`       end`
`   else`
`       return nil                                                                                      -- issue is nil; Return nil.`
`   end`

end

\-- Local function which is used to format with quotes a minor work title of most types. -- For comic book issues, see getFormattedComicMinorWork() (see \[MOS:MINORWORK\]). local function getFormattedGenericMinorWorkTitle(title)

`   if (title ~= nil) then                                                                              -- Check if the title is not nil.`
`       return "\"" .. title .. "\""                                                                    -- Title is not nil; Add quotes to the title.`
`   else`
`       return nil                                                                                      -- Title is nil; Return nil.`
`   end`

end

\-- Local function which is used to format with italics a major work title (see \[MOS:MAJORWORK\]). local function getFormattedMajorWorkTitle(title)

`   if (title ~= nil) then                                                                              -- Check if the title is not nil.`
`       return "`*`"``   ``..``   ``title``   ``..``   ``"`*`"                                                                    -- Title is not nil; Add italics to the title.`
`   else`
`       return nil                                                                                      -- Title is nil; Return nil.`
`   end`

end

\-- Local function which does the actual main process. local function _getFormattedAppearance(args)

`   local appearanceMajor = args['major_work']                                                          -- Get the title of the major work.`
`   local appearanceMinor = args['minor_work']                                                          -- Get the title of the minor work.`
`   `
`   local isComic = false                                                                               -- Variable to save the status of wether the appearence is from a comic book.`
`   if (args['issue'] ~= nil) then                                                                      -- Check if the comic specific issue is not nil.                    `
`       appearanceMinor = args['issue']                                                                 -- Issue is not nil; Get the issue number.`
`       isComic = true                                                                                  -- Set isComic to true.`
`   end`
`   `
`   local appearanceDate = args['date']                                                                 -- Get the release date of the minor work.`
`   `
`   local formattedAppearanceMajor = getFormattedMajorWorkTitle(appearanceMajor)                        -- Call getFormattedMajorWorkTitle() to get a formatted major work title.`

`   if (isComic == false) then                                                                          -- Check if the appearance is a comic book appearance.`
`                                                                                                       -- The appearance is not a comic book appearance; `
`       local formattedAppearanceMinor = getFormattedGenericMinorWorkTitle(appearanceMinor)             -- Call getFormattedGenericMinorWorkTitle() to get a formatted minor work title.`
`       return createGenericEntry(formattedAppearanceMajor, formattedAppearanceMinor, appearanceDate)   -- Call createGenericEntry() to create an appearance entry.`
`   else`
`                                                                                                       -- The appearance is a comic book appearance. `
`       local formattedAppearanceMinor = getFormattedComicMinorWorkTitle(appearanceMinor)               -- Call getFormattedComicMinorWorkTitle() to get a formatted minor work title.`
`       return createComicEntry(formattedAppearanceMajor, formattedAppearanceMinor, appearanceDate)     -- Call createComicEntry() to create a comic book appearance entry.`
`   end`

end

\--\[\[ Public function which is used to format the |first_appeared= and |last_appeared= fields. The usage of this module allows for correct title formatting (see \[MOS:MAJORWORK\] and \[MOS:MINORWORK\]), and correct line breaks based on guidelines (see \[WP:UBLIST\]).

Parameters:

`   -- |major_work=     — optional; The title of the major work the fictional element appeared in.`
`                                       Major works include TV series, films, books, albums and games.`
`   -- |minor_work=     — optional; The title of the minor work the fictional element appeared in.`
`                                       Minor works include TV episodes, chapters, songs and game missions.`
`   -- |issue=          — optional; The number of the comic book issue the fictional element appeared in.`
`   -- |date=           — optional; The date of the publication/release of the minor work where the fictional element appeared in.`

\--\]\] function p.getFormattedAppearance(frame)

`   local getArgs = require('Module:Arguments').getArgs                                                 -- Use Module:Arguments to access module arguments.`
`   local args = getArgs(frame)                                                                         -- Get the arguments sent via the template.`

`   return _getFormattedAppearance(args)                                                                -- Call _getFormattedAppearance() to perform the actual process.`

end

return p