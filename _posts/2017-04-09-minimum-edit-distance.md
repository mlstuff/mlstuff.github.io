---
layout: post
title: Minimum Edit Distance
date: 2017-04-09 00:16
categories: nlp
---
# Minimum Edit Distance

- *Minimum Edit Distance* is a way of solving the problem of string similarity. 
- Few of the major use cases is spell-correction, machine translation, speech recognition, named entity recognition, information extraction etc.

## Definition

-Minimum Edit Distance between two string is the minimum number of editing operations(like _insertion_,_substitution_, _deletion_ & others) required to transform one string into the other.
- For example, transforming a word from _caution_ to _vision_ takes 1 deletion & 3 substitution. Considering cost of each operation is 1, the minimum edit distance between _caution_ and _vision_ would be 4.
- In *levenshtein distance*, substitutions cost 2 while both insertions & deletions cost 1 and therefore, the distance would be 7.

## Finding the Minimum edit distance
*Stages*:
    - Initial State : the word we are transforming.
    - Operators : insert,delete, substitute etc.
    - Goal State : the word we are trying to get to.
    - Path Cost : What we want to minimize: the number of edits 

- Going through all the _n_ letters in each string is very cumbersome. So, we define a distance matrix D(i,j) where
_i_ is first _i_ characters of first string & _j_ is first _j_ characters of second string.


> Ref: https://www.youtube.com/watch?v=CXfJNzD43OI
