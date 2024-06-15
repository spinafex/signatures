\subsection{The problem statement}
Given a rough path X, its truncated (N=1) augmented signature $X_hat$, and its corresponding payoff process 
\\
$$Y = e^{-rt} ((-X_t)-c)$$
\\
Where:
r = risk free rate
c = fixed transaction cost
\\
The optimal policy $l^{*}$ is the supremum of the $\upsilon_l$ series.
\\
Write a script that:
\\
generates a rough path (an OU process),
\\
takes a sample of rough path X (e.g., $X_t$) of 250 increments,
\\
calculates the payoff for each increment, and
\\
a) returns the optimal point for entering a long position ($l_0$).
Then, starting from $l_0$,
\\
b) return the optimal point for exiting the position ($l_1$) defined by supremum of the payoff process $$Y = e^{-rt} ((X_t)-c)$$.
\\Record the combination of entry ($l_0$) and exit ($l_1$) points represented by the tensor product of $l_0$ and $l_1$ which are increments of $X_hat$ that include data from the truncated (N=1), augmented signature of the process $X$.
\\
c) Starting from $l_1$, return the optimal point for entering a second long position ($l_2$).
\\
d) Starting from $l_2$, return the optimal point for exiting a second long position ($l_3$).
\\
e) Record the tensor product of $l_1$ and $l_2$.
\\
f) Proceed recursively until the end of the series.
\\
g) Perform this procedure for ten samples of X.
\\
h) We want the optimal levels of $X$ (based on the payoff function) associated with those timesteps. Since each recorded tensor product contains the levels of X at the optimal entry and exit points, it is possible to solve backwards from the tensor product to the optimal entry and exit levels of X for each pair ($l_n$, $l_n+1$). Using the group of pairs ($l_0, l_1$) from samples #1 through #10, solve for the first optimal policy $l^{*}{(0,1)$.
\\
i) Proceed recursively through each group of pairs until all groups of pairs have been exhausted.
\\
Return a) the number of optimal policies found, and b) the summed profit from the payoff process of all optimal policies $l^{*}{(n,n+1)$ and c) the entry and exit levels of X for each optimal policy.

Graph the sample rough path and overlay the optimal entry and exit points on the chart.
\end{document}
