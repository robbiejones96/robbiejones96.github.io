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


### 1.13

(a) \\(h\\) makes an error in approximating \\(y\\) when it

* incorrectly approximates \\(f(\mathbf{x})\\) with probability \\(\mu\\), and \\(y = f(\mathbf{x})\\) with probability \\(\lambda\\).
* correctly approximates \\(f(\mathbf{x})\\) with probability \\(1 - \mu\\), and \\(y \neq f(\mathbf{x})\\) with probability \\(1 - \lambda\\).

Therefore \\(\mathbb{P}[h(\mathbf{x}) \neq y] = \mu\lambda + (1 - \mu)(1 - \lambda)\\).

(b) Intuitively, a value of \\(\lambda = 0.5\\) would make learning completely infeasible, since
predicting the value of \\(y\\) is essentially identical to guessing the result of a fair coin flip.
To justify, we plug in \\(\lambda = 0.5\\) to our result from (a) to show

$$
	\mathbb{P}[h(\mathbf{x}) \neq y] = 0.5 * \mu + (1 - \mu) * 0.5 = 0.5.
$$

### Problems 

### 1.1

We denote \\(A\\) as the event where the first ball we choose is black, and \\(B\\) as the event where
the second ball is black.  The quantity we want to compute is \\(\mathbb{P}[B | A]\\), which we can do
using Bayes' Theorm:

$$
	\mathbb{P}[B | A] = \frac{\mathbb{P}[B \cap A]}{\mathbb{P}[A]}.
$$

Assuming there is an equal chance that we pick either bag, then \\(\mathbb{P}[B \cap A] = 0.5\\), since
just one of the bags has two black balls. To calculate \\(\mathbb{P}[A]\\), we notice that if we pick
the bag with two black balls (with probability \\(0.5\\)), then \\(A\\) occurs with probability 1;
otherwise, we pick the second bag with probability \\(0.5\\), and then \\(A\\) occurs with probability
\\(0.5\\) (assuming that we pick the balls uniformly at random). Therefore, our final calculation becomes

$$
	\mathbb{P}[B | A] = \frac{0.5}{0.5 + 0.5 * 0.5} = \frac{2}{3}.
$$

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

We can use the [Cauchy-Schwarz inequality][cauchyschwarz-url] to show \\(\frac{\mathbf{w}^T(t)\mathbf{w}^* }{\|\|\mathbf{w}(t)\|\|} \leq \|\|\mathbf{w}^* \|\|\\), so we conclude that

$$
	t \leq \frac{R^2 ||\mathbf{w}^* ||^2}{\rho^2}.
$$

[cauchyschwarz-url]: https://en.wikipedia.org/wiki/Cauchy%E2%80%93Schwarz_inequality
{:target="_blank"}

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
	\mathbb{P}[u \geq \alpha] &\leq \frac{\mathbb{E}_u \left[\prod_{n = 1}^N e^{su_n}\right]}{e^{Ns\alpha}} \\
	&= \frac{\prod_{n = 1}^N \mathbb{E}_{u_n} \left[e^{su_n}\right]}{e^{Ns\alpha}} \\
	&= \frac{\prod_{n = 1}^N U(s)}{e^{Ns\alpha}} = \left(e^{-s\alpha}U(s)\right)^N.
	\end{align}
$$

Note that we can push the expectation operator into the product because the \\(u_n\\) are iid.

(c) We use the definition of expectation to evaluate

$$
	U(s) = \frac{1}{2} + \frac{1}{2}e^s.
$$

To minimize \\(e^{-s\alpha}U(s)\\), we take the derivative with respect to \\(s\\), set it equal to 0, and solve:

$$
	\begin{align}
		\frac{d}{ds}(e^{-s\alpha}U(s)) = \frac{1}{2}(-\alpha e^{-s\alpha} + (1 - \alpha)e^{(1 - \alpha)s}) &= 0 \\
		e^s &= \frac{\alpha}{1 - \alpha} \\
		s &= \log\left(\frac{\alpha}{1 - \alpha}\right).
	\end{align}
$$

We plug in this value of \\(s\\) to minimize \\(e^{-s\alpha}U(s)\\) and then simplify to make (d) easier:

$$
	\begin{align}
		e^{-\alpha\log\left(\frac{\alpha}{1 - \alpha}\right)}\left(\frac{1}{2}e^{\log\left(\frac{\alpha}{1 - \alpha}\right)} + \frac{1}{2}\right) &= \frac{1}{2}\left(\left(\frac{\alpha}{1 - \alpha}\right)^{1 - \alpha} + \left(\frac{\alpha}{1 -\alpha}\right)^{-\alpha}\right) \\
		&= \frac{1}{2}\left(\alpha^{1 - \alpha}(1 - \alpha)^{-(1 - \alpha)} + \alpha^{-\alpha}(1 - \alpha)^\alpha\right) \\
		&= \frac{1}{2}\left(\alpha^{-\alpha}(1 - \alpha)^{-(1 - \alpha)}(\alpha + (1 - \alpha))\right) \\
		&= \frac{1}{2}\left(\alpha^{-\alpha}(1 - \alpha)^{-(1 - \alpha)}\right).
	\end{align}
$$

(d) We let \\(\alpha = \mathbb{E}(u) + \epsilon = \frac{1}{2} + \epsilon\\), so that \\(1 - \alpha = \frac{1}{2} - \epsilon\\). Note this is valid since \\(0 < \epsilon < \frac{1}{2} \implies 0 < \alpha < 1 \\). Substituting this into our result from (c) and using the exponent-log trick gives us

$$
	\begin{align}
	2^{-1} * 2^{\log_2\left(\frac{1}{2} + \epsilon\right)^{-\left(\frac{1}{2} + \epsilon\right)}} * 2^{\log_2\left(\frac{1}{2} - \epsilon\right)^{-\left(\frac{1}{2} - \epsilon\right)}} &= 2^{-\left(1 + \left(\frac{1}{2} + \epsilon\right)\log_2\left(\frac{1}{2} + \epsilon\right) + \left(\frac{1}{2} - \epsilon\right)\log_2\left(\frac{1}{2} - \epsilon\right)\right)} \\
	&= 2^{-\beta},
	\end{align}
$$

where \\(\beta\\) is defined in the problem statement. Therefore from (b), since the inequality holds for
any \\(s\\), we can conclude

$$
	\mathbb{P}[u \geq \mathbb{E}(u) + \epsilon] \leq 2^{-\beta N}.
$$

By taking derivatives, one can show that the minimum value of \\(\beta\\) occurs at \\(\epsilon = 0\\), so we
conclude \\(\beta > 0\\) for \\(0 < \epsilon < \frac{1}{2}\\), finishing the proof.

### 1.10

(a) To simplify, we assume that all the points in \\(\mathcal{X}\\) are unique, which implies

$$
	E_{\text{off}}(h, f) = \frac{1}{M}\left\lfloor\frac{M}{2}\right\rfloor,
$$

since \\(h\\) makes an error whenever \\(\mathbf{x} = \mathbf{x}_k\\) and \\(k\\) is even.


(b) If \\(f\\) generates \\(\mathcal{D}\\), then its output on the first \\(N\\) points are fixed. There are \\(2^M\\) possible outputs on the remaining \\(M\\) points, so we conclude that there are \\(2^M\\) such \\(f\\).

(c) There are \\(\binom{M}{k}\\) ways for \\(f\\) and \\(h\\) to disagree on \\(k\\) points, which is the same as saying there are \\(\binom{M}{k}\\) choices of \\(f\\) with \\(E_{\text{off}}(h, f) = \frac{k}{M}\\). To check our work, we can use a trick using the binomial theorem to show

$$
	2^M = (1 + 1)^M = \sum_{k = 0}^M \binom{M}{k}.
$$

(d) If every \\(f\\) is equally likely, then the definition of expectation says

$$
	\mathbb{E}_f[E_{\text{off}}(h, f)] = \frac{1}{2^M}\sum_{k = 0}^M \binom{M}{k}\frac{k}{M}.
$$

To simplify even further, we can use the identity \\(\sum_{k = 0}^M k\binom{M}{k} = M2^{M - 1}\\) to show

$$
	\mathbb{E}_f[E_{\text{off}}(h, f)] = \frac{1}{2}.
$$

(d) We note that the expression for the expected off-training-set error does not depend on the hypothesis \\(h\\), so we can conclude that no matter what hypotheses \\(A_1\\) and \\(A_2\\) choose, the expected error will be the same.

### 1.11

(a) This is a classic example of a single-variable function that we can minimize via taking the derivative:

$$
	\begin{align}
		\frac{d}{dh}E_{\text{in}}(h) = 2\sum_{n = 1}^N (h - y_n) &= 0 \\
		Nh - \sum_{n = 1}^N y_n &= 0 \\
		h &= \frac{1}{N}\sum_{n = 1} y_n,
	\end{align}
$$

so we conclude that the value that minimizes \\(E_{\text{in}}(h)\\) is the sample mean.

(b) We can also take the derivative for this form of \\(E_{\text{in}}(h)\\). Using the identity
\\(\frac{d}{dx}|x| = \frac{|x|}{x} = \text{sign}(x)\\), we have

$$
	\frac{d}{dh}E_{\text{in}}(h) = \sum_{n = 1}^N \text{sign}(h - y_n) = 0.
$$

For this quantity to be 0, we must have as many values of \\(h - y_n\\) that are positive as there are negative.
This means \\(h\\) should be the *median* of the \\(y_n\\) (or in the case that \\(N\\) is even, any value in between
the two median values).

(c) It is clear that

$$
	h_{\text{mean}} = \frac{1}{N}\sum_{n = 1}^{N - 1} y_n + y_N + \epsilon \xrightarrow{\epsilon \to \infty} \infty,
$$

while \\(h_{\text{med}}\\) is not affected by this outlier.

