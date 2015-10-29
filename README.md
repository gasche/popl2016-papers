# popl2016-papers

Links to [accepted papers][popl2016-accepted] for the [43rd ACM
SIGPLAN-SIGACT Symposium on Principles of Programming
Languages][popl2016-website] (POPL 2016).  **Pull requests welcome!**

[popl2016-website]: http://conf.researchr.org/home/POPL-2016/
[popl2016-accepted]: http://conf.researchr.org/track/POPL-2016/POPL-2016-papers

(Similar pages are available for [POPL 2015][popl2015], [POPL
2014][popl2014], and [2013][popl2013], ICFP ([2012][icfp12],
[2013][icfp13], [2014][icfp14]) and [PLDI 2014][pldi2014-accepted].)

[popl2013]: https://github.com/23Skidoo/popl13-papers-links
[popl2014]: https://github.com/gasche/popl2014-papers
[popl2015]: https://github.com/yallop/popl2015-papers
[icfp12]: https://github.com/technogeeky/icfp12-paper-links
[icfp13]: https://github.com/gasche/icfp2013-papers
[icfp14]: https://github.com/yallop/icfp2014-papers
[haskell2014-accepted]: https://github.com/yallop/haskell2014-papers
[pldi2014-accepted]: https://github.com/yallop/pldi2014-papers

Note: the [POPL'16 website][popl2016-website], powered by the
increasingly convenient [conf.researchr](http://conf.researchr.org/)
platform, has nice eye-candy display of paper abstract on click, etc,
and they have the ability give links to the article
preprint. Unfortunately, we couldn't find any information on how to
contribute such links, so git repositories still remain the most
convenient way to help crowd-source the preprint-gathering
activity. We hope to be able to integrate links contributed here to
their platform, to benefit an even larger audience.


## POPL 2016

* **'Cause I'm Strong Enough: Reasoning about Consistency Choices in Distributed Systems**  
  by Alexey Gotsman, Hongseok Yang, Carla Ferreira, Mahsa Najafzadeh, Marc Shapiro  

    > Large-scale distributed systems often rely on replicated
    > databases that allow a programmer to request different data
    > consistency guarantees for different operations, and thereby
    > control their performance. Using such databases is far from
    > trivial: requesting stronger consistency in too many places may
    > hurt performance, and requesting it in too few places may
    > violate correctness. To help programmers in this task, we
    > propose the first proof rule for establishing that a particular
    > choice of consistency guarantees for various operations on
    > a replicated database is enough to ensure the preservation of
    > a given data integrity invariant. Our rule is modular: it allows
    > reasoning about the behaviour of every operation separately
    > under some assumption on the behaviour of other operations. This
    > leads to simple reasoning, which we have automated in an
    > SMT-based tool. We present a nontrivial proof of soundness of
    > our rule and illustrate its use on several examples.

* **A Program Logic for Concurrent Objects under Fair Scheduling**  
  by Hongjin Liang, Xinyu Feng  

    > Existing work on verifying concurrent objects is mostly concerned
    > with safety only, e.g., partial correctness or
    > linearizability. Although there has been recent work verifying
    > lock-freedom of non-blocking objects, much less efforts are focused
    > on deadlock-freedom and starvation-freedom, progress properties of
    > blocking objects. These properties are more challenging to verify
    > than lock-freedom because they allow the progress of one thread to
    > depend on the progress of another, assuming fair scheduling.
    >
    > We propose LiLi, a new rely-guarantee style program logic for
    > verifying linearizability and progress together for concurrent
    > objects under fair scheduling. The rely-guarantee style logic
    > unifies thread-modular reasoning about both starvation-freedom and
    > deadlock-freedom in one framework. It also establishes
    > progress-aware abstraction for concurrent objects, which can be
    > applied when verifying safety and liveness of client code. We have
    > successfully applied the logic to verify starvation-freedom or
    > deadlock-freedom of representative algorithms such as ticket locks,
    > queue locks, lock-coupling lists, optimistic lists and lazy lists.

* **A Theory of Effects and Resources: Adjunction Models and Polarised Calculi**  
  by Pierre-Louis Curien, Marcelo Fiore, Guillaume Munch-Maccagnoni  

    > We consider the Curry-Howard-Lambek correspondence for effectful
    > computation and resource management, specifically proposing polarised
    > calculi together with enriched adjunction models as the starting point
    > for a comprehensive semantic theory relating logical systems, typed
    > calculi, and categorical models in this context.
    >
    > Our thesis is that the combination of effects and resources should be
    > considered orthogonally. Model theoretically, this leads to an
    > understanding of our categorical models from two complementary
    > perspectives: (i) as a linearisation of Call-by-Push-Value adjunction
    > models, and (ii) as an extension of linear/non-linear adjunction
    > models with an adjoint resolution of computational effects. When the
    > linear structure is cartesian and the resource structure is trivial we
    > recover Levy’s notion of CBPV adjunction, while when the effect
    > structure is trivial we have Benton’s linear/non-linear adjunction
    > models. Further instances of our model theory include the dialogue
    > categories with a resource modality of Melliès and Tabareau, and the
    > [E]EC ([Enriched] Effect Calculus) models of Egger, Møgelberg and
    > Simpson. Our development provides a lifting theorem of linear models
    > into cartesian ones.
    >
    > To each of our categorical models we systematically associate a typed
    > term calculus, each of which corresponds to a variant of the sequent
    > calculi LJ (Intuitionistic Logic) or ILL
    > (Intuitionistic Linear Logic). The adjoint resolution of effects
    > corresponds to polarisation whereby, syntactically, types locally
    > determine a strict or lazy evaluation order and, semantically, the
    > associativity of cuts is relaxed. In particular, our results show that
    > polarisation provides a computational interpretation of
    > Call-by-Push-Value in direct style. As an application, we give
    > a decomposition of commuting conversions that appear in the
    > operational semantics of effects such as Benton and Kennedy’s
    > “exceptional syntax”.

* **A concurrency semantics for relaxed atomics that permits optimisation and avoids thin-air executions**  
  by Jean Pichon-Pharabod, Peter Sewell  

    > Despite much research on concurrent programming languages, especially
    > for Java and C/C++, we still do not have a satisfactory definition of
    > their semantics, one that admits all common optimisations without also
    > admitting undesired behaviour. Especially problematic are the
    > ``thin-air’’ examples involving high-performance concurrent accesses,
    > such as C/C++11 relaxed atomics. The C/C++11 model is in
    > a per-candidate-execution style, and previous work has identified
    > a tension between that and the fact that compiler optimisations do not
    > operate over single candidate executions in isolation; rather, they
    > operate over syntactic representations that represent all executions.
    >
    > In this paper we propose a novel approach that circumvents this
    > difficulty. We define a concurrency semantics for a core calculus,
    > including relaxed-atomic and non-atomic accesses and locks, that
    > admits a wide range of optimisation while still forbidding the classic
    > thin-air examples. It also addresses other problems relating to
    > undefined behaviour.
    >
    > The basic idea is to use an event-structure representation of the
    > current state of each thread, capturing all of its potential
    > executions, and to permit interleaving of execution and transformation
    > steps over that to reflect optimisation (possibly dynamic) of the
    > code. These are combined with a non-multi-copy-atomic storage
    > subsystem, to reflect common hardware behaviour.
    >
    > The semantics is defined in a mechanised and executable form, and
    > designed to be implementable above current relaxed hardware and
    > strong enough to support the programming idioms that C/C++11 does
    > for this fragment. It offers a potential way forward for concurrent
    > programming language semantics, beyond the current C/C++11 and Java
    > models.

* **Abstracting Gradual Typing**  
  by Ronald Garcia, Alison M. Clark, Éric Tanter  

    > Language researchers and designers have extended a wide variety of
    > type systems to support gradual typing, which enables languages to
    > seamlessly combine dynamic and static checking. These efforts
    > consistently demonstrate that designing a satisfactory gradual
    > counterpart to a static type system is challenging, and this challenge
    > only increases with the sophistication of the type system. Gradual
    > type system designers need more formal tools to help them
    > conceptualize, structure, and evaluate their designs. In this paper,
    > we propose a new formal foundation for gradual typing, drawing on
    > principles from abstract interpretation to give gradual types
    > a semantics in terms of pre-existing static types. Abstracting Gradual
    > Typing (AGT for short) yields a formal account of consistency—one of
    > the cornerstones of the gradual typing approach—that subsumes existing
    > notions of consistency, which were developed through intuition and ad
    > hoc reasoning. Given a syntax-directed static typing judgment, the AGT
    > approach induces a corresponding gradual typing judgment. Then the
    > subject-reduction proof for the underlying static discipline induces
    > a dynamic semantics for gradual programs defined over source-language
    > typing derivations. The AGT approach does not recourse to an
    > externally justified cast calculus: instead, run-time checks naturally
    > arise by deducing evidence for consistent judgments during
    > proof-reduction. To illustrate our approach, we develop novel
    > gradually-typed counterparts for two languages: one with record
    > subtyping and one with information-flow security types. Gradual
    > languages designed with the AGT approach satisfy, by construction, the
    > refined criteria for gradual typing set forth by Siek and colleagues.

* **Abstraction Refinement Guided by a Learnt Probabilistic Model**  
  by Radu Grigore, Hongseok Yang  

    > The core challenge in designing an effective static program analysis
    > is to find a good program abstraction – one that retains only details
    > relevant to a given query. In this paper, we present a new approach
    > for automatically finding such an abstraction, by using guidance from
    > a probabilistic model, which itself is tuned by observing prior runs
    > of the analysis. Our approach applies to parametric static analyses
    > implemented in Datalog, and is based on counterexample-guided
    > abstraction refinement. For each untried abstraction, our
    > probabilistic model provides a probability of success, while the size
    > of the abstraction provides an estimate of its cost in terms of
    > analysis time. Combining these two metrics, probability and cost, our
    > refinement algorithm picks an optimal abstraction. Our probabilistic
    > model is a variant of the Erdos–Renyi random graph model, and it is
    > tunable by what we call hyperparameters. We present a method to learn
    > good values for these hyperparameters, by observing past runs of the
    > analysis on an existing codebase. We implemented our approach on an
    > object-sensitive pointer analysis for Java programs with two client
    > analyses (PolySite and Downcast). Experiments show the benefits of our
    > approach on reducing the runtime of the analysis.

* **Algorithmic Analysis of Qualitative and Quantitative Termination Problems for Affine Probabilistic Programs**  
  by Krishnendu Chatterjee, Hongfei Fu, Rouzbeh Hasheminezhad, Petr Novotny  

    > We consider termination of probabilistic programs with real-valued
    > variables. The relevant probabilistic termination questions are as
    > follows: (1) qualitative questions that ask whether (a) the program
    > terminates with probability 1 (almost-sure termination), (b) the
    > expected termination time is finite (finite termination); (2)
    > quantitative questions that ask to (a) approximate the expected
    > termination time (expectation problem), (b) approximate the
    > probability to terminate in a given number of steps
    > (probabilistic problem), (c) compute a bound $B$ such that the
    > probability to terminate after $B$ steps decreases exponentially
    > (concentration problem). The notion of ranking supermartingales is
    > a powerful approach to establish termination for probablistic
    > programs. In this work we consider algorithmic questions related
    > probabilistic termination, and since our focus is algorithms we
    > consider the simplest class of ranking supermartingales, namely linear
    > ranking supermartingales. We consider the class of affine
    > probabilistic programs (APPs) for which linear ranking
    > supermartingales exist and refer the subclass as LRAPPs.
    >
    > Our main results for LRAPPs are as follows: First, we show that the
    > qualitative problems (i) can be answered for probabilistic programs
    > with demonic nondeterminism in polynomial time, (ii) are NP-hard for
    > programs with angelic nondeterminism, and (iii) can be solved in
    > PSPACE for probabilistic programs with both angelic and demonic
    > nondeterminism. Second, we show that the concentration problem can be
    > solved in the same complexity as for the qualitative
    > problems. Finally, we establish complexity results for the expectation
    > and probabilistic problems. For both the problems we show
    > PSPACE-hardness even for deterministic programs, and that the problems
    > for probabilistic programs with both types of nondeterminism can be
    > solved in 2EXPTIME. We present experimental results to show the
    > effectiveness of our approach to answer the qualitative and
    > quantitative questions on probabilistic programs with demonic
    > nondeterminism.

* **Algorithms for Algebraic Path Properties in Concurrent Systems of Constant Treewidth Components**  
  by Krishnendu Chatterjee, Rasmus Ibsen-Jensen, Andreas Pavlogiannis  

    > We study algorithmic questions for concurrent systems where the
    > transitions are labeled from a complete, closed semiring, and path
    > properties are algebraic with semiring operations. The algebraic
    > path properties can model dataflow analysis problems, the shortest
    > path problem, and many other natural properties that arise in
    > program analysis. We consider that each component of the concurrent
    > system is a graph with constant treewidth, and it is known that the
    > controlflow graphs of most programs have constant treewidth. We
    > allow for multiple possible queries, which arise naturally in demand
    > driven dataflow analysis problems (e.g., alias analysis). The study
    > of multiple queries allows us to consider the tradeoff between the
    > resource usage of the \emph{one-time} preprocessing and for
    > \emph{each individual} query. The traditional approaches construct
    > the product graph of all components and apply the best-known graph
    > algorithm on the product. In the traditional approach, even the
    > answer to a single query requires the transitive closure computation
    > (i.e., the results of all possible queries), which provides no room
    > for tradeoff between preprocessing and query time.\r\n\r\nOur main
    > contributions are algorithms that significantly improve the
    > worst-case running time of the traditional approach, and provide
    > various tradeoffs depending on the number of queries. For example,
    > in a concurrent system of two components, the traditional approach
    > requires hexic time in the worst case for answering one query as
    > well as computing the transitive closure, whereas we show that with
    > one-time preprocessing in almost cubic time, each subsequent query
    > can be answered in at most linear time, and even the transitive
    > closure can be computed in almost quartic time. Furthermore, we
    > establish conditional optimality results that show that the
    > worst-case running times of our algorithms cannot be improved
    > without achieving major breakthroughs in graph algorithms (such as
    > improving the worst-case bounds for the shortest path problem in
    > general graphs whose current best-known bound has not been improved
    > in five decades). Finally, we provide a prototype implementation of
    > our algorithms which significantly outperforms the existing
    > algorithmic methods on several benchmarks.

* **Binding as Sets of Scopes**  
  by Matthew Flatt  

* **Breaking Through the Normalization Barrier: A Self-Interpreter for F-omega**  
  by Matt Brown, Jens Palsberg  

* **Casper: An Efficient Approach to Call Trace Collection**  
  by rongxin wu, Xiao Xiao, Shing-Chi Cheung, Hongyu Zhang, Charles Zhang  

* **Certified Causally Consistent Distributed Key-Value Stores**  
  by Mohsen Lesani, Christian J. Bell, Adam Chlipala  

* **Combining Static Analysis with Probabilistic Models to Enable Market-Scale Analysis**  
  by Damien Octeau, Somesh Jha, Matthew Dering, Patrick McDaniel, Alexandre Bartel, Hongyu Li, Jacques Klein, Yves Le Traon  

* **Decidability of Inferring Inductive Invariants**  
  by Oded Padon, Neil Immermal, Sharon Shoham, Aleksandr Karbyshev, Mooly Sagiv  

* **Dependent Types and Multi-Monadic Effects in F***  
  ([paper website](https://www.fstar-lang.org/papers/mumon/)) ([preprint](https://www.fstar-lang.org/papers/mumon/paper.pdf))  
  by Nikhil Swamy, Cătălin Hriţcu, Chantal Keller, Aseem Rastogi, Antoine Delignat-Lavaud, Simon Forest, Karthikeyan Bhargavan, Cedric Fournet, Pierre-Yves Strub, Markulf Kohlweiss, Jean-Karim Zinzindohoue, Santiago Zanella-Beguelin  

* **Effects as sessions, sessions as effects**  
  by Dominic Orchard, Nobuko Yoshida  

* **Environmental Bisimulations for Probabilistic Higher-Order Languages**  
  by Davide Sangiorgi, Valeria Vignudelli  

* **Estimating types in binaries using predictive modeling**  
  by Omer Katz, Ran El-Yaniv, Eran Yahav  

* **Example-Directed Synthesis: A Type-Theoretic Interpretation**  
  by Jonathan Frankle, Peter-Michael Osera, David Walker, Steve Zdancewic  

* **Fabular: Regression Formulas as Probabilistic Programming**  
  by Johannes Borgstrom, Andrew D. Gordon, Long Ouyang, Claudio Russo, Adam Scibior, Marcin Szymczak  

* **From MinX to MinC: Semantics-Driven Decompilation of Recursive Datatypes**  
  by Ed Robbins, Andy King, Tom Schrijvers  

* **Fully-Abstract Compilation by Approximate Back-Translation**  
  by Dominique Devriese, Marco Patrignani, Frank Piessens  

* **Is Sound Gradual Typing Dead?**  
  by Asumu Takikawa, Daniel Feltey, Ben Greenman, Max New, Jan Vitek, Matthias Felleisen  

* **Kleenex: Compiling Nondeterministic Transducers to Deterministic Streaming Transducers**  
  by Bjørn Bugge Grathwohl, Fritz Henglein, Ulrik Terp Rasmussen, Kristoffer Aalund Søholm, Sebastian Paaske Tørholm  

* **Lattice-Theoretic Progress Measures and Coalgebraic Model Checking**  
  by Ichiro Hasuo, Shunsuke Shimizu, Corina Cirstea  

* **Learning Invariants using Decision Trees and Implication Counterexamples**  
  by Pranav Garg, Daniel Neider, P. Madhusudan, Dan Roth  

* **Lightweight Verification of Separate Compilation**  
  by Jeehoon Kang, Yoonseung Kim, Chung-Kil Hur, Derek Dreyer, Viktor Vafeiadis  

* **Maximal Specification Synthesis**  
  by Aws Albarghouthi, Isil Dillig, Arie Gurfinkel  

* **Memoryful Geometry of Interaction II: Recursion and Adequacy**  
  by Koko Muroya, Naohiko Hoshino, Ichiro Hasuo  

* **Model Checking for Symbolic-Heap Separation Logic with Inductive Predicates**  
  by James Brotherston, Nikos Gorogiannis, Max Kanovich, Reuben Rowe  

* **Modelling the ARMv8 Architecture, Operationally: Concurrency and ISA**  
  by Shaked Flur, Kathryn E. Gray, Christopher Pulte, Susmit Sarkar, Luc Maranget, Ali Sezgin, Will Deacon, Peter Sewell  

* **Monitors and Blame Assignment for Higher-Order Session Types**  
  by Limin Jia, Hannah Gommerstadt, Frank Pfenning  

* **Newtonian Program Analysis via Tensor Product**  
  by Thomas Reps, Emma Turetsky, Prathmesh Prabhu  

* **Optimizing Synthesis with Metasketches**  
  by James Bornholt, Emina Torlak, Dan Grossman, Luis Ceze  

* **Overhauling SC atomics in C11 and OpenCL**  
  by John Wickerson, Mark Batty, Alastair Donaldson  

* **PSync: a partially synchronous language for fault-tolerant distributed algorithms**  
  by Cezara Drăgoi, Thomas A. Henzinger, Damien Zufferey  

* **PolyCheck: Dynamic Verification of Iteration Space Transformations on Affine Programs**  
  by Wenlei Bao, Sriram Krishnamoorthy, Louis-Noel Pouchet, Fabrice Rastello, P. (Saday) Sadayappan  

* **Principal Type Inference for GADTs**  
  by Sheng Chen, Martin Erwig  

* **Printing Floating-Point Numbers: A Faster, Always Correct Method**  
  by Marc Andrysco, Ranjit Jhala, Sorin Lerner  

* **Program Synthesis with Noise**  
  by Veselin Raychev, Pavol Bielik, Martin Vechev, Andreas Krause  

* **Prophet: Automatic Patch Generation via Learning from Successful Patches**  
  by Fan Long, Martin Rinard  

* **Pushdown Control-flow Analysis for Free**  
  by Thomas Gilray, Steven Lyde, Michael D. Adams, Matthew Might, David Van Horn  

* **Query-Guided Maximum Satisfiability**  
  by Xin Zhang, Ravi Mangal, Aditya Nori, Mayur Naik  

* **Reducing Crash Recoverability to Reachability**  
  by Eric Koskinen, Junfeng Yang  

* **SMO: An Integrated Approach to Intra-Array and Inter-Array Storage Optimization**  
  by Somashekaracharya G Bhaskaracharya, Uday Bondhugula, Albert Cohen  

* **Satisfiability Modulo Differential Equivalence Relations**  
  by Luca Cardelli, Mirco Tribastone, Max Tschaikowski, Andrea Vandin  

* **Scaling Network Verification using Symmetry and Surgery**  
  by Gordon Plotkin, Nikolaj Bjørner, Nuno P. Lopes, Andrey Rybalchenko, George Varghese  

* **Sound Type-dependent Syntactic Language Extension**  
  ([preprint](http://erdweg.org/publications/soundx-popl16.pdf))  
  by Florian Lorenzen, Sebastian Erdweg  

* **String Solving with Word Equations and Transducers: Decidability and Applications to Detecting Mutation XSS**  
  by Anthony Widjaja Lin, Pablo Barcelo  

* **Symbolic Abstract Data Type Inference**  
  by Michael Emmi, Constantin Enea  

* **System Fω with Equirecursive Types for Datatype-generic Programming**  
  by Yufei Cai, Paolo G. Giarrusso, Klaus Ostermann  

* **Taming Release-Acquire Consistency**  
  by Ori Lahav, Nick Giannarakis, Viktor Vafeiadis  

* **Temporal Verification of Higher-order Functional Programs**  
  by Akihiro Murase, Tachio Terauchi, Naoki Kobayashi, Ryosuke Sato, Hiroshi Unno  

* **The Complexity of Interaction**  
  by Stéphane Gimenez, Georg Moser  

* **The Gradualizer: a methodology and algorithm for generating gradual type systems**  
  by Matteo Cimini, Jeremy Siek  

* **The Hardness of Data Packing**  
  by Rahman Lavaee, Chen Ding  

* **Transforming Spreadsheet Data Types using Examples**  
  by Rishabh Singh, Sumit Gulwani  

* **Type Theory in Type Theory using Quotient Inductive Types**  
  by Thorsten Altenkirch, Ambrus Kaposi  

* **Unboundedness and Downward Closures of Higher-Order Pushdown Automata**  
  by Matthew Hague, Jonathan Kochems, C.-H. Luke Ong  
