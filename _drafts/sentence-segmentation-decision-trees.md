---
layout: post
title: Sentence Segmentation & Decision Trees
date: 2017-04-05 19:24
categories: nlp
---

- Periods like !,? are relatively unambiguous but few like dot(.) are ambiguous which could be a end-of-sentence, abbreviation or decimal point.
- We could build a binary classifier to identify this.
    - Few options we can use are handwritten rules, regular expressions & machine learning algorithms.
- Decisition Tree is the simplest form of it. We could draw a decision tree somethine like this:
    
![You can see this!!?](http://img.ctrlv.in/img/17/04/05/58e4fd15471b7.png)


> Ref: https://www.youtube.com/watch?v=di0N3kXfGYg