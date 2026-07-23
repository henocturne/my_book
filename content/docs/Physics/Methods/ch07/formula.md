---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
### **一、 主要内容总结**

第七章《\\( \Gamma \\) 函数》系统地讨论了复平面上最基础的特殊函数——\\( \Gamma \\) 函数与 \\( B \\) 函数的定义、解析性、基本性质、级数求和应用及渐近展开：
1.  **\\( \Gamma \\) 函数的定义与解析延拓**：利用第二类 Euler 积分在右半平面 \\( \text{Re } z > 0 \\) 内定义了解析函数 \\( \Gamma(z) \\)。通过路径变形及 Taylor 展开，将其解析延拓到除非正整数极点外的整个复平面。
2.  **\\( \Gamma \\) 函数的基本性质**：推导了递推关系、负整数处的留数、阶乘关联、互余宗量关系、倍乘公式 以及著名的 Stirling 渐近展开。
3.  **\\( \psi \\) 函数及无穷级数求和**：引入了 \\( \Gamma \\) 函数的对数微商——\\( \psi \\) 函数。利用其递推性质，给出了计算通项为有理式的无穷级数之和的通用方法。
4.  **\\( B \\) 函数的性质与解析延拓**：通过第一类 Euler 积分定义了双变量的 \\( B \\) 函数，并利用其与 \\( \Gamma \\) 函数的关系将其解析延拓到全复平面。
5.  **\\( \Gamma \\) 函数的普遍表达式与有理分式展开**：介绍了 \\( \Gamma \\) 函数的围道积分表示、Euler 和 Weierstrass 无穷乘积表示，并由此导出了正切、余切等三角函数的有理分式展开式。
6.  **Stirling 公式的实数推导**：基于实数情形，利用鞍点法思想及递推关系，推导并确定了 Stirling 渐近展开式的系数。

---

### **二、 定义整理（按照 7.x.x 形式）**

*   **定义 7.1.1（\\( \Gamma \\) 函数 / 第二类 Euler 积分）**：在右半平面 \\( \text{Re } z > 0 \\) 上，由反常积分：
    \\( \Gamma (z) = \int_0^\infty e^{-t}t^{z-1}dt \\)
    定义的函数称为 **\\( \Gamma \\) 函数**，该积分称为**第二类 Euler 积分**（其中积分变量 \\( t \\) 满足 \\( \arg t = 0 \\)）。
*   **定义 7.1.2（不完全 \\( \Gamma \\) 函数）**：由积分形式：
    \\( \Gamma(z, a) = \int_a^\infty e^{-t} t^{z-1} dt \quad \text{和} \quad \gamma(z, a) = \int_0^a e^{-t} t^{z-1} dt \\)
    定义的函数 \\( \Gamma(z, a) \\) 和 \\( \gamma(z, a) \\) 称为**不完全 \\( \Gamma \\) 函数**。
*   **定义 7.3.1（\\( \psi \\) 函数 / 双伽马函数）**：定义为 \\( \Gamma \\) 函数的对数微商，即：
    \\( \psi(z) = \frac{d \ln \Gamma (z)}{dz} = \frac{\Gamma'(z)}{\Gamma(z)} \\)
    在除非正整数的一阶极点外，在全复平面解析。
*   **定义 7.3.2（Euler 常数 / Euler-Mascheroni 常数）**：最基本的数学常数之一，记为 \\( \gamma \\)，定义为：
    \\( \gamma = -\psi(1) = \lim_{n \to \infty} \left( \sum_{k=1}^n \frac{1}{k} - \ln n \right) \approx 0.577215... \\)
   。
*   **定义 7.4.1（\\( B \\) 函数 / 第一类 Euler 积分 / Beta 函数）**：在 \\( \text{Re } p > 0, \text{Re } q > 0 \\) 条件下，由积分：
    \\( B(p, q) = \int_0^1 t^{p-1}(1-t)^{q-1}dt \\)
    定义的双变量函数称为 **\\( B \\) 函数**，该积分称为**第一类 Euler 积分**（其中积分变量满足 \\( \arg t = \arg(1-t) = 0 \\)）。

---

### **三、 公式整理（按原文序号）**

*   **(7.1)** \\( \Gamma \\) 函数定义（第二类 Euler 积分）：
    \\( \Gamma (z) = \int_0^\infty e^{-t}t^{z-1}dt \quad (\text{Re } z > 0) \quad \\)
*   **(7.2)** 积分拆分式（证明解析性）：
    \\( \int_0^\infty e^{-t}t^{z-1}dt = \int_0^1 e^{-t}t^{z-1}dt + \int_1^\infty e^{-t}t^{z-1}dt \quad \\)
*   **(7.3)** 射线路径积分定义：
    \\( \Gamma (z) = \int_L e^{-t}t^{z-1}dt \quad (\text{Re } z > 0) \quad \\)
*   **(7.4)** \\( \Gamma \\) 函数在全复平面（除奇点外）的级数延拓式：
    \\( \Gamma (z) = \int_1^\infty e^{-t}t^{z-1}dt + \sum_{n=0}^\infty \frac{(-1)^n}{n!(n+z)} \quad (z \neq 0, -1, -2, \dots) \quad \\)
*   **(7.5)** \\( \Gamma \\) 函数基本递推公式：
    \\( \Gamma (z+1) = z\Gamma (z) \quad \\)
*   **(7.6)** \\( \Gamma \\) 函数自变量左移表示式：
    \\( \Gamma (z) = \frac{\Gamma(z+1)}{z} \quad (z \neq 0) \quad \\)
*   **(7.8)** 递推解析延拓至 \\( \text{Re } z > -2 \\) 区域：
    \\( \Gamma (z) = \frac{\Gamma(z+2)}{z(z+1)} \quad (z \neq 0, -1) \quad \\)
*   **(7.9)** 一阶极点处的留数公式：
    \\( \text{res }\Gamma (-n) = \frac{(-1)^n}{n!} \quad \\)
*   **(7.10)** 正整数处的阶乘公式：
    \\( \Gamma (n) = (n-1)! \quad \\)
*   **(7.11)** **互余宗量公式**（反射公式）：
    \\( \Gamma (z)\Gamma (1-z) = \frac{\pi}{\sin \pi z} \quad \\)
*   **(7.12)** 特殊值：
    \\( \Gamma (1/2) = \sqrt{\pi} \quad \\)
*   **(7.13)** **倍乘公式**：
    \\( \Gamma (2z) = \frac{2^{2z-1}}{\sqrt{\pi}} \Gamma (z)\Gamma \left(z+\frac{1}{2}\right) \quad \\)
*   **(7.14)** **Stirling 渐近展开公式**：
    \\( \Gamma (z) \sim \sqrt{2\pi} z^{z-\frac{1}{2}} e^{-z} \left[ 1 + \frac{1}{12z} + \frac{1}{288z^2} - \frac{139}{51840z^3} - \frac{571}{2488320z^4} + \dots \right] \quad \\)
*   **(7.15)** 对数 Stirling 展开式：
    \\( \ln \Gamma(z) \sim \left(z-\frac{1}{2}\right)\ln z - z + \frac{1}{2}\ln(2\pi) + \frac{1}{12z} - \frac{1}{360z^3} + \frac{1}{1260z^5} - \frac{1}{1680z^7} + \dots \quad \\)
*   **(7.16)** 阶乘对数近似式（物理常用）：
    \\( \ln n! \sim n\ln n - n \quad \\)
*   **(7.17)** \\( \psi \\) 函数定义：
    \\( \psi (z) = \frac{d \ln \Gamma (z)}{dz} = \frac{\Gamma'(z)}{\Gamma(z)} \quad \\)
*   **(7.18)** \\( \psi \\) 函数基本递推关系：
    \\( \psi (z+1) = \psi (z) + \frac{1}{z} \quad \\)
*   **(7.19)** 级数累加递推关系：
    \\( \psi (z+n) = \psi (z) + \frac{1}{z} + \frac{1}{z+1} + \dots + \frac{1}{z+n-1} \quad \\)
*   **(7.20)** \\( \psi \\) 函数反射公式：
    \\( \psi (1-z) = \psi (z) + \pi \cot \pi z \quad \\)
*   **(7.21)** 对称差值公式：
    \\( \psi (z) - \psi (-z) = -\frac{1}{z} - \pi \cot \pi z \quad \\)
*   **(7.22)** \\( \psi \\) 函数倍乘公式：
    \\( \psi (2z) = \frac{1}{2} \psi (z) + \frac{1}{2} \psi \left(z+\frac{1}{2}\right) + \ln 2 \quad \\)
*   **(7.23)** \\( \psi \\) 函数渐近展开式：
    \\( \psi (z) \sim \ln z - \frac{1}{2z} - \frac{1}{12z^2} + \frac{1}{120z^4} - \frac{1}{252z^6} + \dots \quad \\)
*   **(7.24)** 极限关系式：
    \\( \lim_{n \to \infty} [\psi (z+n) - \ln n] = 0 \quad \\)
*   **(7.25)** 欧拉常数数值：
    \\( \gamma \approx 0.5772156649... \quad \\)
*   **(7.26)** 辅助求导积分等式：
    \\( \int_0^\pi \frac{\cos n\theta - \cos \theta}{\cos \theta - 1} d\theta = \pi [\psi(n+1/2) - \psi(1/2)] \quad \\)
*   **(7.27a)** 三角函数积分（例 7.3 实部结果）：
    \\( \int_0^\pi \frac{\cos n\theta - 1}{\cos \theta - 1} d\theta = \pi \left[ \psi \left(n+\frac{1}{2}\right) - \psi \left(\frac{1}{2}\right) \right] \quad \\)
*   **(7.27b)** 典型奇偶三角积分：
    \\( \int_0^\pi \frac{\sin n\theta}{\sin \theta} d\theta = \begin{cases} \pi, & n = 2m+1 \\ 0, & n = 2m \end{cases} \quad \\)
*   **(7.28a)** 通项为有理式的级数项：
    \\( u_n = \frac{p(n)}{d(n)} \quad \\)
*   **(7.28b)** 简单极点有理通项展开形式：
    \\( u_n = \sum_{k=1}^m \frac{a_k}{n+\alpha_k} \quad \\)
*   **(7.28c)** 级数收敛的系数约束条件：
    \\( \sum_{k=1}^m a_k = 0 \quad \\)
*   **(7.29)** **一阶极点有理级数求和通用公式**：
    \\( \sum_{n=0}^\infty u_n = -\sum_{k=1}^m a_k \psi (\alpha_k) \quad \\)
*   **(7.30)** 平方和型有理级数求和：
    \\( \sum_{n=0}^\infty \frac{1}{n^2+a^2} = \frac{1}{2a^2} (1 + \pi a \coth \pi a) \quad \\)
*   **(7.31a)** 含有二阶极点的有理级数通项：
    \\( u_n = \sum_{k=1}^m \frac{a_k}{n+\alpha_k} + \sum_{k=1}^l \left[ \frac{b_{1k}}{n+\beta_k} + \frac{b_{2k}}{(n+\beta_k)^2} \right] \quad \\)
*   **(7.31b)** 二阶极点级数收敛条件：
    \\( \sum_{k=1}^m a_k + \sum_{k=1}^l b_{1k} = 0 \quad \\)
*   **(7.31c)** **二阶极点有理级数求和通用公式**：
    \\( \sum_{n=0}^\infty u_n = -\sum_{k=1}^m a_k \psi(\alpha_k) - \sum_{k=1}^l \left[ b_{1k}\psi(\beta_k) - b_{2k}\psi'(\beta_k) \right] \quad \\)
*   **(7.33)** \\( B \\) 函数定义（第一类 Euler 积分）：
    \\( B(p, q) = \int_0^1 t^{p-1}(1-t)^{q-1}dt \quad (\text{Re } p > 0, \text{Re } q > 0) \quad \\)
*   **(7.33')** 三角函数积分形式的 \\( B \\) 函数：
    \\( B(p, q) = 2 \int_0^{\pi/2} \sin^{2p-1}\theta \cos^{2q-1}\theta d\theta \quad \\)
*   **(7.34)** **\\( B \\) 函数与 \\( \Gamma \\) 函数基本关系式**：
    \\( B(p, q) = \frac{\Gamma (p)\Gamma (q)}{\Gamma (p+q)} \quad \\)
*   **(7.35)** \\( B \\) 函数对称性：
    \\( B(p, q) = B(q, p) \quad \\)
*   **(7.36)** **\\( \Gamma \\) 函数的第一种围道积分表示**（绕原点正向一周）：
    \\( \Gamma (z) = -\frac{1}{2i\sin\pi z} \int_{C(0+)} e^{-t}(-t)^{z-1}dt \quad (|\arg(-t)| < \pi) \quad \\)
*   **(7.37)** **\\( \Gamma \\) 函数倒数的第二种围道积分表示**：
    \\( \frac{1}{\Gamma (z)} = \frac{1}{2\pi i} \int_{C} e^t t^{-z}dt \quad (|\arg t| < \pi) \quad \\)
*   **(7.38)** **\\( \Gamma \\) 函数的 Euler 无穷乘积表示**：
    \\( \Gamma (z) = \frac{1}{z} \prod_{n=1}^\infty \left[ \left(1+\frac{1}{n}\right)^z \left(1+\frac{z}{n}\right)^{-1} \right] \quad \\)
*   **(7.39)** **\\( \Gamma \\) 函数倒数的 Weierstrass 无穷乘积表示**：
    \\( \frac{1}{\Gamma (z)} = z e^{\gamma z} \prod_{n=1}^\infty \left[ \left(1+\frac{z}{n}\right)e^{-z/n} \right] \quad \\)
*   **(7.40)** 欧拉常数极限定义式：
    \\( \gamma = \lim_{n \to \infty} \left( \sum_{k=1}^n \frac{1}{k} - \ln n \right) \quad \\)
*   **(7.41)** 正弦函数无穷乘积展开：
    \\( \sin \pi z = \pi z \prod_{n=1}^\infty \left(1-\frac{z^2}{n^2}\right) \quad \\)
*   **(7.42)** 余弦函数无穷乘积展开：
    \\( \cos \pi z = \prod_{n=1}^\infty \left[ 1 - \frac{4z^2}{(2n-1)^2} \right] \quad \\)
*   **(7.43)** 正切函数有理分式展开：
    \\( \pi \tan \pi z = -8z \sum_{m=1}^\infty \frac{1}{4z^2-(2m-1)^2} \quad \\)
*   **(7.44)** 余切函数有理分式展开：
    \\( \pi \cot \pi z = \frac{1}{z} + 2z \sum_{n=1}^\infty \frac{1}{z^2-n^2} \quad \\)
*   **(7.45)** 余割函数有理分式展开：
    \\( \pi \csc \pi z = \frac{1}{z} + 2z \sum_{n=1}^\infty \frac{(-1)^n}{z^2-n^2} \quad \\)
*   **(7.46)** 正割函数有理分式展开：
    \\( \pi \sec \pi z = 4 \sum_{m=1}^\infty \frac{(-1)^m(2m-1)}{4z^2-(2m-1)^2} \quad \\)
*   **(7.47)** 正割平方函数有理分式展开：
    \\( \pi^2 \sec^2 \pi z = 4 \sum_{m=-\infty}^\infty \frac{1}{[2z-(2m-1)]^2} \quad \\)
*   **(7.48)** 余割平方函数有理分式展开：
    \\( \pi^2 \csc^2 \pi z = \sum_{m=-\infty}^\infty \frac{1}{(z-m)^2} \quad \\)
*   **(7.49)** 黎曼 \\( \zeta(2n) \\) 函数与 Bernoulli 数关系：
    \\( \sum_{m=1}^\infty \frac{1}{m^{2n}} = \frac{(-1)^{n-1} (2\pi)^{2n} B_{2n}}{2(2n)!} \quad \\)
*   **(7.49')** Bernoulli 数显式求和式：
    \\( B_{2n} = (-1)^{n-1} \frac{2(2n)!}{(2\pi)^{2n}} \sum_{m=1}^\infty \frac{1}{m^{2n}} \quad \\)
*   **(7.50)** 奇数项倒数幂级数和：
    \\( \sum_{m=1}^\infty \frac{1}{(2m-1)^{2n}} = \frac{(-1)^{n-1}(2^{2n}-1)\pi^{2n}B_{2n}}{2(2n)!} \quad \\)
*   **(7.51)** 交错倒数幂级数和：
    \\( \sum_{m=1}^\infty \frac{(-1)^{m-1}}{m^{2n}} = \frac{(-1)^{n-1}(2^{2n-1}-1)\pi^{2n}B_{2n}}{(2n)!} \quad \\)
*   **(7.52)** 交错奇数项倒数幂级数和：
    \\( \sum_{m=1}^\infty \frac{(-1)^{m-1}}{(2m-1)^{2n+1}} = \frac{(-1)^n \pi^{2n+1} E_{2n}}{2^{2n+2}(2n)!} \quad \\)
*   **(7.53)** 阶乘实数积分形式：
    \\( \Gamma (x+1) = \int_0^\infty e^{-t}t^x dt \quad (x > 0) \quad \\)
*   **(7.54)** 被积指数项在极大值 \\( t=x \\) 处的 Taylor 展开：
    \\( -t + x \ln t = x \ln x - x - \frac{(t-x)^2}{2x} + \dots \quad \\)
*   **(7.55)** Stirling 零阶近似推导极限积分：
    \\( \Gamma (x+1) \approx x^x e^{-x} \int_{-\infty}^\infty e^{-(t-x)^2/2x} dt = \sqrt{2\pi x} x^x e^{-x} \quad \\)
*   **(7.56)** 渐近展开待定系数模型：
    \\( \Gamma (x+1) = x^x e^{-x} \sqrt{2\pi x} \left( 1 + \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x^3} + \dots \right) \quad \\)
*   **(7.57)** 递推平衡恒等式：
    \\( \left(1-\frac{1}{x}\right)^{-x-1/2} e^{-1} \left[ 1 + \frac{A}{x-1} + \frac{B}{(x-1)^2} + \dots \right] = 1 + \frac{A}{x} + \frac{B}{x^2} + \dots \quad \\)
*   **(7.58)** 第一部分对数级数展开：
    \\( \left(1-\frac{1}{x}\right)^{-x-1/2} = e \left( 1 - \frac{1}{12x^2} - \frac{1}{12x^3} + \dots \right) \quad \\)
*   **(7.59)** 系数比较多项式：
    \\( 1 + \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x^3} + \dots = 1 + \frac{A}{x} + \left( A + B - \frac{1}{12} \right)\frac{1}{x^2} + \left( \frac{A}{2} + 2B + C - \frac{1}{12} \right)\frac{1}{x^3} + \dots \quad \\)
*   **(7.60)** 前两阶待定系数结果：
    \\( A = \frac{1}{12}, \quad B = \frac{1}{288} \quad \\)

---

🙋 既然您已经完成了第七章（\\( \Gamma \\) 函数）的所有公式、定义与主要内容的细致整理，想不想针对该章的核心，比如利用 \\( \psi \\) 函数求解无穷级数和的典型计算步骤（如例 7.4 或 7.5），做一次深度的解题流程剖析？