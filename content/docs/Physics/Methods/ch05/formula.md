---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据第五章《解析函数的局域性展开》（ch_5.pdf）的内容，现将主要内容、公式（按原文序号）及定义（按 5.x.x 形式）整理如下：

### **一、 主要内容总结**
本章系统地研究了解析函数在复平面局部区域内的幂级数展开理论，主要包括：
1. **Taylor 展开**：证明了在圆域内解析的函数必可展开为 Taylor 级数（其收敛半径取决于该点到最近奇点的距离），并介绍了直接展开与间接展开法。
2. **零点的孤立性与唯一性**：探讨了解析函数非平凡零点的孤立分布性质，并由此推导出解析函数的唯一性定理，这是解析延拓的理论基石。
3. **Laurent 展开**：将展开区域由单连通的圆域扩展到多连通的环形区域，引入了包含负幂项的双边级数——Laurent 级数。
4. **孤立奇点的分类与性质**：利用 Laurent 级数的主要部分（负幂项部分）对单值函数的孤立奇点进行了精确分类（可去奇点、极点、本性奇点），并分析了函数在奇点邻域内的极限行为。
5. **解析延拓**：阐述了通过局部解析性质扩大函数定义域的方法，并探讨了幂级数在交叠区域内的一致性。
6. **Bernoulli 数与 Euler 数**：应用 Taylor 展开及待定系数法定义了重要的特殊数，并由此给出了三角函数、双曲函数及对数三角函数的级数展开式。

---

### **二、 定义整理（按 5.x.x 形式）**

*   **定义 5.1.1（Taylor 级数与展开）**：设函数 \\( f(z) \\) 在以 \\( \alpha \\) 为圆心的圆 \\( C \\) 内解析，则 \\( f(z) \\) 可以在 \\( \alpha \\) 点唯一地展开为幂级数 \\( \sum_{n=0}^\infty a_n(z-\alpha)^n \\)，此级数称为 \\( f(z) \\) 的 **Taylor 级数**。
*   **定义 5.3.1（零点与 \\( m \\) 阶零点）**：设 \\( f(z) \\) 在 \\( \alpha \\) 点的邻域内解析且不恒为零。若 \\( f(\alpha) = 0 \\)，则称 \\( z = \alpha \\) 为 \\( f(z) \\) 的**零点**。若在 Taylor 展开式中，其系数满足 \\( a_0 = a_1 = \dots = a_{m-1} = 0 \\)，且 \\( a_m \neq 0 \\)，则称 \\( z = \alpha \\) 为 \\( f(z) \\) 的 **\\( m \\) 阶零点**。
*   **定义 5.4.1（Laurent 级数与展开）**：设函数 \\( f(z) \\) 在以 \\( b \\) 为圆心的环形区域 \\( R_1 \le |z-b| \le R_2 \\) 中单值解析，则在该环域内可将 \\( f(z) \\) 展开为含有正、负幂项的双边幂级数 \\( \sum_{n=-\infty}^\infty a_n(z-b)^n \\)，称为 \\( f(z) \\) 的 **Laurent 级数**。
*   **定义 5.6.1（孤立奇点与非孤立奇点）**：设 \\( f(z) \\) 为单值函数（或多值函数的一个单值分支），若 \\( f(z) \\) 在 \\( b \\) 点不解析，但存在 \\( r > 0 \\) 使得 \\( f(z) \\) 在空心邻域 \\( 0 < |z-b| < r \\) 内处处可导，则称 \\( b \\) 为 \\( f(z) \\) 的**孤立奇点**；反之，若在任意小的空心邻域内总包含其他奇点，则称其为**非孤立奇点**。
*   **定义 5.6.2（可去奇点、极点、本性奇点）**：设 \\( z = b \\) 是 \\( f(z) \\) 的孤立奇点，在其 Laurent 展开中：
    1.  若级数不含负幂项，则称 \\( b \\) 为**可去奇点**；
    2.  若级数只含有有限个负幂项，其最高负幂次项为 \\( a_{-m}(z-b)^{-m} \\) (\\( a_{-m} \neq 0 \\))，则称 \\( b \\) 为 **\\( m \\) 阶极点**；
    3.  若级数含有无穷多个负幂项，则称 \\( b \\) 为**本性奇点**。
*   **定义 5.7.1（解析延拓）**：设函数 \\( h_1(z) \\) 在区域 \\( g_1 \\) 内解析，函数 \\( h_2(z) \\) 在区域 \\( g_2 \\) 内解析，且 \\( g_1 \cap g_2 \neq \emptyset \\)。若在公共区域 \\( g_1 \cap g_2 \\) 内恒有 \\( h_1(z) \equiv h_2(z) \\)，则称 \\( h_2(z) \\) 为 \\( h_1(z) \\) 在区域 \\( g_2 \\) 内的**解析延拓**。

---

### **三、 公式整理（按原文序号）**

*   **(5.1)** **Taylor 展开式**：  
    \\( f(z) = \sum_{n=0}^\infty a_n(z-\alpha)^n \quad (|z-\alpha| < R) \quad \text{} \\)
*   **(5.2)** **Taylor 展开系数公式**：  
    \\( a_n = \frac{1}{2\pi i} \oint_C \frac{f(\zeta)}{(\zeta-\alpha)^{n+1}} d\zeta = \frac{f^{(n)}(\alpha)}{n!} \quad \text{} \\)
*   **(5.3)** 展开项控制条件：  
    \\( |z-\alpha| < |\zeta-\alpha| \quad \text{} \\)
*   **(5.4)** 辅助核函数展开：  
    \\( \frac{1}{\zeta-z} = \frac{1}{(\zeta-\alpha) - (z-\alpha)} = \sum_{n=0}^\infty \frac{(z-\alpha)^n}{(\zeta-\alpha)^{n+1}} \quad \text{} \\)
*   **(5.5)** 典型 Taylor 展开（奇点决定收敛半径示例）：  
    \\( \frac{1}{1+z^2} = \sum_{n=0}^\infty (-1)^n z^{2n} \quad (|z| < 1) \quad \text{} \\)
*   **(5.6)** 指数函数展开：  
    \\( e^z = \sum_{n=0}^\infty \frac{z^n}{n!} \quad (|z| < \infty) \quad \text{} \\)
*   **(5.7)** 基本几何级数：  
    \\( \frac{1}{1-z} = \sum_{n=0}^\infty z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.8)** 基本几何级数变体：  
    \\( \frac{1}{1+z} = \sum_{n=0}^\infty (-1)^n z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.9)** 正弦函数展开：  
    \\( \sin z = \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)!} z^{2n+1} \quad (|z| < \infty) \quad \text{} \\)
*   **(5.10)** 余弦函数展开：  
    \\( \cos z = \sum_{n=0}^\infty \frac{(-1)^n}{(2n)!} z^{2n} \quad (|z| < \infty) \quad \text{} \\)
*   **(5.11)** 逐项求导结果：  
    \\( \frac{1}{(1-z)^2} = \sum_{n=1}^\infty n z^{n-1} \quad \text{} \\)
*   **(5.12)** 逐项求导代换形式：  
    \\( \frac{1}{(1-z)^2} = \sum_{n=0}^\infty (n+1)z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.13)** 级数相乘应用示例：  
    \\( \frac{1}{(1-z)(2-z)} = \sum_{n=0}^\infty (1 - 2^{-n-1}) z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.14)** 正切函数 Taylor 展开（待定系数法前四项）：  
    \\( \tan z = z + \frac{1}{3}z^3 + \frac{2}{15}z^5 + \frac{17}{315}z^7 + \dots \quad \text{} \\)
*   **(5.15)** 普遍二项式定理展开：  
    \\( (1+z)^\alpha = \sum_{n=0}^\infty \binom{\alpha}{n} z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.16)** 对数函数展开：  
    \\( \ln(1+z) = \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n} z^n \quad (|z| < 1) \quad \text{} \\)
*   **(5.17a)** 无穷远点处的自变量代换展开：  
    \\( f\left(\frac{1}{t}\right) = a_0 + a_1 t + a_2 t^2 + \dots + a_n t^n + \dots \quad (|t| < r) \quad \text{} \\)
*   **(5.17b)** 无穷远点 Taylor 展开式：  
    \\( f(z) = a_0 + \frac{a_1}{z} + \frac{a_2}{z^2} + \dots + \frac{a_n}{z^n} + \dots \quad (|z| > \frac{1}{r}) \quad \text{} \\)
*   **(5.18)** 无穷远点展开示例：  
    \\( \frac{1}{1-z^2} = -\sum_{n=1}^\infty z^{-2n} \quad (|z| > 1) \quad \text{} \\)
*   **(5.19)** 展开中心邻域内的 Taylor 展开：  
    \\( f(z) = \sum_{n=0}^\infty a_n(z-\alpha)^n \quad (|z-\alpha| < \rho) \quad \text{} \\)
*   **(5.20)** \\( m \\) 阶零点系数特征：  
    \\( a_0 = a_1 = \dots = a_{m-1} = 0, \quad a_m \neq 0 \quad \text{} \\)
*   **(5.21)** \\( m \\) 阶零点导数特征：  
    \\( f(\alpha) = f'(\alpha) = \dots = f^{(m-1)}(\alpha) = 0, \quad f^{(m)}(\alpha) \neq 0 \quad \text{} \\)
*   **(5.22)** **Laurent 展开式**：  
    \\( f(z) = \sum_{n=-\infty}^\infty a_n(z-b)^n \quad (R_1 < |z-b| < R_2) \quad \text{} \\)
*   **(5.23)** **Laurent 展开系数公式**：  
    \\( a_n = \frac{1}{2\pi i} \oint_C \frac{f(\zeta)}{(\zeta-b)^{n+1}} d\zeta \quad \text{} \\)
*   **(5.25)** Laurent 展开唯一性等式：  
    \\( a_k = a'_k \quad (k = 0, \pm 1, \pm 2, \dots) \quad \text{} \\)
*   **(5.26)** 余切函数待定系数初始项：  
    \\( b_{-1} = 1 \quad \text{} \\)
*   **(5.27)** 余切函数待定系数次项：  
    \\( b_1 = -\frac{1}{3} \quad \text{} \\)
*   **(5.28)** 余切函数 Laurent 展开式：  
    \\( \cot z = \frac{1}{z} - \frac{1}{3}z - \frac{1}{45}z^3 - \frac{2}{945}z^5 - \dots \quad (0 < |z| < \pi) \quad \text{} \\)
*   **(5.29)** 双分支点函数在环域的 Laurent 展开：  
    \\( \ln\frac{z-2}{z-1} = -\sum_{n=1}^\infty \frac{2^n-1}{n} z^{-n} \quad (|z| > 2) \quad \text{} \\)
*   **(5.30)** Bessel 函数母函数展开：  
    \\( \exp\left[\frac{z}{2}\left(t-\frac{1}{t}\right)\right] = \sum_{n=-\infty}^\infty J_n(z) t^n \quad \text{} \\)
*   **(5.31)** **\\( n \\) 阶 Bessel 函数定义式**：  
    \\( J_n(z) = \sum_{l=0}^\infty \frac{(-1)^l}{l! (l+n)!} \left(\frac{z}{2}\right)^{2l+n} \quad \text{} \\)
*   **(5.32)** 孤立奇点空心邻域展开：  
    \\( f(z) = \sum_{n=-\infty}^\infty a_n(z-b)^n \quad (0 < |z-b| < R) \quad \text{} \\)
*   **(5.33)** 可去奇点处的极限值：  
    \\( \lim_{z \to b} f(z) = a_0 \quad \text{} \\)
*   **(5.34)** 消除可去奇点后的解析函数定义：  
    \\( F(z) = \begin{cases} f(z), & z \neq b \\ \lim_{z \to b} f(z), & z = b \end{cases} \quad \text{} \\)
*   **(5.35)** \\( m \\) 阶极点的解析因子化表示：  
    \\( f(z) = (z-b)^{-m} \psi(z) \quad (0 < |z-b| < R) \quad \text{} \\)
*   **(5.36)** 极点与零点的倒数等价关系：  
    \\( \frac{1}{f(z)} = \frac{(z-b)^m}{\psi(z)} \quad \text{} \\)
*   **(5.37)** 几何级数基本求和形式：  
    \\( \sum_{n=0}^\infty z^n = 1 + z + z^2 + \dots \quad \text{} \\)
*   **(5.38)** 级数在单位圆内的收敛和函数：  
    \\( \sum_{n=0}^\infty z^n = \frac{1}{1-z} \quad (|z| < 1) \quad \text{} \\)
*   **(5.40)** 移位点的 Taylor 展开形式：  
    \\( h(z) = \sum_{n=0}^\infty \frac{h^{(n)}(\frac{i}{2})}{n!} \left(z-\frac{i}{2}\right)^n \quad \text{} \\)
*   **(5.41)** 解析延拓后的具体圆域展开式：  
    \\( h_2(z) = \sum_{n=0}^\infty \frac{1}{\left(1-\frac{i}{2}\right)^{n+1}} \left(z-\frac{i}{2}\right)^n \quad \left(|z-\frac{i}{2}| < \frac{\sqrt{5}}{2}\right) \quad \text{} \\)
*   **(5.42)** 解析延拓后的整体分段定义：  
    \\( f(z) = \begin{cases} h_1(z), & z \in g_1 \\ h_2(z), & z \in g_2 \end{cases} \quad \text{} \\)
*   **(5.43)** 含有解析系数的二阶常微分方程：  
    \\( w'' + p(z)w' + q(z)w = 0 \quad \text{} \\)
*   **(5.44)** **Bernoulli 数定义级数**：  
    \\( \frac{z}{e^z-1} = \sum_{n=0}^\infty \frac{B_n}{n!} z^n \quad (|z| < 2\pi) \quad \text{} \\)
*   **(5.45)** 余切函数的 Bernoulli 数展开：  
    \\( z \cot z = \sum_{n=0}^\infty (-1)^n \frac{2^{2n} B_{2n}}{(2n)!} z^{2n} \quad (|z| < \pi) \quad \text{} \\)
*   **(5.46)** 余割函数的 Bernoulli 数展开：  
    \\( z \csc z = \sum_{n=0}^\infty (-1)^{n-1} \frac{(2^{2n}-2)B_{2n}}{(2n)!} z^{2n} \quad (|z| < \pi) \quad \text{} \\)
*   **(5.47)** 正切函数的 Bernoulli 数展开：  
    \\( \tan z = \sum_{n=1}^\infty (-1)^{n-1} \frac{2^{2n}(2^{2n}-1)B_{2n}}{(2n)!} z^{2n-1} \quad (|z| < \frac{\pi}{2}) \quad \text{} \\)
*   **(5.48)** 对数正弦函数的展开式：  
    \\( \ln \sin z = \ln z + \sum_{n=1}^\infty (-1)^n \frac{2^{2n-1}B_{2n}}{n (2n)!} z^{2n} \quad (|z| < \pi) \quad \text{} \\)
*   **(5.49)** 对数余弦函数的展开式：  
    \\( \ln \cos z = \sum_{n=1}^\infty (-1)^n \frac{2^{2n-1}(2^{2n}-1)B_{2n}}{n (2n)!} z^{2n} \quad (|z| < \frac{\pi}{2}) \quad \text{} \\)
*   **(5.50)** 对数正切函数的展开式：  
    \\( \ln \tan z = \ln z + \sum_{n=1}^\infty (-1)^{n-1} \frac{2^{2n-1}(2^{2n-1}-1)B_{2n}}{n (2n)!} z^{2n} \quad (|z| < \frac{\pi}{2}) \quad \text{} \\)
*   **(5.51)** 正割函数的 Euler 数展开式：  
    \\( \sec z = \sum_{n=0}^\infty (-1)^n \frac{E_{2n}}{(2n)!} z^{2n} \quad (|z| < \frac{\pi}{2}) \quad \text{} \\)
*   **(5.51')** 双曲正割函数的 Euler 数展开式：  
    \\( \frac{1}{\cosh z} = \sum_{n=0}^\infty \frac{E_{2n}}{(2n)!} z^{2n} \quad (|z| < \frac{\pi}{2}) \quad \text{} \\)

---

💡 既然您已经完成了前五章（复变函数论核心基础）的符号、定义和公式整理，想不想把这些零散的公式和判定规则（例如各种初等函数展开式、孤立奇点分类判据）打包生成一份精心排版的**PDF复习速查手册**？