# Objectives

- Explore the world of programming languages.
- Understand the core concepts that define languages and their families.
- Learn about both familiar and novel programming paradigms.
- Blend theory and practice:
  - Semantics and type systems
  - Program analysis and formal verification
- Dive into powerful features like:
  - Higher-order functions
  - Continuations
  - Monads

---

## Course Prerequisites

- **Theory:**  
  - First-order logic and induction in discrete mathematics
- **Programming:**  
  - Strong programming skills
  - Openness to learning new programming paradigms and tools

---

## Course Takeaways

- Gain a deep appreciation for programming languages as a technical discipline.
- Understand the culture, challenges, and values behind language design.
- Become a more effective programmer by learning to:
  - Systematically evaluate and use programming tools.
  - Anticipate the future of software development.
- Explore key modern languages and active research topics.
- Build a strong foundation for academic or industrial research.

---

# Goals of Programming Languages

- Programming languages aim to balance three key goals:
  - **Productivity**: Easier, faster development (e.g., Python, Haskell, C#, F#)
  - **Safety**: Prevent errors and ensure correctness (e.g., Java, Rust)
  - **Performance**: Maximize speed and efficiency (e.g., C, Rust)
- Different designs prioritize these goals in unique ways, leading to diverse ecosystems.

---

## Software Complexity and Challenges
- **Complex ecosystems**:  
  - From individual languages to entire systems.
- **Developers spend more time reading code than writing it.**
  - Studies show that program comprehension dominates development time.
  - Developers primarily focus on understanding and debugging, not writing.
- **Hardware advances are outpacing software adaptation.**
  - Significant gaps in performance utilization exist.
- **Memory usage has exploded.**
  - Applications demand more resources than ever before.
- **Bugs remain a persistent issue.**
  - Bugs and inefficiencies are stubborn problems.
    - Memory-related vulnerabilities are still a leading cause of security flaws.

---

## 🤔 Do you know in what languages they are written?
- All the programs below print "Hello World!"

- Program 1: 

```plaintext
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>++.>+.+++++++..+++.<<++.>+++++++++++++++.>.+++.------.--------.<<+.<.
```

- Program 2: 

```plaintext
"!dlrow olleH">:#,_@
```

- Program 3: 

```plaintext
DO ,1 <- #13
DO ,1 SUB #1 <- #238
DO ,1 SUB #2 <- #108
DO ,1 SUB #3 <- #112
DO ,1 SUB #4 <- #0
DO ,1 SUB #5 <- #64
DO ,1 SUB #6 <- #194
DO ,1 SUB #7 <- #48
DO ,1 SUB #8 <- #22
DO ,1 SUB #9 <- #248
DO ,1 SUB #10 <- #168
DO ,1 SUB #11 <- #24
DO ,1 SUB #12 <- #16
DO ,1 SUB #13 <- #162
DO READ OUT ,1
DO GIVE UP
```

- Program 4: 
  - `[S]` = Space
  - `[T]` = Tab
  - `[N]` = Newline 

```plaintext
[S][T][S][S]  (Push H ASCII code: 72)
[T][S]       (Output character)
[S][T][S][S]  (Push e ASCII code: 101)
[T][S]       (Output character)
[S][T][S][S]  (Push l ASCII code: 108)
[T][S]       (Output character)
[S][T][S][S]  (Push l ASCII code: 108)
[T][S]       (Output character)
[S][T][S][S]  (Push o ASCII code: 111)
[T][S]       (Output character)
[S][T][S][S]  (Push , ASCII code: 44)
[T][S]       (Output character)
[S][T][S][S]  (Push space ASCII code: 32)
[T][S]       (Output character)
[S][T][S][S]  (Push W ASCII code: 87)
[T][S]       (Output character)
[S][T][S][S]  (Push o ASCII code: 111)
[T][S]       (Output character)
[S][T][S][S]  (Push r ASCII code: 114)
[T][S]       (Output character)
[S][T][S][S]  (Push l ASCII code: 108)
[T][S]       (Output character)
[S][T][S][S]  (Push d ASCII code: 100)
[T][S]       (Output character)
[S][T][S][S]  (Push ! ASCII code: 33)
[T][S]       (Output character)
```

- Program 5:

```plaintext
('&%:9]!~}|z2Vxwv-,POqponl$Hjig%eB@@>}=<M:9wv6WsU2T|nm-,jcL(I&%$#"
`CB]V?Tx<uVtT`Rpo3NlF.Jh++FdbCBA@?]!~|4XzyTT43Qsqq(Lnmkj"Fhg${z@>
```

---

### Esolangs (esoteric programming languages)

| **Program** | **Esolang**   | **Notable Feature**                                    | **Purpose**                            |
|--|---------------|--------------------------------------------------------|----------------------------------------|
| 1 | **Brainfuck** | Minimalism and Turing-completeness                     | Challenge programming skills.          |
| 2 | **Befunge**   | Two-dimensional program flow                           | Explore unconventional execution.      |
| 3 | **INTERCAL**  | Absurdity and politeness                               | Parody of conventional programming.    |
| 4 | **Whitespace**| Invisible syntax using spaces, tabs, and newlines      | Humor and obfuscation.                 |
| 5 | **Malbolge**  | Extreme difficulty and self-modifying code             | Challenge and frustration.             |

---

## 🔭 Explore 
- [esoteric programming languages](https://esolangs.org/wiki/Main_Page)

---

## 📝 [Esolang Interpreters](https://github.com/bangyen/esolangs)
- [Brainfuck](https://github.com/rdebath/Brainfuck)
  - [online](https://copy.sh/brainfuck/)
- [Befunge](https://therenegadecoder.com/code/hello-world-in-befunge/)
- [INTERCAL](http://www.catb.org/~esr/intercal/)
- [Whitespace](https://en.wikipedia.org/wiki/Whitespace_(programming_language))
- [Malbolge](https://malbolge.doleczek.pl/)

---

# The Big Picture of Programming Languages

- **Pioneers in Computing:**
  - Alan Turing: 
    - The `Turing Machine`: a sequential state-based model of computation.
    - `Turing` Languages
  - Alonzo Church: 
    - [Lambda Calculus](https://en.wikipedia.org/wiki/Programming_language_theory): a functional, mathematical abstraction of computation.
    - `Church` Languages
- Computability: `Turing Completeness`
  - Both paradigms are Turing-complete, meaning any computation expressible in one can be expressed in the other.
  - A Turing Machine can simulate lambda calculus and vice versa.

---

## Turing Languages vs. Church Languages

| Aspect     | **Turing Languages**      | **Church Languages**   |
|--------------------|---------------|--------------------------|
| **Foundation**     |  **Turing Machine**,  |  **lambda calculus**,  |
| **Focus**          | step-by-step manipulation of memory (imperative). |  transformations and evaluation of expressions (functional). |
| **Execution Model**| Sequence of instructions, often manipulating a global state. | Function application, substitution, and evaluation. |
| **Paradigm**       | Imperative      | Functional      |
| **Strengths**   | Performance, hardware-level control    | Simplicity, mathematical rigor    |
| **Weaknesses**   | Complexity in state management   | Less intuitive for sequential operations|
| **Use Cases**    | System programming, general software   | Academic research, parallel computing   |

---

## 🍎 Language Examples
- Turing languages

```plaintext
           Turing Machine
                 |
         Assembly Language
                /  \
      Fortran   COBOL   Algol
         |        |       |
      Pascal     C       Smalltalk
        |         \       /   \
     Python       C++   Java  Objective-C
         \          |      |       |
       JavaScript   Rust   C#     Swift
```

- Church languages

```plaintext
         Lambda Calculus
               |
          ----------------
          |              |
        LISP           ISWIM
          |              |
       Scheme            ML
        |         ----------- 
    Haskell       |         |
       |        OCaml      SML
    Clojure      |         
           Functional Hybrids
             (Scala, F#, Kotlin, Elm)
```

---

## 🔭 Explore [Computer Languages History](https://www.levenez.com/lang/)

---

## [Programming paradigms](https://en.wikipedia.org/wiki/Programming_paradigm)

| **Paradigm**   | **Description**    | **Key Features** | **Examples**  | **Applications**     |
|---------|---------|-----------|-----------|--------------|
| **Imperative**         | Focuses on describing *how* a program operates through step-by-step instructions.                       | Mutable state, loops, conditionals, sequential execution.                       | C, Python, Java           | System programming, general-purpose. |
| **`Functional`**         | Based on mathematical `functions and immutability`, emphasizing *what* to compute.                        | First-class functions, immutability, recursion, lazy evaluation.                | Haskell, Lisp, Scheme     | AI, academic research, data analysis.|
| **Object-Oriented**    | Organizes code around objects that encapsulate state and behavior, promoting modularity.                 | Classes, inheritance, polymorphism, encapsulation.                              | C++, Java, Python         | GUI apps, enterprise software.       |
| **`Logic`**             | Focuses on facts, rules, and logical inference to solve problems `declaratively`.                         | Facts, rules, queries, backtracking.                                            | Prolog, CLIPS             | AI, expert systems, knowledge bases. |
| **Declarative**        | Focuses on describing *what* the outcome should be, without specifying *how* to achieve it.             | High-level abstractions, limited control flow constructs.                       | SQL, HTML, XSLT           | Databases, web development.          |
| **Procedural**         | A subset of imperative programming focusing on the use of procedures (functions).                       | Functions, modularization, parameter passing.                                   | C, Pascal, Ada            | Education, embedded systems.         |
| **Event-Driven**       | Executes code in response to external events, commonly used in interactive systems.                     | Event loops, callbacks, asynchronous execution.                                 | JavaScript, Visual Basic  | GUI apps, web development.           |
| **`Concurrent`**         | Focuses on executing multiple tasks simultaneously, often for performance.                             | Threads, message passing, synchronization.                                      | Go, Erlang, Rust          | Distributed systems, networking.     |
| **Scripting**          | Emphasizes ease of use, rapid prototyping, and automation, often interpreted.                          | Dynamic typing, minimal boilerplate, integration with other tools.              | Python, Ruby, Bash        | Automation, web development.         |
| **Reactive**           | Handles asynchronous data streams and event-driven programming in a declarative style.                 | Observables, data streams, asynchronous programming.                            | RxJS, Elm, Dart           | Front-end development, real-time apps.|
| **`Multi-Paradigm`**     | Combines features of multiple paradigms, offering flexibility for developers.                          | Hybrid features, support for imperative, functional, and OO styles.            | Python, Scala, Kotlin     | Versatile, general-purpose.          |


---

# Forces Driving Change

- **Security**:  
  - Software now underpins critical systems, making reliability paramount.
- **Hardware Evolution**:  
  - New architectures demand innovative software designs.
- **Programmer Shortage**:  
  - Automation and better tools are crucial to addressing this gap.

---

## Future Directions in Programming

- **Beyond Turing Languages**:  
  - Expanding beyond traditional computation models.
- **Automation of Programming**:  
  - Tools that write, verify, or optimize code autonomously.
- **Software Verification**:  
  - Ensuring correctness and safety through advanced techniques.

---

## More Productivity, Safety, and Performance

- **Productivity**:  
  - `Declarative and functional programming` simplify common patterns.
  - Example: Transforming iterative logic into reusable functions.
- **Safety**:  
  - Type systems in languages like Rust eliminate many runtime errors.
  - Real-world results: Significantly fewer bugs and faster refactoring.
- **Performance**:  
  - Leverage efficient abstractions without sacrificing speed.

---

# Summary: The Changing World of Software

- Software is evolving, driven by:
  - New ideas in programming languages.
  - Hardware advancements.
  - Increasing demands for security and reliability.
- In this course, you’ll learn:
  - The principles shaping the next generation of programming.
  - How to think critically about tools and techniques in the evolving landscape.