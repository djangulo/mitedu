6.042/18.062J Mathematics for Computer Science

Tom Leighton and Marten van Dijk

---

# Problem set 2

## Problem1. [12 points]

Define a 3-chain to be a (not necessarily contiguous) subsequence of three integers, which is either monotonically increasing or monotonically decreasing. We will show here that any sequence of five distinct integers will contain a 3-chain. Write the sequence as $a_1$, $a_2$, $a_3$, $a_4$, $a_5$. Note that a monotonically increasing sequences is one in which each term is greater than or equal to the previous term. Similarly, a monotonically decreasing sequence is one in which each term is less than or equal to the previous term. Lastly, a subsequence is a sequence derived from the original sequence by deleting some elements without changing the location of the remaining elements.

- **(a)** [4 pts] Assume that $a_1 \lt a_2$. Show that if there is no 3-chain in our sequence, then $a_3$ must be less than $a_1$. (Hint: consider $a_4$!)

Theorem: If there is no 3-chain in a 5 sequence and $a_1 \lt a_2$, then $a_3$ must be less than $a_1$.

$$\frac{(a_1 \lt a_2), \quad \neg(\textnormal{3-chain})}{a_3 \lt a_1}$$

Let $P = (a_1 \lt a_2) \land \neg(\textnormal{3-chain})$, and let $Q = a_3 \lt a_1$.

Assume $P$.

_Proof_. The proof is by case analisis.

1. $a_3 \lt a_1$ ; since $P$, $Q$. $P$ assures us there is no 3-chain, which says something about the value of $a_4$ (it cannot be greater than $a_2$, that is $a3 \lt a2 \nleq a_4$).

2. $\neg(a_3 \lt a_1) \equiv a_3 \geq a_1$ ; Since $P$, this leaves us $a_1 \leq a_3$. This case doesn't hold, as it contradicts $P$ (which states that there is no 3-chain).

The theorem holds for case 1.

- **(b)** [2 pts] Using the previous part, show that if $a_1 \lt a_2$ and there is no 3-chain in our sequence, then $a_3 \lt a_4 \lt a_2$.

Let $P$ and $Q$ mean the same as in part 1.

Since $P$, case 1 proves this as well, since there is no 3-chain, $a_3 \lt a_2 \nleq a_4$, or $a_3 \lt a_4 \lt a_2$

- **(c)** [2 pts] Assuming that $a_1 \lt a_2$ and $a_3 \lt a_4 \lt a_2$, show that any value of $a_5$ must result in a 3-chain.

| Givens                | Goal                                                   |
| --------------------- | ------------------------------------------------------ |
| $a_1 \lt a_2$         | $\forall x\in \Z(a_5=x) \implies \textnormal{3-chain}$ |
| $a_3 \lt a_4 \lt a_2$ |                                                        |

2 cases:

1. $a_4 \lt a_5$, results in a 3-chain, because $a_3 \lt a_4 \lt a_5$.

2. $a_4 \geq a_5$, also results in a 3-chain, since 3-chains **do not necesarilly have to be contiguous**, this results in 2 subcases:

   2.1 $a_1 \lt a_2 \lt a_5$, which is a 3 chain

   2.2 or $a_1 \lt a_4 \leq a_5 \lt a_2$, which implies the 3-chain $a_1 \lt a_4 \leq a_5$

- **(d)** [4 pts] Using the previous parts, prove by contradiction that any sequence of five distinct integers must containa 3-chain.

**Theorem**: Any sequence of five distinct integers contains a 3-chain

| Givens | Goal                                                                    |
| ------ | ----------------------------------------------------------------------- |
| -      | $\forall s\in S=(s_1,s_2, s_3, s_4, s_5) \implies \textnormal{3-chain}$ |
