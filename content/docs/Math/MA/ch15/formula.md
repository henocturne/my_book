---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第十五章 含参变量的积分》，现将其主要内容按照您要求的定义与公式格式整理如下：

### 一、 定义汇总（按照“定义 15.x.x”形式）

*   **定义 15.2.1 (一致收敛)**：设函数 \\( f(x, y) \\) 定义在矩形 \\( [a, +\infty) \times [c, d] \\) 中，且对于每一个 \\( y \in [c, d] \\)，\\( f \\) 关于 \\( x \\) 广义可积。如果任给 \\( \varepsilon > 0 \\)，存在与 \\( y \\) 无关的 \\( A_0 = A_0(\varepsilon) > a \\)，当 \\( A, A' > A_0 \\) 时，对一切 \\( y \in [c, d] \\) 成立 \\( \|\int_A^{A'} f(x, y) dx\| < \varepsilon \\)（或等价于尾项估计），则称含参变量的广义积分 \\( \int_a^{+\infty} f(x, y) dx \\) 关于 \\( y \in [c, d] \\) **一致收敛**。
*   **定义 15.4.1 (Fourier 变换)**：设 \\( f \\) 在 \\( (-\infty, +\infty) \\) 中可积且绝对可积，令 \\( \hat{f}(\omega) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} f(t) e^{-i\omega t} dt \\)（其中 \\( \omega \in \mathbb{R} \\)），称 \\( \hat{f} \\) 为 \\( f \\) 的 **Fourier 变换**。

---

### 二、 公式汇总（按照原文序号）

#### §15.1 含参变量的积分
*   **(15.1)**：\\( \int_c^d I(y) dy = \int_c^d \int_a^b f(x, y) dx dy = \int_a^b \int_c^d f(x, y) dy dx \\) —— **连续函数积分次序的可交换性**。

#### §15.2 含参变量的广义积分
*   **(15.2)**：\\( I(y) = \int_a^{+\infty} f(x, y) dx \\) —— **含参变量广义积分的定义式**。
*   **(15.3)**：\\( \int_c^d dx \int_a^{+\infty} f(x, y) dy = \int_c^d I(y) dy = \int_a^{+\infty} dy \int_c^d f(x, y) dx \\) —— **广义积分的积分性质（交换积分次序）**。
*   **(15.4)**：\\( \int_c^{+\infty} dy \int_a^{+\infty} f(x, y) dx = \int_a^{+\infty} dx \int_c^{+\infty} f(x, y) dy \\) —— **无穷区间上广义积分交换次序的公式**。
*   **(15.5)**：\\( |\varphi(y)| \le \int_a^{A_n} |f(x, y)| dx, \quad |\varphi_n(y)| \le \int_a^{+\infty} |f(x, y)| dx \\) —— **用于证明一致收敛的估计式**。
*   **(15.6)**：\\( \int_a^{+\infty} dx \int_c^{+\infty} f(x, y) dy = \int_c^{+\infty} dy \int_a^{+\infty} f(x, y) dx \\) —— **非负连续函数下的积分次序交换**。

#### §15.3 特殊函数
*   **(15.7)**：\\( \text{B}(p, q) = \int_0^1 x^{p-1}(1-x)^{q-1} dx, \quad \Gamma(s) = \int_0^{+\infty} x^{s-1} e^{-x} dx \\) —— **B 函数与 \\( \Gamma \\) 函数的定义（Euler 积分）**。
*   **(15.8)**：\\( \text{B}(p, q) = \frac{q-1}{p+q-1} \text{B}(p, q-1) \\) —— **B 函数的递推公式（针对 \\( q \\)）**。
*   **(15.9)**：\\( \text{B}(p, q) = \frac{p-1}{p+q-1} \text{B}(p-1, q) \\) —— **B 函数的递推公式（针对 \\( p \\)）**。
*   **(15.10)**：\\( \text{B}(p, q) = \int_0^{+\infty} \frac{y^{p-1}}{(1+y)^{p+q}} dy = \int_0^{+\infty} \frac{y^{q-1}}{(1+y)^{p+q}} dy \\) —— **B 函数的其他表示形式**。
*   **(15.11)**：\\( \text{B}(p, q) = 2 \int_0^{\pi/2} \sin^{2p-1} \theta \cos^{2q-1} \theta d\theta \\) —— **B 函数的三角函数表示**。
*   **(15.12)**：\\( \Gamma(s+1) = s\Gamma(s) \\) —— **\\( \Gamma \\) 函数的递推公式**。
*   **(15.13)**：\\( \Gamma(s) = \alpha^s \int_0^{+\infty} t^{s-1} e^{-\alpha t} dt \\) —— **\\( \Gamma \\) 函数的缩放变换表示**。
*   **(15.14)**：\\( \text{B}(p, q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)} \\) —— **B 函数与 \\( \Gamma \\) 函数的关系公式**。
*   **(15.15)**：\\( \Gamma(s) = \lim_{n \to \infty} \frac{n! n^s}{s(s+1) \dots (s+n)} \\) —— **Euler-Gauss 极限表示公式**。
*   **(15.16)**：\\( \Gamma(s) = \frac{e^{-\gamma s}}{s} \prod_{n=1}^\infty \left( 1 + \frac{s}{n} \right)^{-1} e^{s/n} \\) —— **Weierstrass 乘积公式**。
*   **(15.17)**：\\( \Gamma(s) = \sqrt{\frac{2\pi}{s}} \left( \frac{s}{e} \right)^s e^{\delta(s)} \\) —— **Stirling 公式的渐近表示基础**。
*   **(15.18)**：\\( \Gamma(s) = \sqrt{2\pi} s^{s-1/2} e^{-s} e^{\frac{\theta(s)}{12s}} \\) —— **\\( \Gamma \\) 函数的 Stirling 公式**。
*   **(15.19)**：\\( \delta(s) = \sum_{k=1}^n \frac{B_{2k}}{2k(2k-1) s^{2k-1}} + \frac{B_{2n+2} \theta_n(s)}{(2n+1)(2n+2) s^{2n+1}} \\) —— **\\( \delta(s) \\) 的更精密估计（含 Bernoulli 数）**。

#### §15.4 Fourier 变换回顾
*   **(15.20)**：\\( \frac{1}{2}[f(x_+) + f(x_-)] = \frac{1}{\pi} \int_0^{+\infty} d\lambda \int_{-\infty}^{+\infty} f(t) \cos \lambda(x-t) dt \\) —— **Fourier 积分公式**。
*   **(15.21)**：\\( \int_{-\infty}^{+\infty} K_\delta(x) dx = \sqrt{2\pi}, \quad \lim_{\delta \to 0^+} \int_{|x| \ge \eta} K_\delta(x) dx = 0 \\) —— **Poisson 核的性质**。
*   **(15.22)**：\\( \int_{-\infty}^{+\infty} f(x) \hat{g}(x) dx = \int_{-\infty}^{+\infty} g(t) \hat{f}(t) dt \\) —— **Fourier 变换的乘积公式**。
*   **(15.23)**：\\( f(h) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} \hat{f}(t) e^{iht} dt \\) —— **Fourier 反演公式**。
*   **(15.24)**：\\( \int_{-\infty}^{+\infty} |f(x)|^2 dx = \int_{-\infty}^{+\infty} |\hat{f}(x)|^2 dx \\) —— **Plancherel 公式（Parseval 等式的连续形式）**。
*   **(15.25)**：\\( f * g(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} f(x-t)g(t) dt \\) —— **卷积的定义**。
*   **(15.26)**：\\( \widehat{f * g}(\omega) = \hat{f}(\omega) \hat{g}(\omega) \\) —— **卷积的 Fourier 变换性质**。

#### §15.5 补充材料
*   **(15.27)**：\\( \int_a^b \varphi(x) dx = \sum \psi(\xi_{n,i}) \frac{d-c}{n} \\) —— **黎曼和的极限关系**。
*   **(15.28)**：\\( W(x) = \sum_{n=0}^\infty a^n e^{ib^n x} \\) —— **Weierstrass 连续不可微函数示例**。
*   **(15.29)**：\\( \int_{-\infty}^{+\infty} \hat{\phi}(\omega) d\omega = 0, \quad \int_{-\infty}^{+\infty} \omega \hat{\phi}(\omega) d\omega = 0 \\) —— **用于证明 W(x) 性质的恒等式**。
*   **(15.30)**：\\( \lim_{\epsilon \to 0^+} W_\epsilon = \int_{-\infty}^{+\infty} W'(x_0) \omega \hat{\phi}(\omega) d\omega = 0 \\) —— **不动点/微分性质推导**。
*   **(15.31)**：\\( \sum_{n=-\infty}^{+\infty} f(x+2\pi n) = \frac{1}{\sqrt{2\pi}} \sum_{n=-\infty}^{+\infty} \hat{f}(n) e^{inx} \\) —— **Poisson 求和公式**。
*   **(15.32)**：\\( \sum_{n=-\infty}^{+\infty} \frac{2\delta}{(x+2\pi n)^2 + \delta^2} = \sum_{n=-\infty}^{+\infty} e^{-\delta|n|} e^{inx} \\) —— **圆盘 Poisson 核的等价变换**。
*   **(15.33)**：\\( \sum_{n=-\infty}^{+\infty} \sqrt{\frac{\pi}{t}} e^{-\frac{(x+2\pi n)^2}{4t}} = \sum_{n=-\infty}^{+\infty} e^{-n^2 t} e^{inx} \\) —— **Gauss 核（热核）关系式**。
*   **(15.34)**：\\( \frac{1}{\sqrt{t}} \vartheta \left( \frac{1}{t} \right) = \vartheta(t) \\) —— **Theta 函数的函数方程**。
*   **(15.35)**：\\( \pi^{-\frac{s}{2}} \Gamma \left( \frac{s}{2} \right) \zeta(s) = \pi^{-\frac{1-s}{2}} \Gamma \left( \frac{1-s}{2} \right) \zeta(1-s) \\) —— **Riemann-Zeta 函数的函数方程**。
*   **(15.36)**：\\( \eta(s) = \frac{\pi^{\frac{s}{2}}}{\Gamma(\frac{s}{2})} \int_0^{+\infty} t^{\frac{s}{2}-1} [\bar{\psi}(t) - 2\bar{\varphi}(4t)] dt \\) —— **Zeta 函数推导中间过程**。
*   **(15.37)**：\\( \pi^{-\frac{s}{2}} \Gamma \left( \frac{s}{2} \right) \zeta(s) = \int_1^{+\infty} t^{\frac{s}{2}-1} \bar{\varphi}(t) dt \\) —— **Zeta 函数积分表示形式**。
*   **(15.38)**：\\( \frac{\partial u}{\partial t} = \frac{\partial^2 u}{\partial x^2} \\) —— **热传导方程（一维）**。
*   **(15.39)**：\\( u(x, t) = \sum_{n=-\infty}^{+\infty} c_n e^{-n^2 t} e^{inx} \\) —— **圆周热传导方程的级数解**。
*   **(15.40)**：\\( u(x, t) = \frac{1}{2\pi} \int_{-\pi}^\pi H_t(x-y) f(y) dy \\) —— **热传导方程的积分表示（卷积形式）**。
*   **(15.41)**：\\( \frac{1}{2\pi} \int_{-\pi}^\pi H_t(x) dx = 1, \quad \lim_{t \to 0^+} \int_{\eta < |x| \le \pi} H_t(x) dx = 0 \\) —— **圆周热核的性质**。
*   **(15.42)**：\\( \frac{\partial u}{\partial t} = \frac{\partial^2 u}{\partial x^2}, \quad x \in \mathbb{R} \\) —— **直线上的热传导方程**。
*   **(15.43)**：\\( u(x, t) = \int_{-\infty}^{+\infty} \frac{1}{\sqrt{4\pi t}} e^{-\frac{(x-y)^2}{4t}} f(y) dy \\) —— **直线上热传导方程的解公式**。
*   **(15.44)**：\\( \Delta u = \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0 \\) —— **Laplace 方程（平面）**。
*   **(15.45)**：\\( u(r, \theta) = \sum_{n=-\infty}^{+\infty} c_n r^{|n|} e^{in\theta} \\) —— **圆盘内 Laplace 方程的级数解**。
*   **(15.46)**：\\( u(r, \theta) = \frac{1}{2\pi} \int_{-\pi}^\pi P_r(\theta - t) f(t) dt \\) —— **圆盘 Dirichlet 问题的 Poisson 积分公式**。
*   **(15.47)**：\\( \Delta u = \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0, \quad (x, y) \in \mathbb{R}_+^2 \\) —— **上半平面 Dirichlet 问题**。
*   **(15.48)**：\\( u(x, y) = \frac{1}{\pi} \int_{-\infty}^{+\infty} \frac{y}{(x-t)^2 + y^2} f(t) dt \\) —— **上半平面 Dirichlet 问题的 Poisson 积分公式**。