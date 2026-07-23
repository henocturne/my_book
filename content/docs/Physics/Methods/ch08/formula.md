---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
### **一、 主要内容总结**

第八章《Laplace 变换》系统地讨论了复平面上最核心的积分变换之一——Laplace 变换（拉氏变换）的定义、性质、反演技术及定解应用：
1.  **Laplace 变换的定义及其存在条件**：定义了将正实轴实变函数 \\( f(t) \\)  变换为复平面复变函数 \\( F(p) \\)  的积分变换。给出了拉氏变换存在的充分条件（分段连续且具有有限的增长指数），并引入了收敛横标的概念。
2.  **Laplace 变换的基本性质**：包括线性性质、像函数的解析性、像函数在无穷远处的极限行为、原函数导数的 Laplace 变换、原函数积分的 Laplace 变换。展示了这些性质如何将微积分运算转化为代数运算，从而为求解常微分方程初值问题及电路定解问题提供了强有力的工具。
3.  **Laplace 变换的反演方法**：探讨了反演的唯一性。给出了像函数导数与积分的反演公式。针对像函数在 \\( \infty \\)  点解析的特殊情形，介绍了级数逐项反演的方法。证明了**卷积定理**。
4.  **普遍反演公式**：论述了 **Mellin 反演公式**，并探讨了多值像函数（含有分支点）在复平面上通过构造割线和围道进行留数计算的反演步骤。
5.  **利用 Laplace 变换计算级数和**：展示了如何通过将级数通项表示为像函数积分，并交换求和与积分次序，将离散的无穷级数求和问题转化为连续的定积分计算（如 Basel 问题 \\( \sum \frac{1}{n^2} \\)  等）。

---

### **二、 定义整理（按照 8.x.x 形式）**

*   **定义 8.1.1（Laplace 变换 / 拉氏变换）**：设 \\( f(t) \\)  是定义在正实轴（\\( t > 0 \\) ）上的非负实数函数，则由积分：
    \\( F(p) = \int_0^\infty e^{-pt} f(t) dt \quad (8.1) \\) 
    定义的复变函数 \\( F(p) \\)  称为 \\( f(t) \\)  的 **Laplace 变换式**（或拉氏换式），其中 \\( p = s + i\sigma \\)  为复自变量，\\( e^{-pt} \\)  称为 Laplace 变换的核。
*   **定义 8.1.2（原函数、像函数与反演）**：在 Laplace 变换关系中，称 \\( f(t) \\)  为 **原函数**，\\( F(p) \\)  为 **像函数**。已知像函数 \\( F(p) \\)  求原函数 \\( f(t) \\)  的运算称为 **反演**。
*   **定义 8.1.3（Heaviside 单位阶跃函数）**：定义在实数域上的函数：
    \\( \eta(t) = \begin{cases} 1, & t > 0 \\ 0, & t < 0 \end{cases} \quad (8.4) \\) 
    称为 **Heaviside 单位阶跃函数**。在拉氏变换中，常约定当 \\( t < 0 \\)  时原函数 \\( f(t) = 0 \\) ，即等价地将 \\( f(t) \\)  理解为 \\( f(t)\eta(t) \\) 。
*   **定义 8.1.4（收敛横标）**：设存在正数 \\( M > 0, t_0 > 0 \\)  及 \\( \beta' \ge 0 \\) ，使得当 \\( t > t_0 \\)  时恒有 \\( |f(t)| < M e^{\beta' t} \\) 。符合该指数增长限制条件的参数 \\( \beta' \\)  的下界称为 **收敛横标**，记为 \\( s_0 \\) （或 \\( \beta_0 \\) ），它决定了像函数 \\( F(p) \\)  的解析半平面（\\( \text{Re } p > s_0 \\) ）。
*   **定义 8.3.1（卷积）**：对于两个定义在正实轴上的函数 \\( f_1(t) \\)  和 \\( f_2(t) \\) ，其 **卷积**（记作 \\( f_1(t) * f_2(t) \\) ）定义为积分形式：
    \\( f_1(t) * f_2(t) = \int_0^t f_1(\tau) f_2(t-\tau) d\tau \quad (8.36) \\) 
*   **定义 8.4.1（误差函数与余误差函数）**：
    1. 满足积分形式：
       \\( \text{erf } x = \frac{2}{\sqrt{\pi}} \int_0^x e^{-\xi^2} d\xi \quad (8.44) \\) 
       的函数称为 **误差函数**。
    2. 满足积分形式：
       \\( \text{erfc } x = 1 - \text{erf } x = \frac{2}{\sqrt{\pi}} \int_x^\infty e^{-\xi^2} d\xi \quad (8.43) \\) 
       的函数称为 **余误差函数**。

---

### **三、 公式整理（按原文序号）**

*   **(8.1)** Laplace 变换（拉氏变换）积分定义式：
    \\( F(p) = \int_0^\infty e^{-pt} f(t) dt \\) 
*   **(8.2)** 像函数（拉氏换式）的算符表示：
    \\( F(p) = \mathcal{L} \{f(t)\} \quad \text{或} \quad F(p) \risingdotseq f(t) \\) 
*   **(8.3)** 原函数（反演）的算符表示：
    \\( f(t) = \mathcal{L}^{-1} \{F(p)\} \quad \text{或} \quad f(t) \fallingdotseq F(p) \\) 
*   **(8.4)** Heaviside 单位阶跃函数定义：
    \\( \eta (t) = \begin{cases} 1, & t > 0 \\ 0, & t < 0 \end{cases} \\) 
*   **(8.5)** 常数 1 的拉氏变换：
    \\( \mathcal{L} \{1\} = \int_0^\infty e^{-pt} dt = \frac{1}{p} \quad (\text{Re } p > 0) \\) 
*   **(8.6)** 指数函数的拉氏变换：
    \\( \mathcal{L} \{e^{at}\} = \int_0^\infty e^{-pt} e^{at} dt = \frac{1}{p-a} \quad (\text{Re } p > \text{Re } a) \\) 
*   **(8.7)** 原函数指数增长的充分条件估计：
    \\( |f(t)| < M e^{\beta' t} \\) 
*   **(8.8)** Laplace 变换的线性性质：
    \\( \mathcal{L} \{\alpha_1 f_1(t) + \alpha_2 f_2(t)\} = \alpha_1 F_1(p) + \alpha_2 F_2(p) \\) 
*   **(8.9)** 正弦与余弦函数的拉氏变换：
    \\( \mathcal{L} \{\sin \omega t\} = \frac{\omega}{p^2+\omega^2}, \quad \mathcal{L} \{\cos \omega t\} = \frac{p}{p^2+\omega^2} \\) 
*   **(8.10)** 收敛半平面内的绝对收敛积分估计：
    \\( \left| \int_0^\infty e^{-pt} f(t) dt \right| \le \int_0^\infty M e^{-\delta t} dt < \infty \quad (\text{其中 } \text{Re } p - s_0 \ge \delta > 0) \\) 
*   **(8.11)** 像函数在无穷远处的极限性质：
    \\( \lim_{\text{Re } p \to +\infty} F(p) = 0 \\) 
*   **(8.12)** 一阶导数的拉氏变换：
    \\( \mathcal{L} \{f'(t)\} = p F(p) - f(0) \\) 
*   **(8.13a)** 二阶导数的拉氏变换：
    \\( \mathcal{L} \{f''(t)\} = p^2 F(p) - p f(0) - f'(0) \\) 
*   **(8.13b)** 三阶导数的拉氏变换：
    \\( \mathcal{L} \{f^{(3)}(t)\} = p^3 F(p) - p^2 f(0) - p f'(0) - f''(0) \\) 
*   **(8.13c)** \\( n \\)  阶导数的拉氏变换：
    \\( \mathcal{L} \{f^{(n)}(t)\} = p^n F(p) - p^{n-1} f(0) - p^{n-2} f'(0) - \dots - f^{(n-1)}(0) \\) 
*   **(8.14a, b)** LR 串联电路的微分方程定解问题：
    \\( L \frac{di}{dt} + R i = E, \quad i(0) = 0 \\) 
*   **(8.15)** 电路方程变换后的代数方程：
    \\( L p I(p) + R I(p) = \frac{E}{p} \\) 
*   **(8.16)** 电流的反演解析解：
    \\( i(t) = \frac{E}{R} [1 - e^{-(R/L)t}] \\) 
*   **(8.17a, b)** 常微分方程边值定解问题：
    \\( y''(t) - y'(t) - 2y(t) = 0, \quad y(0) = 1, \quad y(t)|_{t \to \infty} \text{ 有界} \\) 
*   **(8.18)** 原函数积分的拉氏变换：
    \\( \mathcal{L}   \int_0^t f(\tau) d\tau   = \frac{F(p)}{p} \\) 
*   **(8.18')** 积分与导数的恒等关系式：
    \\( \int_0^\infty f(t) e^{-pt} dt = p \int_0^\infty g(t) e^{-pt} dt \quad \left( \text{其中 } g(t) = \int_0^t f(\tau) d\tau \right) \\) 
*   **(8.19a, b)** LC 串联电路的微分积分方程定解问题：
    \\( q(t) = C v_C(t), \quad q(t) = -\int_0^t i(\tau) d\tau + q(0) \\) 
*   **(8.20)** 并联电路电流像函数代数式：
    \\( I(p) = \frac{v_0/L}{p^2 + \frac{1}{LC}} \\) 
*   **(8.21)** 原函数多值反演的非唯一性对抗形式：
    \\( h_1(t) \risingdotseq F(p), \quad h_2(t) \risingdotseq F(p) \\) 
*   **(8.22)** 零函数积分等式：
    \\( g(t) = h_1(t) - h_2(t) \not\equiv 0, \quad g(t) \risingdotseq 0 \\) 
*   **(8.23)** 像函数导数的反演公式：
    \\( F^{(n)}(p) \risingdotseq (-t)^n f(t) \\) 
*   **(8.24)** 二阶倒数幂的反演：
    \\( \mathcal{L}^{-1}\frac{1}{p^2}= t \\) 
*   **(8.25)** 三阶倒数幂的反演：
    \\( \mathcal{L}^{-1} \frac{1}{p^3}  = \frac{1}{2} t^2 \\) 
*   **(8.26)** 有理分式部分分式展开式：
    \\( \frac{1}{p^3(p+a)} = \frac{1}{a p^3} - \frac{1}{a^2 p^2} + \frac{1}{a^3 p} - \frac{1}{a^3(p+a)} \\) 
*   **(8.27)** 像函数积分的反演公式：
    \\( \mathcal{L}^{-1}   \int_p^\infty F(q) dq   = \frac{f(t)}{t} \\) 
*   **(8.28)** 典型三角分式的拉氏变换：
    \\( \mathcal{L}  \frac{\sin \omega t}{t}  = \arctan \frac{\omega}{p} \\) 
*   **(8.29)** 像函数定积分与原函数的关系：
    \\( \int_0^\infty F(p) dp = \int_0^\infty \frac{f(t)}{t} dt \\) 
*   **(8.30)** 典型狄利克雷积分公式：
    \\( \int_0^\infty \frac{\sin \omega t}{t} dt = \frac{\pi}{2} \\) 
*   **(8.31)** 典型对数型积分计算公式：
    \\( \int_0^\infty \frac{e^{-at} - e^{-bt}}{t} dt = \ln \frac{b}{a} \\) 
*   **(8.32)** 像函数在 \\( p = \infty \\)  点的 Taylor 级数展开：
    \\( F(p) = \sum_{n=1}^\infty c_n p^{-n} \\) 
*   **(8.33)** 原函数的级数反演式：
    \\( f(t) = \sum_{n=1}^\infty \frac{c_n}{(n-1)!} t^{n-1} \\) 
*   **(8.34)** 零阶 Bessel 函数的拉氏变换反演关系：
    \\( \mathcal{L}^{-1}   \frac{1}{\sqrt{p^2+1}}   = J_0(t) = \sum_{k=0}^\infty \frac{(-1)^k}{(k!)^2} \left(\frac{t}{2}\right)^{2k} \\) 
*   **(8.35)** 零阶自变量 Bessel 变形反演：
    \\( \mathcal{L}^{-1}   \frac{1}{p} e^{-1/p}   = J_0(2\sqrt{t}) \\) 
*   **(8.36)** **卷积定理**：
    \\( \mathcal{L}\{f_1(t) * f_2(t)\} = F_1(p) F_2(p) \quad \left( \text{其中 } f_1(t) * f_2(t) = \int_0^t f_1(\tau) f_2(t-\tau) d\tau \right) \\) 
*   **(8.37)** 方形脉冲电压函数定义：
    \\( f_s(t) = \begin{cases} E_0, & 0 \le t \le T \\ 0, & t > T \end{cases} \\) 
*   **(8.38)** **普遍反演公式（Mellin 反演积分公式）**：
    \\( f(t) = \frac{1}{2\pi i} \int_{s-i\infty}^{s+i\infty} F(p) e^{pt} dp \quad (s > s_0) \\) 
*   **(8.39)** 像函数高阶分式反演积分示例：
    \\( \mathcal{L}^{-1}  \frac{1}{(p^2+\omega^2)^2}   = \frac{1}{2\pi i} \int_{s-i\infty}^{s+i\infty} \frac{e^{pt}}{(p^2+\omega^2)^2} dp = \frac{1}{2\omega^2} \left( \frac{\sin \omega t}{\omega} - t \cos \omega t \right) \\) 
*   **(8.40)** 多值函数的反演公式（例 8.8）：
    \\( \mathcal{L}^{-1}  \frac{1}{\sqrt{p}} e^{-a\sqrt{p}}   = \frac{1}{\sqrt{\pi t}} e^{-a^2/4t} \quad (a > 0) \\) 
*   **(8.41)** 原、像自变量开方变换公式：
    \\( \frac{1}{\sqrt{\pi t}} \int_0^\infty f(\tau) e^{-\tau^2/4t} d\tau \risingdotseq \frac{1}{\sqrt{p}} F(\sqrt{p}) \\) 
*   **(8.42)** 阶跃余误差变换对：
    \\( \mathcal{L}^{-1}  \frac{1}{p} e^{-a\sqrt{p}}   = \text{erfc}\left( \frac{a}{2\sqrt{t}} \right) \\) 
*   **(8.43)** 余误差函数（Complementary Error Function）定义：
    \\( \text{erfc } x = \frac{2}{\sqrt{\pi}} \int_x^\infty e^{-\xi^2} d\xi \\) 
*   **(8.44)** 误差函数（Error Function）定义：
    \\( \text{erf } x = \frac{2}{\sqrt{\pi}} \int_0^x e^{-\xi^2} d\xi \\) 
*   **(8.45)** 级数求和积分转换模型：
    \\( \sum_{n=1}^\infty F(n) = \int_0^\infty f(t) \left( \sum_{n=1}^\infty e^{-nt} \right) dt = \int_0^\infty \frac{f(t)}{e^t-1} dt \\) 
*   **(8.46)** 典型平方倒数和级数积分式（例 8.10）：
    \\( \sum_{n=1}^\infty \frac{1}{n^2} = \int_0^\infty \frac{x}{e^x-1} dx = \frac{\pi^2}{6} \\) 
*   **(8.47)** 四次方倒数和级数积分式（例 8.11）：
    \\( \sum_{n=1}^\infty \frac{1}{n^4} = \frac{1}{6}\int_0^\infty \frac{x^3}{e^x-1} dx = \frac{\pi^4}{90} \\) 
*   **(8.48)** 有理级数求和公式（例 8.12）：
    \\( \sum_{n=1}^\infty \frac{1}{n^2-a^2} = \frac{1}{2a^2} - \frac{\pi}{2a} \cot \pi a \\) 
*   **(8.48')** 级数的变形余切求和式：
    \\( \sum_{n=1}^\infty \frac{1}{n^2-a^2} = \frac{1}{2a^2} - \frac{\pi}{2a} \cot \pi a \\) 
*   **(8.49)** 双曲余切求和公式（纯虚数代换一）：
    \\( \sum_{n=1}^\infty \frac{1}{n^2+a^2} = -\frac{1}{2a^2} + \frac{\pi}{2a} \coth \pi a \\) 
*   **(8.49')** 双曲余切求和公式（纯虚数代换二）：
    \\( \sum_{n=1}^\infty \frac{1}{n^2+a^2} = -\frac{1}{2a^2} + \frac{\pi}{2a} \coth \pi a \\) 
*   **(8.50)** 含有对数的无穷级数求和式：
    \\( \sum_{n=1}^\infty \ln \left( 1 + \frac{a^2}{n^2} \right) = \ln \left( \frac{\sinh \pi a}{\pi a} \right) \\) 

---

⚡ 既然我们已经系统完成了第八章 Laplace 变换的公式、定义和内容总结，我们可以针对该章的核心，比如利用拉氏变换求解经典微分方程或电路定解问题（如 LR、LC 串联电路初值问题）的完整手写计算步骤进行一次深度拆解，您想看看吗？