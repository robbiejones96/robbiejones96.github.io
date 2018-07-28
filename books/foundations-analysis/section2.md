---
layout: default
title:  "Foundations of Mathematical Analysis - 2"
---

## Section 2: Functions
### 2.6

We first assume that \\(f(A \cap B) = f(A) \cap f(B)\\) for all subsets \\(A, B\\) of \\(X\\), but \\(f\\) is not one-to-one.  This means there exists \\(x \neq y \in X\\) where \\(f(x) = f(y)\\). Therefore, \\(f(\\{x\\}) \cap f(\\{y\\}) = \\{f(x)\\}\\), while \\(f(\\{x\\} \cap \\{y\\}) = f(\varnothing) = \varnothing\\), which is a contradiction, so \\(f\\) must be one-to-one.

We now assume \\(f\\) is one-to-one and prove that \\(f(A \cap B) = f(A) \cap f(B)\\) for all subsets \\(A, B\\) of \\(X\\). We first let \\(f(x) \in f(A \cap B)\\), so \\(x \in A \cap B\\). Then \\(x \in A\\) and \\(x \in B \implies f(x) \in f(A)\\) and \\(f(x) \in f(B) \implies f(x) \in f(A) \cap f(B)\\), so \\(f(A \cap B) \subseteq f(A) \cap f(B)\\).  For the other direction, assume \\(f(x) \in f(A)\\) and \\(f(y) \in f(B)\\), where \\(f(x) = f(y)\\) for some \\(x \in A\\) and \\(y \in B\\). Since \\(f\\) is one-to-one, this means \\(x = y \implies x \in A \cap B \implies f(x) \in f(A \cap B)\\), so \\(f(A) \cap f(B) \subseteq f(A \cap B)\\), and we thus conclude that \\(f(A \cap B) = f(A) \cap f(B)\\).