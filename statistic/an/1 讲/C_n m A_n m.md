排列组合中的组合数 $ C_n^m $ 和排列数 $ A_n^m $ 的完整展开公式如下：

### 1. 组合数（Combination）$ C_n^m $
表示从 $n$ 个不同元素中取出 $m$ 个元素的<span style="border: 1px solid black; padding: 5px; display: inline-block;">组合数</span>，不考虑顺序

公式：<span style="border: 1px solid black; padding: 5px; display: inline-block;">
$$C_n^m = \binom{n}{m} = \frac{n!}{m!(n - m)!}$$
</span>

- $ n! $ 表示 $ n $ 的阶乘，即 $ n! = n \times (n-1) \times \cdots \times 1 $

**例子**：
计算 $ C_5^2 $：
$$
C_5^2 = \frac{5!}{2! \times 3!} = \frac{120}{2 \times 6} = 10
$$

### 2. 排列数（Arrangement）$ A_n^m $
表示从 $ n $ 个不同元素中取出 $ m $ 个元素的<span style="border-bottom: 3px dotted black;">排列数</span>，考虑顺序。

公式：<span style="border: 1px solid black; padding: 5px; display: inline-block;">
$$
A_n^m = P(n, m) = \frac{n!}{(n - m)!}
$$
</span>

**例子**：
计算 $ A_5^2 $：
$$
A_5^2 = \frac{5!}{3!} = \frac{120}{6} = 20
$$

### 总结：
- **组合数 $ C_n^m $**：用于不考虑顺序的选择。
- **排列数 $ A_n^m $**：用于考虑顺序的排列。

两者的关系为：
$$
A_n^m = C_n^m \times m!
$$
即排列数等于组合数乘以 $ m $ 的阶乘。

**最终答案**：
$$
C_n^m = \boxed{\frac{n!}{m!(n - m)!}}
$$
$$
A_n^m = \boxed{\frac{n!}{(n - m)!}}
$$