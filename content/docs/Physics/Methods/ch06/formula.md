---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据您选定的第六章《留数定理及其应用》（对应源文件 `ch_6.pdf`）的内容，现为您整理本章的主要内容、按原文形式编排的所有定义以及按原文序号整理的所有公式。

---

### **一、 主要内容总结**

本章系统地论述了**留数理论**及其在复变积分和实变积分计算中的应用：
1.  **留数定理与留数计算**：定义了留数并证明了留数定理。针对孤立奇点（特别是一阶与高阶极点），给出了利用极限和求导计算留数的实用公式。
2.  **无穷远点留数**：将留数概念推广至无穷远点 \\( \infty \\)，探讨了其定义、计算方法及全体留数和为零的重要性质。
3.  **定积分的留数法计算**：
    *   **有理三角函数积分**：通过变换 \\( z = e^{i\theta} \\) 将区间 \\( [0, 2\pi] \\) 上的三角函数积分转化为单位圆周上的围道积分。
    *   **实轴无穷积分**：通过在上半平面补加大圆弧 \\( C_R \\) 构造闭合围道来计算实轴上的无穷积分。
    *   **含三角函数的无穷积分**：引入了 **Jordan 引理**和**补充引理**，通过构造 \\( e^{ipz} \\) 形式的被积函数来克服 \\( \infty \\) 作为本性奇点带来的计算困难。
4.  **积分路径上有奇点的情形**：讨论了积分路径上含有一阶极点（瑕点）时的处理方法，引入了**柯西主值（V.p.）**概念，并通过绕行小半圆弧 \\( C_\delta \\) 计算极限值。
5.  **多值函数的积分**：针对含有分支点（如 \\( z^s, \ln z \\)）的多值函数，通过引入割线（通常为正实轴）和特殊的割线围道（如匙孔形围道）来计算实数域内的积分。
6.  **特殊积分围道**：介绍了**哑铃型围道**（用于有限区间多值函数积分）和**矩形围道**（用于含有复周期指数函数的积分）。
7.  **无穷级数求和**：将留数定理应用于求和计算。通过构造正方形围道 \\( C_N \\) 及辅助函数 \\( \pi \cot \pi z \\)（在整数点处的留数均为 \\( 1 \\)），将级数求和问题转化为留数计算。

---

### **二、 定义整理（按定义 1.1.1 的 6.x.x 形式）**

*   **定义 6.1.1（留数）**：设 \\( z = b \\) 为函数 \\( f(z) \\) 的孤立奇点，称 \\( f(z) \\) 在 \\( z=b \\) 的空心邻域内 Laurent 展开式中 \\( (z-b)^{-1} \\) 项的系数 \\( a_{-1} \\) 为 \\( f(z) \\) 在 \\( b \\) 处的**留数**，记作 \\( \text{res } f(b) \\)。
*   **定义 6.1.2（无穷远点留数）**：若 \\( \infty \\) 是 \\( f(z) \\) 的孤立奇点，定义：
    \\( \text{res } f(\infty) = \frac{1}{2\pi i} \oint_{C'} f(z)dz \\)
    为 \\( f(z) \\) 在**无穷远点处的留数**，其中 \\( C' \\) 为绕 \\( \infty \\) 点正向（即顺时针方向）一周的简单封闭曲线。
*   **定义 6.3.1（柯西主值/积分主值）**：若无穷积分中对称极限 \\( \lim_{R \to +\infty} \int_{-R}^R f(x)dx \\) 存在，则称此极限为该积分的**柯西主值**，记作：
    \\( \text{V.p.} \int_{-\infty}^{\infty} f(x)dx = \lim_{R \to +\infty} \int_{-R}^R f(x)dx \quad \\)
*   **定义 6.5.1（瑕积分与瑕积分主值）**：若 \\( a < c < b \\) 且 \\( c \\) 是被积函数 \\( f(x) \\) 的瑕点，则积分 \\( \int_a^b f(x)dx \\) 称为**瑕积分**。若对称极限存在，则称其为**瑕积分的主值**，记作：
    \\( \text{V.p.} \int_a^b f(x)dx = \lim_{\delta \to 0} \left[ \int_a^{c-\delta} f(x)dx + \int_{c+\delta}^b f(x)dx \right] \quad \\)

---

### **三、 公式整理（按原文序号）**

*   **(6.1)** **留数定理积分公式**：
    \\( \oint_C f(z)dz = 2\pi i \sum_{k=1}^n \text{res } f(b_k) \quad \\)
*   **(6.2)** \\( m \\) 阶极点处的 Laurent 展开式：
    \\( f(z) = a_{-m}(z-b)^{-m} + a_{-m+1}(z-b)^{-m+1} + \dots + a_{-1}(z-b)^{-1} + a_0 + a_1(z-b) + \dots \quad \\)
*   **(6.3)** **\\( m \\) 阶极点留数计算公式**：
    \\( \text{res } f(b) = \frac{1}{(m-1)!} \lim_{z \to b} \frac{d^{m-1}}{dz^{m-1}} \left[ (z-b)^m f(z) \right] \quad \\)
*   **(6.4)** 一阶极点处的 Laurent 展开式：
    \\( f(z) = a_{-1}(z-b)^{-1} + a_0 + a_1(z-b) + a_2(z-b)^2 + \dots \quad \\)
*   **(6.5)** **一阶极点留数计算公式**：
    \\( \text{res } f(b) = \lim_{z \to b} (z-b)f(z) \quad \\)
*   **(6.6)** **分式型一阶极点留数公式**：
    \\( \text{res } f(b) = \lim_{z \to b} (z-b)\frac{P(z)}{Q(z)} = \frac{P(b)}{Q'(b)} \quad \\)
*   **(6.7)** 简单极点有理函数的部分分式待定形式：
    \\( \frac{1}{(z-1)(z-2)(z-3)} = \frac{A}{z-1} + \frac{B}{z-2} + \frac{C}{z-3} \quad \\)
*   **(6.8a)** 留数计算待定常数 \\( A \\)：
    \\( A = \text{res } f(1) = \frac{1}{2} \quad \\)
*   **(6.8b)** 留数计算待定常数 \\( B \\)：
    \\( B = \text{res } f(2) = -1 \quad \\)
*   **(6.8c)** 留数计算待定常数 \\( C \\)：
    \\( C = \text{res } f(3) = \frac{1}{2} \quad \\)
*   **(6.9)** 高阶极点有理函数的部分分式形式：
    \\( \frac{1}{(z-1)^2(z-2)(z-3)} = \frac{A}{(z-1)^2} + \frac{B}{z-1} + \frac{C}{z-2} + \frac{D}{z-3} \quad \\)
*   **(6.10a)** 系数 \\( A \\) 计算：
    \\( A = \left[ (z-1)^2 f(z) \right]\Big|_{z=1} = \frac{1}{2} \quad \\)
*   **(6.10b)** 留数系数 \\( B \\) 计算：
    \\( B = \text{res } f(1) = \frac{3}{4} \quad \\)
*   **(6.10c)** 系数 \\( C \\) 计算：
    \\( C = \text{res } f(2) = -1 \quad \\)
*   **(6.10d)** 系数 \\( D \\) 计算：
    \\( D = \text{res } f(3) = \frac{1}{4} \quad \\)
*   **(6.11)** **无穷远点留数定义式**：
    \\( \text{res } f(\infty) = \frac{1}{2\pi i} \oint_{C'} f(z)dz \quad \\)
*   **(6.12)** **无穷远点留数与展开系数关系**：
    \\( \text{res } f(\infty) = - \left[ f(z) \text{ 在 } z = \infty \text{ 邻域展开式中的 } z^{-1} \text{ 项系数} \right] \quad \\)
*   **(6.13)** 有理三角函数定积分通用形式：
    \\( I = \int_0^{2\pi} R(\sin\theta, \cos\theta)d\theta \quad \\)
*   **(6.14)** 三角函数积分转化复积分形式：
    \\( I = \oint_{|z|=1} R\left( \frac{z^2-1}{2iz}, \frac{z^2+1}{2z} \right) \frac{dz}{iz} \quad \\)
*   **(6.15)** 有理三角函数留数计算公式：
    \\( I = 2\pi \sum_{|z_k|<1} \text{res } \left\{ \frac{1}{z} R\left( \frac{z^2-1}{2iz}, \frac{z^2+1}{2z} \right) \right\} \quad \\)
*   **(6.16)** 无穷积分围道计算极限式：
    \\( \int_{-\infty}^{\infty} f(x)dx = \lim_{R \to \infty} \int_{-R}^R f(x)dx \quad \\)
*   **(6.17)** 无穷积分留数计算分解式：
    \\( \oint_C \frac{dz}{(1+z^2)^3} = \int_{-R}^R \frac{dx}{(1+x^2)^3} + \int_{C_R} \frac{dz}{(1+z^2)^3} = 2\pi i \cdot \text{res } \left\{ \frac{1}{(1+z^2)^3} \right\}\Big|_{z=i} \quad \\)
*   **(6.18)** 扇形积分围道计算分解式：
    \\( \oint_C \frac{dz}{1+z^4} = \int_0^R \frac{dx}{1+x^4} + \int_{C_R} \frac{dz}{1+z^4} + \int_R^0 \frac{idy}{1+(iy)^4} = 2\pi i \cdot \text{res } \left\{ \frac{1}{1+z^4} \right\}\Big|_{z=e^{i\pi/4}} \quad \\)
*   **(6.19)** 含有无穷多个奇点的上半平面无穷积分公式：
    \\( \int_{-\infty}^{\infty} f(x)dx = 2\pi i \sum_{n} \text{res } f(b_n) \quad \\)
*   **(6.20)** 傅里叶型有理无穷积分形式：
    \\( I = \int_{-\infty}^{\infty} f(x)\cos px \, dx \quad \text{或} \quad I = \int_{-\infty}^{\infty} f(x)\sin px \, dx \quad \\)
*   **(6.21)** **Jordan 引理关系式**：
    \\( \lim_{R \to \infty} \int_{C_R} Q(z)e^{ipz}dz = 0 \quad \\)
*   **(6.22)** 傅里叶型无穷积分示例计算结果：
    \\( \int_0^\infty \frac{x \sin x}{x^4+a^4} dx = \frac{\pi}{2a^2} e^{-a/\sqrt{2}} \sin \frac{a}{\sqrt{2}} \quad \\)
*   **(6.23)** 奇函数余弦傅里叶无穷积分为零性质：
    \\( \int_{-\infty}^{\infty} \frac{x \cos x}{x^4+a^4}dx = 0 \quad \\)
*   **(6.24a)** **下半平面一致趋于零时的留数积分（补充引理一）**：
    \\( \lim_{R \to \infty} \int_{C_R} Q(z)e^{-ipz}dz = 2\pi i \sum_{\text{下半平面}} \text{res } \{ Q(z)e^{-ipz} \} \quad \\)
*   **(6.24b)** **下半平面一致趋于零时的留数积分（补充引理二）**：
    \\( \lim_{R \to \infty} \int_{C_R} Q(z)e^{-ipz}dz = -2\pi i \cdot \text{res } \{ Q(z)e^{-ipz} \}_{z=\infty} \quad \\)
*   **(6.25)** 狄利克雷积分公式：
    \\( \int_{-\infty}^{\infty} \frac{\sin x}{x}dx = \pi \quad \\)
*   **(6.26)** 狄利克雷积分的高阶推广公式：
    \\( \int_{-\infty}^{\infty} \frac{\sin^n x}{x^n} dx = \frac{\pi}{2^{n-1}(n-1)!} \sum_{k=0}^{[n/2]} (-1)^k \binom{n}{k} (n-2k)^{n-1} \quad \\)
*   **(6.27)** 积分路径有奇点时的瑕积分围道方程：
    \\( \oint_C \frac{dz}{z(1+z+z^2)} = \int_{-R}^{-\delta} \frac{dx}{x(1+x+x^2)} + \int_{C_\delta} \frac{dz}{z(1+z+z^2)} + \int_{\delta}^R \frac{dx}{x(1+x+x^2)} + \int_{C_R} \frac{dz}{z(1+z+z^2)} = 2\pi i \cdot \text{res}\Big|_{z=e^{i2\pi/3}} \quad \\)
*   **(6.28)** 瑕积分柯西主值结果：
    \\( \text{V.p.} \int_{-\infty}^{\infty} \frac{dx}{x(1+x+x^2)} = -\frac{\pi}{\sqrt{3}} \quad \\)
*   **(6.29)** 利用绕行半圆直接求出的狄利克雷积分：
    \\( \int_{-\infty}^{\infty} \frac{\sin x}{x}dx = \pi \quad \\)
*   **(6.30)** 多值幂函数反常积分一般形式：
    \\( I = \int_0^{\infty} x^{s-1}Q(x)dx \quad \\)
*   **(6.31)** 割线匙孔围道多值积分分解式：
    \\( \oint_C \frac{z^{a-1}}{z+e^{i\phi}} dz = \int_\delta^R \frac{x^{a-1}}{x+e^{i\phi}} dx + \int_{C_R} + \int_{R}^\delta \frac{(xe^{i2\pi})^{a-1}}{xe^{i2\pi}+e^{i\phi}} dx + \int_{C_\delta} = 2\pi i \cdot \text{res}\Big|_{z=e^{i(\phi+\pi)}} \quad \\)
*   **(6.32)** 含有复参数的多值幂积分公式：
    \\( \int_0^{\infty} \frac{x^{a-1}}{x+e^{i\phi}} dx = \frac{\pi \sin(1-a)\phi}{\sin a\pi \sin \phi} \quad \\)
*   **(6.33)** 常用伽马函数性质相关多值积分：
    \\( \int_0^{\infty} \frac{x^{a-1}}{x+1} dx = \frac{\pi}{\sin a\pi} \quad \\)
*   **(6.34)** 二次型多值幂积分公式：
    \\( \int_0^{\infty} \frac{x^{a-1}}{x^2+2x\cos\phi+1} dx = \frac{\pi \sin(1-a)\phi}{\sin a\pi \sin \phi} \quad \\)
*   **(6.35)** 含有对数的多值围道积分公式：
    \\( \oint_C \frac{\ln z}{1+z+z^2} dz = \int_\delta^R \frac{\ln x}{1+x+x^2} dx + \int_{C_R} + \int_{R}^\delta \frac{\ln x + 2\pi i}{1+x+x^2} dx + \int_{C_\delta} = 2\pi i \left[ \text{res}\Big|_{e^{i2\pi/3}} + \text{res}\Big|_{e^{i4\pi/3}} \right] \quad \\)
*   **(6.36)** 无理分式代数积分结果：
    \\( \int_0^{\infty} \frac{dx}{1+x+x^2} = \frac{2\pi}{3\sqrt{3}} \quad \\)
*   **(6.37)** 常用对数对称积分为零公式：
    \\( \int_0^{\infty} \frac{\ln x}{1+x+x^2} dx = 0 \quad \\)
*   **(6.38)** 哑铃型围道积分示例结果：
    \\( \int_0^1 \frac{\sqrt{x(1-x)^2}}{(1+x)^3}dx = \frac{3\pi \sqrt{3}}{64 \cdot 2^{2/3}} \quad \\)
*   **(6.39)** 矩形围道指数型积分公式：
    \\( \int_{-\infty}^{\infty} \frac{e^{ax}}{1+e^x} dx = \frac{\pi}{\sin a\pi} \quad \\)
*   **(6.40)** 正方形级数积分围道极限：
    \\( \lim_{N \to \infty} \oint_{C_N} \pi \cot \pi z f(z) dz = 0 \quad \\)
*   **(6.41)** **级数求和留数计算公式**：
    \\( \sum_{n=-\infty}^{\infty} f(n) = -\sum \text{res } \{ \pi \cot \pi z f(z) \} \quad \text{（在 } f(z) \text{ 的极点处）} \quad \\)
*   **(6.42)** 级数与围道留数定理平衡关系式：
    \\( \oint_{C_N} \pi \cot \pi z f(z) dz = 2\pi i \left[ \sum_{n=-N}^N f(n) + \sum \text{res } \{ \pi \cot \pi z f(z) \} \right] \quad \\)
*   **(6.43)** 巴塞尔问题（平方倒数和）结果：
    \\( \sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6} \quad \\)

---

💡 既然我们已经将《数学物理方法》前六章（即整个**复变函数论部分**）的所有符号、定义、定理和核心公式整理完毕，它们构成了您期末复习或科研的核心基础。要不要我帮您将这些高频考点和公式打包，生成一份排版精美、便于打印的 **《复变函数基础公式与定理期末复习速查 PDF 手册》**？