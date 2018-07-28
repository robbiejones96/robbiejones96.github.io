---
layout: default
title:  "Foundations of Mathematical Analysis - 3"
---

### Section 3: “The Algebraic Axioms of the Real Numbers”

### 3.1
Let \\(x, y, z \in \mathbb{R}\\) such that \\(x + y = 0\\) and \\(x + z = 0\\) (i.e., \\(y\\) and \\(z\\) are additive inverses of \\(x\\)). Then we have

$$
	\begin{align}
		y + x + z &= y + x + z \\
		(y + x) + z &= y + (x + z) \\
		0 + z &= y + 0 \\
		z &= y,
	\end{align}
$$

so we conclude the additive inverse is unique.

### 3.3

Since \\(-(-x) + -x = 0\\) and \\(-x + x = 0\\), we have

$$
	\begin{align}
		-(-x) + -x &= -x + x \\
		-(-x) + -x + x &= -x + x + x \\
		-(-x) + (-x + x) &= (-x + x) + x \\
		-(-x) &= x
	\end{align}
$$

### 3.4

It's easy to check that both of these quantities are additive inverses of \\(x + y\\), so from 3.1 we conclude they are equal.

### 3.5 

\\(x = 0\\) or \\(y = 0\\) implies \\(xy = 0\\) from Theorem 3.4, so we just need to prove the other direction.  For the sake of contradiction, we assume \\(xy = 0\\), but \\(x\\) and \\(y\\) are both nonzero. We thus have

$$
	\begin{align}
		xy &= 0 \\
		\frac{1}{x} * xy &= \frac{1}{x} * 0 \\
		1 * y &= 0 \\
		y &= 0,
	\end{align}
$$

which is a contradiction, so we conclude \\(x = 0\\) or \\(y = 0\\).

### 3.6

$$
	\begin{align}
		xy &= xz \\
		\frac{1}{x} * xy &= \frac{1}{x} * xz \\
		1 * y &= 1 * z\\
		y &= z
	\end{align}
$$