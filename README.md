# aritifical-intelligence

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



