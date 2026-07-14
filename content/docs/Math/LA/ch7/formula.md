---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
第七章“线性变换”系统地研究了线性空间到其自身的保持加法和数量乘法运算的映射。以下是根据来源内容整理的主要内容、公式及定义：

### 一、 主要内容概括

本章主要探讨了线性变换的性质、运算及其在矩阵理论中的表现。核心内容包括：
1.  **基本理论**：线性变换的定义、性质及其四则运算（加、乘、数乘）与多项式理论。
2.  **矩阵表示**：建立线性变换与矩阵的一一对应，研究不同基下变换矩阵的相似性。
3.  **特征理论**：特征值与特征向量的定义、计算，特征多项式及其性质，以及哈密顿-凯莱定理。
4.  **结构分析**：研究变换矩阵的对角化条件，引入不变子空间、值域与核的概念，并深入探讨复数域下的若尔当（Jordan）标准形。
5.  **化简工具**：利用最小多项式来判断矩阵是否可对角化。

---

### 二、 公式整理（按原文各小节序号）

**§1 线性变换的定义**
*   **(1)** \\( \mathscr{A}(\alpha+\beta)=\mathscr{A}(\alpha)+\mathscr{A}(\beta), \quad \mathscr{A}(k\alpha)=k\mathscr{A}(\alpha) \\)

**§3 线性变换的矩阵**
*   **(1)** \\( \xi = x_1\varepsilon_1 + x_2\varepsilon_2 + \dots + x_n\varepsilon_n \\)
*   **(2)** \\( \mathscr{A}\xi = \mathscr{A}(x_1\varepsilon_1 + \dots + x_n\varepsilon_n) = x_1\mathscr{A}\varepsilon_1 + \dots + x_n\mathscr{A}\varepsilon_n \\)
*   **(3)** \\( \mathscr{A}\varepsilon_i = \alpha_i, \quad i=1, 2, \dots, n \\)
*   **(4)** \\( \mathscr{A}\xi = \sum_{i=1}^n x_i\alpha_i \\)
*   **(5)** \\( (\mathscr{A}\varepsilon_1, \mathscr{A}\varepsilon_2, \dots, \mathscr{A}\varepsilon_n) = (\varepsilon_1, \varepsilon_2, \dots, \varepsilon_n)A \\)
*   **(6)** 选定基 \\( \varepsilon_1, \varepsilon_2, \dots, \varepsilon_n \\)
*   **(7)** 选定基 \\( \eta_1, \eta_2, \dots, \eta_n \\)
*   *(注：其后导出了 \\( B = X^{-1}AX \\) 的基变换公式)*

**§4 特征值与特征向量**
*   **(1)** \\( \mathscr{A}\xi = \lambda_0\xi \\)
*   **(2)** \\( A \begin{pmatrix} x_{01} \\ \vdots \\ x_{0n} \end{pmatrix} = \lambda_0 \begin{pmatrix} x_{01} \\ \vdots \\ x_{0n} \end{pmatrix} \\)
*   **(3)** \\( (\lambda_0 E - A) \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} = \mathbf{0} \\)
*   **(4)** \\( |\lambda E - A| = 0 \\)（特征方程行列式形式）
*   **(5)** \\( |\lambda E - A| = \lambda^n - (a_{11} + \dots + a_{nn})\lambda^{n-1} + \dots + (-1)^n |A| \\)

**§5 对角矩阵**
*   **(1)-(3)** 证明特征向量线性无关时的递推等式
*   **(4)** \\( h_n = h_{n-1} + h_{n-2}, \quad n \ge 2 \\)
*   **(6)-(9)** 证明哈密顿-凯莱定理时涉及的矩阵多项式展开与系数比较式

**§6 线性变换的值域与核**
*   **(1)** \\( l_1\varepsilon_1 + \dots + l_r\varepsilon_r + l_{r+1}\varepsilon_{r+1} + \dots + l_n\varepsilon_n = \mathbf{0} \\)
*   **(2)** 对上式进行线性变换：\\( l_1\eta_1 + \dots + l_r\eta_r = \mathbf{0} \\)

**§7 不变子空间**
*   **(1)** 基扩充：\\( \varepsilon_1, \dots, \varepsilon_k, \varepsilon_{k+1}, \dots, \varepsilon_n \\)
*   **(2)** 对应不变子空间的分块矩阵形式 \\( \begin{pmatrix} A_1 & A_3 \\ 0 & A_2 \end{pmatrix} \\)
*   **(3)** 直和分解后的总基底组合
*   **(4)** 准对角矩阵 \\( \text{diag}(A_1, A_2, \dots, A_s) \\)
*   **(5)** \\( \beta_1 + \beta_2 + \dots + \beta_s = \mathbf{0} \\)
*   **(6)** \\( (\mathscr{A} - \lambda_i \mathscr{E})^{r_i} \beta_i = \mathbf{0} \\)

**§8 若尔当（Jordan）标准形介绍**
*   **(1)** 若尔当块 \\( J(\lambda_0, k) \\) 的定义矩阵
*   **(2)** 幂零变换的链式向量组表示
*   **(3)** 幂零变换的特定准对角阵形式
*   **(4)-(5)** 证明 Jordan 标准形存在性时的归纳法基底排列

---

### 三、 定义整理（采用 7.x.x 形式）

*   **定义 7.1.1**：线性空间 \\( V \\) 的一个变换 \\( \mathscr{A} \\) 称为**线性变换**，如果对于 \\( V \\) 中任意元素 \\( \alpha, \beta \\) 和数域 \\( P \\) 中任意数 \\( k \\)，都有 \\( \mathscr{A}(\alpha+\beta) = \mathscr{A}(\alpha)+\mathscr{A}(\beta) \\) 且 \\( \mathscr{A}(k\alpha) = k\mathscr{A}(\alpha) \\)。
*   **定义 7.3.2**：设 \\( \varepsilon_1, \dots, \varepsilon_n \\) 是 \\( V \\) 的一组基，\\( \mathscr{A} \\) 是线性变换，由基向量的像的坐标构成的矩阵 \\( A \\) 称为 **\\( \mathscr{A} \\) 在该基下的矩阵**。
*   **定义 7.3.3**：设 \\( A, B \\) 是 \\( n \\) 阶矩阵，若存在可逆阵 \\( X \\) 使得 \\( B = X^{-1}AX \\)，则称 **\\( A \\) 相似于 \\( B \\)**，记作 \\( A \sim B \\)。
*   **定义 7.4.4**：若存在 \\( \lambda_0 \\) 和非零向量 \\( \xi \\) 使得 \\( \mathscr{A}\xi = \lambda_0\xi \\)，则 \\( \lambda_0 \\) 为 **特征值**，\\( \xi \\) 为其 **特征向量**。
*   **定义 7.4.5**：矩阵 \\( \lambda E - A \\) 的行列式 \\( |\lambda E - A| \\) 称为 \\( A \\) 的 **特征多项式**。
*   **定义 7.7.7**：若子空间 \\( W \\) 满足 \\( \mathscr{A}W \subset W \\)，则称 \\( W \\) 是 \\( \mathscr{A} \\) 的 **不变子空间**（或 \\( \mathscr{A} \\)-子空间）。
*   **定义 7.7.8**：子空间 \\( V_i = \{ \xi \in V \mid (\mathscr{A} - \lambda_i \mathscr{E})^{r_i} \xi = \mathbf{0} \} \\) 称为 \\( \mathscr{A} \\) 属于特征值 \\( \lambda_i \\) 的 **根子空间**。
*   **定义 7.8.9**：主对角线为 \\( \lambda_0 \\) 且次对角线为 1 的矩阵称为 **若尔当块**；由若干若尔当块组成的准对角阵称为 **若尔当形矩阵**。
*   **定义 7.9.10**：以矩阵 \\( A \\) 为根的次数最低且首项系数为 1 的多项式称为 \\( A \\) 的 **最小多项式**。