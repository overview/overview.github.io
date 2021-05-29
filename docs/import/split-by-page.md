---
title: Splitting massive files into pages
parent: Importing Files
grand_parent: Overview Help
nav_order: 1
---

# Splitting massive files into pages

Our users frequently face a situation where the natural document boundaries are lost. If we’re going to be analyzing 50,000 emails, ideally each email would be stored in its own file. But very often, the source material arrives as a series of massive PDF files, each of which may be thousands of pages long. Or the documents may arrive as a big stack of paper, which becomes a single massive PDF after scanning.

It can be challenging to recover the original document boundaries within a file where everything runs together. For my story on private security contractors in Iraq, I solved this problem with a custom script that tried to detect cover pages. This was a difficult and time-consuming solution.

Fortunately there is an easy trick that works well in most cases: split each long document into pages, and then have Overview sort the large number of pages, not the small number of original documents. Overview can do this automatically when importing from PDF of DocumentCloud, if you tell it that each page counts as a document.

![import options](/wp-content/uploads/2013/04/Split-pages.png)

AP reporter Jack Gillum was the first to suggest this trick, and used it when analyzing 9,000 pages of documents concerning then-Vice Presidential candidate Paul Ryan. In that case, there were many different kinds and lengths of documents within the huge stack of paper he received. Manual splitting was out of the question because it would have been much too time consuming, and there was no easy way to automate the task. Making Overview sort “pages” instead of “documents” was the simple solution, and it worked great.

This might seem counter-intuitive; how could it possibly work to ignore the boundaries of the original documents? But in fact “document” is a somewhat vague term. When we’re looking through a lot of material, we need to chose a “unit of analysis,” and the ideal unit might not be a “document,” especially if the documents are long. For example, we might want to analyze books at the level of chapters, or contracts at the level of paragraphs, or legislation at the level of sections. A “page” may not conform to any such natural division, but it’s a conveniently sized chunk of text to compare to other, similarly sized chunks; if you can imagine that it would be useful to break the source material into pages and then sort the pages by topic, then this splitting trick will work. It’s not perfect, but it’s simple, fast, and works on any type or length of document.
