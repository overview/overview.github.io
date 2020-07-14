---
title: Advanced search
parent: Organizing Documents
grand_parent: Overview Help
nav_order: 2
---

# Advanced search: quoted phrases, boolean operators, fuzzy matching, and more

Overview now supports advanced syntax in the search field, like this:

![search field](https://blog.overviewdocs.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-20-at-11.36.50-AM.png)

This gives you an enormous amount of control over finding specific documents.

* To find all documents that do not contain “elephant” search for “-elephant”

* Use AND, OR and NOT to find all documents with a specific combination of words or phrases.

* Use quotes to search for multiple word phrases like “disaster recovery” or “nacho cheese”.

* Use ~ after any word to do a fuzzy search, like “Smith~”. This will match all words with up to two characters added, deleted, or changed. Great for searching through material with OCR errors.

* By default, multiple words are now ANDed together if you don’t specify anything else.

* Use “title:foo” to search for all documents with the word “foo” in the title (the title is the upload filename, or the contents of the title column if you imported from CSV)

* You can use wildcards like * and ? or even full regular expressions using the syntax text:/regex/ or title:/regex/. Note that regular expressions cannot have spaces in them, because you are actually searching through the index of words used in the documents, not the original text.

There are actually many more things you can do with this powerful search tool. See the ElasticSearch advanced query syntax for details.
