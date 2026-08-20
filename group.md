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

### 1.2 分类

- **按阶数分类**：若群中的元素个数为有限个，称为**有限群 (Finite Group)**；若为无限个，则称为**无限群 (Infinite Group)**。
- **按可交换性分类**：若群满足交换律($\forall a, b \in G \implies a \cdot b = b \cdot a$)，称为**阿贝尔群 (Abelian Group)** / 交换群；否则称为**非阿贝尔群 (Non-Abelian Group)**。

### 1.3 典型例子

**例子 1：无限阿贝尔群**
整数集 $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$ 与常规加法 $+$ 构成群 $(\mathbb{Z}, +)$：

- **类型**：无限群、阿贝尔群。
- **单位元**：$0$(满足 $k + 0 = 0 + k = k$)。
- **逆元**：任意整数 $k$ 的逆元为 $-k$(特别地，$0$ 的逆元是它自己 $0$)。

**例子 2：有限阿贝尔群**
复数集合 $G = \{1, i, -1, -i\}$ 与常规复数乘法 $\times$ 构成群 $(G, \times)$：

- **说明**：由 $i$ 幂次生成($i^1=i, i^2=-1, i^3=-i, i^4=1$)，满足封闭性。
- **类型**：有限群(阶数为 4)、阿贝尔群。
- **单位元**：$1$(满足 $z \cdot 1 = 1 \cdot z = z$)。
- **逆元**：$1$ 和 $-1$ 的逆元是它们自己($1^{-1}=1, (-1)^{-1}=-1$)；$i$ 与 $-i$ 互为逆元($i \cdot (-i) = 1$)。

**例子 3：有限非阿贝尔群**
模 2 算术($\mathbb{Z}_2 = \{0, 1\}$)下的 2 阶可逆矩阵集合 $G = \{I, A, B, C, D, E\}$ 与矩阵乘法构成群 $(G, \cdot)$：

- **说明**：元素包含 $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, B = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, C = \begin{pmatrix} 1 & 0 \\ 1 & 1 \end{pmatrix}, D = \begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix}, E = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$，所有运算均在模 2 下进行(即 $1+1=0$)。
- **类型**：有限群(阶数为 6)、非阿贝尔群。
- **单位元**：$I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$(满足对任意 $M \in G, M \cdot I = I \cdot M = M$)。
- **逆元**：$I, A, B, C$ 的逆元是它们自己(如 $A^2 = I$)；$D$ 与 $E$ 互为逆元($D \cdot E = E \cdot D = I$)。
- **非可交换性**：$A \cdot B = D = \begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix}$，而 $B \cdot A = E = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$，即 $A \cdot B \neq B \cdot A$。
