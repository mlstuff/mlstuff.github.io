---
layout: post
title: Word Tokenization
date: 2017-04-05 17:57
categories: nlp
---

# Word Tokenization

### Text Normalization

Every NLP task needs to text normalization. This involves 3 steps:

- Segmenting/Tokenizing words
- Normalizing word formats
- Segments sentences from text

### Issues in Tokenization:

- Finland's  _could be_ Finlands / Finland / Findland is
- Lowercase _could be_ lowercase / lower-case / lower case
- San Francisco - One letter or two?
- Ph.d, MD _-_ _wtf_?

We need to decide & fixate on normalizing these issues to achieve a better tokenization.

> Ref: https://www.youtube.com/watch?v=jBk24DI8kg0