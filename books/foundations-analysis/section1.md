---
layout: default
title:  "Foundations of Mathematical Analysis - 1"
---

## Section 1: Sets
### 1.2.

Let \\(x \in (A \cap B)'\\). Then \\(x \not\in A \cap B\\), so either \\(x \not\in A\\) or \\(x \not\in B\\) (or both). Either way, \\(x\\) must be an element of \\(A' \cup B'\\), so we conclude \\((A \cap B)' \subseteq A' \cup B'\\).

Now we let \\(x \in A' \cup B'\\). Then \\(x \not\in A\\) or \\(x \not\in B\\) (or both), so \\(x \not\in A \cap B\\). Thus, \\(x \in (A \cap B)'\\), so \\(A' \cup B' \subseteq (A \cap B)'\\), and therefore \\((A \cap B)' = A' \cup B'\\).

### 1.4 

\\(A = \varnothing \implies A \subseteq \varnothing\\) follows immediately from the definition of set equality.  To prove the other direction, we note that \\(\varnothing \subseteq A\\) is vacuously true, and thus assuming \\(A \subseteq \varnothing\\) gives the result.

### 1.5

\\(x \in A \implies x \in B \implies x \in C \implies A \subseteq C\\).

### 1.10

\\(x \in (A')' \implies x \not\in A' \implies x \in A \implies (A')' \subseteq A\\), while \\(x \in A \implies x \not\in A' \implies x \in (A')' \implies A \subseteq (A')'\\), so we conclude \\((A')' = A\\).

### 1.11

Assume for the sake of contradiction that \\(x \in B'\\), but \\(x \not\in A'\\). This means \\(x \in A\\) but \\(x \not\in B\\), which contradicts our assumption that \\(A \subseteq B\\). Therefore, \\(B' \subseteq A'\\).