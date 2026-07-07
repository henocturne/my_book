---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据第十四章《微分形式的积分》的源文件，现将其主要公式和核心定义按照您的要求整理如下：

### 一、 公式汇总（按照原文序号）

*   **(14.1)**：\\( \omega = \sum_{i=1}^n w_i dx_i \\)
    *   **内容**：\\( 1 \\)-形式在标准基下的坐标表示，其中 \\( w_i = \omega(e_i) \\)。
*   **(14.2)**：\\( \omega = \sum_{i<j} \omega_{ij} dx_i \wedge dx_j \\)
    *   **内容**：\\( 2 \\)-形式（或称二次微分形式）的坐标表示，满足反对称性 \\( \omega_{ji} = -\omega_{ij} \\)。
*   **(14.3)**：\\( \phi^1 \wedge \phi^2 \wedge \dots \wedge \phi^q = \sum_{\pi \in S_q} (-1)^\pi \phi^{\pi(1)} \otimes \phi^{\pi(2)} \otimes \dots \otimes \phi^{\pi(q)} \\)
    *   **内容**：利用张量积定义的 \\( q \\) 次多项线性型的外积（楔积）公式。
*   **(14.4)**：\\( \phi^{\pi(1)} \wedge \phi^{\pi(2)} \wedge \dots \wedge \phi^{\pi(q)} = (-1)^\pi \phi^1 \wedge \phi^2 \wedge \dots \wedge \phi^q \\)
    *   **内容**：描述外积在置换作用下的性质，即改变因子的顺序会引入置换的奇偶性符号。
*   **(14.5)**：\\( \omega = \sum_{i_1 < i_2 < \dots < i_q} w_{i_1 i_2 \dots i_q} dx_{i_1} \wedge dx_{i_2} \wedge \dots \wedge dx_{i_q} \\)
    *   **内容**：\\( q \\)-形式（或称 \\( q \\) 次微分形式）的标准坐标表示。
*   **(14.6)**：\\( \omega^n = \omega \wedge \omega \wedge \dots \wedge \omega = (-1)^{\frac{n(n-1)}{2}} n! dx \\)
    *   **内容**：辛形式（symplectic form）的 \\( n \\) 次幂与体积形式之间的关系。
*   **(14.7)**：\\( \psi^*(dx) = \sum_{1 \le j_1 < j_2 < \dots < j_n \le m} \frac{\partial(\psi_1, \psi_2, \dots, \psi_n)}{\partial(x_{j_1}, x_{j_2}, \dots, x_{j_n})} dx_{j_1} \wedge dx_{j_2} \wedge \dots \wedge dx_{j_n} \\)
    *   **内容**：体积形式在拉回（pullback）映射下的变换公式，即 Binet-Cauchy 公式。
*   **(14.8)**：\\( \det J(\psi \circ \varphi) = \sum_{1 \le j_1 < j_2 < \dots < j_n \le m} \frac{\partial(\psi_1, \dots, \psi_n)}{\partial(y_{j_1}, \dots, y_{j_n})}(\varphi) \frac{\partial(\varphi_{j_1}, \dots, \varphi_{j_n})}{\partial(x_1, \dots, x_n)} \\)
    *   **内容**：复合映射 Jacobi 行列式的展开形式。
*   **(14.9)**：\\( \det(BA) = \sum_{1 \le j_1 < j_2 < \dots < j_n \le m} B \begin{pmatrix} 1 & 2 & \dots & n \\ j_1 & j_2 & \dots & j_n \end{pmatrix} A \begin{pmatrix} j_1 & j_2 & \dots & j_n \\ 1 & 2 & \dots & n \end{pmatrix} \\)
    *   **内容**：线性代数中 Binet-Cauchy 公式的矩阵表示。
*   **(14.10)**：\\( \epsilon_0 \text{div } E = \rho \\)
    *   **内容**：Maxwell 方程组中的**电场 Gauss 定律**。
*   **(14.11)**：\\( \text{div } B = 0 \\)
    *   **内容**：Maxwell 方程组中的**磁场 Gauss 定律**。
*   **(14.12)**：\\( \text{rot } B = \mu_0 J + \frac{1}{c^2} \frac{\partial E}{\partial t} \\)
    *   **内容**：Maxwell 方程组中的 **Ampère-Maxwell 定律**。
*   **(14.13)**：\\( \text{rot } E = -\frac{\partial B}{\partial t} \\)
    *   **内容**：Maxwell 方程组中的 **Faraday 定律**。

---

### 二、 定义整理（按照“定义 14.x.x”形式）

*   **定义 14.1.1 (\\( 1 \\)-形式)**：在 \\( \mathbb{R}^n \\) 的对偶空间 \\( (\mathbb{R}^n)^* \\) 中取值的函数称为 **\\( 1 \\)-形式**。其在标准基下可表示为坐标函数与基本微分 \\( dx_i \\) 的线性组合。
*   **定义 14.1.2 (\\( 1 \\)-形式的积分)**：设 \\( \sigma: [\alpha, \beta] \rightarrow \mathbb{R}^n \\) 为分段 \\( C^1 \\) 的连续曲线，\\( \omega \\) 为连续 \\( 1 \\)-形式，则 \\( \omega \\) 沿 \\( \sigma \\) 的积分定义为 \\( \int_\sigma \omega = \int_\alpha^\beta \omega^{\#}(\sigma(t)) \cdot \sigma'(t) dt \\)，这对应于物理上的第二型曲线积分。
*   **定义 14.1.3 (\\( q \\) 次多线型)**：设 \\( 1 \le q \le n \\)，\\( \mathbb{R}^n \\) 中的一个 **\\( q \\) 次多线型**是指定义在 \\( \mathbb{R}^n \times \dots \times \mathbb{R}^n \\)（\\( q \\) 个相乘）中的函数，要求它关于每一分量都是线性的。若其具有反对称性，则称为反对称 \\( q \\) 次多线型。
*   **定义 14.1.4 (\\( q \\)-形式)**：取值在反对称 \\( q \\) 次多线型空间 \\( \wedge^q(\mathbb{R}^n)^* \\) 中的场称为 **\\( q \\)-形式**或 **\\( q \\) 次微分形式**。
*   **定义 14.2.1 (拉回映射)**：设 \\( L: \mathbb{R}^n \rightarrow \mathbb{R}^m \\) 为线性映射，它诱导了对偶空间之间的线性映射 \\( L^*: (\mathbb{R}^m)^\* \rightarrow (\mathbb{R}^n)^\* \\)，称为由 \\( L \\) 所诱导的**拉回映射**。
*   **定义 14.2.2 (外微分)**：给定 \\( C^k \\) 级 \\( q \\)-形式 \\( \omega \\)，其**外微分** \\( d\omega \\) 定义为一个 \\( (q+1) \\)-形式，其计算方式是对 \\( \omega \\) 的分量函数求全微分并与原微分形式作外积。
*   **定义 14.2.3 (闭形式与恰当形式)**：若 \\( d\omega = 0 \\)，则称 \\( \omega \\) 为**闭形式**；若存在 \\( \eta \\) 使得 \\( \omega = d\eta \\)，则称 \\( \omega \\) 为**恰当形式**。
*   **定义 14.2.4 (Hodge 星算子)**：设 \\( dx_I \\) 为基本 \\( q \\)-形式，其 **Hodge 星算子**作用结果为 \\( *(dx_I) = \epsilon_I dx_{\bar{I}} \\)，将 \\( q \\)-形式映射为 \\( (n-q) \\)-形式。
*   **定义 14.3.1 (支集)**：函数 \\( f \\) 的**支集** \\( \text{supp } f \\) 定义为集合 \\( \{x \mid f(x) \neq 0\} \\) 的闭包。
*   **定义 14.3.2 (单位分解)**：设 \\( K \\) 为 \\( \mathbb{R}^n \\) 中的有界闭集，\\( \{V_\alpha\} \\) 为其有限开覆盖，存在一族光滑函数 \\( \{\phi_\alpha\} \\) 使得其和在 \\( K \\) 上恒为 1，且每个函数的支集都包含在某个覆盖元素内，称之为**单位分解**。
*   **定义 14.3.3 (正则区域)**：如果 \\( \mathbb{R}^n \\) 中的区域 \\( \Omega \\) 的边界上每一点都是正则点（即局部可参数化且满足 Jacobi 行列式条件），则称 \\( \Omega \\) 为**正则区域**。