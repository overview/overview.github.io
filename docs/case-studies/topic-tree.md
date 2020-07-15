---
title: Topic tree - Organize documents into folders
parent: Case Studies
grand_parent: Overview Help
nav_order: 2
---


# Topic tree - Organize documents into folders

Before computers, all document-driven stories started with a big stack of paper. Often, the first task was to organize all that paper, by sorting individual documents into piles by type. This gives journalists a high-level idea of “what’s in there” and helps them decide what to read more closely — and just as importantly, what isn’t worth reading.

Today a computer can organize your documents for you. That stack of paper may now be a folder full of PDF files, but it still doesn’t come with any sort of built-in index or obvious categorization system. This is exactly the problem that Overview solves: It splits documents into piles based on their subjects, and then splits each pile into even more specific sub-piles, and so on. The result is a tree of folders.

![overview folders](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Overview-Folders.png)

Above is part of the folder tree that Overview automatically built for the 6,849 documents containing every mention of the city of “Caracas” within the diplomatic cables released by Wikileaks. (Click on the image for a larger version.) Overview labels each folder by the key words in the documents inside. The top folder here has words like PDVSA (the Venezuelan state oil company), “oil”, “billion,” “company” and “production,” so it’s mainly documents concerning the oil industry and other big business. Other top-level folders in this document set (not shown) concern embassy politics, elections, and military operations.

The top-level folder about oil splits into two sub-folders. The one on the left concerns the oil industry specifically, while the one on the right is more about banks and finance. The oil industry folder splits further into regional issues (the Petrocaribe consortium) and documents about PDVSA specifically. Each folder splits into smaller and smaller sub-folders, each of which contains a smaller number of documents on a more specific topic. To let you know when the documents in a folder are getting very specific, Overview tells you when “MOST” or “ALL” of the documents in that folder contain a particular word.

## How a computer understands topics

When I show this to reporters, their first question is always, how does the computer do that? It’s more than curiosity: If you’re going to rely on a computer to organize your documents, you’re asking a machine to help you decide what you should and shouldn’t read. The integrity of the reporting process demands that we understand what our algorithms are doing.

All document categorization algorithms are based on the ability to compare two documents to tell how similar they are. A group of documents which are all very similar to one another belong in the same folder. Computers don’t understand human language, so they need a simple mechanical process which takes two documents as input — literally just the sequence of words that make up the text of each document — and generates a number which is small if the documents are very different, and large if the documents concern the same topic.

Some text analysis systems, such as Open Calais, are based on “named entity recognition,” which extracts people, places, organizations, dates, etc. from the documents. Then, we can say that two documents are similar if they talk about the same entities. This is useful, but such systems will miss important generic words like “oil” and “production.” Instead, Overview examines every word of every document. In a sense, it reads the full text, so you don’t have to.

## Comparing two documents based on their full text

Suppose we have filed an FOIA request for a classified storybook for the children of CIA operatives, and after a long legal battle. The government has given us copies of these three secret documents:

* “The cat sat on the mat. Then the cat chased the rat.”

* “The cat slept all day on the mat.”

* “The rat ran across the floor.”

First, Overview strips capitalization, punctuation, and the grammar words such as “the,” “a,” “on,” etc. These words, also called stop words in natural language processing, aren’t useful for determining the topic of the text, because they appear in almost every document. This leaves us with:

* “cat sat mat cat chased rat”

* “cat slept all day mat”

* “rat ran across floor”

You can see that most of the sense of the document is still there, despite removing lots of words. Then, Overview counts how many times each word appears in each document, producing a word frequency table, like this:

![word frequency table](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Word-frequency-table.png)

This throws out the order of the words, which means the computer can’t understand the difference between “soldiers shot civilians” and “civilians shot soldiers.” This may seem very simplistic, but surprisingly, decades of information retrieval research show that word order usually doesn’t matter when all you want to know is the topic of a document.

Then Overview compares every pair of documents to check how similar they are. It does this by counting the number of words which appear in both documents, but with a twist: If a word appears twice in one document, it’s counted twice. In other words, we multiply the frequencies of corresponding words, then add up the results. This is the final similarity score.

![document similarity scores](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Document-similarity-scores.png)

In this case, the two documents about the cat have a similarity of 3: Cat appears twice in the first document and once in the second, plus rat appears once in each document. The document about the rat has no words in common with the document about the cat sleeping on the mat, so the similarity score is zero.

Documents which are similar enough end up in the same folder, and the folder is labelled by the words which make those documents different from all the others. In this case, the folder is labeled by “cat” and “mat” because those words don’t appear in the remaining document about the rat.

![similar documents](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Similar-documents.png)

And that’s the heart of it. This description omits a number of details for simplicity, but includes all of the things a reporter needs to know:

* Overview uses the full text of each document.

* It is not sensitive to word order.

* Documents with overlapping words are placed in the same folder.

If you’d like to understand the process more deeply, here are a few more details: Overview actually processes text in two word bigrams, not just single words, so it can detect people’s names and other short phrases. Rather than just simple term counts, it weights each word by how rare it is in the document set overall, using a classic formula called TF-IDF. And to generate the folders, given the similarity between every pair of documents, Overview uses k-means clustering, splitting folders recursively at each level of the tree.

## Try it on your own documents

Overview is available for free at overviewproject.org. It can automatically import your projects from the popular DocumentCloud repository, which also handles document upload, OCR, and other tasks. Or, you can upload a CSV file if your text is already in spreadsheet or database format. It also works great on social media data, such as a collection of tweets or blog posts.

You can learn to use Overview by watching a short video on the help page, or viewing the webinar recorded at Poynter’s NewsU.
