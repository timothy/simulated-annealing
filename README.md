# Simulated Annealing
Simulated annealing is a probabilistic technique for approximating the global optimum of a given function. Specifically, it is a metaheuristic to approximate global optimization in a large search space for an optimization problem.

```pseudocode
function SIMULATED-ANNEALING(problem, schedule) # returns a solution state
	current <- problem.INITIAL
	for t = 1 to ∞ do
	T <- schedule(t)
	if T = 0: return current
	next <- randomCur # a randomly selected successor of current
	∆E <- VALUE(current) - VALUE(next)
	if ∆E > 0 then current <- next
	else current <- next only with probability e^{∆E/T}
```

Note: "e^{∆E/T}" == $`e^{∆E/T}`$

Note: In pseudocode, the delta symbol (∆) is used to represent the change in a variable or the difference between two values. In this case: ∆E refers to the difference in energy between the current state and the next state. It is calculated as the difference between the value of the current state and the value of the next state.

 - T is the simulated temperature at time _t_, which reduces from a high value at the beginning to near zero eventually.
 - ΔE is the change in energy going from current to next.


Ref: 4.1 - 115
