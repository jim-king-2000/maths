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

在前面做加法的过程中，我们会观察到：

$$2+3+1=2+(3+1)$$

大一点的数也成立：

$$264872+38101+1542=264872+(38101+1542)$$

我们刚才只是验证了一些具体的例子。**即使很多例子都成立，也不能说明所有情况都成立。**

我们必须提供证明。

我们先来看看 $2+3+1$ ，它可以代表2个红色小球、3个蓝色小球和1个绿色小球。

$$\huge \overset{\color{red}{\bullet}}{\fbox{1}}\overset{\color{red}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{1}}\overset{\color{blue}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{3}}\overset{\color{green}{\bullet}}{\fbox{1}}$$

然后我们从左向右数，我们得到： $1 + 3 + 2$

我们把蓝色小球与绿色小球打包装进一个集装箱里，打包只是把一些小球看成一个整体，并没有增加或减少任何小球。

$$\huge \overset{\color{red}{\bullet}}{\fbox{1}}\overset{\color{red}{\bullet}}{\fbox{2}} \quad \boxed{\overset{\color{blue}{\bullet}}{\fbox{1}}\overset{\color{blue}{\bullet}}{\fbox{2}}\overset{\color{blue}{\bullet}}{\fbox{3}}\overset{\color{green}{\bullet}}{\fbox{1}}}$$

我们单独数这个集装箱，里面正好是： $3+1$

而所有小球就是2个红色小球加上集装箱, 集装箱里有 $3+1$ 个小球： $2+(3+1)$

因为小球的总数没有变化，所以： $2+3+1=2+(3+1)$

现在我们把上面的过程泛化，推广到所有情况。

我们假设有 𝑎 个红色的小球、 𝑏 个蓝色的小球和 c 个绿色小球，其中 𝑎,𝑏,c 可以是任意数。也就是说，无论 𝑎 、 𝑏 和 c 是多少，下面的推理都成立。

$$\huge \overbrace{\color{red}{\bullet}\color{red}{\bullet}\dots\color{red}{\bullet}}^{a个红色小球} \quad \overbrace{\color{blue}{\bullet}\color{blue}{\bullet}\dots\color{blue}{\bullet}}^{b个蓝色小球} \quad \overbrace{\color{green}{\bullet}\color{green}{\bullet}\dots\color{green}{\bullet}}^{c个绿色小球}$$

从左向右数，我们得到： $a+b+c$

我们把蓝色小球和绿色小球打包到一个集装箱里：

$$\huge \overbrace{\color{red}{\bullet}\color{red}{\bullet}\dots\color{red}{\bullet}}^{a个红色小球} \quad \boxed{\overbrace{\color{blue}{\bullet}\color{blue}{\bullet}\dots\color{blue}{\bullet}}^{b个蓝色小球} \quad \overbrace{\color{green}{\bullet}\color{green}{\bullet}\dots\color{green}{\bullet}}^{c个绿色小球}}$$

我们单独数这个集装箱，里面正好是： $b+c$

而所有小球的个数就是a个红色小球加上集装箱： $a+(b+c)$

而所有小球的个数不变，所以： $a+b+c=a+(b+c)$

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

我们把 $2\times3$ 表示成3行、每行2个小球：

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

我们发现，虽然排列的方向变了，但是小球的总数没有变。现在它表示 $3\times2$ 。

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

## 3.给勇敢探索者的“数学彩蛋”

> 在这一章里，我们用装箱“打包”和“换个方向数”，从最简单的小球出发，真正理解了加法的结合律与交换律。你在现实中遇到的所有数学问题，用这些方法就足够解决啦！但作者想偷偷告诉你一个数学家们的终极秘密：其实在严格的数学底层，根本没有“打包”，甚至连“加法”这个词都不存在！在100多年前，数学家皮亚诺把自然数的基础用非常简单的公理系统刻画了出来。我们可以把它想象成两个最基本的“代码指令”：
>
> 1. 一个起点：$0$
> 2. 一个动作：找下一个数，也就是“后继”
>
> 在这样的基础上，数学家可以用严密的逻辑一步一步定义加法、乘法，并证明我们今天熟悉的结合律、交换律等性质。现实中的“打包”和“数小球”，是自然界送给我们最棒的视觉礼物；而数学家在符号世界里的纯粹逻辑推导，则是人类智慧最极致的奇迹。等你长大后，随时可以去底层看看那座完全由逻辑搭建起来的宏伟大厦！

## 4. 运算律的应用
