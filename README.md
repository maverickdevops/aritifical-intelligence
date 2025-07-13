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
![Result(s,a)(image.png)