---
layout: default
title:  "LA Done Right - 1B"
---

## 1.C Subspaces
### 1

(a) Clearly \\(0 = (0, 0, 0)\\) is an element of this set. Let \\(u, v\\) be
elements of this set.

\\(u + v = (u_1 + v_1, u_2 + v_2, u_3 + v_3)\\), so

$$
	\begin{align}
		(u_1 + v_1) + 2(u_2 + v_2) + 3(u_3 + v_3) &=  
			u_1 + 2u_2 + 3u_3 + v_1 + 2v_2 + 3v_3 \\
		&= 0 + 0 = 0,
	\end{align}
$$

and therefore this set is closed under addition. Similarly,
\\(\lambda u = (\lambda u_1, \lambda u_2, \lambda u_3)\\), so

$$
	\begin{align}
		\lambda u_1 + 2\lambda u_2 + 3\lambda u_3 &=
			\lambda(u_1 + 2u_2 + 3u_3) \\
		&= \lambda(0) = 0,
	\end{align}
$$

and thus this set is closed under scalar multiplication. Therefore, this
subset is a subspace of \\(\mathbf{F}^3\\).

(b) 0 is not an element of this set, so this subset is not a subspace of
\\(\mathbf{F}^3\\).

(c) This subset is not closed under addition.  For example, take
\\(u = (1, 0, 1)\\) and \\(v = (0, 1, 0)\\).

(d) 0 is an element of the set. Let \\(u, v\\) be elements of this set.
\\(u_1 = 5u_3\\) and \\(v_1 = 5v_3\\), so 

$$
	u_1 + v_1 = 5u_3 + 5v_3 = 5(u_3 + v_3),
$$

and therefore this subset is closed under addition.  Similarly,

$$
	\lambda u_1 = \lambda(5u_3) \implies \lambda u_1 = 5\lambda u_3,
$$

so this set is closed under scalar multiplication. Therefore, this subset
is a subspace of \\(\mathbf{F}^3\\).

### 2
(a) Proving that the subset is a subspace if \\(b = 0\\) is nearly identical
to proving (d) from the last question. For the opposite direction, it is
easy to see that if \\(b \neq 0\\), then 0 fails to be an element of the
subset, contradicting our assumption that it is a subspace.

(b) \\(0(x)\\) is continuous everywhere, so it is an element of this subset.
The sum of continuous functions is continuous, so for any continuous
\\(f, g\\) defined on \\([0, 1], f + g\\) is continuous on \\([0, 1]\\).
\\(\lambda f\\) is also continuous on \\([0, 1]\\), so this subset is
closed under addition and scalar multiplication and is therefore a 
subspace of \\(\mathbf{R}^{[0, 1]}\\).

(c) \\(0(x)\\) is also differentiable everywhere, so it is an element of this
subset. The sum and scalar product of differentiable functions are also
differentiable, so this subset is closed under addition and scalar
multiplication and is therefore a subspace of \\(\mathbf{R}^\mathbf{R}\\).

(d) If \\(b = 0\\), then \\(0(x)\\) is an element of the subset (because it
is differentiable everywhere with derivative 0). For any functions \\(f, g\\)
of this subset, \\(f'(2) + g'(2) = 0 + 0 = 0\\), so this subset is closed
under addition. Similarly, \\(\lambda f'(2) = 0\\), so this subset is closed
under scalar multiplication and is therefore a subset of
\\(\mathbf{R}^{(0, 3)}\\).

To prove the opposite direction, it is easy to see that if \\(b \neq 0\\),
then \\(0(x)\\) fails to be an element of this subset, contradicting our
assumption that this subset was a subspace.

(e) \\(0 = (0, 0, \ldots)\\) clearly has limit 0, so it is an element of this
subspace. For any two sequences \\((a_n), (b_n)\\) in this subset, 

$$
	\lim_{n\to\infty}(a_n + b_n) = 
		\lim_{n\to\infty} a_n + \lim_{n\to\infty} b_n = 0 + 0 = 0,
$$

so this subset is closed under addition. The scalar multiplication of any
sequence in this subset will also have limit 0, so this subset is closed under
scalar multiplication and is therefore a subspace of \\(\mathbf{C}^\infty\\).

### 3

\\(0(x)\\) with derivative \\(0\\) satisfies the given condition and is
therefore an element of this subset. For any pair of functions \\(f, g\\)
in this subset, if \\(h = f + g\\), then

$$
	h'(-1) = f'(-1) + g'(-1) = 3f(2) + 3g(2) = 3h(2),
$$

so this subset is closed under addition. Similarly, if \\(h = \lambda f\\),
then

$$
	h'(-1) = \lambda f'(-1) = \lambda(3f(2)) 3h(2),
$$

so this subset is closed under scalar multiplication and is therefore a
subspace of \\(\mathbf{R}^{(-4, 4)}\\).

### 4

If \\(b = 0\\), then \\(\int\limits_0^1 0 = 0\\), so \\(0(x)\\) is an element
of this subset. For any pair of functions \\(f, g\\) in this subset, we have

$$
	\int\limits_0^1 (f + g) = \int\limits_0^1 f + \int\limits_0^1 g
		= 0 + 0 = 0,
$$

so this subset is closed under addition. Similarly, 
\\(\int\limits_0^1 \lambda f = \lambda\int\limits_0^1 f = 0\\), so this subset
is closed under scalar multiplication and is therefore a subspace of
\\(\mathbf{R}^{[0, 1]}\\). For the opposite direction, it is easy to see that
if \\(b \neq 0\\), then \\(0(x)\\) is not an element of the subset.

### 5
For \\(\mathbf{R}^2\\) to be a subspace of \\(\mathbf{C}^2\\), we require
\\(\mathbf{R}^2\\) to be closed using the same scalar multiplication as
defined on \\(\mathbf{C}^2\\). But for \\(r \in \mathbf{R}^2\\), 
\\(\lambda r \notin \mathbf{R}^2\\) if
\\(\lambda \in \mathbf{C} / \mathbf{R}\\), so this subset is not closed under
the scalar multiplication rules of \\(\mathbf{C}^2\\) and is therefore not
a subspace of \\(\mathbf{C}^2\\).

### 8
The subset defined in 1(c) is closed under scalar multiplication
(clearly \\(\lambda x_1x_2x_3 = 0\\) if \\(x_1x_2x_3 = 0)\\), but we showed it
is not closed under addition.

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