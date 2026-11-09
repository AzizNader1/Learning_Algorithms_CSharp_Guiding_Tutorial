# Algorithms in C# — The Complete Journey from Absolute Zero to Mastery

> A complete, step-by-step, chapter-by-chapter, line-by-line, word-by-word guided tutorial for understanding, designing, implementing, proving, testing, measuring, and mastering algorithms in C# — starting from zero assumed knowledge and ending with a full working application.

---

## Welcome — Read This First

This guide assumes you may know **little or nothing** about algorithms, and possibly little about C# itself. That is completely fine. This book was written exactly for that starting point.

You will begin with the question *"What is an algorithm, actually?"* — answered in plain everyday language, with no code at all. You will then learn where algorithms came from (history), what they give you (value), and why you should care (motivation). Only after the ideas are solid do we open the C# toolbox and build everything from the first line upward.

Every important piece of code in this guide is explained three ways:

1. **Line by line** — what each line of code does.
2. **Word by word** — what each *word inside a line* means, especially the first time a C# keyword appears.
3. **Trace** — a step-by-step table showing the state of the algorithm while it runs on real input.

Each chapter builds on the previous one. Nothing is used before it has been taught. When a concept reappears, the guide points back to the chapter where it was introduced.

The final destination is a complete, working **Algorithm Lab** console application that reads numerical data from a CSV file, validates it, calculates descriptive statistics (count, minimum, maximum, mean, median, standard deviation), sorts and searches the data, detects outliers, and prints an analytical report — followed by the professional skills that surround real algorithm work: testing, benchmarking, debugging, and design judgment.

---

## How to Use This Guide

### The correct order of learning

Always follow this order, for every problem you ever meet:

1. **Understand the problem.** Restate it in your own words.
2. **Write examples.** Small input → expected output, by hand.
3. **Define inputs and outputs.** A written contract.
4. **Write a simple solution in plain language.** Pseudocode.
5. **Implement the simple solution.** Real C# code.
6. **Prove or test that it is correct.** Invariants and tests.
7. **Measure its performance.** Complexity analysis, then benchmarks.
8. **Improve it only when improvement is justified.** Never optimize blindly.

Do not begin with a famous algorithm just because you have heard its name. First understand the *problem* the algorithm solves. An algorithm without a problem is an answer without a question.

### What to do with every code example

For each code block in this guide:

- read it once **without** typing it;
- **predict** the output before running;
- **type it yourself** — never copy-paste while learning;
- **run it**;
- **change the input** and predict again;
- **test an empty input** (an empty array, an empty string);
- **test one item**;
- **test duplicate values**;
- **test the largest or smallest meaningful input**;
- **explain the algorithm in your own words** — out loud, or in a comment.

Typing and breaking the code is where learning happens. Reading alone creates the *illusion* of knowledge.

### How the word-by-word explanations work

The first time a C# construct appears (for example the keyword `static`, or the type `int[]`), it is explained word by word in a dedicated table or list. Later chapters reuse that construct freely and refer back to the chapter where it was first taught. If you ever feel lost on a keyword, search upward — its full explanation exists exactly once, near its first use.

### What mastery means

Algorithmic mastery means you can:

- **recognize the shape of a problem** (counting? searching? ordering? connecting?);
- **choose an appropriate data structure** for that shape;
- **express a solution with pseudocode** before typing;
- **prove why the solution works** with an invariant;
- **estimate time and memory usage** before running anything;
- **implement the solution clearly in C#**;
- **test edge cases** systematically;
- **compare alternative solutions** with concrete numbers;
- **identify when a simpler algorithm is better**;
- **explain trade-offs to another developer** in plain language.

This entire book is the construction manual for that list.

---

## Table of Contents

**Part I — Foundations: Thinking Before Code**

1. [Chapter 1: What Is an Algorithm?](#chapter-1-what-is-an-algorithm)
2. [Chapter 2: A Short History of Algorithms](#chapter-2-a-short-history-of-algorithms)
3. [Chapter 3: What Algorithms Provide You](#chapter-3-what-algorithms-provide-you)
4. [Chapter 4: The Mindset of an Algorithmic Thinker](#chapter-4-the-mindset-of-an-algorithmic-thinker)

**Part II — The C# Laboratory from Zero**

5. [Chapter 5: Setting Up Your Tools](#chapter-5-setting-up-your-tools)
6. [Chapter 6: C# Building Blocks Word by Word](#chapter-6-c-building-blocks-word-by-word)
7. [Chapter 7: Control Flow Loops and Decisions](#chapter-7-control-flow-loops-and-decisions)
8. [Chapter 8: Your First Complete Algorithm in C#](#chapter-8-your-first-complete-algorithm-in-c)

**Part III — The Method: Describe Before You Code**

9. [Chapter 9: Requirements Are Not Algorithms](#chapter-9-requirements-are-not-algorithms)
10. [Chapter 10: Pseudocode and State Traces](#chapter-10-pseudocode-and-state-traces)
11. [Chapter 11: From Idea to Code the Disciplined Path](#chapter-11-from-idea-to-code-the-disciplined-path)

**Part IV — Correctness and Efficiency**

12. [Chapter 12: Correctness Invariants and Proof](#chapter-12-correctness-invariants-and-proof)
13. [Chapter 13: Measuring Efficiency Big O from Zero](#chapter-13-measuring-efficiency-big-o-from-zero)

**Part V — Core Patterns with Arrays and Strings**

14. [Chapter 14: Fundamental Patterns](#chapter-14-fundamental-patterns)

**Part VI — Searching Algorithms**

15. [Chapter 15: Linear Search](#chapter-15-linear-search)
16. [Chapter 16: Binary Search](#chapter-16-binary-search)
17. [Chapter 17: Beyond Basic Search](#chapter-17-beyond-basic-search)

**Part VII — Sorting Algorithms**

18. [Chapter 18: Why Sorting Helps](#chapter-18-why-sorting-helps)
19. [Chapter 19: Selection Sort](#chapter-19-selection-sort)
20. [Chapter 20: Insertion Sort](#chapter-20-insertion-sort)
21. [Chapter 21: Merge Sort](#chapter-21-merge-sort)
22. [Chapter 22: Quicksort](#chapter-22-quicksort)
23. [Chapter 23: Stability Built-ins and Choosing a Sort](#chapter-23-stability-built-ins-and-choosing-a-sort)

**Part VIII — Hashing Maps and Sets**

24. [Chapter 24: The Hash Idea from Zero](#chapter-24-the-hash-idea-from-zero)
25. [Chapter 25: Hashing in Action](#chapter-25-hashing-in-action)

**Part IX — Stacks Queues and Linked Lists**

26. [Chapter 26: The Stack](#chapter-26-the-stack)
27. [Chapter 27: The Queue](#chapter-27-the-queue)
28. [Chapter 28: Parentheses Validation](#chapter-28-parentheses-validation)
29. [Chapter 29: Linked Lists](#chapter-29-linked-lists)

**Part X — Recursion and Backtracking**

30. [Chapter 30: Recursion from Zero](#chapter-30-recursion-from-zero)
31. [Chapter 31: Backtracking](#chapter-31-backtracking)
32. [Chapter 32: Pruning](#chapter-32-pruning)

**Part XI — Divide and Conquer**

33. [Chapter 33: Divide and Conquer](#chapter-33-divide-and-conquer)

**Part XII — Trees Heaps and Priority Queues**

34. [Chapter 34: Trees from Zero](#chapter-34-trees-from-zero)
35. [Chapter 35: Binary Search Trees](#chapter-35-binary-search-trees)
36. [Chapter 36: Heaps and Priority Queues](#chapter-36-heaps-and-priority-queues)

**Part XIII — Graph Algorithms**

37. [Chapter 37: Graphs from Zero](#chapter-37-graphs-from-zero)
38. [Chapter 38: Breadth-First Search](#chapter-38-breadth-first-search)
39. [Chapter 39: Depth-First Search](#chapter-39-depth-first-search)
40. [Chapter 40: Topological Sorting](#chapter-40-topological-sorting)
41. [Chapter 41: Shortest Paths and Minimum Spanning Trees](#chapter-41-shortest-paths-and-minimum-spanning-trees)

**Part XIV — Greedy Algorithms and Dynamic Programming**

42. [Chapter 42: Greedy Algorithms](#chapter-42-greedy-algorithms)
43. [Chapter 43: Dynamic Programming](#chapter-43-dynamic-programming)

**Part XV — String and Text Algorithms**

44. [Chapter 44: Working with Text](#chapter-44-working-with-text)

**Part XVI — Algorithms for Data Analysis**

45. [Chapter 45: Statistics as Algorithms](#chapter-45-statistics-as-algorithms)

**Part XVII — Building the Algorithm Lab**

46. [Chapter 46: Project Setup and Structure](#chapter-46-project-setup-and-structure)
47. [Chapter 47: The Model](#chapter-47-the-model)
48. [Chapter 48: The CSV Reader](#chapter-48-the-csv-reader)
49. [Chapter 49: The Search Algorithms File](#chapter-49-the-search-algorithms-file)
50. [Chapter 50: The Sort Algorithms File](#chapter-50-the-sort-algorithms-file)
51. [Chapter 51: The Statistics Algorithms File](#chapter-51-the-statistics-algorithms-file)
52. [Chapter 52: The Program Entry Point](#chapter-52-the-program-entry-point)
53. [Chapter 53: Data Running and Manual Testing](#chapter-53-data-running-and-manual-testing)

**Part XVIII — Testing Benchmarking and Debugging**

54. [Chapter 54: Testing Algorithm Contracts](#chapter-54-testing-algorithm-contracts)
55. [Chapter 55: Benchmarking Fairly](#chapter-55-benchmarking-fairly)
56. [Chapter 56: Debugging and Common Bugs](#chapter-56-debugging-and-common-bugs)

**Part XIX — Advanced Design and Mastery**

57. [Chapter 57: Designing for Real Workloads](#chapter-57-designing-for-real-workloads)
58. [Chapter 58: The Mastery Path](#chapter-58-the-mastery-path)

**Appendices**

59. [Appendix A: Complexity Reference](#appendix-a-complexity-reference)
60. [Appendix B: Algorithm Vocabulary](#appendix-b-algorithm-vocabulary)
61. [Appendix C: Practice Roadmap](#appendix-c-practice-roadmap)
62. [Appendix D: C# Quick Glossary](#appendix-d-c-quick-glossary)

---

# Part I — Foundations: Thinking Before Code

---

# Chapter 1: What Is an Algorithm?

## 1.1 Starting from absolute zero

Forget computers for a moment. Forget programming entirely.

You are in your kitchen and you want to make a cup of tea. You perform a sequence of steps, in order:

```text
1. fill the kettle with water
2. boil the water
3. put a tea bag in a cup
4. pour the hot water into the cup
5. wait three minutes
6. remove the tea bag
```

Notice what this list of steps has:

- it is **finite** — it ends; you will not make tea forever;
- it is **ordered** — step 4 comes before step 5, and the order matters (pouring before boiling would give you cold tea);
- each step is **unambiguous** — "boil the water" is a clear instruction; nobody must guess what it means;
- it takes **input** — water, a tea bag, a cup, a kettle;
- it produces **output** — a cup of tea.

That list of steps is, in every meaningful sense, an **algorithm**. You have executed algorithms your entire life: a recipe is an algorithm, a driving route is an algorithm, the method you use to find a word in a dictionary is an algorithm. What computer science did was take this everyday idea and make it *precise*.

## 1.2 The formal definition, word by word

Here is the definition used throughout this guide:

> An **algorithm** is a **finite**, **ordered**, **unambiguous** **procedure** that transforms **input** into a desired **output**.

Every single word carries weight. Let us dissect them one at a time, word by word.

| Word | Meaning | Why it matters | What breaks without it |
|---|---|---|---|
| **finite** | The procedure eventually stops after some number of steps. | A computation that never ends delivers nothing. | An instruction like "keep adding 1 forever" never returns an answer. |
| **ordered** | The steps form a sequence; step 3 happens after step 2 and before step 4. | Many procedures only work in one order. | Boiling after pouring produces cold tea. |
| **unambiguous** | Every step can be interpreted in exactly one way by whoever (or whatever) executes it. | A computer cannot guess your intention. | "Sort the numbers somehow" is not executable; "compare and swap adjacent pairs until no swaps remain" is. |
| **procedure** | A description of *actions to perform*, not merely a description of the result you want. | It tells you *how*, not just *what*. | "The list is sorted" is a wish; the procedure is the machine that makes it true. |
| **input** | The information given to the procedure before (or during) its run. | The same procedure works for many different inputs. | A procedure that works for exactly one input is not a general method. |
| **output** | The result produced when the procedure finishes. | The output is the reason the algorithm exists. | Without a defined output, you cannot even tell whether the algorithm succeeded. |

A useful mental model: an algorithm is a **machine in your mind**. You feed data in at the top, gears turn in a determined order, and a result comes out at the bottom.

## 1.3 Your first algorithm — no code at all

Problem: given a list of numbers, find the **maximum** (the largest one).

Before writing any code, think about how *you* do this by hand with, say, a stack of exam papers:

```text
if the list is empty, report that no maximum exists
assume the first number is the maximum
for each remaining number
    if the number is larger than the current maximum
        replace the current maximum
return the current maximum
```

Read those five lines slowly. They already contain real algorithmic thinking:

- **The empty case is handled first.** Of an empty list there is no maximum; silently inventing one (like zero) would be wrong. Professionals handle the empty case *first* — beginners handle it last, or never.
- **"Assume the first number is the maximum"** is an initialization decision. Why is it safe? Because it is an actual member of the list, so any true maximum is at least as large as it.
- **"For each remaining number"** states that every element is examined exactly once — this is the engine of the algorithm.
- **"Replace the current maximum"** is the update rule — the heart of the process.

This five-line text is already a complete, correct, testable algorithm — and it contains **zero code**. Hold onto this feeling: code is only the final clothing of an idea that already exists.

## 1.4 Algorithm versus program versus code

Three related words that beginners often blur together:

- The **algorithm** is the *idea*: the finite, ordered, unambiguous procedure. It exists independently of any language.
- The **implementation** is that idea expressed in a concrete programming language, such as C#.
- The **program** is the running artifact: implementation plus environment, input, and output.

The same algorithm can be written in many languages. Binary search is one idea; it can be written in C#, Python, Java, or with pencil and paper. This distinction is powerful in both directions:

- If you understand the *algorithm*, you can re-implement it in any language later.
- If you only memorized *syntax*, you will struggle the moment the problem changes shape slightly.

In this guide, every algorithm is first presented as an idea (plain language and pseudocode) and only then as C#.

## 1.5 Algorithm versus data structure

A **data structure** is a way of *organizing* data. An **algorithm** is a way of *processing* data.

| Concept | It answers | Examples |
|---|---|---|
| Data structure | "Where and how is the data stored?" | `int[]` array, `List<T>`, `Dictionary<K,V>`, `HashSet<T>`, `Stack<T>`, tree, graph |
| Algorithm | "What steps transform it into the answer?" | linear search, binary search, merge sort, breadth-first search |

The two are inseparable partners:

- `List<int>` (a data structure) holds numbers; *finding the maximum* (an algorithm) walks through it.
- `Dictionary<string, int>` (a data structure) maps words to counts; *counting word frequencies* is an algorithmic task built on it.
- Binary search (an algorithm) only works at full speed when the data lives in a structure with fast positional access (an array, kept sorted).

A good algorithm usually depends on choosing the right data structure — and choosing the right structure requires imagining which algorithms will run on it. This dance is the core skill this guide trains.

## 1.6 The five questions for every algorithm

Before implementing any algorithm, train yourself to answer these five questions — for the rest of this book and the rest of your career:

1. **What is the input?** — its type, its size, its allowed values.
2. **What is the output?** — its type, and precisely when it counts as correct.
3. **What assumptions are made?** — sorted or unsorted? non-empty? unique? bounded?
4. **How do we know the answer is correct?** — an invariant, an argument, a proof (Chapter 12).
5. **How much time and memory does it need?** — complexity analysis (Chapter 13).

If you cannot answer all five, you are not ready to write code. If you *can* answer all five, the code almost writes itself.

### Exercises for Chapter 1

1. Write the steps of an everyday activity you know (tying shoelaces, boarding a bus) and check them against the six definition words: finite, ordered, unambiguous, procedure, input, output.
2. Identify the input and output of "finding the average of an exam class".
3. Find the ambiguity in this step: "add the numbers". (Which numbers? In what order? To what?)

<details><summary>Solutions</summary>

1. Tying shoelaces: finite (ends with a knot), ordered (cross before looping), unambiguous if written precisely, input = laces, output = a bow. Most everyday instructions fail *unambiguous* first — that is exactly why computers need precise languages.
2. Input: a non-empty list of exam scores. Output: one number, the arithmetic mean, defined as the sum divided by the count.
3. Ambiguities: *which* numbers (all of them? a subset?), added to *what* initial value (zero? something else?), and in *what* order (irrelevant for whole numbers but relevant for floating-point, see Chapter 57).
</details>

---

# Chapter 2: A Short History of Algorithms

Knowing where algorithms came from tells you what they *are*: not a modern software trick, but one of the oldest intellectual tools of humanity.

## 2.1 Ancient procedures — algorithms before computers

Long before any electronic machine, mathematics was written down as **repeatable procedures**, because a procedure can be taught, executed by anyone, and trusted to give the same answer every time.

- **Babylonian tablets (roughly 1800–1600 BCE)** contain step-by-step recipes for solving certain classes of problems — procedures, written to be followed, not just admired.
- **Euclid's algorithm (around 300 BCE)**, from the mathematical tradition of Alexandria, finds the **greatest common divisor** (GCD) of two numbers — the largest integer dividing both. It is arguably the oldest algorithm still in everyday industrial use (it runs inside modern cryptography).

Euclid's procedure, in plain language:

```text
given two positive whole numbers a and b
while b is not zero
    replace the pair (a, b) with the pair (b, remainder of a divided by b)
return a
```

Trace it on `a = 48, b = 18`:

| Step | a | b | remainder of a / b | New pair |
|---:|---:|---:|---:|---|
| 1 | 48 | 18 | 48 = 2×18 + 12 → 12 | (18, 12) |
| 2 | 18 | 12 | 18 = 1×12 + 6 → 6 | (12, 6) |
| 3 | 12 | 6 | 12 = 2×6 + 0 → 0 | (6, 0) |
| 4 | 6 | 0 | stop | answer: 6 |

Indeed, GCD(48, 18) = 6. The algorithm is finite (the second number strictly shrinks each round), ordered, and unambiguous — all definition words from Chapter 1 hold, 23 centuries before C# existed.

- **The sieve of Eratosthenes (around 240 BCE)** finds all prime numbers up to a limit by repeatedly crossing out multiples — again a precise, repeatable procedure.

## 2.2 The origin of the word "algorithm"

The word **algorithm** comes, through Latin and centuries of spelling drift, from the name **Muhammad ibn Musa al-Khwarizmi** (circa 780–850 CE), a Persian mathematician working in the House of Wisdom in Baghdad. His writings described **systematic, step-by-step procedures for arithmetic and algebra** — how to solve entire *classes* of equations by a fixed recipe rather than case-by-case intuition.

The historical lesson matters more than the name: al-Khwarizmi's contribution was the realization that a **calculation can be transformed from an intuitive art into a repeatable method** — a method that gives the right answer *every time*, for *every valid input*, regardless of who executes it. That is exactly the standard we still hold algorithms to today.

(The word *algebra* comes from the title of one of his books, *al-Jabr* — one man's name sits quietly inside two foundational words of computing.)

## 2.3 From hand procedures to machines

The next leap was asking whether a *machine* could execute a procedure.

- **Charles Babbage** (1791–1871) designed general-purpose mechanical computing machines — first the Difference Engine for tabulating calculations, then the far more ambitious Analytical Engine, a design for a programmable mechanical computer a century before electronics.
- **Ada Lovelace** (1815–1852), in her notes on the Analytical Engine, described how such a machine could follow operations on **symbols, not just numbers** — arguably the first published recognition that a procedure could manipulate *anything* representable symbolically, including what we would now call programs and data.
- **Alan Turing** (1912–1954) and contemporaries in the 1930s formalized the question *what can be computed by an effective procedure at all?* The **Turing machine** model gave algorithms a rigorous mathematical definition — and simultaneously proved there are well-defined problems no algorithm can ever solve. Algorithms have *limits*, and we can state them precisely.

This history explains the definition of Chapter 1: every word (finite, ordered, unambiguous) was hardened by a century of asking what procedures a machine can execute *without human judgment*.

## 2.4 Algorithms in modern computing

Modern software is a tower of algorithms. You use thousands of them before lunch:

- **search engines** rank billions of pages against your query;
- **databases** use index structures and query planners to fetch rows;
- **navigation systems** compute shortest routes through road networks (Chapter 41);
- **compression algorithms** shrink the files you send (your images, your video calls);
- **operating systems** schedule which process runs at which millisecond (Chapter 36);
- **machine-learning systems** are optimization algorithms running over data;
- **data-analysis systems** aggregate and summarize information (Chapter 45 and the Algorithm Lab).

The historical lesson: an algorithm is not tied to one programming language or one era. Euclid's procedure has outlived every hardware technology so far — punch cards, vacuum tubes, transistors — and will outlive whatever comes next. When you learn algorithms, you are learning the *permanent* layer of computing.

### Exercises for Chapter 2

1. Run Euclid's algorithm on paper for `a = 252, b = 105`. What is the GCD?
2. Why is the shrinking of `b` important in Euclid's algorithm? Which definition word from Chapter 1 does it protect?

<details><summary>Solutions</summary>

1. 252 = 2×105 + 42 → (105, 42); 105 = 2×42 + 21 → (42, 21); 42 = 2×21 + 0 → (21, 0). **GCD = 21**.
2. `b` strictly decreases (each new `b` is a remainder, therefore smaller than the old `b`) and can never go below zero, so the loop must end after finitely many steps. This protects **finite** — termination — the first word of the definition.
</details>

---

# Chapter 3: What Algorithms Provide You

You now know what an algorithm *is*. The next question is what it *gives you* — the concrete value, in four dimensions.

## 3.1 Correctness — a structure for reasoning

A program can **compile and still be wrong**. The compiler checks syntax, not truth.

An algorithm, written precisely, gives you a structure for *reasoning about correctness* before you trust it. The practical payoff appears the moment a requirement is vague.

Suppose someone asks you: *"find the duplicate in this array."* Before any code, the algorithmic mind asks: what does "duplicate" mean here?

- any value appearing at least twice (there may be many such values);
- the **first** repeated value scanning left to right;
- **all** repeated values;
- duplicates under a **case-insensitive** comparison (if values are strings)?

Different requirements produce **different algorithms** — some returning a boolean, some a value, some a list. Choosing the algorithm before clarifying the requirement is the most common source of wasted work in real teams. The algorithm disciplines you to define the output precisely (the contract idea of Chapter 9).

## 3.2 Performance — the difference between possible and impossible

Two algorithms can both be *correct* and still differ by a factor of a **million** in speed.

Concrete example — searching:

- **Linear search** checks items one by one: for a million unsorted items, up to a million comparisons.
- **Binary search** on sorted data discards **half** of the remaining items at every step: for a million items, at most about 20 comparisons (Chapter 16 shows exactly why 20).

Both are correct. One is ~50,000× faster on this input. Performance is not vanity: at scale it is the difference between "the page loads" and "the page never loads"; between "the analysis finishes tonight" and "the analysis cannot be done at all."

## 3.3 Maintainability — code that a human can verify

A clever algorithm that nobody on the team can understand may be *worse* than a simple algorithm that is easy to verify. If nobody dares touch the code, the project is frozen even while it "works".

The best engineering choice balances a checklist:

- **correctness** — it computes the right thing;
- **performance** — fast enough for the real workload;
- **readability** — the next developer (possibly future you) can follow it;
- **memory use** — it fits the machine;
- **development time** — it was worth building;
- **future change** — it will not shatter when requirements shift.

This guide repeatedly makes you *compare two correct solutions* (insertion sort vs merge sort, linear vs binary search, recursion vs iteration) so that judgment becomes a habit.

## 3.4 Fair and responsible use

Algorithms affect people. A scoring, ranking, filtering, or alerting algorithm is never "just math" — it embodies assumptions about data and about whose outcomes matter.

A data-analysis or decision algorithm can:

- contain **bias** inherited from historical data;
- draw conclusions from **incomplete data**;
- produce results that are **difficult to explain** to the people affected.

When building real systems, professional algorithmic practice includes asking:

- What data is being used — and what data is *missing*?
- Who could be harmed by an incorrect result?
- Can a **person review** the decision?
- Can the result be **explained and challenged**?

Algorithmic skill includes understanding consequences, not only speed. The outlier detector you will build in the Algorithm Lab (Chapter 51) is deliberately designed to *flag* unusual values as "potential" outliers — a flagged value is a question for a human, not a verdict.

### Exercises for Chapter 3

1. A teammate says "find the duplicate" is a fully specified task. Give three different interpretations and the different output types each implies.
2. For each pair, name the dimension (correctness / performance / readability / memory / development time / future change) where the trade-off lives: (a) a 3-line naive sort vs a 40-line fast one; (b) storing all rows in memory vs streaming them.

<details><summary>Solutions</summary>

1. (i) "Is there any duplicate at all?" → boolean. (ii) "Which value repeats first?" → a single value (or absence). (iii) "List every duplicated value" → a collection. Also, for strings, case-insensitive matching changes the answer entirely.
2. (a) readability + development time vs performance; (b) memory use vs (often) development simplicity and the ability to answer questions that need all data — an online/offline trade explored fully in Chapter 57.
</details>

---

# Chapter 4: The Mindset of an Algorithmic Thinker

## 4.1 The universal cycle

Every algorithm in this book — and every algorithm you will ever write professionally — passes through the same cycle:

```text
      ┌──────────────────────────────────────────────┐
      │                                              │
      ▼                                              │
understand ──► examples ──► contract ──► pseudocode ──┼──► implement
the problem     by hand      in/out       plain       │      in C#
                inputs       written      language    │
                            outputs                  │      │
                                                     │      ▼
                 improve ◄── measure ◄── test ◄── prove/invariant
               (only if      and         edge      reasoning
                justified)  benchmark     cases     about why
```

The arrows at the bottom matter as much as the top: **prove → test → measure → improve, and improve only when justified.** A cycle that skips measurement produces superstition; a cycle that skips proof produces luck; a cycle that skips examples produces code for the wrong problem.

## 4.2 What mastery means — the ten abilities

You are ready to begin the journey when you can state what its destination is. Mastery means you can:

1. **recognize the shape of a problem** — counting, searching, ordering, connecting, optimizing;
2. **choose an appropriate data structure** — array, hash set, dictionary, stack, queue, tree, heap, graph;
3. **express a solution with pseudocode** — before touching a keyboard;
4. **prove why the solution works** — with a loop invariant (Chapter 12);
5. **estimate time and memory usage** — with Big-O analysis (Chapter 13);
6. **implement the solution clearly in C#** — with names, structure, and contracts;
7. **test edge cases** — empty, one item, duplicates, boundaries, invalid input;
8. **compare alternative solutions** — with concrete numbers, not adjectives;
9. **identify when a simpler algorithm is better** — the professional's courage;
10. **explain trade-offs to another developer** — in plain words, in a meeting, on a whiteboard.

Everything from the next chapter onward is the construction material for these ten abilities.

---
# Part II — The C# Laboratory from Zero

Part I built the *ideas*. This part builds the *laboratory*: the C# language and tools, explained from the very first word. If you already know C# well, skim Chapters 5–7 and slow down at Chapter 8; if C# is new to you, this part was written for you, word by word.

---

# Chapter 5: Setting Up Your Tools

## 5.1 Install the .NET SDK

**C#** is a programming language. **.NET** is the platform that compiles and runs C# programs. The single package you need is the **.NET SDK** (Software Development Kit), free from Microsoft's official .NET download page — pick the latest LTS (long-term support) version for your operating system (Windows, macOS, or Linux).

The SDK includes:

- the **compiler** (named Roslyn) that translates your C# text into executable code;
- the **runtime** that executes it;
- the **command-line tool** `dotnet` that manages projects;
- the standard **library** — thousands of ready-made, tested building blocks (`Console`, `File`, `List<T>`, `Dictionary<K,V>`, ...).

## 5.2 Verify the installation

Open a terminal (Command Prompt / PowerShell / Terminal) and type:

```bash
dotnet --version
```

Word by word:

- `dotnet` — the name of the .NET command-line tool; you invoke it by typing its name.
- `--version` — an *option* (also called a *flag*): a dash-prefixed word that modifies what the command does. Here it asks: "print your version number, then stop".
- The two spaces matter: command first, options after.

Expected output is a version number such as `8.0.xxx` or `9.0.xxx`. If you instead see "command not found", the SDK is not installed or not on your system's search path — revisit the installer before continuing.

## 5.3 Create and run your first project

```bash
dotnet new console -n AlgorithmJourney
cd AlgorithmJourney
dotnet run
```

Word by word, each piece:

| Piece | Meaning |
|---|---|
| `dotnet` | Invoke the .NET command-line tool. |
| `new` | The sub-command that creates something new. |
| `console` | *Which template* to create from: a console application — a program that reads and writes text in a terminal. (Other templates exist: `classlib`, `webapi`, `xunit`...) |
| `-n AlgorithmJourney` | `-n` is short for `--name`: the new project (and its folder) will be called `AlgorithmJourney`. |
| `cd AlgorithmJourney` | `cd` = *change directory*: move your terminal *into* the new folder so subsequent commands apply there. |
| `dotnet run` | Compile the project (if needed) and immediately execute it. |

If everything works, you will see the template's greeting printed — the exact text depends on your SDK version (older templates print `Hello, World!`). That single line proves the whole chain works: editor → compiler → runtime → console output.

## 5.4 What got created, and how a C# program runs

The folder contains (among other files):

```text
AlgorithmJourney/
├── AlgorithmJourney.csproj    ← project file: settings, target framework
├── Program.cs                 ← your source code lives here
└── obj/                       ← compiler intermediates (safe to ignore)
```

- `Program.cs` — the file you edit; "cs" stands for **C Sharp**.
- `AlgorithmJourney.csproj` — "csproj" = *C# project*: an XML file describing how to build your project (which .NET version, which libraries).

The journey of your code, from typing to output:

```text
you type Program.cs
        │
        ▼
   csc / Roslyn compiler  ──►  translates C# into intermediate language (IL)
        │
        ▼
   .NET runtime           ──►  executes IL, manages memory, prints to console
        │
        ▼
   text appears in your terminal
```

You never manage this machinery by hand — `dotnet run` triggers it all. But knowing the chain exists explains later behaviors (warm-up time, just-in-time compilation in Chapter 55's benchmarking).

### Exercises for Chapter 5

1. Create a second project named `Practice1` and run it, without looking back at this section.
2. What is the difference between `dotnet` and `dotnet run`?

<details><summary>Solutions</summary>

1. `dotnet new console -n Practice1` → `cd Practice1` → `dotnet run`.
2. `dotnet` alone prints its help (list of sub-commands); `dotnet run` is the *specific* sub-command that compiles and executes the current project.
</details>

---

# Chapter 6: C# Building Blocks Word by Word

This chapter is the vocabulary lesson. Every word below will appear inside code in every later chapter, so read it slowly — once — and return whenever a construct feels foggy.

## 6.1 Variables and types — what they actually are

```csharp
int number = 42;
```

Word by word:

| Word | Meaning |
|---|---|
| `int` | A **type**: "a whole number" (32-bit integer). Types say what shape of data a box may hold. |
| `number` | A **name** (identifier) you chose for this box. Naming is a design act — prefer descriptive. |
| `=` | **Assignment**, *not* mathematical equality. Read it as "becomes": `number` *becomes* `42`. |
| `42` | A **literal**: a value written directly in source code. |
| `;` | Statement terminator: one complete command ends here. Forgetting it is the classic first compile error. |

A **variable** is a named box in memory holding one value of one type. The type system is the compiler's promise-checker: it *refuses* to compile `int x = "hello";` because a string does not fit an int-box. That refusal is a gift — hundreds of future bugs die at compile time.

The types used constantly in this guide:

| Type | Holds | Example literals | Used for |
|---|---|---|---|
| `int` | whole numbers, ~±2.1 billion | `0`, `42`, `-7` | counts, indexes |
| `long` | whole numbers, ~±9.2 quintillion | `10000000000L` | huge counts |
| `double` | decimal approximations (64-bit) | `3.14`, `-0.5` | measurements, statistics |
| `bool` | truth values | `true`, `false` | conditions, flags |
| `char` | one single character | `'a'`, `'7'` | text scanning |
| `string` | a sequence of characters | `"hello"` | words, lines, files |

Note `char` uses single quotes `'a'` and `string` uses double quotes `"a"` — mixing them is a compile error, by design.

## 6.2 Methods — named, reusable procedures

A **method** is an algorithm packaged with a name. This one line is the densest line a beginner meets, so it gets the fullest dissection in the whole book:

```csharp
static int CountEvenNumbers(int[] numbers)
```

Word by word:

| Word | Meaning |
|---|---|
| `static` | The method belongs to the *type itself*, not to one object of the class. Practical meaning for us: you may call it directly as `CountEvenNumbers(...)` without first creating an object. |
| `int` | **Return type**: the method will deliver back exactly one `int` when it finishes. |
| `CountEvenNumbers` | The method **name** — PascalCase by C# convention; verbs describing what it computes. |
| `( ... )` | The **parameter list**: the inputs, in parentheses. |
| `int[]` | The type "array of int" — a fixed-length sequence of whole numbers (fully dissected in 6.3). |
| `numbers` | The parameter **name** — how the input will be referred to inside the method. |

A method call is a *question*: `CountEvenNumbers(new[] {4, 7, 9})` asks "how many of these are even?" and the answer (here `1`) comes back **at the place where you called it**, replacing the call expression.

`return` is how a method answers:

```csharp
return count;
```

`return` means two things at once: *"here is the answer"* and *"the method finishes now"*. Everything after an executed `return` in that path is skipped. The returned value must match the declared return type — `return "many";` inside an `int` method is a compile error.

When a method performs an action but produces no value, its return type is `void`:

```csharp
static void PrintArray(int[] numbers)
```

`void` = "nothing comes back". You call such a method *for its effect* (printing), not for an answer.

## 6.3 Arrays — the fundamental data structure

```csharp
int[] numbers = { 4, 1, 9, 2 };
```

Word by word:

- `int[]` — the type: *array of int*. The square brackets `[]` mark "sequence of fixed length".
- `numbers` — the name of the whole sequence.
- `= { 4, 1, 9, 2 }` — an initializer listing every element in order.

Picture it in memory — boxes side by side, each with an **index** (position number) starting at **zero**:

```text
index:      0     1     2     3
          ┌─────┬─────┬─────┬─────┐
numbers:  │  4  │  1  │  9  │  2  │
          └─────┴─────┴─────┴─────┘
length = 4   (indexes run 0 .. 3, never 4)
```

The two operations that make arrays powerful:

```csharp
int first = numbers[0];       // read:   O(1) — direct positional access
numbers[1] = 5;               // write:  O(1)
int length = numbers.Length;  // the count of elements, a stored property
```

- `numbers[0]` — **indexing**: the number inside `[ ]` selects one box. Indexes start at 0, so the last valid index of a 4-element array is `3`. Requesting `numbers[4]` throws `IndexOutOfRangeException` at runtime — the classic off-by-one error (Chapter 56).
- `.Length` — the number of boxes, remembered by the array itself.

Arrays are **fixed size**: created with a length, never grown. When a growing sequence is needed, C# offers `List<T>` (below). The zero-based indexing is a convention inherited from how memory addresses are computed: index *i* means "skip *i* boxes from the start", so skipping zero boxes lands on the first.

## 6.4 The collections you will meet in this guide

```csharp
int number = 42;
int[] numbers = { 4, 1, 9, 2 };
List<int> values = new() { 10, 20, 30 };
Dictionary<string, int> counts = new();
HashSet<string> uniqueWords = new();
```

Read the generic collections word by word — `<...>` is **not** comparison here:

| Collection | Reads as | Meaning | Superpower |
|---|---|---|---|
| `List<int>` | "list of int" | a **growable** sequence | append at the end in amortized O(1) |
| `Dictionary<string, int>` | "dictionary from string to int" | **key → value** pairs | look up a value *by key* in expected O(1) |
| `HashSet<string>` | "hash set of string" | a set of **unique** values | ask "is X in here?" in expected O(1) |

- The angle brackets `< >` declare a **generic** type: a reusable container specialized to a chosen element type. `List<int>` and `List<string>` are the same machinery holding different element shapes.
- `new()` is **target-typed new**: "construct a new instance of whatever type the left side declared". `List<int> values = new()` therefore reads "make a new List-of-int, call it `values`". It is shorthand for `new List<int>()`.
- `new() { 10, 20, 30 }` — construct *and* pre-fill with three elements.

Each structure earns its place in this book by making some algorithm dramatically faster or clearer — the mapping of *problem shape → best structure* is exactly what Parts V–XIII build.

### Exercises for Chapter 6

1. Declare a variable holding a book's price. Which type do you choose, and why not `int`?
2. Write the signature (first line only) of a method that receives a `string` and returns the count of characters.
3. For `int[] data = { 7, 3, 9 };` — what is `data.Length`, `data[0]`, `data[2]`, and what happens at `data[3]`?

<details><summary>Solutions</summary>

1. `double price = 19.99;` (or `decimal` for financial exactness — see Chapter 57). `int` cannot store fractional parts; it would truncate 19.99 to 19.
2. `static int CountCharacters(string text)`
3. `data.Length` = 3; `data[0]` = 7; `data[2]` = 9; `data[3]` throws `IndexOutOfRangeException` (valid indexes are 0, 1, 2 only).
</details>

---

# Chapter 7: Control Flow Loops and Decisions

Algorithms need exactly two kinds of machinery beyond data: **decisions** (do this or that, depending) and **repetition** (do this again and again). C# spells both out plainly.

## 7.1 if / else — the decision

```csharp
if (number % 2 == 0)
{
    Console.WriteLine("even");
}
else
{
    Console.WriteLine("odd");
}
```

Word by word:

- `if ( ... )` — "evaluate the expression in parentheses; if it is `true`, run the first block".
- `number % 2` — the **modulo** operator: the *remainder* after dividing `number` by 2. `9 % 2` is `1`; `8 % 2` is `0`.
- `==` — **equality comparison** (two equals signs!). One `=` assigns; two `==` asks. Confusing them is the classic beginner bug; the compiler catches *most* cases because `int` is not `bool`.
- `else` — the alternative block, run when the condition is `false`.
- `Console.WriteLine(...)` — a library method that prints one line of text to the console. `Console` is a type from the standard library; `.WriteLine` is a method on it; `"even"` is a string argument.

## 7.2 The for loop — counted repetition

```csharp
for (int index = 0; index < numbers.Length; index++)
{
    Console.WriteLine(numbers[index]);
}
```

The three slots inside `for ( ... ; ... ; ... )`, word by word:

1. `int index = 0` — **initializer**: runs once, before the loop starts. Creates a counter named `index` starting at 0 — the first index of an array (Chapter 6).
2. `index < numbers.Length` — **condition**: checked *before every* iteration, including the first. Loop continues while it is `true`. `<` (not `<=`) because valid indexes stop at `Length - 1`.
3. `index++` — **update**: runs *after each* iteration. `++` increases the variable by exactly 1 (`index = index + 1` in short form).

Execution order for `numbers = {4, 1, 9, 2}`:

```text
init:      index = 0
check 0<4  ✓ → body prints numbers[0]=4 → update index=1
check 1<4  ✓ → body prints numbers[1]=1 → update index=2
check 2<4  ✓ → body prints numbers[2]=9 → update index=3
check 3<4  ✓ → body prints numbers[3]=2 → update index=4
check 4<4  ✗ → loop ends
```

Four elements, four iterations, then a clean stop — the anatomy of every counted loop you will ever write.

## 7.3 The foreach loop — visit every element

```csharp
foreach (int value in numbers)
{
    Console.WriteLine(value);
}
```

Word by word:

- `foreach` — "visit each element of the sequence, in order, exactly once".
- `int value` — declares a fresh variable holding *the current element* (its value, not its index).
- `in numbers` — the sequence being walked.

`foreach` is preferred when you need values but not positions: no counter to initialize, no `Length` to bound, no off-by-one possible. Choose `for` when you *need the index* (comparing neighbors, writing into the same slots) and `foreach` when you merely process each value.

## 7.4 The while loop — repeat until a condition dies

```csharp
while (condition)
{
    // repeat while condition is true
}
```

Word by word: `while` checks the condition *before each* iteration; body runs while it stays `true`. The loop ends when the condition becomes `false` — or **never ends** if nothing inside the body can change it. A `while` whose condition never changes is the classic infinite loop (Chapter 56):

```csharp
int i = 0;
while (i < 3)
{
    Console.WriteLine(i);
    i++;                 // remove this line → the loop never ends
}
```

Use `for` when the number of repetitions is known or index-driven; use `while` when the end is *discovered during the run* — binary search (Chapter 16) is the perfect example: the range shrinks until it becomes empty, and only then do we stop.

## 7.5 break, continue, and return inside loops

Three early-exit words you will meet inside real algorithms:

| Word | Effect |
|---|---|
| `break;` | Abandon the loop *immediately*; jump to the first statement after it. Used by linear search the instant the target is found. |
| `continue;` | Skip the rest of *this* iteration; jump straight to the next check/update. |
| `return x;` | Leave the *entire method* now, delivering `x`. The strongest exit — used when the answer is already known. |

## 7.6 A small helper you will reuse forever

```csharp
static void PrintArray(int[] numbers)
{
    Console.WriteLine(string.Join(", ", numbers));
}
```

Word by word:

- `static void` — a method callable without an object, returning nothing (6.2).
- `string.Join(", ", numbers)` — a library method: take a **separator** (`", "`) and a sequence (`numbers`); weave them into one string with the separator *between* elements — `"4, 1, 9, 2"`.
- `Console.WriteLine(...)` prints that single readable line.

Why care? Because *watching state* is the core debugging technique of Part XVIII: printing the array after each phase of a sort is how you *see* an algorithm think. Keep this helper within reach, mentally, forever.

### Exercises for Chapter 7

1. Write a `for` loop that prints the numbers 1 through 5.
2. Same task with a `while`.
3. Predict what `9 % 3`, `10 % 3`, `2 % 7` evaluate to, then verify in a program.
4. In `for (int i = 0; i < n; i++)`, how many times does the body run (in terms of `n`)?

<details><summary>Solutions</summary>

1. `for (int i = 1; i <= 5; i++) { Console.WriteLine(i); }` — note `<=` because we *want* 5 included.
2. `int i = 1; while (i <= 5) { Console.WriteLine(i); i++; }`
3. `0` (9 divides evenly), `1` (one left over), `2` (smaller dividend: quotient 0, remainder the dividend itself).
4. Exactly `n` times (i = 0, 1, …, n−1) — provided `n ≥ 0`; this count is the heart of every O(n) analysis in Chapter 13.
</details>

---

# Chapter 8: Your First Complete Algorithm in C#

Time to combine everything: problem → examples → pseudocode → C#, with the full line-by-line and word-by-word treatment that sets the pattern for the whole book.

## 8.1 The problem, stated precisely

> Count how many numbers in a sequence are even.

Following the discipline of Chapter 4's cycle:

**Understand and restate:** walk through a sequence; for each element decide "even or not"; keep a running total of the "even" verdicts; report the total.

**Examples, by hand:**

| Input | Expected output | Why |
|---|---:|---|
| `{2, 4, 6}` | `3` | all even |
| `{1, 3, 5}` | `0` | none even |
| `{}` | `0` | nothing to count |
| `{7}` | `0` | odd |
| `{8}` | `1` | even |
| `{4, 7, 9, 2}` | `2` | 4 and 2 are even |

**Contract (input/output):**

```text
Input:  a sequence of integers (may be empty)
Output: a single integer ≥ 0 — the count of even elements
Rule:   a number is even exactly when number % 2 == 0
```

## 8.2 The pseudocode

```text
set count to zero
for each number in the sequence
    if the number has remainder zero when divided by two
        increase count
return count
```

Four lines. Every later algorithm in this guide compresses to something this short *before* we let C# near it.

## 8.3 The C# implementation

```csharp
static int CountEvenNumbers(int[] numbers)
{
    int count = 0;

    foreach (int number in numbers)
    {
        if (number % 2 == 0)
        {
            count++;
        }
    }

    return count;
}
```

## 8.4 Line by line

| Line | What it does |
|---|---|
| `static int CountEvenNumbers(int[] numbers)` | Declares the packaged algorithm: name, one input (`int[]`), one `int` answer. (Dissected in Chapter 6.2.) |
| `{` | Opens the method body. |
| `int count = 0;` | Creates the **accumulator** — the running total — starting at zero. Zero is the correct start: an empty sequence has already been handled (count of evens in nothing = 0). |
| `foreach (int number in numbers)` | Visits every element exactly once, in order, binding each to `number`. |
| `if (number % 2 == 0)` | The evenness test: remainder after division by 2 equals zero. |
| `count++;` | The update: total grows by one for each even found. |
| `}` `}` | Close the `if` and the loop. |
| `return count;` | Delivers the answer and ends the method. |

## 8.5 Word by word — the new pieces

- **accumulator** — the name for a variable that *collects* a result across iterations (`count` here; `total` in a sum; `maximum` in a max-search). Accumulators appear in nearly every algorithm in this book.
- `number % 2` — modulo (Chapter 7.1): the remainder. Even numbers leave remainder 0; odd numbers leave 1 (in C#, the remainder of a negative odd number like `-7 % 2` is `-1`, still *not* 0, so the evenness test works for negatives too).
- `count++` — increment (Chapter 7.2, third slot): add 1 to `count` and store it back.

## 8.6 Trace — watching it think

Input `{4, 7, 9, 2}`:

| Iteration | `number` | `number % 2` | even? | `count` after |
|---:|---:|---:|---|---:|
| start | — | — | — | 0 |
| 1 | 4 | 0 | yes | 1 |
| 2 | 7 | 1 | no | 1 |
| 3 | 9 | 1 | no | 1 |
| 4 | 2 | 0 | yes | 2 |
| end | — | — | — | return 2 |

Empty input `{}`: the `foreach` body never runs; `count` stays 0; return 0 — the contract's empty case holds *automatically*, because zero was the right initialization. Design decisions made at initialization time pay off at edge-case time.

## 8.7 Complexity, gently

Two questions (Chapter 1.6, question 5), answered without ceremony:

- **Time:** each of `n` elements is examined exactly once, with constant work per element → the total work grows in direct proportion to `n` → **O(n)** (the notation gets its full construction in Chapter 13).
- **Space:** the method uses two variables (`count`, `number`) regardless of input size → constant extra memory → **O(1)**.

## 8.8 Running it yourself

```csharp
Console.WriteLine(CountEvenNumbers(new int[] { 4, 7, 9, 2 }));   // 2
Console.WriteLine(CountEvenNumbers(new int[] { }));              // 0
Console.WriteLine(CountEvenNumbers(new int[] { 8 }));            // 1
```

- `new int[] { ... }` constructs an array literal argument on the spot; `new int[] { }` constructs the empty one — deliberately test it, always.

### Exercises for Chapter 8

1. Modify the method to count **odd** numbers. Which single token changes?
2. Write `CountMultiplesOfThree` — count elements divisible by 3.
3. Write `SumEven` — the *sum* (not count) of even elements. What changes about the accumulator's type and initialization?

<details><summary>Solutions</summary>

1. The comparison value: `number % 2 == 1` (or `!= 0`). The accumulator, loop, and return are untouched — precise changes, because we understood every word.
2. `if (number % 3 == 0) count++;` inside the same loop; signature and accumulator unchanged.
3. `static int SumEven(int[] numbers)` with `int sum = 0;` and `sum += number;` (add to the accumulator instead of incrementing). Initialization stays 0 because zero is the identity of addition — adding nothing changes nothing.
</details>

---
# Part III — The Method: Describe Before You Code

Part II gave you the laboratory. This part gives you the *method* — the professional habits that separate engineers who solve the right problem from coders who solve the wrong problem quickly.

---

# Chapter 9: Requirements Are Not Algorithms

## 9.1 The difference

A **requirement** says *what* someone wants. An **algorithm** says *how* to obtain it. They live at different levels and are written in different languages:

```text
REQUIREMENT (the wish):
    "Show the most common product category."

ALGORITHM (the machinery):
    "count occurrences per category in a hash map,
     scan entries, keep the key with the maximum count,
     break ties by choosing the alphabetically first category."
```

The gap between the two is where projects fail. Before the algorithm can exist, the requirement must be *interrogated*.

## 9.2 The questions that must be answered

For "Show the most common product category", a professional asks:

- **What happens when there are no rows?** Show nothing? Show "unknown"? Throw? The empty case (Chapter 1.3) is always the first question.
- **Are category names case-sensitive?** Is `"electronics"` the same category as `"Electronics"`? (Chapter 44 normalization — the answer changes the data structure needed.)
- **How are ties handled?** Two categories both appearing 40 times: pick one? show both? order them?
- **Can a category be missing (null/empty)?** Do blank cells count as a category of their own?
- **Is the data in memory, a file, or a database?** In-memory allows a hash map; a database suggests `GROUP BY`; a file suggests streaming (Chapter 57, online vs offline).

None of these is exotic. Every one of them *silently changes the algorithm*. Answering them costs minutes; skipping them costs rewrites.

## 9.3 Input/output contracts — the written agreement

Write the contract down before writing the algorithm down. A contract has four clauses:

```text
Input:        an array of non-negative integers
Output:       the largest value
Precondition: the array must contain at least one element
Postcondition: the returned value is an element of the array
              and is ≥ every element of the array
```

Word by word:

- **Precondition** — a condition that must be *true before* the algorithm starts; the caller's promise. If the caller breaks it, the algorithm owes nothing.
- **Postcondition** — a condition that must be *true after* the algorithm finishes; the algorithm's promise back to the caller.

Note how sharp the postcondition above is: not just "the largest value" but two *checkable* properties — *it is a member of the array* (so `FindMaximum` on `{3}` may not return `999`) and *it is ≥ every element* (so nothing bigger exists inside). Sharp postconditions are what make testing possible (Chapter 54).

## 9.4 Examples and counterexamples — the cheapest tests you will ever write

Before coding, build a small table of inputs and expected outputs. For a function that removes duplicates:

| Input | Expected output | What it teaches |
|---|---|---|
| `[1, 2, 1, 3]` | `[1, 2, 3]` | the general case |
| `[]` | `[]` | empty input |
| `[5]` | `[5]` | single item |
| `[2, 2, 2]` | `[2]` | all duplicates |

A **counterexample** is the sharper tool: an input that *disproves* a proposed algorithm.

Someone proposes: *"the first value is always the maximum — just return `numbers[0]`."*
You answer with one input: `[1, 9, 2]`. The proposal is dead — one line, no code written, no time wasted. Hunting counterexamples is a game you can play in your head, on a whiteboard, in a meeting — and it is exactly how algorithm interviews probe candidates (Chapter 58).

### Exercises for Chapter 9

1. Write the four-clause contract for `CountEvenNumbers` (Chapter 8).
2. Give a counterexample to the claim: "to check whether a list is sorted, it is enough to compare the first and last elements."

<details><summary>Solutions</summary>

1. Input: any `int[]` (empty allowed). Output: an `int ≥ 0`. Precondition: none beyond the type (empty is valid). Postcondition: the returned value equals the number of indices `i` where `numbers[i] % 2 == 0`.
2. `[1, 5, 0]` — first (1) < last (0)? No... first ≤ last holds for `[1, 5, 2]` (1 ≤ 2) yet the list is unsorted in the middle. Either example disproves the claim; the middle can hide any disorder the endpoints know nothing about.
</details>

---

# Chapter 10: Pseudocode and State Traces

## 10.1 Pseudocode — the bridge

**Pseudocode** is not a programming language. Nobody compiles it. It is *the algorithm itself*, written in disciplined plain language — the bridge between the requirement (human wishes) and the implementation (compiler-checked C#).

Rules of good pseudocode — follow them throughout this guide:

1. one action per line;
2. indentation shows structure (what is inside what);
3. names are full words, no types, no semicolons;
4. no language-specific syntax — nothing you would have to unlearn to move to another language.

## 10.2 A worked example — find the first repeated value

Problem: given a sequence, return the **first** value that appears a second time, scanning left to right; report absence otherwise.

Clarified contract:

```text
Input:        a sequence of values
Output:       the first value already seen when scanning left to right,
              or "no repeated value"
Precondition: none (empty sequence allowed)
Postcondition: the returned value occurs at least twice in the input
```

Pseudocode:

```text
function find first repeated value
    create an empty set called seen
    for each value in the input
        if seen contains value
            return value
        add value to seen
    return no repeated value
```

Notice the design decisions already made — *before any code*:

- a **set** (not a list) is chosen for `seen`, because membership tests must be fast (Chapter 24 makes this concrete);
- the membership question is asked **before** inserting, so a value is compared against *strictly earlier* values;
- early `return` exits the moment the answer is known — later elements are never examined.

## 10.3 The state trace — an x-ray of your algorithm

A **state trace** is a table recording the algorithm's state after each step. For input `[4, 2, 4, 7]`:

| Step | Value | `seen` before | Decision |
|---:|---:|---|---|
| 1 | 4 | `{}` | not contained → add 4 |
| 2 | 2 | `{4}` | not contained → add 2 |
| 3 | 4 | `{4, 2}` | **contained → found duplicate, return 4** |
| (4 | 7 | — | never reached) |

The trace reveals things code hides:

- step 4 never executes (early exit) — you *see* the laziness;
- the set grows one element per step — you can *feel* the O(n) space;
- with input `[4, 2, 7]` the loop completes with `seen = {4, 2, 7}` and the answer is "no repeated value" — the empty outcome is also traceable.

State traces reveal mistakes that are hard to see in code — a wrong initialization shows up immediately as an impossible first row. Use them by hand while learning, and as printed debug output later (Chapter 56).

### Exercises for Chapter 10

1. Write the state trace of `find first repeated value` on `[5, 5, 5]`.
2. Write pseudocode (no C#!) for: "return the index of the second occurrence of any value, or report none."

<details><summary>Solutions</summary>

1. Step 1: value 5, seen `{}` → add. Step 2: value 5, seen `{5}` → contained → return 5. Steps 3+ never run.
2. `create empty set seen` / `for each index i with value v` / `if seen contains v: return i` / `add v to seen` / `return none`. (Identical machinery; only the returned quantity changes — the shape-recognition skill of Part V.)
</details>

---

# Chapter 11: From Idea to Code the Disciplined Path

## 11.1 The eight steps, one last time

Here is the full discipline of Chapters 1–10 assembled into the working method you will apply to *every* algorithm in the rest of this book:

```text
1. Understand the problem      — restate it in your own words (Ch 1, 9)
2. Write examples              — small inputs → expected outputs (Ch 9.4)
3. Define inputs and outputs   — the written contract (Ch 9.3)
4. Write a simple solution     — in plain language (Ch 10.1)
5. Implement the simple        — in C# (Ch 6–8 vocabulary)
6. Prove or test correctness   — invariants and tests (Ch 12, 54)
7. Measure performance         — complexity, then benchmarks (Ch 13, 55)
8. Improve only when justified — never optimize blindly (Ch 57)
```

## 11.2 One worked example, end to end — the running maximum

Watch all eight steps on a single small problem. **Problem: compute the running maximum of a sequence** — after each element, the largest value seen so far.

**Step 1 — Understand.** Walk the sequence left to right; after each new element, report the largest value among those seen so far.

**Step 2 — Examples.**

| Input | Output |
|---|---|
| `[3, 1, 4, 1, 5]` | `[3, 3, 4, 4, 5]` |
| `[7]` | `[7]` |
| `[2, 2]` | `[2, 2]` |
| `[]` | `[]` |

**Step 3 — Contract.** Input: any `int[]`. Output: an `int[]` of equal length where output[i] = max(input[0..i]). Precondition: none. Postcondition: `output.Length == input.Length` and each output element is ≥ all input elements up to its index.

**Step 4 — Plain-language solution.**

```text
if the sequence is empty, return an empty sequence
create a result array of the same length
put the first value into the first slot of the result
for each remaining position
    the new running maximum is the larger of (previous running maximum, current value)
    store it in this position
return the result array
```

**Step 5 — Implement.**

```csharp
static int[] RunningMaximum(int[] numbers)
{
    if (numbers.Length == 0)
    {
        return Array.Empty<int>();
    }

    int[] result = new int[numbers.Length];
    result[0] = numbers[0];

    for (int index = 1; index < numbers.Length; index++)
    {
        result[index] = Math.Max(result[index - 1], numbers[index]);
    }

    return result;
}
```

New words, word by word:

- `Array.Empty<int>()` — a library method returning *the* shared empty int-array: no allocation, and semantically explicit ("empty by intent").
- `Math.Max(a, b)` — the library's maximum of two values; the *combine* step of the algorithm in one call.
- `result[index - 1]` — reading the **previous** answer: each output is built from the one before it. This *self-reference to the previous answer* is the seed of a huge idea — dynamic programming (Chapter 43).

**Step 6 — Test.** Run the four example rows; all match. Edge cases `[7]`, `[2,2]`, `[]` are *in* the table by design.

**Step 7 — Measure.** One pass, constant work per element: O(n) time. Output must exist anyway, so extra space is O(1) *beyond the output* (O(n) counting it — always say which convention you use).

**Step 8 — Improve?** O(n) is optimal: any correct algorithm must at least *read* all n inputs, so Ω(n) is a lower bound — no improvement is possible, and we stop. Knowing when to stop is part of mastery.

### Exercises for Chapter 11

1. Run the same eight steps for **running sum** (after each element, the total so far). Expected outputs for `[1, 2, 3]`?
2. Which two design decisions in `RunningMaximum` handle edge cases, and which edge cases?

<details><summary>Solutions</summary>

1. Outputs `[1, 3, 6]`; `[5]`→`[5]`; `[]`→`[]`. Pseudocode mirrors the maximum version with `+` replacing `Math.Max`; the accumulator starts at 0 this time and each result is `previous + current`.
2. (i) The early `Length == 0` branch returns the empty array — handles the empty input. (ii) `result[0] = numbers[0]` seeds position 0 and the loop starts at 1 — handles the single-element input (loop body never runs; the seed alone is the answer).
</details>

---
# Part IV — Correctness and Efficiency

Two questions decide whether an algorithm is *good*: **Is it right?** and **Is it fast enough?** This part builds the two corresponding tools: the loop invariant (for reasoning) and Big-O notation (for growth estimation).

---

# Chapter 12: Correctness Invariants and Proof

## 12.1 What correctness means

An algorithm is **correct** when it produces the required output **for every valid input** within its stated assumptions (its contract, Chapter 9.3).

> "Works on my example" is not a proof. It is one test.

One successful run tells you the algorithm is right *for that input*. The gap between "right for one input" and "right for all inputs" is the entire subject of this chapter. The tool that closes the gap is the **loop invariant**.

## 12.2 Loop invariants — the idea from zero

A **loop invariant** is a statement about your variables that:

1. is **true just before the loop starts** (initialization);
2. **remains true after every iteration** (maintenance — it never breaks);
3. combined with the loop's **ending condition**, yields the final answer (termination).

Think of it as a property the algorithm *carries* like a torch through the darkness of the loop: if it is lit at the start, and no step ever blows it out, then it is still lit when the loop ends — and there it illuminates the answer.

## 12.3 FindMaximum with its invariant

```csharp
static int FindMaximum(int[] numbers)
{
    if (numbers.Length == 0)
    {
        throw new ArgumentException("At least one number is required.");
    }

    int maximum = numbers[0];

    for (int index = 1; index < numbers.Length; index++)
    {
        if (numbers[index] > maximum)
        {
            maximum = numbers[index];
        }
    }

    return maximum;
}
```

Line by line:

| Line | Role |
|---|---|
| `if (numbers.Length == 0) throw ...` | **Guard clause**: the contract requires ≥ 1 element; refusing loudly beats returning a fake answer like 0. |
| `int maximum = numbers[0];` | **Initialization** of the accumulator with a *real* element (a member of the array — never an invented number). |
| `for (int index = 1; ...)` | The scan starts at **1** (0 is already inside the accumulator). |
| `if (numbers[index] > maximum)` | The test that decides whether the torch's property extends to this new element. |
| `maximum = numbers[index];` | The update — re-establishing the invariant for one more element. |
| `return maximum;` | Delivery. |

`ArgumentException` — a standard-library exception meaning "an argument violated the method's contract"; `nameof`-style messages tell the caller *which* rule broke. Exceptions are C#'s loudspeaker for broken preconditions.

**The invariant, stated precisely:**

> Before each iteration, `maximum` is the largest value among `numbers[0..index-1]` — the elements already examined.

**The three-part proof, written out:**

1. **Initialization.** Before the loop, `index = 1` and `maximum = numbers[0]`. The elements examined are exactly `numbers[0..0]` — one element — and `maximum` equals it, hence is the largest among them. The invariant is lit. ✓
2. **Maintenance.** Assume the invariant holds entering an iteration with some `index`. The body examines `numbers[index]`:
   - if `numbers[index] > maximum`, then this element beats everything examined so far (by the invariant, `maximum` already dominated them), so assigning it keeps `maximum` the largest of `numbers[0..index]`;
   - otherwise `maximum` already dominates `numbers[index]` too, and not changing it keeps the property for `numbers[0..index]`.
   Either way, the invariant holds for the *next* iteration. The torch never goes out. ✓
3. **Termination.** The loop ends when `index == numbers.Length`; by the invariant, `maximum` is the largest of `numbers[0..Length-1]` — the entire array. That is exactly the postcondition. ∎

This three-part structure (initialization, maintenance, termination) is *the* standard template for loop proofs — you will meet it again for binary search in Chapter 16 and merge in Chapter 21.

## 12.4 Preconditions and postconditions — binary search preview

For binary search (fully built in Chapter 16):

- **Precondition:** the input array is sorted in ascending order.
- **Postcondition:** return the index of the target if present, otherwise `-1`.

If you *omit* the precondition from the documentation, a perfectly correct binary-search implementation **appears broken** when someone feeds it unsorted data — it will confidently return `-1` for values that are present. The code was never wrong; the contract was never stated. In professional code, preconditions belong in the documentation comment, in guard clauses, and in tests (Chapter 54).

## 12.5 Proof versus testing — allies, not rivals

| | **Proof** | **Testing** |
|---|---|---|
| Covers | *all* valid inputs, by reasoning | the *selected* inputs you ran |
| Cost | minutes of thinking | seconds of execution |
| Catches | logic errors, missing cases | environment bugs, typos, misunderstood requirements |
| Misses | a *misunderstood requirement* (you proved the wrong thing) | unusual inputs you never thought to try |

Both are valuable. Proof can miss a misunderstanding of requirements; tests can miss unusual cases. **Use tests to support your reasoning — never as a substitute for it.**

### Exercises for Chapter 12

1. State and prove (three parts) the invariant of the `for` loop in `CountEvenNumbers` (Chapter 8).
2. A method returns the array's minimum but initializes `minimum = 0`. Give the smallest counterexample input.

<details><summary>Solutions</summary>

1. Invariant: *after processing the first k elements, `count` equals the number of even values among them.* Initialization: before the loop, 0 elements processed, `count = 0`, and there are 0 evens among none — true. Maintenance: each iteration examines one more element; if even, `count++` keeps the equation; if odd, unchanged keeps it. Termination: all n processed → `count` = number of evens in the whole array. ∎
2. `{-3}` (or any all-negative input): the guard passes, the loop never finds anything smaller than 0 among negatives... the true minimum −3 is *less than* the initialized 0, and since no element beats "0", the method wrongly returns 0. The fix — initialize with a *member* (`numbers[0]`), exactly as FindMaximum does.
</details>

---

# Chapter 13: Measuring Efficiency Big O from Zero

## 13.1 Input size — the variable everything depends on

Let `n` represent the **size of the input**:

- for an array or list: `n` = number of elements;
- for a string: `n` = its length in characters;
- for a matrix: often `n` = rows and columns;
- for a graph: two sizes — `V` for vertices and `E` for edges (Part XIII).

Efficiency questions are always of the form: *how does the work grow when `n` grows?* Not "how fast is it on my laptop today" — laptops change; growth rates survive hardware generations (Euclid's algorithm scales today exactly as it did on paper).

## 13.2 Counting operations — the honest way to start

Before notation, count operations on small inputs and *watch the pattern*. For "print all pairs":

```csharp
for (int i = 0; i < numbers.Length; i++)
{
    for (int j = 0; j < numbers.Length; j++)
    {
        Console.WriteLine(numbers[i] + ", " + numbers[j]);
    }
}
```

The outer loop runs `n` times; each outer pass runs the inner loop `n` times; each inner pass prints once:

| n | prints = n×n |
|---:|---:|
| 10 | 100 |
| 100 | 10,000 |
| 1,000 | 1,000,000 |
| 10,000 | 100,000,000 |

Multiply `n` by 10 → the work multiplies by 100. That *squared* relationship is the disease Big-O notation exists to name: **O(n²)**.

## 13.3 Time complexity — the growth classes, one by one

Time complexity describes **how the number of operations grows as the input grows**, ignoring constant factors and machine speed. The classes you must *feel* in your bones:

```csharp
// O(1) — constant: work independent of n
int first = numbers[0];

// O(log n) — logarithmic: work grows by +1 each time n DOUBLES
// (binary search, Chapter 16)

// O(n) — linear: touch every element once
foreach (int number in numbers)
{
    Console.WriteLine(number);
}

// O(n log n) — linearithmic: the best general sorting can do (Part VII)

// O(n²) — quadratic: all-pairs scans
for (int i = 0; i < numbers.Length; i++)
{
    for (int j = 0; j < numbers.Length; j++)
    {
        // compare a pair
    }
}
```

The feel, in a table — **work units for growing n**:

| n | O(1) | O(log n) | O(n) | O(n log n) | O(n²) | O(2ⁿ) |
|---:|---:|---:|---:|---:|---:|---:|
| 10 | 1 | ~3 | 10 | ~33 | 100 | 1,024 |
| 100 | 1 | ~7 | 100 | ~664 | 10,000 | ~10³⁰ |
| 1,000 | 1 | ~10 | 1,000 | ~9,966 | 1,000,000 | ~10³⁰⁰ |
| 1,000,000 | 1 | ~20 | 1,000,000 | ~20 million | 10¹² | beyond astronomical |

Read the last row slowly. Doubling *constants* in your code gains you a factor of 2. Moving one column **left** gains you a factor of thousands to billions. That is why algorithm choice dominates micro-optimization.

## 13.4 Why logarithms — the math, explained

`log₂(n)` answers: *how many times can you divide n by 2 before reaching 1?*

| n | halvings to reach 1 |
|---:|---:|
| 1 | 0 |
| 2 | 1 |
| 8 | 3 (8→4→2→1) |
| 1,000 | ~10 (halve 10 times: ≈0.98) |
| 1,000,000 | ~20 |

The astonishing consequence: **a million items need only ~20 halvings.** A billion items need only ~30. Any algorithm that discards half of its remaining work at every step (binary search, balanced trees, some sorting) therefore pays only ~20–30 units of work even on gigantic inputs. When you meet `low + (high - low) / 2` in Chapter 16, you are looking at the exact line that buys this miracle.

## 13.5 Space complexity — memory grows too

**Space complexity** measures *additional* memory the algorithm allocates beyond its input.

```csharp
// O(1) extra space — a few variables, whatever n is
static int Sum(int[] numbers)
{
    int total = 0;

    foreach (int number in numbers)
    {
        total += number;
    }

    return total;
}

// O(n) extra space — a whole new array, proportional to input
static int[] Copy(int[] numbers)
{
    return numbers.ToArray();
}
```

`Sum` keeps one accumulator regardless of input size → constant extra space. `Copy` must materialize an output as large as the input → linear extra space. Time and space trade against each other constantly in this book: prefix sums (14.1) spend O(n) memory to buy O(1) range queries; hash structures (Part VIII) spend memory to buy lookup speed. Always state *which* you are spending, and why it is worth it.

## 13.6 Best, average, and worst case

The *same* algorithm behaves differently on different inputs:

- **Best case** — the most favorable input (target is the first element: linear search finishes in 1 step).
- **Average case** — expected behavior under an assumption about how inputs are distributed.
- **Worst case** — the most expensive input (target is last or absent: linear search takes n steps).

Engineering rule: **always state which case you are discussing.** Most interviews and most production guarantees care about the *worst* case, because users and attackers both reliably find it. Insertion sort (Chapter 20) is the classic case study: O(n²) worst case, yet O(n) on nearly-sorted data — which is *why* it survives inside real libraries.

## 13.7 Big O, Big Theta, and Big Omega — the three notations

Three sibling notations from mathematics, word by word:

- **O(f(n))** — *upper bound* style: "the work grows **no faster than** f(n)". (A leash.)
- **Ω(f(n))** — *lower bound* style: "the work grows **at least as fast as** f(n)". (A floor.)
- **Θ(f(n))** — *tight bound*: "the work grows **exactly at** the rate f(n)". (Both at once.)

Precisely: T(n) = O(f(n)) means there exist constants c > 0 and n₀ such that T(n) ≤ c·f(n) for all n ≥ n₀. Informally: past small inputs, the curve of T stays under a stretched copy of f.

In beginner and practical engineering discussions, **Big O is used as the everyday shorthand** for growth behavior — "binary search is O(log n)" — even when Θ would be more precise. This guide follows that convention while keeping the distinction honest where it matters (13.6's cases; hash worst cases in Part VIII).

One subtlety worth knowing early: **amortized** analysis averages a *sequence* of operations. `List<T>.Add` is O(1) *amortized*: most calls just write one slot, but occasionally the internal array is full and a doubling copy (O(n)) occurs; spread across all the adds that copy pays for itself (Appendix A uses "amortized" with exactly this meaning).

## 13.8 Do not optimize by guessing

A theoretically better algorithm may be **slower for tiny inputs** because of constants, allocations, or cache behavior (insertion sort beats merge sort below ~small n — Chapter 55 measures exactly this). The professional sequence is always:

1. **correctness** — a fast wrong answer is worthless;
2. **complexity analysis** — know the growth class before running anything;
3. **measurement with realistic data** — benchmarks (Chapter 55), not opinions.

> Rules of thumb are the beginning of judgment, never the end of it.

### Exercises for Chapter 13

1. Classify: (a) print the first element; (b) print every element and its index; (c) for each element, compare with every other element; (d) halve a range until empty.
2. An algorithm takes 2 s on n = 1,000, and its work is O(n²). Estimate the time at n = 4,000.
3. Why is `log₂(1,000,000) ≈ 20`? Show the halvings.
4. You added a hash set to make membership checks O(1). What did you spend, and under which complexity term?

<details><summary>Solutions</summary>

1. (a) O(1); (b) O(n); (c) O(n²); (d) O(log n).
2. Work scales ×16 (4²), so ≈ 32 s. Growth math beats hope.
3. 10⁶ → 5·10⁵ → 2.5·10⁵ → … dividing by 2 twenty times gives 10⁶ / 2²⁰ ≈ 0.95 < 1: about twenty halvings to reach 1.
4. You spent O(n) **extra space** (the set's memory) — the classic time–space trade, stated in 13.5's terms.
</details>

---
# Part V — Core Patterns with Arrays and Strings

Experienced problem-solvers do not see "a new problem every time" — they see a small number of **patterns** recurring under different costumes. This part teaches the four foundational array/string patterns. Learn them once; recognize them forever.

---

# Chapter 14: Fundamental Patterns

## 14.1 Prefix sums — pay once, query forever

### The problem shape — repeated range questions

> "I will ask you **many** range questions about the **same** array: what is the sum of elements from index `start` through `end`?"

The naive answer re-adds the range for every question — O(n) *per question*. With q questions that is O(n·q). The prefix-sum pattern flips the cost.

### The idea — precompute every prefix total

Build one auxiliary array where position `k` stores the sum of *everything before* index `k`. Then any range sum is a single **subtraction of two ready-made numbers**.

```csharp
static int[] BuildPrefixSums(int[] numbers)
{
    int[] prefix = new int[numbers.Length + 1];

    for (int index = 0; index < numbers.Length; index++)
    {
        prefix[index + 1] = prefix[index] + numbers[index];
    }

    return prefix;
}

static int RangeSum(int[] prefix, int start, int end)
{
    return prefix[end + 1] - prefix[start];
}
```

### Line by line — building the prefix array

| Line | What it does |
|---|---|
| `int[] prefix = new int[numbers.Length + 1];` | Allocates **one slot longer** than the input: `prefix[0]` will hold "the sum of zero elements" = 0, and `prefix[k]` the sum of the first k elements. The extra slot removes every special case. |
| `for (int index = 0; ...)` | Walks the input once — this is the single O(n) payment. |
| `prefix[index + 1] = prefix[index] + numbers[index];` | The recurrence: *sum of first (index+1) elements = sum of first index elements + this element*. Each entry leans on the previous — self-reference again, the seed of Chapter 43. |
| `return prefix;` | The query-ready structure. |

### Line by line — answering a range query

| Line | What it does |
|---|---|
| `prefix[end + 1]` | Sum of elements at indexes 0..end ("everything through end"). |
| `prefix[start]` | Sum of elements at indexes 0..start−1 ("everything strictly before start"). |
| subtraction | Sum of elements at indexes start..end — the answer, in one arithmetic step. |

**Why `end + 1`?** Because `prefix[k]` stores the sum of elements *before* index `k`. The sum from `start` through `end` is therefore "sum before `end+1`" minus "sum before `start`". The indexing convention *is* the pattern; internalize it via trace:

For `numbers = {3, 1, 4, 2}`:

```text
index:     0   1   2   3
numbers:   3   1   4   2
prefix:  0 3   4   8   10      (length 5; prefix[0]=0 by meaning)
         ↑
   sum of nothing
```

| Query | Computation | Result |
|---|---|---:|
| sum of [0..2] | `prefix[3] - prefix[0]` = 8 − 0 | 8 (=3+1+4) ✓ |
| sum of [1..3] | `prefix[4] - prefix[1]` = 10 − 3 | 7 (=1+4+2) ✓ |
| sum of [2..2] | `prefix[3] - prefix[2]` = 8 − 4 | 4 ✓ |

**Complexity:** build O(n) time / O(n) space; *every later query O(1)*. The pattern's slogan: **pay once, query forever** — worth it whenever queries outnumber builds.

## 14.2 Two pointers — narrowing from both ends

### The problem shape — pair existence in sorted data

> "In a **sorted** array, do two values add up to exactly `target`?"

### The idea — narrowing from both ends

Place one finger on the smallest value (left end) and one on the largest (right end). Compare their sum to the target. Each comparison **eliminates one candidate permanently**:

- sum too small → only a *larger* left value can help → move `left` right;
- sum too big → only a *smaller* right value can help → move `right` left;
- equal → found.

```csharp
static bool HasPairWithSum(int[] numbers, int target)
{
    int left = 0;
    int right = numbers.Length - 1;

    while (left < right)
    {
        int sum = numbers[left] + numbers[right];

        if (sum == target)
        {
            return true;
        }

        if (sum < target)
        {
            left++;
        }
        else
        {
            right--;
        }
    }

    return false;
}
```

### Line by line — the two-pointer walk

| Line | What it does |
|---|---|
| `int left = 0;` | Finger A: the leftmost remaining candidate. |
| `int right = numbers.Length - 1;` | Finger B: the rightmost (largest, since sorted) candidate. |
| `while (left < right)` | The range is alive while the fingers have not crossed. Crossing = all pairs eliminated. |
| `int sum = numbers[left] + numbers[right];` | The current pair's total. |
| `if (sum == target) return true;` | Success — early exit. |
| `left++` / `right--` | The elimination step: discard exactly one *provably useless* endpoint. |

### Why the moves are safe — the invariant

Invariant: *if any valid pair exists, both of its members are still between `left` and `right`.* When `sum < target`, the pair `(numbers[left], anything ≤ numbers[right])` can never reach the target — every remaining pairing of `numbers[left]` sums even less. So `numbers[left]` is dead and may be discarded. Symmetrically for a too-large sum. Nothing that matters is ever thrown away — that is a proof, not a hope.

### Trace on `{1, 3, 4, 6, 9}`, target 10

| Step | left | right | values | sum | action |
|---:|---:|---:|---|---:|---|
| 1 | 0 | 4 | 1 + 9 | 10 | equal → **true** |

Trace on target 11:

| Step | left | right | values | sum | action |
|---:|---:|---:|---|---:|---|
| 1 | 0 | 4 | 1 + 9 | 10 | < 11 → left++ |
| 2 | 1 | 4 | 3 + 9 | 12 | > 11 → right-- |
| 3 | 1 | 3 | 3 + 6 | 9 | < 11 → left++ |
| 4 | 2 | 3 | 4 + 6 | 10 | < 11 → left++ |
| 5 | 3 | 3 | — | — | left == right → **false** |

**Complexity:** O(n) time — each step permanently removes one element from consideration, so at most n−1 steps; O(1) extra space. Versus the naive all-pairs O(n²): on a million elements, ~10¹² pair-checks become ~10⁶ — the same miracle class as 13.3's table.

**Precondition (the fine print):** the input **must be sorted** — the invariant's "anything ≤ numbers[right]" argument silently assumes order. Unsorted input → sort first (O(n log n), Part VII) or use a hash map (Chapter 25).

## 14.3 Sliding window — reuse the overlap

### The problem shape — best consecutive stretch

> "Find the maximum sum of any `k` **consecutive** elements."

### The idea — reuse the overlap

Computing each window from scratch throws away work: consecutive windows share `k−1` elements. Instead, when the window slides one step right, **add the one entering element, subtract the one leaving** — the sum updates in two operations, not k.

```csharp
static int MaximumWindowSum(int[] numbers, int windowSize)
{
    if (windowSize <= 0 || windowSize > numbers.Length)
    {
        throw new ArgumentOutOfRangeException(nameof(windowSize));
    }

    int windowSum = 0;

    for (int index = 0; index < windowSize; index++)
    {
        windowSum += numbers[index];
    }

    int best = windowSum;

    for (int index = windowSize; index < numbers.Length; index++)
    {
        windowSum += numbers[index];
        windowSum -= numbers[index - windowSize];
        best = Math.Max(best, windowSum);
    }

    return best;
}
```

### Line by line — the window's two loops

| Line | What it does |
|---|---|
| `if (windowSize <= 0 \|\| windowSize > numbers.Length)` | Guard: a window must have a feasible size. `ArgumentOutOfRangeException` = "an argument's *value* is outside the allowed range" (Chapter 12's `ArgumentException`, specialized). |
| first `for` | Builds the **initial** window: sum of elements 0..windowSize−1. |
| `int best = windowSum;` | The running answer starts as the initial window — a real member, never an invented number (the Chapter 12 lesson). |
| second `for`, from `windowSize` onward | One step per slide; `index` is the **entering** element's position. |
| `windowSum += numbers[index];` | The element **entering** on the right joins the sum. |
| `windowSum -= numbers[index - windowSize];` | The element **leaving** on the left departs. `index - windowSize` is exactly the left edge of the old window. |
| `best = Math.Max(best, windowSum);` | The accumulator (Chapter 8) keeps the champion. |

### Trace on `{2, 1, 5, 1, 3, 2}`, windowSize 3

| index entering | window | sum computation | windowSum | best |
|---:|---|---|---:|---:|
| init | [2,1,5] | 2+1+5 | 8 | 8 |
| 3 | [1,5,1] | 8 +1 −2 | 7 | 8 |
| 4 | [5,1,3] | 7 +3 −1 | 9 | **9** |
| 5 | [1,3,2] | 9 +2 −5 | 6 | 9 |

**Complexity:** O(n) — the naive recompute-each-window approach is O(n·k); on n = 10⁶, k = 1,000 that is 10⁹ operations collapsing to 2×10⁶. O(1) extra space. The pattern's essence: **never recompute what an adjacent step already knew**.

## 14.4 Frequency counting — the histogram pattern

### The problem shape — counting occurrences

> "How many times does each item appear?" — letters in a word, words in a document, events per category, responses per bucket.

### The idea — one pass, one histogram

Walk the input once, and for each element increment a counter in a key→count map. After one pass, every membership and multiplicity question is a lookup.

```csharp
static Dictionary<char, int> CountCharacters(string text)
{
    Dictionary<char, int> counts = new();

    foreach (char character in text)
    {
        counts[character] = counts.GetValueOrDefault(character) + 1;
    }

    return counts;
}
```

### Line by line — tallying the histogram

| Piece | What it does |
|---|---|
| `Dictionary<char, int> counts = new();` | The histogram: from each character to its count (Chapter 6.4's dictionary; Part VIII builds the machinery under it). |
| `foreach (char character in text)` | A string yields its characters one at a time — a string *is* a sequence of `char` (Chapter 6.1). |
| `counts[character] = ...` | Indexer assignment: "store (or overwrite) the count for this key". |
| `counts.GetValueOrDefault(character)` | Library method: the current count for the key, or **0 if absent** — no branch needed. Word by word: *get the value, or the default* (0 for int). |
| `+ 1` | The tally. |

The `GetValueOrDefault` + 1 combination is the *entire* pattern: "old-or-zero, plus one" makes a missing key behave as count 0 on first sight — no `if`, no special case.

### Trace on `"aba"`

| step | character | old count | new count stored |
|---:|---|---:|---:|
| 1 | 'a' | 0 (absent) | 1 |
| 2 | 'b' | 0 (absent) | 1 |
| 3 | 'a' | 1 | 2 |

Final: `{'a': 2, 'b': 1}`. **Complexity:** O(n) expected time, O(k) space where k = distinct items.

This one pattern is the engine behind: anagram detection (44.3), word frequencies, category counts, duplicate detection, data profiling, the Algorithm Lab's grouped analysis (51.4), and — with a twist — dynamic programming's memo tables (43.2). When you see "count / tally / how many of each", your hand should reach here first.

## 14.5 Pattern recognition — the field guide

| You hear... | You reach for... | Section |
|---|---|---|
| "many range-sum questions on one array" | prefix sums | 14.1 |
| "sorted; find a pair/triplet with a property" | two pointers | 14.2 |
| "best/longest/shortest **consecutive** stretch" | sliding window | 14.3 |
| "how many of each / same multiset / duplicates" | frequency counting | 14.4 |

### Exercises for Chapter 14

1. Using the `prefix` array of `{5, 2, 8}`: compute `RangeSum(prefix, 1, 2)` by hand, then explain each term.
2. Modify `HasPairWithSum` to return the *pair* (values) instead of a bool. Which lines change?
3. Trace `MaximumWindowSum` on `{4, 2}` with windowSize 2 — how many slides occur after the initial window?
4. Count *word* frequencies in `"the cat the dog the"` (split on spaces) using the frequency pattern; which parts of `CountCharacters` change?

<details><summary>Solutions</summary>

1. prefix = [0, 5, 7, 15]. `RangeSum(1,2)` = prefix[3] − prefix[1] = 15 − 5 = 10 = 2+8 ✓. First term: all through end=2; second: all before start=1 (just element 0).
2. Return type becomes `(int Left, int Second)?` (nullable tuple, as in Chapter 25's two-sum); on `sum == target` return `(numbers[left], numbers[right])`; on failure return `null`. The invariant and moves are untouched.
3. One slide (index 2 does not exist; the sliding loop runs zero times — initial window [4,2] with sum 6 is already the whole array). Note the guard would reject windowSize 3 > length 2.
4. Split first (`text.Split(' ')`), the map becomes `Dictionary<string, int>`, and the loop walks words. Result: the→3, cat→1, dog→1. Only the key type and the iteration source changed — the skeleton is the pattern.
</details>

---
# Part VI — Searching Algorithms

Searching is the most-executed algorithm family in computing — every cache lookup, every database query, every `Contains` call. Two ideas cover the landscape: **scan everything** (linear) and **halve the space** (binary). Mastery is knowing when each wins.

---

# Chapter 15: Linear Search

## 15.1 The idea

Walk the sequence from the beginning; compare each element to the target; the moment one matches, return its index; if the walk ends unmatched, the target is absent — report it with the sentinel `-1`.

It requires **nothing** of the data: unsorted, sorted, strings, doubles — anything comparable with `==` works. That universality is its superpower and the reason it is the correct default for small or one-off lookups.

## 15.2 The code

```csharp
static int LinearSearch(int[] numbers, int target)
{
    for (int index = 0; index < numbers.Length; index++)
    {
        if (numbers[index] == target)
        {
            return index;
        }
    }

    return -1;
}
```

## 15.3 Line by line

| Line | What it does |
|---|---|
| `for (int index = 0; index < numbers.Length; index++)` | The counted walk over every position (anatomy in 7.2). |
| `if (numbers[index] == target)` | The comparison — one position's value against the question. |
| `return index;` | **Early exit** (7.5): the answer is known; later elements are never touched. This is what makes the best case O(1). |
| `return -1;` | The **sentinel**: a return value that means "not found". −1 because no valid array index is negative — it can never collide with a real position. |

## 15.4 Trace on `{4, 7, 2, 9}`, target 9

| index | value | == 9? | action |
|---:|---:|---|---|
| 0 | 4 | no | continue |
| 1 | 7 | no | continue |
| 2 | 2 | no | continue |
| 3 | 9 | **yes** | return 3 |

And target 5: all four comparisons fail → loop ends → return −1. Four comparisons, worst case fully realized.

## 15.5 Complexity — the three cases

- **Best case:** target at position 0 → 1 comparison → O(1).
- **Worst case:** target last or absent → n comparisons → O(n).
- **Average case** (target uniformly present): expected ~n/2 comparisons → still O(n); constants halved, class unchanged.
- **Space:** two variables (`index`, nothing else) → O(1).

> An algorithm that "must potentially look at everything" is Ω(n) when the data is unordered — linear search is *optimal* for unsorted sequences. It is not a naive fallback; it is the correct answer to a provable lower bound.

### Exercises for Chapter 15

1. Write a boolean variant `Contains` using `foreach`. What does it return instead of −1, and why is that simpler?
2. In a 10,000-element unsorted array, roughly how many comparisons for an absent target?

<details><summary>Solutions</summary>

1. `foreach (int v in numbers) if (v == target) return true; return false;` — booleans need no sentinel because "not found" *is* a valid answer (false); positions were the only reason for −1.
2. All 10,000 (the worst case is the honest expectation for absence — no early exit exists).
</details>

---

# Chapter 16: Binary Search

## 16.1 The idea — the phone book

You never read a phone book front to back. You open it in the **middle**, glance at the name there, and instantly know which **half** to discard. Open, glance, discard half; open, glance, discard half. A million pages surrender in ~20 glances — the mathematics of 13.4 made operational.

The single precondition that buys this: **the data must be sorted.** Order is what lets one comparison eliminate *half* the remaining candidates ("too small ⇒ everything to the left is also too small").

## 16.2 The code

```csharp
static int BinarySearch(int[] numbers, int target)
{
    int low = 0;
    int high = numbers.Length - 1;

    while (low <= high)
    {
        int middle = low + (high - low) / 2;

        if (numbers[middle] == target)
        {
            return middle;
        }

        if (numbers[middle] < target)
        {
            low = middle + 1;
        }
        else
        {
            high = middle - 1;
        }
    }

    return -1;
}
```

## 16.3 Line by line

| Line | What it does |
|---|---|
| `int low = 0;` | Left edge of the *alive* range — initially the first index. |
| `int high = numbers.Length - 1;` | Right edge of the alive range — initially the last index. **Everything outside [low, high] has been proven irrelevant.** |
| `while (low <= high)` | Continue while the alive range is non-empty. `<=` (not `<`): a range of exactly one element (low == high) is still worth one look — the classic off-by-one, 56. |
| `int middle = low + (high - low) / 2;` | The midpoint of the alive range — computed the overflow-safe way (16.5). |
| `if (numbers[middle] == target) return middle;` | Found; deliver the index, early exit. |
| `if (numbers[middle] < target)` | Middle is too small ⇒ target, if present, lives strictly right of middle ⇒ discard middle **and everything left of it**. |
| `low = middle + 1;` | The discard executed: the alive range's left edge jumps past middle. The `+ 1` matters — middle itself is *known dead*. |
| `high = middle - 1;` | The mirrored discard: middle too large ⇒ jump the right edge below middle. |
| `return -1;` | Range became empty (low > high) ⇒ every element was eliminated ⇒ the target does not exist. The sentinel, as in 15.3. |

## 16.4 Full trace — `{2, 5, 8, 12, 16, 23, 38, 56, 72, 91}`, target 23

```text
indexes:    0  1  2  3   4   5   6   7   8   9
values:     2  5  8  12  16  23  38  56  72  91
```

| Step | low | high | middle | numbers[middle] | vs 23 | action |
|---:|---:|---:|---:|---:|---|---|
| 1 | 0 | 9 | 4 | 16 | < 23 | low = 5 |
| 2 | 5 | 9 | 7 | 56 | > 23 | high = 6 |
| 3 | 5 | 6 | 5 | **23** | == | **return 5** |

Three comparisons; linear search would have taken six. Now target 24 (absent):

| Step | low | high | middle | numbers[middle] | vs 24 | action |
|---:|---:|---:|---:|---:|---|---|
| 1 | 0 | 9 | 4 | 16 | < 24 | low = 5 |
| 2 | 5 | 9 | 7 | 56 | > 24 | high = 6 |
| 3 | 5 | 6 | 5 | 23 | < 24 | low = 6 |
| 4 | 6 | 6 | 6 | 38 | > 24 | high = 5 |
| 5 | — | — | — | — | low > high | **return −1** |

Watch step 4→5: the alive range narrowed to one element, was examined, eliminated, and the loop condition died — absence *proved* by exhaustion, not assumed.

## 16.5 Why `low + (high - low) / 2` and not `(low + high) / 2`

Both are mathematically the same midpoint. But `low + high` can **overflow**: with huge arrays near 2³¹ elements, `low + high` can exceed `int.MaxValue` (2,147,483,647), wrap to a negative number, and make `middle` negative — an instant `IndexOutOfRangeException` from a "correct" algorithm.

`high - low` is always a small non-negative number (the range's *width*), so no overflow can occur; adding it back to `low` stays in bounds. This one line is a famous piece of engineering history — the same bug lived inside a Java library binary search for years. The lesson: **arithmetic is part of the algorithm**; correctness proofs (12) must include the numbers' behavior, not just the logic.

## 16.6 The invariant — why it is correct

State it precisely:

> **Invariant:** if the target exists in the array, it lies within `numbers[low..high]`.

- **Initialization:** low = 0, high = Length−1 — the whole array; trivially true.
- **Maintenance:** when `numbers[middle] < target`, *sortedness* guarantees every element at indexes ≤ middle is also < target — none of them can be the target — so moving `low` past them preserves the invariant. Mirror argument for the `>` branch.
- **Termination:** the loop ends when the range is empty; the invariant then says "if the target exists, it lies in an empty range" — i.e., it does not exist. Returning −1 is exactly right. ∎

Note how the **precondition (sorted)** carries the entire maintenance argument. Feed this code unsorted data and the invariant's key sentence ("every element left of middle is also < target") becomes false — Chapter 12's warning in the flesh.

## 16.7 Complexity — the halving arithmetic

Each iteration performs O(1) work and **shrinks the alive range to at most half**: from width `w` to at most `⌊w/2⌋`. Widths go n → n/2 → n/4 → ... → 1 → 0. The number of halvings to reach empty is ⌈log₂(n+1)⌉ (13.4):

| n | max comparisons |
|---:|---:|
| 10 | ~4 |
| 1,000 | ~10 |
| 1,000,000 | ~20 |
| 1,000,000,000 | ~30 |

**Time O(log n)** in the worst case; **O(1)** extra space (iterative — two integer variables). The recursive variant spends O(log n) *stack* space (30.4) — one of the many time/space/structure trades this book keeps surfacing.

## 16.8 The classic mistakes — learn them by name

1. `while (low < high)` — skips single-element ranges; misses targets when the range narrows to one (16.4 step 4 would have failed silently).
2. `low = middle` / `high = middle` (forgetting the `± 1`) — the range may stop shrinking → **infinite loop** (56). Always discard middle itself: it is already known dead.
3. `(low + high) / 2` — overflow (16.5).
4. Running it on unsorted input — precondition violation; confidently wrong results (12.4).
5. `return middle` for existence *and* position when duplicates exist — returns *some* occurrence, not the first (17.1 exists precisely for this).

### Exercises for Chapter 16

1. Trace `{1, 3, 5, 7, 9}` searching for 1 — how many iterations? And for 9?
2. Which single character distinguishes correct `while (low <= high)` from the infinite-loop-prone variant, and what does that character protect?
3. Why does each iteration reduce the range to at most half rather than exactly half?

<details><summary>Solutions</summary>

1. Target 1: middle 2 (value 5) > 1 → high = 1; middle 0 (value 1) == → return 0. Two iterations. Target 9: middle 5 < 9 → low = 3; middle 3 == 7? values {1,3,5,7,9}, index 3 = 7 < 9 → low = 4; index 4 = 9 → return. Three iterations. Note the *first* and *last* positions cost 2 and 3 — not 1 and n as in linear search's best/worst.
2. The `=` in `<=`. It protects the **one-element range** — the case where low == high is the last possible home of the target.
3. When the width is odd, halving leaves (w−1)/2 elements on one side and (w−1)/2 on the other *plus* the eliminated middle — the surviving side has at most ⌊w/2⌋ elements; for even widths one side has exactly w/2. "At most half" covers both parities; the bound ⌈log₂(n+1)⌉ uses the worst side.
</details>

---

# Chapter 17: Beyond Basic Search

## 17.1 First and last occurrence — duplicates demand precision

With duplicates, "the index" is ambiguous: `{1, 2, 2, 2, 3}` contains 2 at indexes 1, 2, 3. Counting, deleting, or range queries need the **first** or **last** occurrence specifically.

Chapter 16's algorithm returns *whichever* occurrence the halving happens to land on — the returned index varies with the array's shape. The fix is small and beautiful: **on a match, record it and keep searching on the desired side.**

Pseudocode for the **first** occurrence:

```text
answer = -1
while the search range exists
    calculate middle
    if middle matches
        save middle as answer
        move high left to search for an earlier match
    else if middle is too small
        move low right
    else
        move high left
return answer
```

The C#:

```csharp
static int FirstOccurrence(int[] numbers, int target)
{
    int low = 0;
    int high = numbers.Length - 1;
    int answer = -1;

    while (low <= high)
    {
        int middle = low + (high - low) / 2;

        if (numbers[middle] == target)
        {
            answer = middle;
            high = middle - 1;
        }
        else if (numbers[middle] < target)
        {
            low = middle + 1;
        }
        else
        {
            high = middle - 1;
        }
    }

    return answer;
}
```

New lines, line by line:

| Line | What it does |
|---|---|
| `int answer = -1;` | The **so-far-best** candidate, sentinel-initialized — the accumulator pattern (8.5) applied to a position. |
| `answer = middle;` | On a match: *record* it — but do **not** return. An earlier match may exist. |
| `high = middle - 1;` | On a match: continue searching **left** — an earlier occurrence can only be there. The range keeps shrinking, so termination is untouched. |

Invariant worth savoring: *at every step, if the first occurrence exists, it is either already saved in `answer` or lies in [low, high].* Termination leaves `answer` = the leftmost match ever seen. For the **last** occurrence, mirror one line: on a match set `low = middle + 1`.

Complexity: still O(log n) — each iteration still halves the range; recording costs O(1). On `{1, 2, 2, 2, 3}` target 2: middle 2 matches → answer 2, search left; middle 0 (1) < 2 → low = 1; middle 1 (2) matches → answer 1, search left; range empty → **return 1**. ✓

## 17.2 Search choice — the decision table

| Situation | Algorithm | Why |
|---|---|---|
| Unsorted data, one lookup | **Linear search** | sorting costs O(n log n) > one O(n) scan (12: 15.5's optimality) |
| Sorted data, repeated lookups | **Binary search** | O(log n) each, precondition already paid |
| Repeated key→value lookups | **Dictionary / hash set** (Part VIII) | expected O(1), no order requirement |
| Prefix / range conditions | **Specialized index or tree** (Part XII) | order + structure queries |
| Small n (tens) | Linear, honestly | constants beat asymptotics (13.8) |

The professional reflex: *how many lookups, over what data shape, in what order?* — then the table answers itself.

### Exercises for Chapter 17

1. Modify `FirstOccurrence` into `LastOccurrence` — exactly which lines change?
2. In `{5, 5, 5, 5}`, what does `FirstOccurrence` return, and after how many match-recordings?

<details><summary>Solutions</summary>

1. Two lines: on a match, `low = middle + 1;` replaces `high = middle - 1;` (keep searching **right**), and the method name/docstring. The invariant mirrors: *the last occurrence is either saved or lies in [low, high].*
2. Returns 0 (the first 5) after two recordings (indexes 1 then 0): middle 1 → answer 1, go left; middle 0 → answer 0, go left; range empty. Answer 0. ✓
</details>

---
# Part VII — Sorting Algorithms

Sorting is the most-studied problem in computer science — because *order* unlocks everything else: binary search, duplicate detection, medians, readable reports, efficient merges. This part builds the canon: selection sort, insertion sort, merge sort, quicksort — then the professional question of *which one, when*.

---

# Chapter 18: Why Sorting Helps

Sorting is never only about sorting. An sorted array is a **precondition amplifier** — it converts weaker structures into stronger capabilities:

- **binary search** needs ordered data (Chapter 16's precondition);
- **duplicate detection** becomes "compare neighbors" — adjacent equal values cluster together — instead of an O(n²) all-pairs scan or an O(n)-space hash set;
- **statistics** unlock: the *median* is literally a position in sorted order (Chapter 45);
- **reports** become readable: top sellers, chronological events, ranked pages;
- **merging** two sorted streams is O(n) (the `Merge` of Chapter 21 is that operation in isolation).

The honest accounting: sorting **costs** time (at least O(n log n) for comparison-based sorting — a lower bound you can feel in 21.5) and sometimes memory. The engineering question is always: *will the amortized benefit across many later operations repay the one-time sort?* With repeated searches, almost always yes.

---

# Chapter 19: Selection Sort

## 19.1 The idea

The most human algorithm in this book — how you might sort cards by hand, the laziest possible way:

> Repeatedly **select** the smallest remaining card, and put it at the front of the unsorted region.

The array grows a **sorted prefix** on the left; each round appends exactly one element to it. After n−1 rounds, everything is sorted.

```text
[ unsorted ................ ] sorted-prefix grows from left
       ↑ scan for the minimum
       swap it to the boundary
```

## 19.2 The code

```csharp
static void SelectionSort(int[] numbers)
{
    for (int start = 0; start < numbers.Length - 1; start++)
    {
        int smallestIndex = start;

        for (int index = start + 1; index < numbers.Length; index++)
        {
            if (numbers[index] < numbers[smallestIndex])
            {
                smallestIndex = index;
            }
        }

        (numbers[start], numbers[smallestIndex]) =
            (numbers[smallestIndex], numbers[start]);
    }
}
```

## 19.3 Line by line

| Line | What it does |
|---|---|
| `for (int start = 0; start < numbers.Length - 1; start++)` | `start` is the **boundary**: the first slot of the unsorted region. Runs to `Length - 1` because a final single remaining element is automatically in place. |
| `int smallestIndex = start;` | Assumption: the boundary element is the smallest — until disproven (Chapter 1.3's maximum logic, mirrored). |
| `for (int index = start + 1; ...)` | The scan over *everything right of the boundary*. |
| `if (numbers[index] < numbers[smallestIndex])` | A smaller candidate appears... |
| `smallestIndex = index;` | ...remember **where** it is (position, not value — we must swap positions). |
| `(numbers[start], numbers[smallestIndex]) = (numbers[smallestIndex], numbers[start]);` | **Tuple swap**: the right side builds a pair of the two values; the left side destructures that pair back into the two slots in reversed roles. Two values exchange places in one statement, no temporary variable. |

Word by word — the tuple swap: `(a, b) = (b, a)` reads "assign b's old value to a, and a's old value to b, simultaneously". Both right-side values are read *before* any left-side write — that is what makes the simultaneous exchange safe.

## 19.4 Trace on `{5, 2, 8, 1}`

| round | start | scan finds min at | array after swap |
|---:|---:|---:|---|
| 1 | 0 | index 3 (value 1) | `{1, 2, 8, 5}` |
| 2 | 1 | index 1 (value 2 — already in place) | `{1, 2, 8, 5}` |
| 3 | 2 | index 3 (value 5) | `{1, 2, 5, 8}` ✓ |

Round 2 shows the self-swap (index 1 with itself) — harmless; a `if (smallestIndex != start)` guard would skip it.

## 19.5 Complexity — count honestly

Comparisons: round 1 scans n−1, round 2 scans n−2, ..., last round scans 1. Total = (n−1) + (n−2) + ... + 1 = **n(n−1)/2** — the arithmetic series sum, ≈ n²/2. That is **O(n²)** *regardless of input order*: even a fully sorted array pays the full scan (the algorithm is too unsophisticated to notice). Swaps: exactly n−1 — at most one per round, which is selection sort's one virtue (when writes are expensive, this matters). **Space O(1)** — everything happens inside the original array (**in-place**).

## 19.6 Stability note

Selection sort as written is **not stable** (23.1 defines the word): the swap can leap a value over an equal one, reordering equal-key records. If stability matters, choose insertion or merge sort.

### Exercises for Chapter 19

1. How many comparisons does selection sort perform on `{1, 2, 3}` exactly? And swaps?
2. Why is the outer loop `Length - 1` and not `Length`?

<details><summary>Solutions</summary>

1. 2 + 1 = 3 comparisons; swaps: round 1 finds min already at 0 (self-swap), round 2 likewise → 0 real swaps (or 2 counting self-swaps; both self-swaps are no-ops).
2. When one element remains unsorted, all others are smaller and already placed to its left — a final round would scan an empty region and self-swap; harmless but pointless.
</details>

---

# Chapter 20: Insertion Sort

## 20.1 The idea

How careful people *actually* sort cards:

> Take the next card; **insert** it into its correct place among the already-sorted cards; repeat.

The sorted prefix grows rightward — not by *selecting* the global minimum, but by *placing* each new element where it belongs *locally*. That local placement is what gives insertion sort its legendary behavior on nearly-sorted data.

```text
[ sorted prefix ... ] | next → shift larger values right, drop it in the hole
                       ↑ boundary
```

## 20.2 The code

```csharp
static void InsertionSort(int[] numbers)
{
    for (int index = 1; index < numbers.Length; index++)
    {
        int current = numbers[index];
        int position = index - 1;

        while (position >= 0 && numbers[position] > current)
        {
            numbers[position + 1] = numbers[position];
            position--;
        }

        numbers[position + 1] = current;
    }
}
```

## 20.3 Line by line

| Line | What it does |
|---|---|
| `for (int index = 1; ...)` | Starts at **1**: a one-element prefix (element 0) is trivially sorted; each round admits one new element. |
| `int current = numbers[index];` | **Lift** the new element out — its slot becomes a conceptual hole. |
| `int position = index - 1;` | The probe starts at the sorted prefix's right edge. |
| `while (position >= 0 && numbers[position] > current)` | Two conditions **in order**: (1) not past the left end — 56's short-circuit lesson; (2) prefix element still too large. Both true → shift. |
| `numbers[position + 1] = numbers[position];` | **Shift** the too-large value one slot right — into the hole; the hole moves left. |
| `position--;` | Probe the next candidate leftward. |
| `numbers[position + 1] = current;` | The while died (prefix exhausted or a small-enough neighbor found) — **drop `current` into the hole**. |

Word by word — the `&&`: C# evaluates left condition first; if `position >= 0` is false it **never touches** `numbers[position]` (short-circuit). Reversing the two conditions yields an out-of-bounds read at position −1 — the most classic C-family crash, grown here in miniature.

## 20.4 Trace on `{5, 2, 4, 1}`

| round | current | shifts performed | array after |
|---:|---:|---|---|
| index 1 | 2 | 5 shifts right | `{2, 5, 4, 1}` |
| index 2 | 4 | 5 shifts right | `{2, 4, 5, 1}` |
| index 3 | 1 | 5, 4, 2 shift right | `{1, 2, 4, 5}` ✓ |

Round "index 2" in slow motion: hole at 2; probe 5 > 4 → shift `{2, 5, 5}`; probe 2 > 4? no → drop 4 at position+1 → `{2, 4, 5}`. The element traveled exactly two slots — *only as far as needed*.

## 20.5 Complexity — the adaptive champion

- **Worst case** (reverse-sorted input): each element shifts past the entire prefix → 1 + 2 + ... + (n−1) = n(n−1)/2 comparisons+shifts → **O(n²)**.
- **Best case** (already sorted): each `current` fails the while-test immediately — one comparison per element → **O(n)**. The algorithm *notices* order.
- **Nearly sorted**: close to O(n) — a handful of shifts per element. This is why real libraries (including .NET's hybrid sorts) **switch to insertion sort for small runs** — Chapter 23.

**Space O(1)**, in-place; **stable** (equal elements never leap each other: `>` stops before shifting an equal value, preserving original order among equals).

### Exercises for Chapter 20

1. On `{1, 2, 3, 4}` (sorted input), how many comparisons total? What is that in O-terms?
2. Which single symbol in the while-line controls stability, and how?

<details><summary>Solutions</summary>

1. Exactly n−1 = 3 (each round: one failed comparison) → O(n) — the best case realized.
2. The `>` in `numbers[position] > current`. With `>=`, an equal prefix value would shift right, letting `current` land *before* an equal that was *originally earlier* — unstable. With strict `>`, equals never reorder.
</details>

---

# Chapter 21: Merge Sort

## 21.1 The idea

The first *divide and conquer* algorithm of the book (the pattern gets its own chapter at 33):

```text
        split in half         solve each half          weave together
        ┌───────────┐         ┌───────────┐          ┌───────────┐
{5,2,8,1,9,3}  ──►  {5,2,8} + {1,9,3}  ──►  {2,5,8} + {1,3,9}  ──►  {1,2,3,5,8,9}
        divide                  conquer                    combine
```

Two facts make it work:

1. **splitting is trivial** (cut at the middle — no comparisons needed);
2. **merging two sorted halves is linear and simple** — repeatedly take the smaller *front* element.

And the recursion: a half is sorted the same way — by halving *it* — until pieces of size ≤ 1, which are sorted *by definition*.

> A recursive note before Part X: a method may call **itself**; each call handles a smaller piece and trusts the deeper calls' answers. MergeSort calls MergeSort on the halves. Chapter 30 dissects the machinery — including the memory cost — completely.

## 21.2 The code — split

```csharp
static int[] MergeSort(int[] numbers)
{
    if (numbers.Length <= 1)
    {
        return numbers;
    }

    int middle = numbers.Length / 2;
    int[] left = numbers[..middle];
    int[] right = numbers[middle..];

    int[] sortedLeft = MergeSort(left);
    int[] sortedRight = MergeSort(right);

    return Merge(sortedLeft, sortedRight);
}
```

## 21.3 Line by line — split

| Line | What it does |
|---|---|
| `if (numbers.Length <= 1) return numbers;` | **Base case** (recursion's stopping point — 30.1): zero or one element is already sorted; return it unchanged. Without this line, infinite self-calls. |
| `int middle = numbers.Length / 2;` | The cut point; integer division floors it (7/2 = 3), so odd sizes put the extra element on the right — either side works. |
| `numbers[..middle]` | **Range expression** — "elements from the start **up to but excluding** index `middle`". `numbers[middle..]` — "from middle **through the end**". Both create *new* arrays (copies), leaving the input untouched. |
| `MergeSort(left)` / `MergeSort(right)` | The two **self-calls** — the same algorithm, promised to smaller inputs (halves). Trust them: they return sorted arrays. |
| `return Merge(...)` | The **combine** step — the only place real comparison-work happens. |

## 21.4 The code — merge (the heart)

```csharp
static int[] Merge(int[] left, int[] right)
{
    int[] result = new int[left.Length + right.Length];
    int leftIndex = 0;
    int rightIndex = 0;
    int resultIndex = 0;

    while (leftIndex < left.Length && rightIndex < right.Length)
    {
        if (left[leftIndex] <= right[rightIndex])
        {
            result[resultIndex++] = left[leftIndex++];
        }
        else
        {
            result[resultIndex++] = right[rightIndex++];
        }
    }

    while (leftIndex < left.Length)
    {
        result[resultIndex++] = left[leftIndex++];
    }

    while (rightIndex < right.Length)
    {
        result[resultIndex++] = right[rightIndex++];
    }

    return result;
}
```

## 21.5 Line by line — merge

| Line | What it does |
|---|---|
| `new int[left.Length + right.Length]` | The output — exactly sized, **new** memory (this is merge sort's O(n) space bill). |
| three index variables | Three fingers: one per input's unread front, one per output's next free slot. |
| first `while` | The main weaving: **both** sides still have elements. |
| `left[leftIndex] <= right[rightIndex]` | Take from the left on ties — the `<=` is precisely what makes merge sort **stable** (20.3's lesson, reapplied). |
| `result[resultIndex++] = left[leftIndex++];` | The densest line in the book — read it as two post-increments: *store left's front into result's next slot; then advance both fingers*. `x++` yields the old value *then* increments — so both slots used are the pre-increment ones, exactly the pairing we want. |
| second / third `while` | The **drain**: one side is exhausted; copy the other side's leftovers whole. Only one of these loops ever runs (the first while ended because one side hit its end). |

## 21.6 Trace — `{5, 2, 8, 1}` full recursion tree

```text
MergeSort({5,2,8,1})
├─ split → {5,2} and {8,1}
│   MergeSort({5,2})
│   ├─ split → {5}, {2}        (base cases)
│   └─ Merge({5},{2}) → {2,5}
│   MergeSort({8,1})
│   ├─ split → {8}, {1}        (base cases)
│   └─ Merge({8},{1}) → {1,8}
└─ Merge({2,5},{1,8})
    compare 2 vs 1 → take 1   → {1}
    compare 2 vs 8 → take 2   → {1,2}
    compare 5 vs 8 → take 5   → {1,2,5}
    left exhausted → drain 8  → {1,2,5,8}   ✓
```

Four elements: split (free) + one merge of size 2 + one merge of size 2 + one merge of size 4. The *only* comparisons in the entire sort happened inside merges: 1 + 1 + 3 = 5.

## 21.7 Complexity — the O(n log n) arithmetic

Two contributions:

- **Depth of splitting:** halving until size 1 → **log₂ n** levels (13.4).
- **Work per level:** every level's merges, *together*, touch all n elements once (level 1: two merges of n/2; level 2: four of n/4; each level totals n).

→ **O(n log n) time, on every input — best, average, worst.** No adversarial order punishes merge sort: the split is blind to values. **Space: O(n)** for the result arrays (plus O(log n) recursion stack — 30.4). This *guaranteed* behavior regardless of input order is merge sort's professional signature — and the price is the extra memory.

A boundary worth knowing: comparison-based sorting cannot beat O(n log n) in the worst case (the n! possible orderings of n elements must be distinguished, and each comparison splits the remaining possibilities into at most two camps; log₂(n!) ≈ n log₂ n by Stirling). Merge sort therefore sits at the theoretical floor — you cannot fundamentally out-sort it with comparisons, only match it with better constants (quicksort) or beat it with non-comparison tricks (counting/radix, out of scope but worth knowing they exist).

### Exercises for Chapter 21

1. Merge `{1, 4, 6}` and `{2, 3, 9}` by hand, writing each comparison's winner.
2. Why does only one of the two drain loops ever execute?
3. Where exactly does merge sort spend its O(n) memory, and why is quicksort (next chapter) stingier?

<details><summary>Solutions</summary>

1. 1v2→1; 4v2→2; 4v3→3; 4v9→4; 6v9→6; drain→9. Result `{1,2,3,4,6,9}` — five comparisons, one drain copy.
2. The first while ends exactly when *either* index reaches its end; at most one side can still have unread elements — the other is empty by construction.
3. The `result` array in `Merge` (allocated per level, n total per level, but O(n) alive at the deepest path). Quicksort partitions *inside* the original array — no per-level output allocation.
</details>

---

# Chapter 22: Quicksort

*An extension beyond the original guide — the fourth member of the canon, and the one inside most real libraries.*

## 22.1 The idea

Pick one element as the **pivot**. **Partition**: shuffle everything smaller to the pivot's left, everything larger to its right. The pivot is now *permanently, exactly* in its final sorted position — the only element with that guarantee. Recurse on the two sides.

```text
{5, 2, 8, 1, 6}   pivot 5
   partition: smaller-left | 5 | larger-right
      {2, 1}        5       {8, 6}
   recurse-left    done   recurse-right
```

Merge sort did its real work *after* recursion (merge); quicksort does its real work *before* recursion (partition). That inversion is what removes the O(n) output buffers.

## 22.2 The code

```csharp
static void QuickSort(int[] numbers, int low, int high)
{
    if (low >= high)
    {
        return;
    }

    int pivotIndex = Partition(numbers, low, high);

    QuickSort(numbers, low, pivotIndex - 1);
    QuickSort(numbers, pivotIndex + 1, high);
}

static int Partition(int[] numbers, int low, int high)
{
    int pivotValue = numbers[high];
    int boundary = low - 1;

    for (int index = low; index < high; index++)
    {
        if (numbers[index] <= pivotValue)
        {
            boundary++;
            (numbers[boundary], numbers[index]) = (numbers[index], numbers[boundary]);
        }
    }

    (numbers[boundary + 1], numbers[high]) = (numbers[high], numbers[boundary + 1]);

    return boundary + 1;
}
```

## 22.3 Line by line — QuickSort

| Line | What it does |
|---|---|
| `if (low >= high) return;` | Base case: a range of 0 or 1 elements is sorted — nothing to do. `return` in a `void` method simply stops (7.5). |
| `Partition(...)` | Does the round's real work; returns where the pivot *landed*. |
| two self-calls | Sort the sides **excluding** the pivot — it is finished, final, immovable. `pivotIndex - 1` / `+ 1`: those off-by-ones *are* the correctness. |

## 22.4 Line by line — Partition (Lomuto scheme)

| Line | What it does |
|---|---|
| `int pivotValue = numbers[high];` | Choose the last element as pivot. Simple; consequences in 22.6. |
| `int boundary = low - 1;` | The **wall**: everything at indexes ≤ boundary is ≤ pivot. Starts *before* the range: nothing has been proven small yet. |
| `for (int index = low; index < high; index++)` | Walk every non-pivot element. |
| `if (numbers[index] <= pivotValue)` | A small one appears... |
| `boundary++;` | ...extend the small-side wall to claim it... |
| `swap(boundary, index)` | ...by swapping the newcomer with the wall's next slot (often itself — a self-swap, harmless). |
| final swap `boundary + 1 ↔ high` | Lift the pivot over the wall into its **final position**: smalls left, larges right. |
| `return boundary + 1;` | Report the pivot's final index — the fact QuickSort's recursion needs. |

**Invariant of the walk** (12's tool, applied): *at every loop step, `numbers[low..boundary]` are all ≤ pivot, and `numbers[boundary+1..index-1]` are all > pivot.* The wall's definition *is* the invariant — and the final swap's correctness is nothing but the invariant plus one more exchange.

## 22.5 Trace — Partition on `{5, 2, 8, 1, 6}` (low=0, high=4, pivot=6)

| index | value | ≤ 6? | boundary | array after |
|---:|---:|---|---:|---|
| start | — | — | −1 | `{5, 2, 8, 1, 6}` |
| 0 | 5 | yes | 0 | `{5, 2, 8, 1, 6}` (self-swap) |
| 1 | 2 | yes | 1 | `{5, 2, 8, 1, 6}` (self-swap) |
| 2 | 8 | no | 1 | unchanged |
| 3 | 1 | yes | 2 | `{5, 2, 1, 8, 6}` (swap 8↔1) |
| final | — | — | — | swap idx 3↔4: `{5, 2, 1, 6, 8}`, return 3 |

Pivot 6 landed at index 3: left `{5,2,1}` all ≤ 6, right `{8}` > 6. ✓ Then `QuickSort(0,2)` and `QuickSort(4,4)` (base case) finish the story.

## 22.6 Complexity — the best, the worst, and why libraries care

- **Best/average:** pivots split roughly in half → recursion depth ~log n, each level partitions O(n) total → **O(n log n)** — with *tighter constants than merge sort* (partition is cache-friendly swaps inside one array; merge copies to fresh arrays).
- **Worst:** pivots are always extreme (sorted input + last-element pivot) → every partition peels off *one* element → depth n → **O(n²)**. On `{1,2,3,...}` ascending, this Lomuto-last-pivot degrades exactly so.
- **Space:** O(log n) average recursion stack; O(1) data movement beyond swaps — **in-place**.

This is why production quicksorts randomize or mediate pivot choice ("median-of-three") — defeating adversaries and sorted data alike. .NET's `Array.Sort` is precisely such a hybrid: introspective quicksort for large ranges, **insertion sort below ~16 elements** (20.5's adaptiveness, monetized), heapsort fallback if recursion deepens pathologically. Real engineering is a composition of this book's chapters.

### Exercises for Chapter 22

1. Partition `{3, 8, 2, 5}` by hand (pivot = 5, last). Show every boundary move and the return value.
2. Why must the recursion exclude the pivot's index?

<details><summary>Solutions</summary>

1. boundary=−1. idx0: 3≤5 → b=0, self-swap `{3,8,2,5}`. idx1: 8>5, skip. idx2: 2≤5 → b=1, swap idx1↔2 → `{3,2,8,5}`. Final swap b+1=2 ↔ high=3 → `{3,2,5,8}`, return 2.
2. The pivot is *final*: partitioning proved smaller-left/larger-right around exactly that position. Including it would re-partition a settled element and destroy the invariant of the next round; excluding it is what makes ranges strictly shrink (termination, again).
</details>

---

# Chapter 23: Stability Built-ins and Choosing a Sort

## 23.1 Stability — the invisible requirement

A sort is **stable** if records with **equal keys keep their original relative order**.

Why it matters: multi-criteria sorting. Sort transactions by *time*, then stably by *customer* — each customer's transactions remain time-ordered within their group. An unstable sort silently scrambles that inner order. Concrete: rows `("Ann", 2), ("Bob", 1), ("Ann", 1)` sorted stably by name → `("Ann", 2), ("Ann", 1), ("Bob", 1)` — the two Anns kept their original 2-then-1 order.

| Algorithm | Time (avg / worst) | Space | Stable | Signature strength |
|---|---|---|---|---|
| Selection | O(n²) / O(n²) | O(1) | no | minimum swaps (n−1) |
| Insertion | O(n²) / O(n²) — **O(n) sorted** | O(1) | **yes** | adaptive; tiny inputs |
| Merge | O(n log n) / O(n log n) | O(n) | **yes** | guaranteed, streaming-friendly |
| Quick | O(n log n) / O(n²) | O(log n) | no | fastest constants in practice |

## 23.2 Built-in sorting — the professional default

For production C#, prefer a well-tested library sort unless learning or a special requirement makes custom code appropriate:

```csharp
int[] sorted = numbers.OrderBy(value => value).ToArray();   // LINQ: stable, new sequence
Array.Sort(numbers);                                        // in-place, fast, unstable
```

Word by word:

- `OrderBy(value => value)` — LINQ's sort: `value => value` is a **lambda** — a tiny inline function mapping each element to its sort key; order by the element itself, here. LINQ sorts are documented stable (the 23.1 promise kept) and return *new* sequences (`.ToArray()` materializes).
- `Array.Sort(numbers)` — the in-place workhorse: reorders the actual array, uses the hybrid quicksort of 22.6, and is *not* guaranteed stable.

The mastery position: **know the algorithmic ideas even when you use the library** — because one day the requirement (stability, memory ceiling, streamed input, exotic keys) will push you off the default path, and that day you must know which door to open.

## 23.3 Choosing — the decision sketch

- Tiny arrays (≲ 16): insertion sort — constants win.
- Need stability: insertion (small), merge (large), or LINQ `OrderBy`.
- Need worst-case guarantees (real-time, adversarial data): merge sort's O(n log n) floor.
- Memory-tight, average-speed: quicksort family.
- Nearly-sorted streams: insertion's O(n) adaptivity.

> The correct answer to "which sort?" is always a *question*: how big, how ordered, how memory-tight, does stability matter, who is the adversary?

### Exercises for Chapter 23

1. You must sort a million records by priority, then stably by department. Which two-call composition is correct, and why is the *order* of the two calls not interchangeable?
2. Name the situation where quicksort is the wrong tool despite being fastest on average.

<details><summary>Solutions</summary>

1. First `OrderBy(priority)` (unstable even — it establishes the *inner* order), then `OrderBy(department)` with a **stable** sort — stability preserves priority order within each department. Reversed order would destroy priority grouping, because the unstable first call's inner order is what the stable second call protects.
2. Adversarial or pre-sorted data with a predictable pivot rule (worst case O(n²)); or hard real-time / memory-unpredictable constraints, where merge sort's guarantee wins; or when stability is required and the library quicksort is unstable.
</details>

---
# Part VIII — Hashing Maps and Sets

The patterns so far answered questions *once*. This part answers the question asked **thousands of times**: *"have I seen this before?"* — and answers it in ~one step, every time, by trading memory for speed.

---

# Chapter 24: The Hash Idea from Zero

## 24.1 The lookup problem

Suppose you must answer thousands of questions:

> "Have we already seen this ID?" — for visitor IDs streaming past your desk.

Strategy 1 — scan the list of past IDs per question: each answer costs O(n) (Chapter 15, no order to exploit). Ten thousand questions over a growing list of a million IDs → ~10¹⁰ comparisons. Hopeless.

Strategy 2 — keep IDs somewhere you can jump to *directly*. That "somewhere" is a **hash table**, and it usually answers in **expected O(1)** — a fixed handful of steps regardless of whether the list holds ten IDs or ten million.

## 24.2 How hashing works — the machinery, from zero

The core trick has two moving parts:

**Part 1 — the hash function.** A mathematical function `H` that converts *any* key (an int, a string, an employee object) into an integer:

```text
H("apple")  → 948312
H("banana") → 104522
H("cherry") → 948312        ← collisions happen! (Part 2 deals with them)
```

Requirements on a good `H`: deterministic (same key → same integer, always), fast, and *spready* — scattering similar keys across the whole number range, so different keys rarely collide.

**Part 2 — the bucket array.** Take the hash integer, modulo the array size, and use it as a direct index:

```text
buckets: index = H(key) % 10

          0     1     2     3     4     5     6     7     8     9
        ┌────┬────┬────┬────┬────┬────┬────┬────┬────┬────┐
        │    │"ban│    │    │    │    │    │    │    │"app│
        │    │ana"│    │    │    │    │    │    │    │"le"│
        └────┴────┴────┴────┴────┴────┴────┴────┴────┴────┘
          104522 % 10 = 2              948312 % 10 = 9... (simplified)
```

Adding "apple": compute H, modulo, jump to bucket 9, store. Asking "is 'apple' present?": compute H *again*, modulo, jump to bucket 9, look. **The key itself tells you where it lives** — no scanning, no order required, one jump.

**Collisions.** Two keys can hash to the same bucket ("apple" and "cherry" above). Real tables resolve this by storing a *small chain* (linked list) inside each bucket, or by probing neighboring buckets. With a good hash function and a table kept roughly half-empty (resizing when it fills), chains stay ~1–2 elements long, and the *expected* work per operation stays O(1). This is why every complexity claim in this Part says **expected** O(1) — the *worst* case (all keys colliding into one bucket) degrades to O(n), an adversarial pathology. Appendix A records both numbers.

## 24.3 The two C# structures you get for free

The .NET library ships the machinery, twice, for two different question shapes:

```csharp
HashSet<string> seen = new();          // "IS this key present?"        → membership
Dictionary<string, int> counts = new(); // "WHAT value hangs on this key?" → mapping
```

| Structure | Question it answers | Core operations (expected) |
|---|---|---|
| `HashSet<T>` | "Is X in the set?" | `Add` O(1), `Contains` O(1), `Remove` O(1) |
| `Dictionary<K, V>` | "Give me the value stored under key K" | read/write by key O(1) |

Word by word — the *key* concept: a `Dictionary<K,V>` is a `HashSet` where each stored key carries a *satellite value*. The hash jump locates the key; the value rides along in the same slot. `Dictionary<string, int>` mapping words to counts is exactly Chapter 14.4's histogram — now you know the machinery beneath it.

The equality rule matters: hashing and equality must agree (two keys that are *equal* must hash identically, or the jump lands in the wrong bucket and the key "disappears"). For strings this is built in; for your own classes you must override both consistently — a classic production bug, which is why custom-type keys deserve a warning comment in real code.

---

# Chapter 25: Hashing in Action

## 25.1 Duplicate detection — one set, one pass

```csharp
static bool ContainsDuplicate(int[] numbers)
{
    HashSet<int> seen = new();

    foreach (int number in numbers)
    {
        if (!seen.Add(number))
        {
            return true;
        }
    }

    return false;
}
```

Line by line:

| Line | What it does |
|---|---|
| `HashSet<int> seen = new();` | The memory-for-speed purchase: a growing set of everything already visited. |
| `seen.Add(number)` | Attempts insertion; **returns `bool`** — `false` exactly when the value was already present. One library call fuses "test membership" and "insert if new". |
| `if (!seen.Add(number))` | The `!` negation: *Add reported failure* ⇒ the value pre-existed ⇒ duplicate found. Reading it aloud: "if adding failed...". |
| `return true;` | Early exit with the verdict — later elements never examined. |
| `return false;` | The walk completed clean: every add succeeded; all values distinct. |

**Trace on `{4, 7, 4}`:** add 4 ✓ → add 7 ✓ → add 4 fails → `true`. **On `{4, 7, 9}`:** all adds succeed → `false`.

**Complexity:** O(n) expected time — one hash operation per element — versus the naive all-pairs O(n²) (compare everything with everything), or the sort-then-neighbors O(n log n) (19) that *mutates or copies* the input. **Space: O(n)** — the set itself. The pattern's price, stated plainly: memory.

## 25.2 Two-sum with a dictionary — the complement lookup

**Problem:** given numbers and a target, find two *different positions* whose values sum to the target; return the pair of indexes or "none".

**The hash idea, one sentence:** while scanning, for each value `x`, ask the dictionary — in O(1) — whether the **complement** `target - x` was seen *earlier*.

```csharp
static (int First, int Second)? FindTwoSum(int[] numbers, int target)
{
    Dictionary<int, int> indexByValue = new();

    for (int index = 0; index < numbers.Length; index++)
    {
        int needed = target - numbers[index];

        if (indexByValue.TryGetValue(needed, out int previousIndex))
        {
            return (previousIndex, index);
        }

        indexByValue[numbers[index]] = index;
    }

    return null;
}
```

Line by line, and word by word for the new pieces:

| Piece | What it does |
|---|---|
| `(int First, int Second)?` | **Nullable value tuple**: a value-tuple of two named ints, *or* `null` for "no answer" — the sentinel idea (−1 in 15.3) lifted to pairs. The `?` is what permits "no answer" without inventing fake indexes. |
| `Dictionary<int, int> indexByValue` | The map: *value seen earlier → its index*. The key is the data, the value is where it lives — inverted from how arrays store it. |
| `int needed = target - numbers[index];` | The **complement**: the one value that, added to the current, hits the target. Computing it costs one subtraction. |
| `indexByValue.TryGetValue(needed, out int previousIndex)` | The O(1) question, packaged: "does key `needed` exist?" — returns `bool`, and writes the found value into `previousIndex` *through* the `out` parameter. |
| `out int previousIndex` | **`out`**: an argument the method writes into — the method's second output channel. Declare-in-place with `out int x`, then read `x` after the call returns true. |
| `return (previousIndex, index);` | Earlier partner first, current second — a documented convention. |
| `indexByValue[numbers[index]] = index;` | *After* the failed lookup: record today's value for tomorrow's complements. Order matters: asking before storing prevents an element pairing with itself. |
| `return null;` | Walk finished, no complement ever found. |

**Reasoning, restated as the invariant:** *after processing k elements, the dictionary contains exactly the first k values → their indexes.* Each new element consults this complete record of the past — so if any valid pair exists with the current element as the *later* member, this iteration finds it. Pairs are never missed; each is discovered at its later end.

**Trace on `{2, 7, 11, 15}`, target 9:**

| index | value | needed | in dict? | action |
|---:|---:|---:|---|---|
| 0 | 2 | 7 | no (empty) | store 2→0 |
| 1 | 7 | 2 | **yes** (idx 0) | return (0, 1) ✓ |

**Complexity:** O(n) expected time, O(n) space — versus the sorted two-pointer's O(n log n) time / O(1) space (14.2) and the naive O(n²). One problem, three cost profiles — the trade-off table skill of Chapter 57 in miniature:

| Approach | Time | Extra space | Precondition | Mutates input? |
|---|---|---|---|---|
| Naive pairs | O(n²) | O(1) | none | no |
| Sort + two pointers | O(n log n) | O(1) | (created by) sorting | typically yes |
| Hash map | **O(n)** | **O(n)** | none | no |

## 25.3 Hashing trade-offs — the honest ledger

Hash structures are not free. The bill:

- **Memory:** O(n) — often the dominant cost of an algorithm that "felt free" while coding. On a billion items, the *set itself* is the problem.
- **No order:** a hash table's iteration order is an implementation accident. Need sorted output, min/max, or range queries? The hash set cannot help — that is tree territory (Part XII).
- **Hash-quality dependence:** performance assumes good hashing and equality (24.3); pathological or adversarial inputs degrade expected O(1) toward O(n) worst case.
- **Constants:** per-operation hashing (computing H for a long string, say) is heavier than one integer comparison — for tiny n, a linear scan can genuinely win (13.8 again).

Use hash structures when **fast membership or key lookup is central** — which is precisely the shape of duplicate detection, two-sum, counting, grouping, caching, deduplication, and the Algorithm Lab's analysis passes. That shape-recognition is the deliverable of this Part.

### Exercises for Chapter 25

1. Write `FirstRepeatedValue` (Chapter 10's pseudocode!) as real C# using a `HashSet<string>`.
2. In `FindTwoSum`, why does moving the *store* line before the *lookup* break correctness? Give the smallest failing input.
3. Your colleague replaces `Dictionary<int,int>` with `List<int>` + `Contains`. What changes in the complexity table, and when might they still be right?

<details><summary>Solutions</summary>

1. `HashSet<string> seen = new(); foreach (string s in items) { if (!seen.Add(s)) return s; seen.Add is fused — simply `if (!seen.Add(s)) return s; } return null;` — literally the Chapter 10 pseudocode with the set's fused test-and-add.
2. Input `{3}`, target 6: needed = 3, now *already stored* → returns (0, 0), pairing the element with itself. The pair must use two different positions; ask-before-store is the guard.
3. Lookup becomes O(n) per element → total O(n²) — the entire hash advantage forfeited. They might still be right for n in the dozens (no hashing constants, better locality) or in memory-starved environments — 13.8's discipline, applied honestly.
</details>

---
# Part IX — Stacks Queues and Linked Lists

Three structures, three disciplines of *order*. Stacks and queues are **policies** — rules about who leaves first. Linked lists are a **connectivity** idea — data chained by references. All three underlie algorithms from undo-history to breadth-first search.

---

# Chapter 26: The Stack

## 26.1 The idea — last in, first out

A stack is a pile of plates: you put new plates **on top**, and you also take from **the top**. The most recent arrival is the first departure — **LIFO**, *last-in, first-out*.

```text
   push("details")          pop() → "details"
        │                        ▲
        ▼                        │
   ┌─────────┐             ┌─────────┐
   │ details │  ← top      │  home   │  ← top (now exposed)
   ├─────────┤             └─────────┘
   │  home   │
   └─────────┘
```

Only the top is reachable — that restriction *is* the data structure. Everything else is hidden until the items above it leave.

## 26.2 The C# — word by word

```csharp
Stack<string> pages = new();
pages.Push("home");
pages.Push("details");
string lastPage = pages.Pop();
```

| Piece | What it does |
|---|---|
| `Stack<string>` | the library's stack of strings (generic — 6.4) |
| `Push("home")` | place an element **on top** — O(1) |
| `Push("details")` | ...and another; "details" is now the top |
| `Pop()` | **remove and return the top** ("details") — O(1). Calling `Pop` on an empty stack throws — check `Count` or `TryPop` first |
| `Peek()` | *(mentioned for completeness)* look at the top **without removing** — O(1) |

## 26.3 What stacks are for

The stack discipline powers:

- **undo operations** — each action pushes a record; undo pops the latest;
- **browser history** — back = pop the current page to reveal the previous;
- **expression evaluation** — operators wait on a stack until their operands resolve;
- **depth-first search** — explore one path fully before others: push neighbors, pop to continue (39);
- **matching parentheses/brackets** — the most recent opened bracket must be the first closed (Chapter 28).

The unifying test: *if the answer to "which do we handle next?" is always "the most recent one"*, the structure is a stack.

---

# Chapter 27: The Queue

## 27.1 The idea — first in, first out

A queue is the checkout line: newcomers join at the **back**, service happens at the **front**. Earliest arrival leaves first — **FIFO**, *first-in, first-out*.

```text
 enqueue at back                       dequeue at front
      │                                       ▲
      ▼                                       │
 back ┤ job-2 │ job-1 ├ front
 (newest joins here)              (oldest leaves here)
```

## 27.2 The C# — word by word

```csharp
Queue<string> jobs = new();
jobs.Enqueue("job-1");
jobs.Enqueue("job-2");
string nextJob = jobs.Dequeue();
```

| Piece | What it does |
|---|---|
| `Queue<string>` | the library's FIFO structure |
| `Enqueue(...)` | join the **back** — O(1) |
| `Dequeue()` | remove and return the **front** — here `"job-1"`, the oldest — O(1); throws when empty (`TryDequeue` exists) |

## 27.3 What queues are for

- **customer service order** — fairness *is* FIFO;
- **breadth-first search** — explore by distance layers: first the neighbors at distance 1, then 2... (Chapter 38);
- **background work** — print jobs, email sends, video encodes: producers enqueue, workers dequeue;
- **message processing** — pipelines between systems.

The unifying test: *if "which next?" is always "the oldest waiting one"*, the structure is a queue.

**Stack vs queue — one glance:**

| | Stack | Queue |
|---|---|---|
| Discipline | LIFO — most recent first | FIFO — oldest first |
| Enter at | top | back |
| Leave from | top | front |
| Archetype | undo, DFS, parsing | fairness, BFS, pipelines |

---

# Chapter 28: Parentheses Validation

The canonical interview-level use of order discipline — solved here *without* a stack first, then *with* one when the problem grows teeth.

## 28.1 The easy version — one bracket type, a counter

Valid: every `(` eventually gets its `)` and never a `)` without its `(`.

```csharp
static bool HasBalancedParentheses(string text)
{
    int balance = 0;

    foreach (char character in text)
    {
        if (character == '(')
        {
            balance++;
        }
        else if (character == ')')
        {
            balance--;

            if (balance < 0)
            {
                return false;
            }
        }
    }

    return balance == 0;
}
```

Line by line:

| Line | What it does |
|---|---|
| `int balance = 0;` | The accumulator: *opens minus closes so far* — an integer acting as a "stack depth" counter. |
| `balance++` / `balance--` | An open raises the depth; a close lowers it. |
| `if (balance < 0) return false;` | The **early-ordering rule**: a close with nothing to close is invalid **the instant it happens** — `"())("` fails here at index 2, though the final balance is 0. Order, not just counts. |
| `return balance == 0;` | The walk ended: valid iff nothing is left unclosed (all opens matched). |

**Trace `"(())()"`:** +1 +1 −1 −1 +1 −1 → never negative, ends 0 → true. **Trace `"())("`:** +1 −1 **−1 → false immediately** — even though the string contains three of each bracket... two opens, two closes; the counter would end at 0, but the early dip below zero betrays the ordering violation.

## 28.2 The real version — multiple bracket types, a stack

`"([)]"` is invalid: `(` was opened last, so `)` must wait for `]` first. A **counter cannot remember who opened when** — but a stack *is* that memory.

> Rule: push each opener; on each closer, the **top** of the stack must be its matching opener — pop it. Any mismatch, or a non-empty stack at the end, is invalid.

```csharp
static bool HasBalancedBrackets(string text)
{
    Stack<char> openers = new();
    Dictionary<char, char> closerToOpener = new()
    {
        [')'] = '(',
        [']'] = '[',
        ['}'] = '{'
    };

    foreach (char character in text)
    {
        if (character is '(' or '[' or '{')
        {
            openers.Push(character);
        }
        else if (closerToOpener.ContainsKey(character))
        {
            if (openers.Count == 0 || openers.Pop() != closerToOpener[character])
            {
                return false;
            }
        }
    }

    return openers.Count == 0;
}
```

New pieces, word by word:

| Piece | What it does |
|---|---|
| `closerToOpener` | A **lookup map** from each closer to its required opener — the pairing rule as *data*, not nested ifs (the hash map of Part VIII buying O(1) pairing). |
| `character is '(' or '[' or '{'` | **Pattern matching on a constant set** — modern C#'s readable membership test for single values. |
| `openers.Count == 0 \|\| ...` | Short-circuit (20.3!): a closer with an empty stack is invalid *before* we may `Pop` — evaluating `Pop` first would throw. |
| `openers.Pop() != closerToOpener[character]` | The heart: the **most recent unmatched opener** must exactly match this closer. LIFO discipline = bracket mathematics. |
| `return openers.Count == 0;` | End of input: every opener must have been consumed. |

**Trace `"([)]"`:** push `(`, push `[` → see `)`: top is `[` ≠ `(` → **false** — the interleaving is caught red-handed. **Trace `"([])"`:** push `(`, push `[` → `]`: pop `[` ✓ → `)`: pop `(` ✓ → empty stack, true.

**Complexity:** O(n) time — one stack operation per character; O(n) worst-case space (all openers, e.g. `"((((("`).

---

# Chapter 29: Linked Lists

## 29.1 The idea — data chained by references

An array stores elements in *one contiguous block*, indexed by arithmetic (6.3). A **linked list** stores each element in its own **node** — a small object holding the value *plus a reference to the next node*. The chain, not memory adjacency, defines the order:

```text
head ──► ┌────────┐    ┌────────┐    ┌────────┐
         │ 10 │ ●─┼──►│ 20 │ ●─┼──►│ 30 │ /  │
         └────────┘    └────────┘    └────────┘
           value next    value next    value next=null
```

Reaching element #2 means *walking* from the head through two `Next` hops — there is no arithmetic shortcut. That is the cost; the payoff is surgical insertion and removal *when you are already standing at the spot*.

## 29.2 The C# — a node, word by word

```csharp
public sealed class Node<T>
{
    public Node(T value)
    {
        Value = value;
    }

    public T Value { get; }
    public Node<T>? Next { get; set; }
}
```

| Piece | What it does |
|---|---|
| `public sealed class` | `class` — a reference type: variables of this type hold *references to* objects, not the objects inside themselves (this is what makes chains possible). `sealed` — not intended for inheritance; the design is closed. |
| `Node<T>` | Generic over the payload type: the *chaining machinery* is identical for int-lists, string-lists, anything-lists. |
| `public Node(T value)` | **Constructor**: the special method run at creation (`new Node<int>(5)`); it receives the payload... |
| `Value = value;` | ...and stores it. The parameter `value` is copied into the property `Value` — the capital letter distinguishes the property from the parameter. |
| `public T Value { get; }` | **Property with a getter only**: readable from outside, settable only at construction — the payload is immutable by design. |
| `public Node<T>? Next { get; set; }` | The chain link: readable *and* writable. `Node<T>?` — the `?` marks it **nullable**: a `Node<T>` or `null`; `null` is how the final node signals "no next" (the `/` in the diagram). |

Building a chain, and reading it back:

```csharp
Node<int> head = new(10);
head.Next = new(20);
head.Next.Next = new(30);

for (Node<int>? current = head; current is not null; current = current.Next)
{
    Console.WriteLine(current.Value);        // 10, 20, 30
}
```

Word by word — the walk loop: `current is not null` (the modern "not null" test) guards the dereference; `current = current.Next` is the hop. The loop is O(n) — and n hops is the *only* way to reach the middle: **no random access**.

## 29.3 The trade-off table — the whole chapter in one grid

| Operation | Array | Linked list |
|---|---|---|
| Access element #k | **O(1)** — arithmetic | O(k) — walk from head |
| Insert/remove at *known* position | O(n) — shift the tail | **O(1)** — rewire two references |
| Insert/remove at front | O(n) — shift everything | **O(1)** |
| Memory | one block, tight | one object per node + reference overhead |
| Cache friendliness | excellent (adjacent) | poor (scattered allocations) |

The `Insert at list beginning` row of Appendix A (O(n) for `List<T>`) is precisely why linked lists *exist* — constant-time front insertion that arrays cannot match.

**Engineering verdict.** In most everyday C# application code, **`List<T>` is the better default**: it wins access, cache locality, and simplicity; the append-at-end pattern dominates real workloads. Learn linked lists to understand *reference-based structures* and the trade-off arithmetic — and to meet them inside hash-table buckets (24.2), where they quietly serve. When *you* need a stack or queue, use `Stack<T>`/`Queue<T>` (built on list-like machinery, but exposing exactly the discipline of Chapters 26–27).

### Exercises for Part IX

1. Simulate `Push(1) Push(2) Push(3) Pop() Pop()` on paper; what remains?
2. Same sequence with a queue (`Enqueue`/`Dequeue`); what remains?
3. Why does `"(()"` fail validation, and *which* return line catches it?
4. Write the invariant of the multi-bracket validator's loop.

<details><summary>Solutions</summary>

1. Stack: after pops the top two leave → **1** remains (LIFO removed 3 then 2).
2. Queue: FIFO removes 1 then 2 → **3** remains. Same operations, opposite survivor — the discipline, not the contents, decided.
3. Ends with balance 1 / stack `['(']` — the closes ran out. The counter version's final `return balance == 0` → false; the stack version's `return openers.Count == 0` → false. (The *early* failure lines were never triggered.)
4. *At each step, the stack contains exactly the currently-open, not-yet-matched openers in opening order (top = most recent).* Pushes maintain it trivially; a matching pop removes the most recent — exactly the definition; a mismatch or empty-pop means no valid sequence of openers can explain the input seen so far.
</details>

---
# Part X — Recursion and Backtracking

Recursion is the mind-expander of this book: a method that calls *itself*. Handled carelessly it is infinite and explosive; handled with discipline it is the most elegant tool in computer science — the native language of trees, graphs, divide-and-conquer, and backtracking.

---

# Chapter 30: Recursion from Zero

## 30.1 The idea — Russian dolls

A set of Russian dolls: to open the big one you must open the smaller one inside; to open *that* one, the smaller one inside *it*... until the tiniest doll, which is solid — it opens nothing.

That is recursion's entire anatomy:

- **the recursive case** — "solve this problem by first solving a *smaller* version of the same problem" (open the next doll inside);
- **the base case** — "the smallest problem is solved *directly*, without recursing" (the solid doll).

A recursive method solves *n* by delegating to *n−1*, which delegates to *n−2*... The chain of self-calls must **strictly shrink toward the base case**, or the dolls never end.

## 30.2 The three requirements of every recursive algorithm

1. **A base case** — at least one input solved directly (no self-call). Without it: infinite recursion.
2. **A smaller recursive call** — every self-call must move measurably *toward* a base case. Without it: infinite recursion wearing a disguise.
3. **A way to combine** — the answer is assembled from the smaller answers. Without it: calls happen but nothing is computed.

All three are *checkable by inspection* — before running anything. Checking them is the recursion proof of correctness (initialization→base case, maintenance→shrinking call, termination→the chain ends).

## 30.3 SumTo — the anatomy, fully dissected

> SumTo(n) = 1 + 2 + ... + n, with SumTo(0) = 0.

```csharp
static int SumTo(int number)
{
    if (number <= 0)
    {
        return 0;
    }

    return number + SumTo(number - 1);
}
```

Line by line:

| Line | Role | Requirement |
|---|---|---|
| `if (number <= 0) return 0;` | **Base case**: the smallest problem — the empty sum — answered directly. Note `<=` (not `==`): it also *defends* against negative input instead of recursing forever below zero. | #1 |
| `SumTo(number - 1)` | **The smaller call**: `number - 1` is one step closer to the base case — measurably smaller, every time. | #2 |
| `return number + SumTo(...);` | **The combine**: this level's number *plus whatever the deeper level returns*. Addition is the assembly. | #3 |

## 30.4 The call stack — what "happens" when you run it

A method call is not a jump; it is a **suspension**. When `SumTo(3)` calls `SumTo(2)`, the outer call *pauses mid-line* — it has computed nothing yet, it is waiting for a value to add `3` to. The runtime keeps every paused call alive on the **call stack** — a stack (Chapter 26!) of suspended frames:

```text
CALL phase (winding):                    RETURN phase (unwinding):

SumTo(3)                                 frame SumTo(0) returns 0        → 0
 └─ waits, calls SumTo(2)                frame SumTo(1) returns 1 + 0   → 1
     └─ waits, calls SumTo(1)            frame SumTo(2) returns 2 + 1   → 3
         └─ waits, calls SumTo(0)        frame SumTo(3) returns 3 + 3   → 6 ✓
             └─ base case! returns 0
```

As an arithmetic expression, the winding phase literally builds:

```text
SumTo(3)
= 3 + SumTo(2)
= 3 + 2 + SumTo(1)
= 3 + 2 + 1 + SumTo(0)
= 3 + 2 + 1 + 0
= 6
```

Every line of that expansion corresponds to one frame on the call stack. **The parentheses close in reverse order** — the deepest call finishes first; each level resumes exactly where it paused, with the deeper answer in hand. This winding/unwinding picture is the single most important mental image in the book: *every* recursion you meet — merge sort's halves, tree traversals, DFS, backtracking — is this same two-phase dance.

## 30.5 Recursion and memory — the price of suspension

**Each active recursive call uses stack memory** — its parameters, its local variables, its resume-point. A recursion of depth d holds ~d frames.

The call stack is **large but finite** (roughly a million frames for simple methods in .NET, far fewer for frames with big locals). Very deep recursion → `StackOverflowException` — the runtime's blunt announcement that the dolls ran out of table.

- `SumTo(3)` — 4 frames: trivial.
- `SumTo(1_000_000)` — a million frames: **crash**, despite the answer being a perfectly ordinary integer.

Any recursion of depth ~O(n) on large n is a stack-overflow risk. **An iterative solution may be safer for large input** — the running sum below holds *two variables* instead of a million suspended frames:

```csharp
static int SumToIterative(int number)
{
    int total = 0;
    for (int value = 1; value <= number; value++)
    {
        total += value;
    }
    return total;
}
```

Same answer, O(1) space instead of O(n). The professional rule: **recursion pays stack for clarity; pay it when the structure is genuinely recursive (trees, divide-and-conquer with depth log n), collect it back with iteration when depth is linear and inputs get big.** Note merge sort's depth is only ~log₂ n — a *million* elements recurse merely ~20 deep; that is why recursive sorting survives while recursive summing does not.

## 30.6 Tail shape and conversion — why some recursions convert trivially

`SumTo`'s combine (`number + ...`) happens **after** the recursive call returns — the frame must stay alive *to remember `number`*. If instead the combine is pass-the-accumulator-along:

```csharp
static int SumToAccumulator(int number, int runningTotal)
{
    if (number <= 0)
    {
        return runningTotal;
    }
    return SumToAccumulator(number - 1, runningTotal + number);
}
```

...nothing remains for the frame to remember — the paused call *forgets itself*. Such **tail-shaped** recursion converts mechanically into a loop (the accumulator *is* the loop variable, 30.5's iterative version in disguise). Recognizing this shape tells you instantly: "this recursion is a loop wearing robes" — rewrite it when depth threatens. The *interesting* recursions (merge, tree traversal, backtracking) are non-tail: work genuinely happens during unwinding, and iteration would need an explicit stack to imitate them (39 does exactly that for DFS).

---

# Chapter 31: Backtracking

## 31.1 The idea — choose, explore, unchoose

Backtracking systematically enumerates *combinatorial* structures — all subsets, all permutations, all paths through a maze — by a three-beat rhythm at every decision point:

```text
        CHOOSE      put a tentative piece onto the current partial solution
           │
        EXPLORE     recurse deeper with the piece in place
           │
        UNCHOOSE    remove the piece, restoring the world exactly as it was,
                   so the alternative choice starts from a clean slate
```

The **unchoose** step is what distinguishes backtracking from naive brute force: instead of building a fresh copy of the world per branch (exponential memory), we maintain **one shared mutable partial solution**, rewind it after each branch, and hand the next branch a pristine board. Chess players know the motion: move a knight, read the position, take the move back.

## 31.2 Generate all subsets — the canonical walkthrough

> Problem: print every subset of `{1, 2, 3}` — the eight collections ∅, {1}, {2}, {3}, {1,2}, {1,3}, {2,3}, {1,2,3}.

**The decision structure:** for each element, in order, make exactly **two choices** — *exclude* it, or *include* it. Every subset is one path down this binary decision tree; the leaves (after deciding on every element) are the subsets.

```text
                     decide on 1
                 exclude ↙   ↘ include
            decide on 2         decide on 2
           exclude ↙↘ include  exclude ↙↘ include
          decide on 3 ...       ...
     (8 leaves = 2³ subsets; each leaf's path spells its subset)
```

**The code:**

```csharp
static List<List<int>> GenerateSubsets(int[] numbers)
{
    List<List<int>> result = new();
    List<int> current = new();

    void Explore(int index)
    {
        if (index == numbers.Length)
        {
            result.Add(new List<int>(current));
            return;
        }

        Explore(index + 1);

        current.Add(numbers[index]);
        Explore(index + 1);
        current.RemoveAt(current.Count - 1);
    }

    Explore(0);
    return result;
}
```

## 31.3 Line by line — and word by word

| Line | What it does |
|---|---|
| `List<List<int>> result = new();` | The harvest: every completed subset, collected at the leaves. A list *of lists* — each subset is itself a list. |
| `List<int> current = new();` | **The one shared board** — the partial subset being built and rewound. Its *state at any instant* is the current path through the decision tree. |
| `void Explore(int index)` | A **local function** — a method declared *inside* another method, closed over the outer variables (`result`, `current`, `numbers` are visible to it without parameters). The recursive engine. |
| `if (index == numbers.Length)` | **Base case**: every element has been decided on. `current` now *is* a complete subset — a leaf. |
| `result.Add(new List<int>(current));` | **The copy-and-harvest**: add a *fresh copy* of `current` — never the shared board itself, which is about to be rewound and reused (56's "returning an internal mutable collection" bug, pre-empted). |
| `return;` | Leaf done; unwinding begins. |
| `Explore(index + 1);` | **Choice 1 — exclude**: descend *without* touching `current`. The element is simply skipped. |
| `current.Add(numbers[index]);` | **Choice 2 begins — choose**: the element joins the board. |
| `Explore(index + 1);` | **Explore**: descend with the element aboard. |
| `current.RemoveAt(current.Count - 1);` | **Unchoose**: remove the *last* element (the one just added — LIFO removal, because choices nest LIFO). The board is exactly as before the choose. |
| `Explore(0);` | Start the engine at the first element. |

The choose↔unchoose pair brackets the second explore like opening and closing parentheses (Chapter 28!) — whatever a branch adds, it removes before returning. That bracketing is the proof that every leaf sees a board containing *exactly its own path's choices*.

## 31.4 Trace — GenerateSubsets({1, 2}) in slow motion

| Event | `current` | note |
|---|---|---|
| Explore(0) | `{}` | decide on 1 |
| → Explore(1) (exclude 1) | `{}` | decide on 2 |
| &nbsp;&nbsp;→ Explore(2) = leaf | `{}` | harvest copy → **∅** |
| &nbsp;&nbsp;→ choose 2 | `{2}` | |
| &nbsp;&nbsp;→ Explore(2) = leaf | `{2}` | harvest → **{2}** |
| &nbsp;&nbsp;→ unchoose 2 | `{}` | board rewound |
| back at Explore(0): choose 1 | `{1}` | |
| → Explore(1) (exclude 2) | `{1}` | |
| &nbsp;&nbsp;→ leaf | `{1}` | harvest → **{1}** |
| &nbsp;&nbsp;→ choose 2 | `{1,2}` | |
| &nbsp;&nbsp;→ leaf | `{1,2}` | harvest → **{1,2}** |
| &nbsp;&nbsp;→ unchoose 2 | `{1}` | |
| unchoose 1 | `{}` | done |

Four leaves — ∅, {2}, {1}, {1,2} — exactly the 2² subsets of a 2-element set. Note how the *shared* `current` served all four: added-to and stripped-back, never re-allocated.

**Complexity:** time Θ(2ⁿ·n) — 2ⁿ leaves, each leaf copying up to n elements; space O(n) for the board + recursion depth (plus the Θ(2ⁿ·n) *output*, which the problem itself demands). Exponential time here is **not a flaw**: the output genuinely has 2ⁿ members — no algorithm can enumerate them faster than it can write them.

## 31.5 Permutations — the same rhythm, one knob turned

> Problem: every ordering of `{1, 2, 3}` — 123, 132, 213, 231, 312, 321.

Subsets asked *"in or out?"* per element. Permutations ask *"which unused element goes in position k?"* — the decision tree branches over *remaining candidates* instead of include/exclude:

```csharp
static List<List<int>> GeneratePermutations(int[] numbers)
{
    List<List<int>> result = new();
    List<int> current = new();
    bool[] used = new bool[numbers.Length];

    void Explore()
    {
        if (current.Count == numbers.Length)
        {
            result.Add(new List<int>(current));
            return;
        }

        for (int index = 0; index < numbers.Length; index++)
        {
            if (used[index])
            {
                continue;
            }

            used[index] = true;
            current.Add(numbers[index]);

            Explore();

            current.RemoveAt(current.Count - 1);
            used[index] = false;
        }
    }

    Explore();
    return result;
}
```

The new piece, word by word: `bool[] used` — a **parallel array of flags** marking which elements are currently aboard the board (`used[i]` ↔ element i is in `current`). The loop tries every not-yet-used element at the next position; choose = flag + add; unchoose = remove + unflag. Base case: the board is full (length n) — every element placed — harvest. Six leaves for n = 3: 3! = 3·2·1. Same rhythm, same bracketing, same shared board — the pattern transfers by changing *what the choices at each node are*.

---

# Chapter 32: Pruning

## 32.1 The problem — exponential needs mercy

2ⁿ leaves is honest for subsets; but in *search* problems (n-queens, sudoku, maze, password cracking) we don't want all branches — we want the *one* branch that satisfies the rules. Enumerating everything and filtering at the leaves wastes the entire tree below every doomed prefix.

## 32.2 The idea — cut early, cut often

**Pruning** rejects impossible partial solutions the moment they become impossible — *at the node, not at the leaf*:

```text
without pruning:               with pruning:
   prefix A  ✓                   prefix A  ✓
   ├─ B ✓ → leaf ✗               ├─ B ✗ RULE VIOLATION → stop here
   ├─ C ✗ (still grown!)         ├─ C ✓
   │   ├─ D ✗                     │   └─ ...
   │   └─ E ✗                     → entire subtree under B never born
   └─ ...
```

One violation detected k levels early kills **2^(n−k)** leaves at once. Pruning quality — *how early* the cut fires — is the entire engineering difference between "finishes in a second" and "finishes after the heat death of the universe".

## 32.3 Example — constructing passwords under rules

Constructing a password character-by-character with the rule *"no three identical characters in a row, length ≤ 8"*:

```csharp
static bool IsValidPrefix(List<char> password)
{
    int n = password.Count;
    if (n >= 3
        && password[n - 1] == password[n - 2]
        && password[n - 2] == password[n - 3])
    {
        return false;
    }
    return true;
}
```

Plumb `if (!IsValidPrefix(current)) return;` at the **top of Explore** — before choosing, before descending. Now `"aaa..."` dies at the third `a`, never growing its seven-element subtree of doomed children. The invariant shifts from *"leaves are filtered"* to *"every node is already legal"* — the same total answer, exponentially less tree.

**Where pruning lives:** at the very start of the recursive method, expressed as a cheap check on the *current partial state*. If the partial state violates a rule, `return` immediately — the unchoose above you will restore the board and try the sibling. Rules that depend only on *completed* answers (e.g. "the sum is ≥ target") need leaf checks; rules detectable early ("already exceeds the remaining capacity") belong at the node.

> Backtracking = brute force + discipline. Pruning = discipline applied as early as the rules allow.

### Exercises for Part X

1. Write the call-stack picture (30.4 style) for `Factorial(3)` with `Factorial(n) = n ≤ 1 ? 1 : n * Factorial(n-1)`.
2. In GenerateSubsets, swap the two Explore calls (include-first). Does the *set* of results change? The order?
3. What is the smallest change that turns permutation generation into a *solution-search* (stop at first leaf)?

<details><summary>Solutions</summary>

1. `F(3)` waits → `F(2)` waits → `F(1)` base → 1; then 2·1=2; then 3·2=6. Winding builds `3 * (2 * (1 * 1))`; unwinding closes right-to-left.
2. The set of leaves is identical (every path exists exactly once); the *enumeration order* changes — {1,2} family before ∅ family. For counting/enumeration problems order is cosmetic; for search-with-pruning it changes which solutions are *found first*.
3. Stop at first success: replace the harvest with an immediate upward propagation — e.g. return `bool` from Explore and `return true;` at the leaf, and `if (Explore()) return true;` after each choose. The unchoose is skipped on success paths (the board *is* the answer); the unwinding becomes pure success propagation. (This is the standard "first solution" backtracking refactor.)
</details>

---
# Part XI — Divide and Conquer

Merge sort (Chapter 21) and quicksort (Chapter 22) were two sightings of a deeper pattern. This chapter names it, proves its arithmetic, and marks its boundaries.

---

# Chapter 33: Divide and Conquer

## 33.1 The pattern — three beats

```text
1. DIVIDE     split the problem into smaller subproblems of the same kind
2. CONQUER    solve each subproblem   (recursively — same algorithm, smaller input)
3. COMBINE    assemble the sub-answers into the answer of the whole
```

| Algorithm | Divide | Conquer | Combine |
|---|---|---|---|
| Merge sort | cut at the middle (free) | sort each half | weave two sorted runs — O(n) comparisons |
| Quicksort | **partition** around a pivot (the real work) | sort each side | trivial — pivot already in place |
| Recursive max (below) | split range in half | max of each half | `Math.Max` of two numbers — O(1) |
| Binary search | compare with middle | search *one* half (discard the other) | nothing — the sub-answer *is* the answer |

The last row is the pattern's degenerate beauty: binary search divides, conquers one half, and combines with the identity — "divide and discard" rather than conquer.

## 33.2 Why it works — the recursion-tree arithmetic

Watch the work accumulate down the recursion tree for n = 8 (merge sort's shape):

```text
level 0:                [8 elements]            ── n work at this level
                    ┌───────┴───────┐
level 1:          [4]               [4]         ── n work (two halves of n/2)
                 ┌──┴──┐          ┌──┴──┐
level 2:        [2]   [2]        [2]   [2]      ── n work (four quarters)
               ┌┴┐   ┌┴┐        ┌┴┐   ┌┴┐
level 3:      [1] [1] ...                  8 leaves ── base cases (free)
```

Two multiplicative facts meet:

- **Depth:** each level halves the size → depth = **log₂ n** (13.4 — 8 → 4 → 2 → 1 is 3 = log₂ 8 levels);
- **Width:** at *every* level, all subproblems together still total n elements → **n work per level**.

Multiply: **n × log₂ n = O(n log n)**. That is the whole secret of merge sort's speed, derived as one picture: *the tree is log n tall, and each floor costs n*. Compare with the naive nested-loop sorts' implicit "tree" — one floor costing n, repeated n times: n × n = O(n²). The difference between "log n floors" and "n floors" is the difference between 20 and a million (13.3's table, structural edition).

## 33.3 The recursive maximum — smallest complete specimen

```csharp
static int MaximumInRange(int[] numbers, int start, int end)
{
    if (start == end)
    {
        return numbers[start];
    }

    int middle = start + (end - start) / 2;
    int leftMaximum = MaximumInRange(numbers, start, middle);
    int rightMaximum = MaximumInRange(numbers, middle + 1, end);

    return Math.Max(leftMaximum, rightMaximum);
}
```

Line by line:

| Line | What it does |
|---|---|
| `if (start == end)` | **Base case**: the range has exactly one element — it is the maximum of itself. The solid doll. |
| `int middle = start + (end - start) / 2;` | DIVIDE: the range's midpoint — computed overflow-safely (16.5's lesson is a *habit* now). |
| `MaximumInRange(numbers, start, middle)` | CONQUER left: `[start..middle]` — strictly smaller than `[start..end]`, so the recursion is guaranteed to reach the base case. |
| `MaximumInRange(numbers, middle + 1, end)` | CONQUER right: `[middle+1..end]`. The two halves are **disjoint** (middle belongs to left only) — no element is examined twice, none skipped. |
| `Math.Max(leftMaximum, rightMaximum)` | COMBINE: the whole range's maximum is the larger of its halves' maxima — the one-line theorem the entire algorithm rests on. |

**Why the combine is correct (the invariant, spoken):** the maximum of a set S ∪ T, where S and T partition S ∪ T, is max(max(S), max(T)) — because the overall champion must live in one part, and it dominates that part. Every parent level inherits this guarantee from every child level; by induction up the tree, the root returns the true maximum of the whole range. (Note: like `FindMaximum` (12.3), the caller must respect the precondition `start ≤ end < numbers.Length`; `MaximumInRange(numbers, 0, numbers.Length - 1)` on an empty array violates `start == end`... it would recurse on an invalid range — guard at the call site for empty input.)

**Trace on `{5, 2, 8, 1}` (start 0, end 3):**

```text
M(0,3) ── middle 1 ── M(0,1) and M(2,3)
M(0,1) ── middle 0 ── M(0,0)=5, M(1,1)=2 → max 5
M(2,3) ── middle 2 ── M(2,2)=8, M(1... 2+1=3)→ M(3,3)=1 → max 8
M(0,3) = max(5, 8) = 8 ✓
```

Four leaves (one per element — n total leaves), two combine levels (log₂ 4 = 2) — the recursion tree of 33.2 rendered in miniature, with `Math.Max` as the combine at each fork.

## 33.4 When *not* to use divide and conquer

The pattern is a tool, not a religion. Refuse it when:

- **subproblems overlap heavily** — Fibonacci's two branches both recurse into the *same* smaller problems; the tree explodes to 2ⁿ nodes while only n distinct subproblems exist. Dynamic programming (Chapter 43) exists precisely for this case — it computes each distinct subproblem *once*.
- **the input is tiny** — recursion's call/return overhead (30.4's frame machinery) exceeds the work; a loop is clearer *and* faster. Maximum of 5 numbers: write the loop of Chapter 12.
- **the combine step costs more than the work it saves** — if assembling halves is O(n²), the tree arithmetic of 33.2 becomes n² per level × log n levels = O(n² log n): *worse* than the naive loop. The pattern pays only when combine is cheap (merge: O(n); max: O(1)).
- **recursion creates unnecessary memory pressure** — depth-O(n) recursion on large inputs is a stack overflow (30.5); if a loop or an explicit stack (39) works, prefer it.

The mastery question before reaching for divide and conquer: *are the subproblems genuinely disjoint, genuinely smaller, and cheap to recombine?* Three yeses → divide. Any no → look at Part XIV.

### Exercises for Chapter 33

1. Draw the recursion tree of `MaximumInRange` on 6 elements; how many leaves, how many internal nodes?
2. Split the work as "first element + maximum of the rest" (head/tail recursion instead of half/half). What are the depth and the total work? Which chapter's warning does this trigger?
3. Why is binary search "divide and discard" rather than divide and conquer?

<details><summary>Solutions</summary>

1. 6 leaves; internal nodes: 6−1 = 5 (a binary recursion tree with n leaves over disjoint ranges always has n−1 internal forks — every internal node merges two children; count edges: 2·5 = 10 = 10 parent-child edges ✓).
2. Depth n (each call peels exactly one element) and O(n) total comparisons — correct but stack-depth O(n): the 30.5 stack-overflow risk. The half/half version has depth log n with the *same* work — strictly better risk profile.
3. It divides, then conquers exactly *one* half and discards the other without ever solving it — there is nothing to combine. The subproblem count is 1 per level, not 2 — which is why its cost is O(log n), not O(n log n): the tree of 33.2 collapses to a single spine.
</details>

---
# Part XII — Trees Heaps and Priority Queues

Arrays and lists are *linear* — one neighbor after another. Trees are the first **hierarchical** structure: data branching in layers. That single structural change buys logarithmic search (when ordered), logarithmic priority extraction (when heaped), and the native habitat of recursion.

---

# Chapter 34: Trees from Zero

## 34.1 Vocabulary — the family metaphor

A **tree** is nodes connected in a hierarchy — each node has **one parent** (except the top) and zero or more **children**:

```text
              (A)          ← root: the one parentless node
             /   \
          (B)     (C)      ← children of A
          / \      |
        (D) (E)   (F)      ← leaves: D, E, F have no children
```

| Term | Meaning | In the picture |
|---|---|---|
| **root** | the top node; the single entry point | A |
| **parent** | a node with children | A, B, C |
| **child** | a node one level below its parent | B, C (of A) |
| **leaf** | a node with no children | D, E, F |
| **depth** of a node | edges from the root down to it | depth(D) = 2 |
| **height** of a tree | longest downward path from root to a leaf | 2 here |

The file system on your computer is a tree (folders contain folders); an org chart is a tree; JSON and XML nest as trees. A **binary tree** restricts every node to at most **two** children — left and right — the shape this book uses.

## 34.2 Traversals — the four visiting orders

A linear structure has one obvious reading order; a tree has four conventions, each answering a different question:

| Traversal | Order of the picture | Generated by |
|---|---|---|
| **pre-order** | A, B, D, E, C, F | visit node → left subtree → right subtree |
| **in-order** | D, B, E, A, C, F | left subtree → visit node → right subtree |
| **post-order** | D, E, B, F, C, A | left → right → visit node last |
| **level-order** | A, B, C, D, E, F | floor by floor, using a **queue** (38) |

The code for the first three is three identical lines in three different orders — recursion *is* the tree's native language:

```csharp
public sealed class TreeNode
{
    public TreeNode(int value)
    {
        Value = value;
    }

    public int Value { get; }
    public TreeNode? Left { get; set; }
    public TreeNode? Right { get; set; }
}

static void InOrder(TreeNode? node)
{
    if (node is null)
    {
        return;
    }

    InOrder(node.Left);
    Console.WriteLine(node.Value);
    InOrder(node.Right);
}
```

Line by line:

| Line | What it does |
|---|---|
| `public sealed class TreeNode` | The node: payload + two optional children. `sealed` — closed design (29.2's discipline). |
| `public TreeNode? Left { get; set; }` | Nullable references (29.2): `null` *means* "no child here" — a leaf's edges. The `?` makes that intent compiler-checked. |
| `if (node is null) return;` | **The base case** (30.2): the empty tree (a missing child) is visited by doing nothing. Trees *are* the recursion base-case structure — half their elegance. |
| `InOrder(node.Left);` | Fully traverse the left subtree first. |
| `Console.WriteLine(node.Value);` | *Then* visit the node itself. |
| `InOrder(node.Right);` | Then the right. — Swap lines to get pre-order or post-order. |

**Cost:** every node is visited exactly once → O(n) time; depth = O(h) stack (30.5), where h = tree height — log n if balanced, n if degenerate.

## 34.3 In-order on a binary search tree — the magic sentence

Chapter 35 builds **binary search trees**. Their magic sentence belongs here because it explains *why in-order exists*:

> **In-order traversal of a binary search tree visits values in ascending sorted order.**

No comparison, no sorting pass — the tree's shape *encodes* the order, and walking it left-node-right simply *reads the encoding aloud*. `InOrder` is therefore a sorted-report generator for free.

---

# Chapter 35: Binary Search Trees

## 35.1 The ordering rule

A **binary search tree (BST)** is a binary tree obeying one law at *every* node:

> everything in the **left** subtree is **smaller** than the node; everything in the **right** subtree is **larger**.

```text
              (8)
             /    \
           (3)    (10)
          /   \      \
        (1)   (6)    (14)
             /  \    /
           (4)  (7) (13)
```

Check any node: at 8, left values {1,3,4,6,7} all < 8, right {10,13,14} all > 8. At 3: left {1} < 3, right {4,6,7} > 3. ✓ The law holds *locally everywhere*, which — by the transitivity of < — yields the global property: **every leftward step is a step toward smaller values, every rightward step toward larger**.

## 35.2 The payoff — search that walks one root-to-leaf path

To find 7 in the tree above: start at 8 → 7 < 8, go **left** → at 3 → 7 > 3, go **right** → at 6 → 7 > 6, go **right** → found 7. Three comparisons, one path — every comparison discards an entire **subtree**, exactly like binary search's halving (16). If the tree is **balanced** (height ≈ log₂ n), search is **O(log n)**; if badly unbalanced (each node one child — a tree degenerated into a linked list), it degrades to **O(n)**. The *shape* is everything; Chapter 36's heap and AVL/red-black trees (library territory) exist to police the shape.

## 35.3 The full implementation — insert, search, delete

### The node and the law, in code

```csharp
public sealed class BinarySearchTree
{
    private TreeNode? _root;

    public bool Contains(int value)
    {
        TreeNode? current = _root;

        while (current is not null)
        {
            if (value == current.Value)
            {
                return true;
            }

            current = value < current.Value
                ? current.Left
                : current.Right;
        }

        return false;
    }

    public void Add(int value)
    {
        TreeNode? parent = null;
        TreeNode? current = _root;
        bool goesLeft = false;

        while (current is not null)
        {
            parent = current;
            if (value < current.Value)
            {
                goesLeft = true;
                current = current.Left;
            }
            else
            {
                goesLeft = false;
                current = current.Right;
            }
        }

        TreeNode node = new(value);

        if (parent is null)
        {
            _root = node;
        }
        else if (goesLeft)
        {
            parent.Left = node;
        }
        else
        {
            parent.Right = node;
        }
    }
}
```

### Line by line — Contains (iterative descent)

| Piece | What it does |
|---|---|
| `private TreeNode? _root;` | The tree's single entry point; `null` = empty tree. `private` — the outside world never touches raw nodes; **encapsulation** — the class guarantees the ordering law because *only its own methods* can rewire nodes. |
| `while (current is not null)` | Walk until falling off the tree (the "not found" exit) or matching. |
| `value < current.Value ? current.Left : current.Right` | **The ternary operator** — `condition ? a : b` reads "if condition then a else b", as an *expression* (a value). Here: the next hop — left for smaller, right for larger. The ordering law as one line. |

### Line by line — Add (find the adoption point, attach)

Adding is *searching for a vacancy*: descend exactly as Contains does, remember the **last real node visited** (`parent`), and attach the new node as its left or right child:

| Piece | What it does |
|---|---|
| `TreeNode? parent = null;` | The last non-null node on the descent — the future adopter. |
| `while (current is not null)` | Descend until the vacancy (a `null` child slot) is located. |
| `parent = current;` | Update the memory of the last real node *before* stepping down. |
| `goesLeft = value < current.Value;` | Remember which way the final step went — the new node's side. |
| `if (parent is null) _root = node;` | The loop never ran → the tree was empty → the newcomer *is* the root. |
| `parent.Left = node;` / `parent.Right = node;` | Attach at the vacancy. The tree grows **only at leaves** — existing nodes never move. |

**Complexity:** both operations walk one root-to-leaf path → O(h): **O(log n)** balanced, O(n) degenerate. Insert order controls shape: inserting 1, 2, 3, 4, 5 creates a right-leaning staircase (degenerate!); interleaving (3, 1, 5, 2, 4...) creates the bushy tree of 35.1 — which is why production systems use **self-balancing trees** (AVL, red-black — `SortedSet<T>`/`SortedDictionary<K,V>` in .NET) that rotate nodes to keep h ≈ log n under any insertion order.

### Delete — the three cases (design sketch, then code)

Deletion is the operation with famous teeth, because three topologies can occur:

```text
case 1 — leaf:              case 2 — one child:        case 3 — two children:
    (8)                         (8)                        (8)
   /                             \                       /   \
 (3)  ← delete                  (3) ← delete           (3)   (10)
                                    \                  /  \
                                 (6)  survives       (1)  (6) ← delete
                                    ↑ rewire up              \
                                 replace parent            (7) → successor
```

1. **Leaf** — just remove it; nothing to reconnect.
2. **One child** — the node's single subtree is lifted into its place (`parent` now points at the child).
3. **Two children** — the node cannot be simply removed. The trick: find its **in-order successor** — the smallest value in its *right* subtree (leftmost node of the right subtree: 7 above); copy that value into the doomed node; then delete the successor (which by construction has at most a right child — case 1 or 2). The ordering law survives both edits.

```csharp
public bool Remove(int value)
{
    TreeNode? parent = null;
    TreeNode? current = _root;

    while (current is not null && current.Value != value)
    {
        parent = current;
        current = value < current.Value ? current.Left : current.Right;
    }

    if (current is null)
    {
        return false;
    }

    if (current.Left is not null && current.Right is not null)
    {
        TreeNode successor = current.Right;
        TreeNode successorParent = current;

        while (successor.Left is not null)
        {
            successorParent = successor;
            successor = successor.Left;
        }

        current.Value = successor.Value;

        if (successorParent == current)
        {
            successorParent.Right = successor.Right;
        }
        else
        {
            successorParent.Left = successor.Right;
        }

        return true;
    }

    TreeNode? child = current.Left ?? current.Right;

    if (parent is null)
    {
        _root = child;
    }
    else if (parent.Left == current)
    {
        parent.Left = child;
    }
    else
    {
        parent.Right = child;
    }

    return true;
}
```

Reading map (the full line-by-line ceremony is your exercise — the structures are now familiar): the first `while` is the Contains descent with parent-tracking; the `Left is not null && Right is not null` branch is case 3 (walk right subtree's leftmost spine; splice out the successor); `current.Left ?? current.Right` — the **null-coalescing operator**: "left if it exists, else right" — selects the surviving child for cases 1 and 2 in one expression (a leaf yields `null` — removing works the same). All three cases preserve the law; `TreeNode.Value` must therefore be settable (`{ get; set; }`) for the successor-copy trick.

**Cost of the exercise:** O(h) — one descent plus (case 3) one short successor walk.

## 35.4 BST versus hash structures — the decision

| Question | Winner | Why |
|---|---|---|
| exact-key membership, no order needed | hash set / dictionary (Part VIII) | expected O(1) beats O(log n) |
| sorted iteration / range queries / min / max | **BST** | shape *is* order; hash has none (25.3) |
| predecessor/successor ("next larger value") | **BST** | one walk up/down the spine |
| worst-case guarantees | balanced BST / dictionary | both degrade without care |

In .NET: `SortedSet<T>` / `SortedDictionary<K,V>` = self-balancing trees; `HashSet<T>` / `Dictionary<K,V>` = hash structures. The names map the trade-off table.

---

# Chapter 36: Heaps and Priority Queues

## 36.1 The heap idea — a tournament ladder in an array

A **binary heap** is a tree shaped by a simpler law than the BST's — order only between **parent and child**:

> **min-heap:** every parent ≤ its children. (max-heap: every parent ≥ its children.)

```text
            (3)                     the heap: shape + parent-child order
           /   \                    (no left/right law! 10 vs 7 — anything)
         (10)  (7)
         /  \    \
       (15) (11) (9)
```

Consequences of the weak law:

- the **root is the global minimum** — guaranteed, in O(1);
- **no idea** whether 10 < 9 "in order" — sibling order is unspecified;
- the tree is kept **complete** (all levels full except possibly the last, filled left-to-right) — which permits the famous trick: **store it inside a plain array**, no node objects at all:

```text
array:   [3, 10, 7, 15, 11, 9]
index:     0   1  2   3   4  5

parent(i) = (i - 1) / 2      left(i) = 2i + 1      right(i) = 2i + 2
   e.g. index 4 (11): parent (4-1)/2 = 1 (10) ✓    children of 1: 3, 4
```

**Sift up** (after insert at the end): while smaller than its parent, swap upward — O(log n). **Sift down** (after replacing the root): swap with the *smaller* child until settled — O(log n). Those two repairs are the entire machinery behind "repeatedly extract the extreme element efficiently".

## 36.2 The C# — PriorityQueue, word by word

The library hands you the sift machinery ready-made:

```csharp
PriorityQueue<string, int> queue = new();
queue.Enqueue("normal", 10);
queue.Enqueue("urgent", 1);
string next = queue.Dequeue();   // "urgent"
```

| Piece | What it does |
|---|---|
| `PriorityQueue<TElement, TPriority>` | Generic over *payload* and *priority number* — two independent choices ("patients with severity ints", "tasks with deadline doubles"). |
| `Enqueue(element, priority)` | Insert with its priority — O(log n). |
| `Dequeue()` | Remove and return the element with the **smallest** priority number — O(log n). |
| `Peek()` | Look without removing — O(1). |

**Read the convention carefully:** with the default comparison, **the smaller priority value comes out first** — priority 1 beats priority 10. This startles everyone exactly once: if your domain says "priority 5 is more important than priority 1", either negate numbers when enqueuing or pass a custom comparer. Always verify and document the convention in your application — the queue cannot read your business rules.

## 36.3 Top-K — the pattern that made heaps famous

> Problem: from n values, report the **k largest** — say, top 3 of `[9, 4, 12, 7, 15, 2]`.

**Sort** solves it in O(n log n). **The heap trick** does better when k ≪ n: maintain a **min-heap of size k** (the k champions so far, with the *weakest champion on top*):

```csharp
static int[] TopK(int[] numbers, int k)
{
    if (k <= 0 || k > numbers.Length)
    {
        throw new ArgumentOutOfRangeException(nameof(k));
    }

    PriorityQueue<int, int> champions = new();

    foreach (int number in numbers)
    {
        if (champions.Count < k)
        {
            champions.Enqueue(number, number);
        }
        else if (number > champions.Peek())
        {
            champions.Dequeue();
            champions.Enqueue(number, number);
        }
    }

    int[] result = new int[k];
    for (int index = k - 1; index >= 0; index--)
    {
        result[index] = champions.Dequeue();
    }

    return result;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `champions.Count < k` | Filling phase: the first k elements all join — the heap is not yet full. |
| `number > champions.Peek()` | The gate: a newcomer must beat the **weakest current champion** (the min-heap's root — exactly what `Peek` exposes in O(1)) to deserve membership. |
| `Dequeue(); Enqueue(...);` | Evict the weakest, admit the newcomer — both O(log k). |
| the drain loop, backwards | `Dequeue` yields ascending; filling `result[k-1]` down to `result[0]` reverses it into descending order — the "top-K report" convention. |

**Why a min-heap for a *max* question?** Because among k champions, the one you must *compare against* and *evict* is the **weakest** — and a min-heap exposes its root in O(1). The heap orientation answers "whom do I need fast access to?", not "what am I ranking".

**Complexity:** O(n log k) time, O(k) space — versus sort's O(n log n) and O(n). n = 10⁸, k = 10: ~10⁸·3 versus ~10⁸·27 — an order of magnitude, plus tiny memory. This one pattern runs inside leaderboards, recommendation feeds, streaming analytics (57's online algorithms), and Dijkstra's algorithm below (41.2).

## 36.4 Where priority queues earn their keep

- **scheduling** — OS run queues, job dispatch by urgency;
- **shortest paths** — Dijkstra repeatedly extracts the *closest unfinalized* vertex (41);
- **emergency processing** — triage: severity is the priority;
- **simulations** — event-driven: next-event-time is the priority;
- **selecting the next best candidate** — top-K, k = 1 at a time.

The unifying question: *"which item should be handled next?" answered by a **changing** score, not by arrival order (queue) or recency (stack)* — that is a priority queue.

### Exercises for Part XII

1. In-order walk the BST of 35.1 by hand — write the sequence, and say what you notice.
2. Insert 1,2,3,4,5 into an empty BST (35.3's Add). Draw it. What is its height, and what Chapter 6 structure has it secretly become?
3. Trace `TopK` on `[9, 4, 12, 7, 15, 2]`, k = 3 — show the heap contents after each element.
4. Why does level-order traversal (34.2) need a queue while the other three need recursion?

<details><summary>Solutions</summary>

1. 1, 3, 4, 6, 7, 8, 10, 13, 14 — ascending order: 34.3's magic sentence, experienced.
2. A right-leaning chain of height 5 — effectively a **linked list** (Chapter 29); search degrades to O(n). Balanced insertion orders (3,1,5,2,4) avoid this; self-balancing trees fix it permanently.
3. 9 → {9}; 4 → {9,4}; 12 → {9,4,12} (root 4 = weakest champion); 7: 7 > 4 → evict 4 → {9,7,12} (root 7); 15: 15 > 7 → evict 7 → {9,12,15} (root 9); 2: 2 > 9? no → unchanged. Drain backwards: **15, 12, 9** ✓.
4. Level-order must hold the *later* floors while visiting the earlier ones — a FIFO of discovered-but-unvisited nodes (the exact structure of BFS, 38). The three recursive orders descend and unwind (30.4) — the call stack already provides the memory.
</details>

---
# Part XIII — Graph Algorithms

Trees forbade cycles and multiple parents. **Graphs** drop every restriction: any node may connect to any node. This is the structure of the real world — roads, friendships, dependencies, networks — and the algorithms here power navigation, scheduling, and routing.

---

# Chapter 37: Graphs from Zero

## 37.1 Vocabulary — nodes and edges

A **graph** is:

- a set of **vertices** (nodes) — the entities;
- a set of **edges** — connections between pairs of vertices.

| Property | Meaning | Example |
|---|---|---|
| **directed** | edges have a direction (A→B ≠ B→A) | Twitter follow, task prerequisite |
| **undirected** | edges are two-way | Facebook friendship, road (usually) |
| **weighted** | edges carry a number | road length, latency, cost |
| **cyclic / acyclic** | contains / lacks cycles | dependency graphs must be acyclic |
| **connected** | every vertex reachable from every other | one road network |

Real graphs:

- **roads between cities** — undirected, weighted (distance);
- **users connected by friendships** — undirected, unweighted;
- **services connected by network calls** — directed, weighted (latency);
- **tasks connected by prerequisites** — directed, acyclic (Chapter 40's subject).

## 37.2 Representation — the adjacency list

Two classic encodings compete:

```text
adjacency LIST (per-vertex neighbor roster):     adjacency MATRIX (n×n grid):
   A → [B, C]                                          A  B  C  D
   B → [D]                                        A [  0  1  1  0 ]
   C → [D]                                        B [  0  0  0  1 ]
   D → []                                         C [  0  0  0  1 ]
                                                  D [  0  0  0  0 ]
```

| | Adjacency list | Adjacency matrix |
|---|---|---|
| Space | **O(V + E)** | O(V²) |
| "is A–B an edge?" | O(degree(A)) scan | **O(1)** lookup |
| Walk all edges | **O(V + E)** | O(V²) |
| Fits | sparse graphs (most real ones) | dense graphs, tiny graphs |

Real-world graphs are **sparse** (a city has thousands of intersections but each meets only ~3–4 roads; V² for a million vertices is 10¹² cells) — the list wins almost always in practice. It is the representation used throughout this Part.

```csharp
Dictionary<string, List<string>> graph = new()
{
    ["A"] = new() { "B", "C" },
    ["B"] = new() { "D" },
    ["C"] = new() { "D" },
    ["D"] = new()
};
```

Word by word: `Dictionary<string, List<string>>` — from each vertex's *name* to its *neighbor list*. `new() { "B", "C" }` — target-typed construction with pre-filled elements (6.4). `["D"] = new()` — a vertex with no neighbors still **must appear as a key** (an empty roster ≠ an absent vertex — forgetting isolated vertices is a classic silent bug). For weighted graphs the value type becomes `List<(string To, int Weight)>` — tuples as edges.

---

# Chapter 38: Breadth-First Search

## 38.1 The idea — explore in rings

BFS explores **by distance from the start**: first all vertices at 1 edge, then all at 2 edges, then 3 — expanding rings in a pond. The discipline that enforces ring order is, precisely, a **queue** (27): vertices are discovered in one order and *processed* in the same order — the earliest-discovered unprocessed vertex is always next, which is exactly FIFO.

```text
      A            processing order from A:
    ↙   ↘          ring 1: B, C
   B     C         ring 2: D
    ↘   ↙
      D
```

## 38.2 The code

```csharp
static List<string> BreadthFirstSearch(
    Dictionary<string, List<string>> graph,
    string start)
{
    List<string> order = new();
    Queue<string> queue = new();
    HashSet<string> visited = new();

    queue.Enqueue(start);
    visited.Add(start);

    while (queue.Count > 0)
    {
        string current = queue.Dequeue();
        order.Add(current);

        foreach (string neighbor in graph[current])
        {
            if (visited.Add(neighbor))
            {
                queue.Enqueue(neighbor);
            }
        }
    }

    return order;
}
```

## 38.3 Line by line — three structures, three jobs

| Line | What it does |
|---|---|
| `List<string> order` | The output ledger — the visiting order (and, if you record distances beside it, the ring structure). |
| `Queue<string> queue` | **The frontier**: discovered but not yet processed. FIFO discipline = ring order. |
| `HashSet<string> visited` | **The memory**: everyone ever discovered (25's set — O(1) membership). |
| `queue.Enqueue(start); visited.Add(start);` | Seed: the start is discovered (visited) and scheduled (queued). Adding to *both* at once is the pattern's keystone — see below. |
| `while (queue.Count > 0)` | Until the frontier is empty — i.e., until the entire reachable component is processed. |
| `string current = queue.Dequeue();` | Take the **oldest** discovered vertex — the ring-order guarantee. |
| `order.Add(current);` | Process: record the visit. |
| `foreach (string neighbor in graph[current])` | Consult the adjacency roster. |
| `if (visited.Add(neighbor))` | **The fused test-and-mark** (25.1): returns false if already discovered. Only *newly* discovered vertices... |
| `queue.Enqueue(neighbor);` | ...enter the frontier. |

**The invariant that makes it correct:** *every vertex is enqueued at most once — marked visited at the moment of discovery, not of processing.* Mark at processing instead and a vertex in the queue can be re-enqueued by several earlier vertices before it is processed — the queue fills with duplicates and complexity degrades toward O(V·E). Mark-early is not a style choice; it is the algorithm.

**Why cycles cannot trap it:** a cycle's back-edge leads to an already-`visited` vertex → the `Add` fails → no re-enqueue. The `visited` set is what tames cycles — without it, cyclic graphs cause infinite wandering (56).

**Trace on the 37.2 graph, start A:**

| step | dequeue | neighbors | visited after | queue after |
|---:|---|---|---|---|
| seed | — | — | {A} | [A] |
| 1 | A | B, C → both new | {A,B,C} | [B, C] |
| 2 | B | D → new | {A,B,C,D} | [C, D] |
| 3 | C | D → **already visited** | unchanged | [D] |
| 4 | D | (none) | unchanged | [] → done |

Order: **A, B, C, D** — A's ring (B, C) then the next ring (D). Step 3 is the cycle-tamer visible in action: C→D discovered B's D already.

**Complexity:** each vertex dequeued once, each edge consulted once → **O(V + E)** time; O(V) space for queue + visited. Note the elegance: the cost is *linear in the graph's own size* — no graph algorithm doing real per-vertex or per-edge work can hope to beat it.

## 38.4 What BFS is *for* — the distance theorem

> **BFS from a start vertex visits vertices in nondecreasing order of edge-count distance; therefore BFS finds shortest paths (by edge count) in unweighted graphs.**

Every vertex in ring k was discovered from some vertex in ring k−1; recording *which* neighbor discovered you (a `Dictionary<string, string> cameFrom`) reconstructs the actual shortest path by walking backwards from the target to the start. This is the algorithm inside "degrees of separation", maze shortest-exit, unweighted routing — and it is why 17.2's table assigns BFS to unweighted shortest paths.

---

# Chapter 39: Depth-First Search

## 39.1 The idea — one corridor to the end

DFS commits: follow one corridor as deep as possible; only when it dead-ends, **backtrack** to the last fork and try the next corridor. The discipline that enforces deepest-first is a **stack** (26) — the most recently discovered unexplored vertex is next. Which means DFS is BFS with one data-structure swap:

```text
BFS:  Queue  → rings  → shortest paths (unweighted)
DFS:  Stack  → dives  → structure discovery: cycles, ordering, components
```

## 39.2 The code — iterative, with an explicit stack

```csharp
static List<string> DepthFirstSearch(
    Dictionary<string, List<string>> graph,
    string start)
{
    List<string> order = new();
    Stack<string> stack = new();
    HashSet<string> visited = new();

    stack.Push(start);

    while (stack.Count > 0)
    {
        string current = stack.Pop();

        if (!visited.Add(current))
        {
            continue;
        }

        order.Add(current);

        foreach (string neighbor in graph[current])
        {
            stack.Push(neighbor);
        }
    }

    return order;
}
```

## 39.3 Line by line — and the subtle difference from BFS

| Line | What it does |
|---|---|
| `stack.Push(start);` | Seed the frontier — note: **no** `visited.Add` here. |
| `string current = stack.Pop();` | Take the **newest** discovered vertex — the dive. |
| `if (!visited.Add(current)) continue;` | **The late mark**: test-and-mark at *processing* time. The same vertex may sit in the stack several times (pushed by different neighbors before being processed); this line discards the stale duplicates — the stack may hold copies, the `visited` set never admits one twice. |
| `foreach ... stack.Push(neighbor);` | Schedule neighbors — pushed even if already visited (cheap; the pop-time check filters). |

Why the asymmetry with BFS's mark-early? An explicit stack has no "oldest-first" fairness to exploit — pushing-then-deduplicating-at-pop is the standard robust pattern (marking early *would* also work here and saves some pushes; the crucial invariant — *process each vertex at most once* — is preserved by the pop-time check either way).

**Trace on the 37.2 graph, start A** (neighbors pushed in roster order B then C — the stack yields **C first**):

| step | pop | visited.Add? | pushes | stack after | order |
|---:|---|---|---|---|---|
| seed | — | — | A | [A] | |
| 1 | A | new | B, C | [B, C] | A |
| 2 | C | new | D | [B, D] | A, C |
| 3 | D | new | — | [B] | A, C, D |
| 4 | B | new | D | [D] | A, C, D, B |
| 5 | D | **duplicate — skip** | — | [] | done |

Order: **A, C, D, B** — a dive A→C→D, then backtracking to B. Compare BFS's A, B, C, D: same graph, opposite personality. (Step 5's duplicate-D is the pop-time filter earning its keep.)

**Complexity:** O(V + E) time — each vertex processed once (duplicates are popped-and-discarded in O(1)); O(V) space. The **recursive** formulation (`Visit(v): mark v; foreach neighbor: if unmarked → Visit`) is three lines and 30.4's winding is the backtracking — equally valid until depth threatens the call stack (30.5): explicit-stack DFS survives graphs where recursion overflows.

## 39.3 What DFS is *for*

DFS's dives expose a graph's **structure**, not its distances:

- **cycle detection** — a dive reaching a vertex still *on the current path* (not merely visited) found a cycle;
- **topological sorting** — Chapter 40, built directly on DFS's unwinding order;
- **connected components** — one DFS per unvisited vertex sweeps one whole component;
- **maze/path existence** — any path found is fine (no distance guarantee);
- the skeleton of **backtracking** over graph-shaped choice spaces (Part X's parent, historically).

> Choose by the question: *how far?* → BFS. *is there / how is it structured?* → DFS.

---

# Chapter 40: Topological Sorting

## 40.1 The problem — ordering by dependency

A **directed acyclic graph (DAG)** encodes dependencies: an edge X→Y means "X must come before Y". A **topological order** lists the vertices so that **every edge points forward** — every prerequisite precedes its dependent.

```text
    Course DAG:      101 → 205 → 340
                     101 → 210 → 340        valid orders: 101, 205, 210, 340
                     210 → 350                       or   101, 210, 205, 340
                                               (both respect every arrow)
```

Applications: **build systems** (compile dependencies first), **course prerequisites**, **workflow ordering**, **task scheduling**, and — inside the Algorithm Lab's capstone list — any pipeline whose steps constrain each other.

**The impossibility theorem:** if the graph has a **cycle**, no valid order exists — a cycle means A before B *and* B before A. Detecting cycles and ordering are the same problem in different clothes; the algorithm below reports both.

## 40.2 The algorithm — Kahn's method (peel the ready vertices)

The mirror-inversion of the problem: a vertex is **ready** when nothing still points at it. Repeatedly:

1. compute every vertex's **in-degree** (number of incoming edges);
2. take any ready vertex (in-degree 0) — nothing blocks it — append it to the order;
3. **delete** it conceptually: decrement each neighbor's in-degree;
4. repeat. If the order ends up shorter than the vertex count, the leftovers form a cycle.

```csharp
static List<string> TopologicalSort(Dictionary<string, List<string>> graph)
{
    Dictionary<string, int> inDegree = new();

    foreach (string vertex in graph.Keys)
    {
        inDegree[vertex] = 0;
    }

    foreach (string vertex in graph.Keys)
    {
        foreach (string neighbor in graph[vertex])
        {
            inDegree[neighbor]++;
        }
    }

    Queue<string> ready = new();
    foreach (string vertex in inDegree.Keys)
    {
        if (inDegree[vertex] == 0)
        {
            ready.Enqueue(vertex);
        }
    }

    List<string> order = new();

    while (ready.Count > 0)
    {
        string current = ready.Dequeue();
        order.Add(current);

        foreach (string neighbor in graph[current])
        {
            inDegree[neighbor]--;

            if (inDegree[neighbor] == 0)
            {
                ready.Enqueue(neighbor);
            }
        }
    }

    return order;
}
```

## 40.3 Line by line

| Piece | What it does |
|---|---|
| first loop | **Initialize every in-degree to 0** — including isolated vertices (37.2's warning: every key exists even with an empty roster). The initialization-then-accumulate pattern (14.4's "old-or-zero" in explicit form). |
| second loop | **Count the arrows**: each edge X→Y raises Y's in-degree — Y's blocker count. |
| the seed scan | Every vertex with in-degree 0 enters the `ready` queue — no blockers, safe to place first. (A DAG *always* has at least one such vertex — otherwise follow blockers backwards forever: a cycle.) |
| `while (ready.Count > 0)` | Process until no ready vertex remains. |
| `order.Add(current)` | Place the ready vertex — nothing points at it *that hasn't already been placed*; appending it cannot violate any edge. |
| `inDegree[neighbor]--;` | **Conceptual deletion**: current's outgoing edges no longer block anyone; each neighbor loses one blocker. |
| `if (inDegree[neighbor] == 0) ready.Enqueue(neighbor);` | A neighbor just became unblocked — schedule it. This is the "cascade" that ripples placement through the DAG. |

**The cycle check (your exercise to wire in):** after the loop, `if (order.Count < graph.Count)` → the un-placed leftovers are locked in mutual blocking — a cycle — *report it* (return null / throw). Length equality is not a nicety; it is the algorithm's correctness certificate.

**Trace on the course DAG** `{101: [205, 210], 205: [340], 210: [340, 350], 340: [], 350: []}`:

| in-degrees | ready queue | dequeue → order | cascade decrements |
|---|---|---|---|
| 101:0, 205:1, 210:1, 340:2, 350:1 | [101] | 101 → `[101]` | 205→0, 210→0 → both enqueue |
| | [205, 210] | 205 → `[101, 205]` | 340→1 |
| | [210] | 210 → `[101, 205, 210]` | 340→0 (enqueue), 350→0 (enqueue) |
| | [340, 350] | 340, then 350 | — |

Order: **101, 205, 210, 340, 350** — every arrow respected. **Complexity:** O(V + E) — each vertex enqueued/dequeued once, each edge decrements once; O(V) space.

**The DFS alternative**, for completeness: run DFS, and *prepend each vertex to the order when its exploration finishes* (post-order, reversed) — vertices finishing last have no dependents left... the same order emerges from the opposite direction. Kahn's is the version that detects cycles for free; DFS's is the version that generalizes into SCC/tarjan territory — both are O(V+E).

---

# Chapter 41: Shortest Paths and Minimum Spanning Trees

## 41.1 Choosing the shortest-path algorithm — the table

| Graph situation | Common choice | Why |
|---|---|---|
| Unweighted edges | **BFS** | rings *are* distance (38.4) |
| Non-negative weights | **Dijkstra** | weighted BFS-by-closeness, below |
| Negative edges allowed | **Bellman–Ford** | repeatedly relaxing every edge V−1 times survives negative weights and detects negative cycles |
| All-pairs shortest paths | **Floyd–Warshall** or repeated single-source | a V×V distance matrix, built dynamic-programming style (43) |

## 41.2 Dijkstra's algorithm — BFS with a priority queue

**The problem:** weighted graph, one source; find the cheapest *total weight* path to every vertex (roads with lengths; network hops with latencies). Precondition: **no negative weights** (they break the "settled is final" logic below).

**The idea — BFS's rings, deformed by weights:** BFS processed vertices in *edge-count* order; Dijkstra processes them in *distance-from-source* order, closest unsettled first. The structure that delivers "closest next" in O(log n) is — exactly — the **priority queue** of Chapter 36:

```text
DIJKSTRA in one breath:
    distance[source] = 0; all other distances = ∞
    priority queue of (vertex, tentative distance), source at 0
    while queue not empty:
        take the closest unsettled vertex u                 ← PQ extract-min
        mark u settled — its distance is now FINAL
        for each edge u→v with weight w:
            if distance[u] + w < distance[v]:               ← the RELAXATION
                distance[v] = distance[u] + w               ← found a cheaper route
                update v's place in the queue
```

**Why "settled is final" holds (the invariant, with non-negative weights):** when u is extracted as the closest unsettled vertex, *any* other route to u would have to leave the settled region through some unsettled vertex x — but x is already farther than u, and weights are non-negative, so the route through x cannot be shorter. Negative weights demolish this argument — hence Bellman–Ford's existence.

**The relaxation — the algorithm's heartbeat, word by word:** `distance[u] + w < distance[v]` asks *"does reaching v through u beat the best route we knew?"* — the record-update pattern of FindMaximum (12.3) wearing weights. Every shortest path is discovered as a chain of successful relaxations.

### The implementation

```csharp
static Dictionary<string, double> Dijkstra(
    Dictionary<string, List<(string To, double Weight)>> graph,
    string source)
{
    Dictionary<string, double> distance = new();

    foreach (string vertex in graph.Keys)
    {
        distance[vertex] = double.PositiveInfinity;
    }

    distance[source] = 0;

    PriorityQueue<string, double> frontier = new();
    frontier.Enqueue(source, 0);

    while (frontier.Count > 0)
    {
        string current = frontier.Dequeue();

        foreach ((string to, double weight) in graph[current])
        {
            double candidate = distance[current] + weight;

            if (candidate < distance[to])
            {
                distance[to] = candidate;
                frontier.Enqueue(to, candidate);
            }
        }
    }

    return distance;
}
```

### Line by line

| Piece | What it does |
|---|---|
| `Dictionary<string, List<(string To, double Weight)>>` | Weighted adjacency list: each roster entry is a **tuple** `(To, Weight)` — named tuple fields destructured on use. |
| `distance[vertex] = double.PositiveInfinity;` | **Optimistic initialization**: every vertex presumed unreachable; only evidence (a relaxation) lowers the estimate. ∞ is the identity of "no route known". |
| `distance[source] = 0;` | The source is at distance 0 from itself — the seed of all truth. |
| `PriorityQueue<string, double>` | The frontier: payload = vertex, **priority = tentative distance** — Chapter 36's smallest-first convention, exactly what "closest unsettled" needs. |
| `frontier.Enqueue(source, 0);` | The source enters at distance 0. |
| `string current = frontier.Dequeue();` | Extract the closest unsettled vertex — its distance is now **final** (the invariant above). |
| `foreach ((string to, double weight) in graph[current])` | **Tuple deconstruction** in the loop: each edge splits into its `to` and `weight` parts on arrival. |
| `double candidate = distance[current] + weight;` | The challenger: reaching `to` *through current*. |
| `if (candidate < distance[to])` | **The relaxation test** — does the challenger beat the record? |
| `distance[to] = candidate;` | Record update... |
| `frontier.Enqueue(to, candidate);` | ...and re-schedule `to` at its new, better priority. |

**A practical note on the "lazy" variant shown:** we push a *new* queue entry instead of editing the old one — the queue may briefly hold several entries for one vertex at different priorities. When a stale (worse) copy is dequeued later, its `candidate < distance[to]` re-check fails for every neighbor (the record already beat it), so it does nothing — harmless laziness, standard in production implementations (a `decrease-key` heap would avoid the duplicates at the cost of a more complex structure).

**Trace** — graph: A→B (4), A→C (2), C→B (1), B→D (5), C→D (8):

| step | dequeue | relaxations | distance map |
|---:|---|---|---|
| seed | — | — | A:0, B:∞, C:∞, D:∞ |
| 1 | A (0) | B: 0+4=4 ✓, C: 0+2=2 ✓ | A:0, B:4, C:2, D:∞ |
| 2 | C (2) | B: 2+1=3 < 4 ✓, D: 2+8=10 ✓ | A:0, B:3, C:2, D:10 |
| 3 | B (3) | D: 3+5=8 < 10 ✓ | A:0, B:3, C:2, D:8 |
| 4 | D (8) | (no out-edges) | final |

The gem is step 2: C's relaxation *overwrote* B's route — the path A→C→B (3) beats A→B (4). Final answers: B=3, C=2, D=8 — each proved by the chain of relaxations that produced it.

**Complexity:** with a binary heap, **O((V + E) log V)** — each vertex extracted once (log V per extract), each edge causes at most one push (log V each); O(V) space. Appendix A records exactly this row.

## 41.3 Minimum spanning trees — connect everyone, cheapest

Different question, same family: given a **connected, weighted, undirected** graph, choose edges that keep *every vertex connected* while minimizing **total** edge weight — a **minimum spanning tree (MST)**. The result always has exactly V−1 edges (tree!), and classic greedy algorithms solve it (greedy — Chapter 42 — *with proofs that make it safe*):

- **Kruskal's:** sort all edges by weight; accept each edge that connects two still-separate components (checked with a disjoint-set/union-find structure); stop at V−1 edges. *"Cheapest bridges first, skip anything redundant."*
- **Prim's:** grow one tree from any start; repeatedly attach the cheapest edge leaving the current tree (a priority queue delivers it — Dijkstra's machinery with a different relaxation target: *tree-weight* instead of *source-distance*).

**Applications:** network design (cabling, pipelines), clustering analysis, approximation algorithms. The deep moral carried into Chapter 42: both MST algorithms are **greedy**, and both are *provably* optimal — greed's legitimacy always comes from structure plus proof, never from hope.

### Exercises for Part XIII

1. BFS on the 37.2 graph from **B**: write the order and the rings.
2. Why does DFS (39.2) push neighbors that may already be visited, while BFS (38.2) refuses to enqueue them?
3. Run Kahn's algorithm on `{A: [B], B: [C], A: [C]}` (i.e., A→B, B→C, A→C). Which two valid orders can come out?
4. In the Dijkstra trace above, why was step 3's B-dequeue "final at 3" even though a *later* edge might touch B?

<details><summary>Solutions</summary>

1. B, then ring 1 {D}, then... D has no neighbors → order **B, D** (A, C are unreachable *from B* — edges point away from them). Reachability is directional in directed graphs; a BFS from B cannot see upstream.
2. The stack has no order to protect: DFS's contract is "some unexplored vertex next", and the pop-time `visited.Add` filter enforces *processed at most once* regardless of duplicates in the stack. BFS's contract *is* its order (rings) — a duplicate enqueue would insert a second, later processing of the same vertex and destroy the distance guarantee. Mark-early is a correctness requirement for BFS, a mere optimization for DFS.
3. In-degrees: A:0, B:1, C:2. Start with A → decrement B to 0, C to 1 → dequeue B → C to 0 → dequeue C. Order **A, B, C** — unique here, because the queue held one vertex at a time; with two simultaneously ready vertices either may be taken (the freedom that makes topological orders non-unique in general).
4. At step 2, C was extracted *before* B could be (priority 2 < 3... B entered at 4, C at 2) — by the invariant, when B was extracted at 3, any cheaper route would have needed an unsettled intermediate closer than B; the only remaining unsettled vertex was D (farther than B). Non-negative weights close the escape route: 3 is provably final.
</details>

---
# Part XIV — Greedy Algorithms and Dynamic Programming

Two rival strategies for *optimization* problems (choose the best among many possibilities):

- **Greedy** — make the locally best choice and never look back. Fast, fragile, occasionally provably perfect.
- **Dynamic programming** — solve every small subproblem *once*, remember it, build upward. Heavier, nearly always right when the problem has the right shape.

Mastery is knowing which door to open — and how to *prove* the choice.

---

# Chapter 42: Greedy Algorithms

## 42.1 The idea — choose, never reconsider

A **greedy algorithm** repeatedly chooses the best *local* option according to a fixed rule, commits to it permanently, and moves on:

```text
while a choice remains:
    take the choice that looks best RIGHT NOW
    commit (no undo, no reconsideration)
```

No backtracking (Part X), no re-examination, no memory of alternatives. That rigidity is greed's speed — one pass, often O(n log n) dominated by an initial sort — and its danger: local brilliance can be global ruin. Greedy is therefore an *aspiration* requiring one of two justifications:

- a **proof** that local choices compose into a global optimum (42.2's exchange argument), or
- an explicit decision to accept approximation (out of scope, but named honestly).

## 42.2 Activity selection — greedy with a proof

**Problem:** given events with start and finish times, choose the **maximum number** of non-overlapping events.

**The greedy rule (one of three candidates):**

| Candidate rule | Verdict | Counterexample |
|---|---|---|
| earliest **start** | ✗ wrong | a 9:00–17:00 event blocks five short ones |
| **longest** / shortest duration | ✗ wrong | two medium events can straddle and kill one short one |
| earliest **finish** | ✓ **correct** | — the one that frees you soonest |

```csharp
static List<(int Start, int Finish)> SelectActivities(
    List<(int Start, int Finish)> activities)
{
    List<(int Start, int Finish)> sorted = activities
        .OrderBy(activity => activity.Finish)
        .ToList();

    List<(int Start, int Finish)> chosen = new();
    int lastFinish = int.MinValue;

    foreach ((int start, int finish) in sorted)
    {
        if (start >= lastFinish)
        {
            chosen.Add((start, finish));
            lastFinish = finish;
        }
    }

    return chosen;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `OrderBy(activity => activity.Finish)` | The rule's sort: earliest-finish first. The lambda names each element's sort key (23.2's `OrderBy`, on a tuple field). |
| `int lastFinish = int.MinValue;` | When the calendar is empty; the first event can never collide with "minus infinity". An initialization that makes the first iteration uniform — no special case (the running-maximum lesson, generalized). |
| `if (start >= lastFinish)` | Compatibility test: the event begins at or after everything chosen so far has ended. |
| `chosen.Add(...)` | Commit — the greedy step: this event is in, permanently. |
| `lastFinish = finish;` | The accumulator advances: the new constraint on all future choices. |

**The exchange-argument proof** — why earliest-finish is *safe*, word by word:

> Take *any* optimal schedule S. Consider its **first** event f. If f is not the earliest-finishing event overall, **exchange** it with the earliest-finishing event e: e finishes no later than f, so e collides with *nothing* that f avoided — the rest of S still fits. The swapped schedule is still valid and still has the same size — still optimal. Hence *some* optimal schedule begins with the greedy choice; committing to it loses nothing. Repeat the argument on the remaining events: by induction, the greedy schedule's size equals the optimum. ∎

That is the template for legitimizing *any* greedy rule: show that swapping the greedy choice into any optimal solution preserves optimality. No proof, no trust.

**Complexity:** O(n log n) for the sort, O(n) for the scan — total **O(n log n)**, O(1) extra beyond the sorted copy.

## 42.3 The coin change warning — greed's failure, anatomized

**Problem:** pay an amount using the **fewest coins**, given available denominations.

For *canonical* systems (euro coins, US coins), taking the largest coin ≤ remaining amount works. For **arbitrary** denominations, it fails — memorably. Denominations `{1, 3, 4}`, amount 6:

| Strategy | Coins | Count |
|---|---|---:|
| Greedy: largest first | 4 + 1 + 1 | **3** |
| Optimal | 3 + 3 | **2** |

The greedy choice (4) *looked* best and poisoned the rest: it stranded two 1s. Greedy has no mechanism to notice this — no undo, no lookahead. The correct tools for arbitrary denominations are **exhaustive search** (Part X) or — the professional answer — **dynamic programming** (43.4 solves *this exact instance*). The rule to internalize:

> **Never assume greedy is correct without proving the problem has the required structure.** The proof is the license; the algorithm is merely the vehicle.

## 42.4 The greedy engineering checklist

Before shipping a greedy solution, interrogate it:

1. **Define the local choice precisely** — "earliest finishing time", not "shortest" (42.2's table shows how near-miss rules die).
2. **Test small counterexamples by hand** — the `{1,3,4}`-style probe; five minutes of adversarial doodling kills most wrong rules.
3. **Ask whether a choice can harm later options** — greed cannot undo; if the answer is "yes, and the harm is invisible at commit time", suspect greed.
4. **Search for an exchange- or cut-property proof** — the mathematical license (42.2; MST's cut property in 41.3).
5. **Compare against dynamic programming on small inputs** — DP is slower per run but *reliably* optimal; if DP and greedy agree on hundreds of random small cases and a proof backs the rule, confidence is earned.

When the checklist passes, greedy delivers the best cost/benefit ratio in the algorithmic toolbox: MST (41.3), Dijkstra (41.2 — greedy in its extraction step, licensed by its invariant), Huffman compression, interval scheduling — all proofs-and-passes.

---

# Chapter 43: Dynamic Programming

## 43.1 The two signs — when DP is the answer

Dynamic programming (DP) becomes the tool of choice when a problem shows **both** of these properties:

1. **Overlapping subproblems** — the same smaller problem reappears many times. Fibonacci: computing F(50) needs F(48) *twice* (via F(49) and F(48)'s own subtree) — and F(47) three times... the recursion tree (33.4's warning) explodes to Θ(φⁿ) nodes while only 50 *distinct* problems exist.
2. **Optimal substructure** — an optimal solution *contains* optimal solutions to its subproblems. Shortest paths: the shortest route to D through B *contains* the shortest route to B — if it contained a shorter route to B, swapping it in would shorten the whole (contradiction). Optimal substructure licenses building optimal answers from optimal sub-answers.

The strategy in one sentence: **solve each distinct subproblem once, store it, and answer every repeat by lookup.** Overlapping subproblems make the storage pay; optimal substructure makes the stored pieces assemble into the true optimum.

## 43.2 Memoization — top-down: recursion + a cache

```csharp
static int FibonacciMemoized(int n)
{
    Dictionary<int, int> memo = new();

    int Solve(int value)
    {
        if (value <= 1)
        {
            return value;
        }

        if (memo.TryGetValue(value, out int cached))
        {
            return cached;
        }

        int result = Solve(value - 1) + Solve(value - 2);
        memo[value] = result;
        return result;
    }

    return Solve(n);
}
```

Line by line — five beats:

| Piece | What it does |
|---|---|
| `Dictionary<int, int> memo` | **The memory**: from each solved subproblem to its answer — the entire "dynamic" in dynamic programming. |
| `if (value <= 1) return value;` | Base cases F(0)=0, F(1)=1 — answered directly (30.2). |
| `memo.TryGetValue(value, out int cached)` | **The lookup-before-compute** test (25.2's pattern, reused): solved before? |
| `return cached;` | Deliver the remembered answer — this one line is what collapses exponential into linear. |
| `memo[value] = result;` | **Remember after computing** — before returning, so every future request hits the cache. |

**The transformation's effect, counted:** naive F(50) performs ~2·F(50) ≈ 4·10¹⁰ calls (each F(k) call spawns F(k−1)+F(k−2), and duplicates are recomputed *every* time); memoized F(50) performs **50** computations and 49 cache hits. The recursion *tree* (Θ(φⁿ) nodes) collapses to a recursion *path* (n nodes) — the duplicates that were branches become lookups. Complexity: **O(n) time, O(n) space** (the memo + the call stack).

> Memoization = recursion's elegance + Part VIII's lookup speed. Top-down thinking: *"the answer for n is defined in terms of smaller answers"* — you write the definition and let the cache absorb the repetition.

## 43.3 Tabulation — bottom-up: tables without recursion

```csharp
static int FibonacciTabulated(int n)
{
    if (n <= 1)
    {
        return n;
    }

    int previous = 0;
    int current = 1;

    for (int index = 2; index <= n; index++)
    {
        int next = previous + current;
        previous = current;
        current = next;
    }

    return current;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `int previous = 0;` `int current = 1;` | The "table" **compressed to its last two rows** — F(0) and F(1), the only history the recurrence needs. |
| `int next = previous + current;` | Compute the next entry from the two before it — the recurrence, applied upward. |
| `previous = current; current = next;` | Slide the two-row window up one position; older history is discarded — *it is no longer needed*, which is exactly what O(1) space means here. |

Complexity: **O(n) time, O(1) space** — the memo's dictionary and the call stack both eliminated. Trade-off versus memoization: no recursion risk (30.5 — safe at n = 10⁶), but you must *know the computation order* upfront (small answers before larger ones); memoization discovers the order automatically by demand. The two forms compute **identical recurrences** — choose by risk profile and by how easily dependencies order themselves.

> **The general law of DP space:** a table dimension can be compressed to O(1) (or dropped) whenever the recurrence references only a *fixed-size window* of prior rows. Fibonacci looks back 2 → two variables. The knapsack below looks back 1 row → one row.

## 43.4 Coin change, solved properly — DP on a problem greedy failed

Return to `{1, 3, 4}`, amount 6 (42.3's disaster) and solve it with tabulation.

**Step 1 — define the state (the hard part; the loops are ceremony).**

> `best[a]` = the fewest coins that pay amount `a` exactly, using any denominations.

**Step 2 — the recurrence.** The last coin in any optimal payment of `a` is *some* denomination `c` with `c ≤ a`; before it was placed, we were paying `a − c` optimally:

```text
best[a] = 1 + min over denominations c ≤ a of best[a − c]
best[0] = 0                                (zero coins pay zero)
```

**Step 3 — compute upward** from amount 0 to the target; every `a − c` is smaller than `a`, so it is already final when needed:

```csharp
static int MinCoins(int[] coins, int amount)
{
    const int unreachable = int.MaxValue;

    int[] best = new int[amount + 1];
    best[0] = 0;

    for (int a = 1; a <= amount; a++)
    {
        best[a] = unreachable;

        foreach (int coin in coins)
        {
            if (coin <= a && best[a - coin] != unreachable)
            {
                if (best[a - coin] + 1 < best[a])
                {
                    best[a] = best[a - coin] + 1;
                }
            }
        }
    }

    return best[amount];
}
```

Line by line:

| Piece | What it does |
|---|---|
| `const int unreachable = int.MaxValue;` | A named sentinel for "no exact payment known" — ∞'s stand-in (41.2's `PositiveInfinity`, int edition). `const` = compile-time constant, inlined everywhere. |
| `best[0] = 0;` | The base case: amount zero costs zero coins. |
| `for (int a = 1; a <= amount; a++)` | Ascending amounts — the dependency-safe order (small before large). |
| `if (coin <= a && best[a - coin] != unreachable)` | Guard pair: the coin fits, **and** the sub-amount is itself payable (else 1 + ∞ is nonsense). |
| `if (best[a - coin] + 1 < best[a])` | **The relaxation** (41.2's heartbeat, recurring): does paying via this coin beat the record? |
| `best[a] = best[a - coin] + 1;` | Record update — keep the champion. |

**Trace, `{1, 3, 4}`, amounts 0..6:**

| a | candidates (via coin) | best[a] |
|---:|---|---:|
| 0 | — base | 0 |
| 1 | via 1: best[0]+1 = 1 | 1 |
| 2 | via 1: best[1]+1 = 2 | 2 |
| 3 | via 1: 3; via **3: best[0]+1 = 1** | **1** |
| 4 | via 1: 3; via 3: 2; via **4: 1** | **1** |
| 5 | via 1: 3; via 3: 2; via 4: 2 | 2 |
| 6 | via 1: 3; via **3: best[3]+1 = 2**; via 4: 3 | **2** ✓ |

**best[6] = 2 — the 3+3 payment greedy could not find.** Row 6 is the *entire argument for DP's existence* in one line of table: the optimal solution to 6 was assembled from the optimal solution to 3, which was assembled from 0 — optimal substructure, made operational.

**Complexity:** O(amount × denominations) time, O(amount) space — the two-dimensional loop over (state × choice). `return unreachable` (not shown in the guard) means "no exact payment exists" — a legitimate final answer to report distinctly from errors.

## 43.5 The knapsack pattern — DP's flagship family

**Problem:** items with weights and values; a knapsack of limited **capacity**; choose items to maximize total value within the weight budget.

**The state (the defining act):**

```text
best[i, capacity] = the best value achievable using only the first i items
                    under this remaining capacity
```

**The recurrence — one decision per item:** for item i (weight w, value v):

```text
best[i, capacity] = max(
    best[i − 1, capacity],            ← skip item i      (it simply is absent)
    best[i − 1, capacity − w] + v     ← take item i      (if it fits)
)
```

Every DP over *sequences of choices* has this silhouette: **state = (how far along, what resource remains); transition = the choice at hand.** The hard part is not typing the loops — it is defining the correct state. Type the state wrongly and no amount of clean code rescues the solution.

## 43.6 The dynamic-programming checklist

Run this interrogation for every candidate DP:

1. **What is the smallest subproblem?** (the base row/column — `best[0]`)
2. **What information fully describes a subproblem?** (the state — and nothing more: a *minimal* description, else the table explodes)
3. **What choices can be made next?** (the transitions — skip/take, relax/keep)
4. **What is the recurrence?** (the formula tying state to smaller states)
5. **What are the base cases?** (`best[0] = 0`; unreachable sentinels)
6. **In what order can states be computed?** (dependencies must point backward — ascending amounts, ascending items)
7. **Can the table be compressed?** (43.3's window law — often one row or two variables)

Answer all seven and the implementation is transcription. Which is the point: **DP moves the difficulty from coding to modeling** — from "how do I loop?" to "what exactly is a subproblem?". That relocation of difficulty is the entire discipline.

### Exercises for Part XIV

1. Activities `{(1,4), (2,3), (5,7), (4,6)}`: run SelectActivities by hand.
2. For denominations `{1, 5, 10}`, does greedy coin change work? Prove or find a counterexample.
3. Write the memoized version of MinCoins (top-down) — what changes structurally versus 43.4?
4. Knapsack: items (w=2,v=3), (w=3,v=4), (w=4,v=5), capacity 5. Fill `best[i,c]` for i=0..2, c=0..5 by hand.

<details><summary>Solutions</summary>

1. Sorted by finish: (2,3), (1,4), (4,6), (5,7). Take (2,3) [lastFinish=3]; (1,4): start 1 < 3 skip; (4,6): 4 ≥ 3 take [lastFinish=6]; (5,7): 5 < 6 skip. **{(2,3), (4,6)}** — two events, provably maximum (no three of these are pairwise compatible: (1,4),(4,6) and (2,3) alone... any third overlaps one of the chosen two).
2. Works for *this* system (each coin > sums below it by the canonical-chain property: 1 covers 0–4, 5 = 5, 10 = 5+5 boundary...). Proof sketch: with {1,5,10}, greedy never uses five 1s (a 5 replaces them) nor two 5s (a 10 replaces them) — the exchange argument holds. The lesson's edge: *this* system's proof does not transfer — `{1,3,4}` already falsified the general claim.
3. Signature `int Solve(int a)` with `Dictionary<int,int> memo` closed over; the ascending loop becomes on-demand recursion: base `a == 0 → 0`; lookup; else `min` over coins of `1 + Solve(a - coin)` (guarded). Structurally: the *iteration order* (checklist Q6) disappears — demand discovers it — at the cost of recursion depth O(amount) (30.5) and memo overhead.
4. Row i=0 (no items): all zeros. i=1 (item w2v3): c≥2 → 3. i=2 adds (w3v4): c=2→3; c=3→4; c=4→4; c=5→ max(3, 3+... take: best[1,2]+4=3+4=7, skip: 3) → **7** (items 1+2: weight 5 ≤ 5, value 7 — beating item 3 alone at 5). ✓ The recurrence, seen working: best[2,5] = best[1,2] + 4.
</details>

---
# Part XV — String and Text Algorithms

Text is the most common data in real systems — names, logs, documents, DNA, code. String algorithms are where small details (an invisible space, a different letter case) silently change correctness. This chapter builds the core toolkit and — more than anywhere else — hammers the discipline of **defining the comparison rule before writing the comparison**.

---

# Chapter 44: Working with Text

## 44.1 Normalize before comparing — text equality depends on rules

When are two strings "equal"? The naive answer (`==`) demands *bit-for-bit* identity. Real requirements are usually subtler:

```csharp
bool same = left.Equals(
    right,
    StringComparison.OrdinalIgnoreCase);
```

Word by word:

| Piece | What it does |
|---|---|
| `.Equals(right, ...)` | A comparison *method* with an overload taking an explicit comparison rule. |
| `StringComparison.OrdinalIgnoreCase` | The rule: ignore ASCII case, no culture-specific transformations — **the correct default for identifiers, protocol values, file names, enum-like strings**. |

The critical safety rule: **do not silently apply culture-sensitive transformations** (lowercasing via `ToLower()` with the current culture, or `ToLowerInvariant` used *as a comparison*) when identifiers or protocol values require exact comparison — some cultures transform letters in ways that collide or split unexpectedly (the Turkish dotless-i being the famous case). Encoding the rule *in the comparison call* (`OrdinalIgnoreCase`) instead of *mutating the data* (`left.ToLower() == right.ToLower()`) is both faster (no allocation) and more honest (the data is unchanged; the *comparison* carries the policy).

**The general precept:** every string problem begins with a written rule — case? spaces? accents? punctuation? — *before* a single comparison is typed. The anagram section below shows the rule changing the entire algorithm.

## 44.2 Palindrome check — two pointers on text

> A palindrome reads the same in both directions: `racecar`, `noon`.

The two-pointer pattern (14.2) in its purest form — one finger at each end, walking inward:

```csharp
static bool IsPalindrome(string text)
{
    int left = 0;
    int right = text.Length - 1;

    while (left < right)
    {
        if (text[left] != text[right])
        {
            return false;
        }

        left++;
        right--;
    }

    return true;
}
```

Line by line:

| Line | What it does |
|---|---|
| `int left = 0; int right = text.Length - 1;` | Mirror fingers at the two ends. |
| `while (left < right)` | Continue while a *pair* remains unexamined — the crossing condition is the stop (14.2's discipline, mirrored inward). |
| `if (text[left] != text[right])` | One mirrored pair disagrees — the palindrome verdict is already **false**; early exit. |
| `left++; right--;` | Walk inward one step from each side. |
| `return true;` | All pairs agreed (a middle single character, when length is odd, is compared with nothing — correctly: it equals itself). |

**Trace `"racecar"`:**

| left | right | pair | equal? |
|---:|---:|---|---|
| 0 | 6 | r / r | ✓ |
| 1 | 5 | a / a | ✓ |
| 2 | 4 | c / c | ✓ |
| 3 | 3 | — | loop ends (left == right) → **true** |

**Trace `"perla"`:** pair 0: p/a → **false** immediately — one comparison.

**Complexity:** O(n) time — each character examined at most once (half the pairs, two characters per pair); **O(1) extra space** — two integers. The elegance: no copy, no reversal, no allocation — the comparison happens *in place against itself*.

*(Exercise-in-waiting: the strict version here is case- and space-sensitive — `"Never odd or even"` fails. Normalizing first (44.1's discipline) — filtering to letters and applying `OrdinalIgnoreCase` — is the natural extension; the pointer walk itself is untouched.)*

## 44.3 Anagram detection — frequency counting decides

> Two words are anagrams if they contain the same characters, same counts: `listen` / `silent`, `dormitory` / `dirty room` (with the *right* normalization rule!).

The comparison rule, written first: **ignore spaces; case-insensitive; everything else (punctuation, digits) counts as a character.** Under that rule the problem becomes *multiset equality* — and 14.4's frequency counting is the native tool:

```csharp
static bool AreAnagrams(string first, string second)
{
    string left = first.Replace(" ", "").ToLowerInvariant();
    string right = second.Replace(" ", "").ToLowerInvariant();

    if (left.Length != right.Length)
    {
        return false;
    }

    Dictionary<char, int> counts = new();

    foreach (char character in left)
    {
        counts[character] = counts.GetValueOrDefault(character) + 1;
    }

    foreach (char character in right)
    {
        if (!counts.TryGetValue(character, out int count))
        {
            return false;
        }

        if (count == 1)
        {
            counts.Remove(character);
        }
        else
        {
            counts[character] = count - 1;
        }
    }

    return counts.Count == 0;
}
```

Line by line — three movements:

| Piece | What it does |
|---|---|
| `first.Replace(" ", "")` | **Normalization, applied once, up front** — the written rule, executed. Spaces out. |
| `.ToLowerInvariant()` | Case folding *invariant* across machines — appropriate here because the domain is "letters as letters", not culture-sensitive text (44.1's boundary respected: the data is normalized *by design decision*, not silently). |
| `if (left.Length != right.Length) return false;` | **The cheap kill**: different lengths can never match — O(1) rejection before any counting work. Test cheap necessary conditions first, always. |
| first `foreach` | Build the histogram of the first string (14.4 verbatim). |
| second `foreach` | **Subtract** the second string's histogram: each character must exist and have a positive count... |
| `counts.Remove(character)` / `counts[character] = count - 1` | ...consume one occurrence: drop the key at zero, or decrement. Absence (`TryGetValue` false) → **false** immediately. |
| `return counts.Count == 0;` | Every character perfectly consumed — nothing left over, nothing missing → same multiset → **true**. |

**Trace `"adam"` vs `"mada"`:** histogram of adam {a:2, d:1, m:1}; subtract m,a,d,a → each found; counts empty → **true**. And `"abb"` vs `"aab"`: build {a:1, b:2}; subtract a (1→remove), a → `TryGetValue` **fails → false** — the *excess* a is caught the instant it cannot be consumed.

**Complexity:** O(n) expected time — one pass per string with O(1) hash work per character; O(k) space (k = distinct characters — ≤ 26 for letters... but unbounded in general; state which alphabet you assume).

*The alternative* — sort both strings and compare (`listen` → `eilnst`, `silent` → `eilnst`) — is O(n log n) and famously readable; the frequency version wins asymptotically and generalizes better (to counting, to sliding-window variants, to streams — 45's analyses reuse it verbatim).

## 44.4 Pattern matching — finding a substring

> Does `text` contain `pattern`, and where?

**The naive scan** — try every starting position, verify character-by-character:

```csharp
static int NaiveSearch(string text, string pattern)
{
    for (int start = 0; start + pattern.Length <= text.Length; start++)
    {
        int matched = 0;

        while (matched < pattern.Length && text[start + matched] == pattern[matched])
        {
            matched++;
        }

        if (matched == pattern.Length)
        {
            return start;
        }
    }

    return -1;
}
```

The two nested walks cost **O(n·m)** worst case (n text, m pattern) — pathological on inputs like `"AAAA...A"` searched for `"AAA...AB"`, where every start re-verifies nearly the whole pattern. For small inputs and one-off searches it is *fine* — genuinely, honestly fine (13.8's discipline).

For large or repeated searches, two classics reduce redundant comparisons:

- **Knuth–Morris–Pratt (KMP)** — *precompute the pattern against itself*: a table answers "after matching j characters and then failing, what is the longest pattern-prefix that is already matched?" — so the text pointer **never moves backward**, and total work is **O(n + m)**. The insight: a failed match has already *told* you things about the text — remember them instead of re-reading.
- **Boyer–Moore** — scan the pattern right-to-left and jump the pattern past mismatched characters (with tables of where each character last occurs in the pattern) — sublinear on average for large alphabets: some text characters are never examined at all.

The engineering decision, as always, is a workload question — text size, pattern size, search count, memory limits, library support (`string.Contains`/`IndexOf` ship optimized implementations; C# `IndexOf` uses vectorized SIMD scanning — hardware-accelerated naive-plus). **Know the ideas; use the library; revisit when the workload profile demands it.**

## 44.5 Tokenization and parsing — the text pipeline

Text analysis is rarely one algorithm — it is a **pipeline of small transformations**, each with its own contract (9.3):

```text
raw text ──► normalize ──► tokenize ──► classify ──► aggregate ──► report
 (bytes)     (case, rules)  (split into    (word? num?   (count, sum,    (tables,
                              tokens)       symbol?)     group)           prose)
```

| Stage | Example in/out | The contract |
|---|---|---|
| normalize | `"The  THE"` → `"the the"` | one written rule (44.1) |
| tokenize | `"the the"` → `[the] [the]` | the splitting rule (spaces? punctuation? both?) |
| classify | `[the]` → stopword | per-token decision |
| aggregate | counts → `{the: 2}` | frequency counting (14.4) |
| report | `{the: 2}` → a line of output | the audience's format |

Each stage is an algorithmic transformation and should have a **clear contract** — inputs, outputs, and its own small tests (54). Pipelines fail at their *joints*: a tokenizer that keeps punctuation makes a classifier see `"word,"` and `"word"` as different tokens, and every downstream count silently splits. The discipline of stage contracts is what keeps composed text systems debuggable — the Algorithm Lab's CSV reader (48) is exactly such a stage, with its own documented tolerance rule.

### Exercises for Chapter 44

1. `IsPalindrome("AbBa")` — what does it return, and what one-line preprocessing makes it true?
2. Are `"Dormitory"` and `"Dirty Room"` anagrams under 44.3's code? Walk the normalization step.
3. In NaiveSearch, why `start + pattern.Length <= text.Length` and not `start < text.Length`?
4. Your tokenizer splits on spaces; the input uses commas (`"a, b"`). Name the joint failure and which stages see it.

<details><summary>Solutions</summary>

1. False as written ('A' ≠ 'a' by ordinal comparison at pair 0). Preprocess `text.ToLowerInvariant()` — the 44.1 rule chosen by design (case-insensitive palindromes are the usual intent).
2. Yes: normalization strips spaces and folds case → `dormitory` vs `dirtyroom` — same 9 letters; lengths match; histograms consume exactly. ✓
3. A pattern cannot start where it cannot *fit*: the last legal start is `text.Length − pattern.Length`; without the tightened bound the inner loop reads `text[start + matched]` past the end — an out-of-range crash, i.e. the off-by-one family of 56, prevented by loop-bound design.
4. Tokens `"a,"` and `"b"` — the trailing comma rides a token; classification (is it a word?) sees a different string than intended and aggregates split (`"a,"` ≠ `"a"`). The failure is *visible in aggregate*, but *caused at tokenize* — debug pipelines at their contracts, not their symptoms.
</details>

---
# Part XVI — Algorithms for Data Analysis

Everything so far built machinery. This part points it at a domain: **descriptive data analysis** — the statistics behind every dashboard and report. The chapter's thesis: statistical formulas *are* algorithms, with the same contracts, edge cases, invariants, and complexity discipline as everything else in this book — plus one duty the others don't carry: **an honest account of what the numbers assume.**

---

# Chapter 45: Statistics as Algorithms

## 45.1 The data-analysis pipeline

A reliable analysis is a pipeline (44.5's discipline, data edition):

```text
1. acquisition   ── where does the data come from? (file, sensor, API)
2. validation    ── is it the shape it claims? (numeric? in range?)
3. cleaning      ── what do we do about the bad rows?
4. transformation── normalize units, types, categories
5. aggregation   ── grouping, summing, counting
6. calculation   ── the statistics themselves
7. anomaly       ── detection: what is unusual?
8. interpretation── what does it mean? what can NOT be concluded?
9. reporting     ── for whom, in what format?
```

The governing law, stated once and never forgotten: **the output is only as reliable as the assumptions and transformations that precede it.** A perfect median over dirty data is a perfectly wrong number. This is why the Algorithm Lab (Part XVII) spends its *first* engineering effort on validation and cleaning, not on formulas.

## 45.2 Mean, median, mode — the three "averages"

### Mean — the balance point

```csharp
static double Mean(IReadOnlyList<double> values)
{
    if (values.Count == 0)
    {
        throw new ArgumentException("At least one value is required.");
    }

    double total = 0;

    foreach (double value in values)
    {
        total += value;
    }

    return total / values.Count;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `IReadOnlyList<double>` | The parameter type — "any list you may **read** but not mutate through me" (`Array`, `List`, the lab's loaded data — all fit; 47.2 dissects the choice). The *caller keeps ownership*; the algorithm promises not to reorder or alter the input — a contract expressed as a *type*. |
| `if (values.Count == 0) throw` | The **precondition guard** (12.3's discipline): the mean of nothing is undefined — refuse loudly rather than return `NaN` (0/0) silently. |
| `double total = 0;` | The accumulator (8.5) — `double`, matching the element type. |
| `return total / values.Count;` | Sum ÷ count — the definition itself, one line. |

**Complexity:** O(n) time, O(1) space. **Sensitivity:** the mean is a *balance point* — every value pulls on it. One wildly extreme salary drags the mean of a whole company. That vulnerability is the median's raison d'être:

### Median — the middle person

```csharp
static double Median(IReadOnlyList<double> values)
{
    if (values.Count == 0)
    {
        throw new ArgumentException("At least one value is required.");
    }

    double[] sorted = values.OrderBy(value => value).ToArray();
    int middle = sorted.Length / 2;

    if (sorted.Length % 2 == 1)
    {
        return sorted[middle];
    }

    return (sorted[middle - 1] + sorted[middle]) / 2.0;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `values.OrderBy(...).ToArray()` | **Sort a copy** (23.2's LINQ — new sequence; the caller's order is untouched). The median is a *positional* statistic: it exists only in sorted order. |
| `int middle = sorted.Length / 2;` | The middle index via integer division. For n = 5: 5/2 = 2 — the third element, exact center. |
| `if (sorted.Length % 2 == 1)` | **Odd count** → one exact middle element — return it directly. |
| `(sorted[middle - 1] + sorted[middle]) / 2.0` | **Even count** → no middle element — average the two center elements. The `/ 2.0` (not `/ 2`): integer division would truncate (7's `%` sibling — `/` on two ints discards decimals; 3/2 = 1, while 3/2.0 = 1.5). The `.0` is load-bearing. |

**Trace `{4, 1, 7}`:** sorted `{1, 4, 7}`, odd, middle index 1 → **4**. **Trace `{1, 3, 7, 9}`:** even, middles indexes 1, 2 → (3 + 7)/2.0 = **5** — a value *not in the list*, and correctly so (the definition demands it).

**Complexity:** O(n log n) via the sort (a selection-of-median algorithm exists at O(n) — quickselect, quicksort's partition recycled — noted for the curious; the sort is the readable default). **Robustness:** the median counts *ranks*, not magnitudes — a house price of 90,000,000 beside nine 300,000s moves the mean absurdly and the median by one position. For skewed data (income, house prices, latencies), **the median is the honest "typical" value.**

### Mode — the loudest voice

The most frequent value — **frequency counting (14.4), then scan for the maximum count**: build `Dictionary<T,int>`, one pass to count, one pass over entries to find the key with the largest count. O(n) expected. The mode handles *categorical* data (most popular product) where mean/median are meaningless — and unlike them, it may not exist (all values distinct) or may not be unique (a tie). *Document the tie rule* (first? all? alphabetical?) — 9.2's interrogation, statistical edition.

## 45.3 Variance and standard deviation — how spread out?

The mean says where the center is; **variance** says how far the values scatter from it:

```text
population variance = the average of SQUARED distances from the mean
standard deviation  = the square root of variance  (back in original units)
```

```csharp
static double PopulationStandardDeviation(IReadOnlyList<double> values)
{
    double average = Mean(values);
    double squaredDistance = 0;

    foreach (double value in values)
    {
        double difference = value - average;
        squaredDistance += difference * difference;
    }

    double variance = squaredDistance / values.Count;
    return Math.Sqrt(variance);
}
```

Line by line:

| Piece | What it does |
|---|---|
| `double average = Mean(values);` | The center, computed first — distances need a reference point. |
| `double difference = value - average;` | This value's signed deviation from the mean. |
| `squaredDistance += difference * difference;` | Accumulate the **squared** deviation. Why square? (a) raw deviations sum to *exactly zero* — positives and negatives cancel — so plain averaging measures nothing; (b) squaring punishes large outliers *quadratically*; (c) squares make the algebra clean (57.5's variance tricks depend on it). |
| `variance = squaredDistance / values.Count;` | The average squared deviation — **population** version: divide by n. |
| `Math.Sqrt(variance);` | Un-square — standard deviation returns to the *original units* ("±12.4 mm", not "±153 mm²"), which is what makes it interpretable. |

**The population/sample distinction — document it or be wrong:** for a *sample* estimating a population's spread, the denominator is `n − 1` (Bessel's correction — dividing by n systematically underestimates spread, and n−1 exactly compensates in expectation). **Document which you calculate**: a silent population-vs-sample mismatch between your library and your colleague's yields numbers that differ by up to ~√2 for n=2 — and no error message. The Algorithm Lab's report literally prints the words "Population standard deviation" (52) — the honesty is in the label.

**Trace `{2, 4, 4, 4, 5, 5, 7, 9}`** (mean 5): differences {−3,−1,−1,−1,0,0,2,4}; squares {9,1,1,1,0,0,4,16} summing 32; variance 32/8 = 4; stdev √4 = **2**. Two passes, O(n) time, O(1) space — plus the one subtlety: accumulating squared differences can lose precision on ill-conditioned data (57.5 — the "one-pass variance" trap; the two-pass form here is the numerically safer default).

## 45.4 Grouping and aggregation — GROUP BY as an algorithm

> "Total sales per category" — the shape of half the world's reports.

```csharp
static Dictionary<string, double> TotalByCategory(
    IEnumerable<(string Category, double Amount)> rows)
{
    Dictionary<string, double> totals = new();

    foreach ((string category, double amount) in rows)
    {
        totals[category] = totals.GetValueOrDefault(category) + amount;
    }

    return totals;
}
```

Line by line:

| Piece | What it does |
|---|---|
| `IEnumerable<(string Category, double Amount)>` | **The input shape**: a stream of *tuples* — each row is (category, amount) — declared `IEnumerable` = "any sequence, including lazy ones" (a file read line-by-line, a LINQ query: the algorithm does not care *where* rows come from). **Tuple element names** (`Category`, `Amount`) make the deconstruction self-documenting. |
| `foreach ((string category, double amount) in rows)` | **Tuple deconstruction** — each row splits into named pieces at the loop (41.2's pattern, recurring). |
| `totals.GetValueOrDefault(category) + amount` | 14.4's "old-or-zero" — a category's first sighting starts from 0; later sightings accumulate. The entire GROUP-BY idea in one expression. |
| `return totals;` | Category → running total: the aggregated report, keyed. |

**Complexity:** expected **O(n)** time — one hash update per row; O(k) space for k distinct categories. This is the hash-based aggregation algorithm (Part VIII's payoff, industrial scale) — the same machinery behind database `GROUP BY`, spreadsheet pivot tables, and 51.4's lab statistics. Follow-ups compose: mean-per-category (also accumulate counts), top-category (scan the finished dictionary for the max — the mode, reborn), multi-level grouping (compound keys like `category + "|" + month`).

## 45.5 Outlier detection — the IQR rule

> Which values are so unusual that they deserve a human's attention?

The **interquartile range** rule — a rank-based fence that inherits the median's robustness:

```text
Q1  = 25th percentile     (a quarter of the data lies below)
Q3  = 75th percentile     (three quarters below)
IQR = Q3 − Q1             (the spread of the middle 50%)

lower fence = Q1 − 1.5 × IQR
upper fence = Q3 + 1.5 × IQR
values outside [lower, upper] → flagged as potential outliers
```

Why it works: the fences are defined by the *middle half's* spread, so extreme values cannot inflate their own detection threshold — a point 100× the median stretches IQR only through quartile movement, not proportionally. (For normal-ish data the 1.5 factor flags ≈ 0.7% of points — a historical constant, not a law of nature.)

**Two sentences of professional duty, mandatory:** (1) *A flagged value is not automatically an error* — the 100.0 in the Lab's sample data may be a real sale, a real sensor event, a real fraud attempt; the flag means *look at me*, not *delete me*. (2) *An unflagged dataset is not guaranteed clean* — outliers clustered together, or subtle drift, can hide inside the fences. Detection is a question-generator, never a verdict (3.4's ethics, operationalized).

## 45.6 Data quality checks — the pre-flight list

Before analyzing any data, run this interrogation (the 1–3 stages of 45.1, concretized):

- **missing values** — nulls, blanks, default zeros: are they *recorded zeros* or *absent data*? (Different meanings; different handling.)
- **duplicate records** — double-logged rows inflate counts and bias means (25.1's detector, deployed).
- **impossible ranges** — negative ages, 25-hour durations: validation catches what statistics would silently absorb.
- **inconsistent categories** — `"Electronics"`, `"electronics"`, `"ELECTRONICS "`: three keys in your group-by (44.1 — normalization *before* aggregation, or the report splits).
- **mixed date formats** — `2024-01-05` vs `05/01/2024`: same string, different days.
- **unexpected units** — one sensor in °C, another in °F, mixed into one column.
- **extreme values** — 45.5's flags, awaiting human judgment.
- **sampling bias** — *who is missing from the data entirely?* The users who churned silently, the sensors that never shipped.

The closing law of the Part, and one of the book's:

> **An algorithm can calculate a precise answer from inaccurate data. Precision is not the same as validity.**

Sixteen significant digits of a wrong number are still wrong. The lab you build next treats validation as a *feature*, not a chore — because the pipeline's law (45.1) is enforced in its architecture.

### Exercises for Chapter 45

1. `{1, 2, 3, 1000}`: mean? median? Which better answers "typical", and why in one sentence?
2. Compute population stdev of `{4, 4}`. Then of `{0, 8}`. Same mean — what does the stdev contrast capture?
3. Extend `TotalByCategory` to also return each category's row count. What accumulators change?
4. For data `{1, 2, 3, 4, 5, 6, 7, 8, 100}`: compute Q1, Q3, IQR, and the fences. Is 100 flagged?

<details><summary>Solutions</summary>

1. Mean = 1006/4 = 251.5; median = (2+3)/2 = 2.5. The median — the mean has been dragged ~100× past three of the four values by a single extreme; the median counts rank, not magnitude.
2. Mean 4 both. `{4,4}`: differences 0,0 → stdev **0** (no spread). `{0,8}`: differences ±4 → variance 16 → stdev **4**. The pair (mean, stdev) = (location, spread) — identical centers, opposite scatter, captured precisely.
3. A second dictionary `Dictionary<string,int> counts` with `counts[category] = GetValueOrDefault(...) + 1` beside the totals update — or a single dictionary into `(double Total, int Count)` tuples. One pass, still O(n) expected.
4. Sorted data, n=9: Q1 = element at position (9−1)·0.25 = 2 → **2**; Q3 at (9−1)·0.75 = 6 → **7**; IQR = 5; fences: lower 2 − 7.5 = −5.5, upper 7 + 7.5 = **14.5**. 100 > 14.5 → **flagged** ✓ — despite being ~10× the median, the fence barely moved.
</details>

---
# Part XVII — Building the Algorithm Lab

The capstone: a complete, professional-structured C# console application that **uses the whole book** — reading numerical data from CSV, validating it, sorting it, searching it, computing descriptive statistics, detecting outliers, and printing an analytical report. You will build it file by file, line by line, in the order a real project grows.

---

# Chapter 46: Project Setup and Structure

## 46.1 Create the project

```bash
dotnet new console -n AlgorithmLab
cd AlgorithmLab
mkdir Algorithms Models Services
```

Word by word: the first two lines are Chapter 5's ritual (console template, named `AlgorithmLab`, terminal moved inside). The third line, `mkdir Algorithms Models Services`, creates **three folders in one command** — `mkdir` takes multiple names and creates a directory per argument. Folders in a C# project are *organizational namespaces* (below), not just visual tidiness.

## 46.2 The architecture — why folders at all?

```text
AlgorithmLab/
├── Algorithms/
│   ├── SearchAlgorithms.cs      ← the pure algorithm library (Part VI)
│   ├── SortAlgorithms.cs        ← (Part VII)
│   └── StatisticsAlgorithms.cs  ← (Part XVI)
├── Models/
│   └── AnalysisReport.cs        ← the data shape of a finished analysis
├── Services/
│   └── CsvNumberReader.cs       ← I/O: the outside world, quarantined
└── Program.cs                   ← composition: wires everything together
```

The layout encodes one architectural decision, and it is the most transferable idea in this Part:

> **Algorithms are pure; services touch the world; models carry results; the program composes.**

- `Algorithms/` — no file reads, no console output, no clocks: pure functions from values to values (testable to exhaustion, Chapter 54).
- `Services/` — the *only* place that touches files, networks, clocks: the impure edge, kept thin and quarantined.
- `Models/` — inert data shapes: what the analysis *is*, independent of how it is computed or printed.
- `Program.cs` — the composer: fetches data via a service, runs algorithms, formats output.

When a bug appears, this structure answers "where do I look?" before you open a single file: wrong number → Algorithms; wrong file behavior → Services; wrong output shape → Models; wrong wiring → Program. In C#, each folder becomes a **namespace** — `AlgorithmLab.Algorithms`, `AlgorithmLab.Services`, `AlgorithmLab.Models` — and the names in `using` statements at the top of files (52) are exactly these.

## 46.3 What the application will do — the specification

Written as a contract (9.3), before any code:

```text
1. read numbers from a CSV file (comma-separated values, one or many per line)
2. validate the values (skip cells that are not numbers — and report that policy)
3. show count, minimum, maximum, mean, median, and population standard deviation
4. sort the data (our own merge sort)
5. search for a value (our own binary search, on the sorted copy)
6. report possible outliers (the IQR fences)
7. print all of it as a small analytical report
```

Edge cases, decided *now*, not discovered later: empty file → a clear message, no crash; missing file → a clear message, exit non-zero; invalid cells → skipped (a *documented* choice — the beginner version tolerates them; 58's capstone upgrades replace this with line-and-column reporting); single value → all statistics defined, stdev 0.

---

# Chapter 47: The Model

## 47.1 Create `Models/AnalysisReport.cs`

```csharp
namespace AlgorithmLab.Models;

public sealed class AnalysisReport
{
    public int Count { get; init; }
    public double Minimum { get; init; }
    public double Maximum { get; init; }
    public double Mean { get; init; }
    public double Median { get; init; }
    public double StandardDeviation { get; init; }
    public IReadOnlyList<double> Outliers { get; init; } = Array.Empty<double>();
}
```

## 47.2 Line by line, and word by word

| Piece | What it does |
|---|---|
| `namespace AlgorithmLab.Models;` | Declares this file's namespace — its fully-qualified address in the project (`AlgorithmLab.Models`). The trailing semicolon form ("file-scoped namespace") spares one level of braces for the whole file. Consumers will write `using AlgorithmLab.Models;` to see these types by short name. |
| `public sealed class` | A class: a *reference type* grouping data + behavior (here: only data). `public` — visible outside this namespace. `sealed` (29.2, 35.3) — closed to inheritance: the shape is final, a deliberate design statement. |
| `public int Count { get; init; }` | A **property**: a named value on the object. `get` — readable from outside; `init` (short for *initializer*) — assignable **only during object creation**, frozen afterward. The report is an immutable snapshot: once built, nobody — including its own author's later typos — can quietly edit `Mean`. |

Word by word, `{ get; init; }` deserves the full ceremony — it is modern C#'s most load-bearing punctuation: `get;` declares a *getter* (reading is public), `init;` declares an *init-only setter* (writing is allowed solely inside an object initializer / constructor). After construction, any assignment `report.Mean = 0.5;` is a **compile error**. Immutability-by-construction is the cheapest correctness tool in the language: a report built correctly *stays* correct.

| Piece | What it does |
|---|---|
| `public IReadOnlyList<double> Outliers` | The flagged values — typed **read-only-list** (45.2's discipline at the type level): callers may *read* the outliers but cannot add/remove through this property. |
| `= Array.Empty<double>();` | A **default value**: if a construction does not supply `Outliers`, it is the shared empty array (8's `Array.Empty` — no allocation, no null-check needed downstream). The pattern: *defaults that are safe, not null.* |

## 47.3 Constructing a report — the object initializer

```csharp
AnalysisReport report = new()
{
    Count = 9,
    Minimum = 11.4,
    Maximum = 100.0,
    Mean = 23.14,
    Median = 13.8,
    StandardDeviation = 27.16,
    Outliers = new[] { 100.0 }
};
```

Word by word: `new()` — target-typed construction (6.4); `{ ... }` — the **object initializer**: assign each `init` property by name, in any order, omitting any (defaults apply). The result: a fully-formed, forever-frozen record of one analysis. *Every property assigned exactly once, at birth* — that is the whole lifecycle of this type, and it is the right lifecycle for results.

---

# Chapter 48: The CSV Reader

## 48.1 Create `Services/CsvNumberReader.cs`

```csharp
using System.Globalization;

namespace AlgorithmLab.Services;

public sealed class CsvNumberReader
{
    public IReadOnlyList<double> Read(string path)
    {
        if (!File.Exists(path))
        {
            throw new FileNotFoundException("The data file was not found.", path);
        }

        List<double> values = new();
        string[] lines = File.ReadAllLines(path);

        foreach (string line in lines)
        {
            string[] cells = line.Split(',', StringSplitOptions.RemoveEmptyEntries);

            foreach (string cell in cells)
            {
                if (double.TryParse(
                    cell.Trim(),
                    NumberStyles.Float,
                    CultureInfo.InvariantCulture,
                    out double value))
                {
                    values.Add(value);
                }
            }
        }

        return values;
    }
}
```

## 48.2 Line by line

| Piece | What it does |
|---|---|
| `using System.Globalization;` | Imports the namespace containing `CultureInfo` and `NumberStyles` — the machinery for *culture-independent* number parsing (below). |
| `namespace AlgorithmLab.Services;` | This file lives in the Services namespace — the quarantined I/O edge (46.2). |
| `public sealed class CsvNumberReader` | A *service* as a class: it carries no state (no fields!) — the class is a *naming and organizational* unit; you create one instance and call `Read`. |
| `public IReadOnlyList<double> Read(string path)` | The contract: takes a path, returns a read-only list of parsed numbers (45.2's `IReadOnlyList` — the caller can read, never mutate through it). |
| `if (!File.Exists(path))` | **Validate before acting** (45.6's pre-flight, code-level): check the external world *before* touching it — the empty-case discipline of Chapter 1, applied to files. |
| `throw new FileNotFoundException("...", path);` | The loud refusal (12.3): a specific, standard exception carrying a human message *and the path that was missing*. The caller (52) catches and reports it. |
| `List<double> values = new();` | The accumulator — grown as values are discovered (6.4's growable list; arrays cannot grow, and we do not know the count upfront). |
| `File.ReadAllLines(path)` | Reads the whole file into a `string[]` — one element per line, newlines stripped. (A streaming `ReadLines` alternative exists for huge files — 57's online/offline decision, made here on the side of simplicity.) |
| `line.Split(',', StringSplitOptions.RemoveEmptyEntries)` | **Tokenization** (44.5): cut each line at commas; `RemoveEmptyEntries` drops empty fragments — so `"1,,2"` yields two cells, and a trailing comma is harmless. The *tolerance policy*, one parameter. |
| `cell.Trim()` | Strip surrounding whitespace (`" 12.5 "` → `"12.5"`) — the normalization stage of the pipeline (45.1, step 4). |
| `double.TryParse(...)` | The **safe parser**: attempts conversion, returns `bool` — never throws. On failure we simply skip the cell: the documented tolerance choice of 46.3. |
| `out double value` | The `out` channel (25.2): on success, the parsed number is written here for us to read. |
| `NumberStyles.Float` | Which textual forms are legal: sign, decimal point, leading/trailing whitespace (already trimmed), exponent — but *not* thousands separators or currency symbols. |
| `CultureInfo.InvariantCulture` | **The crucial argument**: parse numbers by the invariant (culture-neutral) convention — `.` as decimal separator, always. Without it, parsing depends on the *machine's regional settings*: `"12.5"` fails on a German-locale machine (which expects `"12,5"`), or worse, silently parses `"12,5"` as 125... The invariant culture makes the **file format** and the **parser** agree, on every machine on Earth — the single most important word in this file. |
| `values.Add(value);` | Harvest the parsed number. |
| `return values;` | The parsed dataset. (The `List<double>` *is* an `IReadOnlyList<double>` — it is returned through that narrower view; the caller cannot mutate what it cannot see through.) |

## 48.3 The reader's pipeline, seen whole

Map the method onto 45.1 and 44.5 — every stage is present:

```text
acquisition   File.ReadAllLines
validation    TryParse + NumberStyles
cleaning      skip invalid cells (documented policy)
normalization Trim, InvariantCulture
tokenize      Split(',')
aggregation   values.Add — the accumulating list
```

One method, one documented personality: *tolerant of bad cells, strict about locale, loud about missing files.* That personality is a **design decision stated in code** — and 58's capstone list item 5 ("report invalid cells with line and column numbers") is exactly the upgrade from tolerant to strict.

---

# Chapter 49: The Search Algorithms File

## 49.1 Create `Algorithms/SearchAlgorithms.cs`

```csharp
namespace AlgorithmLab.Algorithms;

public static class SearchAlgorithms
{
    public static int LinearSearch(
        IReadOnlyList<double> values,
        double target)
    {
        for (int index = 0; index < values.Count; index++)
        {
            if (values[index] == target)
            {
                return index;
            }
        }

        return -1;
    }

    public static int BinarySearch(
        IReadOnlyList<double> sortedValues,
        double target)
    {
        int low = 0;
        int high = sortedValues.Count - 1;

        while (low <= high)
        {
            int middle = low + (high - low) / 2;

            if (sortedValues[middle] == target)
            {
                return middle;
            }

            if (sortedValues[middle] < target)
            {
                low = middle + 1;
            }
            else
            {
                high = middle - 1;
            }
        }

        return -1;
    }
}
```

## 49.2 The new vocabulary — the packaging of an algorithm

The *algorithms* are Chapters 15 and 16 verbatim, in two visible mutations — both about **professional packaging**, and both worth word-by-word ceremony:

| Piece | Meaning |
|---|---|
| `public static class SearchAlgorithms` | A **static class**: cannot be instantiated (no `new SearchAlgorithms()` — a compile error), contains only static members. It is a *named toolbox*: the class exists to group and namespace the algorithms, not to be an object. This is the natural home for pure functions in C#. |
| `public static int LinearSearch(...)` | `public` — visible to `Program` (which lives in another namespace); `static` — callable as `SearchAlgorithms.LinearSearch(...)` with no object (6.2's ceremony, now in its permanent form). |
| `IReadOnlyList<double> values` | The generalization: accept *any* read-only list of doubles — arrays (`double[]`), `List<double>`, lazy LINQ results. The lab's data flows in from the reader as a `List`, and into statistics as arrays — all through this one type. **`.Count`** (not `.Length`): lists report their size via `Count`, arrays via `Length` — the interface's uniform word. |
| `sortedValues` | **The precondition, encoded in the name.** The parameter is *named* "sorted" because it *must be* sorted — binary search's contract (12.4, 16.6) carried into an identifier. Naming is documentation that cannot go stale. |

The line-by-line of the bodies was performed at 15.3 and 16.3 — re-derive them as an exercise before reading back: the guard-trace-proof discipline (Chapter 12) applied to code you did not just write is precisely what code review is.

## 49.3 Doubles and exact equality — a professional warning

The lab searches for `values[0]` (52) — a value read from the *same* file, parsed by the *same* rules, landing on the exact same bits. Equality of doubles that traveled together is safe. But `BinarySearch(data, 0.1 + 0.2)` on data containing `0.3` fails: `0.1 + 0.2 == 0.30000000000000004` in binary floating point (57.5). **Rule: exact `==` on computed floating-point values is a latent bug; on round-tripped identical values it is fine.** State which situation you are in — 56's bug list includes this one by name.

---
# Chapter 50: The Sort Algorithms File

## 50.1 Create `Algorithms/SortAlgorithms.cs`

```csharp
namespace AlgorithmLab.Algorithms;

public static class SortAlgorithms
{
    public static double[] MergeSort(IReadOnlyList<double> values)
    {
        if (values.Count <= 1)
        {
            return values.ToArray();
        }

        int middle = values.Count / 2;
        double[] left = values.Take(middle).ToArray();
        double[] right = values.Skip(middle).ToArray();

        double[] sortedLeft = MergeSort(left);
        double[] sortedRight = MergeSort(right);

        return Merge(sortedLeft, sortedRight);
    }

    private static double[] Merge(
        IReadOnlyList<double> left,
        IReadOnlyList<double> right)
    {
        double[] result = new double[left.Count + right.Count];
        int leftIndex = 0;
        int rightIndex = 0;
        int resultIndex = 0;

        while (leftIndex < left.Count && rightIndex < right.Count)
        {
            if (left[leftIndex] <= right[rightIndex])
            {
                result[resultIndex++] = left[leftIndex++];
            }
            else
            {
                result[resultIndex++] = right[rightIndex++];
            }
        }

        while (leftIndex < left.Count)
        {
            result[resultIndex++] = left[leftIndex++];
        }

        while (rightIndex < right.Count)
        {
            result[resultIndex++] = right[rightIndex++];
        }

        return result;
    }
}
```

## 50.2 Line by line — the packaging and the new pieces

The algorithm is Chapter 21's, generalized from `int[]` to `IReadOnlyList<double>` and re-expressed with LINQ's splitting tools:

| Piece | What it does |
|---|---|
| `public static double[] MergeSort(IReadOnlyList<double> values)` | Takes *any* readable list; returns a **new sorted array** (`double[]`) — the caller's original order is *never* mutated: a pure function (46.2's architecture law). Contrast with `Array.Sort` (23.2), which reorders in place — both are legitimate; the pure form is the testable form. |
| `if (values.Count <= 1) return values.ToArray();` | Base case — generalized: *convert to an array* (`.ToArray()`) so the return type is uniformly `double[]` whether the input was a `List`, an array, or a LINQ view. Even the trivial case respects the type contract. |
| `values.Take(middle).ToArray()` | **LINQ `Take(k)`** — "the first k elements", as a lazy sequence; `.ToArray()` materializes it into the left half. The replacement for `numbers[..middle]`, working on *any* `IReadOnlyList` rather than arrays only. |
| `values.Skip(middle).ToArray()` | **LINQ `Skip(k)`** — "everything after the first k" — the right half. `Take` + `Skip` at the same cut point are disjoint and complete: the two halves concatenate back to the whole. |
| `private static double[] Merge(...)` | **`private`** — the crucial packaging word: visible *only inside `SortAlgorithms`*. `Merge` is an implementation detail (it requires *sorted* inputs to mean anything — a precondition no outsider should be trusted to satisfy); keeping it private **communicates and enforces** that boundary. Public surface: one method, `MergeSort`. That is API design in miniature. |

The `Merge` body is 21.5's line-by-line verbatim (three fingers, the `<=` stability choice, the dense `result[resultIndex++] = left[leftIndex++]` double post-increment, the two drains). Re-derive its trace on `{5, 2, 8, 1}` (21.6) before looking back — the recursion tree picture is unchanged by the element type.

**Complexity, carried over:** O(n log n) time on every input (21.7's log-tall, n-wide tree); O(n) space for the merge outputs. The lab's dataset sizes make this instant — the choice of merge sort over `Array.Sort` is *pedagogical* (we build what we use), documented as such, with 58's capstone inviting you to benchmark both (Chapter 55's method).

---

# Chapter 51: The Statistics Algorithms File

## 51.1 Create `Algorithms/StatisticsAlgorithms.cs`

```csharp
namespace AlgorithmLab.Algorithms;

public static class StatisticsAlgorithms
{
    public static double Mean(IReadOnlyList<double> values)
    {
        RequireValues(values);
        return values.Sum() / values.Count;
    }

    public static double Median(IReadOnlyList<double> values)
    {
        RequireValues(values);
        double[] sorted = SortAlgorithms.MergeSort(values);
        int middle = sorted.Length / 2;

        if (sorted.Length % 2 == 1)
        {
            return sorted[middle];
        }

        return (sorted[middle - 1] + sorted[middle]) / 2.0;
    }

    public static double StandardDeviation(IReadOnlyList<double> values)
    {
        RequireValues(values);
        double average = Mean(values);
        double total = 0;

        foreach (double value in values)
        {
            double difference = value - average;
            total += difference * difference;
        }

        return Math.Sqrt(total / values.Count);
    }

    public static IReadOnlyList<double> FindOutliers(
        IReadOnlyList<double> values)
    {
        RequireValues(values);
        double[] sorted = SortAlgorithms.MergeSort(values);
        double firstQuartile = Percentile(sorted, 0.25);
        double thirdQuartile = Percentile(sorted, 0.75);
        double spread = thirdQuartile - firstQuartile;
        double lower = firstQuartile - 1.5 * spread;
        double upper = thirdQuartile + 1.5 * spread;

        return values
            .Where(value => value < lower || value > upper)
            .ToArray();
    }

    private static double Percentile(
        IReadOnlyList<double> sortedValues,
        double fraction)
    {
        double position = (sortedValues.Count - 1) * fraction;
        int lower = (int)Math.Floor(position);
        int upper = (int)Math.Ceiling(position);

        if (lower == upper)
        {
            return sortedValues[lower];
        }

        double weight = position - lower;
        return sortedValues[lower]
               + (sortedValues[upper] - sortedValues[lower]) * weight;
    }

    private static void RequireValues(IReadOnlyList<double> values)
    {
        if (values.Count == 0)
        {
            throw new ArgumentException("At least one value is required.");
        }
    }
}
```

## 51.2 Line by line — and the design decisions speaking

**`Mean`** — Chapter 45.2's algorithm, compressed to the professional two lines:

| Piece | What it does |
|---|---|
| `RequireValues(values);` | The guard, extracted (below) — one line, same contract. |
| `values.Sum()` | A LINQ extension method: the summation loop (45.2's `foreach`) pre-built, one word. O(n), reads naturally as the math it performs. |

**`Median`** — 45.2's, powered by *our own* sort:

| Piece | What it does |
|---|---|
| `double[] sorted = SortAlgorithms.MergeSort(values);` | **The lab's modules composing**: statistics reaches into the sort toolbox — a pure call to a pure function, our own machinery running our own machinery. The sorted copy is *fresh* — the caller's input order is untouched (the "sorts a copy, not the caller's collection" design decision). |
| the parity branch | Odd → the exact middle; even → the two middles averaged — with the load-bearing `/ 2.0` (45.2's integer-division trap, deliberately avoided). |

**`StandardDeviation`** — 45.3's two-pass population formula verbatim: pass 1 `Mean`, pass 2 squared deviations, divide by n, `Math.Sqrt`. The population-vs-sample choice (45.3's mandate) is *made here in the denominator* and *stated in the report's label* (52).

**`FindOutliers`** — 45.5's fences, operationalized:

| Piece | What it does |
|---|---|
| `Percentile(sorted, 0.25)` / `(sorted, 0.75)` | Q1 and Q3 from the sorted copy — quartiles are *positional*, like the median: sort first, then read ranks. |
| `spread`, `lower`, `upper` | The IQR arithmetic — 45.5's formulas, transcribed. |
| `values.Where(value => value < lower \|\| value > upper).ToArray()` | **LINQ `Where`** — the *filter*: keep elements satisfying the predicate; the lambda `value => ...` states the fence test per element. Returns a lazy sequence; `.ToArray()` materializes. Note it filters the **original** (unsorted) values — the outliers you report should be *the actual data points in original order*, not their sorted positions: a small correctness-of-presentation decision. |

**`Percentile`** — the quartile engine, line by line (the file's most intricate method):

| Piece | What it does |
|---|---|
| `double position = (Count - 1) * fraction;` | The fractional rank: where the percentile *falls* among indexes 0..n−1. The `− 1` is the convention's calibration — for n = 9, the median (0.5) lands at (9−1)·0.5 = 4.0: *exactly* the middle index. Check it: the median of 9 elements is the 5th, index 4. ✓ |
| `int lower = (int)Math.Floor(position);` `int upper = (int)Math.Ceiling(position);` | The two integers the position lies between (Floor rounds down, Ceiling rounds up). |
| `if (lower == upper) return sortedValues[lower];` | The position *is* an integer — no interpolation needed; the exact element is the answer. |
| `double weight = position - lower;` | How far between the two neighbors we sit (0..1). |
| `sortedValues[lower] + (sortedValues[upper] - sortedValues[lower]) * weight;` | **Linear interpolation**: start at the lower value, add the fraction `weight` of the gap to the upper value. Position 1.5 between values 10 and 20 → 10 + (20−10)·0.5 = 15. The percentile is *between data points* when the rank falls between indexes — this is the standard "linear" convention (others exist — numpy calls this `linear` method; document which convention your numbers use). |

**Trace, sorted `{1, 2, 3, 4, 5, 6, 7, 8, 100}` (n=9), Q1 = 0.25:** position = 8·0.25 = **2.0** → lower == upper == 2 → Q1 = sorted[2] = 3. Q3 = 8·0.75 = **6.0** → Q3 = sorted[6] = 7. IQR = 4; fences −3 and 13; 100 > 13 → flagged. (45's exercise, reproduced by the machinery.)

**`RequireValues`** — the extracted guard:

| Piece | What it does |
|---|---|
| `private static void RequireValues(...)` | A named precondition: every public method opens with the same line — the empty-input refusal (12.3) written **once** and *called* everywhere. Repetition of a safety rule across methods is a design smell; extraction is the cure. `private` — an implementation detail of this toolbox. |

**The design decisions, gathered** (the original guide's list, expanded — these are what a code reviewer would *commend*):

1. **All public calculations reject empty input** — one guard, uniformly applied.
2. **Median and outliers sort a copy** — the caller's collection is never reordered through a statistics call.
3. **The standard deviation is explicitly population** — chosen, labeled, documented.
4. **Percentile interpolation is a separate private algorithm** — one subtle idea isolated, testable (54), reusable.
5. **The report can explain the assumptions used** — because every assumption above is *visible in code*, not buried in formulas.

---

# Chapter 52: The Program Entry Point

## 52.1 Replace `Program.cs`

```csharp
using AlgorithmLab.Algorithms;
using AlgorithmLab.Services;

namespace AlgorithmLab;

public static class Program
{
    public static void Main(string[] args)
    {
        string path = args.Length > 0 ? args[0] : "data.csv";
        CsvNumberReader reader = new();

        try
        {
            IReadOnlyList<double> values = reader.Read(path);

            if (values.Count == 0)
            {
                Console.WriteLine("No valid numeric values were found.");
                return;
            }

            double[] sorted = SortAlgorithms.MergeSort(values);
            int searchIndex = SearchAlgorithms.BinarySearch(sorted, values[0]);
            IReadOnlyList<double> outliers =
                StatisticsAlgorithms.FindOutliers(values);

            Console.WriteLine("=== Algorithm Lab Report ===");
            Console.WriteLine($"Source: {path}");
            Console.WriteLine($"Count: {values.Count}");
            Console.WriteLine($"Minimum: {sorted[0]:F2}");
            Console.WriteLine($"Maximum: {sorted[^1]:F2}");
            Console.WriteLine($"Mean: {StatisticsAlgorithms.Mean(values):F2}");
            Console.WriteLine($"Median: {StatisticsAlgorithms.Median(values):F2}");
            Console.WriteLine(
                $"Population standard deviation: " +
                $"{StatisticsAlgorithms.StandardDeviation(values):F2}");
            Console.WriteLine($"First value found at sorted index: {searchIndex}");
            Console.WriteLine(
                $"Potential outliers: {string.Join(", ", outliers)}");
        }
        catch (FileNotFoundException error)
        {
            Console.WriteLine(error.Message);
        }
        catch (ArgumentException error)
        {
            Console.WriteLine($"Invalid data: {error.Message}");
        }
    }
}
```

## 52.2 Line by line — the composition, word by word

| # | Piece | What it does |
|---|---|---|
| 1 | `using AlgorithmLab.Algorithms;` `using AlgorithmLab.Services;` | **Import the namespaces** (46.2): the toolbox and the reader become visible by short name — `SortAlgorithms`, `CsvNumberReader`. The `using` statement *is* the wiring diagram of the composition. |
| 2 | `namespace AlgorithmLab;` | The root namespace — `Program` lives at the project's top level. |
| 3 | `public static class Program` | Static: the program needs no `Program` *object* — it is a pure composition script. |
| 4 | `public static void Main(string[] args)` | **The entry point** — the method the runtime calls to start the application (5.4's chain, at its end). `args` = the command-line arguments, one string each; `void` — the program's value is its *effect* (the report), not a returned answer. |
| 5 | `string path = args.Length > 0 ? args[0] : "data.csv";` | **The ternary** (35.3): first argument if provided, otherwise the documented default `data.csv` — a *usable* program with zero arguments, a parameterized one with one. |
| 6 | `CsvNumberReader reader = new();` | Construct the service (one instance, stateless — 48). |
| 7 | `try { ... }` | **Exception handling, opened**: the guarded region — everything that touches the outside world (file) or refuses bad input (guards) lives inside; failures become `catch`-able events instead of crashes. |
| 8 | `IReadOnlyList<double> values = reader.Read(path);` | Acquisition + validation + cleaning — the reader's whole pipeline (48.3), one call. |
| 9 | `if (values.Count == 0) { ...; return; }` | The empty-file edge case (46.3's decision): a clear message and a clean stop — *before* any statistic throws its guard. Early exit (7.5) as flow design. |
| 10 | `double[] sorted = SortAlgorithms.MergeSort(values);` | Our merge sort, on our data — a fresh sorted array, the original order preserved. |
| 11 | `int searchIndex = SearchAlgorithms.BinarySearch(sorted, values[0]);` | The search demonstration: find where the *first input value* landed in sorted order — binary search on the sorted copy (its precondition satisfied *by construction* — the packaging of 49.2 paying off). Note the double-equality safety: `values[0]` round-tripped through the same file and parser (49.3). |
| 12 | `StatisticsAlgorithms.FindOutliers(values)` | The fences, computed on the original order. |
| 13 | `Console.WriteLine($"Source: {path}");` | **Interpolated strings**, word by word: the `$` prefix turns `"..."` into a template; `{expression}` *embeds the expression's value* at that spot — `$"Count: {values.Count}"` prints `Count: 9`. Readability without concatenation noise. |
| 14 | `$"Minimum: {sorted[0]:F2}"` | **Format specifier inside interpolation**: `:F2` = "fixed-point, 2 decimals" — `13.8`, `100.00`. The report's precision is a *presentation* decision, made at the presentation site — the stored doubles keep full precision. |
| 15 | `$"Maximum: {sorted[^1]:F2}"` | **The index-from-end operator**: `sorted[^1]` is the *last* element (`^1` = "1 from the end"; `^0` would be one-past-the-end — invalid, correctly so). The maximum of a sorted array in one character. |
| 16 | `string.Join(", ", outliers)` | 7.6's helper: the outliers woven into one readable line — `100`. |
| 17 | `catch (FileNotFoundException error)` | **Catch 1 — the missing file**: the reader's loud refusal (48.2), received here at the composition boundary and converted into a human message. This is the architecture's whole point: *the throw happened in the service; the explanation happens in the program*. |
| 18 | `catch (ArgumentException error)` | **Catch 2 — the guards**: any `RequireValues` refusal (51.2) lands here as "Invalid data: ...". Both catches print `error.Message` — the exception's human sentence — and the program ends normally. |

## 52.3 The composition, seen whole

```text
       Program (composition)
       ├── CsvNumberReader.Read          (Services: the world)
       ├── SortAlgorithms.MergeSort      (Algorithms: pure)
       ├── SearchAlgorithms.BinarySearch (Algorithms: pure, precondition by construction)
       ├── StatisticsAlgorithms.*        (Algorithms: pure, guarded)
       └── Console.WriteLine             (output — also the world, quarantined by convention)
```

Every arrow is a namespace `using`; every box is one file; every responsibility has one home. *This diagram is the transferable product of the Lab* — more than the statistics, it is the architecture you will rebuild in every language for the rest of your career.

---

# Chapter 53: Data Running and Manual Testing

## 53.1 Create `data.csv`

```text
12.5,14.0,13.2,15.8,11.4,12.9,14.7,100.0,13.8
```

Nine values — eight clustered in the 11–16 range and one deliberate outlier (100.0): a dataset *designed* to exercise the IQR fence (45.5's trace values: mean 23.14..., the outlier flagged).

## 53.2 Run it

```bash
dotnet run
```

Expected report (verify each number by hand — the *by hand* is the point):

```text
=== Algorithm Lab Report ===
Source: data.csv
Count: 9
Minimum: 11.40
Maximum: 100.00
Mean: 23.14
Median: 13.80
Population standard deviation: 27.16
First value found at sorted index: 1
Potential outliers: 100
```

Cross-check every number by hand — the *by hand* is the point. Sorted order is `{11.4, 12.5, 12.9, 13.2, 13.8, 14.0, 14.7, 15.8, 100.0}`: the median (index 4) is 13.8 ✓; the fences flag only 100 ✓ (45.5's trace values).

**The search line deserves a genuine trace** (16.4's discipline, applied): `values[0]` is 12.5 — where does binary search land? `low=0, high=8` → `middle = 4` → `sorted[4] = 13.8 > 12.5` → `high = 3` → `middle = 1` → `sorted[1] = 12.5` — match → **return 1**. Two iterations, provably index 1 — not "somewhere near the middle by feel". Predict search results with the halving table, never by intuition: when prediction and output disagree, one of them is wrong, and either way you just learned something — *that exact disagreement is what manual testing is for* (53.4's ritual).

## 53.3 Passing another file

```bash
dotnet run -- another-data.csv
```

The `--` separates `dotnet`'s own options from **the program's arguments** — everything after it lands in `Main`'s `args` array. With `args[0] = "another-data.csv"`, the ternary of 52.2 line 5 routes to your file.

## 53.4 The manual test plan — ten cases, predicted *before* running

46.3 promised edge cases *decided in advance*; here is the plan, with expected outcomes — write your prediction for each *before* running, per Chapter 1.2's ritual:

| # | Test | Expected |
|---:|---|---|
| 1 | normal data, several values | the full report, all fields |
| 2 | **one value** (`42`) | Count 1; Min = Max = Mean = Median = 42; stdev **0.00** (no spread); outliers empty — the fences collapse onto the single value |
| 3 | **empty file** | "No valid numeric values were found." — the guard flow of 52.2 line 9 |
| 4 | **missing file** | the `FileNotFoundException` message — catch 1 |
| 5 | invalid cells mixed with valid (`"12.5, oops, 14"`) | tolerated: Count 2 — the documented skip policy (48.2) |
| 6 | negative values (`"-5, -10, -3"`) | Min −10; outliers: *none flagged* — fences at Q1−1.5·IQR = −10 exactly... compute it: sorted {−10, −5, −3}, Q1 −10, Q3 −3... position 8? n=3: Q1 at (3−1)·.25 = 0.5 → interpolate (−10 + (−5−(−10))·0.5) = −7.5; Q3 at 1.5 → −4; IQR 3.5; fences −12.75, 1.25 → none outside. **All inside — correct!** |
| 7 | duplicate values (`"7, 7, 7"`) | Count 3; Min = Max = Mean = Median = 7; stdev 0; BinarySearch returns *some* index of 7 — with all-equal values, any of 0..2 is a correct answer (17.1's ambiguity, in the flesh) |
| 8 | a very large value among small ones | the `100.0` story: flagged as outlier |
| 9 | values already sorted | identical report to the shuffled version — *order-independence* of every statistic (a property worth *testing*, 54.3) |
| 10 | values in reverse order | identical report again — same property, other direction |

Cases 6 and 10 are the quiet professionals: they verify *properties* (fence behavior on negatives; order-independence) rather than single numbers — the bridge to Chapter 54's property-based thinking.

For each test, **write the expected output before running the program**. The discipline — not the checkmarks — is the training: prediction is where the mental model gets audited (53.2's puzzle just demonstrated the method's value on purpose).

---
# Part XVIII — Testing Benchmarking and Debugging

Code that has not been tested is a hypothesis; code that has not been measured is an opinion; code that cannot be debugged is a liability. This part is the professional shell around everything you built.

---

# Chapter 54: Testing Algorithm Contracts

## 54.1 Test the contract, not the implementation

An algorithm's tests should mirror its **contract** (9.3) — every clause becomes cases:

For `BinarySearch`, the contract yields this table *mechanically*:

| Contract clause | Test |
|---|---|
| "returns the index of the target if present" | target in the middle → its index |
| "if present" — anywhere | target at the **first** position; target at the **last** position |
| "otherwise −1" | an absent target |
| "array" edge | **empty array** → −1; **one-item array** (present and absent) |
| "sorted input with duplicates" — ambiguity | duplicates present → *some* valid index (17.1: assert membership, not a specific index) |
| precondition documented | unsorted input → *documented undefined*; the test asserts the precondition is *stated*, not a specific result |

The last row is subtle and professional: you do not test that unsorted input "works" — you test that the *contract says it must be sorted*. Tests enforce promises; they do not grant new ones.

## 54.2 Unit tests with xUnit

Create a test project beside the algorithm project:

```bash
dotnet new xunit -n AlgorithmLab.Tests
cd AlgorithmLab.Tests
dotnet add reference ../AlgorithmLab/AlgorithmLab.csproj
```

Word by word: `dotnet new xunit` — a project from the **xUnit** template (xUnit = a test *framework*: it discovers your test methods, runs them, and reports pass/fail); `dotnet add reference ...` — wire the test project to the code under test (a *project reference*: the tests can `using AlgorithmLab.Algorithms` now).

```csharp
using AlgorithmLab.Algorithms;
using Xunit;

public class BinarySearchTests
{
    [Fact]
    public void BinarySearch_FindsTheTarget()
    {
        int[] values = { 1, 3, 5, 7, 9 };

        int index = SearchAlgorithms.BinarySearch(values, 7);

        Assert.Equal(3, index);
    }

    [Fact]
    public void BinarySearch_ReturnsMinusOneWhenMissing()
    {
        int[] values = { 1, 3, 5, 7, 9 };

        int index = SearchAlgorithms.BinarySearch(values, 8);

        Assert.Equal(-1, index);
    }
}
```

Word by word — the anatomy of a unit test (three beats: **arrange, act, assert**):

| Piece | What it does |
|---|---|
| `[Fact]` | An **attribute** (bracketed metadata on the method): xUnit's marker — "this method is a test; discover and run it." Without it, the method is just a method. |
| `public void BinarySearch_FindsTheTarget()` | One *fact* about the contract, named as a sentence. `void` — the test's value is the assertion inside, not a return. |
| arrange: `int[] values = { 1, 3, 5, 7, 9 };` | The **input** — smallest input that exercises the clause. |
| act: `int index = SearchAlgorithms.BinarySearch(values, 7);` | The **one behavior under test** — a single call. |
| `Assert.Equal(3, index);` | The **assertion**: expected first, actual second. xUnit compares and reports failure with both values if they differ. One assertion per fact keeps failures *diagnostic* — the name tells you which promise broke. |

Run with `dotnet test` — the framework compiles, discovers every `[Fact]`, runs each, and prints a pass/fail summary. **Every algorithm in the Lab deserves its own facts**: guard behavior (empty input throws — `Assert.Throws<ArgumentException>(() => ...)`), median parity (odd/even cases of 45.2), percentile interpolation, outlier fences — the contracts of Part XVII are a ready-made test plan.

## 54.3 Property-based thinking — test the laws, not just the examples

Some results satisfy **general properties** true for *every* input — stronger than any example table:

- a sorted output is **never smaller than its next item** — pairwise, across the whole array;
- sorting **preserves the multiset** of values — same counts before and after (14.4's histogram, as an oracle);
- the **mean of identical values equals that value** — a fixed point of the formula;
- a **palindrome reads the same reversed** — by definition, for any input claiming palindromicity;
- **order-independence of statistics** — Lab case 9/10 of 53.4: shuffled input, identical report.

Even without a property-testing library, *write tests around these properties*: generate 100 random inputs, assert the law for each. One property test replaces a thousand example tests — and catches the example you forgot to write. (The style generalizes into *metamorphic testing* — shuffle in, assert equal out; scale values, assert mean scales — the properties become your imagination's checklist.)

## 54.4 What tests cannot do

Testing runs *selected* inputs (12.5's table) — it can miss the input you never imagined, and it cannot certify correctness the way an invariant proof can. The mature position: **proof for the reasoning, properties for the laws, examples for the contract, and all three in the repository.**

---

# Chapter 55: Benchmarking Fairly

## 55.1 Why measure — and why measurement is hard

Complexity analysis (Chapter 13) predicts *growth*; benchmarking measures *reality* — including the constants, allocations, and cache behaviors that Big-O deliberately ignores. But the runtime is a hostile laboratory: JIT compilation warms up, garbage collection pauses, CPUs boost and throttle, and the operating system multitasks. A naive stopwatch measures all of that noise *plus* your algorithm. Fair benchmarking is noise control:

- **use the same input values** for both contenders — identical data, identical order;
- **test multiple input sizes** — n = 10, 100, 1_000, 10_000: the crossover *is* the answer (below);
- **include favorable and unfavorable orders** — sorted, reversed, shuffled, adversarial (insertion sort's O(n) vs O(n²) spread is the canonical demonstration);
- **warm up the runtime** before timing — the first executions include JIT compilation; measure steady state;
- **avoid measuring file I/O** when comparing sorts — read once, into memory, *then* time;
- **repeat measurements** — several runs, report median/min; a single run is an anecdote;
- **distinguish elapsed time from allocated memory** — GC pressure is a *second cost axis*: an algorithm can win time and lose memory (merge vs quick sorts the canonical case); measure both (`GC.GetAllocatedBytesForCurrentThread()` or a real profiler).

## 55.2 The canonical experiment — insertion sort vs merge sort

The experiment every engineer should run once (58's capstone item 3):

```text
question: at what input size does merge sort become faster
          than insertion sort for this workload?

sizes:   10     50     100    500    1_000   10_000
insert:  ~fast  fast   ~even  slower slower  much slower
merge:   slower slower ~even  faster faster  much faster
                   ↑ the crossover — typically somewhere around n ≈ 30–100
```

The physics behind the crossover: insertion sort does ~n²/4 comparisons *but at tiny constants* (one array read, one compare, one write per step — cache-friendly, allocation-free); merge sort does ~n log n comparisons *at larger constants* (two sub-arrays, copying, allocation). For small n the constants dominate; for large n the exponents do. **There is no paradox — there is a crossover**, and its location is a property of your machine and workload, which is why you measure *yours* rather than citing someone else's.

## 55.3 What a benchmark must answer

A benchmark without a question is a demo. State the question first, in one sentence, with numbers in it:

> "At what input size does merge sort become faster than insertion sort for this workload?"
> "Does the hash-set duplicate check stay under 100 ms at 10 million records?"
> "How much extra memory does the top-K heap use at n = 10⁸, k = 100?"

Then the design falls out: vary the input size (Q1), the one dimension (Q2), both cost axes (Q3). For serious work, use **BenchmarkDotNet** — the .NET benchmarking library that automates warm-up, repetition, and statistical reporting (the professional tool; hand-rolled timing is for learning *why* those protections exist).

> Complexity analysis tells you *which experiments are worth running*. Benchmarking tells you *what actually happens on this machine*. Neither substitutes for the other — 13.8's sequence, closed.

---

# Chapter 56: Debugging and Common Bugs

## 56.1 Traces — watch the algorithm think

The core technique, old as computing: **print the state at each meaningful phase** and read what the algorithm actually did:

```csharp
Console.WriteLine(string.Join(", ", numbers));   // 7.6's helper — keep it forever
```

- **sorting** — print the array after each outer round: watch the sorted prefix grow (selection) or the shifts land (insertion);
- **recursion** — print the current range *and an indentation level*: the recursion tree of 21.6/30.4 drawn live by the program itself. Add one `string indent = new string(' ', depth * 2);` parameter through the calls;
- **searching** — print `low`, `high`, `middle` per iteration: the halving table of 16.4, generated;
- **graphs** — print the queue/stack and the visited set per step: 38.3/39.3's tables, live.

The goal is to **observe state transitions** — not to print everything forever. Traces are scaffolding: add them to *understand*, remove them (or gate them behind a debug flag) to *ship*.

## 56.2 The bug catalog — know them by name

Every bug below has appeared somewhere in this guide's warnings; here is the wanted poster wall:

| Bug | Looks like | The cure (chapter) |
|---|---|---|
| **off-by-one indexes** | `IndexOutOfRangeException`; "the last element is never processed" | `<` vs `<=`; indexes run 0..Length−1; test first/last explicitly (6.3, 7.2) |
| **forgotten empty input** | crash on first empty file in production | guard clauses first; empty case in every test table (1.3, 12.3, 53.4) |
| **binary search on unsorted data** | confidently returns −1 for present values | precondition in name+docs+tests (12.4, 49.2) |
| **infinite loop** (pointer never moves) | 100% CPU, no output | every loop body must shrink the range: `low = middle + 1`, not `middle` (16.8) |
| **modifying a collection while enumerating it** | `InvalidOperationException` mid-foreach | collect removals, apply after; or index-based loops (53's discipline) |
| **integer division when decimals needed** | ` Median` returns 4 instead of 4.5 | `/ 2.0` — the `.0` is load-bearing (45.2, 51.2) |
| **exact float equality** | `0.1 + 0.2 != 0.3` | tolerance comparisons; round-tripped values are safe (49.3, 57.5) |
| **forgetting to mark graph nodes visited** | infinite wandering in cycles | mark-early fused test-and-add (38.3) |
| **returning an internal mutable collection** | caller edits your internals; state corrupts | return copies / read-only views (31.3, 47.2) |
| **best case confused with worst case** | "it's O(n)!" — on sorted data | state the case (13.6); test both orders (55.1) |

## 56.3 The debugging method — five moves

1. **Reproduce** — the smallest input that fails (53's cases become your minimal reproducers).
2. **Predict** — write what you *expect* the output to be (1.2's ritual — the prediction gap localizes the surprise).
3. **Trace** — 56.1's prints, at the phase where prediction and reality diverge.
4. **Bisect the pipeline** — with the Lab's architecture (46.2), check each stage's output: reader → sorted array → statistics → report; the first wrong stage is the crime scene (44.5's contract debugging).
5. **Fix the cause, not the symptom** — the trace tells you *why*; change the reasoning, not the output ("add a +1 until it prints right" is how bugs have grandchildren).

The meta-skill: a bug report that says *"the median of 2 values returns the smaller one"* plus a five-line reproducer is engineering; "the stats are wrong sometimes" is astrology.

### Exercises for Part XVIII

1. Write the missing `[Fact]`s for `BinarySearch`: first position, last position, empty array.
2. Design (in two sentences) a property test for `MergeSort` using 54.3's multiset law.
3. Your benchmark shows algorithm A "winning" at n = 10 and you ship it for n = 10⁷ workloads. Name two distinct mistakes.

<details><summary>Solutions</summary>

1. `{1,3,5}` target 1 → `Assert.Equal(0, ...)`; target 5 → `Assert.Equal(2, ...)`; `Array.Empty<int>()` target 1 → `Assert.Equal(-1, ...)`.
2. "For 100 random arrays: `MergeSort(input)` contains exactly the same value counts as `input` (build both histograms with 14.4's counter, compare dictionaries), *and* is pairwise non-decreasing." One sentence of law + one of oracle.
3. Mistake 1: measuring only one size — the crossover question (55.2) was never asked, let alone answered; O(n²) at n = 10⁷ is ~10¹⁴ operations. Mistake 2: single-run timing without warm-up/repetition (55.1) — the n = 10 "measurement" is likely JIT noise, not algorithm behavior.
</details>

---
# Part XIX — Advanced Design and Mastery

The final part: the judgment layer that sits above all the machinery — how professionals *choose* among correct solutions, reason about scale and approximation, and turn the whole discipline into a repeatable method.

---

# Chapter 57: Designing for Real Workloads

## 57.1 Choose algorithms by workload — the interrogation

Before "which algorithm?", ask these — the answers usually make the choice for you:

- **How large is the data?** — tens (constants rule, 13.8), millions (asymptotics rule), billions (memory itself becomes the algorithm, 57.3).
- **Is the data static or changing?** — a static array amortizes a sort; a churnning collection needs a structure that reorders incrementally (balanced tree, heap).
- **How many queries will be made?** — one lookup: linear; many: sort/hash/preprocess (14.1's "pay once, query forever", generalized).
- **Is preprocessing allowed?** — prefix sums, indexes, and materialized views are all "yes" answers with price tags attached.
- **Is memory limited?** — the time–space ledger (25.3): every hash table is a memory purchase.
- **Is exactness required?** — see 57.3.
- **Does order matter?** — stability (23.1) and iteration order (25.3) silently shape downstream correctness.
- **Are there concurrency concerns?** — 57.6's whole cautionary section.

## 57.2 Online versus offline algorithms

An **online algorithm** processes data **as it arrives** and cannot assume it will see the future. An **offline algorithm** inspects **all input first**, then produces the result.

| Task | Style | Why |
|---|---|---|
| streaming average | **online** | each new value updates a running total — no memory of past values needed |
| median of all records | **offline** (naively) | the median is *positional*: it wants the whole sorted order (two-heap streaming medians exist — a beautiful exception worth knowing) |
| live alerting | **online** | the alert must fire *now*; data keeps coming |
| complete historical report | **offline** | the data is finished; completeness is affordable |

The Lab's reader (48) chose `ReadAllLines` — an **offline** decision, right for a report generator. The streaming capstone upgrade (58, item 9) converts it to online — and *that* redesign is precisely when you discover which statistics cooperate with streaming (mean: yes — running sum; median: needs the machinery) and which do not. Online/offline is a *data-availability* constraint that reaches all the way into the mathematics.

## 57.3 Exact versus approximate algorithms

For very large data, exact answers may cost too much time *or memory*. **Approximate algorithms trade a controlled amount of accuracy for speed or compactness:**

- **frequency sketches** (Count-Min) — approximate per-item counts in fixed memory;
- **approximate distinct counts** (HyperLogLog) — count a billion unique IDs in a few kilobytes, ±2%;
- **sampling** — measure 10,000 rows, state the confidence, ship tonight.

The professional rule: **if you use an approximation, document its error behavior** — the ±%, the failure modes, the bound. "Approximately 840M ± 1.6%" is engineering; "about 800M" is a guess wearing a suit. (And notice: 45.6's precision-vs-validity law returns here at a higher level — approximation makes the *precision* honest by contract.)

## 57.4 Deterministic versus randomized algorithms

A **deterministic algorithm** follows the same path for the same input — rerunnable, cache-friendly, debuggable. A **randomized algorithm** uses random choices, usually to improve *expected* performance or simplify design — quicksort's random pivot (22.6) defeats the sorted-input adversary by making the worst case *improbable* rather than impossible.

When randomness is involved:

- **record the seed** — a seeded random generator replays identically: reproducible tests, reproducible bug reports;
- **distinguish expected from worst-case performance** — expected O(n log n) with a worst case that is astronomically unlikely (randomized quicksort) versus a *guaranteed* O(n log n) (merge sort) — 57.1's exactness question, applied to *time*;
- **verify the result statistically when appropriate** — for randomized correctness (rare but real: primality testing), repeat the trial and bound the error probability — 57.3's discipline, mirrored.

## 57.5 Numerical stability — when the numbers lie quietly

Data-analysis algorithms must consider how numbers are *represented*:

- **floating-point values are approximations** — `0.1` is not exactly 0.1 in binary; `0.1 + 0.2 == 0.3` is false (49.3);
- **adding many values accumulates error** — a million additions of tiny rounding drift can visibly move a sum; prefer Kahan-style compensated summation or `double`→`decimal` where the domain allows;
- **very large and very small values interact poorly** — adding 1e-9 to 1e9 loses the small term entirely (it is below the big value's representable precision);
- **variance formulas can suffer cancellation** — the tempting *one-pass* formula `E[x²] − E[x]²` computes a small answer as the difference of two enormous sums — catastrophic cancellation; the Lab's *two-pass* form (45.3) is numerically safer at the cost of a second pass: a correctness–performance trade that Big-O cannot even *express*.

Practical rules: for **financial** calculations, use `decimal` (base-10, exact for money-like values — never `double` for currency); for **scientific** calculations, document tolerances and units; for equality on computed floats, compare within a tolerance (`Math.Abs(a − b) < epsilon`) rather than `==`.

## 57.6 Parallelism — the multiplier that bites

A problem is **parallelizable** when independent pieces can be processed simultaneously — merge sort's two halves, a map over chunks, statistics over disjoint partitions. But parallel code introduces:

- **synchronization** — locks and barriers serialize what you hoped to speed up;
- **shared-state hazards** — two threads mutating one accumulator interleave: `count++` is read-add-write, and interleaved reads *lose increments* (the lost-update bug — nondeterministic, load-dependent, thus nearly untestable);
- **scheduling overhead** — thread coordination costs more than small work units repay;
- **ordering questions** — results arrive in completion order, not submission order (a *stability* problem reborn);
- **nondeterministic failures** — the bug that appears one run in a million, under load, in production (the debugging nightmare class).

The professional sequence — measure, then parallelize: **parallelize only after measuring that the sequential version is a bottleneck and that the work is sufficiently large.** Parallelism is a performance tool with correctness costs; like every other trade in this book, it is bought deliberately or not at all.

---

# Chapter 58: The Mastery Path

## 58.1 The algorithm design method — the interview protocol, the daily tool

When a new problem lands — in an interview, a ticket, a design review — run this sequence (it is Chapter 11's eight steps, compressed into their terminal form):

1. **Restate the problem** in your own words.
2. **Ask clarifying questions** — empty cases, ties, ranges, order (9.2's interrogation).
3. **Give a simple brute-force solution** — correctness first, even if slow.
4. **Analyze the brute force's complexity** — know what you are paying.
5. **Identify the bottleneck** — the loop, the scan, the recomputation.
6. **Choose a data structure or pattern to remove that bottleneck** — Parts V–XIV's whole catalog is your palette.
7. **Explain correctness** — the invariant, spoken aloud.
8. **Test with examples and edge cases** — 53's table, on the whiteboard.
9. **State time and space complexity** — both, with the case (13.6).
10. **Discuss alternatives and trade-offs** — the third-best solution mentioned, and why it lost.

Steps 3–6 are the engine: *brute force → bottleneck → pattern*. Almost every "clever" solution in this book is a brute force with exactly one bottleneck removed by exactly one structure: pairs scanned repeatedly (→ hash map, 25.2); range sums recomputed (→ prefix array, 14.1); sorted data searched linearly (→ halving, 16); exponential recomputation (→ memo, 43.2). Mastery is seeing the bottleneck *before* typing the brute force.

## 58.2 Capstone upgrades — the Algorithm Lab's growth path

Implement these **in order** — each is one chapter's lesson applied to the running application:

1. Add a command-line option for choosing linear or binary search (parse `args`; document the choice).
2. Add an insertion-sort implementation and compare it with merge sort (20 → the experiment of 55.2).
3. Report the time spent by each sorting method (`Stopwatch` — with 55.1's fairness rules).
4. Add grouped analysis for multiple CSV columns (45.4's aggregation, generalized).
5. Report invalid cells with line and column numbers (48's tolerance → strictness; the reader's `TryParse` branch becomes a *recorded* rejection).
6. Add minimum, maximum, range, and quartiles to the report (45's statistics; the model grows `init` properties).
7. Add a moving average using a sliding window (14.3, applied to time-ordered data).
8. Add a frequency table for rounded numeric buckets (14.4 + rounding — a histogram).
9. Add a streaming mode that does not load the entire file (57.2's online conversion; `ReadAllLines` → `ReadLines` — a lazy `IEnumerable<string>`).
10. Add unit tests and benchmark tests (54, 55 — the whole Part XVIII).
11. Add a graph module that analyzes relationships in a second file (Part XIII; `A,B` lines → adjacency list).
12. Add a shortest-path demonstration (41.2's Dijkstra, on that graph).
13. Export the report to JSON (serialize the 47 model — the immutable snapshot serializes beautifully).
14. Add a web API around the analysis engine (the Algorithms/ project is *already* the engine — put a controller in front of it; the architecture of 46.2 was designed for this day).

For each upgrade, preserve the original behavior and **add tests before refactoring** — 54's discipline, now as an instinct.

## 58.3 The final checklist

Before calling *any* algorithm complete, for the rest of your career:

- [ ] Did I define the **input contract**?
- [ ] Did I define the **output contract**?
- [ ] Did I state **preconditions**?
- [ ] Did I test **empty input**?
- [ ] Did I test **one item**?
- [ ] Did I test **duplicates**?
- [ ] Did I test **boundary values**?
- [ ] Did I consider **invalid input**?
- [ ] Can I **explain why it is correct** (the invariant)?
- [ ] Can I state **time complexity** (with the case)?
- [ ] Can I state **space complexity**?
- [ ] Is there a **simpler solution**?
- [ ] Is there a **faster solution if the data grows**?
- [ ] Does the chosen **data structure fit the operations**?
- [ ] Did I **measure before optimizing**?
- [ ] Did I **document assumptions**?

Sixteen boxes. The book you have just read exists to make all sixteen checkable — not from memory, but from understanding.

---
# Appendix A: Complexity Reference

| Algorithm or operation | Average time | Worst time | Extra space |
|---|---:|---:|---:|
| Array index access | `O(1)` | `O(1)` | `O(1)` |
| Linear search | `O(n)` | `O(n)` | `O(1)` |
| Binary search | `O(log n)` | `O(log n)` | `O(1)` iterative, `O(log n)` recursive |
| Hash-set / dictionary lookup | `O(1)` expected | `O(n)` possible | `O(n)` |
| Array/list append | `O(1)` amortized | `O(n)` resize | `O(1)` extra |
| Insert at list beginning | `O(n)` | `O(n)` | `O(1)` |
| Selection sort | `O(n²)` | `O(n²)` | `O(1)` |
| Insertion sort | `O(n²)` — `O(n)` on sorted input | `O(n²)` | `O(1)` |
| Merge sort | `O(n log n)` | `O(n log n)` | `O(n)` |
| Quicksort | `O(n log n)` | `O(n²)` | `O(log n)` |
| BST search / insert (balanced) | `O(log n)` | `O(log n)` | — |
| BST search / insert (unbalanced) | `O(n)` | `O(n)` | — |
| Heap insert / remove | `O(log n)` | `O(log n)` | `O(1)` extra |
| Top-K with size-k heap | `O(n log k)` | `O(n log k)` | `O(k)` |
| BFS | `O(V + E)` | `O(V + E)` | `O(V)` |
| DFS | `O(V + E)` | `O(V + E)` | `O(V)` |
| Topological sort (Kahn) | `O(V + E)` | `O(V + E)` | `O(V)` |
| Dijkstra with binary heap | `O((V + E) log V)` | `O((V + E) log V)` | `O(V)` |
| Fibonacci (naive) | `O(φⁿ)` | `O(φⁿ)` | `O(n)` stack |
| Fibonacci (memoized / tabulated) | `O(n)` | `O(n)` | `O(n)` / `O(1)` compressed |
| Coin change DP | `O(amount × coins)` | `O(amount × coins)` | `O(amount)` |
| Prefix-sum build / query | `O(n)` / `O(1)` | `O(n)` / `O(1)` | `O(n)` |
| Two pointers / sliding window | `O(n)` | `O(n)` | `O(1)` |
| Frequency counting | `O(n)` expected | `O(n)` worst | `O(k)` distinct |
| Mean / variance (two-pass) | `O(n)` | `O(n)` | `O(1)` |
| Median (via sort) | `O(n log n)` | `O(n log n)` | `O(n)` copy |
| IQR outlier detection | `O(n log n)` | `O(n log n)` | `O(n)` copy |

These are general descriptions. Real performance depends on implementation, input distribution, hardware, allocations, and constant factors — which is exactly why Chapter 55 exists.

---

# Appendix B: Algorithm Vocabulary

| Term | Meaning |
|---|---|
| Adjacency list | A graph representation storing the neighbors of each vertex |
| Algorithm | A finite, precise procedure for transforming input into output |
| Amortized analysis | Average cost over a sequence of operations |
| Backtracking | Exploring choices and undoing them when a branch fails |
| Base case | The stopping condition of a recursive algorithm |
| Big O | A growth-rate upper-bound notation commonly used for complexity |
| Binary search | Search that repeatedly halves a sorted search space |
| Breadth-first search | Graph traversal that explores by layers using a queue |
| Brute force | Directly trying all candidates or possibilities |
| Complexity | How resource usage grows with input size |
| Counterexample | An input that disproves a proposed algorithm |
| Divide and conquer | Divide, solve smaller parts, combine results |
| Dynamic programming | Reusing results of overlapping subproblems |
| Edge | A connection between graph vertices |
| Exchange argument | Proof technique: swapping a greedy choice into an optimal solution preserves optimality |
| Greedy algorithm | Repeatedly choosing a locally best option |
| Hashing | Mapping a value to a bucket location for fast lookup |
| Heap | A tree (stored in an array) where each parent dominates its children |
| Invariant | A fact that remains true during an algorithm |
| In-order traversal | Left subtree, node, right subtree — sorted order on a BST |
| Linear search | Scanning a sequence element by element |
| Linked list | Nodes chained by references |
| Loop invariant | A statement true before and after each loop iteration |
| Memoization | Caching results of recursive subproblems |
| Minimum spanning tree | Cheapest edge set connecting all vertices of a weighted undirected graph |
| Online algorithm | Processes data without seeing all future input |
| Optimal substructure | Optimal solutions built from optimal sub-solutions |
| Overlapping subproblems | The same smaller problem appearing repeatedly |
| Pivot | The partitioning element in quicksort |
| Postcondition | A condition that must hold after an algorithm finishes |
| Preconditions | Conditions required before an algorithm starts |
| Prefix sum | Array where position k stores the sum of elements before k |
| Priority queue | Structure delivering the highest-priority item next |
| Pruning | Rejecting impossible partial solutions early in a search |
| Recursion | A method solving a problem by calling itself on smaller input |
| Relaxation | Updating a record when a better route is found (Dijkstra, DP) |
| Sentinel | A reserved return value meaning "not found" (e.g. −1) |
| Sifting | The up/down repair moves that restore heap order |
| Sliding window | Maintaining a moving contiguous section of data |
| Space complexity | Growth of additional memory use |
| Stability | A sort preserving relative order of equal-key records |
| Stack overflow | Runtime failure from excessively deep recursion |
| Stable sort | A sort that preserves relative order of equal-key records |
| Tabulation | Filling a dynamic-programming table iteratively |
| Topological order | Dependency-respecting order of a directed acyclic graph |
| Trace | A step-by-step table of algorithm state |
| Two pointers | Using two positions to scan or narrow a sequence |
| Vertex | A node in a graph |
| Worst case | Most expensive valid input behavior |

---

# Appendix C: Practice Roadmap

Solve in order; do not advance a stage until its problems feel routine. Each stage's list maps onto the book's parts.

## Stage 1: Fundamentals — loops and arrays (Part II, V)

1. sum all values;
2. find minimum and maximum;
3. reverse an array;
4. count duplicates;
5. rotate an array;
6. remove duplicates while preserving order;
7. merge two sorted arrays;
8. check whether a string is a palindrome;
9. count words;
10. find the first non-repeating character.

## Stage 2: Core patterns (Parts V–VIII)

1. two-sum;
2. three-sum;
3. maximum fixed-size window;
4. longest substring without repeated characters;
5. range sums with prefix arrays;
6. interval merging;
7. first and last occurrence with binary search;
8. top-k values with a heap;
9. parentheses validation;
10. task scheduling with a priority queue.

## Stage 3: Recursion and trees (Parts X–XII)

1. factorial and Fibonacci;
2. tree traversals;
3. tree height;
4. count tree leaves;
5. generate subsets;
6. generate permutations;
7. solve a maze;
8. construct a balanced tree;
9. find lowest common ancestor;
10. serialize and deserialize a tree.

## Stage 4: Graphs (Part XIII)

1. BFS traversal;
2. DFS traversal;
3. connected components;
4. cycle detection;
5. topological sort;
6. shortest path in an unweighted graph;
7. Dijkstra's algorithm;
8. minimum spanning tree;
9. word ladder;
10. network dependency analysis.

## Stage 5: Dynamic programming (Part XIV)

1. climbing stairs;
2. minimum cost path;
3. coin change;
4. knapsack;
5. longest common subsequence;
6. edit distance;
7. longest increasing subsequence;
8. partition equal subset sum;
9. interval scheduling variants;
10. sequence alignment.

## Stage 6: Data-analysis applications (Parts XVI–XVII)

1. streaming mean;
2. running minimum and maximum;
3. moving average;
4. median and quartiles;
5. frequency and distinct-count analysis;
6. grouped aggregation;
7. duplicate-record detection;
8. outlier detection;
9. anomaly alerts over time;
10. scalable report generation.

---

# Appendix D: C# Quick Glossary

The language constructs used in this guide, one line each — find the full ceremony at the referenced chapter.

| Construct | One-line meaning | First dissected |
|---|---|---|
| `static` | member callable without an object | 6.2 |
| `void` | returns nothing | 6.2 |
| `return` | deliver the answer and stop the method | 6.2 |
| `int`, `double`, `bool`, `char`, `string` | the core types | 6.1 |
| `int[]`, `numbers[i]`, `.Length` | fixed array; positional access; its count | 6.3 |
| `List<T>`, `Dictionary<K,V>`, `HashSet<T>` | growable list; key→value map; uniqueness set | 6.4 |
| `new()` | construct an instance of the declared left-side type | 6.4 |
| `if` / `else` | conditional execution | 7.1 |
| `%` | remainder after division | 7.1 |
| `for` | counted loop (init; condition; update) | 7.2 |
| `foreach` | visit each element once | 7.3 |
| `while` | loop until a condition dies | 7.4 |
| `break` / `continue` / `return` | exits: loop; iteration; method | 7.5 |
| `++` / `--` | increment / decrement by one | 7.2 |
| `&&`, `\|\|` | short-circuit and / or | 20.3 |
| `?:` (ternary) | conditional expression | 35.3 |
| `??` | left if it exists, else right | 35.3 |
| `is` / `is not` | type / null pattern tests | 29.2 |
| `enum-like or` patterns | membership test among constants | 28.2 |
| `out` | parameter the method writes into | 25.2 |
| `sealed` | class closed to inheritance | 29.2 |
| `{ get; }` / `{ get; set; }` / `{ get; init; }` | read-only / read-write / create-then-frozen property | 29.2, 47.2 |
| `class` vs `struct` | reference vs value semantics | 29.2 |
| nullable `T?` | a value/reference *or* `null`, compiler-checked | 29.2 |
| local function | method declared inside a method, sharing its variables | 31.3 |
| tuple `(a, b)` and deconstruction | bundled values, split on arrival | 21.5, 41.2 |
| `(x, y) = (y, x)` | simultaneous tuple swap | 19.3 |
| `arr[..k]`, `arr[k..]`, `arr[^1]` | range slices; index-from-end | 21.3, 52.2 |
| `Take(k)` / `Skip(k)` / `Where` / `Sum` / `OrderBy` | LINQ: first k; after k; filter; total; sort | 50.2, 51.2, 23.2 |
| `$"...{expr:F2}"` | interpolated string with format specifier | 52.2 |
| `const` | compile-time constant | 43.4 |
| `throw` / `try` / `catch` | raise and receive failures | 12.3, 52.2 |
| `nameof(x)` | the argument's name as text, refactor-safe | 14.3 |
| `Math.Max` / `Math.Sqrt` / `Math.Floor` / `Math.Ceiling` | the math toolbox | 11.2, 51.2 |
| `string.Join(sep, items)` | weave a sequence into one string | 7.6 |
| `TryParse`, `NumberStyles`, `InvariantCulture` | safe, locale-independent conversion | 48.2 |
| `[Fact]`, `Assert.Equal` | xUnit test marker and assertion | 54.2 |

---

## Final Message to the Learner

Algorithms are the language of precise problem solving. You do not become strong by memorizing a list of names. You become strong by repeatedly practicing this cycle:

> **Define the problem → create examples → design a simple procedure → prove it → implement it → test it → measure it → improve it responsibly.**

Use C# as your laboratory. Type every implementation in this book — every one. Break each deliberately: swap `<` for `<=`, remove the `+ 1`, feed sorted data to a worst case, delete the guard clause. Watch it fail. Repair it. Compare two approaches on the same data. Explain why one is better for one workload and worse for another.

You began this guide at the sentence *"forget computers for a moment"* — with a kettle and a cup of tea. You end it able to prove a loop invariant, price a hash table's memory against its speed, choose a sort by its stability guarantee, read a recursion tree, and ship a validated, tested, measurable analysis application.

That process — from clear requirements to tested, measured, and explainable solutions — is the path from absolute beginner to algorithmic mastery. Walk it slowly. Walk it repeatedly. And when a new problem lands on your desk, smile: you know exactly which questions to ask first.
