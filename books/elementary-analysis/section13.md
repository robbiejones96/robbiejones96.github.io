---
layout: default
title:  "Elementary Analysis - 13"
---

## Section 13: Some Topological Concepts in Metric Spaces
### 13.1

(a) **D1** clearly holds, and **D2** is satisfied by the definition of
absolute value.  To prove **D3**, we use the vanilla triangle inequality
we've been using since Chapter 1:

\\(d_1\\): If \\(j = \arg\max\\{\|x_i - z_i\| : i = 1, 2, \ldots k\\}\\), then
\\(\|x_j - z_j\| = d_1(\mathbf{x}, \mathbf{z})\\).  The triangle inequality
tells us that for any \\(i\\),

$$
	\begin{align}
		|x_j - z_j| &= |x_j - y_i + y_i - z_j| \leq |x_j - y_i| + |y_i - z_j| \\
		&\leq d_1(\mathbf{x}, \mathbf{y}) + d_1(\mathbf{y}, \mathbf{z}).
	\end{align}
$$

\\(d_2\\): We can show directly with the triangle inequality that

$$
	\begin{align}
		d_2(\mathbf{x}, \mathbf{z}) &= \sum\limits_{j=1}^k |x_j - z_j|
			= \sum\limits_{j=1}^k |x_j - y_j + y_j - z_j| \\
		&\leq \sum\limits_{j=1}^k \left(|x_j - y_j| + |y_j - z_j|\right)
			= \sum\limits_{j=1}^k |x_j - y_j| + \sum\limits_{j=1}^k |y_j - z_j| \\
		&= d_2(\mathbf{x}, \mathbf{y}) + d_2(\mathbf{y}, \mathbf{z}).
	\end{align}
$$

### 13.2.

(a) The first inequality is true because
\\((x_j - y_j)^2 \leq \sum\limits_{j=1}^k (x_j - y_j)^2\\). Taking the square
root of both sides gives the result. For the second inequality, we have

$$
	\begin{align}
		d(\mathbf{x}, \mathbf{y})^2 &= \sum\limits_{j=1}^k (x_j - y_j)^2 
			\leq \sum\limits_{j=1}^k \max\{(x_j - y_j)^2 : j = 1, 2, \ldots, k\} \\
			&= k\max\{(x_j - y_j)^2 : j = 1, 2, \ldots, k\} \\
		d(\mathbf{x}, \mathbf{y}) &\leq 
			\sqrt{k}\max\{|x_j - y_j| : j = 1, 2, \ldots, k\}
	\end{align}
$$

where the desired inequality holds after taking the square root because
\\(x^2\\) is strictly increasing for \\(x \geq 0\\).

(b) The proof of the first assertion is very similar to that of the second, 
which makes sense since convergence and Cauchy-ness are directly related.
We again use the inequality that we proved in (a).

We first assume \\((\mathbf{x}^{(n)})\\) converges to some \\(\mathbf{x}\\).  
This means that for each \\(\epsilon > 0\\) there exists an \\(N\\) such that
\\(n > N\\) implies \\(d(\mathbf{x}^{(n)}, \mathbf{x})\\ < \epsilon\\).  But 
because of (a), this means \\(n > N\\) implies
\\(|x^{(n)}_j - x_j| < d(\mathbf{x}^{(n)}, \mathbf{x})\\ < \epsilon.\\) So
each sequence \\(x^{(n)}_j \xrightarrow{n\to\infty} x_j\\), and therefore 
converges in \\(\mathbb{R}\\).

We now assume each \\(x^{(n)}_j\\) converges in \\(\mathbb{R}\\) to some
\\(x_j\\). Let \\(\mathbf{x} = (x_1, x_2, \ldots, x_k)\\). For each
\\(\epsilon > 0\\), there exists an \\(N_j\\) such that \\(n > N_j\\)
implies \\(|x^{(n)}_j - x_j| < \frac{\epsilon}{\sqrt{k}}\\).  Let
\\(N = \max\\{N_1, N_2, \ldots, N_k\\}\\). By (1), \\(n > N\\) implies
\\(d(\mathbf{x}^{(n)}, \mathbf{x}) < \epsilon\\), so \\(\mathbf{x^{(n)}}\\)
converges.



### 13.8
(a) To prove open intervals \\((a, b)\\) are open sets in \\(\mathbb{R}\\), 
the important thing to note is that for any \\(x \in (a, b), a \neq x \neq b\\).
Therefore, there exists \\(\epsilon > 0\\) such that
\\(x - \epsilon \in (a, b)\\) and \\(x + \epsilon \in (a, b)\\). We can let
\\(r = \epsilon\\) so that
\\(\\{s \in \mathbb{R} : |x - s| < r\\} \subseteq (a, b)\\). Since this is
true of every element in \\((a, b)\\), we conclude that \\((a, b)\\) is 
open in \\(\mathbb{R}\\).

To prove closed intervals \\([a, b]\\) are closed, we note that its complement
is \\((-\infty, a) \cup (b, \infty)\\). The two individual sets are clearly
open, and the union of any collection of open sets is open, so \\([a, b]\\)
is therefore closed by definition.

To prove the interior of \\([a, b]\\) is \\((a, b)\\), we note that \\((a, b)\\)
is clearly a *subset* of the interior. We must show that the endpoints \\(a\\)
and \\(b\\) are not in the interior. But we can see this because for any
\\(\epsilon > 0, a - \epsilon \in \mathbb{R}\\)
but \\(a - \epsilon \notin [a, b]\\). A symmetric argument works for \\(b\\),
so \\(a\\) and \\(b\\) are not in the interior of \\([a, b]\\).

### 1-5.

We prove the triangle inequality by algebraic manipulation and applying Theorem 1-1(3):

$$ \begin{align} |z - x| &= |(z - y) + (y - x)| \\
	&\leq |z - y| + |y - x| \end{align}$$

Geometrically, we can interpret these distances as the sides of a triangle.
The triangle inequality states that the length of one side of a triangle must
be less than the sum of the other two. In the case of equality, we have a
degenerate triangle that is essentially a line.

### 1-7.

(a) To prove norm preserving implies inner product preserving, we use the
	polarization identity and the linearity of \\( T \\):

$$ \begin{align} \langle Tx, Ty\rangle &= \frac{|Tx + Ty| - |Tx - Ty|}{4} 
	= \frac{|T(x +y)| - |T(x - y)|}{4} \\ 
	&= \frac{|x + y| - |x - y|}{4} \\
	&= \langle x, y \rangle
\end{align}$$
	
The converse is easier to prove:

$$ |T(x)| = \sqrt{\langle Tx, Tx \rangle} = \sqrt{\langle x, x \rangle} = |x| $$

(b) We can prove \\(T\\) is 1-1 by proving its kernel only contains 0:

$$ Tx = 0 \implies |Tx| = 0 \implies |x| = 0 \implies x = 0 $$

where we use the fact that \\(T\\) is norm-preserving.  To prove that
\\(T^{-1}\\) has the same characteristics as \\(T\\), we use the fact that
\\(TT^{-1} = I\\):

$$ |x| = |T(T^{-1}(x))| = |T^{-1}(x)| $$

$$ \langle x, y\rangle = \langle T(T^{-1}x), T(T^{-1}y)\rangle = \langle T^{-1}x, T^{-1}y\rangle $$

### 1-8.

(a) We've proved that norm preserving implies inner product preserving, so

$$ \angle(Tx, Ty) = \arccos\left(\frac{\langle Tx, Ty\rangle}{|Tx|\cdot|Ty|}\right)
	= \arccos\left(\frac{\langle x, y\rangle}{|x|\cdot|y|}\right) = \angle(x, y)$$

### 1-9.
We write \\(x = (x_1, x_2)\\) and show \\(T\\) is norm preserving (and thus
angle preserving):

$$ \begin{align} T(x) &= (x_1\cos\theta + x_2\sin\theta, -x_1\sin\theta + x_2\cos\theta) \\
	|T(x)|^2 &= x_1^2\cos^2\theta + 2x_1x_2\sin\theta\cos\theta + x_2^2\sin^2\theta
		+ x_1^2\sin^2\theta -2x_1x_2\sin\theta\cos\theta + x_2^2\cos^2\theta \\
		&= x_1^2(\sin^2\theta + \cos^2\theta) + x_2^2(\sin^2\theta + \cos^2\theta)
		= x_1^2 + x_2^2 = |x|^2
\end{align}
$$

For the second part, we calculate \\(\langle x, Tx\rangle\\):

$$ \begin{align} \langle x, Tx\rangle &= x_1^2\cos\theta + x_1x_2\sin\theta
	- x_1x_2\sin\theta + x_2^2\cos\theta \\
	&= \cos\theta(x_1^2 + x_2^2) = \cos\theta|x|^2
	\end{align} $$

Since \\(T\\) is norm preserving, we thus have

$$ \begin{align} 
	\angle(x, Tx) &= \arccos\left(\frac{\langle x, Tx\rangle}{|x||Tx|}\right)
	= \arccos\left(\frac{\cos\theta|x|^2}{|x|^2}\right) = \arccos(\cos\theta) \\
	&= \theta
	\end{align} $$

### 1-12.
We use linearity of the inner product to prove the linearity of \\(T\\):

$$ \begin{align}
	T(u + v)(y) &= \varphi_{u + v}(y) = \langle u + v, y\rangle = \langle u, y\rangle
	+ \langle v, y\rangle \\ 
	&= \varphi_u(y) + \varphi_v(y) = T(u)(y) + T(v)(y) \\
	&\implies T(u + v) = T(u) + T(v)
	\end{align}
	$$

$$ \begin{align}
	T(\lambda v)(y) &= \varphi_{\lambda v}(y) = \langle \lambda v, y \rangle 
	= \lambda\langle v, y\rangle \\
	&= \lambda\varphi_v(y) = \lambda T(v)(y) \\
	&\implies T(\lambda v) = \lambda T(v)
\end{align} $$

### 1-13.

This follows from the definition of the norm:

$$ \begin{align} |x + y|^2 &= \sum\limits_{i=1}^n (x_i + y_i)^2 
	= \sum\limits_{i=1}^n x_i^2 + \sum\limits_{i=1}^n y_i^2 + 2\sum\limits_{i=1}^n x_iy_i \\
	&= \sum\limits_{i=1}^n x_i^2 + \sum\limits_{i=1}^n y_i^2
	+ 2\langle x,y\rangle = \sum\limits_{i=1}^n x_i^2 + \sum\limits_{i=1}^n y_i^2\\
	&= |x|^2 + |y|^2
\end{align} $$