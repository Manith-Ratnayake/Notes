
What is Artificial Intelligence?
The science of making machines that can think and act like a humans.

Sub Fields of Artificial Intelligence
* Knowledge Representation
* Knowledge Reasoning
* Language Understanding
* Machine Learning

1940-1950: Early days
1943: McCulloch & Pitts: Boolean circuit model of brain o1950: Turing's “Computing Machinery and Intelligence”
1950—70: Excitement: Look, Ma, no hands!
1950s: Early AI programs, including Samuel's checkers program, Newell & Simon's Logic Theorist, Gelernter's Geometry Engine
1956: Dartmouth meeting: “Artificial Intelligence” adopted o1965: Robinson's complete algorithm for logical reasoning
1970—90: Knowledge-based approaches
1969—79: Early development of knowledge-based systems o1980—88: Expert systems industry booms
1988—93: Expert systems industry busts: “AI Winter”
1990—: Statistical approaches

Resurgence of probability, focus on uncertainty oGeneral increase in technical depth
Agents and learning systems… “AI Spring”?

----------------------------------------------------------------------------------------------------------------
What is an Agent?
An agent is anything that can be viewed as perceiving its environment through sensor and acting upon that environment through actuators.

What is a Rational Agent?
A rational agent is one that acts so as to achieve the best outcome or, when there is uncertainty, the best expected outcome.

Designing Rational Agents
In designing an agent,  the first step  must always be to specify the task environment as fully as possible.

We need PEAS (Performance, Environment, Actuators, Sensors) description.

Properties of task environment
* Fully Observable vs Partially Observable
* Deterministic vs Stochastic
* Static vs Dynamic
* Discrete vs Continuous
* Benign vs Adversarial
* Episodic vs Sequential
* Single agent vs Multiagent

Fully Observable Environments
- If an agent’s sensors give it access to the complete state of the environment at each point in time, then we say that the task environment is fully observable.


Partially Observable Environments
- An environment might be partially observable because of noisy and inaccurate sensors or because parts of the state are simply. In those environments you need memory on the side of the agent to make the best possible decision.


Deterministic Environments
- If the next state of the environment is completely determined by the current state and the action executed by the agent.

Stochastic Environments
- If the next state of the environment is not determined by the current state and the action executed by the agent. There is certain amount of uncertainty involves the next state.

Static  Environments
- If the environment does not change while an agent is deliberating, then we say  the environment is static.

Dynamic Environments
- If the environment can change while an  agent is deliberating, then we say the environment is dynamic.

Discrete Environments
- Discrete environment is one where you have finitely many choices.

Continuous Environments
- Possible actions or things you could sense may be infinite.

Benign  Environments
- The environment has no objective that would “go against” what you're trying to accomplish.


Adversarial Environments
- The environment observes you and contradict what you're trying to achieve.

Episodic Environments
- In an episodic task environment, the agent’s experience is divided into atomic episodes. In each episode the agent receives a percept and then performs a single action.
- Crucially, the next episode does not depend on the actions taken in previous episodes.

Sequential Environments
- In sequential environments, on the other hand,  the current decision could affect all future decisions.

Single agent environments
- If only one agent is involved in an environment, and operating  by itself then such an environment is called single agent environment.

Multiagent Environments
- If multiple agents are operating in an environment, then such an environment is called  a multi-agent environment.

-------------------------------------------------------------------------------------------------
Structure of the Rational Agent

Agent = Architecture + program
Architecture is the machinery that the agent executes on. It is a device with sensors and actuators, for example : a robotic car, a camera, a PC.
Agent program is an implementation of an agent function. An agent function is a map from the percept sequence to an action

Types of Rational Agents
* Simple Reflex Agents
* Model Based Reflex Agents
* Goal Based Agents
* Utility Based Agents
* Learning Agents

Simple Reflex Agents

* The simplest kind of agent is the simple reflex agent.
* Acts only on the basis of current perception
* Ignore  the rest of the percept history
* Based on the Condition Action Rule

Simple  Reflex  Agents: Examples
Tic-Tac-Toe

1940-1950: Early days
1943: McCulloch & Pitts: Boolean circuit model of brain o1950: Turing's “Computing Machinery and Intelligence”
1950—70: Excitement: Look, Ma, no hands!
1950s: Early AI programs, including Samuel's checkers program, Newell & Simon's Logic Theorist, Gelernter's Geometry Engine
1940-1950: Early days
1943: McCulloch & Pitts: Boolean circuit model of brain o1950: Turing's “Computing Machinery and Intelligence”
1950—70: Excitement: Look, Ma, no hands!
1950s: Early AI programs, including Samuel's checkers program, Newell & Simon's Logic Theorist, Gelernter's Geometry Engine
1956: Dartmouth meeting: “Artificial Intelligence” adopted o1965: Robinson's complete algorithm for logical reasoning
1970—90: Knowledge-based approaches
1969—79: Early development of knowledge-based systems o1980—88: Expert systems industry booms
1988—93: Expert systems industry busts: “AI Winter”
1990—: Statistical approaches
Resurgence of probability, focus on uncertainty oGeneral increase in technical depth
Agents and learning systems… “AI Spring”?
1956: Dartmouth meeting: “Artificial Intelligence” adopted o1965: Robinson's complete algorithm for logical reasoning
1970—90: Knowledge-based approaches
1969—79: Early development of knowledge-based systems o1980—88: Expert systems industry booms
1988—93: Expert systems industry busts: “AI Winter”
1990—: Statistical approaches

Resurgence of probability, focus on uncertainty oGeneral increase in technical depth
Agents and learning systems… “AI Spring”?
Checkers Game
Vacuum Cleaner

Model Based Reflex Agents
* Maintain an internal state which is adjusted by each percept
* Can be used to handle partial observability by use of a model about the world
* Rule  for action depends on both state and percept
Model Based Reflex Agents: Examples
House Cleaning  Robot
Mars Lander

Model Based Reflex Agents
Pros:
Can work on Partially observable environments
Cons:
Impossible to model the world accurately and reliably

Goal Based Agents
* Expansion of Model Based Reflex agents.
* Decision based on how far they are currently from their goal(description of desirable situations).
* Actions are intended to reduce its distance from the goal.
* Agent will account for the future


Goal Based Agents: Examples
Delivery Agents
Route Finding

Goal Based Agents
Pros:
Flexible
Cons:
Need searching and planning


Utility Based Agents

* Sometimes achieving the desired goal is not enough.
* Agent happiness should be taken into consideration.
* Utility describes how “happy” the agent is.
* A utility function maps a state onto a real number which describes the associated degree of happiness.

Utility Based Agents: Examples
* Delivery Agents
* Route Finding


Utility Based Agents
Pros:
Works on conflicting goals or uncertain goals
Cons:
Utility function


Learning Agents
Let the agent figure things out by itself!
Learning element
Makes improvements to performance element
Performance element
Selects actions
Previously this was the whole agent
Critic
Gives performance feedback to learning element
Needed because precepts don’t capture performance
Problem generator
Suggests innovative actions

---------------------------------------------------------------------------------------------------------------------------

Problem Solving:
• Four general steps in problem solving:
• Goal Formulation:
• What are the successful world states
• Problem Formulation:
• What actions and states to consider given the goal
• Search:
• Examine different possible sequences of actions that lead to states of known value and then choose the best sequence
• Execute:
• Perform the actions on the basis of the solution
• Problem-solving agent: a type of goal-based agent
• Decide what to do by finding sequences of actions that lead to desirable states


Properties of a Search Algorithm
• Completeness: Is the algorithm guaranteed to find a solution when there is one?
• Optimality: Does the strategy find the optimal solution?
• Time complexity: How long does it take to find a solution? (with respect to number of inputs)
• Space complexity: How much memory is needed to perform the search? (with respect to number of inputs)


Types of Search
• Uninformed Search (Blind Search)
• Informed Search (Heuristic Search)


Types of Uninformed Search
• Breadth-first Search
• Depth-first Search
• Uniform Cost Search
• Depth-limited search
• Iterative deepening depth-first search

Breadth-first Search

• Breadth-first search is a simple strategy in which the root node is expanded first, then all the successors of
the root node are expanded next, then their successors, and so on

Pros:
• Guarantee to find a solution
• Find a solution with minimal steps
 Cons:
• Need lot of memory
• Time Consuming

Depth-first Search
• Depth-first search always expands the deepest node in the current frontier of the search tree.

Pros:
• Memory efficient
• Less time
 Cons:
• Not guaranteed to find a solution

Uniform cost Search
• Expands the node with the lowest path cost
Pros:
• Complete
• Optimal
• Cons:
• Explore options in every direction

Depth Limited Search
• It is similar to DFS with a predetermined limit.
• Node at the depth limit will treat as it has no successor nodes further
Pros:
• Memory Efficient
• Does not run in to infinite loops
• Cons:
• Incompleteness
• Not Optimal

Iterative Deepening depth-first Search
• It is a combination of Depth First Search (DFS) and Breadth First Search (BFS).

Pros:
• Faster than BFS
• Not going to infinite loops
• Cons:
• Repeat all the work in the previous phase

-------------------------------------------------------------------------------------------------------------------

What is Informed (Heuristic) Search?
• Informed (Heuristic) search strategies use problemspecific knowledge beyond the definition of the problem itself.
• Informed search can find solutions more efficiently than an uninformed strategy.
• It can solve much complex problems which could not be solved in another way.

Types of Informed Search

• Best First Search
• A* Search

Best First Search (Greedy Search)
• It always selects the path which appears best at the moment.
• It is a combination of Depth First Search (DFS) and Breadth First Search (BFS).
• It uses the heuristic function h(n) <= h*(n).
• h(n) = Heuristic Cost
• h*(n) = Cost
• If n is a goal node, h(n) =0

Best First Search
• Pros:
• Efficient than BFS and DFS
• Cons:
• Might lead to infinite loops
• Not optimal
A* Search
• A* search finds the shortest path using heuristic function (h(n)) and the cost to reach the node n (g(n)).
• It is similar to Uniform Cost Search except that it uses g(n) + h(n) instead of g(n).
• A* Score (n) = g (n) + h (n)
A* Search
• Pros:
• It is optimal and complete
• It can solve very complex problems.
• Cons:
• It does not always produce shortest path
• Not practical for large scale problems

---------------------------------------------------------------------------------------------------------------

Introduction to Planning
• Planning is an important topic in AI.
• Planning is required for every task.
• Example: Reaching a particular destination requires planning.

What is Planning?
• Planning is the process of computing several steps of
a problem-solving procedure before executing any of them.
• Find sequence of actions that achieves a given goal when executed from a given initial world state.

Problems with Standard Search
• Overwhelmed by irrelevant actions
• Finding a good heuristic function is difficult
• Cannot take advantage of problem decomposition

Planning vs. Problem Solving

• Planning agent is different from problem solving agent in:
• Representation of goals, states, actions
• Use of explicit, logical representations
• Way it searches for solutions
• Planning is more powerful because of the representation and methods used

Defining a Planning System:
• It requires;
• domain description,
• action specification,
• goal description.

Two Types of Planning
1. Classical Planning:
• Fully Observable
• Deterministic
• Static
2. Non- Classical Planning:
• Partially Observable
• Stochastic

Planning Algorithms:
1.Forward State Space Planning (FSSP)
• Progression
2. Backward State Space Planning (BSSP)
• Regression

Progression
• A plan is a sequence of STRIPS operators
• From initial state, search forward by selecting
operators whose preconditions can be unified with
literals in the state
• New state includes positive literals of effect; the
negated literals of effect are deleted
• Search forward until goal unifies with resulting state
• This is state-space search using STRIPS operators
Regression
• A plan is a sequence of STRIPS operators
• The goal state must unify with at least one of the positive literals in the operator’s effect
• Its preconditions must hold in the previous situation, and these become subgoals which might be satisfied by the initial conditions
• Perform backward chaining from goal
• Again, this is just state-space search using STRIPS operators

Partial Order Planning
• Idea:
• works on several subgoals independently
• solves them with subplans
• combines the subplans
• flexibility in ordering the subplans
• least commitment strategy:
• delaying a choice during search
• Example, leave actions unordered, unless they must be sequential

-----------------------------------------------------------------------------------------------------------------------

Central component of a knowledge-based agent is a Knowledge-Base

Properties of FOL

1.Validity: A formula is valid if it holds true for all possible interpretations. For
instance, the formula P ∨ ¬P (where P is a proposition) is always true, regardless of
the truth value of P. It is known as the principle of the excluded middle.

2.Satisfiability: A formula is satisfiable if it can be made true by some interpretation.
For example, the formula P ∧ Q is satisfiable when both P and Q are true.

3.Unsatisfiability: A formula is unsatisfiable if it cannot be made true by any
interpretation. For instance, the formula P ∧ ¬P (where P is a proposition) is always
false, regardless of the truth value of P . It represents a logical contradiction.

4.Entailment: Entailment occurs when one formula logically implies another. For
example, if we have the premises ∀x (P(x) → Q(x)) and ∀x P(x) , we can logically infer
∀x Q(x). This means that the truth of the premises implies the truth of the conclusion.
