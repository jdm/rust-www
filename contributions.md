---
layout: default
title: Contributing to Rust &middot; The Rust Programming Language
---

# Contributing to Rust

You've started learning Rust. You love it, and you want to be a part
of it. If you're not sure how best to get involved, then this page
will help.

**Just want to report a bug in Rust?** [Follow the Rust bug reporting
guide][bugs]. Thanks in advance!

Rust is an expansive system of projects, some officially maintained
within the [rust-lang organization on GitHub][rust-lang], but with many
increasingly-important efforts driven from without by its enthusiastic
community. Newcomers will be interested in [an overview of the
organization, processes, and policies of The Rust Project][dev_proc]
and the project's [CONTRIBUTING.md] file, which explains the specifics
of contributing to [rust-lang/rust].

There are many ways to contribute to the success of Rust.
This guide focuses on a few avenues for the new contributor:

* [Bugs, triage, and maintenance](#bugs). Finding issues to fix,
  triaging, adding test cases.
* [Documentation](#doc). Not just official documentation, but also
  for crates, blog posts, and other unofficial sources.
* [Community building](#comm). Expanding the reach of Rust, and
  maintaining its excellence.
* [Tooling, IDEs, and infrastructure](#tool). The hard work of making
  Rust accessible to programmers of all kinds.
* [Libraries](#lib). Including the standard library, but also allo the
  other equally-important official and unofficial crates that make
  Rust usable.
* [Language and compiler](#comp). Language design, feature
  implementation, performance improvement.

If you need additional guidance ask on [#rust-internals] or
[internals.rust-lang.org]. All contributors are expected to follow our
[Code of Conduct][coc].

[bugs]: https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md#bug-reports
[dev_proc]: dev_process.html
[rust-lang]: https://github.com/rust-lang
[rust-lang/rust]: https://github.com/rust-lang/rust
[CONTRIBUTING.md]: https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md
[coc]: https://www.rust-lang.org/conduct.html
[#rust-internals]: https://client00.chat.mibbit.com/?server=irc.mozilla.org&channel=%23rust-internals
[internals.rust-lang.org]: https://internals.rust-lang.org/

<a name="bugs"></a>
## Bugs, triage, and maintenance

The day-to-day maintenance of the project revolves around Rust's
[issue tracker] and [pull requests][PR], and more help is always
needed. The most basic way to get started contributing to Rust is to look for
the [E-easy][e_easy_issues] or [E-mentor][e_mentor_issues]
labels. These are meant to be approachable for new Rust programmers.

On `E-mentor` issues an experienced Rust developer has volunteered to
mentor somebody to solve the issue. They will have volunteered in the
issue comments and you should feel free to contact them on the issue
tracker or directly. Note that Rust developers get a lot of email
notifications and it is easy to lose track of them; don't hesitate to
hunt them down by whatever means necessary!

While Rust has an [extensive test suite][test] there is always more to
test. The [E-needstest] label indicates issues that are thought to be
fixed but don't have tests. Writing test cases is a great way to
understand a new project and get started contributing.

Rust is always in need of people to [triage] issues: reproduce bugs,
minimize test cases, apply labels, close resolved issues. Note that
you'll have to get your permissions adjusted on GitHub to apply
labels, but this is easy to obtain for somebody with a bit of
experience with the project. Ask a [team] member.

Once you've found your way around the project and have created a few
pull requests in a particular area of the project, consider actively
reviewing others' pull requests: reviewership is a rare skill and good
reviewers are always appreciated. No prior permission is needed - just
start constructively and politely commenting on pull requests that interest you.

[lru_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-asc
[issue tracker]: https://github.com/rust-lang/rust/issues
[PR]: https://github.com/rust-lang/rust/pulls
[e_easy_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AE-easy
[e_mentor_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AE-easy+label%3AE-mentor
[triage]: https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md#issue-triage
[E-needstest]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AE-needstest
[test]: https://github.com/rust-lang/rust-wiki-backup/blob/master/Note-testsuite.md
[team]: team.html

<a name="doc"></a>
## Documentation

Documentation is never good enough and there's never enough of it, so
writing documentation is a simple and valuable way to contribute.
Many aspects of Rust's documentation don't require deep knowledge, and
writing documentation is also a great way to learn more about the
language or specific libraries. Furthermore, improvements to
documentation are easy to identify and limitless. Don't like the way
something reads? Discover some information that wasn't documented?
Your pull request will be gleefully embraced.

[The Book] is the primary documentation for Rust, maintained in the
main repository. It has its own [issue label][book_issues] and is
continually being refined. Other documentation in the main repository
include [The Rust Reference], the [standard library API
documentation][std], [The Rustonomicon], and [the compiler error
index][err]. The [Rust Style Guidelines] are so incomplete they are
not linked prominently; an ambitious contributor can make much
headway there. Most in-tree documentation lives in the [src/doc]
directory. To contribute simply edit it and submit a pull
request. These are all covered by the [A-docs] label on the issue
tracker.

A great deal of important Rust documentation does not live in the main
repository, or is not maintained by The Rust Project, but is still
critically important to Rust's success. Examples of strategic Rust
documentation that is actively developed and in need of contributors
include [Rust By Example], [Rust Design Patterns], and [rust-rosetta].
For even more ideas for existing documentation projects to contribute
to see [rust-learning].

*The most impactful documentation you can write [may be that for the
crates that make up the Rust ecosystem][crate_docs]*. While the
documentation maintained by The Rust Project is highly-regarded, the
same is not yet true for [many of the popular crates and
tools][awesome-rust] that Rust programmers interact with every
day. Contributing API documentation to a popular Rust project will
earn you the enduring love of that project's maintainer.

[Rust Style Guidelines]: http://doc.rust-lang.org/style/index.html
[The Book]: http://doc.rust-lang.org/book/index.html
[book_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AA-book
[A-docs]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AA-docs
[Rust By Example]: https://github.com/rust-lang/rust-by-example
[The Rust Reference]: http://doc.rust-lang.org/reference.html
[src/doc]: https://github.com/rust-lang/rust/tree/master/src/doc
[err]: http://doc.rust-lang.org/error-index.html
[std]: http://doc.rust-lang.org/std/index.html
[The Rustonomicon]: http://doc.rust-lang.org/nomicon/index.html
[Rust Design Patterns]: https://github.com/nrc/patterns
[rust-rosetta]: https://github.com/Hoverbear/rust-rosetta
[rust-learning]: https://github.com/ctjhoa/rust-learning
[crate_docs]: https://users.rust-lang.org/t/lets-talk-about-ecosystem-documentation/2791
[awesome-rust]: https://github.com/kud1ing/awesome-rust

<a name="comm"></a>
## Community building

TWIR, podcasts.

A-mentor, #rust-beginners, SO

Advocacy in non-Rust communities, expanding to new places

holding and attending meetups

publicizing opportunities for new contributors
project status updates
experience reports
conf talks tutorials, particularly for new audiences
outreach to underserved audiences

Posting in weekly what are you doing threads.

Nearly any new initatives will be well-received.

<a name="tool"></a>
## Tooling, IDEs, and infrastructure

Tools play a huge part in the success of a language. Rust has some
great tool support, in particular with debugging and package
management, but we need much more.

- [cargo](https://github.com/rust-lang/cargo/issues) Rust's package manager and build system.
- [rustdoc](https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AA-rustdoc)
  Produces documentation for the official libraries and user projects.
- [racer](https://github.com/phildawes/racer) Code completion.
- [rustfmt](https://github.com/nrc/rustfmt) Code formatting.
- [multirust](https://github.com/brson/multirust/issues) For managing
  multiple installations of the Rust toolchain.
- [homu](https://github.com/barosl/homu/issues) Acts as a gatekeeper for commits.

<a name="libs"></a>
## Libraries

[Libstd][libstd], [libcollections][libcollections],
[liballoc][liballoc] and [libcore][libcore] are the main library
crates.  These all appear to users as if they are part of libstd, the
standard library. These tend to be very fundamental libraries -
built-in types, low level IO and concurrency, allocation, essential
collections, and so forth. You should join [#rust-libs][libs_irc] if
you are interested in contributing to the Rust libraries.

[libstd]: https://github.com/rust-lang/rust/tree/master/src/libstd
[libcollections]: https://github.com/rust-lang/rust/tree/master/src/libcollections
[liballoc]: https://github.com/rust-lang/rust/tree/master/src/liballoc
[libcore]: https://github.com/rust-lang/rust/tree/master/src/libcore
[libs_irc]: irc://moznet/rust-libs

<a name="comp"></a>
## Language and compiler

The compiler is part of the [main repo][main_repo], which also
includes the standard library crates and a whole bunch of supporting
code. For questions about the compiler, there is the
[#rustc] IRC channel. Compiler errors (ICE for 'Iinternal
Compiler Errors') can be searched for in issues using the
[I-ICE][i_ice_issues] label. These are usually good bugs to start with
because it's easy to know when you've fixed them, and they're often
relatively self-contained. If you're interested in parsing, macros,
syntactic stuff, the [parsing][parsing_issues] label and the
[macro][macro_issues] label are a good places to start.

[main_repo]: https://github.com/rust-lang
[#rustc]: https://client00.chat.mibbit.com/?server=irc.mozilla.org&channel=%23rustc
[i_ice_issues]: https://github.com/rust-lang/rust/labels/I-ICE
[parsing_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AA-parser
[macro_issues]: https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AA-parser+label%3AA-macros

#### Other Contributions

Try [Github Trending][trending] for currently active Rust projects.
There are a number of other ways to contribute to Rust that don't deal
directly with the Rust repository.

- Answer questions in [#rust][rust_irc], on the [Rust Forum][forum] or
  on [Stack Overflow][stack_overflow].
- Participate in the [RFC process][rfcs].
- Find a [requested community library][requested], build it, and
  publish it to [Crates.io][crates]. Easier said than done,
but very, very valuable!

[trending]: https://github.com/trending?l=rust
[rust_irc]: irc://moznet/rust
[forum]: https://users.rust-lang.org/
[stack_overflow]: http://stackoverflow.com/questions/tagged/rust
[rfcs]: https://github.com/rust-lang/rfcs
[requested]: https://github.com/rust-lang/rfcs/labels/A-community-library
[crates]: http://crates.io
