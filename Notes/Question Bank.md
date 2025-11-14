# Nature-Inspired Computation: Comprehensive Concept Definition Bank

## Lecture 1: Introduction to Optimization & Metaheuristics

|Definition|Answer Word|
|---|---|
|A computing paradigm for exact, deterministic solutions using precise models and binary logic. Requires fully specified, unambiguous data.|Hard Computing|
|A computing paradigm for complex, hard-to-model problems. Uses fuzzy logic or neural networks to find "good enough" solutions, prioritizing tractability over exactness in uncertain environments.|Soft Computing|
|A combination of Hard and Soft computing, where one part of a problem is solved with exact models and the other with approximate methods.|Hybrid Computing|
|A pre-optimization problem-solving method that relies on logical deduction and satisfying constraints, which fails to scale for large or complex problems.|Reasoning by Feasibility|
|A classic numerical method for finding roots (or optima) that relies on the function's derivative, making it a gradient-dependent method.|Newton-Raphson|
|The process of finding the best solution (e.g., minimum or maximum) out of all possible feasible solutions.|Optimization|
|The principle that no single optimization algorithm is universally best. Averaged over all problems, all algorithms perform equally, so algorithm choice must fit the problem's characteristics.|No Free Lunch (NFL) Theorem|
|A problem-dependent "rule of thumb" for a "good enough" solution, often using greedy choices. Does not guarantee optimality. _Example: Nearest Neighbor for TSP._|Heuristic|
|A high-level, problem-independent "master strategy" that guides a heuristic search, using mechanisms (randomness, memory) to escape local optima and balance exploration/exploitation.|Metaheuristic|
|The "global" search phase, focused on searching new, diverse regions of the solution space to discover better areas and avoid premature convergence.|Exploration|
|The "local" search phase, focused on intensively searching a known "good" region to refine the best solution. Risks getting "stuck" without exploration.|Exploitation|
|The notation for the decision variable $x$ that results in the minimum value of the function $f(x)$. It represents the _solution_ itself, not the minimum value.|`arg min f(x)`|
|The vector $x$ in an optimization problem that represents the set of parameters or choices to be made.|Decision Variable|
|The function $f(x)$ to be minimized or maximized, which measures the "cost" or "quality" (fitness) of a given solution $x$.|Objective Function|
|The set $S$ containing all valid or permissible solutions $x$ that satisfy the problem's constraints.|Feasible Set|
|A class of optimization where the objective function and all constraints are linear functions of the decision variables.|Linear Optimization|
|A class of optimization where the objective function or at least one constraint is a nonlinear function. These often have complex landscapes with local optima.|Nonlinear Optimization|
|A class of optimization where decision variables can take any real value within a given range (e.g., $x \in \mathbb{R}$).|Continuous Optimization|
|A class of optimization where decision variables are restricted to integers or a finite set of values (e.g., $x \in \{0, 1, 2, 3\}$).|Discrete Optimization|
|An optimization problem where the decision variables must satisfy specific equations or inequalities.|Constrained Optimization|
|An optimization problem where there are no restrictions on the values of the decision variables.|Unconstrained Optimization|
|An optimization method where the same input always produces the exact same output (e.g., Linear Programming).|Deterministic Optimization|
|An optimization method that incorporates randomness. Solutions may vary between runs, making it useful for noisy or complex spaces (e.g., Genetic Algorithms).|Stochastic Optimization|
|An optimization method (like dynamic programming) that guarantees finding the precise optimal solution, but is often computationally infeasible for large problems.|Exact Method|
|An optimization method (like a metaheuristic) that finds near-optimal solutions in a reasonable time, suitable for large-scale problems where exactness is not guaranteed.|Approximate Method|
|A family of metaheuristics inspired by biological evolution, such as natural selection, crossover, and mutation (e.g., Genetic Algorithms).|Evolutionary-based|
|A family of metaheuristics inspired by the collective behavior of decentralized, self-organized systems like insect colonies or bird flocks (e.g., PSO, ACO).|Swarm-based|
|A family of metaheuristics inspired by physical laws, such as the annealing of metals or gravitational forces (e.g., Simulated Annealing).|Physics/Chemistry-inspired|
|A characteristic of a function (like $f(x) =|x|
|A problem with many "false peaks" or "valleys" (local optima), which can trap simple gradient-based or greedy search algorithms.|Multi-modal Problem|
|The exponential growth of the search space as the number of decision variables (dimensions) increases, making brute-force or grid search impossible.|Curse of Dimensionality|

## Lecture 2: Local Search & Hill Climbing

|Definition|Answer Word|
|---|---|
|A search method that iterates on a single solution, moving to a better neighbor. A "myopic" strategy that gets trapped in local optima.|Local Search|
|A search category that operates on one solution at a time, such as Hill Climbing or Simulated Annealing.|Single-State based Search|
|A search category that operates on a set of candidate solutions simultaneously, such as Genetic Algorithms or PSO.|Population-Based Search|
|A local search variant that defines a set of nearby solutions and evaluates them to find an improvement.|Neighborhood-based Search|
|A local search variant that randomly picks one nearby solution to try, rather than generating all neighbors. Good for huge search spaces.|Perturbation-based Search|
|The set of all solutions reachable from a current one by a single "move." A small neighborhood is fast but gets stuck; a large one is costly but explores more.|Neighborhood|
|A neighborhood for categorical or integer variables, where a "move" involves a discrete jump (e.g., $\pm 1$ neuron).|Discrete Neighborhood|
|A neighborhood where a variable is changed by a fixed amount (e.g., $x \pm 0.05$).|Additive (Linear Step)|
|A neighborhood where a variable is changed by a factor (e.g., $x \times 2, x / 2$). Useful for parameters that span orders of magnitude, like learning rates.|Multiplicative (Log-Scale Step)|
|A neighborhood for discrete problems, where a "move" involves swapping, inserting, or flipping elements (e.g., in feature selection).|Combinatorial Neighborhood|
|A neighborhood strategy where only a randomly sampled subset of all possible neighbors is evaluated, saving computation in large search spaces.|Probabilistic Neighborhood|
|A greedy local heuristic that iteratively moves to a better adjacent state. It stops at a "peak" (local optimum) where no neighbor is better.|Hill Climbing|
|A visual representation of all possible states (X-axis) plotted against their objective function values (Y-axis), showing the "landscape" of the search problem.|State-Space Diagram|
|A solution better than all its immediate neighbors, but not the best overall. This "false peak" traps greedy algorithms.|Local Optimum (or Local Maximum)|
|The single best solution in the entire search space. The true goal of optimization.|Global Optimum (or Global Maximum)|
|A flat search space area where neighbors have the same value, causing a Hill Climber to stall or "random walk."|Plateau|
|A feature in a search space sloping gently one way and steeply in others. An algorithm may "oscillate" across it, struggling to find the narrow path.|Ridge|
|A "best-improvement" hill climbing variant that evaluates _all_ neighbors and picks the one with the greatest improvement. It is computationally expensive and still gets stuck.|Steepest-Ascent Hill Climbing|
|A hill climbing variant that randomly selects one _improving_ neighbor. Introduces minor randomness but doesn't effectively escape local optima.|Stochastic Hill Climbing|
|A metaheuristic that runs Hill Climbing multiple times from different random starts, keeping the best solution found.|Random-Restart Hill Climbing|
|A "first-improvement" hill climbing variant that scans neighbors in an arbitrary order and moves to the _first_ one that is better, without checking the rest.|Simple Hill Climbing|
|The mathematical property of an algorithm (like Hill Climbing) where the objective function value is guaranteed to be non-decreasing ($f(x_{t+1}) \ge f(x_t)$) at each step.|Monotonic Improvement|
|The mathematical theorem stating that a non-decreasing sequence (like the objective value in Hill Climbing) that is also bounded (e.g., accuracy $\le 100\%$) must converge to a limit.|Monotone Convergence Theorem|
|An objective function that has a limit (e.g., error $\ge 0$ or accuracy $\le 1$), which guarantees that a monotonically improving algorithm will eventually stop.|Bounded Objective|
|The local search algorithm that uses the function's derivative to find the direction of "steepest descent" and moves in that direction.|Gradient Descent|
|A problem in gradient descent where the step size ($\eta$) is too large, causing the algorithm to jump completely over the minimum and end up in a worse position.|Overshooting|
|The mathematical representation of a local search move, finding the argument $z$ from the neighborhood $N(x^{(t)})$ that minimizes the function.|$x^{(t+1)} = \arg \min_{z \in N(x^{(t)})} f(z)$|
|A perturbation-based rule where the search direction is "flipped" if the last move was bad ($sign = -1$) or maintained if it was good ($sign = +1$).|Adaptive Perturbation|
|The points on a function where the first derivative is zero ($f'(x) = 0$), indicating a potential (local or global) minimum, maximum, or saddle point.|Critical Points|
|General term for problems like plateaus, ridges, and local optima that cause simple greedy search algorithms to fail.|Failure Cases (in Hill Climbing)|

## Lecture 3: Simulated Annealing (SA)

|Definition|Answer Word|
|---|---|
|A metaheuristic that escapes local optima by probabilistically accepting _worse_ solutions, mimicking physical annealing. It starts with high "temperature" (exploration) and "cools" to become greedier (exploitation).|Simulated Annealing (SA)|
|A general category of metaheuristics inspired by natural phenomena, including biological, physical, or swarm-based processes.|Nature-Inspired|
|A category of metaheuristics inspired by human cognition, memory, or problem-solving strategies (e.g., Tabu Search).|Human-Inspired|
|The physical process of heating and then slowly cooling a material. Slow cooling lets atoms settle into a stable, low-energy state (global minimum), while fast cooling "freezes" them in a local minimum.|Annealing|
|The mapping of concepts from thermodynamics to optimization, e.g., System State $\to$ Solution, Energy $\to$ Cost, Ground State $\to$ Global Optimum.|Thermodynamic Analogy|
|In the SA analogy, this represents the current candidate solution ($x$) in the search space.|Physical System State|
|In the SA analogy, this represents the value of the objective function ($f(x)$) or "cost" of the current solution.|Energy of the State|
|In the SA analogy, this represents the global optimum (the best possible solution) with the lowest possible "energy."|Ground State|
|The control parameter in SA governing the probability of accepting worse solutions. High `T` allows "exploratory" jumps; low `T` forces "exploitation" (like Hill Climbing).|Temperature (T)|
|The factor by which `T` is reduced each iteration. A schedule that is too fast leads to premature convergence; too slow wastes computation time.|Cooling Rate (or Schedule)|
|The formula ($P=e^{(-\Delta E/T)}$) used in SA to decide whether to accept a worse solution, based on the move's "badness" ($\Delta E$) and the current temperature ($T$).|Metropolis Criterion|
|The change in "energy" or "cost" ($\Delta E = E_{\text{new}} - E_{\text{old}}$). If this value is positive, the new solution is worse.|$\Delta E$ (Delta Energy/Loss)|
|The probability distribution ($P \propto e^{-E/T}$) that describes the likelihood of a physical system being in a certain energy state $E$ at a given temperature $T$.|Boltzmann Distribution|
|The core mechanism of SA, where a non-improving move is accepted (if $r < P$) to allow the search to escape a local optimum.|Probabilistic Acceptance|
|The initial high temperature value. It must be set high enough to allow the search to "melt" and escape its starting basin.|Initial Temperature ($T_0$)|
|The stopping condition for SA. When $T$ drops below this value, the search is "frozen" and terminates.|Minimum Temperature ($T_{\min}$)|
|The scaling factor (e.g., $\alpha = 0.9$) used in the most common geometric cooling schedule ($T_{\text{new}} = T_{\text{old}} \times \alpha$).|Cooling Factor ($\alpha$)|
|The phase in SA when $T$ is high, acceptance probability $P$ is high, and the algorithm frequently accepts worse moves to "jump" between valleys and find new regions.|Exploration Phase (SA)|
|The phase in SA when $T$ is low, acceptance probability $P$ is very low, and the algorithm behaves like Hill Climbing, only accepting better moves to refine the best-found solution.|Exploitation Phase (SA)|
|A failure case in SA where the cooling schedule is too fast, causing the algorithm to "freeze" in a local optimum before it has time to explore globally.|Premature Convergence|
|A failure case in SA where the cooling schedule is too slow, wasting computational time by exploring too much long after the optimal region has been found.|Slow Convergence|
|A failure case in SA where the "move" function is too conservative and only generates solutions very close to the current one, preventing the algorithm from escaping a local basin.|Weak Neighbor Generation|
|The key difference between SA and HC, where SA can _probabilistically_ accept a non-improving move, while HC _always_ rejects it.|Acceptance of Worse Solutions|
|The step in SA where a random number $r \in [0,1]$ is generated and compared to the acceptance probability $P$ to decide if a worse move is accepted.|Random Decision|
|A search algorithm that uses probabilistic rules to guide its search, such as SA or Stochastic Hill Climbing.|Probabilistic Search|
|A key advantage of SA over HC, as its ability to accept worse moves allows it to "climb out" of local optima.|Escape from Local Minima|
|SA is considered this because it operates on a single solution and explores its neighbors.|Local Search (property of SA)|
|SA is considered this because it uses a high-level strategy (the cooling schedule and probabilistic acceptance) to guide the local search and escape local optima.|Metaheuristic (property of SA)|
|The full procedure for SA, starting with initialization (S, T), and looping: generate $S_{\text{new}}$, calculate $\Delta E$, accept/reject based on $P$, and cool $T$.|SA Pseudocode (Concept)|
|A common state where $r \ge P$, and a non-improving move is _not_ accepted, so the algorithm stays at its current solution for that iteration.|Rejection (of worse move)|

## Lecture 4: Tabu Search (TS)

|Definition|Answer Word|
|---|---|
|A memory-based metaheuristic using a "forbidden" list of recent solutions/attributes to prevent cycling. This memory allows it to "climb down" from local optima by forcing non-forbidden (even if non-improving) moves.|Tabu Search (TS)|
|A metaheuristic category inspired by human behavior, such as using memory to avoid repeating mistakes.|Human-Inspired|
|The core problem TS solves, where a local search oscillates between two or more solutions (e.g., $A \to B \to A$) in a local optimum "basin."|Cycling|
|The short-term memory in TS storing attributes of recent moves (e.g., "reversing move X is forbidden"). It's the core mechanism preventing short-term loops.|Tabu List|
|The number of iterations a move's attributes remain "forbidden." A short tenure risks cycling; a long tenure may "stifle" the search.|Tabu Tenure|
|A move that is _not_ currently forbidden by the Tabu List (or meets the Aspiration Criteria). TS always picks the best move from this set.|Admissible Move|
|A rule in TS that overrides a move's "forbidden" status if that move leads to a new all-time-best solution, ensuring the global optimum isn't accidentally blocked.|Aspiration Criteria|
|An _exploitation_ strategy in TS that temporarily focuses the search on historically high-quality regions, such as by revisiting elite solutions.|Intensification|
|An _exploration_ strategy in TS to break out of a converged area. When "stuck," it forces a major change, like moving to a new region.|Diversification|
|The encoding of a potential solution for the problem (e.g., a vector of parameters, a set of weights).|Solution Representation (TS)|
|The definition of how new solutions (neighbors) are generated from a current one (e.g., $\eta \pm 0.001$).|Neighborhood Structure (TS)|
|A single, small change applied to a solution to generate a neighbor.|Move (TS)|
|The conditions that terminate the algorithm, such as max iterations, time limit, or no improvement for $N$ steps.|Stopping Criteria (TS)|
|A memory structure (used for intensification) that stores a set of the best solutions found during the search.|Intermediate Memory|
|A memory structure (used for diversification) that tracks visited regions or search frequency to guide the search to unexplored areas.|Long-Term Memory|
|A key difference from SA, where TS is deterministic and uses memory, while SA is probabilistic and memoryless.|TS vs. SA|
|A limitation of TS, where its performance is highly dependent on parameters like Tabu Tenure and neighborhood size.|Parameter Sensitivity|
|A limitation of TS, as maintaining complex memory structures (short, intermediate, long-term) can be computationally expensive.|Memory Management (TS)|
|A limitation of TS, as the optimal tenure and neighborhood definition must be re-tuned for each new problem.|Problem-Specific Tuning|
|A TS variant where the Tabu List is dynamically adapted based on search history (e.g., storing solutions instead of moves).|Adaptive Memory TS|
|A TS variant where the tabu tenure changes dynamically based on search progress (e.g., increasing tenure if cycling is detected).|Reactive TS|
|A TS variant that handles multiple, conflicting objectives, often by maintaining a Pareto-optimal set of solutions.|Multi-Objective TS|
|A hybrid method combining TS with Variable Neighborhood Search (VNS) for more diverse exploration.|TS with VNS|
|A hybrid method that combines two or more elite solutions to find an improved path between them in the search space.|TS with Path Relinking|
|The literal meaning of "Tabu," indicating that certain moves are "forbidden."|Forbidden|
|A key characteristic of TS, as it can handle both discrete and continuous problems.|Flexible Strategy|
|The main component of the Tabu List, which stores recent moves to prevent _reversing_ them and thus prevents cycling.|Short-Term Memory|
|The TS strategy of accepting these moves (if not tabu) to escape local optima.|Non-improving moves|
|A limitation of TS, as evaluating all neighbors in a large neighborhood at each iteration can be very slow.|Computational Cost (TS)|
|The core "philosophy" of TS, where it is modeled after human problem-solving, e.g., "don't repeat recent mistakes."|Human Problem-Solving (Inspiration)|

## Lecture 5: Particle Swarm Optimization (PSO)

|Definition|Answer Word|
|---|---|
|A search strategy that maintains and improves multiple solutions (a "population") in parallel. Solutions "interact" or "share information" to guide the population.|Population-Based Search|
|A CI field inspired by the collective, decentralized behavior of social animals. Key idea is _emergent behavior_: complex global intelligence from simple, local agent interactions.|Swarm Intelligence (SI)|
|A population-based metaheuristic where "particles" (solutions) "fly" through the search space. Movement blends inertia, attraction to its own `pbest` (cognitive), and attraction to the swarm's `gbest` (social).|Particle Swarm Optimization (PSO)|
|In PSO, the best position (solution) a _single particle_ has discovered so far. This "individual memory" provides the "cognitive" pull.|`pbest` (Personal Best)|
|In PSO, the best position (solution) _any particle_ in the swarm has discovered so far. This "social information" drives swarm exploitation.|`gbest` (Global Best)|
|A PSO parameter (`w`) controlling the influence of a particle's previous velocity. High `w` promotes exploration ("keep flying"); low `w` promotes exploitation ("braking").|Inertia Weight (w)|
|The part of the PSO velocity update ($c_1 \cdot r_1 \cdot (\text{pbest} - x)$) that pulls a particle toward its `pbest`, representing its "self-confidence."|Cognitive Component (c1)|
|The part of the PSO velocity update ($c_2 \cdot r_2 \cdot (\text{gbest} - x)$) that pulls a particle toward the swarm's `gbest`, representing the "social" aspect.|Social Component (c2)|
|A high-level category of population-based methods that includes PSO, ACO, etc.|Swarm Intelligence (Algorithm Class)|
|A high-level category of population-based methods that includes Genetic Algorithms, Genetic Programming, etc.|Evolutionary Algorithms (EA)|
|An SI Principle: Each agent must know its surroundings and capabilities (e.g., a particle knows its position and `pbest`).|Awareness|
|An SI Principle: The system should self-heal if some members fail (e.g., if some particles get stuck, `gbest` still guides others).|Resiliency|
|An SI Principle: Once a task is done, members autonomously look for new tasks (e.g., particles continuously move and update).|Solidarity|
|An SI Principle: Each agent acts independently while coordinating collectively (e.g., a particle calculates its _own_ velocity).|Autonomy|
|An SI Principle: The swarm can easily expand or shrink by adding/removing agents.|Expandability|
|A single candidate solution in the PSO swarm, which has a position and a velocity.|Particle|
|The natural inspiration for PSO, where individuals coordinate movement based on neighbors' positions.|Bird Flocking / Fish Schooling|
|The social model of PSO, where individuals share information (gbest) to find the best solution, rather than competing.|Cooperation Over Competition|
|The mathematical formula that updates a particle's position: $x_{i}(t+1) = x_{i}(t) + v_{i}(t+1)$.|Position Update Equation|
|The core mathematical formula of PSO that calculates a particle's new velocity based on inertia, cognitive, and social components.|Velocity Update Equation|
|The parameters $c_1$ and $c_2$ that control the "strength" or "pull" of the cognitive and social components, respectively.|Acceleration Coefficients|
|The random numbers $r_1, r_2 \in [0,1]$ that add stochasticity to the cognitive and social "pulls" in the velocity update.|$r_1, r_2$|
|The part of the velocity update ($w \times v(t)$) that represents the particle's tendency to continue in its previous direction (momentum).|Inertia Component|
|The "personal influence" part of the velocity update, representing the particle's own memory.|Cognitive Component (c1)|
|The "social influence" part of the velocity update, representing the swarm's collective memory.|Social Component (c2)|
|The effect of a high inertia weight (`w` $\approx 0.9$), which encourages particles to "fly" past `pbest`/`gbest` and search new areas (exploration).|High 'w' (effect)|
|The effect of a low inertia weight (`w` $\approx 0.4$), which "slows down" particles, causing them to refine solutions near `pbest`/`gbest` (exploitation).|Low 'w' (effect)|
|The "global search" aspect of PSO, driven by high inertia and a particle's cognitive component.|Diversification (in PSO)|
|The "local search" aspect of PSO, driven by low inertia and the strong "pull" of the social (`gbest`) component.|Intensification (in PSO)|
|A limitation of PSO where the social component's pull is too strong, causing all particles to rush to the _first_ good `gbest` found, trapping them in a local optimum.|Premature Convergence (PSO)|

## Lecture 6: Ant Colony Optimization (ACO)

|Definition|Answer Word|
|---|---|
|A metaheuristic where "artificial ants" _constructively build_ solutions (e.g., a path). They deposit "pheromone" on good solution components, which probabilistically attracts more ants.|Ant Colony Optimization (ACO)|
|The simulated chemical trail in ACO used for indirect, environmental memory. Ants deposit it on good solutions, making those components more attractive to future ants.|Pheromone|
|A mechanism of indirect coordination where one agent modifies the environment (e.g., leaves pheromone) and others react to that modification later. This allows complex behavior without central control.|Stigmergy|
|The positive feedback loop in ACO. A good path gets more pheromone, attracting more ants, which deposit more pheromone. Shorter paths reinforce faster, amplifying the best solution's signal.|Autocatalysis|
|The _a priori_ heuristic in ACO (often $1/d_{ij}$), representing a move's "desirability" _before_ pheromone. This greedy information guides ants, especially early in the search.|Visibility ($\eta_{ij}$)|
|The process in ACO where pheromone trails decay. This "forgetting" mechanism prevents mediocre paths from "locking in" the swarm, allowing it to forget bad paths and adapt.|Pheromone Evaporation ($\rho$)|
|The path-finding problem that inspired ACO, where real ants find the shortest route between their nest and a food source.|Shortest Path Problem|
|The starting point for all ants in an ACO simulation, representing the source node.|Nest|
|The target for the ants, representing the destination node or the completion of a solution.|Food|
|The formula $p_k(i,j)$ that combines pheromone ($\tau$) and visibility ($\eta$) to determine the likelihood of ant $k$ choosing to move from node $i$ to node $j$.|Probability Rule (ACO)|
|The _current_ amount of pheromone on an edge or solution component, denoted as $\tau_{ij}$.|Pheromone Intensity|
|The parameter ($\alpha$) that controls the influence of the pheromone trail. A high $\alpha$ makes ants _exploit_ known good paths.|Pheromone Weight ($\alpha$)|
|The parameter ($\beta$) that controls the influence of the heuristic visibility. A high $\beta$ makes ants act greedily, preferring locally shorter edges.|Visibility Weight ($\beta$)|
|The effect of a high $\alpha$ (pheromone weight), where ants strongly follow existing trails, leading to rapid exploitation but risking local optima.|High $\alpha$ (effect)|
|The effect of a high $\beta$ (visibility weight), where ants strongly prefer the locally "best" or "shortest" next step, making the search greedy.|High $\beta$ (effect)|
|The overall process of modifying pheromone levels, combining both evaporation (decay) and deposition (reinforcement).|Pheromone Update Rule|
|The formula ($\tau_{ij} \leftarrow (1-\rho) \times \tau_{ij}$) that reduces pheromone strength on all paths over time, allowing the swarm to "forget" bad solutions.|Pheromone Evaporation Formula|
|The process of adding new pheromone ($\Delta\tau$) to paths that were part of good solutions found by ants.|Pheromone Deposition|
|The amount of pheromone deposited by a single ant $k$ on edge $(i,j)$, often inversely proportional to the ant's total path length $L_k$.|$\Delta \tau_{ij}^k$|
|A constant (Q) that scales the amount of pheromone deposited by ants.|Pheromone Constant (Q)|
|The total length (or cost) of the solution (path) constructed by ant $k$. Shorter $L_k$ leads to higher pheromone deposits.|Path Length ($L_k$)|
|The total number of ants ($m$) in the population that build solutions in each iteration.|Number of Ants (m)|
|A key feature of ACO where ants _build_ solutions piece-by-piece rather than starting with a complete solution and improving it.|Constructive (Algorithm)|
|The probability of an ant moving from one node to another, calculated by the main ACO probability rule.|Transition Probability|
|An application of ACO where "nodes" are features. Ants build "paths" representing feature subsets, depositing pheromone on features that contribute to high accuracy.|ACO for Feature Selection|
|A common drawback of ACO, as it often requires many iterations for the pheromone trails to stabilize and converge to a high-quality solution.|Slow Convergence (ACO)|
|A drawback of ACO, where a strong positive feedback loop on a "good-but-not-great" path can attract all ants, preventing exploration of the true global optimum.|Local Optimum (ACO)|
|A drawback of ACO, as running many ants and updating pheromones across all solution components can be time- and memory-intensive.|High Computation (ACO)|
|A drawback of ACO, as its performance is highly dependent on the "magic values" chosen for $\alpha, \beta, \rho,$ and $m$.|Parameter Sensitive (ACO)|