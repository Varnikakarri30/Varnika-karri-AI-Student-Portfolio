# Day 2 – Six Pattern Drills

## Pattern 1 – Persona

Prompt:
You are a senior placement coach at Aditya University.

You have prepared 200 B.Tech CSE students for TCS, Infosys and Cognizant placement interviews.

A 3rd-year CSE student with 7.5 CGPA asks you about Big-O notation.

Explain it the way you would in a one-on-one placement preparation session.

Use simple language, practical examples and interview-focused explanation.

Output:
Use simple language, practical examples and interview-focused explanation.

2:34 pm
Big-O Notation — The Way I'd Explain It To You In Person
Alright, sit down. Close your phone. This one topic has eliminated more students in TCS and Infosys technical rounds than almost anything else — not because it's hard, but because students memorise definitions without understanding what the interviewer is actually testing.

Let me fix that right now.

First — What Is the Interviewer Actually Asking?
When a TCS or Infosys interviewer says "what's the time complexity of this?", they are not asking you to recite a formula. They are asking:

"If I give you 10 times more data, how much slower does your code get?"

That's it. That's the whole question. Big-O is just a language to answer that question precisely.

The Simplest Way to Understand It
Imagine you're searching for a friend's name in a register.

Scenario 1 — The register has 100 names, all random. You start from page 1 and check every name. Worst case: you check all 100. Now the college grows. The register has 1,000 names. Worst case: you check all 1,000.

10× more data → 10× more work. That's O(n) — Linear.

Scenario 2 — Same register, but now it's sorted alphabetically. You open the middle. Too early? Go to the second half. Repeat. 100 names → roughly 7 steps. 1,000 names → roughly 10 steps.

10× more data → barely more work. That's O(log n) — Logarithmic.

Scenario 3 — You check every name against every other name. 100 names → 10,000 comparisons. 1,000 names → 1,000,000 comparisons.

10× more data → 100× more work. That's O(n²) — Quadratic.

The 6 Complexities You Must Know Cold
Big-O	Name	Real example	Interview verdict
O(1)	Constant	Array index access arr[5]	Excellent
O(log n)	Logarithmic	Binary search	Excellent
O(n)	Linear	Loop through array once	Good
O(n log n)	Log-linear	Merge sort, Quick sort	Acceptable
O(n²)	Quadratic	Nested loops, Bubble sort	Weak — justify it
O(2ⁿ)	Exponential	Recursive Fibonacci (naive)	Never write this in an interview
Print this. Stick it on your wall. You will be asked about at least three of these.

How To Actually Calculate It — The 3-Step Method
I teach every student the same three steps. Do not skip any.

Step 1 — Count your loops. One loop over n elements → O(n). One loop inside another loop, both over n → O(n²). No loop at all → O(1).

Step 2 — Drop the constants. If your code does 3n operations, it's still O(n). Not O(3n). Big-O describes the shape of growth, not the exact count.

Step 3 — Keep only the dominant term. If your code does n² + n operations, drop the n. It's O(n²). At large n, the smaller terms become irrelevant.

The Example I Use In Every Session
python
# What is the time complexity of this?

def find_duplicate(arr):
    for i in range(len(arr)):           # Loop 1 — runs n times
        for j in range(i+1, len(arr)):  # Loop 2 — runs ~n times
            if arr[i] == arr[j]:
                return True
    return False
Two nested loops, both over n → O(n²).

Now I ask you: "Can you do better?"

The answer is yes — use a set:

python
def find_duplicate_better(arr):
    seen = set()
    for num in arr:        # One loop — O(n)
        if num in seen:    # Set lookup — O(1)
            return True
        seen.add(num)
    return False
O(n). You just traded memory for speed. That trade-off conversation — that is what gets you the offer.

What TCS, Infosys, and Cognizant Actually Ask
From the 200 students I've prepared, here are the real patterns:

TCS (written + technical interview): Mostly asks you to identify complexity of given code. They show you a function and ask — "O(n) or O(n²)?" Be fast and be confident.

Infosys (Specialised Analyst track): They go one level deeper. "You said O(n²) — how would you optimise it?" Always have an answer ready. The optimisation matters as much as the identification.

Cognizant (GenC/GenC Pro): They often ask this inside a DSA problem. "You've solved it — now what's the complexity?" Don't freeze. Walk through your own code using the 3-step method aloud.

The One Mistake That Kills Candidates
A student last year — 8.1 CGPA, sharp kid — froze when the interviewer said:

"Your solution works. But what happens when n is 10 million?"

He had never thought about his code at scale. He had only thought about whether it runs.

Big-O is how you think about code at scale. Every time you write a loop from now on, ask yourself: if n becomes 10 million, is this still acceptable?

Before You Leave This Session
Three things I want you to do tonight:

Write the 6 complexities from memory — no looking. If you can't, you're not ready.
Take any 5 functions you've written in your lab assignments. Calculate the time complexity of each using the 3-step method.
Practice saying it aloud. Interviewers notice when you think in complexity vs. when you recite it. The difference shows in 30 seconds.
Your 7.5 CGPA tells me you have the fundamentals. Big-O is not about intelligence — it's about fluency. Get fluent before the drive comes. You have time. Use it.




Self Score:
4/5

---

## Pattern 2 – Few Shot

Prompt:
Here are example explanations from a placement coach.

Q: What is recursion?

A: A function calling itself with a smaller problem. Like Russian dolls. Stops at a base case. Example: factorial.

Q: What is a stack?

A: LIFO data structure. Push to add. Pop to remove. Like a stack of plates.

Q: What is Big-O notation?

A:

Output:
O(n²) — Quadratic.O(n²)** — Quadratic. Two nested loops. Bubble sort.
O(2ⁿ) — Exponential. Never write this in an interview.

Self Score:
4/5

---

## Pattern 3 – Chain of Thought

Prompt:
Explain Big-O notation to a placement interview candidate.

Think step by step before answering.

Step 1: Define Big-O in one sentence.

Step 2: Give one concrete example with code.

Step 3: Explain why interviewers ask about it.

Step 4: Create a 3-sentence summary.

Output:
Step 4: Create a 3-sentence summary.

2:37 pm
Step 1: Define Big-O in one sentence. Big-O measures how your code's runtime grows as input size increases.

Step 2: One concrete example with code.

python
# O(n) — one loop
for i in arr:
    print(i)

# O(n²) — nested loops
for i in arr:
    for j in arr:
        print(i, j)
Ten times more data → O(n) takes 10× longer. O(n²) takes 100× longer.

Step 3: Why interviewers ask about it. They're not testing if your code works — they're testing if it scales. A solution that runs fine on 100 records may crash a production system with 10 million. Interviewers want engineers who think at scale before writing the first line.

Step 4: Three-sentence summary. Big-O describes how code behaves as data grows, not just whether it runs. The four complexities you must know cold are O(1), O(log n), O(n), and O(n²). Every time you write a loop, ask yourself: if n becomes 10 million, is this still acceptable?

Self Score:
5/5

---

## Pattern 4 – Structured Output

Prompt:
Explain Big-O notation for a placement interview.

Return ONLY valid JSON.

{
  "definition":"one sentence",
  "intuition":"analogy",
  "code_example":"Python example",
  "common_pitfall":"mistake students make",
  "interview_test_question":"follow-up question"
}

Output:
{
  "definition": "Big-O measures how an algorithm's runtime grows relative to input size.",
  "intuition": "Like a queue at a bank — one teller serving 100 people takes twice as long as 50 people (O(n)), but a system that checks every person against every other person explodes in time (O(n²)).",
  "code_example": "def has_duplicate(arr):\n    for i in range(len(arr)):\n        for j in range(i+1, len(arr)):\n            if arr[i] == arr[j]:\n                return True\n    return False\n# Two nested loops → O(n²). Rewrite with a set → O(n).",
  "common_pitfall": "Students drop constants correctly (3n → O(n)) but forget to drop smaller terms — writing O(n² + n) instead of O(n²).",
  "interview_test_question": "Your solution works on my test case — what happens to its runtime when the input grows from 1,000 to 1,000,000 records?"
}

Self Score:
4/5

---

## Pattern 5 – System Prompt

system-Prompt:
You are a senior placement coach for B.Tech CSE students at an Indian engineering college.

You prepare students for TCS, Infosys and Cognizant interviews.

You explain technical concepts in 50-80 words maximum, conversationally, with one code example.

user-prompt:
Explain Big-O notation.

Output:
Big-O notation measures how your code's runtime or space grows as input size increases. It ignores constants and focuses on the worst case. Interviewers want to know: "If I double the input, does your solution double in time? Quadruple?"

python
# O(n) - linear: one loop
for i in range(n): print(i)

# O(n²) - quadratic: nested loops (avoid in TCS/Infosys coding rounds!)
for i in range(n):
    for j in range(n): print(i, j)
In interviews, always state the Big-O before you code — it shows structured thinking. 🎯



Self Score:
5/5

---

## Pattern 6 – Prompt Chaining
Chat-1
Prompt:
List the 5 most important sub-concepts a B.Tech student must understand about Big-O notation.

Just give the list.

Output:
Here are the 5 most important Big-O sub-concepts:

Time vs Space Complexity — two separate dimensions to measure
Worst-case analysis — Big-O always describes the upper bound
Dropping constants and lower-order terms — O(2n + 5) → O(n)
Common complexity classes — O(1), O(log n), O(n), O(n log n), O(n²)
How loops determine complexity — single loop = O(n), nested loops = O(n²)
For each of these 5 sub-conc

chat-2:
Prompt:
For each of these 5 sub-concepts write one paragraph for a 3rd-year B.Tech CSE student preparing for placements. 
Here are the 5 most important Big-O sub-concepts:

Time vs Space Complexity — two separate dimensions to measure
Worst-case analysis — Big-O always describes the upper bound
Dropping constants and lower-order terms — O(2n + 5) → O(n)
Common complexity classes — O(1), O(log n), O(n), O(n log n), O(n²)
How loops determine complexity — single loop = O(n), nested loops = O(n²)
For each of these 5 sub-conc

output:
Here's each concept explained placement-style:

1. Time vs Space Complexity
When TCS or Infosys asks "how efficient is your code?", they mean two things — how long it runs and how much memory it uses. Time complexity counts your operations; space complexity counts your extra variables, arrays, or recursion stack. A solution can be fast but memory-hungry, or slow but memory-efficient. In interviews, always mention both — it immediately signals you think like an engineer, not just a coder.

2. Worst-Case Analysis
Big-O is always about the worst possible input. Searching an array of 1000 elements — best case, your target is at index 0. But Big-O doesn't care. It asks: what if your element is the last one? That's O(n). Companies like Cognizant test this by asking "what's the complexity if the element isn't present?" — always answer for the worst case.

3. Dropping Constants and Lower-Order Terms
If your algorithm does 3n + 500 operations, Big-O calls it O(n). Why? Because at scale — say n = 10 million — that 500 is meaningless. TCS interviewers specifically ask you to simplify expressions like O(2n² + 3n + 10) → O(n²). The rule: keep only the fastest-growing term, drop the coefficient. It shows you understand asymptotic behavior, not just arithmetic.

4. Common Complexity Classes
These six are your placement vocabulary — memorize them in order from fastest to slowest: O(1) → O(log n) → O(n) → O(n log n) → O(n²) → O(2ⁿ). Binary search is O(log n), bubble sort is O(n²), merge sort is O(n log n). Infosys frequently asks "which sorting algorithm would you use for large data?" — your answer must include the complexity class and why it matters for that input size.

5. How Loops Determine Complexity
This is your most practical tool in coding rounds. One loop over n elements = O(n). Two nested loops over n elements = O(n²). A loop that halves its range each iteration = O(log n). Cognizant and TCS both give code snippets and ask you to identify complexity on-the-spot. Train yourself to look at the loop structure first — that alone will get you the right answer 80% of the time.

Chat-3:

prompt:
Convert these five paragraphs into one concise 80-word interview-preparation explanation.
Keep all five ideas.
Use conversational language.
End with one practice interview question.
[paste five paragraphs]


Output:
Always analyze your code on two axes — time and space. Big-O measures worst-case behavior, so assume the worst input every time. When simplifying, drop constants and smaller terms — O(3n² + 5n) becomes O(n²). Know your six complexity classes cold: O(1), O(log n), O(n), O(n log n), O(n²), O(2ⁿ). Finally, read loops to crack complexity instantly — nested loops usually mean O(n²).
Practice question: "What is the time and space complexity of bubble sort, and how would you optimize it?"

Self Score:
5/5


# Peer Scores

| Pattern | Peer Score (/10) |
|----------|----------|
| Persona | 8 |
| Few Shot | 7 |
| Chain of Thought | 9 |
| Structured Output | 8 |
| System Prompt | 9 |
| Prompt Chaining | 10 |



# Reflection

For my placement-preparation students, the patterns I will use most are Chain of Thought and Prompt Chaining.

Chain of Thought helps students understand concepts step-by-step instead of memorising answers.

Prompt Chaining helps break complex topics into smaller parts and produces higher-quality explanations than a single prompt.

These two patterns are especially useful when preparing students for technical placement interviews.