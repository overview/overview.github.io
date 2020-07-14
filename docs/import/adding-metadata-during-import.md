---
title: Adding metadata fields during import
parent: Importing Files
grand_parent: Overview Help
nav_order: 6
---

# Import, edit, and create document metadata

Have you ever needed to extract the author or write notes for each document? Now you can, with fields.

The new “Fields” section sits in wait underneath each document. Click it, and you’ll be able to create fields and change their values.

![metadata filled in](https://blog.overviewdocs.com/wp-content/uploads/2015/07/metadata-filled-in.png)

The list of fields is the same for every document in a document set. Each document has its own field values.

You can create new fields directly in Overview, or import them as extra columns in your CSV (see: importing documents using a CSV file.)

All your fields will appear as new columns when you export a spreadsheet:

![metadata-output-csv](https://blog.overviewdocs.com/wp-content/uploads/2015/07/metadata-output-csv.png)

You can use a spreadsheet program to filter for field values.
The “fields” feature is new. We know there’s plenty of pizzazz to add:

* Right now, we only support single-line text fields: no dates, numbers, geo-coordinates, or so forth. As a workaround, format your text values carefully (e.g., use YYYY-MM-DD for dates) so your spreadsheet program can grok them.
* Overview’s search feature doesn’t examine field values.
* You cannot create fields or write to fields using the API. (You can read field values with the API, though: they’re in document.metadata.)
* You can only set metadata on one document at a time.

