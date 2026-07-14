---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
第七章“线性变换”主要讨论了线性空间中最重要的映射类型。以下是根据提供的来源对主要内容、公式及定义的整理。

### 一、 主要内容概括
本章首先定义了**线性变换**及其基本性质（第一节），随后介绍了线性变换的**运算**（加法、乘法、数量乘法及多项式）。第三节建立了**线性变换与矩阵**的一一对应关系，并探讨了不同基下变换矩阵的**相似性**。第四节至第九节深入研究了线性变换的内部结构，包括**特征值与特征向量**、**矩阵对角化**的条件、**不变子空间**、**若尔当（Jordan）标准形** 以及**最小多项式**。

---

### 二、 公式整理（按原文序号）

**§1 线性变换的定义**
*   **(1)** \\( \mathscr{A}(\alpha+\beta)=\mathscr{A}(\alpha)+\mathscr{A}(\beta), \quad \mathscr{A}(k\alpha)=k\mathscr{A}(\alpha) \\)

**§3 线性变换的矩阵**
*   **(1)** \\( \xi = x_1\varepsilon_1 + x_2\varepsilon_2 + \dots + x_n\varepsilon_n \\) （向量在基下的表示）
*   **(2)** \\( \mathscr{A}\xi = \mathscr{A}(x_1\varepsilon_1 + \dots + x_n\varepsilon_n) = x_1\mathscr{A}\varepsilon_1 + \dots + x_n\mathscr{A}\varepsilon_n \\)
*   **(3)** \\( \mathscr{A}\varepsilon_i = \alpha_i, \quad i=1, 2, \dots, n \\)
*   **(4)** \\( \mathscr{A}\xi = \sum_{i=1}^n x_i\alpha_i \\)
*   **(5)** \\( (\mathscr{A}\varepsilon_1, \mathscr{A}\varepsilon_2, \dots, \mathscr{A}\varepsilon_n) = (\varepsilon_1, \varepsilon_2, \dots, \varepsilon_n)A \\) （变换矩阵的定义式）
*   **(6)** \\( (\mathscr{A}\varepsilon_1, \dots, \mathscr{A}\varepsilon_n) = (\varepsilon_1, \dots, \varepsilon_n)A \\)
*   **(7)** \\( (\mathscr{A}\eta_1, \dots, \mathscr{A}\eta_n) = (\eta_1, \dots, \eta_n)B \\)

**§4 特征值与特征向量**
*   **(1)** \\( \mathscr{A}\xi = \lambda_0\xi \\) （特征值定义方程）
*   **(2)** \\( A \begin{pmatrix} x_{01} \\ \vdots \\ x_{0n} \end{pmatrix} = \lambda_0 \begin{pmatrix} x_{01} \\ \vdots \\ x_{0n} \end{pmatrix} \\)
*   **(3)** \\( (\lambda_0 E - A) \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} = \mathbf{0} \\) （特征向量的齐次方程组形式）
*   **(4)** \\( |\lambda E - A| = \begin{vmatrix} \lambda - a_{11} & \dots & -a_{1n} \\ \vdots & & \vdots \\ -a_{n1} & \dots & \lambda - a_{nn} \end{vmatrix} \\) （特征多项式）
*   **(5)** \\( |\lambda E - A| = \lambda^n - (a_{11} + \dots + a_{nn})\lambda^{n-1} + \dots + (-1)^n |A| \\)

**§5 对角矩阵**
*   **(1)-(3)** 证明不同特征值的特征向量线性无关时的中间过程等式
*   **(4)** \\( h_n = h_{n-1} + h_{n-2}, \quad n \ge 2 \\) （斐波那契数列关系）
*   **(6)-(9)** 证明哈密顿-凯莱定理时的矩阵多项式推导过程

**§7 不变子空间（及定理11）**
*   **(1)** （在定理11证明中）\\( l_1\varepsilon_1 + \dots + l_r\varepsilon_r + l_{r+1}\varepsilon_{r+1} + \dots + l_n\varepsilon_n = \mathbf{0} \\)
*   **(2)** （在定理11证明中）\\( l_1\mathscr{A}\varepsilon_1 + \dots + l_r\mathscr{A}\varepsilon_r + l_{r+1}\mathscr{A}\varepsilon_{r+1} + \dots + l_n\mathscr{A}\varepsilon_n = \mathscr{A}\mathbf{0} = \mathbf{0} \\)
*   **(3)** （在例2中）\\( A^2 = A \\) 的矩阵形式
*   **(1)** （在§7正文中）不变子空间基的扩充形式 \\( \varepsilon_1, \dots, \varepsilon_k, \varepsilon_{k+1}, \dots, \varepsilon_n \\)
*   **(2)** \\( \begin{pmatrix} A_1 & A_3 \\ 0 & A_2 \end{pmatrix} \\) （不变子空间对应的分块矩阵）
*   **(3)** 各个不变子空间的基合并
*   **(4)** \\( \text{diag}(A_1, A_2, \dots, A_s) \\) （空间分解为直和后的准对角矩阵）
*   **(5)** \\( \beta_1 + \beta_2 + \dots + \beta_s = \mathbf{0} \\)
*   **(6)** \\( (\mathscr{A} - \lambda_i \mathscr{E})^{r_i} \beta_i = \mathbf{0} \\)

**§8 若尔当（Jordan）标准形介绍**
*   **(1)** 若尔当块 \\( J(\lambda_0, k) \\) 的矩阵形式
*   **(2)** 幂零变换的链式基向量组
*   **(3)** 幂零变换在链式基下的矩阵形式
*   **(4)-(5)** 证明 Jordan 标准形存在性时的归纳法基向量组

---

### 三、 定义整理

*   **定义 1**：线性空间 \\( V \\) 的一个变换 \\( \mathscr{A} \\) 称为**线性变换**，如果对于 \\( V \\) 中任意元素 \\( \alpha, \beta \\) 和数域 \\( P \\) 中任意数 \\( k \\)，都有 \\( \mathscr{A}(\alpha+\beta) = \mathscr{A}(\alpha)+\mathscr{A}(\beta) \\) 和 \\( \mathscr{A}(k\alpha) = k\mathscr{A}(\alpha) \\)。
*   **定义 2**：设 \\( \varepsilon_1, \varepsilon_2, \dots, \varepsilon_n \\) 是数域 \\( P \\) 上 \\( n \\) 维线性空间 \\( V \\) 的一组基，\\( \mathscr{A} \\) 是 \\( V \\) 中的一个线性变换，基向量的像可以经基线性表示。由表示系数构成的矩阵 \\( A \\) 称为 \\( \mathscr{A} \\) **在基 \\( \varepsilon_1, \varepsilon_2, \dots, \varepsilon_n \\) 下的矩阵**。
*   **定义 3**：设 \\( A, B \\) 为数域 \\( P \\) 上两个 \\( n \\) 阶矩阵，如果可以找到数域 \\( P \\) 上的 \\( n \\) 阶可逆矩阵 \\( X \\)，使得 \\( B = X^{-1}AX \\)，就说 **\\( A \\) 相似于 \\( B \\)**，记作 \\( A \sim B \\)。
*   **定义 4**：设 \\( \mathscr{A} \\) 是数域 \\( P \\) 上线性空间 \\( V \\) 的一个线性变换，如果对于数域 \\( P \\) 中一数 \\( \lambda_0 \\)，存在一个非零向量 \\( \xi \\)，使得 \\( \mathscr{A}\xi = \lambda_0\xi \\)，那么 \\( \lambda_0 \\) 称为 \\( \mathscr{A} \\) 的一个**特征值**，而 \\( \xi \\) 称为 \\( \mathscr{A} \\) 的属于特征值 \\( \lambda_0 \\) 的一个**特征向量**。
*   **定义 5**：设 \\( A \\) 是数域 \\( P \\) 上一个 \\( n \\) 阶矩阵，\\( \lambda \\) 是一个文字，矩阵 \\( \lambda E - A \\) 的行列式 \\( |\lambda E - A| \\) 称为 \\( A \\) 的**特征多项式**。
*   **定义 7**：设 \\( \mathscr{A} \\) 是数域 \\( P \\) 上线性空间 \\( V \\) 的线性变换，\\( W \\) 是 \\( V \\) 的子空间。如果 \\( W \\) 中的向量在 \\( \mathscr{A} \\) 下的像仍在 \\( W \\) 中，就称 \\( W \\) 是 \\( \mathscr{A} \\) 的**不变子空间**，简称 \\( \mathscr{A} \\)-子空间。
*   **定义 8**：设 \\( V \\)、\\( \mathscr{A} \\)、\\( f(\lambda) \\) 如定理12所述，称 \\( V_i = \{ \xi \in V \mid (\mathscr{A} - \lambda_i \mathscr{E})^{r_i} \xi = \mathbf{0} \} \\) 为 \\( \mathscr{A} \\) 的属于特征值 \\( \lambda_i \\) 的**根子空间**，常记为 \\( V^{\lambda_i} \\)。
*   **定义 9**：形如原文 (1) 式的矩阵称为**若尔当块**；由若干个若尔当块组成的准对角矩阵称为**若尔当形矩阵**。