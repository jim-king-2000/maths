# 群论 (Group Theory)

## 1. 群的定义

### 1.1 基本公理

群(Group)是一个集合 $G$ 与其上的二元运算符 $\cdot$ 组成的二元组 $(G, \cdot)$，且必须满足以下四条公理：

1. **封闭性 (Closure)**
   $\forall a, b \in G \implies a \cdot b \in G$

2. **结合律 (Associativity)**
   $\forall a, b, c \in G \implies (a \cdot b) \cdot c = a \cdot (b \cdot c)$

3. **单位元 (Identity)**
   $\exists e \in G, \text{ 使得 } \forall a \in G, e \cdot a = a \cdot e = a$

4. **逆元 (Inverse)**
   $\forall a \in G, \exists a^{-1} \in G, \text{ 使得 } a \cdot a^{-1} = a^{-1} \cdot a = e$

群 $G$ 中元素的个数称为**群的阶 (Order of a Group)**，记作 $|G|$ 或 $o(G)$。

> **重点注意**：
> 即使在**非阿贝尔群**（不满足交换律 $a \cdot b \neq b \cdot a$）中，单位元与逆元也具有**双边性 (Two-sidedness)**：
>
> - 单位元必须同时是左单位元和右单位元($e \cdot a = a \cdot e = a$)。
> - 逆元必须同时是左逆元和右逆元($a^{-1} \cdot a = a \cdot a^{-1} = e$)。

### 1.2 分类

- **按阶数分类**：若群中的元素个数为有限个，称为**有限群 (Finite Group)**；若为无限个，则称为**无限群 (Infinite Group)**。
- **按可交换性分类**：若群满足交换律($\forall a, b \in G \implies a \cdot b = b \cdot a$)，称为**阿贝尔群 (Abelian Group)** / 交换群；否则称为**非阿贝尔群 (Non-Abelian Group)**。

### 1.3 典型例子

**例子 1：无限阿贝尔群**
整数集 $\mathbb{Z} = \lbrace \dots, -2, -1, 0, 1, 2, \dots \rbrace$ 与常规加法 $+$ 构成群 $(\mathbb{Z}, +)$：

- **类型**：无限群、阿贝尔群。
- **单位元**： $0$ (满足 $k + 0 = 0 + k = k$)。
- **逆元**：任意整数 $k$ 的逆元为 $-k$(特别地， $0$ 的逆元是它自己 $0$)。

**例子 2：有限阿贝尔群**
复数集合 $G = \lbrace 1, i, -1, -i \rbrace$ 与常规复数乘法 $\times$ 构成群 $(G, \times)$：

- **说明**：由 $i$ 幂次生成($i^1=i, i^2=-1, i^3=-i, i^4=1$)，满足封闭性。
- **类型**：有限群(阶数为 4)、阿贝尔群。
- **单位元**： $1$ (满足 $z \cdot 1 = 1 \cdot z = z$)。
- **逆元**： $1$ 和 $-1$ 的逆元是它们自己($1^{-1}=1, (-1)^{-1}=-1$)； $i$ 与 $-i$ 互为逆元($i \cdot (-i) = 1$)。

**例子 3：有限非阿贝尔群**
模 2 算术($\mathbb{Z}_2 = \{0, 1\}$)下的 2 阶可逆矩阵集合 $G = \{I, A, B, C, D, E\}$ 与矩阵乘法构成群 $(G, \cdot)$：

- **说明**：元素包含：

$$ I = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix}, \quad A = \begin{pmatrix} 0 & 1 \\\\ 1 & 0 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} $$

$$ C = \begin{pmatrix} 1 & 0 \\\\ 1 & 1 \end{pmatrix}, \quad D = \begin{pmatrix} 0 & 1 \\\\ 1 & 1 \end{pmatrix}, \quad E = \begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} $$

所有运算均在模2下进行（即 $1+1=0$）。

- **类型**：有限群（阶数为 6）、非阿贝尔群。
- **单位元**： $I$（满足对任意 $M \in G, M \cdot I = I \cdot M = M$）。
- **逆元**： $I, A, B, C$ 的逆元是它们自己（如 $A^2 = I$）； $D$ 与 $E$ 互为逆元($D \cdot E = E \cdot D = I$)。
- **非可交换性**：

$$ A \cdot B = \begin{pmatrix} 0 & 1 \\\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 0 & 1 \\\\ 1 & 1 \end{pmatrix} = D $$

$$ B \cdot A = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 0 & 1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} = E $$

即 $A \cdot B \neq B \cdot A$。

## 2. 核心概念与基本定理

### 2.1 循环群 (Cyclic Group)

**定义**：
如果一个群 $G$ 中的每一个元素，都可以表示为某一个固定元素 $g \in G$ 的整数次幂（即 $G = \{g^k \mid k \in \mathbb{Z}\}$），则称 $G$ 为**循环群**，元素 $g$ 称为该群的**生成元 (Generator)**，记作 $G = \langle g \rangle$。

- **阶与生成元**：若 $g$ 的阶为有限数 $n$（即 $g^n = e$ 且 $n$ 为最小正整数），则 $G = \{e, g, g^2, \dots, g^{n-1}\}$，阶数 $|G| = n$。
- **重要性质**：**所有的循环群都是阿贝尔群**（因为 $g^a \cdot g^b = g^{a+b} = g^b \cdot g^a$）。

### 2.2 陪集 (Coset)

**定义**：
设 $H$ 是群 $G$ 的一个子群，对于 $G$ 中的任意固定元素 $a \in G$：

- **左陪集 (Left Coset)**：集合 $`aH = \{a \cdot h \mid h \in H\}`$
- **右陪集 (Right Coset)**：集合 $`Ha = \{h \cdot a \mid h \in H\}`$

> **关键性质**：
>
> 1. **等大小**：每一个陪集的大小都与子群 $H$ 完全相同，即 $|aH| = |H|$。
> 2. **分划性（核心）**： $G$ 的所有左（或右）陪集要么完全相同，要么完全不相交。它们就像“砌砖”一样，把大群 $G$ 均匀地分割成了若干个大小为 $|H|$ 的块。

### 2.3 拉格朗日定理 (Lagrange's Theorem)

**定理内容**：
设 $G$ 为有限群，$H$ 是 $G$ 的子群，则子群的阶必能整除大群的阶，即：

$$ |H| \mid |G| $$

结合陪集的性质，大群 $G$ 可以完美拆分为子群 $H$ 的各个陪集之和，因此有等式：

$$ |G| = [G : H] \cdot |H| $$

其中 $[G : H]$ 称为子群 $H$ 在 $G$ 中的**指数 (Index)**，代表陪集的数量。
