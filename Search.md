# aritifical-intelligence

# Search
terminology
1. Agent - entity that perceives its environment and acts upon that environment
    example - AI or a person who is trying to navigate to solution
2. State - a config of the agent and its environment
3. Initial state - the start of the state. 
4. Actions - choices that can be made in a state. 
    Actions(x) returns the set of actions that can be executed in states s
5. Transition model - a description of what state results from performing any applicable action in any state
    RESULT(s, a), where s = state, a = action. 
    returns the state resulting from performing action a in state s.
    refer to image 5.a in excalidraw
    output result will be a new state. 
6. State Space - the set of all states reachable from the initial state by any sequence of actions. 
    refer to image 6.a in excalidraw

How will the AI know that we have arrived at our destination, solution? It is done by Goal Test. 

7. Goal test - way to determine whether a given state is a goal state. 
8. Path cost - numerical cost associated with a given path. helps to choose the solution/destination. 
    Every state will get a numerical cost applied. 
    Refer to the image 8.a in excalidraw
9. Solution - a sequence of actions that leads from the initial state to a goal state.
10. Optimal solution - A solution that has the lowest path cost among all solutions.


11. Node - a data structure that keeps track of
    a state
    a parent (node that generated this node.)
    an action (action applied to parent to get node)
    a path cost (from initial state to node)

12. frontier - collection or a space where we got future states (potential solutions)

13. The approach
    Start with a frontier that contains the initial state.
    Repeat:
        if the frontier is emply, then no solution
        remove a node from the frontier
        if node contains goal state, return the solution.

![Approach intial state](/images/search/approach_initial.png)

14. Following the approach
    A is a state and it foes into the frontier. 
    Repeat:
        Frontier is not empty.
        remove the node 
        not goal state, return the state and get the next state.

    B goes is frontier now. 
    Repeat:
        Frontier is not empty.
        remove the node.
        not goal state. return the state and get the next state. 

    C and D goes in frontier now.
    Repeat:
        Frontier is not empty.
        remove the node C
        not a goal state. return the state "C" and get the next state. 
        D is still in the frontier.
    
    E goes in the frontier along with D. 
    Repeat:
        Frontier is not empty.
        remove the node E
        It is the goal state. A to E path is traversed.

15. What could go wrong?
    A and B could keep going back and forth. Looping infinitely.
    We can avoid this, by keeping a state/memory.

16. Revised Approach
    Start with a frontier that contains the initial state.
    start with an empty explored set.
    Repeat:
        if the frontier is empty, then no solution.
        remove a node from the frontier.
        if node contains goal state, return the solution.
        add the node to the explored set.
        expand node, add resulting nodes to the frontier if they aren't already in the frontier or the explored set.

17. Frontier is a data structure hence it must follow a pattern on how we remove the node. We can follow LIFO. Last in first out. 

18. Depth-first search - search algorithm that always expands the deepest node in the frontier.

19. Breadth-first search - search algorithm that always expands the shallowest node in the frontier. OR
    quueue - FIFO, first in first out. 

20. Uniformed Search

21. Informed seach - search strategy that uses problem-specific knowledge to find solutions more efficiently.
    Types of informed searches
        a. Greedy best - first search - search algo that expands the node that is closest to the goal. as estimated by a heuristic function h(m)
             - Greedy best first search algo is heavily dependent on the quality of heuristics produced. 
             - When the algo reaches "decision 1" (look at 21. a in excalidraw), it has to make a decision to go left or right. Algo makes a decision to go right because the heuristics function has recorded 11 steps to goal. 
             - Similar decisions are done at later stages. 

        b. A* search - search algo that expands node with lowest value of g(n) + h (n)
        where, g(n) = cost to reach node.
               h(n) = estimated cost to goal.

22. Minimax - adversarial search
 - given a state s:
    - MAX picks action a in Actions(s) that produces highest value of Min-Value(result(s,a))
    - MIN picks action a in Actions(s) that produces least/smallest value MAX-value(result(s,a))
    
    - fucntion MAX-Value(state):


