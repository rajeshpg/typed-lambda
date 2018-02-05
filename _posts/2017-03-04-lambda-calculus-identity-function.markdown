---
layout: post
title: 'Lambda Calculus: Identity function'
date: '2017-03-04 12:00:00'
published: false
tags:
- lambda-calculus
- identity-function
---

In the [previous](/lambda-calculus-lexical-syntax) post we saw the lexical syntax of lambda calculus. From now on we will explore lambda calculus functions starting with Identity function in this post.
### Identity function
A function which returns the argument to which it is applied is an `Identity function`.
`λx.x` is an identity function. If the function is applied to an argument, the function simply returns the argument.

``` 
(λx.x y)

y
```

In the above `function application` the identity function `λx.x` when applied to the argument `y` returns `y`, by replacing the bound variable `x` which is also the body expression.

An identity function is like 0 in addition/subtraction or like 1 in multiplication/division.
It serves its purpose better in Category theory.
