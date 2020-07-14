---
title: Overview's search syntax
parent: Organizing Documents
grand_parent: Overview Help
nav_order: 1
---

# Overview's search syntax

![search bar](https://blog.overviewdocs.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-20-at-11.36.50-AM.png)

Overview supports phrase searches, fuzzy searches, and booleans. Here’s what you can search for in the search box and the Multi-Search plugin:

`John Smith`: All documents containing the phrase “John Smith“.  All the words, in order.

`Pizza~`: All documents matching the word “Pizza” or similar words such as “Piazza” or “Pizzas“. (“~” after a single word means fuzzy search. It can find documents that contain typos.)

`John Smith AND Alice Smith`: All documents containing both the phrase “John Smith” and the phrase “Alice Smith“. (“AND” means both phrases must appear.)

`John Smith OR Alice Smith`: All documents containing either the phrase “John Smith” or the phrase “Alice Smith” Or both phrases. (“OR” means any phrase must appear.)

`John Smith AND NOT Alice Smith`: All documents containing the phrase “John Smith” and not the phrase “Alice Smith“. (“NOT” means the phrase must not appear.)

`Alice AND NOT (Bob OR Carol)`: All documents containing the phrase “Alice” and neither the phrase “Bob” nor the phrase “Carol“. (Parentheses help organize complicated queries.)

`"John and Alice Smith"`: All documents containing the phrase “John and Alice Smith“. (Without quotation marks, it would have been interpreted as “(John) AND (Alice Smith)“. Quotation marks tell Overview to ignore operators such as AND, OR and NOT. You can use quotation marks or apostrophes.)

`John Smith~2`: All documents matching the phrase “John Smith” or phrases with the words John and Smith at most 2 words apart, such as “John 'The Culprit' Smith“. (“~N” after a multi-word phrase means proximity search.)
Smith*: All documents containing a word that begins with “Smith“, such as  “Smith“, “Smithy” or “Smithsonian“. (“*” after a phrase means prefix search.)

`title:John Smith`: All documents containing the phrase “John Smith” in their titles. The other way around is `text:John Smith`. By default, Overview searches both the title and the text.

In the coming months, we’ll be sitting with users to see how this new query language works for them. If you have any feedback about a particular query, please use the “Talk to Us” link at the top of Overview.
