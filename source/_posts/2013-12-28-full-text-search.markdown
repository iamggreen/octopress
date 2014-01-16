---
layout: post
title: "Full Text Search"
date: 2013-12-28 00:00:00 -0600
comments: true
categories: 
---

Since I have never had a project that requires full text document search I haven't thought much about how it's done.  After reading an assignment from the MIT OpenCourseware course Software Engineering for Web Applications  I think I have a much better understanding of how it is done and from the reading this would be how I would approach it.

Let's take for example a database of movies.

**To insert a movie into our database:**

1.  Remove stopwords.  These are all words that occur too often to be useful as a search word.  Examples are: "a", "and", "as", "at", "for", "or", "the", etc.  When building a full-text search for a particular domain I believe there may be additional domain-specific stopwords as well.

2.  Normalize words.  When a user searches for the word "worried", we should probably include the words "worries", "worry".  So we would normalize that to "worry".

3.  Normalize synonyms.  This is probably optional since it is harder to determine what context a word is used in.  If we used the word "like" as an adjective then we could also search for the words "alike", "comparable", etc..  But if it's a verb similar words would be "enjoy" or "admire".

4. Store each word along with its frequency in a database

**To query a movie from our database:**

1.  Do the same steps 1-3 that we did when we inserted the movie into our database.  Remove stopwords, normalize words and normalize synonyms.

2. Perform the query of the database.  Find the entries and sort by those with the greatest number of word matches followed by the words used most frequently.

Now this is just a very basic full-text search.  I can think of some optimizations to be made.

1.  Dynamically determine stopwords.  Prior to rebuilding the search database analysis could be done beforehand to determine stopwords instead of having a static list of words.  So if i built a database to search words for a computer sales website I may find that the word "computer" shows up in 90% of the documents so I might add that as a stopword since it's not helpful.

2. Tune the rankings.  Give certain matches different weights based on meeting different criteria.  Matching all words, matching words in order, matching words before normalizing, word frequency.  We could tune our search result rankings by changing how much those criteria matter and determine if that gives us better search results.

References

MIT OpenCourseware - Software Engineering for Web Applications - [Search Assignment](http://philip.greenspun.com/seia/search)

MIT OpenCourseware - [Software Engineering for Web Applications](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-171-software-engineering-for-web-applications-fall-2003/index.htm)