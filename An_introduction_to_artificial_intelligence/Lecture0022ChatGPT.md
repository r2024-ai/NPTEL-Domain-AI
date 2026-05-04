# What is admissible Heuristic - First Priniples

## 1. Start with the core problem: search

Imagine you are trying to go from a **start state** to a **goal state**.

Example:

* You are in city A, want to reach city B
* There are many possible paths
* Each path has a **cost** (distance, time, money)

Your goal:
👉 Find the **least-cost path**

---

## 2. How do we search efficiently?

A brute-force way:

* Try all paths → pick the best

But that’s too slow.

So we use **informed search**, where we guide the search using a *guess*.

This is where a **heuristic** comes in.

---

## 3. What is a heuristic (h(n))?

A heuristic is:

> A function that estimates how far you are from the goal.

Formally:

* ( h(n) ) = estimated cost from node ( n ) to goal

Example:

* Straight-line distance from your current city to destination

---

## 4. The key question

If we are using a *guess*, how do we make sure we still get the **optimal (best) path**?

This is where **admissibility** comes in.

---

## 5. First principle idea: “Never be over-optimistic in the wrong way”

Think like this:

* If your estimate says:

  > "Remaining cost is 10"

* But actual cost is:

  > 8 → OK (you overestimated? actually this is bad)
  > 12 → OK (you underestimated)

Wait, let's think carefully.

---

## 6. What can go wrong?

If your heuristic **overestimates**, e.g.:

* Actual cost = 10
* Heuristic says = 20

Then:
👉 You might avoid the correct path because it *looks expensive*

This breaks optimality.

---

## 7. Safe condition

To **never miss the optimal path**, your heuristic must satisfy:

> It should **never overestimate** the true cost.

Formally:

[
h(n) \leq h^*(n)
]

where:

* ( h(n) ) = heuristic estimate
* ( h^*(n) ) = true minimum cost to goal

---

## 8. Definition (now it makes sense)

An **admissible heuristic** is:

> A heuristic that never overestimates the true cost to reach the goal.

---

## 9. Intuition (very important)

Think of it like this:

👉 Admissible heuristic = **optimistic guess**

* It can say:

  * “You need at least 5 steps” (actual might be 8) ✅
* But never:

  * “You need 15 steps” when actual is 8 ❌

---

## 10. Why “optimistic” works?

Because:

* If you underestimate → you still explore good paths
* If you overestimate → you might skip the best path

So admissibility ensures:

👉 **You never ignore the optimal solution**

---

## 11. Real example

Suppose you're navigating on a map:

* Heuristic = straight-line distance (Euclidean distance)

This is admissible because:

👉 You can never reach faster than a straight line
(roads can only make it longer, not shorter)

---

## 12. Connection to algorithms

In algorithms like **A* search algorithm**:

We use:

[
f(n) = g(n) + h(n)
]

where:

* ( g(n) ) = cost so far
* ( h(n) ) = estimated remaining cost

If ( h(n) ) is admissible:

👉 A* is guaranteed to find the **optimal solution**

---

## 13. One-line summary

👉 **Admissible heuristic = a heuristic that never overestimates the true cost, ensuring optimal solutions in search.**

