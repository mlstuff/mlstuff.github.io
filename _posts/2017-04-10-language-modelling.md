---
layout: post
title: Language Modelling
date: 2017-04-10 20:08
categories: nlp
---

# Language Modelling

- The goal of language modelling is to assign a probability to a sentence (sequence of words)
    
    `P(W) = P(w1,w2,w3...wn)`.
- This model of calculating the probabilty of whole sentence, P(W) or conditional probability P(wn|w1,w2..wn) is called *Language Modelling*. 
- Language model (LM) tells us how good a group of words fit together.

# Computing the Probability

- It is computed based on chain rule.
    
        => P(A|B) = P(A,B)/P(B)
        => P(A,B) = A(A|B).P(B)

- For more variables,
        
        P(x1,x2...xn) = P(x1).P(x2|x1).P(x3|x1,x2)...P(xn|x1,x2...xn-1)

# Estimate these probabilites

- Could we just count & divide?  Like:

        P(w1|w2..wn) = Count(w1...wn) / Count(w2..wn)

- No! _Reason_: Too many sentences to calculate.

# Markov Assumption

- Markov Assumption suggests that the probability of a word given all words in sequence can be calculate just by computing the probabilty of the word given the last word (or last few words) in the sequence.

        i.e., P(w1|w2...wn) = P(w1|wi..wn) 
        where i could be a small number like 1 for unigram, 2 for bigram and so on..

## Unigram

- The simplest case is taking the product of probabilities of individual words. This model is called Unigram.
    
        P(w1w2w3...wn) = P(w1).P(w2)....P(wn)

- Words are completely independent in this model.


## Bigram

- Bigram is a slightly intelligent model where we condition on single previous word.
    
        P(wi | w1,w2...wn) = P(wi | wi-1)

- These can be extended to trigram, 4-grams, 5-grams ... n-gram model.

- Clearly, n-gram models are clearly not going to help because to get everything correct you need a very-big-gram model which is very hard on computation. But, in practice, these models are proven to show good results.

