---
layout: math
title:  "Learning From Data - 1"
---

## Chapter 1: The Learning Problem

### Exercises

### 1.3

(a) If \\(\mathbf{x}(t)\\) is misclassified, we either have \\(y(t) = 1\\) and \\(\text{sign}(\mathbf{w}^T(t)\mathbf{x}(t)) < 0\\), or \\(y(t) = -1\\) and \\(\text{sign}(\mathbf{w}^T(t)\mathbf{x}(t)) > 0\\). In either case, \\(y(t)\mathbf{w}^T(t)\mathbf{x}(t) < 0\\).

(b) Substituting the update rule for \\(\mathbf{w}^T(t + 1)\\), we have

$$
	\begin{align}
		y(t)\mathbf{w}^T(t + 1)\mathbf{x}(t) &= y(t)(\mathbf{w}(t) + y(t)\mathbf{x}(t))^T\mathbf{x}(t) \\
		&= y(t)\mathbf{w}^T(t)\mathbf{x}(t) + y^2(t)\mathbf{x}^T(t)\mathbf{x}(t) \\
		&= y(t)\mathbf{w}^T(t)\mathbf{x}(t) + y^2(t)||\mathbf{x}(t)||^2 \\
		&> y(t)\mathbf{w}^T(t)\mathbf{x}(t),
	\end{align}
$$

where we use the fact that \\(y^2(t)\|\|\mathbf{x}(t)\|\|^2\\) is strictly positive.

(c) Since a correctly classified data point has \\(y(t)\mathbf{w}^T(t)\mathbf{x}(t) > 0\\), it makes sense to change our weight vector such that this quantity increases.

### 1.4

Check out my jupyter notebook [here](https://github.com/robbiejones96/LearningFromDataExercises/blob/master/LearningFromDataEx1-4.ipynb){:target="_blank"}.


### Problems 

### 1.3

(a) Since \\(\mathbf{w}^* \\) separates the data, we know that for \\(n = 1, \ldots, N\\), 

$$
	\begin{align}
		{\mathbf{w}^* }^Tx_n &> 0 \text{ if } y_n = 1 \\
		{\mathbf{w}^* }^Tx_n &< 0 \text{ if } y_n = -1, \\
	\end{align}
$$

so it is immediately clear that \\(y_n({\mathbf{w}^* }^Tx_n) > 0\\) for \\(n = 1, \ldots, N\\).  We conclude that \\(\rho = \min_{1 \leq n \leq N}y_n({\mathbf{w}^* }^Tx_n) > 0\\).

(b) We can prove the first statement directly.  Using our update rule for \\(\mathbf{w}(t)\\), we have

$$
	\begin{align}
		\mathbf{w}^T(t)\mathbf{w}^* &= (\mathbf{w}(t - 1) + y(t)\mathbf{x}(t - 1))^T\mathbf{w}^* \\
		&= \mathbf{w}^T(t - 1)\mathbf{w}^* + y(t)(\mathbf{x}^T(t - 1)\mathbf{w}^* ) \\
		&\geq \mathbf{w}^T(t - 1)\mathbf{w}^* + \rho,
	\end{align}
$$

where the inequality comes from the fact that \\(\rho \leq y(t)(\mathbf{x}^T(t - 1)\mathbf{w}^* )\\).

We prove the second statement by induction.  For \\(t = 1\\), note that

$$
	\mathbf{w}^T(1)\mathbf{w}^* \geq \mathbf{w}^T(0)\mathbf{w}^* + \rho = \rho
$$

since \\(\mathbf{w}(0) = \mathbf{0}\\).  For the inductive step, we assume the inequality holds for \\(t - 1\\), which allows us to write

$$
	\mathbf{w}^T(t)\mathbf{w}^* \geq \mathbf{w}^T(t - 1)\mathbf{w}^* + \rho \geq (t - 1)\rho + \rho = t\rho.
$$

(c) We again use our update rule for \\(\mathbf{w}(t)\\) to write

$$
	\begin{align}
		||\mathbf{w}(t)||^2 &= (\mathbf{w}(t - 1) + y(t)\mathbf{x}(t - 1))^T(\mathbf{w}(t - 1) + y(t)\mathbf{x}(t - 1)) \\
		&= ||\mathbf{w}(t - 1)||^2 + 2y(t - 1)(\mathbf{w}^T(t - 1)\mathbf{x}(t - 1)) + y(t - 1)^2||\mathbf{x}(t - 1)||^2 \\
		&\leq ||\mathbf{w}(t - 1)||^2 + ||\mathbf{x}(t - 1)||^2,
	\end{align}
$$

where we use the hint and the fact that \\(y^2 = 1\\).

(d) For \\(t = 1\\), we have

$$
	||\mathbf{w}(1)||^2 \leq ||\mathbf{w}(0)||^2 + ||\mathbf{x}(0)||^2 = ||\mathbf{x}(0)||^2 \leq R^2.
$$

Assuming the inequality holds for \\(t - 1\\), it follows that

$$
	||\mathbf{w}(t)||^2 \leq ||\mathbf{w}(t - 1)||^2 + ||\mathbf{x}(t - 1)||^2 \leq (t - 1)R^2 + R^2 = tR^2.
$$

(e) Combining and rearranging gives us

$$
	\begin{align}
		\sqrt{t}R\mathbf{w}^T(t)\mathbf{w}^* \geq t\rho||\mathbf{w}(t)|| \\
		\frac{\mathbf{w}^T(t)\mathbf{w}^* }{||\mathbf{w}(t)||} \geq \sqrt{t}\frac{\rho}{R}.
	\end{align}
$$

We can use the Cauchy-Schwarz inequality to show \\(\frac{\mathbf{w}^T(t)\mathbf{w}^* }{\|\|\mathbf{w}(t)\|\|} \leq \|\|\mathbf{w}^* \|\|\\), so we conclude that

$$
	t \leq \frac{R^2 ||\mathbf{w}^* ||^2}{\rho^2}.
$$

### 1.8 

(a)  (Note: this inequality is known as Markov's inequality).

 We denote the density function of \\(t\\) as \\(f\\), which gives us

$$
	\mathbb{P}[t \geq \alpha] = \int_\alpha^\infty f(t)dt.
$$


Since \\(t \geq \alpha \implies \frac{t}{\alpha} \geq 1\\), we have

$$
	\int_\alpha^\infty f(t)dt \leq \int_\alpha^\infty \frac{t}{\alpha}f(t)dt.
$$

Finally, since \\(\frac{t}{\alpha} \geq 0\\), it follows that

$$
	\int_\alpha^\infty \frac{t}{\alpha}f(t)dt \leq \int_0^\alpha \frac{t}{\alpha}f(t)dt + \int_\alpha^\infty \frac{t}{\alpha}f(t)dt = \int_0^\infty \frac{t}{\alpha}f(t)dt.
$$

Altogether, we have shown

$$
	\mathbb{P}[t \geq \alpha] \leq \int_0^\infty \frac{t}{\alpha}f(t)dt = \frac{\mathbb{E}[t]}{\alpha}.
$$

(b) We can prove this inequality by utilizing Markov's inequality.  Note that

$$
	\mathbb{E}[(u - \mu)^2] = \mathbb{E}[(u - \mathbb{E}[u])^2] = \text{Var}(u), 
$$

so Markov's inequality tells us

$$
	\mathbb{P}[(u - \mu)^2 \geq \alpha] \leq \frac{\mathbb{E}[(u - \mu)^2]}{\alpha} = \frac{\text{Var}(u)}{\alpha} = \frac{\sigma^2}{\alpha}.
$$

(c) We can again prove this inequality using Markov's inequality, since linearity of expectation tells us

$$
	\mathbb{E}[u] = \mathbb{E}\left[\frac{1}{N}\sum_{n = 1}^N u_n\right] = \frac{1}{N}\sum_{n = 1}^N \mathbb{E}[u_n] = \mu.
$$

Remember that independent random variables are also uncorrelated, so taking the variance of \\(u\\) gives us

$$
	\text{Var}(u) = \text{Var}\left(\frac{1}{N}\sum_{n = 1}^N u_n\right) = \frac{1}{N^2}\sum_{n = 1}^N \text{Var}(u_n) = \frac{\sigma^2}{N}.
$$

We then apply Markov's inequality as we did in (b), and the inequality immediately follows.

### 1.9

(a) Note that because \\(s > 0\\) and the exponential function is monotonically increasing, we have

$$
	\mathbb{P}[t \geq \alpha] = \mathbb{P}[st \geq s\alpha] = \mathbb{P}[e^{st} \geq e^{s\alpha}].
$$

Applying Markov's inequality to this probability gives us

$$
	\mathbb{P}[t \geq \alpha] \leq \frac{\mathbb{E}_t[e^{st}]}{e^{s\alpha}} = e^{-s\alpha}T(s).  
$$

(b) We apply a similar transformation as in part (a) and expand the definition of \\(u\\) to write

$$
	\mathbb{P}[u \geq \alpha] = \mathbb{P}\left[e^{s\frac{1}{N}\sum_{n = 1}^N u_n} \geq e^{s\alpha}\right] = \mathbb{P}\left[e^{\sum_{n = 1}^N su_n} \geq e^{Ns\alpha}\right] = \mathbb{P}\left[\prod_{n = 1}^N e^{su_n} \geq e^{Ns\alpha}\right].
$$

Applying Markov's inequality gives us the result:

$$
	\begin{align}
	\mathbb{P}[t \geq \alpha] &\leq \frac{\mathbb{E}_u \left[\prod_{n = 1}^N e^{su_n}\right]}{e^{Ns\alpha}} \\
	&= \frac{\prod_{n = 1}^N \mathbb{E}_{u_n} \left[e^{su_n}\right]}{e^{Ns\alpha}} \\
	&= \frac{\prod_{n = 1}^N U(s)}{e^{Ns\alpha}} = \left(e^{-s\alpha}U(s)\right)^N.
	\end{align}
$$

Note that we can push the expectation operator into the product because the \\(u_n\\) are iid.


