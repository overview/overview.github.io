---
title: Exporting to Microsoft Excel
parent: Exporting
grand_parent: Overview Help
nav_order: 1
---

# Exporting to Microsoft Excel

Overview has long had a fairly important (if little-used) feature: it can export all documents into a spreadsheet. Day one, we wrote the spreadsheet in “comma-separated values” (“CSV”) format.

Then we realized that Microsoft Excel couldn’t open all CSV files.

Day two, we implemented a separate export file type, just for Microsoft Excel. Here are the differences.


## We truncate document text

One of the columns in our exported spreadsheet contains the entire text of each document. Microsoft Excel limits cell size to 32,767 characters. If Excel encounters a document with more than 32,767 characters of text, it stops importing. (We’ve found that most documents in Overview are far shorter than 32,767 characters. For a sense of scale: The Adventures of Huckleberry Finn is 610,000 characters; its average chapter is about 14,000 characters.)

When you choose Excel format, Overview truncates the text of very-long documents.

## We avoid Excel for Mac file-encoding issues

We spent ages debugging this issue, because we had to quell our disbelief. It turns out the “Encoding” option in Excel for Mac 2011’s CSV-import dialog doesn’t do anything. If you import an Overview CSV into Microsoft Excel for Mac 2011, Excel will garble those special characters. The same holds for virtually any CSV on the Internet that has special characters such as “smart quotes”. (Techno-lingo: Excel for Mac does not decode UTF-8, even though it presents the choice to decode UTF-8.)

We don’t know whether Microsoft solved this issue in Excel for Mac 2016.

Overview doesn’t do anything special to overcome this problem: it’s only a bug with the CSV-import feature. We recommend you avoid importing any CSVs into Microsoft Excel for Mac 2011 unless you’re certain they aren’t encoded in UTF-8. (UTF-8 is the most common encoding on the Internet.)

## The take-away

If you use Microsoft Excel, pick Excel format when you export from Overview. Overview will give you a file that’s as close to the original data as possible, and Excel will be able to open that file.

If you use a different spreadsheet program, pick CSV format for an _exact_ copy of the data within Overview.
