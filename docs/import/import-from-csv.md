---
title: Importing documents from a CSV file
parent: Importing Files
grand_parent: Overview Help
nav_order: 3
---

# Importing documents from a CSV file

There are different ways to get your documents into Overview. This post is about loading documents into Overview using the file CSV file format, and the format that Overview expects.

## The quick answer
Overview expects all documents in a single CSV file, one document per row, plus a header row. Overview can read the following columns:

* text — this is the only required column, and must contain the document text.
* title — This is displayed when viewing the document. Documents are sorted by title in the document list.
* url — If the URL begins with https Overview will display the page when viewing the document. Otherwise Overview will display the plain text and a source link.
* id — ignored by Overview, but saved when the document set is exported, so you can match against other tables.
* tags — a comma-separated list of tags applied to each document. Great for comparing text to data.

Every other column will appear as editable document metadata.
The “text” column must exist. (It may also be named “snippet” or “contents” for compatibility with files exported by Radian 6 and Sysomos). All other columns are optional.

Need more details? Read on.

## Creating a CSV file
Many programs can save a CSV file.  For example, Excel can save a spreadsheet as a CSV file. Be sure to include the column names in the first row. You can also export a CSV file from a MySQL database.

Overview can probably read just about any CSV file created with any program, if you can ensure that the header is right. You may need to rename existing columns to the names that Overview expects, or you may need to add the header row entirely because some programs do not write a header. To do this, edit the CSV file with any text editor such as Notepad or TextEdit — but not Microsoft Word, as you will probably break the CSV file if you try to edit it in a word processor.

## What a CSV file for Overview should look like
A CSV file is simply a list of “comma-separated values,” organized into rows and columns, like a spreadsheet or a table. The file starts with a list of the column names, separated by commas. This is followed by each row of data, one row per line, with the values for each column again separated by commas. Overview only requires one column, which much be named “text.” Here is an example file:

```
text
This is the content of the first document.
And here is the text of document the second
Document three talks about quick brown foxes.
⋮
```

If the text of a document spans multiple lines, or itself contains commas, then it needs to be quoted. Quotes inside a quoted document must be “escaped” by turning them into double quotes. This is all standard CSV stuff, and any program or library that writes CSVs should do it automatically.

```text
"This document is really long and crosses multiple lines and contains
commas, which is why it is quoted."
"This is the second document. I'd like to say ""Hi!"" to everyone
to show how to put quotes inside a quoted document. The text of
this document can cross as many lines as needed, or even contain
blank lines like this:

The second document ends with this final quote."
The third document fits all on one line so no quotes needed.
"The fourth document has a comma in it, so it's quoted too."
⋮
```

Overview will display the text in the viewer pane when you click on each document. If you want to display something else for the document, you can add a “url” column which tells Overview to load a particular web page when you view that document. For security reasons, this must be an https URL. Here’s an example using tweets:

```text,url
New deploy today -- cleaner clustering, better handling of larger document sets. Anyone got a pile of PDFs they want to look at? Try it!,https://twitter.com/overviewproject/status/281075194557259777
"""“I’m not going to sit out on the newsroom floor and sort pages into stacks of documents"" ~@jackgillum on need for document mining software.",https://twitter.com/overviewproject/status/264450385928929280
⋮
```

There are three more columns that Overview can read. You can add a “title” to each document, which Overview displays in the document list. Documents are sorted by title, so this is a way to control the order that documents are listed.  You can add a unique ID column, simply named “id”, which Overview will read and associate with the document, and export with the document set. And you can add a comma separated list of “tags” if you want to import documents with tags already applied, or want to compare text to data.

The columns can be in any order; all that matters is that the order of the column names matches the order of the data.

Every other column will appear as editable document metadata. When Overview exports a document set, it writes out id, text, title, url, and tags fields, as well as any other fields you imported, or created within Overview.

## Uploading your CSV file to Overview

First, select the upload option from the document set list page:

![create a document set](/wp-content/uploads/2014/05/Upload-methods.png)

Then choose a file. Overview will show a preview and do some basic checks to ensure that the format is OK. It should look like this:

![upload a csv file](/wp-content/uploads/2014/05/Upload-CSV.png)

After these checks you will see the usual import options, then a preview of the file contents. You may need tell Overview what character encoding the file uses. Try changing this if you see funny square characters in the preview, or accents aren’t displaying right. Then hit upload, and away we go.
