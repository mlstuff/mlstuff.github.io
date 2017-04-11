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
    - <sent>I am Sam</sent>
    - <sent>Sam I am</sent>
    - <sent>I do not like green eggs and ham</sent>

    P(I|<sent>)    = count(<sent>,I) / count(<sent>) 
                = occurrence of _I_ followed by _<sent>_ **by** occurrence of _<sent>_ 
                = 2/3
                = 0.67

## Bi-gram probabilities of sentences

- Now we have bi-gram probabilities of words. We can calculate the bi-gram probability of sentence like this:

    P(<sent>I am Sam</sent>) = P(I|<sent>) * P(am|I) * P(Sam|am) * P(</sent>|Sam)


## Practical Issues

- We never keep these probabilities in probability metrics but in a log space.
- Reasons: 
    - We can avoid underflow. Imagine a very large probability with 0 probability.
    - Adding is faster than multiplying. (Since, log(pq) = log(p) + log(q) )

## Public Language modelling toolkits:
    
    - SRILM
    - Google N-gram corpus (Released in 2006). Contains 13m unique words.
    - Google Books N-gram corpus
