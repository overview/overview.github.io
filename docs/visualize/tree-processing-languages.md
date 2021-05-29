---
title: Tree - Processing multiple languages
parent: Visualizing documents
grand_parent: Overview Help
nav_order: 7
---


# Tree - Processing multiple languages

Overview supports several different languages, but you can only pick one language per document set. Fortunately, there is an easy workaround to analyze a document set that contains several different languages.

The trick is to paste a stop words list into the “words to ignore” box. Stop words are the short, common, grammatical words in a language such as “a” and “for” in English, or “un” and “soy” in Spanish. Overview automatically ignores the stop words from whatever language you tell it to use. This is necessary, otherwise you would always get a folder labelled “MOST: the” when processing English documents. Overview only removes stop words form one language at a time, but you can get exactly the same effect by pasting in stop words for other languages.

This trick can also be used to process documents in a language that Overview doesn’t officially support yet!

Suppose you have a document set containing English and French text. You can tell Overview that the documents are in English, then paste in a French stop words list in the “words to ignore” box. Separate the words with spaces or put them on different lines. The result should look like this:

![multiple languages stopwords](/wp-content/uploads/2013/11/Screen-Shot-2013-11-04-at-12.41.45-PM.png)

This isn’t a perfect technique, because some stop words in one language can be legitimate words in another language, but it will get you 95% of the way there. Most importantly, it will allow you to use Overview on multi-language documents right now, before we develop a more integrated solution. As noted above, you can also process documents in any language, not just the ones Overview supports.
