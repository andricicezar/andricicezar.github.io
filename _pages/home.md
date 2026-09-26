---
layout: home
permalink: /
---

## Motivation

My goal is to bring trust to digital systems.
More of our lives run on software every day: our money, our identities, our public services, our votes,
and soon the autonomous robots around us.
We are asked to trust this software, and the companies and institutions behind it,
with our data and our safety, yet we have little evidence that it deserves that trust.
As a growing share of code is written by AI, faster than anyone can review it, this gap only widens.

Law and policy try to restore that trust, but compliance often turns into a formality
that people neither understand nor believe protects them.
Audits and testing help, but they struggle to keep up and cannot offer mathematical guarantees.
Formal verification can: a machine-checked proof holds no matter who, or what, wrote the code.
My research works toward making such guarantees practical for real programs:
verifying effectful code in proof-oriented languages such as F\*,
and securely compiling verified code so that its guarantees survive when linked with unverified code.
I use AI agents every day to write both code and proofs,
and I believe they will make verification cheap enough for all critical software.

## Research Projects

### Verification of Rust programs with Aeneas

I am extending [Aeneas](https://github.com/AeneasVerif/aeneas) to verify Rust programs
that manipulate raw pointers directly.
Aeneas translates safe Rust into pure functional code, which keeps proofs simple,
but this approach does not apply once a program uses raw pointers in `unsafe` code.
To handle such programs, I am adding support for separation logic to Aeneas,
targeting its [Lean](https://lean-lang.org/) backend,
together with proof automation so that these proofs stay as simple as possible.

### Secure compilation from F\*

My Ph.D. thesis is about securely compiling programs verified in
[F\*](https://fstar-lang.org/), a proof-oriented programming language:
the guarantees proved in F\* should still hold once the compiled code
is linked with unverified code.
I developed [SCIO\*](https://github.com/andricicezar/fstar-io/tree/master/sciostar) for programs with IO ([POPL 2024](https://arxiv.org/abs/2303.01350))
and [SecRef\*](https://github.com/andricicezar/fstar-io/tree/master/secrefstar) for programs that share mutable references with unverified code ([ICFP 2025](https://arxiv.org/abs/2503.00404)).
Most recently, I developed [SEIO\*](https://github.com/andricicezar/fstar-io/tree/master/seiostar), which securely extracts F\* programs with IO
to an OCaml-like language ([ICFP 2026](https://arxiv.org/pdf/2602.19973)).

### Verified SAT solving in Dafny

Earlier, I built [TrueSAT](https://github.com/andricicezar/truesat), a verified implementation of the DPLL algorithm, the basis of modern SAT solvers,
in [Dafny](https://dafny.org/), a verification-aware programming language
([FROM 2019](https://arxiv.org/abs/1909.01743), [Mathematics 2022](https://doi.org/10.3390/math10132264)).

## News

{% include news.html items=site.data.news %}
