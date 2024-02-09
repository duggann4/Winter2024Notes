- Prog 1 imminent actions:
	- Github repo accept (done)
	- plan checkpoint
- time intensive assignment
	- GIVE IT TIME
	- todo: backlogged videos
# Continuing
- Picking up from the preliminary optimization problem
	- Scalar problem
	- Add constraint $||w|| = \frac{1}{m}$
- Plugging in the new constraint:
	- $argmax_{w, b, m}\frac{1}{||w||} st y_i(\frac{w^Tx_i+b}{||w||}) \geq \frac{1}{||w||}$
	- $argmin_{w, b}||w|| st y_i(\frac{w^Tx_i+b}{||w||}) \geq \frac{1}{||w||}$
	- $argmin_{w, b}\frac{1}{2}||w||^2 st y_i(\frac{w^Tx_i+b}{||w||}) \geq \frac{1}{||w||}$
	- $argmin_{w, b}\frac{1}{2}||w||^2 st y_i(w^Tx_i+b) \geq 1$: Hard margin primal problem
		- gentlest slope such that no points are in $[-1,1]$
	- Hard margin dual problem: $argmax_\alpha \sum_{i=1}^N\alpha_i - \frac{1}{2}\sum_{i=1}^N \sum_{j=1}^N \alpha_i \alpha_j y_i y_j x_i^T x_j \ st\  \alpha_i \geq 0 \wedge \sum_{i=1}^N \alpha_i y_i = 0$ 
		- $\alpha$ and $N$ dimensional vector
		- $\alpha_i >0$ IFF $x_i$ on margin
		- $x_i$ for which $\alpha_i > 0$ are "support vectors"
			- points not on margin don't matter
	- Converting $\alpha \to w$: $w = \sum_{i=1}^N \alpha_i y_i x_i$
	- Getting $b$: $y_i - w^Tx_i$ for any SV $x_i$
	- Note: $w^*$, $b^*$ unique, $\alpha^*$ not necessarily unique
	- Between primal and dual problems:
		- primal better if $D << N$
		- dual better if $N << D$, the "useful" case
# Moving forward
- monday: relaxing hard margin
- tues: non-linearity
- Wed: multiclass