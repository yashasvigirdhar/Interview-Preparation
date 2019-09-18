

“Be fast and well versed in whichever language you code. That will give more time to think and probability of interviewer asking more questions is more if you are done fast. So, chances of clearing increase!”

“I can solve one question at one point of time but to solve when I am stressed during an interview, I really need a good grip so I can drive my own way rather than depending upon my memory”

[https://leetcode.com/problems/house-robber/](https://leetcode.com/problems/house-robber/), [https://leetcode.com/problems/house-robber-ii/](https://leetcode.com/problems/house-robber-ii/), [https://leetcode.com/problems/house-robber-iii/](https://leetcode.com/problems/house-robber-iii/)

Using solution for a simpler problem. A new constraint added to simple problem.

Two Pointer sliding window:

[https://leetcode.com/problems/longest-repeating-character-replacement/](https://leetcode.com/problems/longest-repeating-character-replacement/)

[https://leetcode.com/problems/max-consecutive-ones-iii/](https://leetcode.com/problems/max-consecutive-ones-iii/)

[https://leetcode.com/problems/max-consecutive-ones-ii/](https://leetcode.com/problems/max-consecutive-ones-ii/)

[https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/](https://leetcode.com/problems/longest-substring-with-at-most-k-distinct-characters/)

[https://leetcode.com/problems/longest-substring-without-repeating-characters/](https://leetcode.com/problems/longest-substring-without-repeating-characters/)

[https://leetcode.com/problems/longest-substring-with-at-most-two-distinct-characters/](https://leetcode.com/problems/longest-substring-with-at-most-two-distinct-characters/)

[https://leetcode.com/problems/minimum-size-subarray-sum/](https://leetcode.com/problems/minimum-size-subarray-sum/)

[https://leetcode.com/problems/subarrays-with-k-different-integers/](https://leetcode.com/problems/subarrays-with-k-different-integers/)

[https://leetcode.com/problems/minimum-window-substring/](https://leetcode.com/problems/minimum-window-substring/)

[https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/](https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/)

[https://leetcode.com/problems/degree-of-an-array/](https://leetcode.com/problems/degree-of-an-array/) : But for this problem, sliding window is an overhead. Can be done in a single pass with two hashmaps.

Greedy non-overlapping activities:

[https://leetcode.com/problems/non-overlapping-intervals/](https://leetcode.com/problems/non-overlapping-intervals/)

We have to sort by end time in above. We can’t sort by start time. Example:

(1,11),(12,100),(13,14),(14,15),(15,16).

The problem is we want to remove minimum. If we just want to cover the range,sorting by start would have worked. But here, it’ll result in removing a lot more intervals than min answer.

We don’t want to pick an interval at the start of the processing if it has a very farther end, since it might then overlap with a lot of intervals since it’s length is very large. We want to push these “farther-end” intervals to as right as possible.

Wrong answer here is 3. Right answer is 1.

Interesting follow up: What if we have to remove the max possible number of intervals, such that range covered remains same?

This variant is actually similar to [https://leetcode.com/problems/video-stitching/](https://leetcode.com/problems/video-stitching/). 

[https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/](https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/)

[https://leetcode.com/problems/meeting-rooms/](https://leetcode.com/problems/meeting-rooms/)

[https://leetcode.com/problems/meeting-rooms-ii/](https://leetcode.com/problems/meeting-rooms-ii/)

Range Queries:

[https://leetcode.com/problems/range-sum-query-2d-immutable/](https://leetcode.com/problems/range-sum-query-2d-immutable/)

[https://leetcode.com/problems/range-addition-ii/](https://leetcode.com/problems/range-addition-ii/)

[https://leetcode.com/problems/range-addition/](https://leetcode.com/problems/range-addition/) : V.Good question. [https://leetcode.com/problems/range-sum-query-immutable/](https://leetcode.com/problems/range-sum-query-immutable/)

[https://leetcode.com/problems/range-sum-query-mutable/](https://leetcode.com/problems/range-sum-query-mutable/) : Segment tree.

2d Segment tree : 

[https://leetcode.com/problems/range-sum-query-2d-mutable/](https://leetcode.com/problems/range-sum-query-2d-mutable/)  : to write code.

[https://leetcode.com/problems/range-sum-query-2d-mutable/discuss/75863/Segment-Tree-Solution-in-Java](https://leetcode.com/problems/range-sum-query-2d-mutable/discuss/75863/Segment-Tree-Solution-in-Java)

[http://kaidul.xyz/2d-segment-quad-tree-problem-solving/](http://kaidul.xyz/2d-segment-quad-tree-problem-solving/)

dfs/bfs: finding cycle, connected components:

[https://leetcode.com/problems/number-of-islands/](https://leetcode.com/problems/number-of-islands/)

[https://leetcode.com/problems/graph-valid-tree/](https://leetcode.com/problems/graph-valid-tree/)

[https://leetcode.com/problems/course-schedule/](https://leetcode.com/problems/course-schedule/)

To find cycle,

Undirected graph:

We have to pass parent.

And for each node, only two states are needed. Visited and non-visited.

Directed graph:

3 states for dfs.

1 more permanently marked, so that we don’t start dfs from there again.

1 more marking nodes in current dfs path. -> can directly check if present in stack.

If the current node has an edge to second state, then it’s a cycle. Having an edge to first state might not be a cycle, since that node might not present in current path.

[https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)

Very good problem for applying union find solution. Standard DFS solution can also be used.

Todo : [https://leetcode.com/problems/course-schedule-ii/](https://leetcode.com/problems/course-schedule-ii/) and

[https://leetcode.com/problems/course-schedule-iii/](https://leetcode.com/problems/course-schedule-iii/) 

Dp:

maximize value, adjacent node constraints. Practice for iterative thinking rather than recursion + memoization.

[https://leetcode.com/problems/paint-house/](https://leetcode.com/problems/paint-house/)

[https://leetcode.com/problems/paint-house-ii/](https://leetcode.com/problems/paint-house-ii/) : V.Good question. First intuition comes for O(N*(K^2)) solution. Similar to the above first version.   

[https://leetcode.com/problems/paint-fence/](https://leetcode.com/problems/paint-fence/)

Design:

[https://leetcode.com/problems/logger-rate-limiter/](https://leetcode.com/problems/logger-rate-limiter/)

[https://leetcode.com/problems/design-hit-counter/](https://leetcode.com/problems/design-hit-counter/)

Reservoir Sampling:

[https://gregable.com/2007/10/reservoir-sampling.html](https://gregable.com/2007/10/reservoir-sampling.html)

To generate all the submatrices of a m*n matrix:

for (int rsize = 1; rsize <= m; rsize++) {

      for (int csize = 1; csize <= n; csize++) {

        // submatrices of size (rsize,csize)

        for (int i = 0; i <= m - rsize; i++) {

          for (int j = 0; j <= n - csize; j++) {

            int row1 = i, row2 = i + rsize - 1, col1 = j, col2 = j + csize - 1;

            //submatrix of size (rsize,csize) starting at (row1,col1) and ending at (row2,col2)

Whenever there is an **Integer **in question, consider negative values !!.

**Interval overlap checking:**

Another way to check overlap of 2 intervals is a started with b, or, b started within a.

Keep the intervals sorted,

if the interval started right before the new interval contains the start, or

if the interval started right after the new interval started within the new interval.


```
  floor      ceiling
... |----| ... |----| ...
       |---------|
      s         e
if s < floor.end or e > ceiling.start, there is an overlap.
```


Map.Entry<Integer, Integer> floorEntry = **points**.floorEntry(start);

**if **(floorEntry != **null **&& start < floorEntry.getValue()) **return false**;

Map.Entry<Integer, Integer> ceilingEntry = **points**.ceilingEntry(end);

**if **(ceilingEntry != **null **&& end > ceilingEntry.getKey()) **return false**;

Tree path problems:

[https://leetcode.com/problems/binary-tree-maximum-path-sum/](https://leetcode.com/problems/binary-tree-maximum-path-sum/)

[https://leetcode.com/problems/longest-univalue-path/](https://leetcode.com/problems/longest-univalue-path/)  : this is also good.

[https://leetcode.com/problems/path-sum/](https://leetcode.com/problems/path-sum/)

[https://leetcode.com/problems/path-sum-ii/](https://leetcode.com/problems/path-sum-ii/)

[https://leetcode.com/problems/path-sum-iii/](https://leetcode.com/problems/path-sum-iii/) : good question. tests prefixSum technique + tree traversal

Bit Manipulation:

[https://leetcode.com/problems/single-number-ii/](https://leetcode.com/problems/single-number-ii/)

[https://leetcode.com/problems/single-number-iii/](https://leetcode.com/problems/single-number-iii/)

N & (N-1) : to unset the leftmost set bit

N & ~(N-1) : to get the leftmost set bit.

Decent explanation for figuring out that time complexity is exponential:

[https://leetcode.com/problems/word-break/discuss/169383/The-Time-Complexity-of-The-Brute-Force-Method-Should-Be-O(2n)-and-Prove-It-Below](https://leetcode.com/problems/word-break/discuss/169383/The-Time-Complexity-of-The-Brute-Force-Method-Should-Be-O(2n)-and-Prove-It-Below)

[https://leetcode.com/problems/word-break-ii/discuss/44167/My-concise-JAVA-solution-based-on-memorized-DFS/43432](https://leetcode.com/problems/word-break-ii/discuss/44167/My-concise-JAVA-solution-based-on-memorized-DFS/43432)

V.Good Q. Extension of 2 sum:

[https://leetcode.com/problems/pairs-of-songs-with-total-durations-divisible-by-60/](https://leetcode.com/problems/pairs-of-songs-with-total-durations-divisible-by-60/)

Design:

Very Imp: [https://leetcode.com/problems/lru-cache/](https://leetcode.com/problems/lru-cache/)

[https://leetcode.com/problems/moving-average-from-data-stream](https://leetcode.com/problems/moving-average-from-data-stream)

[https://leetcode.com/problems/design-hashmap](https://leetcode.com/problems/design-hashmap)

Very imp: [https://leetcode.com/problems/serialize-and-deserialize-binary-tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree)

[https://leetcode.com/problems/logger-rate-limiter/](https://leetcode.com/problems/logger-rate-limiter/)

[https://leetcode.com/problems/trapping-rain-water/](https://leetcode.com/problems/trapping-rain-water/)

Similar concept to histogram ^ . 

[https://leetcode.com/problems/circular-array-loop/](https://leetcode.com/problems/circular-array-loop/)

One simple solution is dfs^.

Other interesting solution is slow-fast pointer technique that we use in linked list.

Similar to dfs, keep marking the visited nodes and their results. And start only from unvisited notes.

Linkedin me jump distance is fixed 1 unit, isme the distance is variable, that’s it.

[https://leetcode.com/problems/maximum-width-ramp/](https://leetcode.com/problems/maximum-width-ramp/)

Problem to solve : for every index, we need to find the farthest** larger element on its right**.

[https://medium.com/@yashgirdhar/maximum-width-ramp-problem-b1687a40d0bf](https://medium.com/@yashgirdhar/maximum-width-ramp-problem-b1687a40d0bf) 

[https://leetcode.com/problems/majority-element/](https://leetcode.com/problems/majority-element/)

Interesting solutions to this:



*   Choosing randomized index and checking count
*   Divide and conquer
*   Moore’s voting algorithm
    *   This will report an element even if it’s not majority. So if we don’t have this guarantee that there will always be a majority element in the array, we need to do a second pass to verify that element returned from the first pass is actually a majority element.
    *   **no algorithm can correctly distinguish the cases when an item is just above or just below the threshold in a single pass without using a large amount of space (linear space). This is proven. **
*   Bit Manipulation. Keep a bits array of size 32. Iterate over original array and for each element, increase the count of bit positions for which it has 1. At the end, the majority element will be formed by combining all the bits where count is > n/2.

[https://leetcode.com/problems/majority-element-ii/](https://leetcode.com/problems/majority-element-ii/) 

Uses concept of moore’s voting.

[https://leetcode.com/problems/pancake-sorting/](https://leetcode.com/problems/pancake-sorting/)

Similar to selection sort.

Game Theory



*   Minimax:
    *   [https://leetcode.com/problems/can-i-win/](https://leetcode.com/problems/can-i-win/)

    [https://leetcode.com/problems/can-i-win/discuss/95277/Java-solution-using-HashMap-with-detailed-explanation](https://leetcode.com/problems/can-i-win/discuss/95277/Java-solution-using-HashMap-with-detailed-explanation) : nice explanation of choosing state and it’s representation.


    [https://leetcode.com/problems/can-i-win/discuss/155321/DFS-with-Memorization-Java-with-Explanations](https://leetcode.com/problems/can-i-win/discuss/155321/DFS-with-Memorization-Java-with-Explanations) : same ^.

*   [https://leetcode.com/problems/stone-game/](https://leetcode.com/problems/stone-game/)

In Minimax the two players are called maximizer and minimizer. The **maximizer** tries to get the highest score possible while the **minimizer** tries to do the opposite and get the lowest score possible.

Easy level: 

[https://leetcode.com/problems/nim-game/](https://leetcode.com/problems/nim-game/)

Basic concept is:

There are states. Each state is either losing or winning. If you land on winning state, you win. If you land on losing state, you lose.

You are on state s. You can make n moves, each transforms the state of the game to p1,p2,p3...pn.

Now, if any of pi is a losing state, the current state s becomes winning state. Why? Since you’ll optimally and try to land your opponent in a losing state.

We build the tree bottom up. We know the state of the leaves, whether they are winning or losing. And then, we compute the value of intermediate states.

If all of the pi’s state are winning states, no matter what move you make, your opponent will land in a winning state.

[https://leetcode.com/problems/minimum-cost-for-tickets/](https://leetcode.com/problems/minimum-cost-for-tickets/)

Very good problem for dp iterative thinking. Dp + memoization is decent.

[https://leetcode.com/problems/delete-node-in-a-bst/](https://leetcode.com/problems/delete-node-in-a-bst/) : Good tree question. Good if done in one iteration. And, has edge cases.

[https://leetcode.com/problems/shopping-offers/](https://leetcode.com/problems/shopping-offers/) : very good problem for dfs + backtracking thinking.

[https://leetcode.com/problems/paint-fence/](https://leetcode.com/problems/paint-fence/) : Very good problem for dp state thinking. Listed as easy on leetcode but not at all easy.

[https://leetcode.com/problems/longest-palindromic-subsequence/](https://leetcode.com/problems/longest-palindromic-subsequence/) : Simple with O(n^2) space. But space can be reduced to O(n). Still don’t understand how :P

[https://leetcode.com/problems/longest-palindromic-subsequence/discuss/194748/Java-DP-From-O(n2)-to-O(n)-space-with-only-one-array](https://leetcode.com/problems/longest-palindromic-subsequence/discuss/194748/Java-DP-From-O(n2)-to-O(n)-space-with-only-one-array)

[https://leetcode.com/problems/kth-largest-element-in-an-array/](https://leetcode.com/problems/kth-largest-element-in-an-array/)

For revising quickselect algorithm ^. One imp things is always shuffling the array before processing runtime reduces the runtime by a large margin. Avg runtime is O(n).

Min heap solution also exists with O(Nlogk) solution.

[https://leetcode.com/problems/top-k-frequent-elements/](https://leetcode.com/problems/top-k-frequent-elements/)

Very good question to learn the concept of buckets.

If we have to store some information for numbers within a fixed range, let’s say 0 to n.

IN SORTED ORDER, we can go for buckets array.

Adding new information is O(1). Then, we can iterate the array in sorted order as our key is the array index. So you get sorted data in o(1), just the cost of traversing.WOW!

Other solutions to this problem: 

map + max heap

Map + min heap (better).

[https://leetcode.com/problems/sparse-matrix-multiplication/](https://leetcode.com/problems/sparse-matrix-multiplication/) :

Sparse matrix can have good number of real world applications. So good to revise this.

[https://leetcode.com/problems/sum-of-root-to-leaf-binary-numbers/](https://leetcode.com/problems/sum-of-root-to-leaf-binary-numbers/discuss/270025/JavaC%2B%2BPython-Recursive-Solution) 

A very good way to convert base 2 to base 10, when iterating from MSB to LSB.

Initialize n to 0, and then while iterating, multiple the previous value by 2 and add current bit value.	

[https://leetcode.com/problems/design-phone-directory/](https://leetcode.com/problems/design-phone-directory/):

Data structure for:



*   Reserve an element
*   Release an element
*   Get next available element

All operations in O(1).

One application of above is parking lot !

[https://leetcode.com/problems/https://leetcode.com/problems/design-phone-directory/discuss/85335/Java-AC-solution-with-Bitset-and-efficient-get()-%2B-comments/](https://leetcode.com/problems/design-phone-directory/) : Interesting solution using bitset.

[https://leetcode.com/problems/game-of-life/discuss/73223/Easiest-JAVA-solution-with-explanation](https://leetcode.com/problems/game-of-life/discuss/73223/Easiest-JAVA-solution-with-explanation)


<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: Definition &darr;&darr; outside of definition list. Missing preceding term(s)? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


: Very important technique.

An integer is initially 0 or 1 and might switch to either 0 or 1. We need to represent both the states (old and new) in a single integer and should be able to retrieve either old or new state at any point of time.

[https://leetcode.com/problems/number-of-subarrays-with-bounded-maximum/](https://leetcode.com/problems/number-of-subarrays-with-bounded-maximum/)


<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: Definition &darr;&darr; outside of definition list. Missing preceding term(s)? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


: very important technique of calculating the subarrays.

Array given, have to find the number of subarrays. Numbers in the subarray follow certain conditions.

There are three types of elements:



*   That can’t be included in the subarray at all
*   That may/may not be included in the subarray but that don’t fulfill all the requirement of the subarray. Basically they do nothing, just increase the length of subarray.
*   That are essential for the subarray. At least one of these elements should be included. Multiple can be there.

Let’s say an array has only 2s, 0s, and 1s. 2s are the first type of element, 0s are second type and 1s are third type.

Give me the count of all the qualified subarrays.

[https://leetcode.com/problems/count-complete-tree-nodes/](https://leetcode.com/problems/count-complete-tree-nodes/)

Very important technique : for counting nodes in a complete binary tree.

A pattern is given in the tree, that it is complete. We use it to reduce our problem space at each step.

[https://leetcode.com/problems/find-all-duplicates-in-an-array/](https://leetcode.com/problems/find-all-duplicates-in-an-array/):

Again, important technique.

Need to store a different state at array index with the current number.

You negate the number if it has been visited. And when consuming the number, take the absolute value.

[https://leetcode.com/problems/unique-letter-string/](https://leetcode.com/problems/unique-letter-string/)

**Imp technique:**

In any questions, when we are forming numbers from a stream, _starting from MSB_.

Let’s say we have formed number from first k digits. Now, when the next digit arrives,

We have to left shift this complete number by 1. This “shift” can be taken into account by

Multiplying the entire number by the base of the number system. For eg. if we are talking about binary numbers, I’ll multiple the complete number by 2, if we are talking about decimal numbers, I’ll multiple by complete no by 10 and similarly 16 in case of hexadecimal numbers.

And then, we add to it the next digit encountered. So, the equation that comes up is:

**_Num = num*(base) + next digit._**

Questions that use this technique:

[https://leetcode.com/problems/smallest-integer-divisible-by-k/](https://leetcode.com/problems/smallest-integer-divisible-by-k/)

[https://leetcode.com/problems/binary-prefix-divisible-by-5/](https://leetcode.com/problems/binary-prefix-divisible-by-5/)

In second question, one more modular arithmetic technique is being used:

(a+b)%k = a%k + b%k.

So, Num%k = ((num*base)%k + nextDigit%k)%k.

So basically, you just store the remainder in num, not the original number. As that’s sufficient to tell you, what will the remainder for next number.

**Generating Permutation/Subsets:**

For generating subsets, just initialize a binary number with num of digits equal to the length of the array. Iterate this binary number from 0 to all 1s, and in each iteration, pick numbers in the current subset where the bit position is 1.

[https://leetcode.com/problems/subsets/](https://leetcode.com/problems/subsets/)

For generating string permutation,



*   Start from the first element
*   swap it with every other element including itself.
*   Proceed to next element for each iteration.
*   Repeat these steps for each index.

[https://leetcode.com/problems/permutations/](https://leetcode.com/problems/permutations/)

Now, if the string has duplicates and we want only unique permutations at the end,

In the second step, when swapping with other element, make sure that an element is considered only once as the starting element.

Example:

1,2,3,1 : No need to swap the first one with the last 1. They’ll produce identical permutations.

[https://leetcode.com/problems/permutations-ii/](https://leetcode.com/problems/permutations-ii/)

[https://leetcode.com/problems/minimum-number-of-refueling-stops/](https://leetcode.com/problems/minimum-number-of-refueling-stops/):

Very good dp problem. Seems easy at first. 

This is NOT same as jump game II !!. In jump game, at each step, we choose the next best answer and then discard other candidate solutions.

In this question, you never discard a solution. Every candidate solution might be used sometime in future.

So, you keep accumulating all the candidate solutions and then use them at the apt time if required. The important point here is accumulating !!. in jump game, I don’t accumulate. I just choose 1 out of k options and discard others.

So this is a separate type of problem.

When exactly you add a candidate to the probable solution set and when exactly you remove it from the set to make it a part of actual solution. These are important.

When to add is trivial here. The real game is when do you remove and make it a part of the solution.

[https://leetcode.com/problems/sum-of-subarray-minimums/](https://leetcode.com/problems/sum-of-subarray-minimums/):

Very good question.

Imp things:



*   Concepts for generating all the continuous subarrays of an array should be deeply ingrained in your mind. 
    *   How exactly do you generate? (iterating over each index and computing subarrays ending at that index).
    *   How many subarrays are you generating at a particular index i? i+1
    *   Of all those subarrays, how many times an element at index j (j<i) will be part of them? j+1
    *   Using the above information, you should be able to tell for a particular element i, how many subarrays will it be a part of? ((n-i)*i+1)
    *   Now that’s the total number of subarrays of this element, now we need to calculate that for how many subarrays, this element actually contributes to answer, i.e. it is minimum. For this, use info in point two.
*   Generating nearest smaller element for each index of the array, in O(n). stack based solution. For this question, we need to generate for both sides.

Union-Find data structure:



*   Cycle detection in both undirected and directed graphs
*   Determining the no of components

[https://leetcode.com/problems/odd-even-jump/](https://leetcode.com/problems/odd-even-jump/)

Very important technique for:

In an array, for each index, find smallest of all elements on the right which are >= current element.

Find j for i, such that A[j] is smallest of all A[k]’s where A[k] >= A[i] and k>i.

It’s not straightforward. On the lines of popular stack-based solution to find nearest smaller element on right but needs one more trick.

So here, we know that we want just bigger number than the current so we need to check through the complete remaining array. And after some calculation, we observe that ans to ith index can NOT be derived using result of i-1th or i+1th index.

So stop deriving the o(n) stack based solution on original array. This is imp.

Next, what can be done. Think if it’d help if we had the numbers sorted. In that case, for each i, the next number is the ceiling to it. But, that no might appear behind i in the original array. So, for each i, you keep going right until you find a number whose original index is > i.

Now, think again for a stack based solution.

Other important technique is, we know i can only jump to a single idx j. So if we have the result for j, we have the result for i. So keep calculating and caching the result from right.

[https://leetcode.com/problems/binary-search-tree-to-greater-sum-tree/](https://leetcode.com/problems/binary-search-tree-to-greater-sum-tree/)


<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: Definition &darr;&darr; outside of definition list. Missing preceding term(s)? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


: one more example of technique:

Whenever a problem for BST is given, try to think of solving the same thing in a sorted array.

Shortest Path problem:

ALWAYS go for BFS.



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Algo-notes0.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Algo-notes0.jpg "image_tooltip")


Generating subsets:

[https://leetcode.com/submissions/detail/224866009/](https://leetcode.com/submissions/detail/224866009/)

Avoiding duplicates:

[https://leetcode.com/submissions/detail/224866626/](https://leetcode.com/submissions/detail/224866626/)

[https://leetcode.com/problems/partition-equal-subset-sum/](https://leetcode.com/problems/partition-equal-subset-sum/)

[https://leetcode.com/problems/target-sum/](https://leetcode.com/problems/target-sum/)

[https://leetcode.com/problems/coin-change-2/](https://leetcode.com/problems/coin-change-2/)

[https://leetcode.com/problems/coin-change/](https://leetcode.com/problems/coin-change/)

Vgood: [https://leetcode.com/problems/last-stone-weight-ii/](https://leetcode.com/problems/last-stone-weight-ii/)

All of the above questions can be solved using this approach:



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Algo-notes1.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Algo-notes1.jpg "image_tooltip")


graph coloring:

[https://leetcode.com/problems/flower-planting-with-no-adjacent/](https://leetcode.com/problems/flower-planting-with-no-adjacent/)

[https://leetcode.com/problems/possible-bipartition/](https://leetcode.com/problems/possible-bipartition/)

Can be done using either BFS or DFS. DFS seems more elegant.

If it’s guaranteed that a solution exists, we can greedily assign colors.

Same concept:

[https://leetcode.com/problems/rearrange-string-k-distance-apart/](https://leetcode.com/problems/rearrange-string-k-distance-apart/)

[https://leetcode.com/problems/reorganize-string/](https://leetcode.com/problems/reorganize-string/)

[https://leetcode.com/problems/task-scheduler/](https://leetcode.com/problems/task-scheduler/)

Follow greedy approach. Take the one with maximum occurrence.

Implementation is also important here.

Put elements in PQ. and then repeatedly loop to fill k spaces till the time PQ is empty.

[https://leetcode.com/problems/shortest-path-visiting-all-nodes](https://leetcode.com/problems/shortest-path-visiting-all-nodes) : very good question for using BFS !. 

Whenever there is a shortest path, always think of BFS first.

LCA techniques:



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Algo-notes2.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Algo-notes2.jpg "image_tooltip")


Problem which utilises the second technique:

[https://leetcode.com/problems/lowest-common-ancestor-of-deepest-leaves/](https://leetcode.com/problems/lowest-common-ancestor-of-deepest-leaves/)

Prefix sum technique: more questions :

[https://leetcode.com/problems/longest-well-performing-interval/](https://leetcode.com/problems/longest-well-performing-interval/)

[https://leetcode.com/problems/contiguous-array/](https://leetcode.com/problems/contiguous-array/)

[https://leetcode.com/problems/linked-list-cycle-ii/](https://leetcode.com/problems/linked-list-cycle-ii/)

Slow and fast pointer technique to detect cycle. This concept is used at other places too:

[https://leetcode.com/problems/find-the-duplicate-number/](https://leetcode.com/problems/find-the-duplicate-number/)

A type of DP ( I couldn’t think of the solution myself, after spending a lot of time).

You have to partition things based on a constraint and optimize for a value in this process.

[https://leetcode.com/problems/filling-bookcase-shelves](https://leetcode.com/problems/filling-bookcase-shelves)

[https://leetcode.com/problems/partition-array-for-maximum-sum/](https://leetcode.com/problems/partition-array-for-maximum-sum/)

Still not able to grasp the logic completely.

[https://leetcode.com/problems/partition-array-for-maximum-sum/discuss/299443/Java-O(NK).-Faster-than-99.82.-Less-memory-than-100.-With-Explanation](https://leetcode.com/problems/partition-array-for-maximum-sum/discuss/299443/Java-O(NK).-Faster-than-99.82.-Less-memory-than-100.-With-Explanation).

Very good explanation of the subproblem structure.

[https://leetcode.com/problems/encode-and-decode-tinyurl/](https://leetcode.com/problems/encode-and-decode-tinyurl/)

Imp question.

Some basic problems:

Serialization and serialization of trees

Encoding and decoding of strings

Finding duplicate files in a system.

[https://leetcode.com/problems/find-duplicate-file-in-system/](https://leetcode.com/problems/find-duplicate-file-in-system/)

todo:

[https://leetcode.com/problems/remove-invalid-parentheses/](https://leetcode.com/problems/remove-invalid-parentheses/)

[https://leetcode.com/problems/median-of-two-sorted-arrays/](https://leetcode.com/problems/median-of-two-sorted-arrays/)

[https://leetcode.com/problems/push-dominoes/](https://leetcode.com/problems/push-dominoes/)

[https://leetcode.com/problems/split-array-largest-sum/](https://leetcode.com/problems/split-array-largest-sum/)

[https://leetcode.com/problems/binary-tree-longest-consecutive-sequence/](https://leetcode.com/problems/binary-tree-longest-consecutive-sequence/)

[https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/](https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/)

[https://leetcode.com/problems/daily-temperatures/](https://leetcode.com/problems/daily-temperatures/)

[https://leetcode.com/problems/find-the-closest-palindrome/](https://leetcode.com/problems/find-the-closest-palindrome/)

[https://leetcode.com/problems/design-log-storage-system/](https://leetcode.com/problems/design-log-storage-system/)

[https://leetcode.com/problems/design-in-memory-file-system/](https://leetcode.com/problems/design-in-memory-file-system/)


<!-- Docs to Markdown version 1.0β17 -->

