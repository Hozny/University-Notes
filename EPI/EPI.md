# Elements of Programming Interviews (C++) 
Notes for EPI (Version 2.0.0)

## The EPI editorial style 
Problems: 
1. Establish context (e.g, real-world scenario)
2. State the problem to be solved (does not specify detailed constraints, input format, etc...)
4. Give a short hint (only read this if stuck)

Solutions: 
1. Develop simple brute-force
2. Aanalyze brute-force to get intution for inefficiencies and where to improve
3. Develop more efficient algorithm 
4. Apply program to concrete input
5. Give code for key steps
6. Analyze space and time complexity
7. Outline variants - problems whose solution is similar to the solved problem 

## Recommended algorithm books (for those who require prerequisite knowledge)
Algorithms by Dasgupta, et al.  ("succinct and beautifully written")
Introduction to Algirhtms by Cormen, et al. ("amazing reference")           

## Study guide 
Hackacthon (weekend entirely devoted to preparation)            
Finals cram (one week, 3-4 hours a day)         
Term project (four weeks, 1.5-2.5 hours per day)        
Algorithms class (3-4 months, 1 hour per day)

## The interview lifecycle
1. Identify companies you are interested in. Ideally find people you know at these companies. 
2. Prepare resume. Submit through personal contact (preferred)
3. Perform phone screening (question-answer with engineer). Might require submitting code via shared document. Don't take this casually - can be very challenging.  
4. Go for an on-site interview. One-on-one interviews with engineers and managers, and a convo with your HR contact. 
5. Receive offers. Usually starting point for negotiations. 

## The resume (this advice makes more sense for full-time positions than internships, or really sought-after internships)
1. Have a clear statement of your objective (tailor resume for a given employer)
2. The most important points (the differentiating points) should come first. Logical order comes second to this principle. 
    - list significant class projects, standardized test scores (if exceptionsal), etc... 
3. The resume should be high-quality: no spelling mistakes, good formatting, capitilzations, numberings, correct grammar/punction. Use few fonts. PDF is preferred.
4. Concact information, LinkedIn profile, URL to personal homepage with examples of work. 
5. If you can work at company without special processing (e.g., green card) make note of it. 
6. Have friends review your resume. It is better to write something quickly and then refine based on feedback. 
7. Resume does not have to be one page, two pages is appropriate (more than two is likely not). This advice does not apply to juniors/first internship. 
8. Prefer not to see a list of hobbies/ECs unless they are different "olympic" or high level achievements

## Mock interviews 
Get a friend. Code on paper. Give hints when stuck. Record and review session. Give feedback both positive and negative.        

## Language review
C++ best practices: 
- follow Google's C++ style guide: 
    - input arguments are either values or const references. 
    - use pointers to pass output arguments to functions
    - use `deque<bool>` for Boolean arrays, `vector<bool>` is not an STL container. 

Review the [Google C++ style guide](https://google.github.io/styleguide/cppguide.html) 

# Strategies For A Great Interview 
A typical one hour interview will be 5 minutes of introduction/questions about resume, 5-15 minutes of questions on basic programming concepts. The core of the interview is one or two detailed design questions where candidate will present a solution. 

## Aproaching the problem 
Clarify the question
- good way to clarify is state a concrete exmaple of the problem (example case)
- ask interviewer about complexity they would like, they might refuse but no harm in asking and you may get some clues. 

Work on concrete examples            

Spell out the brute-force solution:
- good idea and shows ur problem solving process 
- can be detrimental if it takes long time to describe the brute-force approach

Think out loud: 
- helps u stay on track 
- gives interviewers ability to guide you in right direction

Apply patterns: 
- good data structure, general algorithm technique, etc.. 

##Presenting solution: 
- once you have algorithm it is important to present it in clear manner. 

Libraries: 
-  don't reinvent the wheel (unless asked to)

Focus on the top-level algirhtm: 
- for example use BST and implement it later
- add TODO comment to portions u want to come back to 

Manage the white board: 
- you will likely use more space than you expect

Assum valid inputs          

Test corner cases           

Syntax 
- don't have lots of syntax erroes (a few small ones is ok)

Memory management 
- avoid memory management operations altogether

## Know your interviewers & the company 
TODO

## General conversation 
TODO 

# Problem Solving
Work hard...

## Data Structure Review 

|Data Structure | Key Points | 
|---|---|
|Promitive types | know how `int,char,double,etc.` are represented in memory|
|Arrays| Fast index access, slow lookup. Be comfortable with iteration, resizing, partitioning, merging, etc.|
|Strings| Know memory representation. Understanding comparison, copying, matching, joining, splitting, etc.|
|Lists|Understand trade-offs with respect to arrays. Iteration, insertion, deletion in singly and doubly linked lists. Know implementation with dynamic memory and arrays |
|Stacks and queues| LIFO FIFO know implementations|
|Binary trees| know depth, heigh, leaves, search path, traversal sequences, successor/predecessor operations|
|Heaps| O(1) lookup of Max, O(log n) insertion and O(log n) deletion of max. Node and array implemenation. Min-heap variant|
|Hash tables| O(1) insertions, deletions and lookups. Not suitable for order-related queries; need for resizing; poor worst-case performacnce. Understand implementation using array of buckets and collision chains. Know has functions for integers, strings, objects.|
|Binary search trees| O(log n) insertions, deletions, lookups, find-min, find-max, successor predecessor when tree is height balanced. Familiar with balance and operations maintaining balance.|

Counting how many set bits in an `int`
- `y = x & ~(x-1)`  ~ is complement operator
    - y is set to 1 at the lowest set bit of x
    - this bit is removed from x using y XOR x
    - O(s) where s is set bits in x
`(x-1)` will set the rightmost 1 bit to 0 and all bits to its right to 1. So `x & ~(x-`)` isolates the right most bit

if we will repeatedly need to look it up we can create an array size 65536 and then break up a 64 bit integer into 16 bits and get the sum of the precomputed values in our array by adding the 16 bit chunk values

problems involving bit manipulation are often asked in interviews. 

**Analaysis patterns:**
|Analysis principle| Key Points | 
|---|---|
|Concrete examples| manually solve concrete example and generalize solution|
|Case analysis | split input/exeuction into cases and solve each separately|
|Iterative refinement| Find brute-force solution and improve on it|
|Reduction| use a well-known solution to another problem as a subroutine|
|Graph modeling| describe the problem using a graph and solve it using an existing algorithm| 

**Algorithm design patterns:**
|Technique| Key Points| 
|---|---|
|Sorting| uncover some structure by sorting input|
|Recursion| if input structure is recursive design recursive algorithm that follows input definition|
|Divide-and-conquer| divide the problem into two or more smaller independent subproblems and solve original using solutions to subproblems|
|Dynamic programming| compute solution for smaller instances of a given input and use these solutions to construct a solution to the pobrlem. Cache results for performance|
|Greedy algorithms| computing solution in stages, making choices that are locally optimum at step; these choices are never undone. (locally optimum solution is globally optimum)|
|Invariants| identify and invariant and use it to rule out potential solutions that are suboptimal/dominated by other solutions|

### Concrete examples
What is the smallest value that cannot be constructed from a set of coins
- at each point if we can construct up to V  but not V+1 and add a coin u. if u <= V+1 then we can construct up to V + u + 1 but if u > V + 1 we cannot construct V + 1. So we keep track of what could be constructed at each point in sorted fashion
```C++
int smallestImpossible(vector<int> A) { 
    sorts(A.begin(), A.end());
    int max_possible = 0; 
    for (int a : A) {
        if (a > max_possible + 1) { 
            break;
        }
        max_possible += a;
    }
    return max_possible;
}
```
- O(nlog n) to sort O(n) to iterate

### Case analysis
example

### Iterative refine-ment of brute-force
Given array A of **n-numbers** rearrange A to get B such that B[0] <= B[1] >= B[2] <= B[3] ...
```C++
void Rearrange(vector<int>* A_ptr) { 
    vector<int>& A = *A_ptr;
    for (size_t i = 1; i < A.size(); ++i) { 
        if ((! I % 2) && A[i - 1] < A[i] || ((i % 2) && A[i - 1] > A[i])) { 
            swap(A[i], A[i-1]);
        }
    }
}
```
- notice this requires unique values 

### Reduction
Problem: determine if string is a rotation of another "car" and "arc" are rotations

This problem is very similar to string search
- we add the string to itself and see if we can find the original string using famous String Search algorithms gives O(n + m)
- bca + bca = bc abc a 

### Graph modelling
see if arbitrage can be formed in currency exchange
- we can set graph to currency with edges being logarithm of exchange rate 
- then using Bellman-Ford we can see if positive cycle exists which is arbitrage

### Sorting
sorting problems...

### Recursion
recursion problems

### Divide and conquer
number of pairs of elements in an array that are out of sorted order

how many ways to place trimineos

### Dynamic programming
how many ways to form a score as the sum of 2, 3, 7
- notice C(s) = C(s-7) + C(s - 3) + C(s-2)

### Greedy algorithm 
map 2n white and black cities in 1 to 1 fashion
- sort white and black and pair left to right each one

### Invariants 
given sorted A find A[i] + A[j] = k 
- use two pointers on each end 
- works because invariant is maintained that when we increment left or right pointer all values we rule out are not possible

# Part 3 - Problems
# Primitive Types