# LeetCode Course

A guide to crushing tech interviews. At some point I will be expanding upon concepts in this general guide, but I'm quickly typing this up now to help some friends.

### How to use this Doc

At any step, feel free to continue to any later step. That said, this stuff is inherently a graph of knowledge and so it is not well presented linearly. However, at the very least, you can trust that following this guide in a linear fashion will be a valid progression strategy.

### Step 0: Requirements

You will need:

1. A [LeetCode](https://leetcode.com/) account, ideally with premium (you can share with friends)
2. The latest version of Python, downloadable [here](https://www.python.org/)
3. This doc + internet connection

### Step 1: Learn Python

What:

- Basic syntax (variables math, strings, lists, sets, dicts, printing, functions, classes, loops, ...)
- Runtime + Space complexity concepts, [here](https://medium.com/karuna-sehgal/a-simplified-explanation-of-the-big-o-notation-82523585e835) or [here](https://stackabuse.com/big-o-notation-and-algorithm-analysis-with-python-examples/)
- I also recommend you learn generators, coroutines, list comprehension, useful builtins (sorted, breakpoint, zip, enumerate, etc) as knowing this can impress interviewers but more importantly, make you more effective at coding

How:

- If you have very limited programming experience start [here](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers), otherwise continue
- I start learning any language by browsing its [Learn X in Y](https://learnxinyminutes.com/), check out the one for Python [here](https://learnxinyminutes.com/docs/python3/)
- [https://stackoverflow.com/](https://stackoverflow.com/)
- [https://www.google.com/](https://www.google.com/)
- A realistic [guide](https://realpython.com/async-io-python/) to AsyncIO in Python3.7+

### Step 2: Jump into Leetcode

At this point, many people would encourage you to start reading up about algorithms and data structures. If you want to to that then skip to the next step, but otherwise I recommend jumping into LeetCode and doing a few *"Easy"* difficulty level problems in order to give you a feel for it. Whatever your approach is to picking problems to try, I highly recommend avoiding ones that have a high proportion of thumbs-down's to thumbs-up's. Here is a list of simple problems.

- [Two Sum](https://leetcode.com/problems/two-sum/) will teach you about how using data structures can often improve runtime
- [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/) shows you that having this sorted can be useful
- [Rotate Array](https://leetcode.com/problems/rotate-array/) is a great example of how you can take an easy question and make it harder by posing follow up questions (very common in interviews!)
- [Best Time to Buy a Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) lays the groundwork for thinking about problems in a magical way, called "dynamic programming"
- [Fizz Buzz](https://leetcode.com/problems/fizz-buzz/), while meme'ed, can teach some unlucky folks (including me 7 years ago) that control flow requires some thought

I will add more to this list, but for now I think those 5 are good enough to test some basic Python skills.

### Step 3: Learn Concepts

Often times in programming, we work with *data structures* which are simply objects that have rules for how data is accessed and added. Typically data structures will have an *insertion time*, *deletion time*, and a *lookup time*. For more on data structure basic, go [here](https://www.geeksforgeeks.org/inbuilt-data-structures-python/). Now we can dive into commonly seen basic data structures and good LeetCode questions to make use of them. We often see specific algorithms tied to each of these structures.

**Important Note**: For each of these data structures, you should implement them locally with classes and everything. To learn more about each of these just use Google. Do this before trying the LeetCode questions.

**Linked List**

- [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) will get you familiar with linked lists
- [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) shows you how to do deletion
- [Reverse linked list](https://leetcode.com/problems/reverse-linked-list/) is a good exercise regardless, but if you do it recursively I think you have a solid understanding of these
- [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/) is a good example of the "two pointer" approach which comes up *everywhere*
- [LRU Cache](https://leetcode.com/problems/lru-cache/) is a super underrated linked list question because it shows why they're useful and also introduces doubly linked lists, but note that this question will take time

**Stacks and Queues**

- [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) is a classic stack question and often times gets extended to make hard questions
- [Implement Stack using Queues](https://leetcode.com/problems/implement-stack-using-queues/) is another prototypical question
- [Design Circular Queue](https://leetcode.com/problems/design-circular-queue/) is a fantastic data structure question which combines many concepts together, also circular buffers are widely used everywhere, the most popular big data processing frameworks use them as an example
- [Flatten Nested List Iterator](https://leetcode.com/problems/flatten-nested-list-iterator/) demonstrates the common "flattened list" type problem, but I highly recommend also solving this one with a generator, it's a lot of fun and is also ideal, `yield from` in Python is awesome :)
- [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/solution/) is fun because there are so many ways of doing it, note that O(n) time with O(1) space is possible!

**Trees**

- [Search in a Binary Search Tree](https://leetcode.com/problems/search-in-a-binary-search-tree) teaches you about BSTs (not the same as binary trees)
- [Cousins in a Binary Tree](https://leetcode.com/problems/cousins-in-binary-tree/) shows you how to breadth first search on trees
- [Merge Two Binary Trees](https://leetcode.com/problems/merge-two-binary-trees/) is a common "comparison" question
- [N-ary Tree Preorder Traversal](https://leetcode.com/problems/n-ary-tree-preorder-traversal/) teaches you about N-ary trees and pre-order vs in-order vs post-order traversals
- [Maximum Binary Tree](https://leetcode.com/problems/maximum-binary-tree/) gives you a common framework for recursively operating on trees
- [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/) is easy for a hard, but it teaches you why recursion is useful

**Graphs**

Learn pseudocode for DFS, BFS, Belman-Ford, and Djikstra's first. Also remember that sometimes you can solve the question by reversing all the edges in the graph.

- [Max Area of Island](https://leetcode.com/problems/max-area-of-island/) is the perfect simple graph search question
- [Perfect Squares](https://leetcode.com/problems/perfect-squares/) teaches you that graphs are everywhere
- [Word Search](https://leetcode.com/problems/word-search/) another prototypical graph question
- [Shortest Path in Binary Matrix](https://leetcode.com/problems/shortest-path-in-binary-matrix/) introduces the shortest path problem

**Next Steps**

Learn the following.

- Divide and conquer approach (often involves assuming parts of the inputs are solved and then merging them, recursively solving each part)
- Greedy algorithm approach (often involves sorting first, and maximizing/minimizing some heuristic)
- Tries (implement an autocomplete system)
- Dynamic Programming, try https://leetcode.com/problems/best-meeting-point/ and beat my 36ms solution with a different approach c:




