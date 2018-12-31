---
id: intro
title: Introduction
---

[`react-testing-library`][gh] builds on top of `dom-testing-library` by adding APIs for working with React components.

```
npm install --save-dev react-testing-library
```

- [react-testing-library on GitHub][gh]

[gh]: https://github.com/kentcdodds/react-testing-library

## The problem

You want to write maintainable tests for your React components. As a part of
this goal, you want your tests to avoid including implementation details of your
components and rather focus on making your tests give you the confidence for
which they are intended. As part of this, you want your testbase to be
maintainable in the long run so refactors of your components (changes to
implementation but not functionality) don't break your tests and slow you and
your team down.

## This solution

The `react-testing-library` is a very light-weight solution for testing React
components. It provides light utility functions on top of `react-dom` and
`react-dom/test-utils`, in a way that encourages better testing practices. Its
primary guiding principle is:

> [The more your tests resemble the way your software is used, the more
> confidence they can give you.](guiding-principles.md)

So rather than dealing with instances of rendered react components, your tests
will work with actual DOM nodes. The utilities this library provides facilitate
querying the DOM in the same way the user would. Finding for elements by their
label text (just like a user would), finding links and buttons from their text
(like a user would). It also exposes a recommended way to find elements by a
`data-testid` as an "escape hatch" for elements where the text content and label
do not make sense or is not practical.

This library encourages your applications to be more accessible and allows you
to get your tests closer to using your components the way a user will, which
allows your tests to give you more confidence that your application will work
when a real user uses it.

This library is a replacement for [Enzyme](http://airbnb.io/enzyme/). While you
_can_ follow these guidelines using Enzyme itself, enforcing this is harder
because of all the extra utilities that Enzyme provides (utilities which
facilitate testing implementation details). Read more about this in
[the FAQ](./faq).

**What this library is not**:

1.  A test runner or framework
2.  Specific to a testing framework (though we recommend Jest as our preference,
    the library works with any framework. See
    [Using Without Jest](./setup#using-without-jest))

> NOTE: This library is built on top of
> [`dom-testing-library`](/)
> which is where most of the logic behind the queries is.

## What is react-testing-library?

Have a look at the video below for an explanation. <br/><br/>
[![what is react testing library](https://img.youtube.com/vi/JKOwJUM4_RM/0.jpg)](https://youtu.be/JKOwJUM4_RM 'what is react testing library')