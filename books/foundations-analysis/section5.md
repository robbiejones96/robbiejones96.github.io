---
layout: default
title:  "Foundations of Mathematical Analysis - 5"
---

## Section 5: The Least-Upper-Bound Axiom
### 5.1

Assume for the sake of contradiction that there does not exist such an \\(x\\). That means for all \\(x \in X, x \leq a - \epsilon\\), which contradicts our assumption that \\(a\\) is the least upper bound of \\(X\\).

### 5.3 

Since \\(X\\) is bounded below, there exists some number \\(c \in \mathbb{R}\\) such that \\(c \leq x\\) for all \\(x \in X\\). Thus, \\(-c \geq -x\\) for all \\(-x \in -X\\), so \\(-X\\) is bounded above, and therefore the completeness axiom for the real numbers tells us \\(-X\\) has a least upper bound. We prove that

$$
	-\text{lub}(-X) = \text{glb}X.
$$

Since \\(\text{lub}(-X) \geq -x\\) for all \\(-x \in -X\\), \\(-\text{lub}(-X) \leq x\\) for all \\(x \in X\\) and thus \\(-\text{lub}(-X)\\) is a lower bound for \\(X\\). To prove that \\(-\text{lub}(-X)\\) is the greatest lower bound, assume that there exists \\(g\\) which is a lower bound of \\(X\\) such that \\(g > -\text{lub}(-X)\\). By similar reasoning to above \\(-g\\) must be an upper bound for \\(-x\\). However, we also have that \\(-g < \text{lub}(-X)\\), which contradicts the fact that \\(\text{lub}(-X)\\) is the least lower bound. Therefore, \\(g\\) must be \\(\leq -\text{lub}(-X)\\), so we conclude that \\(-\text{lub}(-X) = \text{glb}X\\).

### 5.5 

Let \\(c\\) be an upper bound for \\(y\\). Then \\(c\\) is also an upper bound for \\(X\\). Otherwise, there exists \\(x \in X\\) such that \\(x > c\\). But because \\(X \subseteq Y\\), \\(x \in Y\\), which contradicts our assumption that \\(c\\) is an upper bound for \\(Y\\). The completeness axiom for real numbers thus tells us that \\(X\\) has a least upper bound.  We now assume that \\(\text{lub}X > \text{lub}Y\\). If we set

$$
	\epsilon = \frac{\text{lub}X - \text{lub}Y}{2}
$$

then 5.1 tells us there exists \\(x \in X\\) such that \\(\text{lub}X - \epsilon < x \leq \text{lub}X\\). But again because \\(X \subseteq Y\\), \\(x \in Y\\), and we thus reach a contradiction because \\(x > \text{lub}Y\\). We therefore conclude that \\(\text{lub}X \leq \text{lub}Y\\).

### 5.6

Since \\(x \leq a\\) for all \\(x \in X\\), we have \\(tx \leq ta\\) for all \\(tx \in tX\\) and thus \\(ta\\) is an upper bound for \\(tX\\). In the case that \\(t = 0\\), it is clear that \\(ta\\) is the least upper bound, since \\(tX\\) is just the set \\(\\{0\\}\\). For \\(t > 0\\), we assume for the sake of contradiction that there exists an upper bound \\(c\\) of \\(tX\\) such that \\(c < ta\\). Since \\(tx \leq c\\) for all \\(tx \in tX\\), we have \\(x \leq \frac{c}{t}\\) for all \\(x \in X\\), and thus \\(\frac{c}{t}\\) is an upper bound for \\(X\\). But we also have \\(\frac{c}{t} < a\\), which contradicts our assumption that \\(a\\) is the least upper bound of \\(X\\). We therefore conclude that \\(\text{lub}(tX) = ta\\). A symmetric argument holds for showing \\(\text{glb}(tX) = ta\\) if \\(t < 0\\).