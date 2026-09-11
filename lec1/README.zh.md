# 第 1 课：二元关系

## 1. 关系的定义

设 $A, B$ 为任意集合，$A \times B$ 的子集 $R$ 称为从 $A$ 到 $B$ 的**二元关系**（或简称**关系**）。
若 $(x, y) \in R$，记作 $x R y$。

## 2. 逆关系的定义

设 $R \subseteq A \times B$ 为关系，**逆关系** $R^{-1} \subseteq B \times A$ 定义为：
$$R^{-1} = \{(y, x) \mid (x, y) \in R\}$$

## 3. 关系的复合

**定义 2.1.3** 给定关系 $R \subseteq A \times B$，$S \subseteq B \times C$，$R$ 和 $S$ 的**复合** $R \circ S$ 是一个从 $A$ 到 $C$ 的关系，定义为：
$$R \circ S = \{(x, z) \mid \exists y \in B,\ (x, y) \in R,\ (y, z) \in S\}$$

---

## 4. 关系运算的性质

设 $R \subseteq A \times B$，$S \subseteq B \times C$，$T \subseteq C \times D$，则：

1. **逆关系的逆**：$(R^{-1})^{-1} = R$
2. **复合的逆**：$(R \circ S)^{-1} = S^{-1} \circ R^{-1}$
3. **结合律**：$(R \circ S) \circ T = R \circ (S \circ T)$
4. **恒等关系**：设 $R$ 为 $A$ 上的任意关系，$I_A \circ R = R \circ I_A = R$，其中 $I_A = \{(x, x) \mid x \in A\}$

### 关系的幂

设 $R$ 为 $A$ 上的关系：
- $R^0 = I_A$
- $R^{n+1} = R^n \circ R$（$n \ge 0$）

---

## 5. 关系的性质

**定义 2.2.1** 设 $R$ 为 $A$ 上的关系。

| 性质 | 定义 |
|------|------|
| **自反性** | $\forall x \in A,\ (x, x) \in R$ |
| **反自反性** | $\forall x \in A,\ (x, x) \notin R$ |
| **对称性** | $\forall (x, y) \in R,\ (y, x) \in R$ |
| **反对称性** | $(x, y) \in R \land (y, x) \in R \implies x = y$ |
| **传递性** | $(x, y) \in R \land (y, z) \in R \implies (x, z) \in R$ |

### 例子

- **自反关系**：$A$ 上的恒等关系 $I_A$、全域关系 $A \times A$、实数上的 $\le$、正整数上的整除关系 $D_{\mathbb{Z}^+}$、集族上的包含关系 $\subseteq$
- **反自反关系**：空关系、小于关系 $<$、大于关系 $>$、真包含关系 $\subset$

---

## 6. 关系性质的特征定理

**定理 2.2.1** 设 $R$ 为 $A$ 上的关系，则：

| 性质 | 集合表达式 | 关系矩阵 $M_R$ | 关系图 |
|------|------------|----------------|--------|
| 自反性 | $I_A \subseteq R$ | 主对角线元素全为 1 | 每个顶点都有自环 |
| 反自反性 | $R \cap I_A = \varnothing$ | 主对角线元素全为 0 | 每个顶点都没有自环 |
| 对称性 | $R = R^{-1}$ | 矩阵是对称矩阵 | 若两顶点间有边，则是一对方向相反的边（无单边） |
| 反对称性 | $R \cap R^{-1} \subseteq I_A$ | 若 $r_{ij} = 1$ 且 $i \ne j$，则 $r_{ji} = 0$ | 若两顶点间有边，则只有一条有向边（无双向边） |
| 传递性 | $R \circ R \subseteq R$ | $M_R^2$ 中 1 所在的位置，$M_R$ 中对应位置也是 1 | 若 $x_i \to x_j$ 有边，$x_j \to x_k$ 有边，则 $x_i \to x_k$ 也有边 |

---

*参考教材：《离散数学》第 2 章 二元关系*
