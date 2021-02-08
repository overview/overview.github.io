---
title: Importing Files
parent: Overview Help
has_children: true
nav_order: 2
---

# Getting your documents into Overview — the complete guide

The first and most common question from Overview users is _how do I get my documents in?_ The answer varies depending the format of your material. There are three basic paths to get documents into Overview: as multiple files, from a single CSV file, and via DocumentCloud. But there are several other tricks you might need, depending on your situation.

![import options](https://blog.overviewdocs.com/wp-content/uploads/2013/12/Create-a-document-set.png)

## 1. The simple case – a folder full of documents

Overview can directly read many file types, such as PDFs, Word, PowerPoint, RTF, text files, and so on. Choose “Upload document files” and add each document using the file selection dialog box.

If you are using the Chrome browser, you can also select entire folders at once. If you are not using Chrome, you can add all files in a folder in one step by clicking on the first file, then scrolling down and shift+clicking on the last file. Overview will  skip any files that are already uploaded, which makes it easy to sync up your document set with your local files.

Overview will automatically OCR files that are scanned images, though this takes much longer. You may want to split long documents into individual pages. See below for details.

## 2. Upload from the command line

If you have a large number of document files, or you wish to integrate Overview into an automatic pipeline, you can use the command line upload script to get files into Overview, or automatically synchronize a local directory with a document set.

## 3. Documents as data – a CSV file

Overview can read an entire document set as a single CSV file, with one row per document containing the document text and optional information such as URL, tags, and unique ID.  This simple format is documented here. A CSV file is a good choice if you need to bring data in from another application, such as a social media monitoring tool. You also use a CSV file to import tags, which can be used to compare text to data.

## 4. Journalist collaboration – DocumentCloud project import

DocumentCloud is collaborative document hosting service operated exclusively for professional journalists. It supports upload, OCR, search, annotation, publishing of documents, which may be public or private. Overview can import a DocumentCloud project directly, and DocumentCloud’s annotation tools are available directly within the Overview document viewer. This method is a good choice if you have access to DocumentCloud and the document set isn’t too large, up to a few thousand documents.

## 5. Everything is in one huge file — split the pages

Our users often receive their documents as a small number of huge files, thousands of pages each. This is especially common with FOIA requests, or when the source material is a stack of paper. In this case you will want Overview to analyze your material at the page level, not the file level. Overview can split pages automatically when importing files.

Learn more: [Splitting massive documents into pages](/docs/ingest/split-by-page)
