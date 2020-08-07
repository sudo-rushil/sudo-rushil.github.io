---
layout: post
tags: lambda
---

I suppose this is a good place to start. Since RMP ended, I've been working on what was originally a small untyped lambda calculus interpreter. Originally, it was just an excuse to practice writing parsers using Alex/Happy in Haskell for an upcoming project, but slowly, it grew to a good exercise in language design in itself.

Recently, with the hurricane that passed through CT, knocking out internet connectivity, I've had lots of time to expand this, leading to a language with runnable files, binds, and a module system. Of course, it's still a pure untyped lambda calculus, but with extensions that enable a level of "useful" programming. So, I wanted to formally introduce [lambda](https://github.com/sudo-rushil/lambda), a Haskell implementation of the untyped lambda calculus.

Lambda does a few things differently from some other lambda calculus implementations I've seen. First, it is well and truly *untyped*. This is in contrast to the simply-typed lambda calculus that is at the conceptual core of type systems like HM, or higher rank calculi like F2. This means that all lambda expressions are syntactically pure. However, it also has a powerful bind system; variable bindings can be introduced easily, which act as function macros enabling you to avoid unnecessary repetition. Moreover, as a current experimental feature, you can use commands to reverse function bindings back into their symbol, enabling a form of "pretty printing" output. I'm in the process of documenting everything into a language reference, so stay tuned!

With such a nice platform for practicing language design, where will I go from here? I've had a couple ideas bouncing around right now. First, I want to implement DeBruijn indexes, primarily as an experiment in term rewriting strategies but also due to the fact that DeBruijn indexes for lambda terms is invariant to alpha conversion, meaning I can potentially simplify the reduction logic and compress the data needed to store terms. I also want to experiment with compiling expressions to LLVM, although the benefit and doability of this is questionabale. Finally, I have lots to expand in the standard library (combinators, lists, etc.).

Keep an eye out on Github, and do let me know what you think!
