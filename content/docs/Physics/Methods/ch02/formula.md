---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据源文件《第二章 解析函数》的内容，现按照您的要求将主要内容、公式（按原文序号）及定义（按 2.x.x 形式）整理如下：

### **一、 主要内容总结**
本章系统阐述了复变函数微积分的基础理论，重点是**解析函数**的性质及其应用。
1.  **极限与连续**：将实变函数的极限与连续概念扩展至复域，并探讨了有界闭区域内连续函数的性质（如一致连续性）,。
2.  **导数与微分**：定义了复变函数的导数，强调了复平面内趋近方式的任意性，并导出了**Cauchy-Riemann (C-R) 条件**作为可导的必要条件,。
3.  **解析函数**：定义了在区域内处处可导的函数为解析函数，证明了其虚实部互为**共轭调和函数**且满足 Laplace 方程,。
4.  **初等函数**：详细讨论了幂函数、指数函数、三角函数和双曲函数在复域中的定义、周期性及导数关系,,。
5.  **保角性**：从几何角度解释了导数的意义，阐明了解析映射具有保持角度和伸缩率不变的性质，并展示了其在简化物理方程（如 Laplace 方程）中的作用,。
6.  **多值函数**：深入探讨了根式函数和对数函数的多值性来源，引入了**分支点**、**割线**、**单值分支**及 **Riemann 面**等关键概念,,。

---

### **二、 定义整理（按指定格式）**

*   **定义 2.1.1（极限）**：若对于任意 \\( \epsilon > 0 \\)，存在 \\( \delta(\epsilon) > 0 \\)，当 \\( 0 < |z - z_0| < \delta \\) 时恒有 \\( |f(z) - A| < \epsilon \\)，则称 \\( z \to z_0 \\) 时 \\( f(z) \\) 的极限为 \\( A \\)。
*   **定义 2.1.2（连续）**：若函数 \\( f(z) \\) 在 \\( z_0 \\) 点的极限值等于在该点的函数值 \\( f(z_0) \\)，则称 \\( f(z) \\) 在 \\( z_0 \\) 点连续。
*   **定义 2.1.3（一致连续）**：对于任意 \\( \epsilon > 0 \\)，存在 \\( \delta(\epsilon) > 0 \\)，使得对于区域内任意两点 \\( z_1, z_2 \\)，只要 \\( |z_1 - z_2| < \delta \\)，就有 \\( |f(z_1) - f(z_2)| < \epsilon \\)。
*   **定义 2.2.1（可导）**：若极限 \\( \lim_{\Delta z \to 0} \frac{f(z+\Delta z) - f(z)}{\Delta z} \\) 存在且为有限值，则称函数 \\( f(z) \\) 在 \\( z \\) 点可导。
*   **定义 2.2.2（微分）**：函数改变量的线性部分 \\( f'(z)dz \\) 称为函数在 \\( z \\) 点的微分,。
*   **定义 2.3.1（解析函数）**：在区域 \\( G \\) 内每一点都可导的函数，称为 \\( G \\) 内的解析函数。
*   **定义 2.3.2（调和函数）**：满足二维 Laplace 方程 \\( \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0 \\) 的函数。
*   **定义 2.5.1（保角映射）**：在解析映射下，过同一点的两条曲线夹角保持不变，且伸缩率相同的变换。
*   **定义 2.6.1（多值函数）**：对于区域内的复数 \\( z \\)，有多个复数 \\( w \\) 与之对应的对应关系。
*   **定义 2.6.2（分支点）**：若 \\( z \\) 绕某点一圈回到原处时，\\( w \\) 值不能还原，则该点称为多值函数的分支点。
*   **定义 2.6.3（单值分支）**：通过限制宗量辐角变化范围，使得多值函数在定义域内唯一确定的单值函数。

---

### **三、 公式整理（按原文序号）**

*   **(2.1)** 导数定义：\\( f'(z) = \lim_{\Delta z \to 0} \frac{\Delta w}{\Delta z} = \lim_{\Delta z \to 0} \frac{f(z+\Delta z) - f(z)}{\Delta z} \\)
*   **(2.2)** Cauchy-Riemann 条件：\\( \frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x} \\)
*   **(2.3)** 微分表达式：\\( dw = f'(z_0)dz \\)
*   **(2.4)** 族曲线正交条件：\\( \frac{\partial u}{\partial x}\frac{\partial v}{\partial x} + \frac{\partial u}{\partial y}\frac{\partial v}{\partial y} = 0 \\)
*   **(2.5)** Laplace 方程：\\( \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0, \quad \frac{\partial^2 v}{\partial x^2} + \frac{\partial^2 v}{\partial y^2} = 0 \\)
*   **(2.6)** 复三角函数定义：\\( \sin z = \frac{e^{iz} - e^{-iz}}{2i}, \quad \cos z = \frac{e^{iz} + e^{-iz}}{2} \\),
*   **(2.7)** 复双曲函数定义：\\( \sinh z = \frac{e^z - e^{-z}}{2}, \quad \cosh z = \frac{e^z + e^{-z}}{2} \\)
*   **(2.8)** 双曲函数导数：\\( (\sinh z)' = \cosh z, \quad (\cosh z)' = \sinh z, \quad (\tanh z)' = \text{sech}^2 z \\)
*   **(2.9)** 算符变换中间项（链式法则结果之和）,
*   **(2.10)** 二维 Laplace 算符变换：\\( \nabla_{xy}^2 = |f'(z)|^2 \nabla_{\xi\eta}^2 \\)
*   **(2.11)** 区域 \\( G \\) 内的 Laplace 方程：\\( (\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2})u(x,y) = 0 \\)
*   **(2.12)** 变换后的 Laplace 方程：\\( (\frac{\partial^2}{\partial \xi^2} + \frac{\partial^2}{\partial \eta^2})u(\xi, \eta) = 0 \\)
*   **(2.13)** 二维 Poisson 方程：\\( (\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2})u(x,y) = \rho(x,y) \\)
*   **(2.14)** 变换后的 Poisson 方程：\\( (\frac{\partial^2}{\partial \xi^2} + \frac{\partial^2}{\partial \eta^2})u(\xi, \eta) = \frac{\rho(\xi, \eta)}{|f'(z)|^2} \\)
*   **(2.15)** Helmholtz 方程变换形式
*   **(2.17)** 平方根定义式：\\( w^2 = z - a \\)
*   **(2.18)** 根式函数表示：\\( w = \sqrt{z-a} \\)
*   **(2.19)** 根式函数的模与辐角：\\( |w| = \sqrt{|z-a|}, \quad \arg w = \frac{1}{2}\arg(z-a) \\)
*   **(2.20)** 对数函数定义：\\( \ln z = \ln |z| + i(\theta + 2n\pi) \\)
*   **(2.21)** 对数函数导数：\\( (\ln z)' = \frac{1}{z} \\)
*   **(2.22)** 反正弦函数：\\( \arcsin z = -i \ln(iz + \sqrt{1-z^2}) \\)
*   **(2.23)** 反余弦函数：\\( \arccos z = -i \ln(z + \sqrt{z^2-1}) \\)
*   **(2.24)** 反正切函数：\\( \arctan z = \frac{1}{2i} \ln \frac{1+iz}{1-iz} \\)
*   **(2.25)** 一般幂函数定义：\\( z^\alpha = e^{alpha \ln z} \\)