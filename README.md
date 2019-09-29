# LeetCode Course

This is a course designed to ramp up an individual ASAP to crush tech interviews.

At some point I will be expanding upon concepts in this general guide, but I'm quickly typing this up now to help some friends (shoutout to hansson and revanth).

### How to use this Doc

At any step, feel free to continue to any later step. That said, this stuff is inherently a graph of knowledge and so it's not well suited to linear presentation. However, at the very least, you can trust that following this guide in a linear fashion will be a valid progression strategy.

### Step 0: Requirements

You will need:

1. A [LeetCode](https://leetcode.com/) account, ideally with premium (you can share with friends and use the "session" feature to differentiate yourselves)
2. The latest version of Python, downloadable [here](https://www.python.org/)
3. This doc + internet connection

### Step 1: Optionally Learn Python

Python is the best language for interviews because it's quick to write, it's readable, and it's heavily used in industry.

What to learn:

- Basic syntax
  - Variables
  - Math
  - Strings
  - Lists, sets, dicts
  - Printing
  - Functions
  - Classes
  - Loops and control flow
  - Recursion
- Runtime + Space complexity concepts, [here](https://learnxinyminutes.com/docs/asymptotic-notation/) or [here](https://medium.com/karuna-sehgal/a-simplified-explanation-of-the-big-o-notation-82523585e835) or [here](https://stackabuse.com/big-o-notation-and-algorithm-analysis-with-python-examples/), make sure you know the runtime for all the Python data structures you use
- I also recommend you learn generators, coroutines, list comprehension, useful builtins (sorted, breakpoint, zip, enumerate, etc) as knowing this can impress interviewers but more importantly, make you more effective at coding
- It will take many years to have intuition for what's pythonic vs not, but at the very least learn what I've mentioned here

How to learn:

- If you have very limited programming experience start [here](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers), otherwise continue
  - I learned Python [here](https://cscircles.cemc.uwaterloo.ca/) when I was 12 and to this day it's the simplest intro I've seen
- I start learning any language by browsing its [Learn X in Y](https://learnxinyminutes.com/)
  - Check out the one for Python [here](https://learnxinyminutes.com/docs/python3/)
- [https://stackoverflow.com/](https://stackoverflow.com/)
- [https://www.google.com/](https://www.google.com/)
- A realistic [guide](https://realpython.com/async-io-python/) to AsyncIO in Python3.7+, don't look at this unless you plan on truly knowing Python

### Step 2: Jump into Leetcode

At this point, many people would encourage you to start reading up about algorithms and data structures. If you want to do that then skip to the next step, but otherwise I recommend jumping into LeetCode and doing a few *"Easy"* difficulty level problems in order to give you a feel for it. Whatever your approach is to picking problems to try, I highly recommend avoiding ones that have a high proportion of thumbs-down's to thumbs-up's. If you have a subscription, don't look at the solution until after you've tried it, and if you needed to look at the solution then favourite the problem and do it again a week later.

Here is a list of simple problems. You will notice that the problems cover simple data structures like lists and dictionaries, which is why they aren't covered in the next step. Make sure you at least know those two before diving in!

- [Two Sum](https://leetcode.com/problems/two-sum/) will teach you about how using data structures can often improve runtime
- [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/) shows you that having things already sorted can be useful
- [Rotate Array](https://leetcode.com/problems/rotate-array/) is a great example of how you can take an easy question and make it harder by posing follow up questions (very common in interviews!)
- [Best Time to Buy a Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) lays the groundwork for something magical, dynamic programming
- [Fizz Buzz](https://leetcode.com/problems/fizz-buzz/), while meme'ed, can teach some unlucky folks (including me 7 years ago) that control flow requires some thought

I will add more to this list, but for now I think those 5 are good enough to test some basic Python skills.

### Step 3: Learn Concepts

Often times in programming, we work with *data structures* which are simply objects that have rules for how data is accessed and added. Typically data structures will have an *insertion time*, *deletion time*, and a *lookup time*. For more on data structure basics, go [here](https://www.geeksforgeeks.org/inbuilt-data-structures-python/). Now we can dive into commonly seen basic data structures and good LeetCode questions to make use of them. We often see specific algorithms tied to these structures.

**Important Note**: For each of the data structures, you should implement them locally with classes and everything. To learn more about each of these just use Google. Do this before trying the LeetCode questions, it's a useful exercise and sometimes the interviewer will be impressed with your ability to write `__repr__` dunders.

**Binary Search**

- For learning
  - Read [this](geeksforgeeks.org/binary-search/)
  - [Search Insert Position](https://leetcode.com/problems/search-insert-position/) requires that you implement it
- For a challenge
  - [Search in Rotate Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) teaches you about how modifying algorithms you know will yield dividends

**Sorting**

To be honest, sorting questions are pretty rare. I still can't for the life of me remember the *quick sort* algorithm. It's definitely useful to know, but you can usually get away with just knowing *merge sort*, which IMO is much easier to remember and has the same average runtime. For sorting runtimes, look [here](https://en.wikipedia.org/wiki/Sorting_algorithm). That said some other algorithms like *radix sort* can come in handy, but if you're time strapped I would just learn *merge sort* and move on.

**Linked List**

- For learning
  - Learn about [linked lists](https://www.geeksforgeeks.org/linked-list-set-1-introduction/)
  - [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) will get you familiar with linked lists
  - [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) shows you how to do deletion
  - [Reverse linked list](https://leetcode.com/problems/reverse-linked-list/) is a good exercise regardless, but if you do it recursively I think you have a solid understanding of these
  - [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/) is a good example of the "two pointer" approach which comes up *everywhere*
  - [LRU Cache](https://leetcode.com/problems/lru-cache/) is a super underrated linked list question because it shows why they're useful and also introduces doubly linked lists, but note that this question will take time, refer to [this](https://www.geeksforgeeks.org/doubly-linked-list/)
- For a challenge
  - [Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/) is fun and builds on what you've seen

**Stacks and Queues**

- For learning
  - Learn about the [stack](https://www.geeksforgeeks.org/stack-data-structure-introduction-program/) and [queue](https://www.geeksforgeeks.org/queue-set-1introduction-and-array-implementation/)
  - Check out `Stacks and Queues.ipynb` in this repo for an example Python implementation, note that a node implementation is also valid, and ideally you also have accessors
  - [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) is a classic stack question and often times gets extended to make hard questions
  - [Implement Stack using Queues](https://leetcode.com/problems/implement-stack-using-queues/) is another prototypical question
  - [Design Circular Queue](https://leetcode.com/problems/design-circular-queue/) is a fantastic data structure question which combines many concepts together, also circular buffers are widely used everywhere, the most popular big data processing frameworks use them as an example, refer to [this](https://www.geeksforgeeks.org/circular-linked-list/)
  - [Flatten Nested List Iterator](https://leetcode.com/problems/flatten-nested-list-iterator/) demonstrates the common "flattened list" type problem, but I highly recommend also solving this one with a generator, it's a lot of fun and is also ideal, `yield from` in Python is awesome :)
  - [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/solution/) is fun because there are so many ways of doing it, note that O(n) time with O(1) space is possible!
- For a challenge
  - [Basic Calculator](https://leetcode.com/problems/basic-calculator/) requires good understanding of control flow
  - [Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/) teaches you the `deque`

**Trees**

- For learning
  - Read up on the binary tree intro [here](https://www.geeksforgeeks.org/binary-tree-data-structure/#Introduction) and implement locally
  - Check out `Binary Trees.ipynb` in this repo for an example Python implementation
  - [Search in a Binary Search Tree](https://leetcode.com/problems/search-in-a-binary-search-tree) teaches you about BSTs (not the same as binary trees)
  - [Cousins in a Binary Tree](https://leetcode.com/problems/cousins-in-binary-tree/) shows you how to breadth first search on trees
  - [Merge Two Binary Trees](https://leetcode.com/problems/merge-two-binary-trees/) is a common "comparison" question
  - [N-ary Tree Preorder Traversal](https://leetcode.com/problems/n-ary-tree-preorder-traversal/) teaches you about N-ary trees and pre-order vs in-order vs post-order traversals
  - [Maximum Binary Tree](https://leetcode.com/problems/maximum-binary-tree/) gives you a common framework for recursively operating on trees
  - [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/) is easy for a hard, but it teaches you why recursion is useful
- For a challenge
  - [Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/) teaches you about serialization

**Heaps**

- For learning
  - Read up on them [here](https://www.geeksforgeeks.org/heap-data-structure/) and implement locally
  - [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) is my favourite heap question for learning because there are many ways to solve it, try doing it with a max heap and also doing it with a min heap - note that they have different runtime complexities!
  - [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/) is easy for a hard, so it's a nice ego boost :)
- For a challenge
  - Usually the hardest problems that use heaps require other knowledge and become a part of the solution for some other topic

**Tries**

- For learning
  - Learn about em [here](https://www.geeksforgeeks.org/trie-insert-and-search/)
  - I will note that trie questions become 1000x easier if you remember that tries are a thing
  - [Implement Trie](https://leetcode.com/problems/implement-trie-prefix-tree/) is a good starter
  - [Map Sum Pairs](https://leetcode.com/problems/map-sum-pairs/) shows why tries are useful
- For a challenge
  - [Palindrome Pairs](https://leetcode.com/problems/palindrome-pairs/) is a good display for how multivariate runtime problems have vague optimality

**Dynamic Programming**

This took me a long time to learn properly, and I don't think I really truly understood it until I took an algorithms course at school. Approximately 50% of my LeetCode time is dedicated to DP, and now I feel more comfortable with it than other concepts. Note that a lot of tech companies ask this stuff.

- For learning
  - I haven't found many great resources for DP but I'll defer to the "Basic Concepts" section of the [DP guide](https://www.geeksforgeeks.org/dynamic-programming/#concepts) at Geeks for Geeks
  - For solving these, I recommend having a piece of paper on hand
  - You should try to explicitly state the recurrence
  - If you can't come up with the recurrence then make an intuitive guess as what subproblems you need, and then mock up a memoization table for a simple example input to the problem, and try to infer the recurrence from the pattern in the table
  - [Triangle](https://leetcode.com/problems/triangle/) is one of the simplest DP problems I've seen that I would actually classify as a DP problem
  - [Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/) is another easy one and the board path pattern comes up often
  - [Longest Palandromic Substring](https://leetcode.com/problems/longest-palindromic-substring/) is the *perfect* DP question, I recommend writing up the memo table for this one to get comfortable with that concept
  - [Decode Ways](https://leetcode.com/problems/decode-ways/) is another good one that I've been asked many times, a cool follow up question is how would you implement this with distributed machines that each can only fit part of the input into memory?
  - [Coin Change](https://leetcode.com/problems/coin-change/), getting a bit harder
  - [Unique Binary Search Trees](https://leetcode.com/problems/unique-binary-search-trees/), I have banged my head on this problem many times over the years because it requires looking at it in a certain way
  - [Edit Distance](https://leetcode.com/problems/edit-distance/) this is one of my favorite questions on LeetCode, because I come from an NLP background and this algorithm is super super important. I've used it at work countless times and in a project [here](https://github.com/sarthfrey/slurp)
- For a challenge
  - [Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/) requires other stuff you've learned before
  - [Best Time to Buy and Sell Stock IV](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iv/) makes me cry at night
  - If you have a subscription then try https://leetcode.com/problems/best-meeting-point/ and beat my 36ms solution with a different approach :)

**Graphs**

If you're strapped for time then don't spend much time on this, just learn traversals.

- For learning
  - Learn about [graphs](https://www.geeksforgeeks.org/graph-and-its-representations/), [BFS](https://www.geeksforgeeks.org/breadth-first-search-or-bfs-for-a-graph/, ), [DFS](https://www.geeksforgeeks.org/depth-first-search-or-dfs-for-a-graph/), and [coloring](https://www.geeksforgeeks.org/detect-cycle-direct-graph-using-colors/). If you have time then learn [Djikstra's](https://www.geeksforgeeks.org/dijkstras-shortest-path-algorithm-greedy-algo-7/), [Belman-Ford](https://www.geeksforgeeks.org/bellman-ford-algorithm-dp-23/), and [Floyd-Warshal](https://www.geeksforgeeks.org/floyd-warshall-algorithm-dp-16/), and the tradeoffs between them. You could also dig into [topological sorting](https://www.geeksforgeeks.org/topological-sorting/) and [MSTs](https://www.geeksforgeeks.org/prims-minimum-spanning-tree-mst-greedy-algo-5/).
  - [Max Area of Island](https://leetcode.com/problems/max-area-of-island/) is the perfect simple graph search question
  - [Perfect Squares](https://leetcode.com/problems/perfect-squares/) teaches you that graphs are everywhere
  - [Word Search](https://leetcode.com/problems/word-search/) another prototypical graph question
  - [Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/) introduces the shortest path problem
- For a challenge
  - [Number of Squareful Arrays](https://leetcode.com/problems/number-of-squareful-arrays/) builds of the previous perfect square question well

### Step 4: Consolidate Knowledge

This is the part where you make sure you know your stuff. Previously, you knew what data structure you needed before trying the question. Now you should pick 5-10 random mediums and do them. If you are struggling, then either go back to step 3 or take a breather, read through the solutions, and go back later. Here are some tips for general LeetCode use.

- If you find you are struggling on a certain kind of problem use the "tags" feature in LeetCode to look for specific problem types
- If you have an interview with a specific company coming up, LeetCode compiles a list of questions that specific companies have asked. I would not count on memorizing solutions to those problems - it's unlikely to help, and even if you get lucky then it's not sustainable for the future - so put in the work
- That said, I do recommend looking at those lists to get an idea of what kinds of questions your interviewer might favour, and if you see some good problems on the list for a company you have an interview with then definitely prefer doing those problems over others

### Step 5: Next Steps

Do the following.

- Read more on divide and conquer approach, but tbh if you know merge sort this is easy (often involves assuming parts of the inputs are solved and then merging them, recursively solving each part)
- Read more on greedy algorithm approach (often involves sorting first, and maximizing/minimizing some heuristic)
- Practice more DP/Graphs
- Do heavily liked LeetCode mediums/hards
- LeetCode has great SQL and concurrency questions too, highly recommend trying some
- **Do mock interviews with friends!** Communication is an [underrated skill](https://twitter.com/SarthFrey/status/1175429238473801728), and extra points for practicing on a whiteboard
- Once you learn all this, in the future you need only refresh your knowledge, my friends and I do around 15-20 problems at the beginning of each job search, usually starting ~1 month before we expect any interviews




