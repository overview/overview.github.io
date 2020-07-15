---
title: Tree - Important and ignored words
parent: Visualizing documents
grand_parent: Overview Help
nav_order: 6
---

# Tree - Important and ignored words

Overview automatically files documents by topic. But you know things that the computer doesn’t, like what’s important for your particular documents. Now you can tell Overview that certain words are important when you import your documents.

This works in combination with the ability to ignore unimportant words. Suppose you’re looking at the White House emails about drilling in the Gulf of Mexico (one of Overview’s example document sets) and you’re specifically interested in environmental topics. You can enter words like “environment” and “environmental” in the important words box, like this:

![important words import option](https://blog.overviewdocs.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-30-at-2.26.14-PM.png)

Here we’ve used the “words to ignore” feature to tell Overview to ignore the names of the two main email writers, because we don’t want to organize emails by who sent them — just their contents. Then we’ve entered “environment” and “environmental” as important words to tell Overview that that’s what we want to look for. Note that we’ve also entered “Environment” and “Environmental” because the important words list is case-sensitive (ignore words are not case sensitive.)

Overview throws out the ignored words, then gives extra weight to any of the important words it finds. Usually it ends up filing all the documents containing important words in their own folder, like this:

![important words](https://blog.overviewdocs.com/wp-content/uploads/2014/01/Screen-Shot-2014-01-30-at-2.27.34-PM.png)

Overview doesn’t put all documents containing the important words into their own folder. If a document contains “environment” but is much more closely related to other documents which do not, it will be filed with them instead. (You can always search to see where Overview has filed documents containing a particular word.)

Also, each important word might or might not get its own folder. Overview doesn’t know “environment” and “environmental” have similar meanings, but it does see that the documents containing these words are similar, so it puts them together.

You can also use Java regular expressions to find important words. For example you can create a folder for each all-uppercase ACRONYM by using the expression [A-Z]+.  Even if you’re not using regular expressions, important words are case-sensitive. (This is to make it easier to find names, which are often capitalized. In the future we’ll add a check box to turn this on or off.)

Taken together, ignored and important words are a powerful way to tell Overview how you want certain documents organized, while letting the computer make automatic decisions for the rest.
