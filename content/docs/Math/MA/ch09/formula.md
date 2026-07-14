---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第九章 Fourier 分析》，现将其主要内容按照您要求的格式整理如下：

### 一、 定义汇总（按照“定义 9.x.x”形式整理）

*   **定义 9.1.1 (Fourier 系数)**：设 \\( f \\) 为 \\( 2\pi \\) 周期函数，且 Riemann 可积或广义绝对可积。令
    \\( a_0 = \frac{1}{\pi} \int_{-\pi}^\pi f(x) dx, \quad a_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \cos kx dx, \\)
    \\( b_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \sin kx dx, \quad k = 1, 2, \dots \\)
    \\( a_0, a_k, b_k \\) 称为 \\( f \\) 的 **Fourier 系数**。

---

### 二、 公式汇总（按照原文序号整理）

*   **(9.1)**：\\( a_0 = \frac{1}{\pi} \int_{-\pi}^\pi f(x) dx, \quad a_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \cos kx dx, \quad b_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \sin kx dx \\)
    *   **内容**：\\( 2\pi \\) 周期函数的 Fourier 系数计算公式。
*   **(9.2)**：\\( \sigma_n(u) = \frac{\sin(n + \frac{1}{2})u}{2 \sin \frac{u}{2}} \\)
    *   **内容**：**Dirichlet 核**（狄利克雷核）的封闭形式表达式。
*   **(9.3)**：\\( S_n(x) = \frac{1}{\pi} \int_0^\pi \frac{f(x+u) + f(x-u)}{2} \frac{\sin(n + \frac{1}{2})u}{\sin \frac{u}{2}} du \\)
    *   **内容**：利用 Dirichlet 核表示的 Fourier 级数**第 \\( n \\) 个部分和的积分形式**。
*   **(9.4)**：\\( \sin \mu x = \frac{2 \sin \mu\pi}{\pi} \sum_{n=1}^\infty \frac{(-1)^n n}{\mu^2 - n^2} \sin nx \\)
    *   **内容**：当 \\( \mu \notin \mathbb{Z} \\) 时，函数 \\( \sin \mu x \\) 的 Fourier 展开式。
*   **(9.5)**：\\( \frac{1}{\pi} \int_{-\pi}^\pi [S_n(x) - f(x)]^2 dx = \frac{1}{\pi} \int_{-\pi}^\pi f^2(x) dx - [\frac{a_0^2}{2} + \sum_{k=1}^n (a_k^2 + b_k^2)] \\)
    *   **内容**：描述部分和 \\( S_n(x) \\) 逼近 \\( f(x) \\) 时**平均误差**（平方误差）的恒等式。
*   **(9.6)**：\\( \frac{1}{\pi} \int_{-\pi}^\pi f^2(x) dx = \frac{a_0^2}{2} + \sum_{n=1}^\infty (a_n^2 + b_n^2) \\)
    *   **内容**：**Parseval 恒等式**，建立了函数平方积分与 Fourier 系数平方和之间的关系。
*   **(9.7)**：\\( \sigma_n(f)(x) - f(x) = \int_{-\pi}^\pi [f(x+u) - f(x)] \mathcal{F}_n(u) du \\)
    *   **内容**：利用 **Fejér 核** \\( \mathcal{F}_n(u) \\) 表示的 Fourier 级数平均收敛误差的积分式。
*   **(9.8)**：\\( S_n(f, x) - f(x) = \frac{1}{2\pi} \int_{-\pi}^\pi [g(t) - g(t + \frac{\pi}{\mu})] \sin \mu t dt \\)
    *   **内容**：在证明 Hölder 连续函数 Fourier 展开一致收敛时使用的**误差估计积分变形**。
*   **(9.9)**：\\( |S_n(f, x) - f(x)| \le C(\frac{2}{n} + 1) \frac{3\pi + 2 \ln n}{2n+1} \\)
    *   **内容**：针对 **Lipschitz 连续函数**（\\( \alpha=1 \\)）Fourier 展开的一致收敛速度估计。
*   **(9.10)**：\\( |S_n(f, x) - f(x)| \le C(\frac{1}{\alpha} + \frac{1}{2}) \frac{3\pi + 2 \ln n}{(n + \frac{1}{2})^\alpha} \\)
    *   **内容**：针对 **Hölder 连续函数**（\\( 0 < \alpha < 1 \\)）Fourier 展开的一致收敛速度估计。
*   **(9.11)**：\\( 1 + \frac{2}{\pi} \ln(n+1) < \int_0^\pi |\sigma_n(t)| dt < 3 + \frac{2}{\pi} \ln n \\)
    *   **内容**：**Dirichlet 核在 \\( L^1 \\) 范数意义下的估计**，说明了部分和算子范数随 \\( n \\) 对数增长。
*   **(9.12)**：\\( h^{-2} F_h(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx) \phi(\frac{nh}{2}) \\)
    *   **内容**：在 Du Bois-Reymond 定理证明中，将函数的**对称二阶差分**与三角级数联系起来的公式。
*   **(9.13)**：\\( \cos nx = \frac{1}{2}(e^{inx} + e^{-inx}), \quad \sin nx = \frac{1}{2i}(e^{inx} - e^{-inx}) \\)
    *   **内容**：**Euler 公式**的三角函数表现形式，用于推导 Fourier 级数的复数表示。
*   **(9.14)**：\\( \lim_{n \to \infty} \frac{s_n[a,b]}{n} = b-a \\)
    *   **内容**：序列在 $$ 中**等分布**（Uniform Distribution）的定义准则公式。
*   **(9.15)**：\\( \lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^n P(x_k) = \int_0^1 P(x) dx \\)
    *   **内容**：**Weyl 判别准则**，说明等分布序列关于三角多项式（及连续函数）的极限性质。
*   **(9.16)**：\\( f(x) = \frac{1}{\pi} \int_0^{+\infty} [\int_{-\infty}^{+\infty} f(t) \cos \lambda(x-t) dt] d\lambda \\)
    *   **内容**：非周期函数的 **Fourier 积分公式**。
*   **(9.17)**：\\( f(x) = \int_0^{+\infty} [a(\lambda) \cos \lambda x + b(\lambda) \sin \lambda x] d\lambda \\)
    *   **内容**：Fourier 积分利用连续系数 \\( a(\lambda), b(\lambda) \\) 的表示形式。
    