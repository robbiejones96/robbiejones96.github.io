---
layout: default
title:  "Foundations of Mathematical Analysis - 10"
---

## Section 10: Sequences of Real Numbers
### 10.1

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{1}{\epsilon}\\). Therefore for \\(n \geq N\\),

$$
	\left|\frac{1}{n}\right| = \frac{1}{n} \leq \frac{1}{N} < \epsilon.	
$$

### 10.2

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{1}{2\epsilon}\\).

Therefore for \\(n \geq N\\),

$$
	\left|\frac{1}{2n}\right| = \frac{1}{2n} \leq \frac{1}{2N} < \epsilon.	
$$

### 10.3

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{1}{\epsilon}\\).

Therefore for \\(n \geq N\\),

$$
	\left|\frac{1}{n + 2}\right| = \frac{1}{n + 2} < \frac{1}{n} \leq \frac{1}{N} < \epsilon.	
$$

### 10.4

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{1}{\epsilon}\\).

Therefore for \\(n \geq N\\),

$$
	\left|2 - \frac{1}{n} - 2\right| = \frac{1}{n} \leq \frac{1}{N} < \epsilon.
$$

### 10.5

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{2}{\epsilon}\\).

Therefore for \\(n \geq N\\),

$$
	\begin{align}
		\left|\frac{n}{n + 2} - 1\right| &= \left|\frac{n}{n + 2} - \frac{n + 2}{n + 2}\right| = \frac{2}{n + 2} \\
		&< \frac{2}{n} \leq \frac{2}{N} < \epsilon.
	\end{align}
$$

### 10.6

Let \\(\epsilon > 0\\), and let \\(N \in \mathbf{P}\\) such that \\(N > \frac{4}{\epsilon}\\).

Therefore for \\(n \geq N\\),

$$
	\begin{align}
		\left|\frac{2n}{n + 2} - 2\right| &= \left|\frac{2n}{n + 2} - \frac{2n + 4}{n + 2}\right| = \frac{4}{n + 2} \\
		&< \frac{4}{n} \leq \frac{4}{N} < \epsilon.
	\end{align}
$$

### 10.7

We note that for any \\(n\\),

$$
	\left|\frac{(-1)^n}{n}\right| = \frac{1}{n},
$$

so the proof proceeds exactly like that of 10.1.

### 10.11

Let \\(\epsilon > 0\\). Since \\(\lim_{n \to \infty}a_n = L\\), there exists some \\(N' \in \mathbf{P}\\) such that for all \\(n \geq N'\\),

$$
	|a_n - L| < \epsilon.
$$

If we let \\(N_0 = \max\\{N, N'\\}\\), then we have for all \\(n \geq N_0\\),

$$
	|a_n - L| = |b_n - L| < \epsilon,
$$

so we conclude \\(\lim_{n \to \infty}b_n = L\\).