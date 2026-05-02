# Informed Search: Best First Search Part-1

> If you ask a lot of traditional people, people who have been working in the AI field for the last 50-60 years, they will say AI is search  
> Search is so important, so central to the field of AI, that you can almost say that AI is search.  
> If you can do search right, you can solve all AI problems, all problems of intelligence  
> I am not going to go as far as saying that  
> Algorithms that we considered DFS, BFS, iterative deepening, beam search and bidirectional search are good algorithms  
> but in the last part of the class we realized that they are not satisfying. They look in all directions  
> They are not guided towards the goal somehow  
> **We need to add guidance and we call it as informed search**. It is an important topic in the field of AI

# Informed Search: Best First Search Part-1
* Based on Slides by Stuart Russell, Richard Korf, Subbarao Kambhampati, and UW-AI faculty

"Intuition, like the rays of the sun, acts only  
in an inflexibly straight line; it can guess  
right only on condition of never diverting  
its gaze; the freaks of chance disturb it."  
-- Honore de Balzac

## Informed(Heuristic) Search
* Idea - be smart about what paths to try

![alt text](image-53.png)

### Blind Search vs. Informed Search
* What's the difference?
* How do we formally specify this?
    * A node is selected for expansion based on an evaluation function that estimates cost to goal.

### General Tree Search Paradigm

```txt
function tree-search(root-node)
    fringe <-- successors(root-node)
    while ( notempty(fringe) )
        {node<--remove-first(fringe) //lowest f value
            state<--state(node)
            if goal-test(state) return solution(node)
            fringe<--insert-all(successors(node),fringe) }
    return failure
end tree-search
```

### General Graph Search Paradigm

```txt
function tree-search(root-node)
    fringe<--successors(root-node)
    explored<--empty
    while ( notempty(fringe) )
        {node<--remove-first(fringe)
            state<--state(node)
            if goal-test(state) return solution(node)
            explored<--insert(node,explored)
            fringe<--insert-all(successors(node),fringe),if node not in explored)
return failure
end tree-search
```
## Best-First Search
* Use an evaluation function f(n) for node n.
* Always choose the node from fringe that has the lowest f value.

