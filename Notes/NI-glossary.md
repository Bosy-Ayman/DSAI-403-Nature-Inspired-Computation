# Metaheuristics
| **Term**                              | **Definition**                                                                                                                                    |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Approximate Method                    | An optimization method that yields near-optimal solutions in reasonable time; suitable for large problems but cannot guarantee the exact optimum. |
| Artificial Neural Network (ANN)       | A soft computing tool used for learning, modeling complex patterns, and adaptation.                                                               |
| Constrained Optimization              | Optimization where variables must satisfy constraints or restrictions.                                                                            |
| Continuous Optimization               | Optimization where variables can take any real-valued numbers within a continuous range.                                                          |
| Convex Function                       | A bowl-shaped function where any local minimum is also the global minimum, making optimization easier.                                            |
| Cost Function                         | The objective function f(x) that is minimized or maximized during optimization.                                                                   |
| Curse of Dimensionality               | The exponential increase in search space size as the number of dimensions grows, making optimization more difficult.                              |
| Decision Variable                     | The variable(s) adjusted by the optimization process to search for the best solution.                                                             |
| Deterministic Optimization            | Optimization where identical inputs always produce the same output; predictable and reproducible.                                                 |
| Discrete Optimization                 | Optimization involving integer or finite-set variables.                                                                                           |
| Evolutionary-based Algorithms         | Metaheuristics inspired by biological evolution using crossover and mutation; strong in exploration (e.g., GA, DE).                               |
| Exact Method                          | An optimization method that guarantees the true optimal solution but becomes impractical for large problems due to exponential complexity.        |
| Exploitation                          | Searching intensively near known good regions to refine a solution.                                                                               |
| Exploration                           | Searching globally across new or unknown areas of the solution space.                                                                             |
| Feasible Set                          | The set of all valid solutions satisfying constraints, denoted S.                                                                                 |
| Fuzzy Logic (FL)                      | A soft computing method for reasoning with uncertainty, imprecision, and partial truth.                                                           |
| Genetic Algorithm (GA)                | A soft computing optimization method and a key evolutionary-based metaheuristic.                                                                  |
| Hard Computing                        | A precise, deterministic approach using strict mathematical models, ideal for well-defined problems.                                              |
| Heuristic                             | A problem-specific approximate method inspired by intuitive or rule-based strategies.                                                             |
| Hybrid Computing                      | A mixture of hard and soft computing used to leverage strengths of both approaches.                                                               |
| Linear Optimization                   | Optimization with linear objective and linear constraints.                                                                                        |
| Metaheuristic                         | A general optimization framework, often nature-inspired, capable of handling complex problems without domain-specific assumptions.                |
| Multi-modal Function                  | A function containing many local minima and maxima, challenging for greedy methods.                                                               |
| No Free Lunch (NFL) Theorem           | A theorem stating that no algorithm is universally superior across all optimization problems.                                                     |
| Non-Convex Function                   | A function with multiple local minima that can trap gradient descent methods.                                                                     |
| Non-differentiable Function           | A function with points where derivatives do not exist, causing issues for gradient-based methods.                                                 |
| Nonlinear Optimization                | Optimization where the objective or at least one constraint is nonlinear.                                                                         |
| Optimization                          | The process of finding the best possible solution among all feasible solutions.                                                                   |
| Physics/Chemistry-inspired Algorithms | Metaheuristics inspired by natural physical or chemical processes (e.g., SA, Harmony Search).                                                     |
| Soft Computing                        | A flexible approach to solving complex, real-world problems involving uncertainty or approximation.                                               |
| Stochastic Optimization               | Optimization that uses randomness; results may vary between runs.                                                                                 |
| Swarm-based Algorithms                | Metaheuristics inspired by collective behaviors (e.g., PSO, ACO).                                                                                 |
| Unconstrained Optimization            | Optimization without any variable restrictions.                                                                                                   |
| Unimodal Function                     | A function with a single peak or trough, easy for algorithms to optimize.                                                                         |

#  Hill Climbing
| **Term**                        | **Definition**                                                                                                                                                              |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Adaptive Perturbation           | An update rule where the next solution is the current one plus a scaled random perturbation, with direction influenced by whether the previous move improved the objective. |
| Additive Neighborhood           | A neighborhood created by adding or subtracting a fixed step size to a parameter (e.g., d ± 0.05); also called a Linear Step.                                               |
| Combinatorial Neighborhood      | A neighborhood for discrete problems where moves involve swapping, flipping, toggling, or exchanging elements.                                                              |
| Convergence                     | The point where the algorithm stops changing significantly and stabilizes; Hill Climbing always converges to a local optimum.                                               |
| Discrete Neighborhoods          | Neighborhoods defined for categorical or integer parameters, such as architecture choices in neural networks.                                                               |
| Fitness Function                | The objective function f(x) that measures solution quality; the goal is to maximize or minimize it.                                                                         |
| Global Maximum                  | The single best possible point in the entire state space where the objective reaches its highest value.                                                                     |
| Heuristic Algorithm             | A method that finds good (often approximate) solutions quickly when exact algorithms are too slow or fail.                                                                  |
| Hill Climbing                   | A heuristic local search that starts from an initial solution and repeatedly moves to a better neighbor until no improvement is found.                                      |
| Local Maximum                   | A state better than its neighbors but not the best overall state.                                                                                                           |
| Local Optima                    | Solutions that are optimal relative to nearby alternatives; can trap local search algorithms.                                                                               |
| Local Search                    | A heuristic that improves a single solution by repeatedly selecting better neighbors; simple and fast but prone to trapping.                                                |
| Metaheuristic Algorithm         | A higher-level optimization strategy that balances exploration and exploitation (e.g., GA, PSO).                                                                            |
| Multiplicative Neighborhood     | A neighborhood created by scaling parameters by multiplication or division (e.g., η/2 or η×2); also called Log-Scale Step.                                                  |
| Neighborhood (N(x))             | The set of solutions reachable from the current solution through a small change or move.                                                                                    |
| Neighborhood-based LS           | A local search that evaluates many or all neighbors and moves to the best one.                                                                                              |
| Perturbation-based LS           | A local search that samples one random neighbor instead of evaluating all; ideal for huge search spaces.                                                                    |
| Plateau                         | A flat region where neighboring states have the same objective value, making search direction ambiguous.                                                                    |
| Population-Based Local Search   | Algorithms that work with multiple solutions at once (e.g., GA, PSO).                                                                                                       |
| Probabilistic Neighborhoods     | Neighborhoods where only a random subset of neighbor solutions is evaluated, useful for very large search spaces.                                                           |
| Random-Restart Hill Climbing    | A method that performs multiple independent hill-climbing runs from random starting points to increase the chance of reaching the global optimum.                           |
| Ridge                           | A sloped, narrow high region in the search space that restricts movement and can cause premature stopping.                                                                  |
| Shoulder                        | A plateau with an uphill edge that allows escape toward better solutions.                                                                                                   |
| Simple Hill Climbing            | A fast method that scans neighbors in arbitrary order and takes the first improvement found.                                                                                |
| Single-State based Local Search | Algorithms that operate on only one solution at a time (e.g., Hill Climbing, SA).                                                                                           |
| State-Space Diagram             | A representation of all possible states and their objective values across the landscape.                                                                                    |
| Steepest-Ascent Hill Climbing   | A variant that evaluates all neighbors and chooses the one with the highest improvement; more expensive but systematic.                                                     |
| Stochastic Hill Climbing        | A variant that selects a random neighbor and accepts it only if it is better, adding randomness to avoid local maxima.                                                      |




# Simulated Annealing

| **Term**                    | **Definition**                                                                                                                                                                   |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Annealing                   | A physical process of heating and slowly cooling metals or glass, allowing atoms to settle into a stable, low-energy structure.                                                  |
| Boltzmann Distribution      | The probability distribution used in the Metropolis criterion to determine acceptance of a worse solution, computed as **P = e^(−ΔL / T)**.                                      |
| Cooling Rate (α)            | A parameter (0–1) controlling how fast temperature decreases in SA; values near 1 cool slowly, while smaller values cool quickly.                                                |
| Exploitation Phase          | The low-temperature stage of SA where the algorithm rarely accepts worse solutions and behaves like a greedy local search to refine the best solution.                           |
| Exploration Phase           | The high-temperature stage of SA where the algorithm frequently accepts worse solutions, enabling broad search and avoiding early local minima.                                  |
| Hill-Climbing Search        | A greedy local search method that always moves to a better neighbor; effective but easily trapped in local maxima, plateaus, or ridges.                                          |
| Local Maximum               | A suboptimal peak that is lower than the global maximum; Hill Climbing can become stuck here.                                                                                    |
| Metaheuristic               | A high-level strategy that guides local search to improve exploration and avoid local optima; SA qualifies because its temperature schedule shapes the search.                   |
| Metropolis Criterion        | The SA rule that determines whether to accept a worse solution by comparing Boltzmann probability to a random number.                                                            |
| Nature-Inspired Computation | A computational field inspired by natural processes such as physics (SA), swarm behavior (ACO), and evolution (GA).                                                              |
| Plateau                     | A flat region in the search space where no local move improves the solution, causing Hill Climbing to perform a random walk.                                                     |
| Ridges                      | Long, gently sloping features in the search landscape that cause algorithms to oscillate sideways, making progress toward the peak difficult.                                    |
| Simulated Annealing (SA)    | A probabilistic optimization algorithm modeled after physical annealing, capable of escaping local minima by accepting worse solutions with a temperature-dependent probability. |


# Tabu

| **Term**                        | **Definition**                                                                                                                      |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Adaptive Memory Tabu Search     | A variant of Tabu Search that automatically adjusts the Tabu list size based on search history and performance.                     |
| Aspiration Criteria             | A rule that permits a tabu move if it produces a solution better than any previously found.                                         |
| Diversification Strategy        | An exploration technique that pushes the search toward new, unexplored regions when progress stalls.                                |
| Evaluation (Objective Function) | A function that scores solution quality; the goal is to maximize or minimize this value depending on the problem.                   |
| Hill Climbing                   | A local search method that always moves to a better neighbor but is easily trapped in local optima.                                 |
| Intensification Strategy        | An exploitation technique that deepens the search near promising or high-quality solutions.                                         |
| Local Search                    | An optimization method that explores neighbors of a current solution, iteratively moving to better ones.                            |
| Metaheuristics                  | High-level optimization frameworks that incorporate principles like randomness, memory, or cooperation to solve difficult problems. |
| Neighborhood Structure          | The set of possible neighboring solutions defined by small modifications to the current solution.                                   |
| No Free Lunch (NFL) Theorem     | A theoretical result stating that no optimization algorithm outperforms all others on every type of problem.                        |
| Reactive Tabu Search            | A dynamic version of Tabu Search where the tabu tenure changes in response to the search’s behavior.                                |
| Simulated Annealing             | A local search algorithm that accepts worse solutions with a decreasing probability to escape local minima; it does not use memory. |
| Solution Representation         | The encoding format of a solution (e.g., vectors, configurations) allowing easy generation of neighbors.                            |
| Stopping Criteria               | Conditions that determine when the algorithm should stop, such as time limits, no improvement, or iteration count.                  |
| Tabu List                       | A short-term memory structure storing forbidden moves or solutions to prevent cycling.                                              |
| Tabu Search (TS)                | A memory-enhanced local search algorithm that uses tabu restrictions to escape local optima and explore more effectively.           |
| Tabu Tenure                     | The number of iterations a move remains forbidden on the Tabu List.                                                                 |




| **Term**                        | **Definition**                                                                                                                      |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Adaptive Memory Tabu Search     | A variant of Tabu Search that automatically adjusts the Tabu list size based on search history and performance.                     |
| Aspiration Criteria             | A rule that permits a tabu move if it produces a solution better than any previously found.                                         |
| Diversification Strategy        | An exploration technique that pushes the search toward new, unexplored regions when progress stalls.                                |
| Evaluation (Objective Function) | A function that scores solution quality; the goal is to maximize or minimize this value depending on the problem.                   |
| Hill Climbing                   | A local search method that always moves to a better neighbor but is easily trapped in local optima.                                 |
| Intensification Strategy        | An exploitation technique that deepens the search near promising or high-quality solutions.                                         |
| Local Search                    | An optimization method that explores neighbors of a current solution, iteratively moving to better ones.                            |
| Metaheuristics                  | High-level optimization frameworks that incorporate principles like randomness, memory, or cooperation to solve difficult problems. |
| Neighborhood Structure          | The set of possible neighboring solutions defined by small modifications to the current solution.                                   |
| No Free Lunch (NFL) Theorem     | A theoretical result stating that no optimization algorithm outperforms all others on every type of problem.                        |
| Reactive Tabu Search            | A dynamic version of Tabu Search where the tabu tenure changes in response to the search’s behavior.                                |
| Simulated Annealing             | A local search algorithm that accepts worse solutions with a decreasing probability to escape local minima; it does not use memory. |
| Solution Representation         | The encoding format of a solution (e.g., vectors, configurations) allowing easy generation of neighbors.                            |
| Stopping Criteria               | Conditions that determine when the algorithm should stop, such as time limits, no improvement, or iteration count.                  |
| Tabu List                       | A short-term memory structure storing forbidden moves or solutions to prevent cycling.                                              |
| Tabu Search (TS)                | A memory-enhanced local search algorithm that uses tabu restrictions to escape local optima and explore more effectively.           |
| Tabu Tenure                     | The number of iterations a move remains forbidden on the Tabu List.                                                                 |





# particale swarm 
| **Term**                           | **Definition**                                                                                                                                  |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Acceleration Coefficients (c1, c2) | Cognitive and social learning coefficients: c1 drives a particle toward its personal best; c2 drives it toward the global best.                 |
| Autonomy                           | A Swarm Intelligence principle where each agent acts independently while still contributing to collective coordination.                         |
| Awareness                          | A Swarm Intelligence principle where each agent must understand its environment and its own capabilities.                                       |
| Cognitive Component                | The PSO term **c1 × r1 × (pbest − x(t))**, which guides a particle toward its own best-found solution.                                          |
| Exploitation                       | Refining and improving the best-known solutions. In PSO, encouraged by low inertia weight (w) and high social coefficient (c2).                 |
| Exploration                        | Searching broad areas of the search space for new solutions. In PSO, encouraged by high inertia weight (w) and high cognitive coefficient (c1). |
| gbest (Global Best)                | The best solution found by any particle in the swarm up to the current iteration.                                                               |
| Hill Climbing (HC)                 | A deterministic, single-solution optimization method that always moves to better neighbors; prone to getting stuck in local optima.             |
| Inertia Component                  | The term **w × v(t)** in PSO, representing momentum from the particle’s previous movement direction.                                            |
| Inertia Weight (w)                 | A PSO parameter controlling the trade-off between exploration (high w) and exploitation (low w).                                                |
| pbest (Personal Best)              | The best solution found by an individual particle so far.                                                                                       |
| Particle                           | A candidate solution in PSO that moves through the search space, analogous to a bird in a flock.                                                |
| Particle Swarm Optimization (PSO)  | A population-based meta-heuristic inspired by swarm behavior, using pbest and gbest for collective learning.                                    |
| Population-Based Search            | Optimization methods that evaluate and evolve a set of solutions simultaneously, improving global exploration.                                  |
| Position Update Equation           | The equation **x(t + 1) = x(t) + v(t + 1)**, determining how particles move to new positions.                                                   |
| Resiliency                         | A Swarm Intelligence principle where the group can continue functioning even if some agents fail or leave.                                      |
| Simulated Annealing (SA)           | A probabilistic, single-solution method that occasionally accepts worse moves to escape local minima.                                           |
| Social Component                   | The PSO term **c2 × r2 × (gbest − x(t))**, which pulls a particle toward the swarm’s global best.                                               |
| Solidarity                         | A Swarm Intelligence principle where agents autonomously seek new tasks after completing their current one.                                     |
| Swarm Intelligence (SI)            | Collective, decentralized, self-organized problem solving inspired by natural systems.                                                          |
| Tabu Search (TS)                   | A memory-based single-solution optimization technique that avoids revisiting recent solutions.                                                  |
| Velocity Update Equation           | The PSO formula **v(t + 1) = w × v(t) + c1 × r1 × (pbest − x(t)) + c2 × r2 × (gbest − x(t))**, determining particle velocity updates.           |



# Ant Colony Optimization (ACO)

| **Term**                      | **Definition**                                                                                                                                                                                                         |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Ant Colony Optimization (ACO) | A nature-inspired optimization algorithm based on how ants find shortest paths using pheromone trails; a population-based global search method used for routing, feature selection, and other hard optimization tasks. |
| α (Alpha)                     | The pheromone weight parameter controlling how strongly ants rely on pheromone trails (exploitation).                                                                                                                  |
| Autocatalysis                 | A positive feedback process where more ants following a path increase pheromone deposition, attracting even more ants and reinforcing that path.                                                                       |
| β (Beta)                      | The visibility weight parameter determining the importance of heuristic or distance information, guiding ants toward more desirable edges (exploration).                                                               |
| Cumulative Probability        | A selection technique that converts discrete probabilities into continuous intervals on a 0–1 scale, allowing random sampling for decision-making.                                                                     |
| Evaporation                   | The reduction of pheromone strength over time, preventing excessive accumulation and encouraging exploration by reducing influence of older paths.                                                                     |
| Exploitation                  | Ant behavior in which strong pheromone trails and desirable paths are preferred; increased with higher α and β and lower ρ.                                                                                            |
| Exploration                   | Ant behavior that involves trying lesser-known or low-pheromone paths to uncover new solutions; increased with lower α and β and higher ρ.                                                                             |
| Feature Selection             | An optimization task where the objective is to identify the best subset of features that balances accuracy and complexity; ACO can treat features as nodes to solve this.                                              |
| Fitness                       | A measure of solution quality produced by an ant; in feature selection, typically computed as accuracy gain divided by complexity cost.                                                                                |
| η (Eta)                       | Visibility or heuristic information for choosing edges; often 1/dᵢⱼ in routing, or Gain/Cost in feature selection.                                                                                                     |
| Pheromone                     | A numerical value representing collective memory of ants about path quality, analogous to chemical trails in real ant colonies.                                                                                        |
| Pheromone Deposition          | The act of adding pheromone to edges after traversal; shorter or better-quality paths yield larger deposits.                                                                                                           |
| Population-Based Search       | A global search strategy that uses multiple candidate solutions simultaneously (e.g., ACO, PSO, GA).                                                                                                                   |
| Probability Rule              | The formula that determines the likelihood of an ant choosing a specific next node, based on τ (pheromone) and η (visibility).                                                                                         |
| ρ (Rho)                       | The evaporation rate (0–1), controlling how quickly pheromone trails decay.                                                                                                                                            |
| Q                             | The pheromone constant defining the total pheromone an ant can deposit along its path.                                                                                                                                 |
| Stigmergy                     | Indirect communication where ants influence each other by modifying the environment (via pheromone trails), enabling decentralized coordination.                                                                       |
| τ (Tau)                       | The pheromone intensity on an edge or path, updated each iteration based on evaporation and deposition.                                                                                                                |

