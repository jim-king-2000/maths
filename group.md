# 群论 (Group Theory)

## 1. 群的定义

群（Group）是一个集合 $G$ 与其上的二元运算符 $\cdot$ 组成的二元组 $(G, \cdot)$，且必须满足以下四条公理：

1. **封闭性 (Closure)**
   $\forall a, b \in G \implies a \cdot b \in G$

2. **结合律 (Associativity)**
   $\forall a, b, c \in G \implies (a \cdot b) \cdot c = a \cdot (b \cdot c)$

3. **单位元 (Identity)**
   $\exists e \in G: \forall a \in G \implies e \cdot a = a \cdot e = a$

4. **逆元 (Inverse)**
   $\forall a \in G, \exists a^{-1} \in G: a \cdot a^{-1} = a^{-1} \cdot a = e$
