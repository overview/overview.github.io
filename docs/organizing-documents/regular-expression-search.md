---
title: Regular expression search
parent: Organizing Documents
grand_parent: Overview Help
nav_order: 3
---

# Regular expression search

![search all documents](/wp-content/uploads/2017/08/Screenshot-from-2017-08-08-15-01-36.png)

In addition to being able to search for _words_ Overview also lets you search for _characters_. (Unicode characters, to be precise) including expressions with spaces, digits, punctuation, or unusual characters in them.

Here are some example searches:

`/Smith/`: Search for all documents that contain the five characters: S, m, i, t, h. This will match “The Smithsonian”, because it contains those five characters. It won’t match “wordsmiths”, because there’s no uppercase S. (Searches are offset by slashes, and they’re case-sensitive.)

* `/(?i)Smith/`: Search for all documents that contain the five characters: s, m, i, t, h, either lowercase or uppercase. This will match “wordsmiths.” (`(?i)` enables case-insensitive mode.)

* `/caf[ée]/`: Search for the sequence: c, a, f, and then either e or é. (Beware: Unicode has two ways of representing é, and this expression only searches for one.)

* `/(?m)^-- \nAdam/`: Search for a line starting with two dashes, a space, a newline, and then the letters Adam — someone’s plain-text email signature. (`(?m)` enables scanning for line beginnings and endings; `^` scans for line start; `--` scans punctuation and spaces; `\n` scans for a newline. Don’t bother searching for `\r`: Overview stores all newlines as `\n`. Also, Overview stores all ISO control characters except `\n` and `\t` as spaces.)

* `/path/to/file.txt` isn’t a regular expression: it’s a normal text search. (Regular expressions must end with `/` and can’t contain an inner `/`.)

* `/path\/to\/file\.txt/` matches this filename with the slashes. (Use `\` to escape `/` and `\` inside your regular expressions. You don’t need to double up on backslashes for typical regular-expression features like `\.` (match a period) and `\b` (match a word break).)
 
* `title:/file\.txt/` only searches the document title. (You can search text, title, notes and any other field. By default, Overview scans document text and title.)

* `text:Smith AND text:/Smith/`: Search the index for the word smith, then scan the matching documents for the correct capitalization.

Alas, that last search raises an annoying pitfall. Since regular-expression search doesn’t use an index, it can be slow. When it gets too slow, Overview will stop searching and return an incomplete list of results. (Today, the limit is 2,000 documents.) You’ll see a warning when this happens. The workaround: use a normal search to find all documents that might match the regular expression, then `AND` that search with your regular-expression search. Only the documents matching the normal search will be scanned for your regular expression.

Regular expressions can be tricky to write. Use a regex tester to make sure you’re searching correctly. Our syntax is identical to the Go language’s regex syntax.
