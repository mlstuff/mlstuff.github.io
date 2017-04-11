---
layout: post
title: Estimating N-gram probabilities
date: 2017-04-11 20:39
categories: nlp
---

# Estimating n-gram probabilities

Let's start by estimating bi-gram probabilities

## Estimating bi-gram probabilities

- Bi-gram probability can be calculated using:
    
        P(wi|wi-1) = count(wi-1, wi) / count(wi-1)

- This simply means, Of all the times we saw _wi-1_, how many times _wi-1_ & _wi_ occur together.

- For example, consider the sentences,
    - <s>I am Sam</s>
    - <s>Sam I am</s>
    - <s>I do not like green eggs and ham</s>

    P(I|<s>)    = count(<s>,I) / count(<s>) 
                = occurrence of _I_ followed by _<s>_ **by** occurrence of _<s>_ 
                = 2/3
                = 0.67

## Bi-gram probabilities of sentences

- Now we have bi-gram probabilities of words. We can calculate the bi-gram probability of sentence like this:

    P(<s>I am Sam</s>) = P(I|<s>) * P(am|I) * P(Sam|am) * P(</s>|Sam)


## Practical Issues

- We never keep these probabilities in probability metrics but in a log space.
- Reasons: 
    - We can avoid underflow. Imagine a very large probability with 0 probability.
    - Adding is faster than multiplying. (Since, log(pq) = log(p) + log(q) )

## Public Language modelling toolkits:
    
    - SRILM
    - Google N-gram corpus (Released in 2006). Contains 13m unique words.
    - Google Books N-gram corpus
