---
layout: default
title:  "Foundations of Mathematical Analysis - 11"
---

## Section 11: Subsequences
### 11.5

We prove by induction on \\(n\\).  Clearly \\(f(1) \geq 1\\) since we are mapping from \\(\mathbf{P} \to \mathbf{P}\\). Now we assume that \\(f(n) \geq n\\) for \\(n \in \mathbf{P}\\).  Since \\(f\\) is strictly increasing, we have

$$
	f(n + 1) > f(n) \geq n.
$$

Because \\(f\\) maps from \\(\mathbf{P} \to \mathbf{P}\\), we conclude \\(f(n + 1) \geq n + 1\\).

### 11.6

For \\(\lim_{n \to \infty}\frac{1}{n^2}\\), we define \\(f : \mathbf{P} \to \mathbf{P}\\) as \\(f(n) = n^2\\), which is strictly increasing. Then this sequence is just a subsequence of \\(\\{1/n\\}_{n = 1}^\infty\\) using the function \\(f\\).  Then Theorem 11.2 tells us this subsequence has limit 0.

For the other sequence we can define \\(g : \mathbf{P} \to \mathbf{P}\\) as \\(g(n) = n + 2\\), which is also strictly increasing.  Then we have another subsequence of \\(\\{1/n\\}_{n = 1}^\infty\\), so Theorem 11.2 again tells us this subsequence has limit 0.

### 11.7

By defining two functions \\(f, g : \mathbf{P} \to \mathbf{P}\\) as \\(f(n) = 2n\\) and \\(g(n) = 2n - 1\\) (i.e., mapping to even and odd numbers), we construct two subsequences: the constant sequences 1 and 0. These clearly have two different limits, so we conclude \\(\\{a_n\\}_{n = 1}^\infty\\) does not have a limit.

### 11.8

We identify \\(a_{2n}\\) and \\(a_{2n - 1}\\) as the even and odd terms of \\(a_n\\), respectively.  Thus, for any \\(n \in \mathbf{P}\\), there exists an \\(m \in \mathbf{P}\\) such that \\(n = 2m\\) or \\(n = 2m - 1\\). Let \\(\epsilon > 0\\). By the limit definition, we know that there exists \\(N_1 \in \mathbf{P}\\) such that for \\(2m \geq N_1\\),

$$
	|a_{2m} - L| < \epsilon,
$$

as well as \\(N_2 \in \mathbf{P}\\) such that for \\(2m - 1 \geq N_2\\),

$$
	|a_{2m - 1} - L| < \epsilon.
$$

Since we can identity \\(a_n\\) as one of these two numbers, we have proved

$$
	|a_n - L | < \epsilon,
$$

and therefore \\(\lim_{n \to \infty}a_n = L\\).

