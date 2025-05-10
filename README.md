# Bridge game search agent
## Contributor:

- **Nguyen** **Phuong** **Thuy**: Problem definition, Search strategies, Data Visualisation.
- **Nguyen** **Duy**: Problem definition, Agent Definition, Writing report.
- **Chu** **Gia** **Han**: Problem Definition, Environment Definition.

---

## Problem definition:

In this problem, a group of people needs to cross a bridge at night. They have only **one torch**, and at most **two people** can cross at a time. The time it takes to cross is determined by the **slower** of the two. The objective is to **minimize the total time** for all individuals to cross the bridge.
        
### Start and Goal:

- Start: All people and the torch are one side A
- End: All people and the torch move to side B

### Key Constraints

- At most **two people** can cross at once.
- They must carry the **torch** to cross.
- The **torch must be returned** if there are people still waiting on the starting side.
- When **two people** travel together, their **travel time** would be equal to the speed of the **slower person**.
- The goal is to find the **optimal crossing sequence** with the **least total time**.

---

## Goal:

- All four people must reach the other side of the bridge. 
- The total time taken must the the smallest value. 

---

## Metrics:

- The time cost of each move is equal to the slowest person’s speed in that move. 
- The total cost would be the sum of all moves.

---

## Search algorithms:

1. `Uninformed` search:
- Breadth-First Search
- Depth-First Search
- Uniform-Cost Search
- Depth-Limited Search
- Iterative Deepening Search

2. `Informed` search:
- Greedy Search
- A* Search

---

## Conclusion:

In general, informed search strategies perform better than uninformed search strategies.
- Both Greedy Search and A* Search are able to find the optimal path while explore only a small number of nodes.
- Uniform-Cost Search strategy also returns the optimal answer. However, it has to explore 25 nodes before reaching the best option.
- Breadth-First Search also explores many nodes, but it cannot give the least pathcost because the cost of the steps are different.
- Depth-First Search, Depth-Limited Search and Iterative Deepening Search can find the solution with the minimum number of exploration but their costs are much higher than other strategies. This implies that these search strategies maybe more suitable for larger problems, which require their benefit in memory.  

Therefore, it would be better if we can use informed search strategies. However, these strategies require information generated from heuristics function. As a result, it would take more time and consideration to create these functions before implementing the search strategies.
