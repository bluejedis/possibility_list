### **1. 全概率公式（Law of Total Probability）**
**公式：**

<span style="border: 1px solid black; padding: 5px; display: inline-block;">

\[
P(A) = \sum_{i=1}^{n} P(B_i) P(A|B_i)
\]

</span>

**含义：**  
全概率公式用于计算一个<span style="border-bottom: 3px dotted black;">复杂事件</span> \( A \) 的概率，方法是将其分解为<u>若干个</u> 互斥（互不相容）且完备（覆盖所有可能）的事件 \( B_1, B_2, \dots, B_n \) 的<span style="border-bottom: 3px dotted black;">加权和</span>。

**关键点：**
1. **\( \{B_i\} \) 构成一个完备事件组**：
   - 互斥性：\( B_i \cap B_j = \varnothing \)（\( i \neq j \)），即不同 \( B_i \) 不会同时发生。
   - 完备性：\( \bigcup_{i=1}^n B_i = \Omega \)（所有 \( B_i \) 覆盖整个样本空间）。
2. **\( P(A|B_i) \) 是条件概率**：
   - 表示在 \( B_i \) 发生的条件下，\( A \) 发生的概率。
3. **应用场景**：
   - 当直接计算 \( P(A) \) 比较困难，但 <span style="border-bottom: 2px solid black;">\( A \) 在不同 \( B_i \) 下的条件概率 \( P(A|B_i) \)</span> 已知时，可以使用全概率公式。

**例子：** 

假设某工厂有 3 条生产线 \( B_1, B_2, B_3 \)，分别占总产量的 50%、30%、20%。已知各生产线的次品率分别为 1%、2%、3%。求随机抽一个产品是次品（事件 \( A \)）的概率。  
解：

<span style="border: 1px solid black; padding: 5px; display: inline-block;">

\(P(A) = P(B_1)P(A|B_1) + P(B_2)P(A|B_2) + P(B_3)P(A|B_3) = 0.5 \times 0.01 + 0.3 \times 0.02 + 0.2 \times 0.03 = 0.017
\)

</span>

---

### **2. 贝叶斯公式（Bayes' Theorem）**
**公式：**
\[
P(B_i|A) = \frac{P(B_i)P(A|B_i)}{\boxed{\sum_{j=1}^n P(B_j)P(A|B_j)}}
\]
**含义：**  
贝叶斯公式用于“执果索因”，即在观察到事件 \( A \) 发生后，反推某个原因 \( B_i \) 发生的概率。

**关键点：**
1. **先验概率 \( P(B_i) \)**：
   - 表示在不知道 \( A \) 是否发生时，\( B_i \) 本身的概率。
2. **似然概率 \( P(A|B_i) \)**：
   - 表示在 \( B_i \) 发生的条件下，\( A \) 发生的概率。
   - ---
3. **后验概率 \( P(B_i|A) \)**：
   - 表示在观察到 \( A \) 发生后，\( B_i \) 发生的概率。
4. **分母是全概率公式**：
   - \( \sum_{j=1}^n P(B_j)P(A|B_j) = P(A) \)，即 \( A \) 的总概率。

**应用场景：**
- 医学诊断（已知检测结果，反推患病概率）。
- 垃圾邮件过滤（已知邮件内容，判断是否为垃圾邮件）。
- 机器学习中的<span style="border-bottom: 3px dotted black;">贝叶斯分类器</span>。

**例子（接上例）：**  
假设抽到一个次品（\( A \) 发生），求它来自第 2 条生产线 \( B_2 \) 的概率。  
解：
\[
\boxed{P(B_2|A) = \frac{P(B_2)P(A|B_2)}{P(A)} }= \frac{0.3 \times 0.02}{0.017} \approx 0.3529
\]

---


**关系：**  
贝叶斯公式的**分母就是全概率公式**，两者通常结合使用：
- 先用全概率公式计算 \( P(A) \)；
- 再用贝叶斯公式计算 \( P(B_i|A) \)。

