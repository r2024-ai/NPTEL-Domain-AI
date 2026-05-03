# What led up to Iterative Deepening A* Algorithm?

Iterative Deepening A* (**IDA***) didn’t come out of nowhere—it was invented to fix a very specific weakness in A*.

Let’s trace the *real problem → idea → solution* path.


## 1. A* Was Great… But Had a Serious Flaw

You already know A* uses:

f(n)=g(n)+h(n)

It works beautifully because:

* It finds optimal paths
* It’s guided by heuristics

👉 **But the problem:**
A* stores **all generated nodes in memory (OPEN + CLOSED lists)**

### Why this becomes a problem

* Memory grows **exponentially**
* For large problems (like puzzles, pathfinding, AI planning), RAM gets exhausted
* Even if the solution exists, A* may fail due to **memory limits**, not logic

👉 This is called the **state-space explosion problem**

## 2. Earlier Idea: Iterative Deepening (IDDFS)

Before IDA*, people already had a trick:

### Iterative Deepening DFS (IDDFS)

* Run DFS with depth limit = 1
* Then 2, then 3, then 4…
* Repeat until goal found

✔ Uses **very little memory (like DFS)**
✔ Still finds optimal solution (like BFS for unit cost)

👉 Key idea:

> “Search repeatedly, but with increasing limits instead of storing everything.”

## 3. The Key Insight 💡

Researchers thought:

> “Can we apply the *same iterative idea* to A*?”

Instead of:

* Limiting **depth**

We limit:

* **f-cost (g + h)**

## 4. Birth of IDA*

Instead of storing all nodes, IDA*:

1. Sets a threshold:

   * ( \text{threshold} = f(\text{start}) )

2. Performs DFS, but:

   * Only explores nodes where
     [
     f(n) \le \text{threshold}
     ]

3. If goal not found:

   * Increase threshold to next minimum exceeded value
   * Repeat search

### Visual Intuition

Think of it like:

* Expanding a boundary outward based on **cost contours**, not depth

## 5. Why IDA* Was Created

### Core Motivation

| Problem in A*                 | IDA* Solution                |
| ----------------------------- | ---------------------------- |
| Huge memory usage             | Uses DFS → very low memory   |
| Stores all nodes              | Stores only current path     |
| Not scalable for big problems | Works for large state spaces |

## 6. Trade-Off

IDA* is not “free improvement”

* ✔ Memory efficient
* ❌ Repeats work (same nodes explored multiple times)
* ❌ Can be slower than A*

👉 So:

* A* = **time efficient, memory heavy**
* IDA* = **memory efficient, time heavier**

## 7. Evolution Summary

| Step            | Idea                                 |
| --------------- | ------------------------------------ |
| A*              | Optimal + heuristic but memory-heavy |
| IDDFS           | Memory-efficient via iteration       |
| 💡 Combine both | Apply iteration on f-cost            |
| IDA*            | A*-like optimality with DFS memory   |

## Final Intuition

If A* is like:

> “Keep everything in memory and choose best”

Then IDA* is like:

> “Try within a cost limit, then gradually allow more”
