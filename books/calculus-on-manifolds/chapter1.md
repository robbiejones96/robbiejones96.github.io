---
layout: default
title:  "Calculus on Manifolds"
---

## Chapter 1: Functions on Euclidean Space
### 1-1.

We notice \\( \|x\| \leq \sum\limits_{i=1}^n \|x_i\| \\) if and only if
\\(\|x\|^2 \leq \left(\sum\limits_{i=1}^n \|x_i\|\right)^2 \\).  Expanding the right side gives us

$$ \begin{align} \left(\sum\limits_{i=1}^n |x_i|\right)^2 &=
	\sum\limits_{i=1}^n x_i^2 + \sum\limits_{i\neq j} |x_i||x_j| \\ 
	&\geq \sum\limits_{i=1}^n x_i^2  = |x|^2 \end{align}$$

### 1-2.

Looking back at the proof of 1-1(3), we see equality holds when 
\\(\sum\limits_{i=1}^n x_iy_i = \|x\|\|y\|\\), which is a stricter condition
than that of 1-1(2). This happens if and only if \\(x\\) and \\(y\\) are
non-negative multiples of each other.

### 1-3.

Theoretically we could write \\(\|x - y\| = \|x + (-y)\|\\) and use 1-1(3), but
proving from the definition of the norm and using 1-1(2) makes it clear when
equality holds:

$$ \begin{align}
	|x - y|^2 &= \sum\limits_{i = 1}^n (x_i - y_i)^2 = \sum\limits_{i=1}^n x_i^2
		+ \sum\limits_{i=1}^n y_i^2 - 2\sum\limits_{i=1}^n x_iy_i \\
		&\leq \sum\limits_{i=1}^n x_i^2 + \sum\limits_{i=1}^n y_i^2 
		+ 2|x||y| = (|x| + |y|)^2
	\end{align}
$$

where we again use 1-1(2) to get the bound. So equality holds if and only if
\\(-\sum\limits_{i=1}^n x_iy_i = |x||y|\\), i.e., \\(x\\) and \\(y\\) are 
non-*positive* multiples of each other.

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