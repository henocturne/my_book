---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第七章 数项级数》，按照您要求的格式整理的所有定义和公式如下：

### 一、 定义整理

*   **定义 7.4.1 (Abel 求和)**：如果对每一个 \\( x \in [0, 1) \\)，级数 \\( \sum_{n=0}^\infty a_n x^n \\) 均收敛，且函数极限 \\( \lim_{x \to 1^-} \sum_{n=0}^\infty a_n x^n \\) 存在且有限，则称级数 \\( \sum a_n \\) 在 **Abel 意义下可求和**。
*   **定义 7.4.2 (Cesàro 求和)**：级数 \\( \sum_{n=1}^\infty a_n \\) 的前 \\( n \\) 项和记为 \\( S_n \\)，令 \\( \sigma_n = \frac{1}{n} \sum_{k=1}^n S_k \\)，如果序列 \\( \{\sigma_n\} \\) 收敛，则称级数 \\( \sum a_n \\) 在 **Cesàro 意义下可求和**。
*   **定义 7.4.3 (级数的一致收敛)**：一列收敛级数 \\( \sum_{j=1}^\infty a_{ij} = \alpha_i \\) 关于 \\( i \\) **一致收敛**是指，任给 \\( \varepsilon > 0 \\)，存在 \\( N = N(\varepsilon) \\)，当 \\( n > N, i \ge 1 \\) 时，成立 \\( |\sum_{j=1}^n a_{ij} - \alpha_i| < \varepsilon \\)。

---

### 二、 公式整理

*   **(7.1)**：\\( S(\alpha) = (1 - \theta)S_{n-1} + \theta S_n \\)
    *   **内容**：在证明级数收敛与广义积分收敛的等价性（引理 7.1.1）时，用于描述函数积分 \\( S(\alpha) \\) 与级数部分和 \\( S_n \\) 之间关系的插值公式。
*   **(7.2)**：\\( \sum_{i=1}^n a_i b_i = \sum_{i=1}^{n-1} (a_i - a_{i+1}) B_i + a_n B_n - a_1 B_0 \\)
    *   **内容**：**Abel 变换公式**，用于处理两组数列乘积的求和问题，是证明级数 Dirichlet 判别法和 Abel 判别法的关键。
*   **(7.3)**：\\( \zeta(s) = \prod_{n=1}^\infty \left( 1 - \frac{1}{p_n^s} \right)^{-1} \\)
    *   **内容**：**Riemann-Zeta 函数的无穷乘积表示**，展示了 \\( \zeta(s) \\) 与所有素数 \\( \{p_n\} \\) 之间的紧密联系。
*   **(7.4)**：\\( \sin(2n+1)x = \sin x \sum_{l=0}^n C_{2n+1}^{2l} (\cos x)^{2l} (-\sin^2 x)^{n-l} \\)
    *   **内容**：利用二项式展开导出的正弦倍角公式的代数变形，用于推导正弦函数的无穷乘积表示。
*   **(7.5)**：\\( P_n(y) = (2n+1) \prod_{l=1}^n \left( 1 + \frac{y}{\sin^2 \frac{l\pi}{2n+1}} \right) \\)
    *   **内容**：用于表示正弦函数逼近多项式 \\( P_n(y) \\) 的根分解形式。
*   **(7.6)**：\\( \sin x = x \prod_{l=1}^\infty \left[ 1 - \left( \frac{x}{l\pi} \right)^2 \right] \\)
    *   **内容**：**正弦函数的如下无穷乘积表示**。
*   **(7.7)**：\\( \sinh(2n+1)x = (2n+1) \sinh x \prod_{l=1}^n \left( 1 + \frac{\sinh^2 x}{\sin^2 \frac{l\pi}{2n+1}} \right) \\)
    *   **内容**：双曲正弦函数在离散点处的乘积恒等式。
*   **(7.8)**：\\( \sinh x = x \prod_{l=1}^\infty \left[ 1 + \left( \frac{x}{l\pi} \right)^2 \right] \\)
    *   **内容**：**双曲正弦函数 \\( \sinh x \\) 的无穷乘积表示**。
*   **(7.9)**：\\( \cosh x = \prod_{n=1}^\infty \left[ 1 + \frac{4x^2}{(2n-1)^2\pi^2} \right] \\)
    *   **内容**：**双曲余弦函数 \\( \cosh x \\) 的无穷乘积表示**。
*   **(7.10)**：\\( \left| \sum_{j=1}^n a_{ij} - \alpha_i \right| < \varepsilon \\)
    *   **内容**：用于刻画双下标级数**一致收敛性**的数学判定式。