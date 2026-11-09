# Algorithms in C# — From Absolute Beginner to Mastery

> A complete, step-by-step guide to understanding, designing, implementing, analyzing, testing, and improving algorithms in C#.

This guide assumes that you may know little or nothing about algorithms. It starts by defining the subject in plain language, explains why algorithms matter, introduces the historical ideas that shaped computer science, and then builds toward advanced algorithmic thinking.

The examples use **C#** and are written to be read slowly. Important implementations are followed by line-by-line explanations. The final guided project is an **Algorithm Lab** console application that loads numerical data, calculates descriptive statistics, searches and sorts values, detects outliers, and prints a small analytical report.

---

## Table of Contents

1. [How to Use This Guide](#1-how-to-use-this-guide)
2. [Chapter 1 — What an Algorithm Is](#2-chapter-1--what-an-algorithm-is)
3. [Chapter 2 — A Short History of Algorithms](#3-chapter-2--a-short-history-of-algorithms)
4. [Chapter 3 — Why Algorithms Matter](#4-chapter-3--why-algorithms-matter)
5. [Chapter 4 — The C# Tools You Need](#5-chapter-4--the-c-tools-you-need)
6. [Chapter 5 — Describe a Problem Before Coding](#6-chapter-5--describe-a-problem-before-coding)
7. [Chapter 6 — Correctness, Invariants, and Proof](#7-chapter-6--correctness-invariants-and-proof)
8. [Chapter 7 — Measuring Efficiency](#8-chapter-7--measuring-efficiency)
9. [Chapter 8 — Arrays, Strings, and Fundamental Patterns](#9-chapter-8--arrays-strings-and-fundamental-patterns)
10. [Chapter 9 — Searching Algorithms](#10-chapter-9--searching-algorithms)
11. [Chapter 10 — Sorting Algorithms](#11-chapter-10--sorting-algorithms)
12. [Chapter 11 — Hashing, Maps, and Sets](#12-chapter-11--hashing-maps-and-sets)
13. [Chapter 12 — Stacks, Queues, and Linked Lists](#13-chapter-12--stacks-queues-and-linked-lists)
14. [Chapter 13 — Recursion and Backtracking](#14-chapter-13--recursion-and-backtracking)
15. [Chapter 14 — Divide and Conquer](#15-chapter-14--divide-and-conquer)
16. [Chapter 15 — Trees, Heaps, and Priority Queues](#16-chapter-15--trees-heaps-and-priority-queues)
17. [Chapter 16 — Graph Algorithms](#17-chapter-16--graph-algorithms)
18. [Chapter 17 — Greedy Algorithms](#18-chapter-17--greedy-algorithms)
19. [Chapter 18 — Dynamic Programming](#19-chapter-18--dynamic-programming)
20. [Chapter 19 — String and Text Algorithms](#20-chapter-19--string-and-text-algorithms)
21. [Chapter 20 — Algorithms for Data Analysis](#21-chapter-20--algorithms-for-data-analysis)
22. [Chapter 21 — Build the Algorithm Lab](#22-chapter-21--build-the-algorithm-lab)
23. [Chapter 22 — Testing, Benchmarking, and Debugging](#23-chapter-22--testing-benchmarking-and-debugging)
24. [Chapter 23 — Advanced Design and Mastery](#24-chapter-23--advanced-design-and-mastery)
25. [Appendix A — Complexity Reference](#appendix-a--complexity-reference)
26. [Appendix B — Algorithm Vocabulary](#appendix-b--algorithm-vocabulary)
27. [Appendix C — Practice Roadmap](#appendix-c--practice-roadmap)

---

# 1. How to Use This Guide

## 1.1 The correct order of learning

Always follow this order:

1. Understand the problem.
2. Write examples.
3. Define inputs and outputs.
4. Write a simple solution in plain language.
5. Implement the simple solution.
6. Prove or test that it is correct.
7. Measure its performance.
8. Improve it only when improvement is justified.

Do not begin with a famous algorithm just because you have heard its name. First understand the problem that the algorithm solves.

## 1.2 What to do with every code example

For each example:

- read it once without typing;
- predict the output;
- type it yourself;
- run it;
- change the input;
- test an empty input;
- test one item;
- test a duplicate value;
- test the largest or smallest meaningful input;
- explain the algorithm in your own words.

## 1.3 What mastery means

Algorithmic mastery means you can:

- recognize the shape of a problem;
- choose an appropriate data structure;
- express a solution with pseudocode;
- prove why the solution works;
- estimate time and memory usage;
- implement the solution clearly in C#;
- test edge cases;
- compare alternative solutions;
- identify when a simpler algorithm is better;
- explain trade-offs to another developer.

---

# 2. Chapter 1 — What an Algorithm Is

## 2.1 Plain-language definition

An **algorithm** is a finite, ordered, unambiguous procedure that transforms input into a desired output.

Every word matters:

- **Finite**: it eventually stops.
- **Ordered**: the steps have a sequence.
- **Unambiguous**: each step can be interpreted clearly.
- **Procedure**: it describes actions, not only a desired result.
- **Input**: information provided to the procedure.
- **Output**: the result produced by the procedure.

Example: finding the maximum number in a list.

```text
if the list is empty, report that no maximum exists
assume the first number is the maximum
for each remaining number
    if the number is larger than the current maximum
        replace the current maximum
return the current maximum
```

## 2.2 Algorithm versus code

The same algorithm can be written in many languages:

- an algorithm is the idea and sequence of steps;
- C# code is one concrete expression of that idea.

This distinction is powerful. If you understand the algorithm, you can implement it in another language. If you only memorize syntax, you may struggle when the problem changes slightly.

## 2.3 Algorithm versus data structure

A **data structure** organizes data. An **algorithm** performs a process on data.

Examples:

- `List<int>` is a data structure.
- binary search is an algorithm.
- `Dictionary<string, int>` is a data structure.
- counting word frequencies is an algorithmic task using that structure.

The two are connected. A good algorithm often depends on choosing the right data structure.

## 2.4 The five questions for every algorithm

Before implementing any algorithm, answer:

1. What is the input?
2. What is the output?
3. What assumptions are made?
4. How do we know the answer is correct?
5. How much time and memory does it need?

## 2.5 Example: count even numbers

Input: a sequence of integers.

Output: the number of even integers.

Pseudocode:

```text
set count to zero
for each number in the sequence
    if the number has remainder zero when divided by two
        increase count
return count
```

C# implementation:

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

Line by line:

- `static`: this method can be called without an object of its containing class.
- `int`: the method returns a whole number.
- `CountEvenNumbers`: a descriptive method name.
- `int[] numbers`: an array of integers named `numbers`.
- `int count = 0`: the result starts at zero.
- `foreach`: visit each element exactly once.
- `number % 2`: calculate the remainder after division by two.
- `== 0`: an even number has no remainder.
- `count++`: increase the count by one.
- `return count`: send the result back to the caller.

The time complexity is `O(n)` because each of `n` numbers is inspected once. The extra space is `O(1)` because the algorithm uses only a few variables.

---

# 3. Chapter 2 — A Short History of Algorithms

## 3.1 Ancient procedures

Long before electronic computers, mathematics was expressed as repeatable procedures. Euclid's algorithm for finding the greatest common divisor is one of the best-known ancient examples.

The procedure repeatedly replaces a pair of numbers with a smaller pair based on remainders until the remainder becomes zero. The last non-zero remainder is the answer.

## 3.2 The origin of the word algorithm

The word algorithm is associated with the name of Muhammad ibn Musa al-Khwarizmi, a Persian mathematician whose writings described systematic procedures for arithmetic and algebra.

The broad idea is more important than the name: a calculation can be transformed from an intuitive activity into a repeatable method.

## 3.3 Mechanical and theoretical computation

The work of mathematicians and engineers gradually moved computation from hand procedures to machines. Charles Babbage designed general-purpose mechanical computing concepts, and Ada Lovelace described how a machine might follow operations on symbols, not just numbers.

In the twentieth century, formal models of computation asked what can be computed by an effective procedure. The work associated with Alan Turing and others helped define the theoretical boundaries of algorithms.

## 3.4 Algorithms in modern computing

Modern software depends on algorithms everywhere:

- search engines rank results;
- databases use indexes and query planners;
- navigation systems find routes;
- compression algorithms reduce file sizes;
- operating systems schedule work;
- machine-learning systems optimize models;
- data-analysis systems aggregate and summarize information.

The historical lesson is that an algorithm is not tied to one programming language or one era. It is a disciplined way to describe computation.

---

# 4. Chapter 3 — Why Algorithms Matter

## 4.1 Correctness

A program can compile and still be wrong. An algorithm gives you a structure for reasoning about correctness.

For example, if you want to find a duplicate in an array, you must define what “duplicate” means:

- any value appearing at least twice;
- the first repeated value from left to right;
- all repeated values;
- duplicates based on a case-insensitive string comparison.

Different requirements produce different algorithms.

## 4.2 Performance

Two correct algorithms may differ dramatically in speed or memory use.

Searching an unsorted list usually requires checking items one by one. Searching sorted data can use binary search and discard half of the remaining values at each step.

## 4.3 Maintainability

A clever algorithm that nobody can understand may be worse than a simple algorithm that is easy to verify. The best engineering choice balances:

- correctness;
- performance;
- readability;
- memory use;
- development time;
- future change.

## 4.4 Fair and responsible use

Algorithms affect people. A data-analysis or decision algorithm may contain bias, use incomplete data, or produce results that are difficult to explain.

When building real systems, ask:

- What data is being used?
- What data is missing?
- Who could be harmed by an incorrect result?
- Can a person review the decision?
- Can the result be explained and challenged?

Algorithmic skill includes understanding consequences, not only speed.

---

# 5. Chapter 4 — The C# Tools You Need

## 5.1 Create an algorithm project

Install the .NET SDK and verify it:

```bash
dotnet --version
```

Create a console project:

```bash
dotnet new console -n AlgorithmJourney
cd AlgorithmJourney
dotnet run
```

Meaning:

- `dotnet`: the .NET command-line tool.
- `new`: create a project from a template.
- `console`: use the console-application template.
- `-n`: specify a name.
- `AlgorithmJourney`: the project name.
- `cd`: change directory.
- `run`: build and execute the application.

## 5.2 Variables and collections

```csharp
int number = 42;
int[] numbers = { 4, 1, 9, 2 };
List<int> values = new() { 10, 20, 30 };
Dictionary<string, int> counts = new();
HashSet<string> uniqueWords = new();
```

The collection type strongly influences algorithm performance.

## 5.3 The most useful C# loop forms

```csharp
for (int index = 0; index < numbers.Length; index++)
{
    Console.WriteLine(numbers[index]);
}

foreach (int value in numbers)
{
    Console.WriteLine(value);
}

while (condition)
{
    // repeat while condition is true
}
```

## 5.4 A small helper for printing

```csharp
static void PrintArray(int[] numbers)
{
    Console.WriteLine(string.Join(", ", numbers));
}
```

`string.Join` converts the values into one readable line. It is useful for observing algorithm state while debugging.

---

# 6. Chapter 5 — Describe a Problem Before Coding

## 6.1 Requirements are not algorithms

A requirement says what someone wants. An algorithm says how to obtain it.

Requirement:

> “Show the most common product category.”

Questions that must be answered:

- What happens when there are no rows?
- Are category names case-sensitive?
- How are ties handled?
- Can a category be missing?
- Is the data in memory or a database?

## 6.2 Inputs and outputs

Write a contract:

```text
Input: an array of non-negative integers
Output: the largest value
Precondition: the array must contain at least one element
Postcondition: the returned value is greater than or equal to every input value
```

A **precondition** must be true before the algorithm starts. A **postcondition** must be true after it finishes.

## 6.3 Examples and counterexamples

For a function that removes duplicates:

| Input | Expected output |
|---|---|
| `[1, 2, 1, 3]` | `[1, 2, 3]` |
| `[]` | `[]` |
| `[5]` | `[5]` |
| `[2, 2, 2]` | `[2]` |

A counterexample disproves a proposed algorithm. If someone says “the first value is always the maximum,” `[1, 9, 2]` disproves it.

## 6.4 Pseudocode

Pseudocode is not a programming language. It is a bridge between requirements and implementation.

```text
function find first repeated value
    create an empty set called seen
    for each value in the input
        if seen contains value
            return value
        add value to seen
    return no repeated value
```

## 6.5 Draw a small state trace

For input `[4, 2, 4, 7]`:

| Step | Value | Seen before | Decision |
|---:|---:|---|---|
| 1 | 4 | `{}` | add 4 |
| 2 | 2 | `{4}` | add 2 |
| 3 | 4 | `{4, 2}` | found duplicate |

State traces reveal mistakes that are hard to see in code.

---

# 7. Chapter 6 — Correctness, Invariants, and Proof

## 7.1 What correctness means

An algorithm is correct when it produces the required output for every valid input within its stated assumptions.

“Works on my example” is not a proof. It is one test.

## 7.2 Loop invariants

A **loop invariant** is a statement that remains true before and after each iteration.

For maximum search:

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

Invariant:

> Before each iteration, `maximum` is the largest value among the items already examined.

Proof structure:

1. **Initialization**: before the loop, the first item is the largest among the one examined item.
2. **Maintenance**: when a new item is examined, either the old maximum remains larger, or the new item becomes the maximum.
3. **Termination**: after all items are examined, `maximum` is the largest value in the entire array.

## 7.3 Preconditions and postconditions

For binary search:

- precondition: the input array is sorted in ascending order;
- postcondition: return the index of the target if present, otherwise `-1`.

If you omit the precondition, a correct binary-search implementation may appear broken when it receives unsorted data.

## 7.4 Proof versus testing

- **Proof** reasons about all valid inputs.
- **Testing** runs selected inputs.

Both are valuable. Proof can miss a misunderstanding of requirements. Tests can miss unusual cases. Use tests to support your reasoning.

---

# 8. Chapter 7 — Measuring Efficiency

## 8.1 Input size

Let `n` represent the size of the input. For an array, `n` is usually the number of elements. For a string, `n` may be its length. For a graph, you may use `V` for vertices and `E` for edges.

## 8.2 Time complexity

Time complexity describes how the number of operations grows as the input grows.

Examples:

```csharp
// O(1)
int first = numbers[0];

// O(n)
foreach (int number in numbers)
{
    Console.WriteLine(number);
}

// O(n²)
for (int i = 0; i < numbers.Length; i++)
{
    for (int j = 0; j < numbers.Length; j++)
    {
        // compare a pair
    }
}
```

## 8.3 Space complexity

Space complexity measures additional memory used by the algorithm.

This uses `O(1)` extra space:

```csharp
static int Sum(int[] numbers)
{
    int total = 0;

    foreach (int number in numbers)
    {
        total += number;
    }

    return total;
}
```

This uses `O(n)` extra space:

```csharp
static int[] Copy(int[] numbers)
{
    return numbers.ToArray();
}
```

## 8.4 Best, average, and worst case

An algorithm may behave differently depending on the input:

- **best case**: most favorable input;
- **average case**: expected behavior under an input distribution;
- **worst case**: most expensive input.

Always state which case you are discussing.

## 8.5 Big O, Big Theta, and Big Omega

- `O(f(n))` gives an upper-bound style description.
- `Ω(f(n))` gives a lower-bound style description.
- `Θ(f(n))` describes a tight growth rate.

For beginner and practical engineering discussions, Big O is commonly used as a shorthand for growth behavior.

## 8.6 Do not optimize by guessing

A theoretically better algorithm may be slower for tiny inputs because of constants, allocations, or cache behavior. Use:

1. correctness;
2. complexity analysis;
3. measurement with realistic data.

---

# 9. Chapter 8 — Arrays, Strings, and Fundamental Patterns

## 9.1 Prefix sums

A prefix-sum array allows repeated range-sum queries to be answered quickly.

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

Why `end + 1`? `prefix[k]` stores the sum of elements before index `k`. Therefore, the sum from `start` through `end` is the sum before `end + 1` minus the sum before `start`.

Build time is `O(n)`. Each later range query is `O(1)`.

## 9.2 Two pointers

Two pointers move through a sequence from different positions.

Example: determine whether a sorted array contains two values whose sum equals a target.

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

This requires sorted input. If the sum is too small, increasing the left value is the only move that can increase the sum. If the sum is too large, decreasing the right value can reduce it.

## 9.3 Sliding window

A sliding window maintains a changing section of an array or string.

Find the maximum sum of a window of fixed size:

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

The first loop calculates the first window. Each later window adds one new value and removes one old value, so the full algorithm is `O(n)` rather than `O(n * windowSize)`.

## 9.4 Frequency counting

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

This pattern appears in:

- anagram detection;
- word frequencies;
- category counts;
- duplicate detection;
- data profiling.

---

# 10. Chapter 9 — Searching Algorithms

## 10.1 Linear search

Linear search works on any sequence:

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

Complexity: `O(n)` time and `O(1)` extra space.

## 10.2 Binary search

Binary search requires sorted data:

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

Line by line:

- `low` is the first possible index.
- `high` is the last possible index.
- `low <= high` means the search range is not empty.
- `middle` is computed without adding `low + high` directly, avoiding integer overflow in extreme cases.
- If the middle value equals the target, return its index.
- If the middle value is too small, discard the left half including the middle.
- Otherwise discard the right half including the middle.
- If the range becomes empty, the target does not exist.

Complexity: `O(log n)` time and `O(1)` extra space.

## 10.3 First and last occurrence

With duplicates, you may need the first or last position rather than any matching position. Modify binary search so that a match is recorded and the search continues toward the desired side.

Pseudocode for the first occurrence:

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

## 10.4 Search choice

| Situation | Algorithm |
|---|---|
| Unsorted data, one lookup | Linear search |
| Sorted data, repeated lookup | Binary search |
| Repeated key lookup | Dictionary or hash set |
| Prefix or range conditions | Specialized index or tree |

---

# 11. Chapter 10 — Sorting Algorithms

## 11.1 Why sorting helps

Sorting can make later work easier:

- binary search needs ordered data;
- duplicate detection can compare neighbors;
- reports are easier to read;
- merge operations become efficient.

Sorting also costs time and may use additional memory.

## 11.2 Selection sort

Selection sort repeatedly selects the smallest remaining item.

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

Complexity: `O(n²)` time, `O(1)` extra space. It is easy to understand but inefficient for large input.

## 11.3 Insertion sort

Insertion sort builds a sorted prefix one item at a time.

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

Insertion sort is `O(n²)` in the worst case but can be fast for small or nearly sorted data.

## 11.4 Merge sort

Merge sort divides the input, recursively sorts each half, and merges the sorted halves.

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

Complexity: `O(n log n)` time and `O(n)` additional space.

## 11.5 Built-in sorting

For production C# code, prefer a well-tested library sort unless learning or a special requirement makes a custom implementation appropriate:

```csharp
int[] sorted = numbers.OrderBy(value => value).ToArray();
Array.Sort(numbers);
```

Know the algorithmic idea even when you use the library.

## 11.6 Stability

A sorting algorithm is **stable** if equal-key records retain their original relative order. Stability matters when sorting records by multiple criteria.

---

# 12. Chapter 11 — Hashing, Maps, and Sets

## 12.1 The lookup problem

Suppose you must answer thousands of questions:

> “Have we already seen this ID?”

Scanning a list each time may cost `O(n)` per question. A hash-based structure usually gives expected `O(1)` membership lookup.

## 12.2 Duplicate detection

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

`HashSet.Add` returns `false` when the value already exists.

## 12.3 Two-sum with a dictionary

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

Reasoning:

- for current value `x`, the required partner is `target - x`;
- look for the partner among values already seen;
- if it exists, return both indexes;
- otherwise store the current value and continue.

Expected complexity: `O(n)` time and `O(n)` space.

## 12.4 Hashing trade-offs

Hash structures are not free:

- they use additional memory;
- ordering is not the main purpose;
- performance depends on good hashing and equality behavior;
- worst-case behavior can differ from expected behavior.

Use them when fast membership or key lookup is central.

---

# 13. Chapter 12 — Stacks, Queues, and Linked Lists

## 13.1 Stack

A stack is last-in, first-out (LIFO).

```csharp
Stack<string> pages = new();
pages.Push("home");
pages.Push("details");
string lastPage = pages.Pop();
```

Use a stack for:

- undo operations;
- browser history;
- expression evaluation;
- depth-first search;
- matching parentheses.

## 13.2 Queue

A queue is first-in, first-out (FIFO).

```csharp
Queue<string> jobs = new();
jobs.Enqueue("job-1");
jobs.Enqueue("job-2");
string nextJob = jobs.Dequeue();
```

Use a queue for:

- customer service order;
- breadth-first search;
- background work;
- message processing.

## 13.3 Parentheses validation

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

For multiple bracket types such as `()`, `[]`, and `{}`, use a stack to remember the opening bracket that must be closed next.

## 13.4 Linked list idea

A linked list stores nodes connected by references. Each node contains a value and a reference to the next node.

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

Linked lists allow efficient insertion when you already have the correct node, but random access is slow because you must follow links.

In most everyday C# application code, `List<T>` is often a better default. Learn linked lists to understand algorithmic trade-offs and pointer-like references.

---

# 14. Chapter 13 — Recursion and Backtracking

## 14.1 The three requirements of recursion

A recursive algorithm must have:

1. a base case;
2. a smaller recursive call;
3. a way to combine the result.

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

The call sequence for `SumTo(3)` is:

```text
3 + SumTo(2)
3 + 2 + SumTo(1)
3 + 2 + 1 + SumTo(0)
3 + 2 + 1 + 0
6
```

## 14.2 Recursion and memory

Each active recursive call uses stack memory. Very deep recursion can cause a stack overflow. An iterative solution may be safer for large input.

## 14.3 Generate subsets with backtracking

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

At each index, the algorithm makes two choices:

- exclude the value;
- include the value.

The removal step undoes the choice before returning to a previous level. That is the “backtracking” action.

## 14.4 Pruning

Backtracking becomes practical when impossible partial solutions are rejected early.

Example: when constructing a password, stop exploring a branch as soon as it violates a length or character rule.

---

# 15. Chapter 14 — Divide and Conquer

## 15.1 The pattern

Divide and conquer has three parts:

1. divide the problem into smaller subproblems;
2. solve each subproblem;
3. combine the results.

Merge sort is the classic example.

## 15.2 Why it works

If a problem of size `n` becomes several problems of size approximately `n / 2`, the depth of the recursion is often logarithmic. If each level processes all `n` items, the total complexity may become `O(n log n)`.

## 15.3 Recursive maximum

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

The base case handles one item. The recursive calls solve the left and right halves. `Math.Max` combines the two answers.

## 15.4 When not to use it

Do not use divide and conquer when:

- the subproblems overlap heavily and dynamic programming is better;
- the input is tiny and a loop is clearer;
- the combination step is more expensive than the original work;
- recursion creates unnecessary memory pressure.

---

# 16. Chapter 15 — Trees, Heaps, and Priority Queues

## 16.1 Tree vocabulary

A tree contains nodes connected in a hierarchy:

- root: the top node;
- parent: a node with children;
- child: a node below a parent;
- leaf: a node with no children;
- depth: distance from the root;
- height: longest path downward.

## 16.2 Binary search tree idea

A binary search tree follows an ordering rule:

- values smaller than a node go left;
- values larger go right.

If balanced, search is approximately `O(log n)`. If badly unbalanced, it can degrade to `O(n)`.

## 16.3 Tree traversal

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

For a binary search tree, in-order traversal prints values in sorted order.

## 16.4 Heap and priority queue

A heap lets you repeatedly remove the highest- or lowest-priority item efficiently. C# provides `PriorityQueue<TElement, TPriority>`:

```csharp
PriorityQueue<string, int> queue = new();
queue.Enqueue("normal", 10);
queue.Enqueue("urgent", 1);
string next = queue.Dequeue();
```

With the default priority comparison, the smaller priority value is dequeued first. Always verify and document that convention in your application.

Use priority queues for:

- scheduling;
- shortest paths;
- emergency processing;
- simulations;
- selecting the next best candidate.

---

# 17. Chapter 16 — Graph Algorithms

## 17.1 Graph vocabulary

A graph has:

- **vertices** or nodes;
- **edges** connecting them;
- optional direction;
- optional weights.

Examples:

- roads between cities;
- users connected by friendships;
- services connected by network calls;
- tasks connected by prerequisites.

## 17.2 Adjacency list

```csharp
Dictionary<string, List<string>> graph = new()
{
    ["A"] = new() { "B", "C" },
    ["B"] = new() { "D" },
    ["C"] = new() { "D" },
    ["D"] = new()
};
```

An adjacency list stores the neighbors of each vertex. It is efficient for sparse graphs.

## 17.3 Breadth-first search

BFS explores by distance from the start and uses a queue:

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

The `visited` set prevents infinite loops in cyclic graphs. Complexity is `O(V + E)` for an adjacency-list graph.

## 17.4 Depth-first search

DFS explores as far as possible before backtracking. It can use recursion or an explicit stack:

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

## 17.5 Topological sorting

A topological order lists directed acyclic graph vertices so that every prerequisite appears before the item that depends on it.

Use it for:

- build systems;
- course prerequisites;
- workflow ordering;
- task dependencies.

If a cycle exists, no valid topological order exists.

## 17.6 Shortest paths

Algorithm choice depends on edge weights:

| Graph situation | Common choice |
|---|---|
| Unweighted edges | BFS |
| Non-negative weights | Dijkstra's algorithm |
| Negative edges allowed | Bellman–Ford |
| All-pairs shortest paths | Floyd–Warshall or repeated single-source methods |
|

## 17.7 Minimum spanning trees

For a connected weighted undirected graph, a minimum spanning tree connects every vertex with minimum total edge weight.

Common algorithms:

- Kruskal's algorithm;
- Prim's algorithm.

Applications include network design and infrastructure planning.

---

# 18. Chapter 17 — Greedy Algorithms

## 18.1 The greedy idea

A greedy algorithm repeatedly chooses the best local option according to a rule.

Greedy algorithms can be excellent when a proof shows that local choices lead to a global optimum.

## 18.2 Activity selection

Suppose you want the maximum number of non-overlapping events. Sort by finishing time and repeatedly select the next compatible event.

The key proof idea is an exchange argument: choosing the event that finishes earliest leaves at least as much room for future events as any other first choice.

## 18.3 Coin change warning

For some coin systems, choosing the largest coin first works. For arbitrary coin values, it can fail.

Example denominations `{1, 3, 4}` and target `6`:

- greedy: `4 + 1 + 1` = 3 coins;
- optimal: `3 + 3` = 2 coins.

Never assume greedy is correct without proving the problem has the required structure.

## 18.4 Greedy engineering checklist

Before using greedy:

- define the local choice;
- test small counterexamples;
- ask whether the choice can harm later options;
- search for an exchange or cut-property proof;
- compare with dynamic programming for small inputs.

---

# 19. Chapter 18 — Dynamic Programming

## 19.1 The two signs of dynamic programming

Dynamic programming is often useful when a problem has:

1. **overlapping subproblems**: the same smaller problem appears repeatedly;
2. **optimal substructure**: an optimal solution can be built from optimal smaller solutions.

## 19.2 Memoization

Memoization stores recursive results:

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

The dictionary changes repeated exponential work into approximately linear work.

## 19.3 Tabulation

Tabulation fills a table from small solutions toward the final solution:

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

This version uses `O(1)` extra space because only the previous two values are needed.

## 19.4 Knapsack pattern

A common dynamic-programming problem is selecting items with weights and values under a capacity limit.

A state may be:

```text
best[i, capacity] = the best value using the first i items with this capacity
```

For each item, choose between:

- not taking it;
- taking it if it fits.

The hard part is not typing the loops. It is defining the correct state.

## 19.5 Dynamic-programming checklist

1. What is the smallest subproblem?
2. What information fully describes a subproblem?
3. What choices can be made next?
4. What is the recurrence?
5. What are the base cases?
6. In what order can states be computed?
7. Can the table be compressed?

---

# 20. Chapter 19 — String and Text Algorithms

## 20.1 Normalize before comparing

Text equality depends on rules:

```csharp
bool same = left.Equals(
    right,
    StringComparison.OrdinalIgnoreCase);
```

Do not silently apply culture-sensitive transformations when identifiers or protocol values require exact comparison.

## 20.2 Palindrome check

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

Two pointers compare mirrored characters. Complexity is `O(n)` time and `O(1)` extra space.

## 20.3 Anagram detection

Two words are anagrams if they contain the same character counts under the chosen normalization rule.

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

## 20.4 Pattern matching

Simple substring search may be sufficient for small input. For large repeated searches, algorithms such as Knuth–Morris–Pratt or Boyer–Moore reduce unnecessary comparisons.

The engineering decision depends on:

- text size;
- pattern size;
- number of searches;
- memory limits;
- library support.

## 20.5 Tokenization and parsing

Text analysis often follows this pipeline:

```text
raw text → normalize → tokenize → classify → aggregate → report
```

Each step is an algorithmic transformation and should have a clear contract.

---

# 21. Chapter 20 — Algorithms for Data Analysis

This chapter connects algorithmic thinking to practical data analysis.

## 21.1 Data-analysis pipeline

A reliable analysis usually contains:

1. acquisition;
2. validation;
3. cleaning;
4. transformation;
5. aggregation;
6. calculation;
7. anomaly detection;
8. interpretation;
9. reporting.

The output is only as reliable as the assumptions and transformations that precede it.

## 21.2 Mean, median, and mode

Mean:

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

Median requires sorted values:

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

The mean is sensitive to extreme values. The median is often more robust for skewed data.

## 21.3 Variance and standard deviation

Population variance measures average squared distance from the mean:

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

Document whether you are calculating population or sample standard deviation. The denominator differs.

## 21.4 Grouping and aggregation

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

This is a hash-based aggregation algorithm with expected `O(n)` time.

## 21.5 Outlier detection with the IQR rule

The interquartile range is:

```text
IQR = Q3 - Q1
lower bound = Q1 - 1.5 × IQR
upper bound = Q3 + 1.5 × IQR
```

Values outside the bounds are often flagged as potential outliers. A flagged value is not automatically an error. It may represent a real event.

## 21.6 Data quality checks

Before analyzing data, check:

- missing values;
- duplicate records;
- impossible ranges;
- inconsistent categories;
- mixed date formats;
- unexpected units;
- extreme values;
- sampling bias.

An algorithm can calculate a precise answer from inaccurate data. Precision is not the same as validity.

---

# 22. Chapter 21 — Build the Algorithm Lab

We now build a complete C# console application that demonstrates algorithms and data analysis.

## 22.1 Create the project

```bash
dotnet new console -n AlgorithmLab
cd AlgorithmLab
mkdir Algorithms Models Services
```

Create this structure:

```text
AlgorithmLab/
├── Algorithms/
│   ├── SearchAlgorithms.cs
│   ├── SortAlgorithms.cs
│   └── StatisticsAlgorithms.cs
├── Models/
│   └── AnalysisReport.cs
├── Services/
│   └── CsvNumberReader.cs
└── Program.cs
```

The application will:

- read numbers from a CSV file;
- validate the values;
- show count, minimum, maximum, mean, median, and standard deviation;
- sort the data;
- search for a value;
- report possible outliers.

## 22.2 Create the model

Create `Models/AnalysisReport.cs`:

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

Explanation:

- `sealed` says this type is not intended to be inherited from.
- `init` allows each property to be assigned during object creation but not changed afterward.
- `IReadOnlyList<double>` exposes results without allowing callers to modify the report's list through the property.
- `Array.Empty<double>()` provides an empty default without allocating a new array every time.

## 22.3 Create the CSV reader

Create `Services/CsvNumberReader.cs`:

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

Line by line:

- `using System.Globalization` gives access to culture and numeric-format rules.
- `Read` receives a file path and returns read-only numeric data.
- `File.Exists` checks the external input before reading.
- `List<double>` grows as values are discovered.
- `ReadAllLines` loads the file as lines.
- `Split` separates comma-delimited cells.
- `RemoveEmptyEntries` ignores empty cells.
- `Trim` removes surrounding whitespace.
- `InvariantCulture` makes decimal parsing predictable across machines.
- Invalid cells are skipped in this beginner version; a production version should usually report them with line and column numbers.

## 22.4 Create search algorithms

Create `Algorithms/SearchAlgorithms.cs`:

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

The first method works on any order. The second method has a crucial precondition: `sortedValues` must be sorted in ascending order.

## 22.5 Create sorting algorithms

Create `Algorithms/SortAlgorithms.cs`:

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

The public method divides the input. The private method combines two already sorted lists. Keeping `Merge` private communicates that it is an implementation detail.

## 22.6 Create statistics algorithms

Create `Algorithms/StatisticsAlgorithms.cs`:

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

Important design decisions:

- all public calculations reject empty input;
- median and outlier detection sort a copy, not the caller's collection;
- standard deviation is explicitly population standard deviation;
- percentile interpolation is written as a separate private algorithm;
- the report can explain the assumptions used.

## 22.7 Create the application entry point

Replace `Program.cs` with:

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

Line-by-line explanation:

1. The `using` statements import the algorithm and reader namespaces.
2. `namespace AlgorithmLab` groups the program type.
3. `Program` is a static class because the application does not need a `Program` object.
4. `Main(string[] args)` is the entry point and accepts command-line arguments.
5. The path is the first argument if provided; otherwise it defaults to `data.csv`.
6. `new()` creates a CSV reader.
7. The `try` block surrounds external file access and calculations that may reject input.
8. The reader returns read-only numeric data.
9. Empty data is handled before calculations that require at least one value.
10. Merge sort creates an ordered copy.
11. Binary search runs only on the sorted data.
12. The statistics service calculates potential outliers.
13. Interpolated strings format report lines.
14. `sorted[^1]` uses the index-from-end operator to access the final item.
15. The `catch` blocks convert technical failures into readable messages.

## 22.8 Add sample data

Create `data.csv`:

```text
12.5,14.0,13.2,15.8,11.4,12.9,14.7,100.0,13.8
```

Run:

```bash
dotnet run
```

Or pass another file:

```bash
dotnet run -- another-data.csv
```

## 22.9 Test the application manually

Test these cases:

1. normal data with several values;
2. one value;
3. an empty file;
4. a missing file;
5. invalid cells mixed with valid values;
6. negative values;
7. duplicate values;
8. a very large value that may become an outlier;
9. values already sorted;
10. values in reverse order.

For each test, write the expected output before running the program.

---

# 23. Chapter 22 — Testing, Benchmarking, and Debugging

## 23.1 Test algorithm contracts

For `BinarySearch`, test:

- target at the first position;
- target at the last position;
- target in the middle;
- target absent;
- empty array;
- one-item array;
- duplicate values;
- unsorted input to confirm the precondition is documented.

## 23.2 Unit-test example

Using xUnit:

```csharp
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
```

## 23.3 Property-based thinking

Some results have general properties:

- a sorted output is never smaller than its next item;
- sorting preserves the same multiset of values;
- the mean of identical values equals that value;
- a palindrome reads the same in both directions.

Even without a property-testing library, write tests around these properties.

## 23.4 Benchmarking fairly

When comparing algorithms:

- use the same input values;
- test multiple input sizes;
- include favorable and unfavorable orders;
- warm up the runtime when appropriate;
- avoid measuring file I/O when comparing sorting;
- repeat measurements;
- distinguish elapsed time from allocated memory.

A benchmark should answer a question such as:

> At what input size does merge sort become faster than insertion sort for this workload?

## 23.5 Debugging with traces

For a sorting algorithm, print the array after each meaningful phase:

```csharp
Console.WriteLine(string.Join(", ", numbers));
```

For recursion, print the current range and indentation level. For graphs, print the queue or stack and visited set. The goal is to observe state transitions, not to print everything forever.

## 23.6 Common algorithm bugs

- off-by-one indexes;
- forgetting an empty input case;
- using binary search on unsorted data;
- infinite loops because a pointer never moves;
- modifying a collection while enumerating it;
- using integer division when decimal precision is needed;
- comparing floating-point values with exact equality when tolerance is required;
- forgetting to mark graph nodes visited;
- returning an internal mutable collection;
- confusing an algorithm's best case with its worst case.

---

# 24. Chapter 23 — Advanced Design and Mastery

## 24.1 Choose algorithms by workload

Ask:

- How large is the data?
- Is the data static or changing?
- How many queries will be made?
- Is preprocessing allowed?
- Is memory limited?
- Is exactness required?
- Is approximate output acceptable?
- Does order matter?
- Are there concurrency concerns?

## 24.2 Online versus offline algorithms

An **online algorithm** processes data as it arrives and cannot assume it will see the future. An **offline algorithm** can inspect all input before producing the result.

Examples:

- streaming average: online;
- sort all records then calculate median: offline;
- live alerting: online;
- complete historical report: often offline.

## 24.3 Exact versus approximate algorithms

For very large data, exact answers may require too much memory or time. Approximate algorithms trade a controlled amount of accuracy for speed or compactness.

Examples include sketches for frequency, approximate distinct counts, and sampling. If you use an approximation, document its error behavior.

## 24.4 Deterministic versus randomized algorithms

A deterministic algorithm follows the same path for the same input. A randomized algorithm uses random choices, often to improve expected performance or simplify design.

When randomness is involved:

- record the seed for reproducible tests;
- distinguish expected from worst-case performance;
- verify the result statistically when appropriate.

## 24.5 Numerical stability

Data-analysis algorithms must consider numeric representation:

- floating-point values are approximations;
- adding many values can accumulate error;
- very large and very small values can interact poorly;
- variance formulas can suffer cancellation.

For financial calculations, use appropriate decimal or fixed-point rules. For scientific calculations, document tolerances and units.

## 24.6 Parallelism

A problem may be parallelizable when independent pieces can be processed at the same time. But parallel code introduces:

- synchronization;
- shared-state hazards;
- scheduling overhead;
- ordering questions;
- nondeterministic failures.

Parallelize only after measuring that the sequential version is a bottleneck and that the work is sufficiently large.

## 24.7 Algorithm design interview method

When solving a new problem:

1. Restate it.
2. Ask clarifying questions.
3. Give a simple brute-force solution.
4. Analyze the brute-force complexity.
5. Identify the bottleneck.
6. Choose a data structure or pattern to remove that bottleneck.
7. Explain correctness.
8. Test with examples and edge cases.
9. State time and space complexity.
10. Discuss alternatives and trade-offs.

## 24.8 Capstone upgrades for Algorithm Lab

Implement these in order:

1. Add a command-line option for choosing linear or binary search.
2. Add an insertion-sort implementation and compare it with merge sort.
3. Report the time spent by each sorting method.
4. Add grouped analysis for multiple CSV columns.
5. Report invalid cells with line and column numbers.
6. Add minimum, maximum, range, and quartiles.
7. Add a moving average using a sliding window.
8. Add a frequency table for rounded numeric buckets.
9. Add a streaming mode that does not load the entire file.
10. Add unit tests and benchmark tests.
11. Add a graph module that analyzes relationships in a second file.
12. Add a shortest-path demonstration.
13. Export the report to JSON.
14. Add a web API around the analysis engine.

For each upgrade, preserve the original behavior and add tests before refactoring.

---

# Appendix A — Complexity Reference

| Algorithm or operation | Average time | Worst time | Extra space |
|---|---:|---:|---:|
| Array index access | `O(1)` | `O(1)` | `O(1)` |
| Linear search | `O(n)` | `O(n)` | `O(1)` |
| Binary search | `O(log n)` | `O(log n)` | `O(1)` iterative |
| Hash-set lookup | `O(1)` expected | `O(n)` possible | `O(n)` |
| Array/list append | `O(1)` amortized | `O(n)` resize | `O(1)` extra |
| Insert at list beginning | `O(n)` | `O(n)` | `O(1)` |
| Selection sort | `O(n²)` | `O(n²)` | `O(1)` |
| Insertion sort | `O(n²)` | `O(n²)` | `O(1)` |
| Merge sort | `O(n log n)` | `O(n log n)` | `O(n)` |
| BFS | `O(V + E)` | `O(V + E)` | `O(V)` |
| DFS | `O(V + E)` | `O(V + E)` | `O(V)` |
| Heap insertion | `O(log n)` | `O(log n)` | `O(1)` |
| Heap removal | `O(log n)` | `O(log n)` | `O(1)` |
| Dijkstra with binary heap | `O((V + E) log V)` | same | `O(V)` |

These are general descriptions. Real performance depends on implementation, input distribution, hardware, allocations, and constant factors.

---

# Appendix B — Algorithm Vocabulary

| Term | Meaning |
|---|---|
| Adjacency list | A graph representation storing neighbors for each vertex |
| Algorithm | A finite, precise procedure for transforming input into output |
| Amortized analysis | Average cost over a sequence of operations |
| Backtracking | Exploring choices and undoing choices when a branch fails |
| Base case | The stopping condition of a recursive algorithm |
| Big O | A growth-rate upper-bound notation commonly used for complexity |
| Binary search | Search that repeatedly halves sorted search space |
| Breadth-first search | Graph traversal that explores by layers using a queue |
| Brute force | Directly trying all candidates or possibilities |
| Complexity | How resource usage grows with input size |
| Divide and conquer | Divide, solve smaller parts, combine results |
| Dynamic programming | Reusing results of overlapping subproblems |
| Edge | A connection between graph vertices |
| Greedy algorithm | Repeatedly choosing a locally best option |
| Hashing | Mapping a value to a location or bucket for fast lookup |
| Invariant | A fact that remains true during an algorithm |
| Memoization | Caching results of recursive subproblems |
| Node | An element in a linked structure or graph/tree |
| Online algorithm | Processes data without seeing all future input |
| Precondition | A condition required before an algorithm starts |
| Postcondition | A condition that should hold after an algorithm finishes |
| Recursion | A method solving a problem by calling itself on smaller input |
| Sliding window | Maintaining a moving contiguous section of data |
| Space complexity | Growth of additional memory use |
| Stable sort | A sort that preserves relative order of equal-key records |
| Tabulation | Filling a dynamic-programming table iteratively |
| Topological order | Dependency-respecting order of a directed acyclic graph |
| Two pointers | Using two positions to scan or narrow a sequence |
| Vertex | A node in a graph |
| Worst case | Most expensive valid input behavior |

---

# Appendix C — Practice Roadmap

## Stage 1: Fundamentals

Solve these with loops and arrays:

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

## Stage 2: Core patterns

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

## Stage 3: Recursion and trees

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

## Stage 4: Graphs

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

## Stage 5: Dynamic programming

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

## Stage 6: Data-analysis applications

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

## Final checklist

Before calling an algorithm complete, ask:

- [ ] Did I define the input contract?
- [ ] Did I define the output contract?
- [ ] Did I state preconditions?
- [ ] Did I test empty input?
- [ ] Did I test one item?
- [ ] Did I test duplicates?
- [ ] Did I test boundary values?
- [ ] Did I consider invalid input?
- [ ] Can I explain why it is correct?
- [ ] Can I state time complexity?
- [ ] Can I state space complexity?
- [ ] Is there a simpler solution?
- [ ] Is there a faster solution if the data grows?
- [ ] Does the chosen data structure fit the operations?
- [ ] Did I measure before optimizing?
- [ ] Did I document assumptions?

---

## Final message to the learner

Algorithms are the language of precise problem solving. You do not become strong by memorizing a list of names. You become strong by repeatedly practicing this cycle:

> Define the problem → create examples → design a simple procedure → prove it → implement it → test it → measure it → improve it responsibly.

Use C# as your laboratory. Type every implementation. Break it deliberately. Repair it. Compare two approaches on the same data. Explain why one is better for one workload and worse for another.

That process—from clear requirements to tested, measured, and explainable solutions—is the path from absolute beginner to algorithmic mastery.
