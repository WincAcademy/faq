+++
title = "How bad is duplication in my test code?"
extra.tags =[ "testen"]
created = "Mar 8, 2021 5:05 PM"
+++

# How bad is duplication in my test code?

Here's a famous quote about debugging.

> Everyone knows that debugging is twice as hard as writing a program in the first place. So if you're as clever as you can be when you write it, how will you ever debug it?
> — The Elements of Programming Style, 2nd edition, chapter 2

The same can be said about testing code, to a degree.

## Keep your testing code simple

A good rule of thumb is that your tests should be easy to read. You should not
have to jump around a lot in your code (to helper functions) to be able to
understand a single test case.

It can be tempting to write a lot of helper functions to make your test code
more DRY. In general we advise against this as this makes your test code harder
to read. Having duplication in your tests is also less of a problem than having
them in your code-under-test. In general test code is changed less often than
the code-under-test.

You can jump to 7:22 in [this video](https://vimeo.com/504723308/5a35db2299) to
see a (Dutch language) live-lesson on this very topic.

There _is_ a point where you might want to DRY your test code, this is when you
need to do a lot of similar setup for a number of tests. So things like mocking
an API or pre-filling a database. You should put that kind of functionality in
the setup or fixture of your test code.

So, to answer the question: duplication in your test code is not bad.
