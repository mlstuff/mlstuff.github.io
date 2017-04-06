---
layout: post
title: Lemmatization and Stemming
date: 2017-04-05 18:48
categories: nlp
---

# Lemmatization and Stemming

Once the tokenization is done, we have to normalize & stem them.

### Normalization

- This includes keeping the indexed text & query text to have the same form like converting all the text to lowercase.
- As alternative, this could also include asymmetric expansion like matching windows to window.
- Note that, everything you do for normalization has its both good & bad effects. Like, for example, US & us are completely different & must be case-preserved.

### Lemmatization

- Lemmatization is the process of reducing certain words into their base form.
- Like:
    - am, are, is _=>_ be
    - car, car's, cars _=>_ car
- So the _boy's car is red_ becomes _boy car be red_

### Morphology
- *Morphemes*: Morphemes are the smallest _meaningful_ units that make up words.
- Two types:
     - *Stems* : Core meaning-bearing units
     - *Affixes* : Bits & pieces that often adhere to Stems
- For example, in word _cars_, _car_ is the _stem_ and _s_ is _affix_.

### Stemming
- Stemming is the process of chopping of all the _Affixes_.
- For example,
    - Compression => Compress
    - Compressed => Compress
    - Automatic => Automat
- The most common stemming algorithm used is Porter's Algorithm.

> Ref: https://www.youtube.com/watch?v=2s7f8mBwnko

