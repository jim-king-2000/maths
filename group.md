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
- **按元素个数分类**: **平凡群 (Trivial Group)** 是只包含单位元一个元素的群 $G = \lbrace e \rbrace $，阶数为 1，是阶数最小的群。

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
模 2 算术($\mathbb{Z}_2 = \lbrace 0, 1 \rbrace$)下的 2 阶可逆矩阵集合 $G = \lbrace I, A, B, C, D, E \rbrace$ 与矩阵乘法构成群 $(G, \cdot)$：

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

#### 2.1.1 定义：

如果一个群 $G$ 中的每一个元素，都可以表示为某一个固定元素 $g \in G$ 的整数次幂（即 $G = \lbrace g^k \mid k \in \mathbb{Z} \rbrace $），则称 $G$ 为**循环群**，元素 $g$ 称为该群的**生成元 (Generator)**，记作 $G = \langle g \rangle$。

- **阶与生成元**：若 $g$ 的阶为有限数 $n$（即 $g^n = e$ 且 $n$ 为最小正整数），则 $G = \lbrace e, g, g^2, \dots, g^{n-1} \rbrace $，阶数 $|G| = n$。
- **重要性质**：**所有的循环群都是阿贝尔群**（因为 $g^a \cdot g^b = g^{a+b} = g^b \cdot g^a$）。

#### 2.1.2 典型例子

**例子 1：复数乘法群**
复数集合 $G = \lbrace 1, i, -1, -i \rbrace$ 与常规复数乘法 $\times$ 构成群 $(G, \times)$。

- **说明**：由 $i$ 的幂次生成 ($i^0=1, i^1=i, i^2=-1, i^3=-i$)。
- **生成元与阶**：生成元为 $i$（即 $G = \langle i \rangle$），阶为 4（满足 $i^4=1$）。

**例子 2：模 7 乘法群 $(\mathbb{Z}_7^\times, \cdot_7)$**
集合 $G = \lbrace 1, 2, 3, 4, 5, 6 \rbrace $ 与模 7 乘法构成群：

- **说明**：由 3 的幂次模 7 生成：

  $$3^0 \equiv 1 \pmod 7, \quad 3^1 \equiv 3 \pmod 7, \quad 3^2 \equiv 2 \pmod 7$$

  $$3^3 \equiv 6 \pmod 7, \quad 3^4 \equiv 4 \pmod 7, \quad 3^5 \equiv 5 \pmod 7$$

- **生成元与阶**：生成元为 3（即 $G = \langle 3 \rangle$），阶为 6（满足 $3^6 \equiv 1 \pmod 7$）。

### 2.2 陪集 (Coset)

#### 2.2.1 定义：

设 $H$ 是群 $G$ 的一个子群，对于 $G$ 中的任意固定元素 $a \in G$：

- **左陪集 (Left Coset)**：集合 $aH = \lbrace a \cdot h \mid h \in H \rbrace$
- **右陪集 (Right Coset)**：集合 $Ha = \lbrace h \cdot a \mid h \in H \rbrace$

> **关键性质**：
>
> 1. **等大小**：每一个陪集的大小都与子群 $H$ 完全相同，即 $|aH| = |H|$。
> 2. **分划性（核心）**： $G$ 的所有左（或右）陪集要么完全相同，要么完全不相交。它们就像“砌砖”一样，把大群 $G$ 均匀地分割成了若干个大小为 $|H|$ 的块。

#### 2.2.2 陪集的划分性证明

**定理**：设 $H \le G$ 为群 $G$ 的子群。若两个左陪集 $g_1 H$ 与 $g_2 H$ 包含至少一个公共元素 $x$，则两个陪集完全相等（$g_1 H = g_2 H$）。

**证明**：
设两个陪集包含公共元素 $x$，则存在 $h_1, h_2 \in H$，使得：

$$ x = g_1 h_1 = g_2 h_2 $$

两边同时右乘 $h_1^{-1}$，得：

$$ g_1 h_1 h_1^{-1} = g_2 h_2 h_1^{-1} \implies g_1 = g_2 h_2 h_1^{-1} $$

对于 $H$ 中的任意元素 $h_i$，陪集 $g_1 H$ 中的任意元素 $g_1 h_i$ 可表示为：

$$ g_1 h_i = (g_2 h_2 h_1^{-1}) h_i = g_2 (h_2 h_1^{-1} h_i) $$

因为 $H$ 是子群，根据封闭性与逆元存在性，必有 $h_2 h_1^{-1} h_i \in H$。令 $h_j = h_2 h_1^{-1} h_i \in H$，则有：

$$ g_1 h_i = g_2 h_j \in g_2 H $$

这说明陪集 $g_1 H$ 中的任意元素都属于 $g_2 H$，即 **$g_1 H \subseteq g_2 H$**。

同理，将 $g_2$ 用 $g_1$ 表示，可证 **$g_2 H \subseteq g_1 H$**。

综上所述，**$g_1 H = g_2 H$**。

#### 2.2.3 典型例子

**例子 1：复数乘法群**
复数集合 $G = \lbrace 1, i, -1, -i \rbrace$ 与常规复数乘法 $\times$ 构成群 $(G, \times)$，其子群为 $H = \lbrace 1, -1 \rbrace$。

对 $G$ 中不同的元素 $a$ 计算陪集：

- 当 $a = 1$ 时， $1H = \lbrace 1 \cdot 1, 1 \cdot (-1) \rbrace = \lbrace 1, -1 \rbrace$
- 当 $a = -1$ 时， $-1H = \lbrace (-1) \cdot 1, (-1) \cdot (-1) \rbrace  = \lbrace -1, 1 \rbrace  = 1H$
- 当 $a = i$ 时， $iH = \lbrace i \cdot 1, i \cdot (-1) \rbrace = \lbrace i, -i \rbrace$
- 当 $a = -i$ 时， $-iH = \lbrace (-i) \cdot 1, (-i) \cdot (-1) \rbrace  = \lbrace -i, i \rbrace  = iH$

**现象观察**：
$G$ 中虽然有 4 个元素，但最终只生成了 **2 个互不相交的本质陪集**：

1. $H = \lbrace 1, -1 \rbrace $
2. $iH = \lbrace i, -i \rbrace $

它们正好把 4 个元素的群 $G$ 完美拆成了两块（每块 2 个元素），验证了指数 $[G : H] = 4 / 2 = 2$。

**例子 2：由 3 生成的模 7 乘法群 $(\mathbb{Z}_7^\times, \cdot_7)$**
集合 $G = \lbrace 1, 2, 3, 4, 5, 6 \rbrace$ 与模 7 乘法构成阶数为 6 的群，且 $G$ 由 3 的幂模 7 生成($G = \langle 3 \rangle$)。

- **情况 A：选择 2 阶子群 $H_1 = \lbrace 1, 6 \rbrace$**
  - $1H_1 = 6H_1 = \lbrace 1, 6 \rbrace$
  - $2H_1 = 5H_1 = \lbrace 2, 5 \rbrace$
  - $3H_1 = 4H_1 = \lbrace 3, 4 \rbrace$

  **现象**：生成了 **3 个本质陪集**，将群 $G$ 均匀切分为 3 块，指数 $[G : H_1] = 6 / 2 = 3$。

- **情况 B：选择 3 阶子群 $H_2 = \lbrace 1, 2, 4 \rbrace$**
  - $1H_2 = 2H_2 = 4H_2 = \lbrace 1, 2, 4 \rbrace$
  - $3H_2 = 5H_2 = 6H_2 = \lbrace 3, 5, 6 \rbrace$

  **现象**：生成了 **2 个本质陪集**，将群 $G$ 均匀切分为 2 块，指数 $[G : H_2] = 6 / 3 = 2$。

### 2.3 拉格朗日定理 (Lagrange's Theorem)

#### 2.3.1 定理内容

设 $G$ 为有限群，$H$ 是 $G$ 的子群，则子群的阶必能整除大群的阶，即：

$$ |H| \mid |G| $$

结合陪集的性质，大群 $G$ 可以完美拆分为子群 $H$ 的各个陪集之和，因此有等式：

$$ |G| = [G : H] \cdot |H| $$

其中 $[G : H]$ 称为子群 $H$ 在 $G$ 中的**指数 (Index)**，代表陪集的数量。

#### 2.3.2 定理证明

#### 2.3.3 定理应用

拉格朗日定理可以用来证明数论中的费马小定理和欧拉定理。

#### 2.3.4 总结

⚠️ 注意（拉格朗日逆定理不成立）：如果 $d \mid \vert{}G\vert{}$，$G$ 中不一定存在 $d$ 阶子群。
最经典的反例：交错群 $A_4$ 的阶是 12，虽然 $6 \mid 12$，但 $A_4$ 没有任何 6 阶子群。

### 2.4 有限循环群的子群基本定理

拉格朗日定理说子群阶数必整除大群，但反过来不一定成立。我们先看在最简单的循环群里，逆定理是如何完美成立的。

### 2.5 轨道-稳定子(Orbit-Stabilizer Theorem)定理

前面我们是通过‘静态的子群’来切分大群；现在我们将引入群作用（Group Action），通过‘动态的旋转与变换’来切分大群。这是证明后续柯西定理与西洛定理的核心钥匙。

### 2.6 柯西定理

对于一般的非循环群，拉格朗日定理的逆定理失效了。但如果这个因子是质数 $p$，逆定理是否成立？柯西定理给出了肯定的回答。

### 2.7 西洛定理

从质数 $p$ 推广到质数的最高次幂 $p^k$，我们迎来了有限群结构的终极定理——西洛定理。
