---
layout: post
title: Computing Minimum Edit Distance
date: 2017-04-09 01:11
categories: nlp
---
# Computing Minimum Edit Distance - D(n,m)

## Using Dynamic Programming

- Consider 2 strings X (length=m), Y (length=n)
- The psuedo-code can be written as:
    
    For each _i_ in _X_:
        For each _j_ in _Y_:
            D(i,j) = min( D(i-1,j) + 1 , D(1,j-1) + 1 , D(i-1,j-1) + 2 )
