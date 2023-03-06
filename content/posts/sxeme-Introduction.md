---
author: snowmang1
title: Sxeme Introduction
date: 2023-01-15T14:00:45-05:00
description: Introduction to Scheme compiler project
tags:
    - Scheme
    - Compiler
series:
    - sxeme
aliases:
    - sxeme-intro
math: true
draft: false
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css" integrity="sha384-vKruj+a13U8yHIkAyGgK1J3ArTLzrFGBbBc0tDp4ad/EyewESeXE/Iv67Aj8gKZ0" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js" integrity="sha384-PwRUT/YqbnEjkZO0zZxNqcxACrXe+j766U2amXcgMg5457rve2Y7I6ZJSm2A0mS4" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>

<!-----------------------Body----------------------->

## My <cite>Scheme[^1]</cite> compiler.

<div style="text-align: center"> 
    <!-- overview of project -->
    <p>
<<<<<<< HEAD
    To give an overview Scheme is a Lisp derivative functional language with an emphasis on simplistic syntax.
=======
    To give an overview, Scheme is a Lisp derivative functional language with an emphesis on simplistic syntax.
>>>>>>> origin/trunk
    I chose this language b/c of its power and simplicity. Scheme uses a delimiter surrounded prefix notation
    for function execution which makes it incredibly compact (if that is the goal), or explicit & easy to read.
    Scheme has a small token table making it easier to make a parser for it. The difficulty I see with making a
    Scheme compiler is the IR, getting from syntax to semantics is difficult in high level language.
    </p>
    <!-- compiler structure -->
    <p>
<<<<<<< HEAD
    I am using a common compiler implantation scanner -> parser -> IR(LLVM IR) -> binary. My focus on this project will
    be Rust-like *Errors*. The Errors given by this compiler will in theory give critical debug info
    such as: _line #_, _error msg_, _column #_, _correct implementation_
=======
    This will be a standard compiler implantation scanner -> parser -> IR -> LLVM. My focus on this project will
    be Rust-like *Errors*. The Errors given by this compiler take inspiration
    from Rust, they will in theory give critical debug info such as: line #, error msg, column #, example
>>>>>>> origin/trunk
    of correct code. The speed will come from my IR implementations. Paired with LLVMs natural speed,
    performance should not be an issue.
    </p>
    <!-- general info -->
    <p>
    I will be using GitHub to host and orchestrate work. I am using this project to learn modern compiler techniques & LLVM. I will be
    posting regularly on progress updates along with full descriptions of the inter workings.
    </p>
</div>

#### Tech stack
- (safe) Rust
- LLVM

## Main Focus
Currently the main focus of this project will be *Error* messages. However this is subject to change.

In Theory the error terminal output will look like this:

{{< highlight bash >}}
unidentified function 'defin'
Line with Error [10:6]: (defin name)
                              |
possible correct: (define name)
{{< /highlight >}}

## Time Table
I plan to make small but complete projects throughout. For example first create a math centric scheme sub-language.
This language would only be able to handle integers and integer operators with no standard library. The next work will
be for Boolean and Boolean operators. Then Control Flow in the form of *cond*.

This <cite>timeline[^2]</cite> is rough and subject to change.

## Sources
I will be using certain books to guide my development.
- *Programming Language Pragmatics* by Michael L. Scott
- *Engineering a Compiler* by Keith D. Cooper & Linda Torczon

<!----------------------Footer---------------------->

<hr>

[^1]: Scheme standard [r7rs](https://small.r7rs.org/attachment/r7rs.pdf)
[^2]: I will more clearly highlight my timeline on [GitHub](https://github.com/snowmang1/sxeme)
