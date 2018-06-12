---
layout: post
title: 'Lambda Calculus: Lexical syntax'
featured: true
published: true
date: '2017-02-08 12:02:35'
tags:
- lambda-calculus
---

Lambda Calculus was invented by Alonzo Church as a formal system to model computations using functions to define abstractions and applications. It is the most simplest programming language. 

### Lexical Syntax:
#### Symbols or keywords:  
Lambda Calculus reserves very few symbols for use.  
The Greek letter `λ` has become the unofficial keyword to represent start of a function.  
A dot `.` is used to separate function parameter and function body.  
Paratheses `()` is optionally used to group function application.

#### Identifiers:
In Lambda Calculus, unlike other programming languages, any sequence of non-blank characters can be used as identifiers.

#### Lambda Expressions:
A `λ expression` may be a name to identify an abstraction point, a function to introduce an abstraction or a function application to specialize an abstraction.  
``` 
<expression> ::= <name> | <function> | <application> 
```  
A `name` may be any sequence of non-blank characters.  
`example: "lambda", "calculus", "10", "15", "+", "-->"`  
##### Function:
A `λ function` is an abstraction over a `λ expression`.  
``` 
<function> ::= λ<name>.<body>
```  
`example: λx.x`  
The above `λ expression` is a function abstraction(or simply a function) generally knows as an `identity` function which returns the parameter passed to the function.    
The `x` after the `λ` represents the name of the parameter used in the function abstraction.
The `.` after name `x` separates it from the expression `x` which is called function's body.

The `<body>` can be a `λ expression` including another function or `function application`.
``` 
<body> ::= <expression>
```
for example `λx.λy.x` is a function where `λy.x` is the function body which is another function.

###### Bound variable:  
A function's name is also called as the function's `bound variable` and it is like a parameter in a function.

##### Function Application:
A `function application` has the following syntax:
``` 
<application> ::= (<function expression> <argument expression>)
```
where
``` 
<function expression> ::= <expression>

<argument expression> ::= <expression>
```
`example: (λx.x λa.λb.b)`

In a function application the function expression(or function abstraction) is _applied_ to the argument expression.  

There are two approaches to evaluate a function application, `applicative order` and `normal order`

In `applicative order` all occurrences of the function expression's bound variable is replaced by the value of the argument expression.

In `normal order` all occurrences of the function expression's bound variable is replaced by unevaluated argument expression.

we will see more about functions and function applications in the next post
