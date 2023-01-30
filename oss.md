---
title: "Open Source Projects"
description: null
---

## The Rust Programming Language

A language empowering everyone to build reliable and efficient software. I'm
officially part of the [operational semantics team] tasked with owning, refining,
documenting, and specifying the semantics of unsafe code. This is the team
which is in charge of defining what exactly it means to run a Rust program.

[operational semantics team]: https://rust-lang.github.io/rfcs/3346-t-opsem.html

In addition to that, I'm generally active in the forums for development of the
language to discuss design of potential extensions to the language and/or standard
library. I also do my best to give contribute to the ecosystem at large by the
means of issues, pull requests, and discussion of common ecosystem libraries.

## pest, The Elegant Parser

A general purpose declarative parser generator built in and for use from Rust,
based on the formal class of Parsing Expression Grammars. While I'm not quite as
involved in development anymore as I have been previously, I helped refine the
bootstrapping build system and still assist in project management and direction.

The original developer of pest had to step away for personal reasons, so it fell
to me to ensure that the project would not be fully abandoned and find people from
the community to maintain the library. I like to think I've done a reasonable job.

## point-rs

A collection of abstractions focused on making working with raw pointers easier
in Rust. Helps stretch the boundaries of what is accomplishable in safe Rust,
including the use of custom variably-sized types not safely constructible in
the base language and type-erased pointers without giving up the API safety of
"fat" typed pointers at the interface of the implementation.
