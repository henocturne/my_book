---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第八章 函数项级数》，现将其主要内容按照您要求的格式整理如下：

### 一、 定义汇总（按照“定义 8.x.x”形式整理）

*   **定义 8.1.1 (一致收敛)**：设 \\( I \\) 为区间，\\( \{g_n(x)\} \\) 为 \\( I \\) 中定义的一列函数。如果任给 \\( \varepsilon > 0 \\)，均存在与 \\( x \\) 无关的正整数 \\( N = N(\varepsilon) \\)，使得当 \\( n > N, x \in I \\) 时，\\( |g_n(x) - g(x)| < \varepsilon \\) 总成立，则称函数列 \\( \{g_n\} \\) 在 \\( I \\) 中**一致收敛**于 \\( g \\)，记为 \\( g_n \rightrightarrows g \\)。
*   **函数项级数的一致收敛**（注：原文在 8.1 节中通过部分和定义）：设有函数项级数 \\( \sum_{n=1}^\infty f_n(x) \\)，若其部分和序列 \\( S_n(x) = \sum_{k=1}^n f_k(x) \\) 在区间 \\( I \\) 上一致收敛于 \\( S(x) \\)，则称该函数项级数在 \\( I \\) 上**一致收敛**。
*   **内闭一致收敛**（注：见 8.1 节末尾）：如果函数列 \\( \{f_n\} \\) 在区间 \\( I \\) 的每一个闭子区间 \\( J \subset I \\) 中都一致收敛，则称 \\( \{f_n\} \\) 在 \\( I \\) 中**内闭一致收敛**。

---

### 二、 公式汇总（按照原文序号整理）

*   **(8.1)**：\\( A_1 \supset A_2 \supset \dots \supset A_n \supset A_{n+1} \supset \dots \\) —— 用于 Dini 定理证明中的集合嵌套序列。
*   **(8.2)**：\\( |f_n(x) - f(x)| \le \frac{\varepsilon}{4(b-a)} \\) —— 定理 8.2.1 证明中关于函数一致收敛的估计式。
*   **(8.3)**：\\( \arcsin^2 x = \sum_{n=0}^\infty \frac{(2n)!!}{(2n+1)!!} \frac{x^{2n+2}}{n+1} \\) —— \\( \arcsin^2 x \\) 的 Maclaurin 展开式。
*   **(8.4)**：\\( \frac{1}{\sin^2 x} = \sum_{k \in \mathbb{Z}} \frac{1}{(x+k\pi)^2} \\) —— \\( \frac{1}{\sin^2 x} \\) 的部分分式展开。
*   **(8.5)**：\\( \frac{1}{\sin^2 x} = \frac{1}{x^2} + \sum_{n=1}^\infty \left[ \frac{1}{(x+n\pi)^2} + \frac{1}{(x-n\pi)^2} \right] \\) —— (8.4) 的另一种级数表现形式。
*   **(8.6)**：\\( \zeta(2) = \sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{6} \\) —— Riemann-Zeta 函数在 \\( s=2 \\) 时的值。
*   **(8.7)**：\\( \frac{\cos x}{\sin x} - \frac{1}{x} = \sum_{n=1}^\infty \left( \frac{1}{x+n\pi} + \frac{1}{x-n\pi} \right) \\) —— 余切函数的部分分式展开。
*   **(8.8)**：\\( \frac{\sin x}{x} = \prod_{n=1}^\infty \left[ 1 - \left( \frac{x}{n\pi} \right)^2 \right] \\) —— 正弦函数的无穷乘积表示。
*   **(8.9)**：\\( \frac{\sin x}{\cos x} = \sum_{n=1}^\infty \left[ \frac{1}{(2n-1)\frac{\pi}{2} - x} - \frac{1}{(2n-1)\frac{\pi}{2} + x} \right] \\) —— 正切函数的部分分式展开。
*   **(8.10)**：\\( \frac{1}{\sin x} = \frac{1}{x} + \sum_{n=1}^\infty (-1)^n \left( \frac{1}{x+n\pi} + \frac{1}{x-n\pi} \right) \\) —— 正割函数（此处为 \\( 1/\sin x \\)）的展开式。
*   **(8.11)**：\\( \tan x = \sum_{n=1}^\infty \frac{\zeta(2k)}{\pi^{2k}} 2(2^{2k}-1)x^{2k-1} \\) —— 正切函数的幂级数表示（含 Zeta 函数值）。
*   **(8.12)**：\\( \frac{1}{\sin^2 x} - \frac{1}{x^2} = \sum_{m=0}^\infty \frac{\zeta(2m+2)}{\pi^{2m+2}}(4m+2)x^{2m} \\) —— 涉及 \\( \sin^2 x \\) 与 Zeta 函数的关系式。
*   **(8.13)**：\\( (1+x)^\alpha = \sum_{n=0}^\infty C_\alpha^n x^n \\) —— 二项式级数展开公式。
*   **(8.14)**：\\( \frac{1}{\sqrt{1-x^2}} = 1 + \sum_{n=1}^\infty \frac{(2n-1)!!}{(2n)!!} x^{2n} \\) —— 特殊幂级数展开。
*   **(8.15)**：\\( \arcsin x = \sum_{n=0}^\infty \frac{(2n-1)!!}{(2n)!!} \frac{x^{2n+1}}{2n+1} \\) —— \\( \arcsin x \\) 的幂级数展开。
*   **(8.16)**：\\( \frac{1}{1-x} = \sum_{n=0}^\infty x^n \\) —— 几何级数基本公式。
*   **(8.17)**：\\( \frac{x}{e^x-1} = \sum_{n=0}^\infty \frac{B_n}{n!} x^n \\) —— Bernoulli 数的定义展开式。
*   **(8.18)**：\\( x \coth x = \sum_{n=0}^\infty \frac{2^{2n} B_{2n}}{(2n)!} x^{2n} \\) —— 双曲余切函数的展开式。
*   **(8.19)**：\\( \zeta(2n) = (-1)^{n-1} \frac{2^{2n} B_{2n} \pi^{2n}}{2(2n)!} \\) —— 偶数阶 Zeta 函数值与 Bernoulli 数的关系。
*   **(8.20)**：\\( \sum_{n=1}^\infty x^{n-1} \cos n\alpha = \frac{\cos \alpha - x}{1-2x \cos \alpha + x^2} \\) —— 涉及三角函数的幂级数求和。
*   **(8.21)**：\\( \sum_{n=1}^\infty \frac{x^n}{n} \cos n\alpha = -\frac{1}{2} \ln(1-2x \cos \alpha + x^2) \\) —— 级数求和公式。
*   **(8.22)**：\\( B_n(t) = \sum_{k=0}^n C_n^k B_{n-k} t^k \\) —— Bernoulli 多项式的展开式。
*   **(8.23)**：\\( B_{k+1}(t+1) - B_{k+1}(t) = (k+1)t^k \\) —— Bernoulli 多项式的差分性质。
*   **(8.24)**：\\( 1^k + 2^k + \dots + n^k = \frac{1}{k+1} \sum_{l=1}^{k+1} C_{k+1}^l B_{k+1-l} (n+1)^l \\) —— 自然数幂和的公式。
*   **(8.25)**：\\( \frac{\pi}{4} = 4 \arctan \frac{1}{5} - \arctan \frac{1}{239} \\) —— Machin 计算 \\( \pi \\) 的公式。
*   **(8.26)**：\\( \pi = 16 \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)5^{2n+1}} - 4 \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)239^{2n+1}} \\) —— 基于 Machin 公式的级数展开。
*   **(8.27)**：\\( \frac{1}{\pi} = \frac{2\sqrt{2}}{9801} \sum_{k=0}^\infty \frac{(4k)! (1103 + 26390k)}{(k!)^4 396^{4k}} \\) —— Ramanujan 计算 \\( 1/\pi \\) 的级数公式。
*   **(8.28)**：Chudnovsky 兄弟给出的 \\( \pi \\) 计算公式。
*   **(8.29)**：\\( \pi = \sum_{k=0}^\infty (\frac{4}{8k+1} - \frac{2}{8k+4} - \frac{1}{8k+5} - \frac{1}{8k+6}) \frac{1}{16^k} \\) —— BBP 公式。
*   **(8.30)**：\\( \ln 2 = \frac{2}{3} \sum_{k=0}^\infty \frac{1}{(2k+1)9^k} \\) —— 用于高精度计算 \\( \ln 2 \\) 的公式。
*   **(8.31)**：\\( \frac{xe^{tx}}{e^x-1} = \sum_{n=0}^\infty \frac{B_n(t)}{n!} x^n \\) —— Bernoulli 多项式的母函数定义。
*   **(8.32)**：Euler-Maclaurin 公式的积分表示形式。
*   **(8.33)**：带有中值余项的 Euler-Maclaurin 公式。
*   **(8.34)**：一般区间 \\( [a, b] \\) 上的 Euler-Maclaurin 公式。
*   **(8.35)**：离散形式的 Euler-Maclaurin 公式（\\( n \\) 等分）。
*   **(8.36)**：Euler-Maclaurin 公式的最终近似形式。
*   **(8.37)**：应用于 \\( f(t) = \ln t \\) 的近似求和公式。
*   **(8.38)**：\\( n! = \sqrt{2\pi n} (\frac{n}{e})^n e^{\delta_n} \\) —— Stirling 公式的精确形式。