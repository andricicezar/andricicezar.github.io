---
layout: home
author_profile: true
permalink: /
---


I’m a Ph.D. candidate at [MPI-SP](https://mpi-sp.org), Bochum, Germany working with [Cătălin Hriţcu](https://catalin-hritcu.github.io/).
My Ph.D. project is about secure interoperability between verified F\* programs and unverified ML code.
I earned my Bachelor’s and Master’s degrees in *Computer Science* from Alexandru Ioan Cuza University of Iași, Romania.
I also hold a Master’s degree in *Regional Development* from the same university.

<h3 id="research">Research interests</h3>

**Verification of effectful code.**
In a pure dependently-typed language, like Rocq or F\*, one can write pure terminating computations and verify them.
If one wants to write effectful computations (e.g., with state, non-termination, input/output (IO), etc.),
then one has to give a representation to those computations. One common way is to do a shallow embedding,
by embedding the effect in the language using a monad.
F\* has this idea at its core and uses a construction called the Dijkstra monad.
Such constructions were used successfully to verify big developments and realistic projects.
My work in this space was involved into finding the pre-conditional effect (specific to F\*),
and building Dijkstra monads for terminating/non-terminating IO and Monotonic State.
These results are interesting because the effects F\* supports out of the box
do not have a monadic representation (are axiomatized),
and if one finds a representation for each of them,
the TCB of F\* would be minimized.
Right now, I am interested in finding a monadic representation for the effects Div, Ghost,
Monotonic State with cyclic higher-order stores, and Concurrency with IO.

**Secure Compilation of F\*.**
The language F\* was used successfully in the verification of some big
projects, some of them milestones in the verification community.
One convenient feature of F\* is primitive
extraction to OCaml of effectful computations, meaning that the monadic representation
of the computation is erased during extraction and the monad's operations are replaced
with the corresponding OCaml operations.
This extraction, however, it is part of the TCB of F\* so it is not verified to be correct.
This is problematic because if the verified extracted code gets linked to unverified code, then there is a chance
of a bug or an attack, meaning it may be unsound or insecure (the logical
invariants proved about the verified code are broken by the unverified code).
To bring some trust to this, my work proposes SCIO\* and SecRef\*,
two secure compilation frameworks for verified IO programs, and respectively stateful programs,
that can be safely linked with unverified code. The long-term goal of the project
is to have secure interoperability between F\* and OCaml.
<!-- Another idea I am interested in, is to also explore if one could give up on the effect system of F\*
and instead use the typing abstractions provided by the module system. -->

<h3 id="papers">Publications, drafts and extended abstracts</h3>

* [**Towards formally secure compilation of verified F\* programs against unverified ML contexts (Extended Abstract)**](/wp-content/uploads/publications/prisc26.pdf).<br/> *Cezar-Constantin Andrici*, Danel Ahman, Cătălin Hrițcu, Guido Martínez, Abigail Pribisova, Exequiel Rivas, and Théo Winterhalter.
* [**SecRef\*: Securely Sharing Mutable References between Verified and Unverified Code in F\***](https://arxiv.org/abs/2503.00404).<br/> *Cezar-Constantin Andrici*, Danel Ahman, Cătălin Hrițcu, Ruxandra Icleanu, Guido Martínez, Exequiel Rivas, and Théo Winterhalter. <br/>
  In [ACM SIGPLAN International Conference on Functional Programming (ICFP)](https://doi.org/10.1145/3747522), October 2025.<br/>[Slides :new:](./wp-content/uploads/ICFP2025-SecRef.pdf) | [Artifact](https://zenodo.org/records/15659350) - *The artifact received the Functional and Reusable badges.*
* [**Securing Verified IO Programs Against Unverified Code in F\***](https://arxiv.org/abs/2303.01350).<br/> *Cezar-Constantin Andrici*, Ștefan Ciobâcă, Cătălin Hrițcu, Guido Martínez, Exequiel Rivas,&nbsp;Éric Tanter and Théo Winterhalter. <br/>In [51st ACM SIGPLAN Symposium on Principles of Programming Languages (POPL)](https://doi.org/10.1145/3632916), January 2024.<br/>[Artifact](https://zenodo.org/doi/10.5281/zenodo.10125015) - *The artifact received the Functional and Reusable badges.*
* [**A Verified Implementation of the DPLL Algorithm in Dafny**](https://doi.org/10.3390/math10132264).<br/> *Cezar-Constantin Andrici* and Ștefan Ciobâcă. In Mathematics, 10(13), 2264, June 2022. <br/> [Artifact](https://github.com/andricicezar/truesat)
* [**Verifying non-terminating programs with IO in F\* (Extended Abstract)**](https://theowinterhalter.github.io/res/iodiv-hope.pdf).<br/> *Cezar-Constantin Andrici*, Théo Winterhalter, Cătălin Hrițcu and Exequiel Rivas.<br/> At the 10th ACM SIGPLAN Workshop on Higher-Order Programming with Effects (HOPE), September 2022. <br/> [Artifact](https://github.com/andricicezar/fstar-io/tree/hope-submission)
* [**Partial Dijkstra Monads for All (Extended Abstract)**](https://types22.inria.fr/files/2022/06/TYPES_2022_paper_18.pdf). <br/> Théo Winterhalter, *Cezar-Constantin Andrici*, Cătălin Hrițcu, Kenji Maillard, Guido Martínez and Exequiel Rivas.<br/>At the 28th International Conference on Types for Proofs and Programs (TYPES), June 2022. <br/> [Artifact](https://github.com/TheoWinterhalter/pdm4all/releases/tag/types2022)
* [**Verifying the DPLL Algorithm in Dafny**](https://arxiv.org/abs/1909.01743).<br/> *Cezar-Constantin Andrici* and Ștefan Ciobâcă. <br/>In Proceedings Third Symposium on
Working Formal Methods, EPTCS 303, pp. 3-15, 2019.

<h3 id="papers">Talks</h3>

* **Securing Verified IO Programs Against Unverified Code in F\***.<br/>At the 51st ACM SIGPLAN Symposium on Principles of Programming Languages (POPL), January 2024 ([video](https://www.youtube.com/watch?v=7jCChuyZHR4)), and an extended version at the [F\* PoP Up Seminar](https://fstar-lang.org/popup/seminar.html), July 2023 ([video](https://www.youtube.com/watch?v=BFyKX1li8Zw)).
* **Verifying non-terminating programs with IO in F\* (Extended Abstract)**.<br/> At the 10th ACM SIGPLAN Workshop on Higher-Order Programming with Effects (HOPE), September 2022. <br/> [Slides](https://cezarandrici.com/wp-content/uploads/2022/09/HOPE22_Andrici_Slides.pdf). [Video](https://www.youtube.com/watch?v=i6gfZteKAAw).
* **Gradual Enforcement of IO Trace Properties at Student Research Competition**,<br/> At the 25th ACM SIGPLAN International Conference on Functional Programming (ICFP), August 2020.<br/>:trophy: **First place winner of ICFP SRC 2020, graduate section**<br/> [Video](https://youtube.com/watch?v=fMkYhgFYQA0)
* **Verification of IO programs in F\*** at Faculty of Computer Science, UAIC, January 2020.

<h3 id="research">Teaching Assistant</h3>
* Proofs are Programs, RUB, Bochum, Fall 2024-2025
* Functional Programming, RUB, Bochum, Summer 2023-2024
* Logics in Computer Science, UAIC, Iași, Fall 2020-2021

<h3 id="research">Scientific Service</h3>
* Sub-reviewer at CPP'26, ICFP'25, POPL'24, SP'21
* Member in Artifact Evaluation Committee at POPL'26, POPL'23
* Student Volunteer at POPL'24, POPL'23, ICFP'22, PLDI'20, POPL'20, ETAPS'19, FROM'18
