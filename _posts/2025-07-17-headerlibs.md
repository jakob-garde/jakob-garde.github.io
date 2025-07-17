---
title: "Working with your own header-only libraries"
---

Org text:

Have you ever written a pointer-hash map? It is surprisingly fun and satisfying.

Here's my baselayer project - many such projects exist out there - and this one is what I have come up with so far. At some point I discovered 
the existence of custom memory allocators, custom buffers and length-based strings, and started writing my own versions. Some of the code 
was collected in homebrew libraries ([baselayer] and [cbui]).

Such "baselayer" libraries provide basic utilities for effective programming in a small language like C. It feels luxurious to have light-weight
tools at hand, not having to worry about installing and linking gigabytes of helper libraries, or reading monolithic APIs, just to do 
relatively basic and normal things.

The concept of header-only libraries seemed well worth copying. Using "unity build", the entire program is statically compiled from source.
Code is organized in .h files, meaning the headers and implementations are found in the same place. This is already standard practice in 
most languages - so why not?

A rudimentary CMake config file in included, for linking convenience in the cases where this is needed, and for seamless integration with certain tools.

[baselayer]: https://github.com/climbcat/baselayer
[cbui]: https://github.com/climbcat/cbui
