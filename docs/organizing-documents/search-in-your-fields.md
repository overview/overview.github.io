---
title: Search in your fields
parent: Organizing Documents
grand_parent: Overview Help
nav_order: 5
---

# Search in your fields

If you’ve added metadata fields to your documents, rejoice: now you can search them!

I’ll set metadata on two documents for a quick demonstration:

![I've set metadata on this document....](https://blog.overviewdocs.com/wp-content/uploads/2017/06/Screenshot-from-2017-06-14-13-11-41.png)

I've set metadata on this document....

![I… And then I set metadata on this second document….](https://blog.overviewdocs.com/wp-content/uploads/2017/06/Screenshot-from-2017-06-14-13-12-49.png)

… And then I set metadata on this second document….

Now, I can search these new fields by prepending [Field Name]: to the search:

![Search can now include custom fields](https://blog.overviewdocs.com/wp-content/uploads/2017/06/Screenshot-from-2017-06-14-13-13-35.png)

Search can now include custom fields

Here are the subtle rules. Consider them an addendum to our previous search syntax blog post:

* `Date:2015-11-08` will match all documents containing the phrase “2015-11-08” in the “Date” field (assuming you created a “Date” field).

* `date:2015-11-08` will not match any documents in this example. (Field names are case-sensitive.)
"Full Name":John Smith lets you specify a field name with spaces. (Field names with spaces or parentheses must be quoted.)

* `Author:Adam H*` will search for any phrase starting with “Adam H” in the “Author” field. (All usual search syntax works on metadata fields.)

* Be wary when your field names clash with Overview’s built-in names. `text:Overview` and `title:Overview` continue to search the actual documents’ texts and titles, not any “text” or “title” metadata fields you may have added. If you have a metadata field named “text“, you can force a metadata search by quoting the field name: for instance, `"text":Overview`.

* We search all metadata the same way we search document text: we ignore punctuation, and don’t support number or date comparisons  (e.g. “search for all documents with a Date within the past year”.)
