---
layout: default
title:  "Elementary Analysis - 4"
---

## Section 4: The Completeness Axiom

### 4.6

(a) For any element \\(s \in S\\), we have \\(\inf{S} \leq s \leq \sup{S}\\).
We conclude \\(\inf{S} \leq \sup{S}\\).

(b) We prove \\(S\\) only has one element. Assume for the sake of contradiction
that \\(S\\) has two elements \\(s_1, s_2\\). Without loss of generality,
assume \\(s_1 < s_2\\). We have \\(\inf{S} = s_1 < s_2 = \sup{S}\\), a
contradiction.

### 4.7

(a) The inner and outer inequalities are proven by 4.6. To prove
\\(\inf T \leq \inf S\\), assume for the sake of contradiction that
\\(\inf T > \inf S\\). This means there exists an element \\(s \in S\\)
such that \\(\inf S \leq s < \inf T\\); otherwise, \\(\inf S\\) would not be
the greatest lower bound.  But \\(S \subseteq T\\), so \\(s \in T\\), giving
us a contradiction because \\(s < \inf T\\). Therefore,
\\(\inf T \leq \inf S\\). A symmetric argument can be made for the last
inequality.

(b) Without loss of generality, assume
\\(\max\\{\sup{S}, \sup{T}\\} = \sup{S}\\), i.e., \\(\sup{S} \geq \sup{T}\\).

To prove \\(\sup{S} \geq \sup(S \cup T)\\), we let \\(x \in S \cup T\\).  If
\\(x \in S\\), we have \\(x \leq \sup{S}\\). If \\(x \in T\\), then we have
\\(x \leq \sup{T} \leq \sup{S}\\). Therefore, \\(\sup{S}\\) is an upper bound
for \\(S \cup T\\), so we conclude \\(\sup{S} \geq \sup(S \cup T)\\).

To prove \\(\sup{S} \leq \sup(S \cup T)\\), let \\(s \in S\\).
\\(s \in S \implies s \in S \cup T \implies s \leq \sup(S \cup T)\\), so we
conclude \\(\sup(S \cup T)\\) is an upper bound for \\(S\\) and thus
\\(\sup{S} \leq \sup(S \cup T)\\). Therefore,
\\(\sup(S \cup T) = \max\\{\sup{S}, \sup{T}\\}\\).

### 4.8

(b) We prove \\(\inf{T}\\) is an upper bound for \\(S\\). Assume for the sake
of contradiction that there exists \\(s \in S\\) such that \\(\inf{T} < s\\).
This means there exists \\(t \in T\\) such that \\(\inf{T} \leq t < s\\);
otherwise, \\(\inf{T}\\) would not be the greatest lower bound of \\(T\\).
But \\(t < s\\) contradicts the property of \\(S\\) and \\(T\\), so we conclude
that \\(s \leq \inf{T}\\) for all \\(s \in S\\), and therefore
\\(\sup{S} \leq \inf{T}\\).

(c) \\(S = \\{0, 1\\}, T = \\{1, 2\\}\\).

(d) \\(S = (0, 1), T = (1, 2)\\).


### 4.9

We again let \\(s_0 = \sup(-S)\\). This means for all
\\(-s \in -S, s_0 \geq -s\\), and therefore \\(-s_0 \leq s\\) for all
\\(s \in S\\).

Now assume there is some \\(t\\) such that \\(t \leq s\\) for all
\\(s \in S\\). For the sake of contradiction, assume \\(t > -s_0\\). Our
assumption tells us \\(-t \geq -s\\), i.e., \\(-t\\) is an upper bound for
the set \\(-S\\). But \\(t > -s_0 \implies -t < s_0\\), contradicting the fact
that \\(s_0\\) is the least upper bound for \\(-S\\). Therefore,
\\(t \leq -s_0\\), so we conclude \\(\inf{S} = -\sup(-S)\\).