# 运算律

## 1. 加法运算律

### 1.1 加法交换律

在前面做加法的时候，我们会观察到：

$$4+2=2+4$$

也就是说，两个数相加，交换顺序，和不变。

这就是为什么，加法表会沿着主对角线（从左上到右下的斜线）对称。

如果你愿意，你可以验证 $38572653 + 9267351 = 9267351 + 38572653$ 。

我们刚才只是验证了一些具体的例子。**即使很多例子都成立，也不能说明所有情况都成立。**

数学和普通的猜测不一样。数学家不仅要发现规律，还要说明为什么这个规律对所有情况都成立。这个过程叫做“证明”。

我们先用 $2 + 3$ 来看看，为什么加法交换律成立。

我们先放2个红色的小球，再放3个蓝色的小球，然后从左到右数一遍，这就是 $2+3$ 。

$$\huge \overset{\color{red}{\bullet}}{\fbox{1}}\overset{\color{red}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{1}}\overset{\color{blue}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{3}}$$

同样个数的小球，这次我们从右到左数，我们数到3个蓝色小球和2个红色小球，这就是 $3 + 2$ 。

$$\huge \overset{\color{red}{\bullet}}{\fbox{2}}\overset{\color{red}{\bullet}}{\fbox{1}}\overset{\color{blue}{\bullet}}{\fbox{3}}\overset{\color{blue}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{1}}$$

所以我们得到： $2 + 3 = 3 + 2$ 。

这次，让我们把上面的方法泛化，推广到任意个数的小球上。

我们假设有 \(a\) 个红色的小球和 \(b\) 个蓝色的小球，其中 \(a,b\) 可以是任意数。也就是说，无论 \(a\) 和 \(b\) 是多少，下面的推理都成立。

$$\huge \overbrace{\color{red}{\bullet}\color{red}{\bullet}\dots\color{red}{\bullet}}^{a个红色小球} \quad \overbrace{\color{blue}{\bullet}\color{blue}{\bullet}\dots\color{blue}{\bullet}}^{b个蓝色小球}$$

我们从左往右数，数到a个红色小球和b个蓝色小球，得到： $a+b$ 。

我们从右往左数，数到b个蓝色小球和a个红色小球，得到： $b+a$ 。

但小球的总个数是不变的。所以：$a+b=b+a$ 。

**练习:**

1. 请在下面的空白处填入合适的数字，使得等式成立。

$$
\begin{array}{rrr}
16 + 5 = 5+\underline{\qquad} & \qquad 24 + 8 = 8+\underline{\qquad} & \qquad 37 + 3 = 3+\underline{\qquad} \\\\
2 + 19 = 19+\underline{\qquad} & \qquad 5 + 57 = 57+\underline{\qquad} & \qquad 8 + 88 = 88+\underline{\qquad} \\\\
13 + 12 = 12+\underline{\qquad} & \qquad 26 + 58 = 58+\underline{\qquad} & \qquad 99 + 94 = 94+\underline{\qquad}
\end{array}
$$

2. 不用计算，请说出下面两个和是否相等。

$$1938476187265+746251192 \qquad 746251192+1938476187265$$

### 1.2 加法结合律

### 1.3 加法运算律推论

## 2. 乘法运算律

### 2.1 乘法交换律

在前面做乘法的时候，我们会观察到：

$$4\times2=2\times4$$

也就是说，两个数相乘，交换顺序，积不变。

这就是为什么，乘法表会沿着主对角线（从左上到右下的斜线）对称。

如果你愿意，你可以验证 $38572653 \times 9267351 = 9267351 \times 38572653$ 。

我们刚才只是验证了一些具体的例子。**即使很多例子都成立，也不能说明所有情况都成立。**

我们必须证明它。

我们先用 $2 \times 3$ 来看看，为什么乘法交换律成立。

我们把 \(2\times3\) 表示成3行、每行2个小球：

$$
\huge
\begin{array}{cc}
\bullet & \bullet \\
\bullet & \bullet \\
\bullet & \bullet \\
\end{array}
$$

我们把这个小球的排列转一个方向，让原来的行变成列，原来的列变成行。

$$
\huge
\begin{array}{ccc}
\bullet & \bullet & \bullet \\
\bullet & \bullet & \bullet \\
\end{array}
$$

我们发现，虽然排列的方向变了，但是小球的总数没有变。现在它表示 \(3\times2\)。

所以： $2 \times 3 = 3 \times 2$ 。

这次，让我们把上面的方法泛化，推广到任意个数的小球上。

我们假设有 \(b\) 行、每行 \(a\) 个小球，其中 \(a,b\) 可以是任意数。也就是说，无论 \(a\) 和 \(b\) 是多少，下面的推理都成立。

我们把小球排列成b行、每行a个的长方形阵列，得到 $a\times b$ ：

$$
\huge
\text{b行}
\begin{cases}
\overbrace{\bullet\bullet\dots\bullet}^{a个小球} \\
\bullet\bullet\dots\bullet \\
\dots \\
\bullet\bullet\dots\bullet
\end{cases}
$$

我们把它转一个方向，让原来的行变成列，原来的列变成行，得到： $b\times a$ ：

$$
\huge
\text{a行}
\begin{cases}
\overbrace{\bullet\bullet\dots\bullet}^{b个小球} \\
\bullet\bullet\dots\bullet \\
\dots \\
\bullet\bullet\dots\bullet
\end{cases}
$$

因为转动前后，小球的总数没有改变，所以： $a\times b=b\times a$ 。

**练习:**

1. 请在下面的空白处填入合适的数字，使得等式成立。

$$
\begin{array}{rrr}
16 \times 5 = 5\times\underline{\qquad} & \qquad 24 \times 8 = 8\times\underline{\qquad} & \qquad 37 \times 3 = 3\times\underline{\qquad} \\\\
2 \times 19 = 19\times\underline{\qquad} & \qquad 5 \times 57 = 57\times\underline{\qquad} & \qquad 8 \times 88 = 88\times\underline{\qquad} \\\\
13 \times 12 = 12\times\underline{\qquad} & \qquad 26 \times 58 = 58\times\underline{\qquad} & \qquad 99 \times 94 = 94\times\underline{\qquad}
\end{array}
$$

2. 不用计算，请说出下面两个积是否相等。

$$1938476187265\times746251192 \qquad 746251192\times1938476187265$$

### 2.2 乘法结合律

### 2.3 乘法分配律

## 3. 运算律的应用
