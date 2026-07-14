---
title: "definition"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第九章 Fourier 分析》，本章定义并使用了多类关于三角级数、收敛性估计、核函数以及 Fourier 积分的数学符号。以下是这些符号的总结：

### 1. Fourier 级数与系数符号
*   **\\( a_k, b_k \\)**：**Fourier 系数**。其中 \\( a_0 = \frac{1}{\pi} \int_{-\pi}^\pi f(x) dx \\)，\\( a_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \cos kx dx \\)，\\( b_k = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \sin kx dx \\)。
*   **\\( \sim \\)**：**Fourier 展开符号**。表示函数 \\( f(x) \\) 形式上展开为对应的 Fourier 级数。
*   **\\( S_n(x) \\) 或 \\( S_n(f, x) \\)**：Fourier 级数的**第 \\( n \\) 个部分和**，定义为 \\( \frac{a_0}{2} + \sum_{k=1}^n (a_k \cos kx + b_k \sin kx) \\)。
*   **\\( \{1, \cos x, \sin x, \dots\} \\)**：**三角函数系**。

### 2. 特殊核函数符号
*   **\\( \sigma_n(u) \\)**：**Dirichlet 核**（狄利克雷核），其表达式为 \\( \sigma_n(u) = \frac{1}{2} + \sum_{k=1}^n \cos ku = \frac{\sin(n + \frac{1}{2})u}{2 \sin \frac{u}{2}} \\)。
*   **\\( \mathcal{F}_n(u) \\)**：**Fejér 核**（费耶核），用于定义 Fourier 级数的平均收敛性，表达式为 \\( \mathcal{F}_n(u) = \frac{1}{2n\pi} \frac{\sin^2 \frac{nu}{2}}{\sin^2 \frac{u}{2}} \\)。

### 3. 复数表示与算子符号
*   **\\( i \\)**：**虚数单位**，满足 \\( i = \sqrt{-1} \\)。
*   **\\( e^{inx} \\)**：复指数形式的基函数，通过 Euler 公式 \\( e^{ix} = \cos x + i \sin x \\) 与三角函数联系。
*   **\\( c_n \\)**：**复 Fourier 系数**，定义为 \\( c_n = \frac{1}{2\pi} \int_{-\pi}^\pi f(x) e^{-inx} dx \\)。

### 4. 极限、估计与空间符号
*   **\\( f(x+0), f(x-0) \\)** 或 **\\( f(x_+), f(x_-) \\)**：函数 \\( f \\) 在点 \\( x \\) 处的**右极限与左极限**。
*   **\\( o(\frac{1}{n^k}), O(\frac{1}{n^k}) \\)**：**渐近符号**，用于描述 Fourier 系数随 \\( n \\) 增大的趋近速度（如 Riemann-Lebesgue 引理相关估计）。
*   **\\( C^k[-\pi, \pi] \\)**：表示在 \\( [-\pi, \pi] \\) 上具有 **\\( k \\) 阶连续导数**的函数空间。
*   **\\( R[-\pi, \pi] \\)**：表示在该区间上 **Riemann 可积**的函数集合。
*   **\\( L, \alpha \\)**：常用于定义 **Hölder 条件** 或 **Lipschitz 条件** 的常数。

### 5. 一般周期与积分变换符号
*   **\\( 2l \\)**：表示**一般周期**。此时 Fourier 系数 \\( a_n, b_n \\) 中的积分区间变为 \\( [-l, l] \\)，三角函数变为 \\( \cos \frac{n\pi x}{l} \\) 和 \\( \sin \frac{n\pi x}{l} \\)。
*   **\\( a(\lambda), b(\lambda) \\)**：**Fourier 积分系数**。当周期趋于无穷大时，由级数系数演变而来的关于连续变量 \\( \lambda \\) 的函数。
*   **\\( S(\alpha, x) \\)**：**Fourier 积分的部分和**（积分形式）。

### 6. 其他特殊数学符号
*   **\\( \zeta(s) \\)**：**Riemann-Zeta 函数**。本章通过 Fourier 级数计算了特定值，如 \\( \zeta(2) = \frac{\pi^2}{6} \\) 和 \\( \zeta(4) = \frac{\pi^4}{90} \\)。
*   **\\( \sigma_n(f)(x) \\)**：部分和的**算术平均值**（Cesàro 平均），用于 Fejér 定理。