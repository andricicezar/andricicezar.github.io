---
layout: home
author_profile: true
permalink: /
---


<p>I’m a Ph.D. candidate at <a href="https://mpi-sp.org">MPI-SP</a>, Bochum, Germany working with <a href="https://catalin-hritcu.github.io/">Cătălin Hriţcu</a>.
My Ph.D. project is about secure interoperability between verified F* programs and unverified ML code.</p>

<h3 id="research">Research</h3>

<p>
    <strong>Verification of effectful code.</strong>
    In a pure dependently-typed language, like Rocq or F*, one can write pure terminating computations and verify them.
    If one wants to write effectful computations (e.g., with state, non-termination, input/output (IO), etc.),
    then one has to give a representation to those computations. One common way is to do a shallow embedding, 
    by embedding the effect in the language using a monad.
    F* has this idea at its core and uses a construction called the Dijkstra monad.
    Such constructions were used successfully to verify big developments and realistic projects.
    My work in this space was involved into finding the pre-conditional effect (specific to F*),
    and building Dijkstra monads for terminating/non-terminating IO and Monotonic State.
    These results are useful because the effects F* supports out of the box,
    do not have a monadic representation, and my hope is that one would be able to find one
    for all of them.
    Right now, I am interested in finding a Dijkstra monad for the effects Div, Ghost, 
    Monotonic State with higher-order stores and Concurrency with IO.
</p>

<p>
    <strong>Secure Compilation of F*.</strong>
    The language F* was used successfully in the verification of some big
    projects, some of them milestones in the verification community.
    One of the big features of F* is that it is easy to have primitive
    extraction for effectful computations to OCaml, meaning that the monadic representation
    of the computation is erased during extraction and the monad's operations are replaced
    with the corresponding OCaml operations.
    This extraction, however, it is part of the TCB of F* so it cannot be trusted to be correct.
    Moreover, if the verified extracted code gets linked to unverified code, then the chance
    that there is a bug, or an attack, is even bigger, so it may be even insecure (the logical
    invariants proved about the verified code are broken by the unverified code).
    To bring some trust to this, my work proposes SCIO* and SecRef*,
    two secure compilation frameworks for verification of IO programs, and respectively stateful programs,
    that can be safely linked with unverified code. The long-term goal of the project
    is to have secure interoperability between F* and OCaml.
    Another idea I am interested in, is to also explore if one could give up on the effect system of F*
    and instead use the typing abstractions provided by the module system.
</p>

<h3 id="papers">Publications, drafts and extended abstracts</h3>

* **SecRef\*: Securely Sharing Mutable References Between Verified and Unverified Code in F\***.<br/> *Cezar-Constantin Andrici*, Danel Ahman, Cătălin Hrițcu, Ruxandra Icleanu, Guido Martínez, Exequiel Rivas, and Théo Winterhalter.<br/>[PrePrint](https://arxiv.org/abs/2503.00404).
* [**Securing Verified IO Programs Against Unverified Code in F\***](https://doi.org/10.1145/3632916).<br/> *Cezar-Constantin Andrici*, Ștefan Ciobâcă, Cătălin Hrițcu, Guido Martínez, Exequiel Rivas,&nbsp;Éric Tanter and Théo Winterhalter. <br/>ACM SIGPLAN Symposium on Principles of Programming Languages (**POPL 2024**) *The artifact received the Functional and Reusable badges.*<br/>[PrePrint](https://arxiv.org/abs/2303.01350). [Video](https://www.youtube.com/watch?v=7jCChuyZHR4). [Artifact](https://zenodo.org/doi/10.5281/zenodo.10125015)
* [**Who Verifies the Verifiers? A Computer-Checked Implementation of the DPLL Algorithm in Dafny.**](https://doi.org/10.3390/math10132264)<br/> *Cezar-Constantin Andrici* and Ștefan Ciobâcă. In *Mathematics 2022*, 10(13), 2264. <br/> [Artifact](https://github.com/andricicezar/truesat)
* [**Verifying non-terminating programs with IO in F\* (Extended Abstract)**](https://theowinterhalter.github.io/res/iodiv-hope.pdf).<br/> *Cezar-Constantin Andrici*, Théo Winterhalter, Cătălin Hrițcu and Exequiel Rivas.<br/> ACM SIGPLAN Workshop on Higher-Order Programming with Effects (**HOPE'22**). <br/> [Slides](https://cezarandrici.com/wp-content/uploads/2022/09/HOPE22_Andrici_Slides.pdf). [Video](https://www.youtube.com/watch?v=i6gfZteKAAw). [Artifact](https://github.com/andricicezar/fstar-io/tree/hope-submission)
* [**Partial Dijkstra Monads for All (Extended Abstract)**](https://types22.inria.fr/files/2022/06/TYPES_2022_paper_18.pdf). <br/> Théo Winterhalter, *Cezar-Constantin Andrici*, Cătălin Hrițcu, Kenji Maillard, Guido Martínez and Exequiel Rivas.<br/>International Conference on Types for Proofs and Programs (**TYPES'22**). <br/> [Slides](https://types22.inria.fr/files/2022/06/TYPES_2022_slides_18.pdf). [Artifact](https://github.com/TheoWinterhalter/pdm4all/releases/tag/types2022)