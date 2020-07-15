---
title: How to use Overview to analyze social media posts
parent: Case Studies
grand_parent: Overview Help
nav_order: 1
---


# How to use Overview to analyze social media posts

Even when 10,000 people post about the same topic, they’re not saying 10,000 different things. People talking about an event will focus on different aspects of it, or have different reactions, but many people will be saying pretty much the same thing. People posting about a product might be talking about one or another of its features, the price, their experience using it, or how it compares to competitors. Citizens of a city might be concerned about many different things, but which things are the most important? Overview’s document sorting system groups similar posts so you can find these conversations quickly, and figure out how many people are saying what.

This post explains how to use Overview to quickly figure out what the different “conversations” are, how many people are involved in each, and how they overlap.

__Step 1: Get the data into Overview__

Overview does not capture or scrape social media. Fortunately, there are lots of other monitoring tools to do that, such as Radian 6, Sysomos, and Datasift. Overview can read data exported from each of these tools as CSV files. This is a simple file format used by spreadsheet programs, so if you can open it in Excel, you should be able to import it to Overview. Or, you can create your own files in this format.

Then upload the file into overview. Select “Import a New Document Set” as usual, then choose “CSV upload” and select your file. Overview will check the file for errors and show a preview of the file, like this:

If it all looks good, click Upload.

__Step 2: Explore your documents__

Overview reads the full text of each post — not just names and keywords — and groups similar documents together into different folders. Then it takes each folder, and groups similar documents into sub-folders, and so on. The folder tree shows how Overview has organized your posts.

There won’t always be strictly one type of “conversation” per folder, because conversation is a fuzzy concept, and Overview doesn’t know how you want to categorize things. But all the documents in the folder will be the same in some way — or if the folder seems to include too many different types of posts, try exploring the sub-folders, which have narrower topics.

As you select each folder, Overview shows a list of the posts in that folder in the bottom left. Each post is summarized by the most “characteristic” words in that post — not the words that are most common, but the words that make the documents in that folder different from the documents in other folders.

It’s the tags you create that define which conversations you’re interested in. These might be very broad categories such as “positive” and “negative,” or much more specific tags such as “didn’t like the color.” Generally, you’ll explore the documents top-to-bottom and left-to-right, inventing and assigning tags as you go. You can assign tags to one document at a time if you like, but usually you’ll want to assign a tag to all documents in the folder at the same time. To do this, select the folder, then move the mouse over the tag and press the + button.

![addtag](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Screen-Shot-2013-04-17-at-4.53.28-PM.png)

Tags are non-exclusive, meaning that each document can have as many tags as you like.

__Step 3: Export your data__

Now that you’ve seen what’s in your data, and tagged it for future reference, you probably want to use these results in some way. You can see how many documents have each tag just by selecting that tag. Or, you can export your entire document set, including the tags you just added. The export button is on the document set list page. It creates a spreadsheet (CSV file) and gives you a choice how you want your tags.

![tag export](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Screen-Shot-2013-04-17-at-4.58.44-PM.png)

Each document will be one row in the speradsheet. If you put all tags in one column they will be separated by commas, like “Sunshine, Positive.” But putting each tag in its own column makes it easy to do things like find all the documents that have a specific tag, or take column totals to get the number of documents with each tag — useful for making a visualization of your results, like this visualization of 16,000 tweets about drones (created with Overview by Tempero UK):

![16,000 tweets about drones](https://blog.overviewdocs.com/wp-content/uploads/2013/04/Screen-Shot-2013-12-03-at-7.33.58-AM.png)

