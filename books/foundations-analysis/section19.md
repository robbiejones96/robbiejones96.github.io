---
layout: default
title:  "Foundations of Mathematical Analysis - 19"
---

## Section 19: The Cauchy Condition

### 19.1

Let \\(\epsilon > 0\\). There exists a positive integer \\(N_1\\) such that if \\(m, n \geq N_1\\), then

$$
	|a_m - a_n| < \frac{\epsilon}{2}.
$$

There also exists a positive integer \\(N_2\\) such that if \\(m, n \geq N_2\\), then

$$
	|b_m - b_n| < \frac{\epsilon}{2}.
$$

Therefore, if \\(m, n \geq \max\\{N_1, N_2\\}\\), then

$$
	|(a_m + b_m) - (a_n + b_n)| \leq |a_m - a_n| + |b_m - b_n| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon. 
$$

Similarly, if \\(m, n \geq \max\\{N_1, N_2\\}\\), then

$$
	|(a_m - b_m) - (a_n - b_n)| \leq |a_m - a_n| + |b_n - b_m| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon. 
$$

Now, let \\(N_c\\) be the positive integer such that if \\(m, n \geq N_c\\), then

$$
	|a_m - a_n| < \frac{\epsilon}{|c|}.
$$

This means

$$
	|ca_m - ca_n| = |c||a_m - a_n| < |c|\frac{\epsilon}{|c|} = \epsilon.
$$