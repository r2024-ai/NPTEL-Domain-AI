# Informed Search: Iterative Deepening A* and Depth First Branch & Bound Part-5

![alt text](image-73.png)

* For real problems we implement A* Algorithm

## Depth First Branch and Bound Algorithm

![alt text](image-74.png)

![alt text](image-75.png)

![alt text](image-76.png)

![alt text](image-77.png)

![alt text](image-78.png)

* If there is an infinite depth graph, which algorithm will be better? IDA* is better because it is possible I go into some ruthole and never come back
* When would DFS branch and bound will be better algorithm?
  * When I have a better estimate of an upper bound. it requires additional domain knowledge

![alt text](image-79.png)

> If it is easy to find a sub optimal solution, branch and bound might do better. If it is difficult to construct a single solution IDA* might do better


## Non-optimal variations

![alt text](image-80.png)