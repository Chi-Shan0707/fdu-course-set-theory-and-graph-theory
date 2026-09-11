# Lesson 1: Binary Relations

## 1. Definition of a Relation

Let $A$ and $B$ be arbitrary sets. Any subset $R$ of $A \times B$ is called a **binary relation** (or simply a **relation**) from $A$ to $B$.
If $(x, y) \in R$, we write $x R y$.

## 2. Definition of Inverse Relation

Let $R \subseteq A \times B$ be a relation. The **inverse relation** $R^{-1} \subseteq B \times A$ is defined by:
$$R^{-1} = \{(y, x) \mid (x, y) \in R\}$$

## 3. Composition of Relations

**Definition 2.1.3** Given relations $R \subseteq A \times B$ and $S \subseteq B \times C$, the **composition** $R \circ S$ is a relation from $A$ to $C$, defined by:
$$R \circ S = \{(x, z) \mid \exists y \in B,\ (x, y) \in R,\ (y, z) \in S\}$$

---

## 4. Properties of Relation Operations

Let $R \subseteq A \times B$, $S \subseteq B \times C$, and $T \subseteq C \times D$. Then:

1. **Inverse of inverse**: $(R^{-1})^{-1} = R$
2. **Inverse of composition**: $(R \circ S)^{-1} = S^{-1} \circ R^{-1}$
3. **Associativity**: $(R \circ S) \circ T = R \circ (S \circ T)$
4. **Identity relation**: For any relation $R$ on $A$, $I_A \circ R = R \circ I_A = R$, where $I_A = \{(x, x) \mid x \in A\}$

### Powers of a Relation

Let $R$ be a relation on $A$:
- $R^0 = I_A$
- $R^{n+1} = R^n \circ R$ for $n \ge 0$

---

## 5. Properties of Relations

**Definition 2.2.1** Let $R$ be a relation on $A$.

| Property | Definition |
|------|------|
| **Reflexive** | $\forall x \in A,\ (x, x) \in R$ |
| **Irreflexive** | $\forall x \in A,\ (x, x) \notin R$ |
| **Symmetric** | $\forall (x, y) \in R,\ (y, x) \in R$ |
| **Antisymmetric** | $(x, y) \in R \land (y, x) \in R \implies x = y$ |
| **Transitive** | $(x, y) \in R \land (y, z) \in R \implies (x, z) \in R$ |

### Examples

- **Reflexive relations**: the identity relation $I_A$ on $A$, the universal relation $A \times A$, $\le$ on real numbers, the divisibility relation $D_{\mathbb{Z}^+}$ on positive integers, and $\subseteq$ on families of sets
- **Irreflexive relations**: the empty relation, $<$, $>$, and proper subset $\subset$

---

## 6. Characterization Theorems for Relation Properties

**Theorem 2.2.1** Let $R$ be a relation on $A$. Then:

| Property | Set Expression | Relation Matrix $M_R$ | Relation Digraph |
|------|------------|----------------|--------|
| Reflexive | $I_A \subseteq R$ | All diagonal entries are 1 | Every vertex has a self-loop |
| Irreflexive | $R \cap I_A = \varnothing$ | All diagonal entries are 0 | No vertex has a self-loop |
| Symmetric | $R = R^{-1}$ | The matrix is symmetric | Any edge appears with its reverse edge (no one-way edge) |
| Antisymmetric | $R \cap R^{-1} \subseteq I_A$ | If $r_{ij} = 1$ and $i \ne j$, then $r_{ji} = 0$ | Between two vertices, at most one directed edge exists (no two-way edge) |
| Transitive | $R \circ R \subseteq R$ | Wherever $M_R^2$ has 1, $M_R$ has 1 at the same position | If $x_i \to x_j$ and $x_j \to x_k$, then $x_i \to x_k$ |

---

*Reference: Chapter 2 (Binary Relations), Discrete Mathematics*
