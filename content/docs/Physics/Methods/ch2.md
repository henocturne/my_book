---
title: "ch2_解析函数"
weight: 1
---
{{< katex display=true >}}
{{< /katex >}}

根据《数学物理方法（第三版）》第二章“解析函数”的内容，按照原文公式序号整理如下：

### 一、 导数与 Cauchy-Riemann 条件
*   **(2.1) 导数定义**：$f^{\prime}(z) = \lim_{\Delta z\rightarrow0}\frac{f(z+\Delta z)-f(z)}{\Delta z}$。
*   **(2.2) Cauchy-Riemann 条件**：$\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}, \frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}$。
*   **(2.3) 微分表达式**：$dw=f^{\prime}(z_{0})dz$ 或 $\frac{dw}{dz}|_{z=z_0}=f^{\prime}(z_0)$。

### 二、 解析函数的几何性质
*   **(2.4) 正交性**：解析函数的实部 $u$ 和虚部 $v$ 的等值曲线族互相正交：$\frac{\partial u}{\partial y}\frac{\partial v}{\partial y}+\frac{\partial u}{\partial x}\frac{\partial v}{\partial x}=0$。
*   **(2.5) Laplace 方程**：解析函数的实部和虚部都是调和函数，满足 $\frac{\partial^{2}u}{\partial x^{2}}+\frac{\partial^{2}u}{\partial y^{2}}=0$ 和 $\frac{\partial^{2}v}{\partial x^{2}}+\frac{\partial^{2}v}{\partial y^{2}}=0$。

### 三、 初等解析函数
*   **(2.6) 复三角函数定义**：$\sin z=\frac{e^{iz}-e^{-iz}}{2i}, \cos z=\frac{e^{iz}+e^{-iz}}{2}$。
*   **(2.7) 双曲函数定义**：包括 $\sinh z, \cosh z, \tanh z$ 等，由指数函数定义。
*   **(2.8) 双曲函数恒等式**：如 $\cosh^{2}z-\sinh^{2}z=1$ 等性质。

### 四、 保角变换下的算符变换
*   **(2.9) Laplace 算符定义**：$\nabla^{2}=\frac{\partial^{2}}{\partial x^{2}}+\frac{\partial^{2}}{\partial y^{2}}$。
*   **(2.10) 算符变换关系**：在保角变换 $\zeta=f(z)$ 下，$\nabla^{2}=|f^{\prime}(z)|^{2}(\frac{\partial^{2}}{\partial\xi^{2}}+\frac{\partial^{2}}{\partial\eta^{2}})$。
*   **(2.11) 变换后的 Laplace 方程**：仍保持形式不变。
*   **(2.12) & (2.13) Poisson 方程变换**：变换后的非齐次项变为 $\frac{1}{|f^{\prime}(z)|^{2}}\rho$。
*   **(2.14) 面积元变换**：$dxdy=|f^{\prime}(z)|^{-2}d\xi d\eta$。
*   **(2.15) & (2.16) Helmholtz 方程变换**：常数项 $k^2$ 变为 $\frac{k^{2}}{|f^{\prime}(z)|^{2}}$。

### 五、 多值函数
*   **(2.17) & (2.18) 根式定义**：$w^{2}=z-a$ 或 $w=\sqrt{z-a}$。
*   **(2.19) 根式的单值分支规定**：$|w|=\sqrt{|z-a|}, \arg w=\frac{1}{2}\arg(z-a)$。
*   **(2.20) 对数函数定义**：$\ln z=\ln|z|+i\arg z = \ln|z|+i(\theta+2n\pi)$。
*   **(2.21) 对数函数导数**：$\frac{d}{dz}(\ln z)=\frac{1}{z}$。
*   **(2.22) 至 (2.24) 反三角函数**：通过对数和根式定义的 $\arcsin z, \arccos z, \arctan z$。
*   **(2.25) 一般幂函数**：$z^{\alpha}=e^{\alpha \ln z}$。



在第二章中，作者通过极限、导数、解析性以及保角变换等概念，构建了复变函数微积分的基础。以下是根据各小节内容整理的核心定理与数学性质：

### §2.1 复变函数的极限和连续
本节确立了连续函数在有界闭区域 $\overline{G}$ 上的两个核心性质：
*   **有界性定理**：若 $f(z)$ 在 $\overline{G}$ 上连续，则 $|f(z)|$ 在该区域内有界，并能达到其上界和下界。
*   **一致连续性定理**：在有界闭区域 $\overline{G}$ 上连续的函数在该区域内必一致连续。

### §2.2 可导与可微
*   **可导的必要条件（Cauchy-Riemann 条件）**：若 $f(z) = u + iv$ 在点 $z$ 可导，则其实部 $u$ 和虚部 $v$ 的偏导数必满足 $\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}$ 和 $\frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}$。
*   **可导的充分条件**：若 $u(x,y)$ 和 $v(x,y)$ 在点 $(x,y)$ 可微且满足 C-R 条件，则 $f(z)$ 在该点可导。
*   **导数与连续性的关系**：函数在某点可导必在该点连续，但连续不一定可导。
*   **可微与可导等价性**：在复变函数中，函数在某点可微与可导是互为充要条件的。

### §2.3 解析函数
*   **调和性定理**：解析函数的实部 $u$ 和虚部 $v$ 都是调和函数，即它们都满足二维 Laplace 方程,。
*   **共轭调和性质**：解析函数的实部和虚部构成一对共轭调和函数，已知其中一个可唯一确定另一个（相差一个常数）,。
*   **几何正交性**：解析函数的实部等值线族 $u(x,y)=C_1$ 与虚部等值线族 $v(x,y)=C_2$ 互相正交。

### §2.4 初等函数
本节主要通过性质定义了复域下的初等函数，并明确了其解析区域：
*   **解析域判定**：多项式在全平面解析；指数函数 $e^z$、正弦函数 $\sin z$ 和余弦函数 $\cos z$ 均在整个复平面 $\mathbb{C}$ 内解析,,。
*   **周期性性质**：复指数函数具有虚周期 $2\pi i$；双曲函数的周期性可由三角函数推导出,。

### §2.5 解析函数的保角性
*   **保角映射定理**：在 $f'(z) \neq 0$ 的点，解析函数所代表的变换具有保角性（夹角保持不变）和伸缩比例的不变性。
*   **Riemann 映射定理**：任何有界单连通区域 $G$ 都可以通过解析函数双向单值地映射到另一个单连通区域 $G'$。
*   **算符变换定理**：在保角变换 $\zeta = f(z)$ 下，二维 Laplace 方程、Poisson 方程和 Helmholtz 方程的形式保持不变,,。

### §2.6 多值函数
*   **单值化准则**：通过在分支点（如 $z=a$ 和 $z=\infty$）之间作割线并限制宗量辐角范围，可将多值函数划分为若干单值分支，每个分支在割开的平面内是解析的,。
*   **对数函数导数公式**：在每一个单值分支内，对数函数均满足 $\frac{d}{dz}(\ln z) = \frac{1}{z}$。

