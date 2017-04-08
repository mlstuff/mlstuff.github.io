---
layout: post
title: Sentence Segmentation & Decision Trees
date: 2017-04-06 19:24
categories: nlp
---

- Periods like !,? are relatively unambiguous but few like dot(.) are ambiguous which could be a end-of-sentence, abbreviation or decimal point.
- We could build a binary classifier to identify this.
    - Few other options we can use are handwritten rules, regular expressions & machine learning algorithms.
- Decisition Tree is the simplest form of it. We could draw a decision tree somethine like this:
    
![You can see this!!?](/images/sent_segm_dt.png)

- A Decisition tree is just an if-then-else statement.
- The interesting research in a decision tree is choosing the features.
- These features could be exploited by any kind of classifier like Logistic Regression, SVMs etc.


> Ref: https://www.youtube.com/watch?v=di0N3kXfGYg