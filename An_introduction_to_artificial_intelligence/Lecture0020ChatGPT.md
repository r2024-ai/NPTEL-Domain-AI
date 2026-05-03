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

# ==========================================================

# What is weighted A* algorithm

**Weighted A*** is a variation of A* designed to be **faster**, even if that means giving up guaranteed optimality.

## 1. Start from Regular A*

Normal A* uses:

f(n)=g(n)+h(n)

* ( g(n) ): cost so far
* ( h(n) ): estimated cost to goal

It balances both → gives **optimal path**

## 2. The Problem with A*

Even though A* is optimal:

* It can be **slow**
* It explores many nodes to ensure the best path

👉 In real-world systems (games, robotics, large maps),
sometimes **speed matters more than perfect optimality**

## 3. Idea Behind Weighted A*

> “What if we trust the heuristic more and push the search toward the goal faster?”

So we **increase the importance of ( h(n) )**.

## 4. Weighted A* Formula

f(n)=g(n)+w\cdot h(n),\quad w>1

* ( w ): weight (usually > 1)
* Higher ( w ) → more greedy behavior

## 5. Intuition

Think of navigation:

* A*: “Let’s carefully consider distance traveled and estimated remaining distance”
* Weighted A*: “Let’s **rush toward the goal**, even if path might not be perfect”

## 6. Visual Behavior

* A* explores broadly → finds best path
* Weighted A* goes more directly → explores fewer nodes

## 7. What Changes with Weight?

### When ( w = 1 )

* Same as A*

### When ( w > 1 )

* Faster
* Less node expansion
* Not guaranteed optimal

### When ( w \gg 1 )

* Becomes similar to **Greedy Best-First Search**

## 8. Trade-Off

| Aspect     | A*       | Weighted A*       |
| ---------- | -------- | ----------------- |
| Optimality | ✅ Yes    | ❌ Not guaranteed  |
| Speed      | ❌ Slower | ✅ Faster          |
| Memory     | ❌ High   | ✅ Lower (usually) |
| Behavior   | Balanced | Goal-directed     |

## 9. Important Property

Weighted A* is often **bounded suboptimal**:

* If ( w = 2 ),
  solution cost ≤ **2 × optimal cost**

👉 So you can control:

* **Speed vs Accuracy** using ( w )

## 10. Where It’s Used

* Game AI (fast decisions matter more than perfect ones)
* Robotics (real-time planning)
* Route planning with time constraints

## Final Intuition

* A* = “Be correct”
* Weighted A* = “Be fast, close enough is fine”


